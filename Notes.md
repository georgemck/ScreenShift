

https://www.reddit.com/r/pokemongodev/comments/6554k1/tutorial_set_your_android_phone_to_a_lower/

Tutorial

Enable USB debugging developer options on your phone. Settings > About Phone > Tap (Build version or build number) until you get a prompt that developer options are available.

Enable USB debugging find and enable USB debugging on your phone. Settings > Developer options > Enable USB debugging

Install adb on your PC!or Mac!

Once installed run cmd on pc (Windows key + R, Type CMD and hit enter) or Terminal on mac

Once in CMD or Terminal enter: adb shell dumpsys display

5.5. If you get an error Check your phone and authorize the PC

If the code is accepted find the following data and write it down, this will allow you to revert back if you do not like the lower resolution, do not skip this step.:
(this is mine Sony Xperia Z3) width: 1080 height: 1920 density: 480

Once you have the original values written down you can enter the following:
1080

adb shell wm size 1080x1920

adb shell wm density 480 <-- This value can vary per phone, you'll know it's right when you can read text and apps don't render too small value is from 120 up to 640

720

adb shell wm size 720x1280

adb shell wm density 350

1440.bat (original settings)

adb shell wm size 1440x2560
adb shell wm density 560
adb shell input keyevent KEYCODE_POWER
adb shell input keyevent KEYCODE_WAKEUP
adb shell input keyevent KEYCODE_MENU
1080.bat

adb shell wm size 1080x1920
adb shell wm density 420
adb shell input keyevent KEYCODE_POWER
adb shell input keyevent KEYCODE_WAKEUP
adb shell input keyevent KEYCODE_MENU
720.bat

adb shell wm size 720x1280
adb shell wm density 280
adb shell input keyevent KEYCODE_POWER
adb shell input keyevent KEYCODE_WAKEUP
adb shell input keyevent KEYCODE_MENU
print.bat (prints your current settings)

adb shell wm size
adb shell wm density
pause
