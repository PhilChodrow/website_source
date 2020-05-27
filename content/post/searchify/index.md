---
title: "Creating Domain-Specific Search URLs with R"
subtitle: ""
summary: ""
authors: [phil]
tags: [R]
categories: []
date: 2020-05-27T08:56:28-04:00
lastmod: 2020-05-27T08:56:28-04:00
featured: false
draft: false
share: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

I recently started on a project in which we need to generate a large number of URLs corresponding to Google searches. We're hoping that the information we want will be in one of the top returned search results, and we'll crowdsource the step of actually retrieving that information from the URLs. 

Crowd-sourcing isn't perfect, and we'll have the highest rate of success if we can help our crowdsourcers zero in on the information with a fairly specific search. In our case, we are trying to retrieve information from a large number of American institutions of higher learning -- we want one page of results for each college or university. 

With this in mind, I wrote some simple code in `R` that makes it easy to automatically form URLs of search results from colloquial input. The intensive work that the team behind the [Tidyverse](https://www.tidyverse.org/) ecosystem, and especially the [`rvest`](https://github.com/tidyverse/rvest) package really shows here. I have no experience interacting programmatically with websites, and yet I was able to code up a functional solution here before I was done with my first cup of morning tea. 

The first function uses Bing (yes, Bing!) to attempt to find out the URL of a college from a colloquial search. 

```r
library(tidyverse)
library(rvest)
library(stringr)

edufy <- function(name){
	out <- name %>% 
		str_replace_all(" ", "+") %>% 
		paste0('https://www.bing.com/search?q=', .) %>% 
		read_html() %>% 
		html_nodes("cite") %>% 
		xml_text() %>% 
		purrr::keep(str_detect(., 'edu'))
	
	if(length(out) == 0){
		return(NaN)
	}
	else{
		return(out[[1]])
	}
} 
```

The function `edufy()` first searches Bing for the colloquial `name` of an institution, and then returns the first .edu domain it finds. The assumption here is that, among all .edu domains found by a reasonable search, the institution's official webpage should usually be first on the list. Here's some examples: 

```r
> c("Swarthmore", "MIT", "UCLA") %>% map_chr(edufy)

[1] "https://www.swarthmore.edu" "web.mit.edu" "www.ucla.edu"
```

There's some variability in the form of the addresses returned by `edufy()` -- for example, Swarthmore's contains the `https://` prefix, while the others don't. But all three work on recent versions of Chrome and Safari. 

It's now easy to construct domain-specific search URLs:

```r
google_searchify <- function(edu, search_terms){
	domain_prefix <- "https://www.google.com/search?q=site%3A"
	search_terms <- search_terms %>% 
		str_replace_all(" ", "+")
	paste0(domain_prefix, edu, "+", search_terms)
}
```

This function ouputs the URL of a Google search for the `search_terms` within the domain specified by `edu`. 
For example, we can get the URLs of searches for "NinjaGram Charities" for Swarthmore, MIT, and UCLA: 

```r
> c("Swarthmore", "MIT", "UCLA") %>% 
+   map_chr(edufy) %>% 
+   map_chr(google_searchify, search_terms = "NinjaGram Charities")

[1] "https://www.google.com/search?q=site%3Ahttps://www.swarthmore.edu+NinjaGram+Charities"
[2] "https://www.google.com/search?q=site%3Aweb.mit.edu+NinjaGram+Charities"               
[3] "https://www.google.com/search?q=site%3Awww.ucla.edu+NinjaGram+Charities"           
```

If we then paste the first result into the browser, we'll see this: 

![](search_illustration.png)

Looks good! Only the first returned URL will return any search results, because, much to my shame, I never successfully established NinjaGram at MIT. UCLA is TBD...

