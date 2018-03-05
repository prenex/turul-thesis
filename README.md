ELTE thesis-template-markdown
=============================

Markdown template for thesis works in the Budapest Eötvös Lóránd university. **This is an experimental work** and is only recommended for users experienced with _both Markdown and LaTeX_ - or crazy people such as myself.

Forked from a BME template with very similar goals and a nice structure.
Tested on Ubuntu Linux 16.04 with pandoc 1.16.0.2 and texlive (1.2).

### Plan

With this template I have the following plan personally:

* OK: Clear it up, so that it builds on my machine
* OK: Make the fork support ELTE university so that it can be used as a markdown base for ELTE thesis (and tech paper) writing
* WIP: Fork this into my thesis - then add that as a submodule into the source code for my Turul system as its documentation.

Current state TL;DR: Complete conversion for ELTE-IK MSc thesis documents are quite finished as of now!

After that there will be a working example but I think I will lose interest in the base template unless I actively use it.
It is very much free to fork however and start your own things.

I very much hope it will be used by people who have skills and preserverance so that I do not need to answer a lot of issues.

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
  ```bash
  git clone https://github.com/prenex/thesis-template-markdown.git
  ```
  
* Use `make all` `make pdf`, `make html`, `make epub` to generate the thesis in your desired output format.

Rem.: Mostly I only test pdf however because I do not have endless time ;-)
