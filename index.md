# Stats 220 Assignment 1 2022

![spongebob meme](my_meme.png)

## How I created the meme
```r
library(magick)

#Title
title <- image_blank(width = 802,
                     height = 50,
                     color = "#000000") %>%
  image_annotate(text = "My meme",
                 color = "#FFFFFF",
                 size = 48,
                 font = "Impact",
                 gravity = "center")
# Top left panel
panel1 <- image_read("../Assignment1/Images/Meme1.png") %>%
  image_scale(400) %>%
  image_annotate(text = "Welcome to the Salty\nSpitoon. How tough are ya?",
                 color = "#FFFFFF",
                 size = 24,
                 font = "Impact",
                 gravity = "NorthEast" ) %>%
  image_annotate(text = "How tough am I?",
                 color = "#FFFFFF",
                 size = 24,
                 font = "Impact",
                 location = geometry_point(20, 220) )
#Top right panel 
panel2 <- image_read("../Assignment1/Images/Meme2.png") %>%
  image_scale(402) %>%
  image_annotate(text = "Yeah, so?",
                 color = "#FFFFFF",
                 size = 24,
                 font = "Impact",
                 location = geometry_point(250, 50)) %>%
  image_annotate(text = "I finished the Stats 220\nAssignment 1 in one day",
                 color = "#FFFFFF",
                 size = 20,
                 font = "Impact",
                 location = geometry_point(5, 200))
#Bottom left panel
panel3 <- image_read("../Assignment1/Images/Meme3.png") %>%
  image_scale(402) %>%
  image_annotate(text = "Without looking back\nat the lab tasks",
                 color = "#FFFFFF",
                 size = 36,
                 font = "Impact",
                 location = geometry_point(50, 20))

#Bottom right panel
panel4 <- image_read("../Assignment1/Images/Meme4.png") %>%
  image_scale(400) %>%
  image_annotate(text = "Uh... Right this way sir!",
                 color = "#FFFFFF",
                 size = 24,
                 font = "Impact",
                 location = geometry_point(150, 220))

top_row <- image_append(c(panel1, panel2))
bottom_row <- image_append(c(panel3, panel4))
meme_panel <- image_append(c(title, top_row, bottom_row), stack = TRUE) %>%
  image_scale (400)

image_write(meme_panel, "my_meme.png")
```
## Meme Information

In this section, I'll be looking at explaining the following: 
* What my motivation was for making the meme 
* How my meme is original 
* Challenges I faced when making the meme 

### Motivation
I'll be honest. This was an assignment. It had to be done. However, I found that this was as good opportunity to practice the skills learnt in class and in the lab tasks. I soon got stuck in and found myself really enjoying the coding process so that was a motivator as well, to be able to see a finished product. 

### Is it original?
While this memepays homage to the famous "Spongebob tries to enter the Salty Spitoon" meme, I've taken liberties to bring it into modern times. It provides social commentary through a localised topic that everyone in this course is familiar with, the course. It also looks to tackle the the social issue of learning to code and depicts a heirachy where those who ***know how to code*** are given easier passage through life. 

### Challenges faced 
There were quite a few here as I tried to embody the meme and **not** look at the lab tasks. For the most part, this worked and I found it reinforced what I knew. However, some of the syntax threw me, especially the text placement as the method we learnt was fairly restricted in terms of where the text could go. I did get to learn some interesting syntax because of this though

## Thank you for coming to my TED talk
