by using only git init
we get master branch we dont need that
for that we use
       git init  -b main
                               U=Untracked by git
to see status of repo we use
          git status

after looking status it gives like below

On branch main

No commits yet


for adding a file: git add first.txt<filename>
for looking status :  git status

for commiting file we shouldn't use just
          git commit

we also should give msg also like
         git commit -m "firstcommit" 

after that it gives like
      [main (root-commit) 1b2886b] firstcommit
       1 file changed, 1 insertion(+)
       create mode 100644 first.txt    
           
       1b2886b it is unique num of every commit    
       git creates a checksum for each commit if any 
       change happened in code it will changed 
       actually it is 20 digits but we take 7digits hexadecimal

we can see oomits in repo by using 
           >git log

commit 1b2886bedb235e844076cfd640277392e77a98c3 (HEAD -> main)
Author: venukumar <venumadhav8675@gmail.com>
Date:   Fri Dec 12 15:53:41 2025 +0530

    firstcommit       

if any chnage done in file 
it again add by sing git add command
and commit by using git commit -m "msg" 

to skip this staging area we use command like
     
     git commit -a -m "msg"   (m=msg,a=all(only tracked files ,files that are added before))
directly committed instead of add and commit     
It skips the staging area for tracked files and directly commits them

  git diff:

to track changes occured in file we use  
     git diff command(if file is not added)

if file is added we use    
      git diff --staged  
        
        reult output:
       diff --git a/first.txt b/first.txt
       index d08c101..cf3e1de 100644
       --- a/first.txt
       +++ b/first.txt
       @@ -1,3 +1,7 @@
        HELLOWORLD 1st commit
        HELLOWORLD\\\ 2nd commit
        HELLOWORLD\\\?  3rd commit
       +
       +take input from user
       +apply add operation 
       +show result   


removing a file from git:
instead of deleting file in directory directly 
we should delete file from git first by using
      git rm --cached filename       

if you created more files to add
instead of using separate add's we use
    git add .  command


after init,add,commit
next step: we should provide link of repo by following command
       >git remote add origin (https://github.com/[repo link]dvenukumar55/git-tutorial-demo).git

we need to push file to that repo:
       >git push origin main    


TAGGING
 two types:
    annotated tagging   we use this
    lightweight tagging
