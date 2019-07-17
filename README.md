# The .csv's

A .csv file already exists for each video that needs to be annotated. For example, `2015 002 08-30-15 LAURIER D @ YORK O.csv` will already contain the fields:  
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

### snap

For determining when the snap occurs (when the play begins), try to get the frame where the center has hiked the ball completely through his legs and the offensive line has just started to move. Sometimes you will get a clear view of the center which makes this pretty easy:

![](clear_snap.gif)

![](clear_snap2.gif)

Other times your view of the ball is not so clear. In these cases you just simply do your best by going off of when the offensive line starts to move and when the receivers cross the line of scrimmage (when they start to cross over onto the defenses side of the field).

![](hard_to_see_snap.gif)

The exact moment a ball is technically snapped is a little subjective and these videos run at about 60 fps so don't stress too much over annotating things to be exactly frame perfect. If you are unsure if you are annotating correctly just ask me and I can come do a couple with you.

### play_type

Enter one of the following six strings for the `play_type` field:  
* **run**: When the quarterback hands the ball off to the runningback
* **pass**: When the quarterback attempts to pass the ball*
* **play action**: When the quarterback first pretends to hand the ball off and then attempts to pass the ball*
* **broken**: This is usually when there is a penalty *before* the ball is snapped and the play is stopped before it begins
* **late**: When the clip begins after the play has already started and you never got to see the snap (this is rare)
* **missing**: Sometimes the film will go blank and have "NO FILM DETECTED" written on the screen, or sometimes a team calls a timeout and no play happens in the clip

\***IMPORTANT**: Sometimes a quarterback is tackled before they are able to throw the ball, other times the quartback may take off running if there is no open receiver to throw the ball to. On an official game stats sheet, these plays are recorded as running plays; *however*, for the purpose of film analysis these are considered pass plays and should be annotated as such.

Examples of each of the above play types can be found ...

For plays you label as `broken`, `late`, or `missing`, you can simply set the `snap` field to 0.

## What to do if you are unsure about a play

Sometimes you may be unsure about when the ball is snapped or how you should label a play type. Perhaps a scenario arises that I didn't cover above, or the play is hard to see, or you simply are not confident in what to put. In this case just set `snap` to 0 and `play_type` to "nico", and then create a new csv that is `filename_uncertain_plays.csv` that contains the `mark_in` frame and I will go back and check it out myself.

For example, if you are annotating `2015 002 08-30-15 LAURIER D @ YORK O_fps.mp4` and are thus saving your annotations in `2015 002 08-30-15 LAURIER D @ YORK O.csv`, then you would make a new csv titled `2015 002 08-30-15 LAURIER D @ YORK O_uncertain_plays.csv` that would look something like the following:



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
