# maxring
`Method A` Locks the ringer volume to max state, gets triggered only when VOL- key is pressed or when volume is decreased through the OS. Trigger-based, so expect minimal battery drain

`Method B` Time-based, checks ringer volume level at fixed intervals, and maxes it out if it's not maxed out already. Might cause more battery drain than method A depending on interval set

| Table of Contents|
| ------------- |
| <a href="#method-a-recommended">Method A (recommended)</a>|
| <a href="#method-b-if-a-fails">Method B</a>|

## Method A (`recommended`)
This video covers steps 3-14, you may need to pause it frequently to see what was done. **<a href="#instructions">Full instructions are below.</a>**

<a href="http://www.youtube.com/watch?feature=player_embedded&v=5YNqA8xSYPM
" target="_blank"><img src="http://img.youtube.com/vi/5YNqA8xSYPM/0.jpg" 
alt="Method A" width="240" height="180" border="1" /></a>
### Instructions

1. Download the files at: https://goo.gl/CQPzE4
2. Place the files at an appropriate directory on the device
3. Install **Tasker-5.0b2.apk**, followed by **volume-profile.apk**
4. Launch **Tasker**, hit the check mark for the first two agreements/prompts that appear on first launch
5. Tap the the three dots (`⋮`) on the top-left corner🡲`Preferences`🡲`Monitor` tab
6. Make sure that `Run In Foreground` is checked. *(OPTIONAL)You can also check `Show Notification Icon` for your own convenience (to check whether Tasker is running in the background/foreground without actually opening the app in the future). It'll have an icon in the status bar to let you know that*
7. Go back, tap the three dots again (`⋮`) and hit `Exit`. Tap `save first` and you should see a Tasker icon now (if checked) and status bar notification that'll always be visible
8. Open up the **Volume profile** app and switch to the the `VOLUMES` tab
9. Set `Ringer Mode` to `Normal`, `Ring/Notification` to 7/7 (or whatever the max is) and `Voice Call` to 5/5 (or the max)
10. Tap the save icon on the top right (floppy disk icon; 💾) and name it whatever you want
11. Switch over to the `PROFILES` tab and tap on the newly created profile, a blue dot should appear to the right which means it is now active
12. Hold down the newly created profile for a few seconds to bring up the menu, and select `edit`. Check the `Lock` boxes next to `Ring/Notification` and `Voice Call` and save again (💾)
13. Hit the padlock icon on the top right of the app which will now show a padlock in the locked position (🔓🡲🔒)
14. You can test this profile, by exiting both apps, and trying to lower the volume (which should now be not possible)
15. Restart the device and test the profile once again to make sure it's restart-proof
16. All done

## Method B (if A fails/doesn't work) [WIP]
This video covers steps 5-xx, you may need to pause it frequently to see what was done. **<a href="#instructions-1">Full instructions are below.</a>**
<a href="http://www.youtube.com/watch?feature=player_embedded&v=yfJek7yY-sw
" target="_blank"><img src="http://img.youtube.com/vi/yfJek7yY-sw/0.jpg" 
alt="Method B" width="240" height="180" border="1" /></a>
### Instructions

1. Download the files at: https://goo.gl/CQPzE4
2. Place the files at an appropriate directory on the device
3. Install **Tasker-5.0b2.apk**
4. Launch **Tasker**, hit the check mark for the first two agreements/prompts that appear on first launch
5. Tap the the three dots (`⋮`) on the top-left corner🡲`Preferences`🡲`Monitor` tab
6. Make sure that `Run In Foreground` is checked. *(OPTIONAL)You can also check `Show Notification Icon` for your own convenience (to check whether Tasker is running in the background/foreground without actually opening the app in the future). It'll have an icon in the status bar to let you know that*
7. Switch to `Profile` tab and hit the `+` button, select `Time`
8. Tap on `FROM` and `TO` to deactivate them. Tap `EVERY` to activate (ORANGE underline= Active, GRAY underline= Inactive)
9. Set `EVERY` to 30 Minutes and go back
10. Tap `New Task` and give it a name, under Task Edit screen, hit the `+` button ad select `Audio`🡲`Ringer Volume`
11. Set `Level` to 7 (or max) and expand the If section via the `+` button to its right
12. Tap the button to left of the cup and select `Volume-Ringer`
13. Tap the tilde button (`~`) and select `Doesn't Equal` under the Condition Operator screen
14. Under `Value` field enter the max volume for the device set at step #9 and hit back (twice) to get back to the initial Tasker page
15. Hit the three dots (`⋮`) and select `Exit` and select `save first`
16. 

<img src="/images/tasker.png" align=right height="200" width="200">
