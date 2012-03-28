# Assignments for Aalto Web Apps course
This repository contains all the assignments repositories as submodules.

##Cloning
To clone locally, you must clone the main repository and update the submodules:

    git clone git@github.com:aaltowebapps/assignments.git
    cd assignments
    git submodule init
    git submodule update
  
##Updating one submodule for the main repository
The submodules are not automatically update but must be updated manually. First we must go to the submodule 
to update, pull the new version and commit the main repository: 

    cd <path to submodule>
    git pull origin master
    cd ..
    git commit -am "Upgrading the submodule xxx"
    git push origin 

## Updating all the submodules for the main repository
Before updating all the submodules it's better to pull the latest version of the main repository. After that 
you can update all the submodules and push the changes to the main repository. Here is the sequence of commands:

    git pull origin master
    git submodule update
    git submodule foreach git pull origin master
    git commit -am "Update all the submodules"
    git push origin master

##Adding a submodule
You can add a new submodule to the main repo in the following way:

    git submodule add <url to git repor>
    git add .
    git commit -m "Added a new submodule"

##Pulling the submodules updates from the main repository
If you have already cloned the main repository, you can update the submodules to the latest version that is 
stored in the main repository in the following way (this will not update to the latest versions of the submodules):

    git pull origin
    git submodule update
