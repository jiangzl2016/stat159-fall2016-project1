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

#### 3. Github
Github is a **web-based** Git repository hosted service [1]. It uses Git's distribution version control functionality, and adds its own features such as access control and collatoration. User could share their source code through this platfrom by uploading. They could also invite collaborators to work on the code together. In this assignment, I would also upload all files and reports on the Github. This is an important part for upholding scientific reproducibility. The way to use Github by using Git is following:

After having committed all changes in Git, we push the local repository as well as all commit messages to Github:

    git remote add [SSH URL]
    git push origin master 

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













 
 
