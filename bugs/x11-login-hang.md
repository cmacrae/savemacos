Notes for the X11.app login hang bug
====================================

Notes dipicting my investigation into a rather annoying bug that Beastie and I have come across with starting XQuartz from login with our modified services (lots disabled). Upon logging in, the system will hang for approximately 20-30 seconds before launching XQuartz.

I have found a rather awkward workaround for the timebeing; once the system logs in, press the power button to summon the power prompt, press 'esc' to close it, then proceed to press 'Command+Shift+Q' this will invoke the logout dialogue, once this is left on the screen for approximately 1 second, X should start.

(Perhaps this workaround works purely because there's some intervention from the user, interacting with the system, focusing on "something".)

The following notes have been compiled whilst examining a fresh /var/log/system.log


Potential causes
----------------

* Screenshare notification *
-- Possibly due to deactivation of the Notification Centre --// After further investigation, I've found this same message in a "clean" systems log

Jun  4 23:46:16 faber.local loginwindow[1434]: ERROR | ScreensharingLoginNotification | Failed sending message to screen sharing GetScreensharingPort, err: 1102

* Login Window trying to initiate disabled services *
-- It looks like the login window app is still looking for various disabled services --// After further investiagetion, I have come to recognise this as the most likely cause, these messages do not appear in a "clean" systems log.


Jun  4 23:46:16 faber com.apple.launchd.peruser.501[112] (com.apple.Dock.agent[1456]): Exited with code: 2
Jun  4 23:46:16 faber com.apple.launchd.peruser.501[112] (com.apple.SystemUIServer.agent[1457]): Exited with code: 2
Jun  4 23:46:16 faber com.apple.launchd.peruser.501[112] (com.apple.Finder[1458]): Exited with code: 2
Jun  4 23:46:16 faber.local BezelServices 236.3[1434]: Failed to lookup server port for com.apple.BezelUI due to error: Bootstrap Unknown Service.

* Apple ID auth check *
-- Although disabled, applid service looks like it's trying to authenticate, as it can clearly be observed below, this process creates a timeout around 20 seconds. I believe this is the most likely candidate at the point of writing. --// This is no longer considered the cause, this message is echo'd in a "clean" systems log.

Jun  4 23:46:36 faber com.apple.launchd[1] (com.apple.coreservices.appleid.authentication[1443]): Exit timeout elapsed (20 seconds). Killing
