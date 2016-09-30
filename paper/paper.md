#Project 1 - How to Write a Paper
###Stats 159, Fall 2016, Zhongling Jiang
ID:3032197416   
Email:jzljohn18@berkeley.edu

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

[1]: the definition from wikipedia:  [https://en.wikipedia.org/wiki/Reproducibility](wikipedia:https://en.wikipedia.org/wiki/Reproducibility)  


##Discussion

The discussion would be mainly led by a series of questions and introductions of softwares that are used in writing a paper. 

#### 1. Makefile 
With the help of Makefile, the entire file-making process becomes easier. It resembles the shell programming except that it also focuses on dependencies among files. The code takes the following form: All actions is acted upon a single file target, whose creation may or may not depend on other files.

    [target]: [dependent files]
    		actions 

#### 2. Git   
Git is a version control system. Simply speaking, it manages all the changes made to use files, computer programs, and all other information. The role it plays in reproducible research is that it records each step of change that a user performs during his research, e.g. adding/deleting files, editing files, creating html, etc. Here are some code:

    git init
    touch file1.txt
    git add file1.txt  # put file1.txt under monitor
    git commit -m "add file1"   # commit the change
Another important functionality of Git is that it allows user to undo unintended changes by simply use

    git checkout 

![](../images/git-logo.png)


#### 3. Github
Github is a **web-based** Git repository hosted service [1]. It uses Git's distribution version control functionality, and adds its own features such as access control and collatoration. User could share their source code through this platfrom by uploading. They could also invite collaborators to work on the code together. In this assignment, I would also upload all files and reports on the Github. This is an important part for upholding scientific reproducibility. The way to use Github by using Git is following:

After having committed all changes in Git, we push the local repository as well as all commit messages to Github:

    git remote add [SSH URL]
    git push origin master 
[1] From Wikipedia: https://en.wikipedia.org/wiki/GitHub  

![](../images/github-logo.png)



#### 4. Pandoc
Pandoc converts one type of file into another. For exmaple, it can covert documents in markdown, HTML, Latex, etc. Below are examples:  
Converting markdown file into latex：

     pandoc file.md -f markdown -t latex -s -o file1.tex
Converting markdown to pdf (without detail -f -t):  

     pandoc file1.md -s -o file1.pdf
With pandoc, we could easily convert files into required formats using command line

![](../images/git-logo.png)

#### 5. Markdown 
Markdown is one of the most essential tools for generating the report. More specifically, Markdown is a "_markup language with plain text formatting designed syntax_"[2] so that it could be converted to an HTML easily. This report is a result of using Markdown for editing all texts.

 [1]: from wikipedia: https://en.wikipedia.org/wiki/Markdown
 
![](../images/markdown-logo.png)

#### 6. Questions 

* Describe resources that is used to get the job done: 

	Online tutorials of all above mentioned softwares, consulting with professor and teaching assistant, and wikipedia 

* What are the easy part? challenging part?   

	The easier part is creating directories and empty files in command lines. However, the harder part are using git to monitor the entire process, from creating directories to editing all files. Another hard thing is to upload all your changes to Github by using pull and push commands.

* Things that I am stuck with:

	Using Makefile to concatnate four markdown files under 'section' directory to create the 'paper.md' under 'paper' directory. It involves file dependence.  
	Secondly, it takes me quite a long time before I find I do not have a public SSH key to push any document. So there has been a time I am wondering why I could not push anything to Github.

*  What is the most time consuimg part?  
	Describe the usage and functionalities of these softwares, including giving code examples. 


*  Whether I work with or receive help from others?   
	Lab assistant Sindhuja gives me help on using Makefile to generate file dependence. 

*  How much time does it take?  
	It takes several days to finish. 













 
 
##Conclusion

The report mainly introduces several useful tools in systematically creating a paper. To summarize, the process will experience the following steps:  

Firstly, use command line to create the structure of the file. As soon as the author creates the project folder, he/she uses **git init** to start monitoring all files.  
Secondly, create empty files that are needed and use Makefile to create file dependency among all files. During the process, the author should repeatedly use **git add** and **git commit** to record all changes to the files.   
Thirdly, use pandoc to convert markdown files into html file. That is also included in Makefile.   
At last, confirm that all changes has been committed and then push the result to Github. 

To sum up, the process of creating a paper is no longer as simple as creating a single word document before. It involves more things to work together, especially we want the report to be 'smart' as it can auromarically update itself when we modify any input. There will be more things involved as the class moves on, so this is just a start.

![](../images/stat159-logo.png) 
 