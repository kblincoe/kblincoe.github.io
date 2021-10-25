# kblincoe.github.io

This website is built using Jekyll. 
Jekyll Scholar is used to create the publications list from the references.bib file in the _bibliography folder. 
The code is released under an MIT license. 

My students can submit pull requests if they want to add or modify their publications. 
All pull requests should be submitted to the source branch. 
GitHub actions automatically builds the website and creates the html files on the main branch. 

To add a publication, add a BibTeX entry to the references.bib file in the _bibliography folder on the source branch. 
You can also modify existing entries in this file to add additional details as needed.
You can use the fields pdf, slides, video, and award. 
In these fields, you can use absolute paths (if the file is stored elsewhere) or a relative path (if the file is stored in this repo). 
If you use a relative path, make sure you have also added the file to the repo in the appropriate folder on the source branch. 
If you add a pdf of the publication, make sure you have also included the doi field as this is a condition of most copyright agreements. 

To test locally before submitting a pull request, you can do the following:
Note: before trying to run locally ensure you have installed Jekyll and its prerequisites (see: https://jekyllrb.com/docs/)
1. Clone this repo
2. Install the dependencies specified in the Gemfile 
```
bundle install
```
3. Compile and run
```
bundle exec jekyll serve
```
4. Verify changes build correctly by going to http://localhost:4000 in your browser
