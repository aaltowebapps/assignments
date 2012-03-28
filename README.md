# Assignments for Aalto Web Apps course
This repository contains all the assignments repositories as submodules.

##Cloning
To clone locally, you must clone the main repository and update the submodules:

    git clone git@github.com:aaltowebapps/assignments.git
    cd assignments
    git submodule init
    git submodule update
  
##Pulling the submodules updates from the main repository
If you have already cloned the main repository, you can update the submodules in the following way:
  
    git pull origin
    git submodule update

##Updating the submodules for the main repository
The submodules are not automatically update but must be updated manually. First we must go to the submodule 
to update, pull the new version and commit the main repository: 

    cd <path to submodule>
    git pull origin master
    cd ..
    git commit -am "Upgrading the submodule xxx"
    git push origin 

##Adding a submodule
You can add a new submodule to the main repo in the following way:

    git submodule add <url to git repor>
    git add .
    git commit -m "Added a new submodule"
