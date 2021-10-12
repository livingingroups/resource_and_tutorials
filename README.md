# Resources and Tutorials
Below is a compiled list of various resources and tutorials, both internal and external, for tools, programming tricks, and tutorials related to science reform, reproducibiluty, and open data science in the department.
We can break this into sub pages as it grows.
## Data Management
<details>
  <summary>Click to expand!</summary>

### A cautionary note on Excel

If you do use a spreadsheet software like Excel (or Open/LibreOffice), **please be aware of the *Column type* settings** when importing plain-text spreadsheets (eg. `.csv` or `.tsv`).

![](https://i.imgur.com/C75CZN0.png)

**Make sure to actually select the appropriate column type**, because otherwise your program will overwrite the data with what it **thinks** you want them to be. This can *easily go unnoticed*, be *irreversible* and has actually lead to [widespread issues in the scientific literature](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-1044-7)!

### Open Data Kit
#### ODK collect

- [Official docs](https://docs.getodk.org/getting-started/)

#### Kobo collect
Open source version of ODK, forms can be version controlled. Useful tutorial [here](https://test2.biogeo.ucdavis.edu/guides/kobo.html)

### Exiftool

- [exif tool tutorial series](https://www.weareavp.com/exiftool-tutorial-series/)
- [{exiftoolr}](https://github.com/JoshOBrien/exiftoolr): R package to call exiftool from within R (also works on windows) ([quick demo](https://gist.github.com/k-hench/7e8d8e1ee23ab4b4dc293acd08305893#file-r_exiftool-r))

### Hashing
Download .RMD tutorial [here](https://github.com/livingingroups/hashing_digest_tutorial)
### ReadMe files
### Best naming practices
  
</details>

## Version Control with Git

<details>
  <summary>Click to expand!</summary>

**Basic Idea:** 
*Git* is a tool for version control, which means it is a method to keep track of changes within a specified set of files on your computer.
It provides the possibility to take *snapshots* during the development of a project that can be restored or referenced later.
It therefor is a clean method to protocol and track changes of an entire project.

Git is particularly tracking changes in sets of plain text files, usually used for coordinating work among programmers collaboratively developing source code. 
In research it is largely used for Code Collaboration and Version Control.
Git can be run in the terminal, but most researchers use a Git Interface GUI (s. below).

*GitHub* is an online platform where repositories can be stored, managed and distributed.
It provides convenient tools to work on a project collaboratively like eg. the option to have project related discussion within in the form of *issues*.
It is also a popular way of distributing software like for example *R* or *python* packages.

**Glossary:**

- **git**: the actual program doing the version control
- **github**: an online platform to manage and distribute version controlled projects that facilitates easy collaboration
- **repository**: the specific project folder that is monitored (version controlled) by *git*
- **add**: selecting modified files that for the next snapshot (aka. **staging**) 
- **commit**: taking a snapshot of selected file modifications of the repository and archiving them
- **remote**: an online instance of the repository (typically on *github*) that is connected to a the locally downloaded folder.
- **push**: updating the *remote* with new changes from the local instance of the repository
- **pull**: updating the local instance of the repository with new changes from the *remote*
- **branch**: creating a parallel copy of the repository on which it is save to for example try experimental changes
- **merge**: incorporate changes from a branch into the main (consensus branch) of the repository
- **clone**: downloading a repository from a remote to a local computer
- **fork**: creating a copy of someone elses repository on github

### Resources

**git:**
- the original *git* [homepage](https://git-scm.com/) (with *git* [documentation](https://git-scm.com/book/en/v2))
- *git* for [windows](https://gitforwindows.org/index.html) users
- the *git* intro slides from the ODS workshop ([pt I]() (not available? can replace with [my own one (kh)](https://k-hench.github.io/git/git.html)) and [pt II](https://k-hench.github.io/git/gitII.html))
- the *git* [discussion slides](https://github.com/livingingroups/ODS/blob/main/week.10/Version%20Control%20with%20git(Hub).pdf) from the ODS workshop
- the [Atlassian terminal tutorial](https://www.atlassian.com/git) from the makers of Bitbucket
- the [Software Carpentry Tutorial](https://swcarpentry.github.io/git-novice/)

**github:**
- [Github](https://github.com/): The most heavily used, and well known provider of Internet hosting for software development and version control using Git. You are on it now. Owned by Microsoft
- [Bitbucket](https://bitbucket.org/): Another commonly used, open source code version control site.
- [zenodo](https://zenodo.org/): the place to store your github repositories for posterity (and create a doi) 
- the [*github* group](https://github.com/livingingroups) of the EAS

**Git GUI Clients:**
- [RStudio](https://www.rstudio.com/): RStudio has a great built in Git Interface. [Tutorial here](https://happygitwithr.com/).
- [GitKraken](https://www.gitkraken.com/): As taught in the EoAS Workshop.
- [GitHub Desktop](https://desktop.github.com/): a GUI by the developers of github (only on windows or mac)
- [Sublime Merge](https://www.sublimemerge.com/): Another GUI that works Seamlessly with SublmeText, a great open source mutli (programming) language text editor
- [Visual Studio](https://visualstudio.microsoft.com/): an cross-platform integrated development environment (IDE, aka. text editor on steroids). Heavily customizable and convenient environment that also manges git
  
</details>

## Programming Languages
<details>
  <summary>Click to expand!</summary>
  
### R
<details>
  <summary>Click to expand!</summary>
  
R is likely the first programming language that most ecologists come across.
It is widely used throughout biology and specifically intended for statistical programming.
The basic elements of R are distributed by the Comprehensive R Archive Network ([CRAN](https://cran.r-project.org/)) who also provide a huge catalog of additional *packages* that extend the base functionality of R.
Appart from CRAN, there are also other sources of custom R packages such as [github](https://www.github.com) or [bioconductor](http://bioconductor.org/) that can provide very specific tools for particular biological analysis.
The most commonly used editor for working with R is [RStudio](https://www.rstudio.com/), which is available for all operating systems.

#### Intoduction to R Tutorials

- [tinystats](https://tinystats.github.io/teacups-giraffes-and-statistics/): cute basic R intro
- [R for data science](https://r4ds.had.co.nz/): getting up to speed with the core elements of the {[tidyverse](https://www.tidyverse.org/)}
- [What They Forgot to Teach You About R](https://rstats.wtf/): a workshop once you have the basics of R down
- [Advanced R](https://adv-r.hadley.nz/): getting into the more detailed aspects of R

#### Creating Packages in R
- [R packages](https://r-pkgs.org/): concise intro into package creation
- [{usethis}](https://usethis.r-lib.org/): incredibly helpful templating package

#### Asking for help
- EAS Slack channel #coding_group: first line of defense
- [stackoverflow](https://stackoverflow.com/questions/tagged/r): asking the global R community
- [{reprex}](https://reprex.tidyverse.org/): a handy package to *"help you help me help you"* (how to effectively ask R related questions)

#### Tutorials held at EAS

- [Functional programming in R](https://k-hench.github.io/x_functional/functional.html): introduction into functional programming - the R superpower that prevents you from repeating yourself within R scripts.
- [ggplot (I/II)](https://k-hench.github.io/x_ggplot/ggplot.html): introduction into the basic concepts of the *grammar of graphics* as implemented within the [{ggplot2}](https://ggplot2.tidyverse.org/) package
- [ggplot (II/II)](https://k-hench.github.io/x_ggplot/ggplotII.html): arranging multiple ggplots, annotations and fancy hacks for ggplot

  </details>
  
### Python
  
- [Tutorial](https://www.codecademy.com/learn/learn-python) by *codecademy*

### [mcSTAN](https://mc-stan.org/)
STAN is the most commonly used Hamiltonian MCMC proabailistic sampling engine for Bayesian inference. It can be implented in R, Python, Linux Shell, MatLab, Mathematica, Julia, Stata, and Scala.
For R users, there are several "convenience" wrappers that can fir simple hierarchical models (and more) in stan.
1. [rethinking pacakage](https://github.com/rmcelreath/rethinking) and Richard McElreaths accompanying textbook.
2. [brms](https://github.com/paul-buerkner/brms) fits STAN generlized linear regressions using lme4 syntax
3. [rstanarm](https://github.com/stan-dev/rstanarm)

### Bash aka Linux Terminal

<details>
<summary>Click to expand!</summary>
    
**Background**:
The *Terminal* is the program that gives you access to your systems [*shell*](https://en.wikipedia.org/wiki/Shell_%28computing%29). It is that *black box* that you might have seen on the Matrix or any news-piece about hackers - it is also very useful for data science.

![matrix](https://i.imgur.com/aN8WbJu.gif)

In short, the shell allows you to interface with your computer by typing in commands rather than clicking on icons or graphical user interface programs (GUIs) - it might be a little surprising, but this *can* actually be a huge advantage.

Unfortunately, the exact behavior (the language) that your shell uses is *depending on your operating system*. The general rule is: *Windows* is different than everything else, the *unix*-based systems (*MacOS* and *Linux*) are mostly similar and run [*bash*](https://en.wikipedia.org/wiki/Bash_(Unix_shell)) as shell language.
You can, however, install [*git for windows*](https://gitforwindows.org/index.html), which will also come with a basic *bash* functionality on *Windows*.

**Access**:
- On *MacOS* and *Linux* find and open the program called *Terminal* (eg. using the basic search function of either OS).
- On *Windows* (with [*git for windows*](https://gitforwindows.org/index.html) installed), right-click on a folder or on the desktop and select *"Git Bash Here"*.
- Using [RStudio](https://www.rstudio.com/) (if *Windows*: with [*git for windows*](https://gitforwindows.org/index.html) installed): look for the *"Terminal"* tab in one of the four main panes.

All of those options should bring you to a black or white void (or even a colorful one), where a `$` prompt is waiting for your input.

**First commands**:

Here just a few very basic *bash* commands and tips:

- `pwd` is short for "print working directory" and reports the location on your file system where the command line is currently operating (this tells you *where you are*)
- `ls` will print the content (the files & folders) of the current directory (*what is around you*)
- `cd` is short for "change directory" and allows you to change your working directory (*move around*)
- `echo` allows you to print some text as output (it allows you to *speak*)
- `./` is the current directory
- `..` is the *parent* directory (the directory which contains the current directory)

One thing that makes your life easier when using the command line is the `<tab>` key on your keyboard. If you don't know what it does, *do try it*. It's basically an auto-complete for your input.

**Tutorials**
- [quick intro](https://k-hench.github.io/getting_stuff_done/bash.html)
- [popper tutorial](https://www.learnshell.org/) (by *learnshell*)
- [more tutorial](https://www.javatpoint.com/bash) (by *javatpoint*)
- [bash one-liners](https://github.com/fcenobi/Bash-Oneliner#grep)
  
</details>
  
</details>

## Manuscript Preparation  
<details>
<summary>Click to expand!</summary>
  
### LaTeX

  
LaTeX is a plain text document preapartion editor that uses the TeX language. 
It typsets plain text files. It integrates with BibTeX, an open source citation manager service. 
LaTeX is great for complicated mausccripts (i.e. dissertations and books) and manuscripts with alot of mathematical notation. 
It can also be used to make slides for presenatations. 
TeX documents can also be versioned controlled on GitHub. 
Many journals also have LaTeX templates one may use for submission.

- [Intro Video](https://www.youtube.com/watch?v=xYzg-gfx6dQ)
- [texstudio](https://www.texstudio.org/): a latex editor


#### [Overleaf](https://www.overleaf.com/project)
Here is a [Youtube Video Tutorial](https://www.youtube.com/watch?v=5dnK2knSu0Q&t=2s) and [sample document](https://www.overleaf.com/project/5c3c4116de500c6cd5652f2f) for collaborative document preparation using Overleaf. 
Overleaf also integrated with GitHub for document version control.

- [phd thesis template](https://www.overleaf.com/project/5f4629293ce1bd0001fece17) by kh

#### [ShareLaTeX](https://www.sharelatex.com/)
This is a similar collaborative LaTeX document preparation. 
The University has a free Pro account.
This has merged with Overleaf
  
### Markdown
   
Markdown is a lightweight markup language for created formatted text, whose source code is human readable.
These are saved as `.md` or `.mdown` file extensions.
This page you are currently reading now and any GitHub readme is written in Markdown.

Markdown files behave specially on github in the sense github is aware of the format. Markdown files will thus be displayed nicely formatted on github.
Also, within any folder of a repository, github will display the content of a `README.md` file if present.

1. [Tutorial in multiple languages](https://www.markdowntutorial.com/)
2. [GitHub Markdown Tutorial](https://guides.github.com/features/mastering-markdown/)
    
  
### RMarkdown
     
RMarkdown is another programming language that integrated R code with Markdown style writing to integrate text, Rcode, and R terminal output. 
It can be used to publish HTML (which can be publiched as websites), PDF, and MS word documents where code and the products of code are desirealbe to share. 
It is great to share intermediate results, write living documents (can be integrated wit BibTeX for citations) where results in text can be changed if analysis changes or more data is added, or publish tutorials and websites.

- [R Markdown: The Definitive Guide](https://bookdown.org/yihui/rmarkdown/)
- [R Markdown Cookbook](https://bookdown.org/yihui/rmarkdown-cookbook/)
- [RMarkdown for Scientists](https://rmd4sci.njtierney.com/index.html)
- [bookdown](https://bookdown.org/yihui/bookdown/): for more complex documents spanning multiple pages
  

  
### PanDoc
   
This is what powers the magic of markdown - the actual program that translates all sorts of document types (i.e. PDF to LaTeX to Word to Markdown to .txt).

You can for example convert this `.md` file to `pdf` or `html` simply by running:

```sh
# md -> pdf
pandoc README.md -s -o readme.pdf
# md -> html
pandoc README.md -s -o readme.html
```
(Conversion to `pdf` works only if you have LaTeX installed on your computer.)

- [Official Documentation](https://pandoc.org/getting-started.html)

1. Brendan add LaTeX to Word example
   
  
#### Ciation Mangers
##### Zotero

- [Zotero](https://www.zotero.org/): the actual program 
- [ZotFile](http://zotfile.com/): a zotero extension that allows to sync pdf annotations across devices (eg. tablet <=> laptop) ([github](https://github.com/jlegewie/zotfile))
- [How To](https://eighty-twenty.org/2018/06/13/mendeley-encrypted-db) decrypt your encrypted Mendeley data base for import with zotero (migrating all notes, annotations, links to pdfs and folder structures)

##### BibDesk
##### JabRef

<\details>
