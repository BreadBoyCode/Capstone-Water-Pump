Added a bunch of simulation stuff and made a yet-untuned charge controller that is partially incomplete (need a way to track 85%-100% full battery). Simulation currently seems to be giving complete nonsense as current out of the solar panel is always at its max regardless of duty cycle. I think this is due to simscape's built-in buck converter being poopoo for our purposes. We should try making a custom one and seeing if that fixes the problem.
OTHER IMPORTANT THINGS OF NOTE:

* .gitignore file tells git and MATLAB source control not to track certain files and file types. When running Simulink, some local files that are machine-specific will be created (such as .slxc files), which should not be pushed to the repo. gitignore should prevent them from accidentally being committed.
* vars.sldd: A data dictionary containing global variables that will apply to the main circuit and all subsystems or referenced models. Right now it only has the time step (Ts), but others could be added. This way, we can easily change the resolution of the simulation by having all blocks reference the same variable. To open and make changes, can open directly from the MATLAB file hierarchy or, within Simulink model, go MODELING-->DESIGN drop down-->Data Dictionary. Right click vars and click "Save Changes" after modifying. If Simulink isn't recognizing variables for some reason, click "Link to Data Dictionary" in the same drop down and browse for vars.sldd

&#x20;



