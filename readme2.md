# 1. Create branch


Open local folder **campusciff** with GitBash:



    git branch v0.2


Switch to new branch:


    git checkout v0.2
    Switched to branch 'v0.2'


Now I am located in branch v0.2

    Mark@DESKTOP-05COGMK MINGW64 ~/Desktop/Master/Data Science             Toolkit/Practicas/campusciff (v0.2)$
    
    
# 2. Create file in branch v0.2

    cat > fichero2.txt
    CTRL + D


# 3. Upload to remote branch


Stagged and commited: 

    git add -A
    git commit -m "initial commit"
    
Upload to new remote branch:
     
     
     git push origin v0.2
     
New branch in repository created:


    To git@github.com:Mark-Wellings/campusciff.git
    * [new branch]      v0.2 -> v0.2



![ignored](https://github.com/Mark-Wellings/campusciff/blob/master/newbranch.jpg)


I noticed a mistake here should have been: 

    
    git push --set-upstream origin v0.2 



After solving the merge conflicts with various 'git add' and 'git commit' I could finaly merge:



    git checkout master
    git merge v0.2

If I am located in branch v0.2 and change fichero2.txt I have to add, commit and push. Then my branch v0.2 is different to master. 

If I then use: 


    git checkout master
    git merge v0.2
    git push origin master


They are identical again. 




 