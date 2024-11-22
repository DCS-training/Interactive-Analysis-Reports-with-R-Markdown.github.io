# Interactive-Analysis-Reports-with-R-Markdown

This workshop will help you create your own reproducible, customisable, and interactive analysis reports through R Markdown. By building on the basics of R, we will show you how to instantly prepare your results into a ready-made document (No more copy and pasting your results! Less human error!).

We will guide you on how to also create visually pleasing tables and plots, so that engagement can be maximized. To top it all off, you will also learn how to add interactive elements to the report. All of this will be designed into a html document, so that when it’s finished, your analysis can be communicated online with the world.

The workshop will be dedicated to exploring and learning the basics of R markdown documents, along with some basics of html (don’t worry, this will be kept at a very simple level). From there, we will learn how to create beautiful tables, and how to automate the reporting of your results section.

From there, we will learn how to support your tables with plots, and how to add interactive elements to your plot. We will also share some simple tricks on how to add other interactive elements to your report. Finally, we will show you how to host your report online through GitHub, so that you can better communicate your research with the world.

Aims:

* Learn to create interactive analysis reports with R.

* Creating and customising your own R markdown reports.

* Learn the basics of rendering documents through R markdown.

* Create beautiful tables to show off your results.

* Automating reporting.

* Supporting your tables with plots.

* Adding interactive elements, to increase engagement and accessibility of your report.


This is an intermediate-level course. You will need to already understand the basics of programming, preferably in R (i.e., having previous experience with tidyverse functions). Previous knowledge of statistical analysis is not required but will help you follow the content.

For those who want an additional challenge to their skills, we have included an example document of an interactive flexdashboard. It's built on a rmarkdown document, but contains some extra perks to play around with!

## R Setting Up

You can either run the code on your own machine or through Posit (RStudio Online IDE) or if you are part of the University of Edinburgh through [Noteable](https://noteable.edina.ac.uk/).
Below are the instructions for setting up. 


### On Posit

1. Go to https://posit.cloud/
2. Signup either via Gmail or GitHub
3. Go on New Project
4. New Project from Git Repository
5. Copy and Paste this repository URL  [https://github.com/DCS-training/Interactive-Analysis-Reports-with-R-Markdown.github.io](https://github.com/DCS-training/Interactive-Analysis-Reports-with-R-Markdown.github.io) as the Repository URL
6. The Project directory name will filled in automatically
7. Navigate to the rmd file you want to explore

### Locally

- R and RStudio are separate downloads and installations. R is the underlying statistical computing environment, but using R alone is no fun. RStudio is a graphical integrated development environment (IDE) that makes using R much easier and more interactive. You need to install R before you install RStudio. After installing both programs, you will need to install some specific R packages within RStudio. Follow the instructions below for your operating system, and then follow the instructions to install the needed packages(below)

_Windows_

- If you already have R and RStudio installed

  - Open RStudio, and click on "Help" > "Check for updates". If a new version is available, quit RStudio, and download the latest version for RStudio.
  - To check which version of R you are using, start RStudio and the first thing that appears in the console indicates the version of R you are running. Alternatively, you can type `sessionInfo()`, which will also display which version of R you are running. Go on the [CRAN website](https://cran.r-project.org/bin/windows/base/) and check whether a more recent version is available. If so, please download and install it. You can [check here](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#How-do-I-UNinstall-R_003f) for more information on how to remove old versions from your system if you wish to do so.

- If you don't have R and RStudio installed

  - Download R from the [CRAN website](https://cran.r-project.org/bin/windows/base/release.htm).
  - Run the `.exe` file that was just downloaded
  - Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
  - Under _Installers_ select **RStudio x.yy.zzz - Windows Vista/7/8/10** (where x, y, and z represent version numbers)
  - Double click the file to install it
  - Once it's installed, open RStudio to make sure it works and you don't get any error messages.

_macOS_

- If you already have R and RStudio installed

  - Open RStudio, and click on "Help" > "Check for updates". If a new version is available, quit RStudio, and download the latest version for RStudio.
  - To check the version of R you are using, start RStudio and the first thing that appears on the terminal indicates the version of R you are running. Alternatively, you can type `sessionInfo()`, which will also display which version of R you are running. Go on the [CRAN website](https://cran.r-project.org/bin/macosx/) and check whether a more recent version is available. If so, please download and install it.

- If you don't have R and RStudio installed

  - Download R from the [CRAN website](https://cran.r-project.org/bin/macosx/).
  - Select the `.pkg` file for the latest R version
  - Double-click on the downloaded file to install R
  - It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed by some packages)
  - Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
  - Under _Installers_ select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)** (where x, y, and z represent version numbers)
  - Double-click the file to install RStudio
  - Once it's installed, open RStudio to make sure it works and you don't get any error messages.

_Linux_

- Follow the instructions for your distribution from [CRAN](https://cloud.r-project.org/bin/linux), they provide information to get the most recent version of R for common distributions. For most distributions, you could use your package manager (e.g., for Debian/Ubuntu run `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we don't recommend this approach as the versions provided by this are usually out of date. In any case, make sure you have at least R 3.5.1.
- Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
- Under _Installers_ select the version that matches your distribution, and install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i rstudio-x.yy.zzz-amd64.deb` at the terminal).
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

Once you have R and R Studio installed, open R Studio

1.  Go to File>New Project> Version Control >Git
2.  Enter the Repository URL  [https://github.com/DCS-training/Interactive-Analysis-Reports-with-R-Markdown.github.io](https://github.com/DCS-training/Interactive-Analysis-Reports-with-R-Markdown.github.io)
3.  Select the Name for the directory project and where to save it
4.  Press Create Project

### On Noteable
1. Go to https://noteable.edina.ac.uk/login
2. Login with your EASE credentials
3. Select RStudio as a personal notebook server and press start
4. Go to File > New Project> Version Control > Git
5. Copy and Paste this repository URL [https://github.com/DCS-training/Interactive-Analysis-Reports-with-R-Markdown.github.io](https://github.com/DCS-training/Interactive-Analysis-Reports-with-R-Markdown.github.io) as the Repository URL (The Project directory name will filled in automatically but you can change it if you want your folder in Notable to have a different name).
6. Decide where to locate the folder. By default, it will locate it in your home directory
7. Press Create Project
Congratulations you have now pulled the content of the repository on your Notable server space.

  
