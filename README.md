# Resources and Tutorials
Below is a compiled list of various resources and tutorials, both internal and external, for tools, programming tricks, and tutorials related to science reform, reproducibiluty, and open data science in the department.
We can break this into sub pages as it grows.
## Data Management
### Exiftool
### Hashing
SHA-1 (Secure Hash Algorithm 1) is a cryptographic has function that takes an input and produces a unique hash value (often a 40 digit hexadecimal number) designed by the NSA. An object creates a new has, but that hash cannot be used to identify the original object (it is encrypted). It is relevant to us as reaserchers for 2 reasons.
1. Files (images, mp3, csvs, .doc, pdf) can have a unique hash based on the , allowing us to inventory files. 
This hash is based on the underlying code, unique to each file, and does not change in case the file name changes.
This allows us to inventory files, and ensure there are not duplicates or lost cases, before we performa analysis. 
This is particularly useful when there are multiple people creating multiple copies of data in the field, and when data ends up going out to collaborators (who are not as tidy as us).
2. Unique, encrypted hashes can be created for unique individuals, field sites, samples, speicies, integer, or any text object. 
This is useful as we can append hash metadata to different files, to build relational databases that are resistant to transcription errors.
We can also use hashes to prublish reproducible code with annonymized individual or location information if there are privacy or conservation converns
### ReadMe files
### Best naming practices
## Version Control with Git

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

### Further Resources

**git:**
- the original *git* [homepage](https://git-scm.com/) (with *git* [documentation](https://git-scm.com/book/en/v2))
- *git* for [windows](https://gitforwindows.org/index.html) users
- the *git* intro slides from the ODS workshop ([pt I]() (not available? can replace with [my own one (kh)](https://k-hench.github.io/git/git.html)) and [pt II](https://k-hench.github.io/git/gitII.html))
- the *git* [discussion slides](https://github.com/livingingroups/ODS/blob/main/week.10/Version%20Control%20with%20git(Hub).pdf) from the ODS workshop
- the [Atlassian terminal tutorial](https://www.atlassian.com/git) from the makers of Bitbucket
- the [Software Carpentry Tutorial](https://swcarpentry.github.io/git-novice/)
- ...

**github:**
- [Github](https://github.com/): The most heavily used, and well known provider of Internet hosting for software development and version control using Git. You are on it now. Owned by Microsoft
- [Bitbucket](https://bitbucket.org/): Another commonly used, open source code version control site.
- the [*github* group](https://github.com/livingingroups) of the EAS

**Git GUI Clients**
- [RStudio](https://www.rstudio.com/): RStudio has a great built in Git Interface. [Tutorial here](https://happygitwithr.com/).
- [GitKraken](https://www.gitkraken.com/): As taught in the EoAS Workshop.
- [GitHub Desktop](https://desktop.github.com/): a GUI by the developers of github (only on windows or mac)
- [Sublime Merge](https://www.sublimemerge.com/): Another GUI that works Seamlessly with SublmeText, a great open source mutli (programming) language text editor
- [Visual Studio](https://visualstudio.microsoft.com/): an cross-platform integrated development environment (IDE, aka text editor on steroids). Heavily customizable and convenient environment that also manges git

## Programming Languages
### R
#### Intoduction to R Tutorials
#### Creating Packages in R
### Python
### [mcSTAN](https://mc-stan.org/)
STAN is the most commonly used Hamiltonian MCMC proabailistic sampling engine for Bayesian inference. It can be implented in R, Python, Linux Shell, MatLab, Mathematica, Julia, Stata, and Scala.
For R users, there are several "convenience" wrappers that can fir simple hierarchical models (and more) in stan.
1. [rethinking pacakage](https://github.com/rmcelreath/rethinking) and Richard McElreaths accompanying textbook.
2. [brms](https://github.com/paul-buerkner/brms) fits STAN generlized linear regressions using lme4 syntax
3. [rstanarm](https://github.com/stan-dev/rstanarm)
### Bash aka Linux Terminal

## Manuscript Preparation
### LaTeX
LaTeX is a plain text document preapartion editor that uses the TeX language. 
It typsets plain text files. It integrates with BibTeX, an open source citation manager service. 
LaTeX is great for complicated mausccripts (i.e. dissertations and books) and manuscripts with alot of mathematical notation. 
It can also be used to make slides for presenatations. 
TeX documents can also be versioned controlled on GitHub. 
Many journals also have LaTeX templates one may use for submission.
#### (Overleaf)[https://www.overleaf.com/project]
Here is a [Youtube Video Tutorial](https://www.youtube.com/watch?v=5dnK2knSu0Q&t=2s) and [sample document](https://www.overleaf.com/project/5c3c4116de500c6cd5652f2f) for collaborative document preparation using Overleaf. 
Overleaf also integrated with GitHub for document version control..
#### (ShareLaTeX)[https://www.sharelatex.com/]
This is a similar collaborative LaTeX document preparation. 
The University has a free Pro account.
This has merged with Overlead
### Markdown
Markdown is a lightweight markup language for created formatted text, whose source code is human readable.
These are saved as `.md` or `.mdown` file extensions.
This page you are currently reading now and any GitHub readme is written in Markdown.
1. [Tutorial in multiple languages](https://www.markdowntutorial.com/)
2. [GitHub Markdown Tutorial[(https://guides.github.com/features/mastering-markdown/]
### RMarkdown
RMarkdown is another programming language that integrated R code with Markdown style writing to integrate text, Rcode, and R terminal output. 
It can be used to publish HTML (whichcan be publiched as websites), PDF, and MS word documents where code and the products of code are desirealbe to share. 
It is great to share intermediate results, write living documents (can be integrated wit BibTeX for citations) where results in text can be changed if analysis changes or more data is added, or publish tutorials and websites.
### PanDoc
Useful resource to translate document types (i.e. PDF to LaTeX to Word to Markdown to .txt)
1. Brendan add LaTeX to Word example
#### Ciation Mangers
##### Zotero
##### BibDesk
##### JabRef

