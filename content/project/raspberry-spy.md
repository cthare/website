+++
# Date this page was created.
date = "2017-11-12"

# Project title.
title = "Raspberry Spy"

# Project summary to display on homepage.
summary = "Personal project using a Raspberry Pi and the camera module,"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "rsb-spy.gif"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["personal"]

# Optional external URL for project (replaces project detail page).
external_link = "https://github.com/cthare/Raspberry-Spy"

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "rsb-spy.gif"
caption = "Raspberry Pi with PIR sensor and camera module"

+++

The goal for the Raspberry Spy was to expand on the [Parent Dectector](https://projects.raspberrypi.org/en/projects/parent-detector) project from the Raspberry Pi Foundation. I wanted to see if I could configure the existing project to email me a photo whenever the PIR sensor was triggered instead of just taking a video.

A majority of the project was spent on mailPi module which handles all the email of the program. The camPi module is essentially the Parent Dectector code with a slight modification to have it take a picture and then call sendmessage() from mailPi in order to send an email.

The remainder of the project was spent figuring out how I could avoid leaving passwords and emails embedded in the code. I ended up using the keyring library to handle both email and passwords. I setup a quick prompt to input everything along with a function to check for if an archive had already been created.

In the end I had achieved what I had set out to do with my limited knowledge at the time. While there are tons of improvements that could be made to this little pet project, I'm proud of it because it was the first that I had completed since learning to program.





