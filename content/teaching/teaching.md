+++
# A Recent and Upcoming Talks section created with the Pages widget.
# This section displays recent talks from `content/talk/`.

widget = "custom"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 70  # Order that this section will appear.

title = "Teaching"
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

My goal as a teacher is to make mathematical reasoning and quantitative problem-solving accessible to all students. I consistently gather data about my teaching, and use it to assess the accessibility and relevance of my offerings. I am especially interested in inclusive teaching practices for ameliorating race and gender disparities in applied mathematics and data science. 

<!-- Some educational techniques I'm excited about include: 

- **Learning micro-communities**. Especially during the isolating time of COVID-19, I aim to build small, persistent groups of students who can offer support and act as witnesses to the learning of their peers. 
- **Flipped classrooms**. The theory is simple: the critical time in a student's learning journey comes when they are actively solving problems. Flipped methodologies allow me to prioritize this active time, while simultaneously giving students flexibility on how my course fits into their schedules. 
- **[Mastery grading](https://www.masterygrading.com/)**. Mastery grading is an assessment methodology that promotes high standards, clear communication, and student control over their journey through the course. *This is a new technique for me,* and I am still learning more. I aim to implement it in PIC16B starting in Fall 2021.  -->

If you'd like, you can read some [nice things my students have said about me](/feedback).  

## Gender Gap in Computing

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

# Courses at UCLA




**[PIC16A](https://philchodrow.github.io/PIC16A/):** **Python with Applications I.** A flipped-classroom, team-based course focusing on Python basics and technical computing. Special emphasis on techniques for data science and machine learning.
- Taught in Fall 2020, Winter 2021, Spring 2021. 
  - [Current syllabus](https://philchodrow.github.io/PIC16A/syllabus/)
  - [Sample homework](https://nbviewer.jupyter.org/github/PhilChodrow/PIC16A/blob/master/homework/HW6.ipynb)
  - Sample lecture on handwritten digit classification: [video](https://www.youtube.com/watch?v=H6YG4HMAZPU) and [notes](https://youtu.be/H6YG4HMAZPU). 
  - Final Exam, Winter 2021 (mean score: 93%)
    - [Problem 1](https://nbviewer.jupyter.org/github/PhilChodrow/PIC16A/blob/master/prior_exams/W21/final/P1.ipynb)
    - [Problem 2](https://nbviewer.jupyter.org/github/PhilChodrow/PIC16A/blob/master/prior_exams/W21/final/P2.ipynb)
  - Narrowing the gender gap: [custom evaluation](#gender-gap-in-computing). 
- Scheduled for Fall 2021.

**[PIC16B](https://philchodrow.github.io/PIC16B/):** **Python with Applications II.** A project-based course in advanced technical computing and data science with Python. Topics include data analysis and acquisition; numerical programming; machine learning via TensorFlow; natural language processing; and network science.
- Taught in Spring 2021
  - [Current syllabus](https://philchodrow.github.io/PIC16B/syllabus/)
  - [Sample homework](https://nbviewer.jupyter.org/github/PhilChodrow/PIC16B/blob/master/HW/spectral-clustering.ipynb)
  - [Project prompt](https://philchodrow.github.io/PIC16B/project/)
- Scheduled for Fall 2021 and Winter 2022. 

**MATH 168**: An upper division course in the mathematics of network science. To cover topics including measuring networks, random graph models, learning tasks on networks, and dynamical systems on networks. 
- Scheduled for Spring, 2022. 



# Before UCLA

This page is devoted to my teaching at UCLA. For my teaching history, including assistantships at MIT and other experience, please consult my [CV](https://philchodrow.github.io/CV/cv.pdf). 



<!-- # MIT

### 2019-20

- 15.S60: Computing in Optimization and Statistics (session instructor, PhD level)
- 15.003: Analytics Tools (organizer, instructor, master's level)

### 2018-19

- 15.S60: Computing in Optimization and Statistics (organizer, session instructor, PhD level)
- 15.003: Analytics Tools (organizer, instructor, master's level)

### 2017-18 

- 6.268, Network Science and Models (head TA, PhD level)
- 6.431, Introduction to Probability (TA, undergrad + master's level)
- 15.S60: Computing in Optimization and Statistics (organizer, session instructor, PhD level)
- 15.003: Analytics Tools (organizer, instructor, master's level)

### 2016-17

- 1.204, Computer Modeling: From Individual Mobility to Networks  (head TA, PhD level)


# Before MIT

- The Philosophy of Action, (TA, master's level, University of Oslo, 2012)
- The Philosophy of Plato (TA, Swarthmore College)
- Senior Thesis Mentor
- Writing Mentor
- Mathematics Academic Support

# Aikido

I have also been privileged to teach the traditional Japanese martial art of Aikido for several dojos in the Boston area, including Aikido Tekkojuku, Harvard Aikikai, and New England Aikikai. 





 -->
