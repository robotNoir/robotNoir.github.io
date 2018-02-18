---
layout: post
date: '2018-02-18 21:03 +1100'
comments: true
published: true
title: LaTeX for Chemistry
description: A beginners guide to writing a synthetic chemistry report or thesis in LaTeX.
tags:
  - LaTex
---
For those unfamiliar, LaTeX is a sort of document preparation system that yields really high quality published documents. It's used for a lot of technical and scientific documentation including by a number of big journals. 

Unlike a word processor (ie. Word), LaTeX aims to seperate the actualy content of a document from the appearance or styling. Whilst at times it can feel a bit more intensive to write in the LaTeX 
'code' it does provide a much more consistent document and mitigates a lot of the fiddling that comes with other word processors. 

Personally, I used LaTeX when writing my MSc Thesis and aim to share some of the hints and tricks that I learnt during that process - in particuar, those relevant to anyone writing a thesis or report in chemistry.

## Getting started with LaTeX


## Structures, schemes and automatic compound numbering
One of the most painful experiences in writing any type of report or thesis in chemistry is the need to number all the compounds. Particuarly when your supervisor decides you should add another scheme, or you notice a mistake - it takes forever to go back through a (correctly) renumber everything. 

Hello [chemnum](https://ctan.org/pkg/chemnum?lang=en)! Chemnum is a LaTeX package that offers a couple of really nice features around numbering chemical compounds. It allows you to assign a *label* to a compound (ie. 'ester-a') and when the document is compiled with automatic generate and assign numbers to every *label*. Even better is it allows the replacing a text in EPS or PS files, meaning we can automatically number compounds in chemdraw schemes. Hecking cool!

To start we need to set up a basic report-style document using `TeX \documentclass[]{report}`. Then load in the chemnum package with `TeX \usepackage{chemnum}` and finally start out document via `TeX \start{document}`.


```TeX
\documentclass[]{report}

% Load Packages
\usepackage{chemnum}

% Start Document
\start{document}
	% Declare our compounds
    \cmpd*{cmpd:carboxylic-acid}
    \cmpd*{cmpd:alcohol}
    \cmpd*{cmpd:ester}
    
\end{document}
	

```



![latex-chemistry-esterification.png]({{site.baseurl}}/assets/latex-chemistry-esterification.png)








![latex-chemistry-isomerisation.png]({{site.baseurl}}/assets/latex-chemistry-isomerisation.png)
{: .center}


## Referencing
