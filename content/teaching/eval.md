+++
# A Recent and Upcoming Talks section created with the Pages widget.
# This section displays recent talks from `content/talk/`.

widget = "custom"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 2  # Order that this section will appear.

title = "Gender Gap in Computing"
subtitle = ""

[content]
  # Page type to display. E.g. post, talk, or publication.
  page_type = "talk"
  
  # Choose how much pages you would like to display (0 = all pages)
  count = 5
  
  # Choose how many pages you would like to offset by
  offset = 0

  # Page order. Descending (desc) or ascending (asc) date.
  order = "desc"

  # Filter posts by a taxonomy term.
  [content.filters]
    tag = ""
    category = ""
    publication_type = ""
    exclude_featured = false
    exclude_past = false
    exclude_future = false
    
[design]
  # Toggle between the various page layout types.
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   4 = Citation (publication only)
  view = 2
  
[design.background]
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.

  # Background color.
  # color = "navy"
  
  # Background gradient.
  # gradient_start = "DeepSkyBlue"
  # gradient_end = "SkyBlue"
  
  # Background image.
  image = "headers/eigenvector_no_frame.png"  # Name of image in `static/img/`.
  image_darken = 0.0  # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
  image_size = "actual"  #  Options are `cover` (default), `contain`, or `actual` size.
  image_position = "center"  # Options include `left`, `center` (default), or `right`.
  image_parallax = true  # Use a fun parallax-like fixed background effect? true/false
  
[advanced]
 # Custom CSS. 
 css_style = ""
 
 # CSS class.
 css_class = ""
+++

Starting in Winter 2021, I began to measure the effectiveness of my course in narrowing the  [known gender gap](https://www.computerscience.org/resources/women-in-computer-science/#:~:text=According%20to%20the%20American%20Association%20of%20University%20Women%2C%20computer%20science,94%25%20of%20what%20men%20earn.&text=Only%2020%25%20of%20computer%20science%20professionals%20are%20women.) in computing.  Below is a table highlighting some of my findings; click [here](/img/resources/W21-eval.png) for a graph of full results. Percentages indicate the fraction of respondents who **agreed** or **strongly agreed** with the supplied statement. 32 female and 31 male students completed both the Entrance and the Exit surveys. 

| Question | Gender | Entrance | Exit | 
| -------  |--- |-----|--------| 
| If I wanted to, I could have a career that involved computer programming. | F | 64% | 80% |  
| | M | 82% | 88% | 
| If I wanted to, I could have a career that involved data science or machine learning. | F | 70% | 87% |  
| | M | 82% | 94% | 
| I can see connections between computer programming and my long-term career goals. | F | 87% | 97% |  
| | M | 97% | 97% | 
| Computer programming is fun. | F | 85% | 97% |  
| | M | 94% | 100% | 
| I feel comfortable writing about how my code works. | F | 67% | 97% |  
| | M | 88% | 97% | 
| I feel comfortable when explaining my thought process to others. | F | 58% | 93% |  
| | M | 85% | 100% | 

Students' tendency to agree with most of the supplied statements increased over the course of the class, with larger increases among female students. Students who take my class---especially women---leave with strengthened convictions that: 

- They have the power to choose a career in computing. 
- Computing is an enjoyable and relevant activity. 
- They are able to effectively communicate about code, both alone and in groups. 

Currently, I am working on both improving this evaluation tool and leveraging these insights to further develop my teaching activities toward equity and inclusion. 

