Software, Programs and Tools for the Scientific Workflow
================
10 April, 2017

-   [The Scientific Workflow (Source:
    <http://r4ds.had.co.nz/introduction.html>)](#the-scientific-workflow-source-httpr4ds.had.co.nzintroduction.html)
-   [SPT's for scientific writing](#spts-for-scientific-writing)
    -   [LaTeX](#latex)
    -   [Markdown](#markdown)
-   [SPT's for statistical and data
    analysis](#spts-for-statistical-and-data-analysis)
    -   [R](#r)
    -   [Stata](#stata)
-   [SPT's for visualization](#spts-for-visualization)
    -   [ggplot2](#ggplot2)
    -   [ggvis](#ggvis)
    -   [TikZ](#tikz)
    -   [Shiny](#shiny)
-   [SPT's for presentations](#spts-for-presentations)
    -   [Latex-beamer](#latex-beamer)
    -   [IoSlide and Slidy](#ioslide-and-slidy)
-   [SPT's that bring 'em all
    together](#spts-that-bring-em-all-together)
    -   [Pandoc](#pandoc)
    -   [Knitr](#knitr)
    -   [RMarkdown v2](#rmarkdown-v2)
    -   [Jupyter](#jupyter)
    -   [Git and GitHub](#git-and-github)
-   [Miscellaneous SPT's](#miscellaneous-spts)
    -   [Virtual Box](#virtual-box)
    -   [ShareX](#sharex)
    -   [JabRef](#jabref)
    -   [PureSync](#puresync)

This is a collection of useful software, programs and tools (SPT's) that
in some way or another help ease the scientific workflow. While the term
"scientific workflow" may mean different things to different
disciplines, I explicitly assume a data-driven workflow which implies
that at some point within the process of answering a scientific
question, data comes into play. While studying the scientific workflow
as such is interesting - especially from a developers perspective - it
is sufficient to think of it as a circle of three mutually dependent
parts:

-   Get, manage, and clean data
-   Analysis data - Visualize, model, transform
-   Communicate results - Write, present, share

This is nicely summarized in the following graphic that has been
popularized by [Hadley Wickham](http://hadley.nz/), the author of many
useful R packages and excellent books (see below).

#### The Scientific Workflow (Source: <http://r4ds.had.co.nz/introduction.html>)

![ssdsd](http://r4ds.had.co.nz/diagrams/data-science.png)

When talking about SPT's that help ease the scientific workflow I have
this workflow in mind.

The SPT's are roughly grouped by their main purpose, although this is by
no means a sharp distinction as most SPT's are useful for different
tasks within the circle. Help, documentation, tutorials and examples for
each of the SPT's mentioned below may easily be found on
[Google.com](https://www.google.de). I will, however, mention
recommended reading if I find something particularly useful.

------------------------------------------------------------------------

SPT's for scientific writing
----------------------------

Scientific writing poses challenges that regular word processors such as
[Microsoft Word](https://products.office.com/de-de/word) or
[OpenOffice](https://www.openoffice.org/de/) are not designed for, most
notably

-   extensive use of mathematical characters and symbols
-   ability to control the layout in detail
-   state of the art style requirements
-   convertibility between different formats (e.g. .pdf and .html)
-   reproducibility and cross-platform independence
-   seamless integration with other SPT's within the scientific workflow
    in particular the connection between computer code/output
    and writing.

### LaTeX

[LaTeX](https://www.latex-project.org/) is a free and open-source
high-quality typesetting system. It may be used for pretty much anything
related to typesetting whether it is a short technical paper or
presentation trenched in mathematical symbols, graphs and tables or a
lengthy book with many chapters and detailed style guidelines. Since
[LaTeX](https://www.latex-project.org/) includes features that are
explicitly designed for the production of technical and scientific
writing (e.g. mathematical notation and detailed control of the
bibliography), it excels at that and has hence become the de facto
standard for the communication and publication of scientific documents.
While learning [LaTeX](https://www.latex-project.org/) requires more
effort than learning [Microsoft
Word](https://products.office.com/de-de/word) (at least initially) it
has many advantages that make the initial effort worthwhile, in
particular for those that regularly use mathematical notation.

Installation:

-   For Windows: [MikTeX](http://miktex.org/) or
    [proTeXt](http://www.tug.org/protext/)
-   For Mac: [MacTeX](http://www.tug.org/mactex/)
-   Unix/Linux: [TeX Live](http://www.tug.org/texlive/)

Recommended Editors: [TeXMaker](http://www.xm1math.net/texmaker/),
[TeXstudio](http://texstudio.sourceforge.net/)

### Markdown

[Markdown](https://guides.github.com/features/mastering-markdown/) is a
very simple markup language with plain text formatting syntax that was
designed to be as easy-to-read and easy-to-write for humans as possible.
Originally, documents written in standard
[Markdown](https://guides.github.com/features/mastering-markdown/) were
only intended to be converted to HTML, however, in particular with the
introduction of [Pandoc](http://pandoc.org/index.html), the number of
formats increased significantly now supporting well known formats such
as .pdf and .docx ([Microsoft
Word](https://products.office.com/de-de/word)).
[Markdown](https://guides.github.com/features/mastering-markdown/) is
standard in most scientific forums and platforms, most notably
[StackOverflow](http://stackoverflow.com/) and
[GitHub](https://github.com/), although each of them uses a different
[Markdown](https://guides.github.com/features/mastering-markdown/)
dialect (extension). The number of different dialects that have evolved
since the original
[Markdown](https://guides.github.com/features/mastering-markdown/)
language was first introduced in 2004 may be a bit confusing to
newcomers, however, they are largely compatible amongst each other.

Text written in
[Markdown](https://guides.github.com/features/mastering-markdown/) is
basically regular text with some additional "comments" like "\#" that
tell the processing engine what it should do with the text (in this
case: "\#" tells the engine to convert the line following the "\#" to
the appropriate html code indicating a first-level header). Allowing
only a small set of such "comments", it is easy to learn, yet powerful
enough to cover most of the formatting tasks you usually want to do
while leaving the rest to more advanced programs such as
[LaTeX](https://www.latex-project.org/). In this respect, although
fundamentally different, it may be seen as at "LaTeX-light".

The major advantages of
[Markdown](https://guides.github.com/features/mastering-markdown/),
besides simplicity, are state of the art styling, convertibility, and
seamless integration with other SPT's such as
[R](https://www.r-project.org/), [GitHub](https://github.com/),
[Jupyter](http://jupyter.org/) or [Shiny](http://shiny.rstudio.com/).

Installation: none needed  
Recommended Editor: [Atom](https://atom.io/),
[RStudio](https://www.rstudio.com/)

------------------------------------------------------------------------

SPT's for statistical and data analysis
---------------------------------------

Statistical analysis is at the heart of the answer to most scientific
questions. This is especially true for questions related to economics
and/or businesses management. While classical statistical and
econometric *theory* does not necessarily require the use of computer
software, actual *application* and data analysis in general is
inherently computer driven. Furthermore modern statistics (like neural
nets or Monte Carlo simulation) by and large evolved around computer
driven progress and may thus be seen as inherently computer-dependent.
This is emphasized by a quote in the 2016 book [Computer Age Statistical
Inference](https://web.stanford.edu/~hastie/CASI/) by Bradley Efron and
Trevor Hastie, two of the most famous statisticians/computer scientists:

> Almost all topics in twenty-first century statistics are now
> computer-dependent \[...\]

Hence, a set of SPT's that help built, explore, evaluate, and interpret
models of any complexity is therefore indispensable. While standard
spread sheet programs such as [Microsoft
Excel](https://products.office.com/de-de/excel) do have its benefits, it
is important to realize that they are not designed for more complex
statistical tasks. Additionally, they usually only poorly integrate with
other SPT's, which is a major obstacle in the scientific workflow. See
e.g.
[this](http://ekonometrics.blogspot.de/2015/12/not-so-sweet-sixteen.html)
post.

### R

[R](https://www.r-project.org/) is an open-source software environment
for statistical computing and graphics. It is a primarily a command
language, although a graphical user interface (GUI) called
[RCommander](http://www.rcommander.com/) may be used. Compared to
software such as [EViews](http://www.eviews.com/home.html),
[Stata](http://stackoverflow.com/),
[SPSS](https://de.wikipedia.org/wiki/SPSS) or
[Gretl](http://gretl.sourceforge.net/) it has a relatively steep
learning curve - although the initial hurdle has been considerably
lowered over the last years, thanks to tutorials, introductory videos,
well written books and tons of detailed and easy-to-read documentation.
The learning curve is usually an obstacle for those new to
[R](https://www.r-project.org/), however, as mentioned above and as
described
[here](https://thetarzan.wordpress.com/2011/07/15/why-use-r-a-grad-students-2-cents/)
and [here](http://www.inside-r.org/why-use-r), there are numerous
reasons why [R](https://www.r-project.org/) should nevertheless be your
pick as statistical software, most notably:

-   It is free
-   [R](https://www.r-project.org/) forces you to think about what you
    want to do
-   By seamlessly integrating with other SPT's
    [R](https://www.r-project.org/) open the door to a world of other
    SPT'S (and incredibly important aspect that as of March 2017 no
    other software is able to beat)
-   Conceptually intuitive, uniform data cleaning and transformation
    capabilities (thanks to the [tidyverse](http://tidyverse.org/)
    (including packages such as `dplyr`, `tidyr`, `purrr`, `readr` and
    `magrittr`) and its underlying philosophy as described in [this
    paper](https://www.jstatsoft.org/article/view/v059i10) by [Hadley
    Wickham](http://hadley.nz/)), unparalleled visualization
    possibilities (thanks to packages such `ggplot2` and (in the future)
    `ggvis`), and almost every model function you can think of (thanks
    to over 6000 packages on CRAN alone as of April 2016).
-   A vibrant and helpful community.

Installation: [CRAN](https://cran.r-project.org/)  
Recommended Editor: [RStudio](https://www.rstudio.com/)  
Recommended Reading:

-   Norman Matloff: *The Art of R Programming*
-   Hadley Wickham: [R for Data Science](http://r4ds.had.co.nz/*)
-   Hadely Wickham: [Advanced R](http://adv-r.had.co.nz/)

### Stata

[Stata](http://stackoverflow.com/) is a powerful commercial software for
data analysis and graphics. It has a relatively simple syntax mitigating
the initial pain associated with learning a new language.
[Stata](http://stackoverflow.com/) has outstanding documentation for its
functions as well as for the mathematical concepts underlying these
functions. There are good reasons to learn
[Stata](http://stackoverflow.com/) and in fact, I think mastering both
[Stata](http://stackoverflow.com/) and [R](https://www.r-project.org/)
is ideal as it allows to combine the best of both.

------------------------------------------------------------------------

SPT's for visualization
-----------------------

Visualization is an integral part of the data analysis. Proper
visualization does not only help to summarize what you already know but

> it forces us to notice what we never expected to see (John Tukey).

While there are many aspects to what makes visualization good (see e.g.
[this](http://www.amazon.de/Show-Me-Numbers-Designing-Enlighten/dp/0970601972)
brilliant book by Stephen Few, or literately anything written by Edward
Tufte), this section only describes helpful tools to be used in creating
objectively good and meaningful visualizations.

### ggplot2

[ggplot2](https://github.com/hadley/ggplot2) is **the**
[R](https://www.r-project.org/) package for producing statistical and/or
data graphics, written by [Hadley Wickham](http://hadley.nz/), one of
the most productive - if not the most productive - member of the
[R](https://www.r-project.org/) family. It has become the de facto
standard for displaying graphics made with
[R](https://www.r-project.org/). Unlike most other graphics packages in
[R](https://www.r-project.org/) - or any other statistical program for
that matter - it does not only provide a set of commands useful to
produce beautiful, hassle-free graphics but aims higher by building on a
deep underlying **grammar of graphics**. This is what makes
[ggplot2](https://github.com/hadley/ggplot2) so powerful! Learning the
grammar will not only help new users to master the many commands used in
producing a high class graphic, but will also force you -or, to put it
more mildly, help you- to think about what a specific graphic should
contain. The importance of [ggplot2](https://github.com/hadley/ggplot2)
cannot be overstated and should be a must-use for any serious
visualization attempt .

Installation: `install.packages("ggplot2")` in your R console  
Recommended Reading:

-   Hadley Wickham: [ggplot2: Elegant Graphics for Data
    Analysis](http://www.springer.com/de/book/9783319242750)
-   Hadley Wickham: [R for Data Science](http://r4ds.had.co.nz/*)
-   Winston Chang: [*R Graphics
    Cookbook*](http://www.amazon.de/R-Graphics-Cookbook-Winston-Chang/dp/1449316956/ref=pd_bxgy_14_img_3?ie=UTF8&refRID=1X86HJ6XDM6N9HDH32ZR)
-   [Data Visualization Cheat
    Sheet](https://www.rstudio.com/resources/cheatsheets/)

### ggvis

[ggvis](http://ggvis.rstudio.com/) is a still-in-active-development
[R](https://www.r-project.org/) package for data visualization. Like
[ggplot2](https://github.com/hadley/ggplot2), it centers around the
grammar of graphics, but adds interactivity by incorporating
[shiny](http://shiny.rstudio.com/)'s' reactive programming model. The
package is still in its very early stages and is likely to undergo
significant changes in the future, however, it is definitely worth
keeping an eye on it's development as it is probably going to set the
standard of interactive visualization in a couple of years.

Installation: `install.packages("ggvis")` in your R console

### TikZ

[TikZ](https://www.google.de/search?q=tikz&ie=utf-8&oe=utf-8&gws_rd=cr&ei=KLZlVqaKNcKWPIKYq5gP#)
is a Tex package that offers a huge amount of commands to produce vector
graphics of any kind. As
[TikZ](https://www.google.de/search?q=tikz&ie=utf-8&oe=utf-8&gws_rd=cr&ei=KLZlVqaKNcKWPIKYq5gP#)
is to be used in (La)TeX, fonts and appearance beautifully go along with
that of LaTeX. Once installed, learning
[TikZ](https://www.google.de/search?q=tikz&ie=utf-8&oe=utf-8&gws_rd=cr&ei=KLZlVqaKNcKWPIKYq5gP#)
is comparably simple but can be quite time consuming when a certain
flexibility is needed. There is a [great
documentation](http://pgf.sourceforge.net/pgf_CVS.pdf) for all of
[TikZ](https://www.google.de/search?q=tikz&ie=utf-8&oe=utf-8&gws_rd=cr&ei=KLZlVqaKNcKWPIKYq5gP#)
features but being more than 1200 pages strong, this documentation is
overwhelming at first but very helpful once you know your way around its
content.

Installation: `usepackage(tikz)` in your LaTeX preamble.  
Recommended Editor: [TikzEd](http://www.tikzedt.org/),
[TeXMaker](http://www.xm1math.net/texmaker/)

### Shiny

[Shiny](http://shiny.rstudio.com/) is an [R](https://www.r-project.org/)
package created by [RStudio](https://www.rstudio.com/) that provides a
framework to build beautiful, interactive web application without
extended knowledge of HTML, CSS or JavaScript. The commands necessary to
write basic and intermediate shiny application are surprisingly easy to
learn, however, a working knowledge of JavaScript and HTML is probably
very handy for more complex projects. As all the statistical work is
done in [R](https://www.r-project.org/), a proper knowledge of how to do
things in [R](https://www.r-project.org/) is required. While
[Shiny](http://shiny.rstudio.com/) is by no means confined to
visualization, it is particularly helpful when combined with
[ggplot2](https://github.com/hadley/ggplot2) to produce beautiful
graphics that can be changed on the fly.

Installation: `install.packages("shiny")` in your R console  
Recommended Editor: [RStudio](https://www.rstudio.com/)  
Recommended Tutorial: The best way to learn Shiny is to use the
[tutorial on the Shiny webpage](http://shiny.rstudio.com/tutorial/).  
Recommended Reading: [Interactive web apps cheat
sheet](http://www.rstudio.com/wp-content/uploads/2016/01/shiny-cheatsheet.pdf)
and literally anything that [Dean Attali](http://deanattali.com/)
writes.

------------------------------------------------------------------------

SPT's for presentations
-----------------------

### Latex-beamer

The beamer class is used to create presentation slides with
[LaTeX](https://www.latex-project.org/). As it is a
[LaTeX](https://www.latex-project.org/) class, it is perfectly suited
for high-quality presentations that make extensive use of mathematical
notations and symbols and require fine control over the appearance.

Installation: A working [LaTeX](https://www.latex-project.org/)
installation such as [MikTeX](http://miktex.org/).  
Recommended Editor:

-   [TexMaker](http://www.xm1math.net/texmaker/) if you want to create
    the presentation directly with Latex.
-   [RStudio](https://www.rstudio.com/) if you want to create a beamer
    presentation from an R Markdown file using `beamer_presentation` in
    you YAML header.

Recommended Reading: [Beamer User
Guide](http://sunsite.informatik.rwth-aachen.de/ftp/pub/mirror/ctan/macros/latex/contrib/beamer/doc/beameruserguide.pdf)

### IoSlide and Slidy

Both IoSlides and Slidy are web-based alternatives to standard pdf
presentations. IoSlides or Slidy slides are basically html pages that
can be run directly within the browser. This makes them highly shareable
and portable. Slides are best from within RStudio created by knitting an
R Markdown file using `ioslide_presentation` or `slidy_presentation` in
your YAML header.

------------------------------------------------------------------------

SPT's that bring 'em all together
---------------------------------

### Pandoc

Pandoc is a universal markup language document converter written by John
MacFarlane. You can pass any documents written in a markup language like
LaTeX, Markdown, HTML to Pandoc and convert these from one format to
another including different slide show formats, HTML code and pdf (try
it out yourself [here](http://pandoc.org/try/). Pandoc works best,
however, if given a (R)Markdown file as input. Pandoc is not that easy
to use (requires a command line) but as it is nicely integrate into the
[RStudio](https://www.rstudio.com/) IDE via the R Markdown package,
there is usually no need to use it directly, although its good to know
that it exists in case you need it.

### Knitr

First of all, [Knitr](http://yihui.name/knitr/) is an
[R](https://www.r-project.org/) package. More importantly, however, it
is a general-purpose literate programming engine. Literate programming
is a term coined by Donald Knuth the creator of the TeX typesetting
system. It basically centers around the idea that programming does not
only consist of writing many lines of code but, equally important, it
involves writing a narrative that explains what the code actually does
and how the program or its functions are supposed to be used.
Traditionally, this was done by either writing comments directly in the
source file, or by writing a separate documentation. The former has the
obvious drawback of being limited to almost no formatting possibilities
and requires the readers to be able to open and understand the source
file. While the latter approach is better it still has major
shortcomings, mainly:

-   it involves lots of human effort (copy-and-pasting)
-   it is error-prone due to copy-and-pasting
-   inherently static: if results depend on previous results, the whole
    chain has to be manually rewritten if any of the results within the
    chain are changed.
-   it is likely to produce layout conflicts and inconsistent styling
    which

[Knitr](http://yihui.name/knitr/) enables the use of both program code
and sophisticated comments within one single document. Although
[Knitr](http://yihui.name/knitr/) is an [R](https://www.r-project.org/)
package it does not only support R but the most often used document
formats such as LaTeX, HTML, Markdown and a broad variety of other
programming languages such as Python, Julia or even (after some
tweaking) Stata. [Knitr](http://yihui.name/knitr/) is tightly integrated
into [RStudio](https://www.rstudio.com/) but does not depend on it.

Recommended Reading:

-   Yihui Xie - Dynamic Documents with R and knitr

### RMarkdown v2

R Markdown is an [R](https://www.r-project.org/) package that is usually
referred to R Markdown v2 to distinguish it from an earlier version. It
basically brings Markdown, [Knitr](http://yihui.name/knitr/) and
[Pandoc](http://pandoc.org/index.html) together. It enables easy
creation of dynamic documents (via [Knitr](http://yihui.name/knitr/)) in
different formats (via [Pandoc](http://pandoc.org/index.html)) including
Pandoc's version of the Markdown language. Similar to
[Knitr](http://yihui.name/knitr/), it is tightly integrated into the
[RStudio](https://www.rstudio.com/) IDE making it extremely easy to use
(literally one click is sometimes enough). Recommended Reading:

-   [This](http://www.introductoryr.co.uk/Reproducibility/Markdown_guide.html)
    is a very good, detailed but also long intro to
    [RMarkdown](http://rmarkdown.rstudio.com/) and reproducible research
    in general.
-   [R Markdown cheat
    sheets](https://www.rstudio.com/resources/cheatsheets/)

### Jupyter

As explained [on its homepage](http://jupyter.org/)
[Jupyter](http://jupyter.org/) is a web application that allows you to
create and share documents that contain live code, equations,
visualizations and explanatory text. Uses include: data cleaning and
transformation, numerical simulation, statistical modeling, and much
more. While its predecessor, IPython notebook, was only built to work
with Python, [Jupyter](http://jupyter.org/) supports many other
languages such as Julia and R, although both Kernels are still in its
early stages. This is, by the way, where the name is coming from, as
[Jupyter](http://jupyter.org/)is an acronym for Ju(lia)Py(ton)te(R). The
difference between [knitr](http://yihui.name/knitr/) and
[Jupyter](http://jupyter.org/) is that the latter allows for live code
and text evaluation. While R Markdown files need to be compiled for
evaluation to take place, code cells in a [Jupyter](http://jupyter.org/)
notebook are evaluated on the fly. This makes
[Jupyter](http://jupyter.org/) highly recommendable for interactive
teaching of programming since students can follow live and take notes
while the instructor dynamically changes the code in response to
questions and suggestions.

Installation:

### Git and GitHub

[GitHub](https://github.com/) is primarily a code sharing and
collaboration platform that is build around [Git](https://git-scm.com/),
a highly sophisticated version control system that is nowadays used by
many open source developers worldwide. While developing software is
probably not really that interesting to students,
[GitHub](https://github.com/) is nevertheless very useful when working
together on a project that involves writing code of any kind. Even when
not working on an own project, knowing your way around
[GitHub](https://github.com/) is indispensable when you have an interest
in anything related to coding as this would sooner or later lead you to
[GitHub](https://github.com/) .

Installation: Start [here](https://help.github.com/articles/set-up-git/)

------------------------------------------------------------------------

Miscellaneous SPT's
-------------------

### Virtual Box

[Virtual Box](https://www.virtualbox.org/) lets you set up a virtual
machine on your local computer. This is especially useful if you want to
have Linux running in parallel on a windows machine (or the other way
around) and don't want the inconvenience of a dual boot machine. When
setting up the machine the user can choose how much of the computer
resources (such as RAM, Disk Space etc.) the virtual machine should be
able to use.

### ShareX

[ShareX](https://getsharex.com/%5D) is a free, modern screen capturing,
screen recording tool. The tool allows capturing a screenshot in a
variety of modes, such as full screen, window, monitor, rectangle,
polygon and more. ShareX also offers various after-capture tasks like
annotating, adding effects, watermarking, uploading and printing. It
conveniently saves screenshots as a regular .png or as url for immediate
sharing.

### JabRef

[JabRef](http://www.jabref.org/) is a jave-based open source
bibliography reference manager that helps you organize your books,
papers and other documents. It is designed to work with
[LaTeX](https://www.latex-project.org/) as it stores its information in
[LaTeX'](https://www.latex-project.org/) native BiTeX style. Hence, it
is the ideal tool for storing and organizing your
[LaTeX](https://www.latex-project.org/) bibliography.

<!-- ### BibSonomy:scraping -->
<!-- The [bibsonomy::scraping service](http://scraper.bibsonomy.org/) can be given  -->
<!-- any url that contains bibliography information in its HTML code. Once given an url,  -->
<!-- the web scraper search the HTML code for bibliography information and returns it  -->
<!-- as BibTeX code which can immediately be used in [LaTeX][Latex] bibliography  -->
<!-- file (.bib)  or more conveniently in JabRef. In my experience the pipeline  -->
<!-- Scraping -> JabRef -> LaTeX is the quickest and cleanest way to get your  -->
<!-- bibliography information into LaTeX. A list of supported web pages that  -->
<!-- allow scraping may be found [here](http://www.bibsonomy.org/scraperinfo). -->
### PureSync

[PureSync](https://www.jumpingbytes.com/puresync.html) is a free
software - for personal use only, a professional version is available
but not necessary - that lets you automate internal and external files
and folders synchronization on your computer. This is usually only of
interest to Windows users as Mac offers a nice standard backup system.
There are many similar programs that might be equally good.
