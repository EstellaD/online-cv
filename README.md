There are a lot of things to be updated. Even a small typo would make the page fail to compile, so I want to document my customization process and make it slightly easier for someone who is reading this :blush:


## Initializaiton
1. Fork the repo from [template](https://github.com/sharu725/online-cv), and without changing your forked repository name, or go to setting to change the github page to *master* branch, or deleting the *gh-pages* branch, your website should **already** be hosted automatically at https://username.github.io/online-cv. I used to be able to change the repo name and the website url, but it leads to compilation failure and it’s not working anymore. So let’s stick with the repo name of ‘online-cv’, and the url of ‘https://username.github.io/online-cv'. A small customization can be made is change the ‘title’ in *_config.yml* to your name’s resume. 
____________________________
FYI what I used to do to change the repo name and self define a url. I think this could be submitted as an issue to the original repo owner. 

2. Got to Settings, change your repo name to something you like, e.g. estella.github.io. Then:
	a. change url to something you like, e.g. ‘http://estellad.github.io’ (This way you can define your own url)
	b. change baseurl to repeat the url last part, which is also your repo name. e.g. ‘/estellad.github.io’
  
3. Now in browser go to the new url you defined: ‘http://estellad.github.io’, and you can monitor your updates here later on. 
____________________________


## Content Updates
1. Go to *_data/data.yml*, and replace the contents in career profile, experience, and sidebar. Change sidebar>about to 'FALSE'. 

2. Change the CV theme to a color you like. There are six colors available: Blue, Turquoise, Green, Berry, Orange, Ceramic. 

- For source code of these templates, you can find them at */_sass/skins/*. (That being said, you should not delete this *_sass* folder because it is needed for compiling. I learnt it the hard way.) 
- For a quick preview of each theme, you can go to *assets/images/* for the color *.jpg*. (These you can delete, not crucial) 

I personally will go with Berry :sparkles:. There are two things you need to do to change the theme color:
- First, go to *assets/css/main.scss* and update the 'blue' in line 7 to 'berry'. 
- Then, go to *_config.yml* and update 'theme_skin: blue' in line 9 to 'berry'. 

3. I added this line to the end of the page of *_data/data.yml*: ‘Customized by Estella Dong.’

4. Replace the profile photo at *assets/images* to your 100x100 pixel photo, and if your photo format is not .png anymore, replace to correct photo format at line 12 'avatar:' *_data/data.yml*.


## Appearance
1. If you want your sidebar to appear on the left side, make changes inside *_sass/_base.scss*:

  - change the position of sidebar to left
  .sidebar-wrapper {
	  background: $theme-color;
	  position: absolute;
	  left: 0;

  - change the position of main-wrapper to padding to the left
  .main-wrapper {
	  padding-left: 340px;

2. You can change job title font to darker than the current gray, by changing:
  .job-title, .degree {
		color: #3F4650;

3. For project and publication title, decrease the font size a little bit to 15pt:

   -  .project-title {
	   font-size: 15px;

   -  .publication-title {
 	   font-size: 15px;

4. Remove project-title color from project-title section:
   .project-title {
		~~color: darken($theme-color, 15%);~~

5. Remove the font color from publication-authors section:
  .publication-authors {
       ~~color: $text-grey;~~


## Advanced - Adding and Removing Sections
In this part, we try to change how the files in *_inludes/.html* renders the information we put in *_data/data.yml *. These will be the most error-prone part of the online-cv building, so please pay attention to syntax error, etc.

1. Remove {% include skills.html %} from index.html, and also remove {% include projects.html %} for now. Project section can be used for adding R packages. 

2. I want to bold all the sections on the online-cv website, so go in to each section html file to add `<b> … </b>`: career-profile.html, experiences.html, publication.html, conferences.html. Bold section header, and bold each role title. 

3. Simplify publication.html inner part to `<div> title </div>`, `<div> author </div>`, and `<div> conference </div>`.

4. Add in {% include conferences.html %} to after publication. Create a conferences.html file in */_includes* folder, and the implement can follow publication.html exactly. 

5. Add in a .html file for hobbies and a .html file for softwareskills and display them in sidebar. The implementation of these two add-ons can follow interest.html. Thereafter, these .html files should be sourced in sidebar.html, by adding {% include softwareskills.html %} and {% include hobbies.html %}.

6. Change the name of language.html to languages.html.

7. Now it’s time to fill in the contents for these new sections in the *_data/data.yml* file. I tried many times to format these new sections and make sure they compile with the .html file in data.yml. 


## The End
Now you have a website like mine. It may look like an exact copy of Linkedin, but I like the minimalistic feeling and everything is all here. During the development of this repo, I referenced the style a lot from [here](https://github.com/CraigWangStat/CraigWangStat.github.io). However, his website is currently down due to the modified naming of repo issue I mentioned earlier. There are other small things to note:

1. Currently you still carry all the historical version control messages from others who forked the original repo. Since this is your own website, to have a clean version, you can duplicate the entire repo and make it independent from the source. However, do add a license for the original author. 












