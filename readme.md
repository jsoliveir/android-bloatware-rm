# Removing Pre-Installed Apps

> Root access is not needed

## TCL 10 PRO

Get into a shell session using adb 

```bash
adb shell
```

1) Remove all unwanted apps:

```bash
for i in $(pm list packages netflix); do pm uninstall -k --user 0 ${i#*:}; done

for i in $(pm list packages facebook); do pm uninstall -k --user 0 ${i#*:}; done

for i in $(pm list packages com.tct.smart.); do pm uninstall -k --user 0 ${i#*:}; done

pm uninstall -k --user 0 com.tcl.tct.filemanager
pm uninstall -k --user 0 com.tclhz.gallery
pm uninstall -k --user 0 com.tcl.android.video
pm uninstall -k --user 0 com.tct.smart.notes
pm uninstall -k --user 0 com.tct.smart.tlink
pm uninstall -k --user 0 com.tct.music
pm uninstall -k --user 0 com.tct.iris
pm uninstall -k --user 0 com.tct.simplelauncher
pm uninstall -k --user 0 com.tct.tctsmartapprecommend
pm uninstall -k --user 0 com.tcl.usercare
pm uninstall -k --user 0 com.tct.simplelauncher.a_overlay
pm uninstall -k --user 0 com.tcl.android.launcher.a_overlay
pm uninstall -k --user 0 com.tct.sidebar
pm uninstall -k --user 0 com.tclhz.gallery.a_overlay

pm uninstall -k --user 0 com.google.android.apps.youtube.music
pm uninstall -k --user 0 com.google.android.apps.wellbeing
pm uninstall -k --user 0 com.google.android.apps.tachyon
pm uninstall -k --user 0 com.google.android.apps.podcasts
pm uninstall -k --user 0 com.google.android.apps.subscriptions.red
pm uninstall -k --user 0 com.google.android.videos
pm uninstall -k --user 0 com.google.android.apps.docs
pm uninstall -k --user 0 com.google.android.apps.maps
pm uninstall -k --user 0 com.google.android.apps.photos
pm uninstall -k --user 0 com.google.android.apps.docs.editors.sheets
pm uninstall -k --user 0 com.google.android.calendar
pm uninstall -k --user 0 com.google.android.gm
pm uninstall -k --user 0 com.google.android.googlequicksearchbox
pm uninstall -k --user 0 com.google.android.keep
pm uninstall -k --user 0 com.google.android.youtube
pm uninstall -k --user 0 com.google.android.apps.nbu.files
pm uninstall -k --user 0 com.tct.tctsmartapprecommend
pm uninstall -k --user 0 com.tct.onetouchbooster
pm uninstall -k --user 0 com.tct.applock
```

2) Required apps:

```bash
pm install-existing com.tctui
pm install-existing com.tcl.token
pm install-existing com.tcl.fota.system
pm install-existing com.tcl.tct.weather
pm install-existing com.tcl.camera
pm install-existing com.tcl.android.launcher
pm install-existing com.tcl.screenshotex
pm install-existing com.tct.smartcover
pm install-existing com.tct.dialer.a_overlay
pm install-existing com.tct.phone
```
