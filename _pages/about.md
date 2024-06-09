---
permalink: /
<<<<<<< HEAD
#layout: archive
title: "Homepage"
excerpt: "About me"
=======
title: "Academic Pages is a ready-to-fork GitHub Pages template for academic personal websites"
>>>>>>> 5dee723c4017b7d297a31daa3950d8eeb6570c61
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<<<<<<< HEAD
<br />
Greetings, I am <b>Dewinda</b>, and I am delighted to have you on my webpage!

I am a Doctoral candidate in Computer Science. My research is centered around the application of Deep Learning for medical imaging.
=======
This is the front page of a website that is powered by the [Academic Pages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages. [GitHub pages](https://pages.github.com) is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the respository. This template was forked from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) created by Michael Rose, and then extended to support the kinds of content that academics have: publications, talks, teaching, a portfolio, blog posts, and a dynamically-generated CV. You can fork [this repository](https://github.com/academicpages/academicpages.github.io) right now, modify the configuration and markdown files, add your own PDFs and other content, and have your own site for free, with no ads! An older version of this template powers my own personal website at [stuartgeiger.com](http://stuartgeiger.com), which uses [this Github repository](https://github.com/staeiou/staeiou.github.io).

A data-driven personal website
======
Like many other Jekyll-based GitHub Pages templates, Academic Pages makes you separate the website's content from its form. The content & metadata of your website are in structured markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the [GitHub pages](https://pages.github.com/) service creates static HTML pages based on these files, which are hosted on GitHub's servers free of charge.
>>>>>>> 5dee723c4017b7d297a31daa3950d8eeb6570c61

Here, you can find a combination of personal and professional details about me.
<br />
## Updates
<style>
table, tr, td {
    border: none;
}
</style>
<div style="height:250px;overflow:auto;border:0px;border-collapse: collapse;" >
<table  border="none" style="border:0px;border-collapse: collapse;" rules="none" >
<colgroup>
       <col span="1" style="width: 12%;">
       <col span="1" style="width: 88%;">
</colgroup>
<tr><td>  May. 2024: </td> <td>I have joined the activity committee for the <a href="https://faimi-workshop.github.io/" target="_blank">FAIMI workshop</a>  at MICCAI! 💼 This role will allow me to contribute to the advancement of medical imaging and AI. Looking forward to supporting the community!
</td></tr> 
<tr><td>  Mar. 2024: </td> <td>Excited to be invited as a reviewer  for the <a href="https://2024.midl.io/" target="_blank"> MIDL 2024</a>! 🧐 I’ll be reviewing two papers related to my experience in brain MRI analysis. Learn more about my first reviewing experience <a href="https://2024.midl.io/" target="_blank"> here</a>
</td></tr> 
<tr><td>  Oct. 2023: </td> <td>Thrilled to receive the Best Poster Presentation Award for my paper 'How You Split Matters' at MICCAI FAIMI Workshop 2023! 🏆🎉Check out the winning poster <a href="https://djrumala.github.io/publications/how-you-split-matters" target="_blank">here</a>
</td></tr> 
<tr><td> Aug. 2023: </td> <td> My work "<a href="https://arxiv.org/abs/2309.00350" target="_blank">How You Split Matters</a>: Data Leakage and Subject Characteristics Studies in Longitudinal Brain MRI Analysis" has been accepted for publication at MICCAI FAIMI 2023 workshop. Congratulations!
</td></tr> 
<tr><td> April. 2023: </td> <td> Our work "Deep-Stacked Convolutional Neural Networks for Brain Abnormalities Classification Based on MRI Images" has been accepted for publication at <a href="https://link.springer.com/article/10.1007/s10278-023-00828-7" target="_blank">Journal of Digital Imaging</a> (Springer). Congratulations!
</td></tr> 
<tr><td> Nov. 2022: </td> <td> I have started a research visit in the <a href="http://bioimage.khu.ac.kr/" target="_blank">Bio-Imaging Laboratory</a> at Kyung Hee University, South Korea (supervised by Prof. Tae-Seong Kim).
</td></tr> 
<tr><td> Sep. 2022: </td> <td> I have received a grant from the Ministry of Education, Culture, Research, and Technology Indonesia in the program of Enhancing International Publication/PKPI as part of my PMDSU scholarship to conduct a research abroad
</td></tr> 
<tr><td> Aug. 2022: </td> <td> Our work "The Effect of Noisy and Blurry Data on Deep Learning: Application in Brain Image Classification" has been accepted for publication at <a href="https://ieeexplore.ieee.org/abstract/document/9977591" target="_blank">IEEE Region 10 Conference (TENCON) 2022</a>
</td></tr>

<<<<<<< HEAD
</table>
=======
Getting started
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section

Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the Academic Pages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring Academic Pages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
>>>>>>> 5dee723c4017b7d297a31daa3950d8eeb6570c61
