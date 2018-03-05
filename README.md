Struktúrált formában tárolt programszöveg
=========================================

### Introduction, short description

This repository contains my original MSc thesis text in Hungarian language about structured representation of source codes. This basically serves as a documentation alongside the "turul" project too - which project is also here on github.

My goal with the "turul" project is to try to create an "engine" for programming language development - using some of my very specific ideas about a generic and simple representation of trees. With all hopes, once this tool can evolve into something that "3D engines" are to "games" in a very much different scene. This is an idea for a "programming language engine" one would say.

When a language compiler is made, there are usually only libraries and methods available but I cannot see if anyone ever approached the compiler contruction problem in a way that resembles 3D engines. Surely this field has nothing to do with three dimensions now, but there are very good ideas that can be used in a different field in my opinion. One of those ideas is giving a framework or one would say "container" for "scripts" and "plugins" that change the behaviour of the build result made with the engine. Alongside this, engines usually provide a "scene graph" or related data structures for which in our case we will see solutions for parsing, representation of code, semantics of transforming trees etc.

Looking at the problem in this light also enables very interesting new approaches: languages with never-seen-before metaprogramming capabilities and extensibility. I do not know how much I can demonstrate from this ideas using this toolset, but I will try to present some interesting new points of research too.

The text will be deliberately in Hungarian, but the code should be well documented in english and there will be some technical descriptions on the "turul" project page on github. Everything will be of course completely open source forever ;-)

### Technological description of the text template I am using

Markdown template for thesis works in the Budapest Eötvös Lóránd university. **This is an experimental work** and is only recommended for users experienced with _both Markdown and LaTeX_ - or crazy people such as myself.

Forked from a BME template with very similar goals and a nice structure.
Tested on Ubuntu Linux 16.04 with pandoc 1.16.0.2 and texlive (1.2).

### Requirements

* Pandoc 1.12.4.2 with pandoc-citeproc (see http://johnmacfarlane.net/pandoc/installing.html#all-platforms). Ubuntu 14.04 only provides version 1.12.2.1 which does not produce proper cross references in the HTML output. I am doing my testing with 1.16.0.2 at this time because that is the version I can readily apt-get on my good old 16.04 Ubuntu laptop.
* TeX Live (I have found out that `texlive-full` is not necessary! You can use texlive-base and then use tlmgr to get missing stuff)

### Troubleshooting

After trying this on the 16.04 and the named software version I have found myself with a lot of errors:

* TexLive complained about missing components because (I think that is the reason) I was only using texlive-base and not the full 2Gb pack
* For getting those packages I tried tlmgr but that failed miserably and forums wrote a lot of weird things about it being a bug in ubuntu. This have solved it however: https://tex.stackexchange.com/questions/137428/tlmgr-cannot-setup-tlpdb
* magyar.ldf file was missing so I downloaded one from the BME Latex pages (now it is included in this git repo and tex finds it like this)
* There was some weird error in chapter04.tex: It complained about a single quote mark or something so I looked up the problematic place and just removed the text around it as a quickfix. You can see my change in the git commit so you will not find the same stuff but worth mentioning there was this problem. It seems there is nothing in there I would need for myself so I just ignore this...

### Usage

* Clone this repository:
* Use `make all` `make pdf`, `make html`, `make epub` to generate the thesis in your desired output format.

Rem.: Mostly I only test pdf however because I do not have endless time ;-)
