# kblincoe.github.io

This website is built using Jekyll. 
Jekyll Scholar is used to create the publications list. 

# Want to create your own website?
This code is released under an MIT license. Here are some tips on how to create your own academic website based on this code.

First you will need to clone or fork and then clone this repository, so that you have your own copy where you can make the following changes to personalize the site with your own content.

The _config.yml file is the main configuration file. You will want to change the site title in that file. You can also modify the Jekyll Scholar configuration, which specifies the order and grouping of the publication list, if you wish. If you decide to use any other Jekyll plugins, you would specify them in this file (and in Gemfile). 

The _bibliography folder contains two files, a csl file which specifies the format of the publications listed on the publication page and a references.bib file which contains the BibTeX entries of all of my publications. Simply replace the bib file with your own BibTeX entries and the publication page will show your own publications. If you want to change the reference style, you can find many csl files at https://github.com/citation-style-language/styles. Just add your preferred csl file to the _bibliography folder and change the reference to acm-sigchi-proceedings.csl in _config.yml to that csl file.

The _layouts/bib.html file should be modified to include your own name (if you want your name bolded in your publications). Note that the format of your name may need to change if you change the csl file to use a different reference format. The _layouts/bib.html file specifies how to handle additional BibTeX entry fields. Currently, it supports the fields: award, doi, html, pdf, slides, code, and video. Add these fields to your own BibTeX entries in the references.bib file if you want to add links to preprints, replication packages, etc. These links can be absolute paths (if you store your files on some other site) or relative paths. I currently use the publications and slides folder to store copies of my publications (you should delete all of my publications from your copy of the website and replace them with your own or just delete these folders if you store your publications elsewhere).

The _includes and _layouts folders store the html files that specify the layout of the website. These files can be edited if you wish to change the design. You will definitely want to change the _includes/google_analytics.html to include your own Google Analytics site tag (or simply remove this file and the line {% include google_analytics.html %} in _includes/header.html if you are not using Google Analytics).

You can easily change the look and feel of the website by pointing to a different stylesheet in the _includes/header.html file. The website currently uses the Minty theme by Bootswatch via CDN at jsDelivr. If you want to use a different Bootswatch theme, just replace minty with the name of your preferred theme (see https://bootswatch.com/). Or you can replace the entire href to another CDN. Note that I have slightly modified the minty theme by using a cursive font in the navbar for the site title text (my name). If you want to remove this customization, simply remove style="font-family: 'Homemade Apple', cursive;" from _includes/navbar.html.

The _data folder and the .md files in the root directory is where you will make most of your changes. The yml files in the _data folder contain all of the information that is populated to the various pages of the site, like my list of students or service roles. Edit these lists with your own information, making sure to keep the correct format.
Finally, update the .md files in the root directory with your own content and delete the survey folder (this just holds some of my research study materials). 

The _site folder is built based on all of the files described above. See below for how to build and test the site.

If you are using GitHub pages to host your site, make sure you have two branches (main and source). Set the source branch as default. The .github/workflows/build.yml file specifies a GitHub action which will build the website and push the files onto the main branch everytime new changes are pushed to the source branch. It ignores changes made on the main branch. If you are hosting your website somewhere else, you do not need this file. 

# How to build and test locally 
Note: before trying to run locally ensure you have installed Jekyll and its prerequisites (see: https://jekyllrb.com/docs/)

1. Install the dependencies specified in the Gemfile (note: you only need to do this once)
```
bundle install
```
2. Compile and run
```
bundle exec jekyll serve
```
3. Verify changes build correctly by going to http://localhost:4000 in your browser

# Want to submit a pull request for this website?
If the above instructions need to be improved or you have suggestions on the website, feel free to submit a pull request or create a new issue. 

My students can also submit pull requests if they want to add or modify their publications or any other details about themselves on the site. 
All pull requests should be submitted to the source branch. 
GitHub actions automatically builds the website and creates the html files on the main branch. 

Clone this repo and make any required changes in your local copy.
To add a publication, add a BibTeX entry to the references.bib file in the _bibliography folder on the source branch. 
You can also modify existing entries in this file to add additional details as needed.
You can use the fields pdf, slides, video, award, html, and doi. 
In these fields, you should use absolute paths as the bib file also populates the HASEL website. 
If you add a pdf of the publication, make sure you have also included the doi field as this is a condition of most copyright agreements. 

Make sure you test locally before submitting a pull request (see instructions above).
