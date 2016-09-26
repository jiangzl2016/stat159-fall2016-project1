##Discussion

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













 
 
