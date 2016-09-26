#Project 1 - How to Write a Paper
###Stats 159, Fall 2016, Zhongling Jiang
###ID:3032197416 Email:jzljohn18@berkeley.edu

##Abstract

> The purpose of this paper is to describe a systematic, standardized approach of writing a paper, using computational tools learned so far in this course such as bash, markdown, pandoc, Git, Github and so on. As the paper elaborates on each step of the process, it will also cover on the functionality of each tool, as well as the role they play in writing a paper.   
> The main body of this paper contains three parts. The first part -- Introduction part -- explains several main problems that is to be addressed in this paper. It will also provides with reader more background knowledge on these tools so as to prepare them for the following in-depth discussion. The second part -- dicussion -- which is also the most essential part of this paper, brings readers to more specific questions related to paper writing. In this section, the author would raise his personal viewpoint to these questions and descibes in great detail that all the steps he goes through to write a paper. The last part -- conclusions -- briefly summarizes the procedure and closes the discussion with some author's further thought on paper-writing. 

##Introduction 

Different from the concept of high school writing, the university-level writing focuses much more on the paper's [**reproducibility**](https://en.wikipedia.org/wiki/Reproducibility). The term reproducibility refers to "**the ability of scientific study to be duplicated, either by the same researcher or by someone else working independently**" [1].  So the question that how to integrate the idea of reproducibility into writing a paper becomes the key topic that navigates through this paper. An outline of dicussion:   

* Building a file directory 
* Monitor all the actions 
* Create a markdown file
* Possible difficulties and Issues 

Among the four major topics, the first three are more techique-related, while the last one is more empirical. An important concept needed to stressed here is that creating a paper needs much more than a single .txt or .docx file. It needs a set of files, called **directory**, where all files have more complicated nested relationship. Why do we need a directory? The answer is, again, [**reproducibility**](https://en.wikipedia.org/wiki/Reproducibility). The author should not only present his/her paper, but also supply all relevant material that is critical to the paper itself. And the purpose of the directory is to help organize all files in a neat way.  

Another topic is about how to monitor user's actions when creating a paper. The purpose is also keeping tracking of what user does at each step so that the user could revise easily. The software that we use here is [**Git**](https://git-scm.com), a version control system used for monitoring workflow. In addition,  [**Makefile**](https://en.wikipedia.org/wiki/Make_software) helps simplify the file building process, which will also be covered in this paper. 

At last, the paper will discuss the role of [**Github**](https://en.wikipedia.org/wiki/GitHub) in the scientific reproducibility, with some demonstrations on pushing and pulling files from Github through the use of Git. 

[1]: the definition from wikipedia:  [https://en.wikipedia.org/wiki/Reproducibility](wikipedia:https://en.wikipedia.org/wiki/Reproducibility)##Discussion

The discussion would be mainly led by a series of questions and introductions of softwares that are used in writing a paper. 

#### 1. Makefile 
With the help of Makefile, the entire file-building process becomes easier. It resembles the shell programming except that it also focuses on dependencies among files. For example,



#### 2. Git   
Git is a version control system. Simply speaking, it manages all the changes made to use files, computer programs, and all other information. The role it plays in reproducible research is that it records each step of change that a user performs during his research, e.g. adding/deleting files, editing files, creating html, etc. Here are some code:

    git init
    touch file1.txt
    git add file1.txt  # put file1.txt under monitor
    git commit -m "add file1"   # commit the change
Another important functionality of Git is that it allows user to undo unintended changes by simply use

    git checkout 

#### 3. Github
Github is a **web-based** Git repository hosted service [1]. It uses Git's distribution version control functionality, and adds its own features such as access control and collatoration. User could share their source code through this platfrom by uploading. They could also invite collaborators to work on the code together. In this assignment, I would also upload all files and reports on the Github. This is an important part for upholding scientific reproducibility. 

[1] From Wikipedia: https://en.wikipedia.org/wiki/GitHub
#### 4. Pandoc
Pandoc converts one type of file into another. For exmaple, it can covert documents in markdown, HTML, Latex, etc. Below are examples:  
Converting markdown file into latex：

     pandoc file.md -f markdown -t latex -s -o file1.tex
Converting markdown to pdf (without detail -f -t):  

     pandoc file1.md -s -o file1.pdf
With pandoc, we could easily convert files into required formats using command line

#### 5. Markdown 
Markdown is one of the most essential tools for generating the report. More specifically, Markdown is a "_markup language with plain text formatting designed syntax_"[2] so that it could be converted to an HTML easily. This report is a result of using Markdown for editing all texts.

 [1]: from wikipedia: https://en.wikipedia.org/wiki/Markdown

#### 6. Questions 

1. Describe resources is used to get the job done: 

Online tutorials of all above mentioned softwares, and wikipedia. 

2.  What are the easy part? challenging part? 

The easier part is to describe the usage and functionalities of these softwares, including giving code examples. However, the harder part are using git to monitor the entire process, from creating directories to editing all files. Another hard thing is to upload all your changes to Github by using pull and push commands.

3.  Things that I am stuck with:

Makefile   

4.  What is the most time consuimg part?

5.  Whether I work with or receive help from others? 

6.  How much time does it take?













 
 
##Conclusion