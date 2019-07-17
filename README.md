# The .csv's

A .csv file already exists for each file that needs to be annotated. For example, `2015 002 08-30-15 LAURIER D @ YORK O.csv` will already contain the fields:  
* **camera_view**: denotes if the camera is from the sideline (SL) or endzone (EZ)
* **mark_in**: denotes the frame number of when the clip begins
* **duration**: denotes how many frames long the clip is

![alt text](csv_before.png)

I need you to add two new fields:  
* **snap**: denotes the frame number of when the ball is snapped (when the play starts)
* **play_type**: denotes the type of play, usually if it was a run or pass play

![alt text](csv_after.png)

### camera_view

You will see each play twice, back-to-back. First you will see it from the side (SL) and then you will see it from the end (EZ).

SL stands for sideline and is the same view you would get if you watched a game of football on t.v.:

![alt text](sidecut_example.jpeg)

EZ stands for endzone and is the view you get when a camera is placed in the endzone:

![alt text](endcut_example.jpeg)

These fields are already filled in for you, but make sure that you fill the `play_type` field the same for each SL-EZ pair since the play is the same no matter what the camera angle is.

## Snap field

For determining when a snap occurs, try to get the frame where the center has hiked the ball completely and the offensive line has just started to move. Sometimes you will get a clear view of the center which makes this pretty easy:

![](clear_snap.gif)

Other times your view of the ball is not so clear. In these cases you just simply do your best by going off of when the offensive line starts to move:

![](test_gif.gif)

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/nicohiggs/football_annotations/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/nicohiggs/football_annotations/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
