There are a lot of things to be updated. Even a small typo would make the page fail to compile, so I want to document my customization process and make it slightly easier for someone who is reading this :D

## Initializaiton
1. Fork the repo from [template](https://github.com/sharu725/online-cv), and without changing your forked repository name, or go to setting to change the github page to *master* branch, or deleting the *gh-pages* branch, your website should **already** be hosted automatically at https://username.github.io/online-cv/. We can try to change your repo name and the website url later, but let's launch the website first. 

## Content Updates
1. Go to *_data/data.yml*, and replace the contents in career profile, experience, and sidebar. Change sidebar>about to 'FALSE'. 
3. Change the CV theme to a color you like. There are six colors available: Blue, Turquoise, Green, Berry, Orange, Ceramic. For source code of these templates, you can find them at . For a quick preview of each theme, you can go to *assets/images/* for the *.jpg*. I personally will go with Berry :) There are two things you need to do to change the theme color. First, go to *assets/css/main.scss* and update the 'blue' in line 7 to 'berry'. Then, go to *_config.yml* and update 'theme_skin: blue' in line 9 to 'berry'. 
4. I added this line to the end of the page of *_data/data.yml*: 
5. Replace the profile photo at *assets/images* to your 100x100 pixel photo, and if your photo format is not .png anymore, replace to correct photo format at line 12 'avatar:' *_data/data.yml*.
