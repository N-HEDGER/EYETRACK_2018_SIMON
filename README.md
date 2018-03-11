# EYETRACK_2018_SIMON

## Instructions.

1. First run the 9 point calibration, contained within Main/ Calibration. It will throw a warning if no eyetracker is detected.
The filename should ony contain numbers. Get the observer to sit at a good distance (65 cm) with their eyes as close as possible to the horizontal line.
The eyes will appear in green if they are being sampled reliably. If you keep losing them, then re-position or change the lighting. You can re-do the calibration by pressing
the 'r' key, or accept it by pressing the spacebar. The calibration data will be saved in Data/ Calibration. You should perform the calibration again
if the subject takes a break, or if the eyetracker disconnects.

2. Next run the freeview task itself. The main file that drives the experiment is Main/expLauncher.m. Again, a warning will appear if no eyetracker
is detected.

3. A GUI will appear and ask you to put in some details for the experiment. The only mandatory one is the filename, I believe.

4. There will then be 30, 5 second trials. The trial details will be printed in the command window. The data is plotted after each trial.

5. At the end of each trial, it will wait for keyboard input. Press space for the new trial, or press escape to quit. If you quit and re-start
the experiment, it will re-start from where you left off (after putting the same filename into the GUI).

6. 3 data files will be saved for each participant in the /Data folder. *Log* contains details of each trial and when each trial was completed
*const* contains all the experiment config and *gaze* contains the gaze data (one mat file per trial).


## Things you need to change, depending on the setup.

1. In Config/ scrConfig: *scr.disp_sizeX*, *scr.disp_sizeY*. These will need to be changed to the physical size of your display (in mm).\
2. In Config/ scrConfig: *scr.dist* . This will need to be changed to the viewing distance in cm (although it shouldnt be too far from 65cm)
3. In Main/ expLauncher: *const.desiredFD* - the desired refresh rate (hz).
4. In Main/ expLauncher: *const.desiredRes* - the desired resolution (pixels).
5. In Main/Calibrate:  *const.desiredFD* and *const.desiredRes* will also need to be changed.
6. In Trials/ runTrials: The path to the stimuli will need to be changed (after they are put on your computer).
7. In Main/Calibrate: The path to the eyetracking SDK will need to be changed (after it is put on your computer).
8. In Main/expLauncher: The path to the eyetracking SDK will need to be changed (after it is put on your computer).
9. In Config/eyeConfig: The path to the eyetracking SDK will need to be changed (after it is put on your computer).


