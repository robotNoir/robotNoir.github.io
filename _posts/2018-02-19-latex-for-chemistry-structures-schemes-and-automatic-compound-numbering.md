---
layout: post
date: '2018-02-19 00:45 +1100'
comments: true
published: true
title: 'LaTeX for Chemistry #2 - Automatic Compound Numbering'
description: Automatically numbering compounds in text and chemdraw schemes in LaTeX.
tags:
  - LaTeX
---
One of the most painful experiences in writing any type of report or thesis in chemistry is the need to number all the compounds. Particuarly when your supervisor decides you should add another scheme, or you notice a mistake - it takes forever to go back through a (correctly) renumber everything. 

Hello [chemnum](https://ctan.org/pkg/chemnum?lang=en)! Chemnum is a LaTeX package that offers a couple of really nice features around numbering chemical compounds. It allows you to assign a _label_ to a compound (ie. 'ester-a') and when the document is compiled with automatic generate and assign numbers to every _label_. Even better is it allows the replacing a text in EPS or PS files, meaning we can automatically number compounds in chemdraw schemes. Hecking cool!

## A Basic Example

To start we need to set up a basic report-style document using `\documentclass[]{report}`. Then load in the chemnum package with `\usepackage{chemnum}` and finally start out document via `\begin{document}`.

```TeX
\documentclass[]{report}
\usepackage{chemnum}

\begin{document}

\end{document}
```


```TeX
\documentclass[]{report}

% Load Packages
\usepackage{chemnum}

% Start Document
\begin{document}
% Declare our compounds
    \cmpd*{cmpd:carboxylic-acid}
    \cmpd*{cmpd:alcohol}
    \cmpd*{cmpd:ester}
    
    A Steglich esterification is as esterification between \cmpd{cmpd:carboxylic-acid} and \cmpd{cmpd:alcohol} to afford \cmpd{cmpd:ester} with the coupling reagent DCC and catalytic DMAP.
    
\end{document}
```






![latex-chemistry-esterification.png]({{site.baseurl}}/assets/latex-chemistry-esterification.png)


## More complex numbering

```TeX
\documentclass[]{report}

% Load Packages
\usepackage{chemnum}

% Start Document
\begin{document}
% Declare our compounds
    \cmpd*{cmpd:carboxylic-acid}
    \cmpd*{cmpd:alcohol}
    \cmpd*{cmpd:ester}
\end{document}
```



![latex-chemistry-isomerisation.png]({{site.baseurl}}/assets/latex-chemistry-isomerisation.png)
{: .center}


## Referencing
