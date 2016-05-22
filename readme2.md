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