---
layout: post
date: '2018-02-18 20:00 +1100'
comments: true
published: true
title: 'LaTeX for Chemistry #1 - Getting Started'
tags:
  - LaTeX
description: A beginners guide to LaTeX for writing a synthetic chemistry report/thesis.
---
For those unfamiliar, LaTeX is a sort of document preparation system that yields really high quality published documents. It's used for a lot of technical and scientific documentation including by a number of big journals. 

Unlike a word processor (ie. Word), LaTeX aims to seperate the actualy content of a document from the appearance or styling. Whilst at times it can feel a bit more intensive to write in the LaTeX 
'code' it does provide a much more consistent document and mitigates a lot of the fiddling that comes with other word processors. 

LaTeX is totally free and can be installed on Linux, Mac or Windows (and can even be used online via a couple of services). Personally, I decided to write my MSc Thesis in LaTeX because of the benefits it offered and as a means to learn a bit of a new skill. 

My aim is to make a number of posts that share some of the hints, tricks and experiences that I learnt during the process of writing a thesis - in particuarly in synthetic organic chemistry - in the hopes they may help others! 

## Getting Latex
First things first - getting your hands on LaTeX. Heading over to [https://www.latex-project.org/get/] and scrolling down will show links to LaTeX distributions for Linux, Mac and Windows. Be warned - these downloads can take a fair bit of time, so be prepared to wait a little. 

Once downloaded follow through with the instructions to install the distribution, and you'll likely end up with a bunch applications - ignore these for now.

## Text Editor
I prefer to use latex through a text editor that allows me to keep everything clean and minimal. Personally I'm a big fan of the incredibly awesome [Atom text editor](https://atom.io) which is open source, supported by GitHub, has a tonne of really neat functionality and looks pretty darn amazing. 

Follow the instruction on the site to install - for me I clicked the 'Download for Mac' button, opened the zip file, copied the file to my Applications folder and then launched it.

Once Atom is open you'll have to open the preferences tab (in Mac thats via Atom > Preferences) and then click on the 'Install' tab on the left. We're going to install some packages for Atom which will allow us to compile/run LaTeX documents within Atom, get special highlighting in LaTeX documents and view pdf's within Atom. 

Type in `latex` (at the time of writing the latex package is v0.49.0) and click install, then do the same for `language-latex`, `latex-tools` and `pdf-view`. Whilst were here click on the 'Packages' tab on the left, then on the `latex` package and under _Settings_ toggle the _Enable Shell Escape_ (this is going to allow the latex program to run other subprograms needed when compling our documents). 

You're now ready to start writing - and compling - LaTeX documents!

## Version Control/Backup


## Setting up your first TeX document
LaTeX works by allowing you to write a plain text file which contains all the documents content and structure, this plain text file is then compiled and LaTeX converts all the content and structure into a pdf document for you. 

To get started in Atom create a new file and save it in a new folder as `latex-example.tex` making sure it has the .tex extension. 

The first thing we need to do with a new LaTeX document is tell LaTeX what kind of document we want to make, which in this case is done by the `\documentclass{article}` command. This tells LaTeX we want to use the layout for an article, we could also tell latex we want to use a base font size of 11pt by instead using the `\documentclass[11pt]{article}` command.

Next we define where all the content of our document will go by adding two lines with `\begin{document}` and `\end{document}` respectively. Whilst this seems a little bit funky to have to start the document, it allows us to have whats know as the _preamble_ above it where we can provide any setup instructions.

Finally, let's add some content to our document by typing `Hello World!` between the `\begin{document}` and `\end{document}` lines. Hopefully your `latex-example.tex` file now looks like this:

```TeX
\documentclass{article}

\begin{document}
Hello World!
\end{document}
```
To compile this to a pdf file in Atom, go to Packages > LaTeX > Build or `CMD + SHIFT + P` and then 'Build' followed by `Enter` on Mac. In the bottom left corner of Atom there's a little spinning wheel to show that LaTeX is building the file which should be done really quickly and generate a number of files in the same folder as the `.tex` file. 

If all has gone well you should end up with a pdf that looks like this: 

![PDF output]({{site.baseurl}}/assets/latex-chemistry-1-example-output.png)
{: .center}
