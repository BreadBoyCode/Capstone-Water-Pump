Start of the main Simulink file. So far, there is a pv cell block to model the solar panel, V and I sensors, which track pv and input to a matlab function block, which will contain the MPPT code. This code will be adapted to whichever microcontroller we use in the physical circuit. The output will be a PWM signal, which controls a buck converter between the solar panel and battery.  
Commit 2: Added a bunch of stuff. I think the general high-level layout of the charging circuit is there but not certain. See the annotations within Simulink file. If you make changes to this file, please either make them on a separate copy and push that copy when done (ideal, I think) or make a new branch to push to.
Commit 3: Added .gitattributes file to repo. Pull from this branch, then open matlab, and in Command Window, enter
comparisons.ExternalSCMLink.setupGitConfig()
After doing this, all subsequent merges will actually work with matlab/simulink files.
