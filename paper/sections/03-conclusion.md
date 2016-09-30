##Conclusion

The report mainly introduces several useful tools in systematically creating a paper. To summarize, the process will experience the following steps:  

Firstly, use command line to create the structure of the file. As soon as the author creates the project folder, he/she uses **git init** to start monitoring all files.  
Secondly, create empty files that are needed and use Makefile to create file dependency among all files. During the process, the author should repeatedly use **git add** and **git commit** to record all changes to the files.   
Thirdly, use pandoc to convert markdown files into html file. That is also included in Makefile.   
At last, confirm that all changes has been committed and then push the result to Github. 

To sum up, the process of creating a paper is no longer as simple as creating a single word document before. It involves more things to work together, especially we want the report to be 'smart' as it can auromarically update itself when we modify any input. There will be more things involved as the class moves on, so this is just a start.

![](../images/stat159-logo.png) 
 