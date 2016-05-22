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



If I am located in branch v0.2 and change fichero2.txt I have to add, commit and push. Then my branch v0.2 is different to master (on local and remote). 

If I then use: 


    git checkout master
    git merge v0.2
    git push origin master


They are identical again both on local and remote. 


# 4. Merge conflict

    git checkout master
    echo "hola" >> fichero1.txt
    git add -A
    git commit -m "changed"


Now master has a file which doesnt exist in v0.2


    git checkout v0.2
    echo "adios" >> fichero1.txt
    git add -A
    git commit -m "changed"

Now both branches have a file named fichero1.txt but different content. 

When merging I get an error, because line 1 has got different entries: 

    git checkout master
    git merge v0.2
    Auto-merging fichero1.txt
    CONFLICT (add/add): Merge conflict in fichero1.txt
    Automatic merge failed; fix conflicts and then commit the result.

# 5. List branches


with merge: 


    git branch --merged


without merge



    git branch --no-merged



# 6. Fix conflict


Wrongly merged file: 

    <<<<<<< HEAD
    hola
    =======
    adios
    >>>>>>> v0.2


Deleting manually lines 1,3 and 5. New file: 


    hola
    adios

Add and commit after changes: 


    git add -A
    git commit -m "noconflict"


# 7. Create tag and delete branch



    git tag v0.2
    git branch -d v0.2

# 8. List commits tags branches: 

Predefined in class: 

    git list



![list1](https://github.com/Mark-Wellings/campusciff/blob/master/list1.jpg)




![list2](https://github.com/Mark-Wellings/campusciff/blob/master/list2.jpg)



# 9. Create organization:




![orga](https://github.com/Mark-Wellings/campusciff/blob/master/orga.jpg)


# 10. Create team:



Invitations not yet accepted: 




![team](https://github.com/Mark-Wellings/campusciff/blob/master/team.jpg)




Different auth rights: 




![auth](https://github.com/Mark-Wellings/campusciff/blob/master/auth.jpg)









 