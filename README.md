# New version and the keyboard shortcut issues:

With the new version of the IME plugin, the feature itself seems to have been restored with its original functionality.

However, in Windower v4, the keyboard shortcuts to switch languages doesn't seem to want to switch to Japanese, and the keyboard shortcut to switch input modes doesn't work.
For example, having the keyboard layout for German, English and Japanese installed, the typical Alt+Shift - or whatever you configure it to - will only switch between German and English.
If I assign specific shortcuts, say Ctrl+Shift+1 for German, Ctrl+Shift+2 for English and Ctrl+Shift+3 for Japanese, only the first two will work.

So our first hurdle is that, when using the IME plugin ingame, to switch the language manually via the windows language bar.
The second issue, not being able to switch input modes, we will address below.

In addition, I recommend not switching between languages at all, as the input mode can get stuck and you won't be able to type in any keyboard layout other than Japanese.
Since one of the two input modes for japanese, Romaji-Input, is similar to the English layout, I recommend sticking with the Japanese layout and just keeping it in Romaji mode most of the time. You'll get used to it, and if you didn't want to use Japanese input anyways, why do you have the IME plugin loaded?
It doesn't have to be on auto-load.

## Setup

Since the original guide still remains below, I will not re-introduce the entire setup procedure.
I set my language for non-Unicode programs to Japanese, but as the guide says, using an AppLocale setter might also work for you.

The basic requirements are therefore:

* Install the Japanese IME Keyboard. This is different for each operating system.
In Windows 7 the steps were as shown here:
![Step 1](https://raw.githubusercontent.com/Elvaron/fwime/master/screen1.png)
In Windows 10 you'll want to find your Region & language options:
![Step 1 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/1.png)
Click on _Add a language_ and search for Japanese
![Step 2 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/2.png)
Confirm the installation

![Step 3 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/3.png)
* Either set your input language for non-unicode programs to Japanese, or experiment with an AppLocale tool.
* Have the current IME plugin.

## Input Mode Selection

To address the issue of not being able to switch input modes, we navigate to the keyboard options.
Once again, the screenshots show Windows 7 and Windows 10, but it should be similar for other Windows operating systems.

Opening the properties of the Japanese IME Keyboard, you'll likely be presented with the following screen:
![Step 2](https://raw.githubusercontent.com/Elvaron/fwime/master/screen2.png)


If you're like me, this view is a bit intimidating.
Let's change it to English, shall we? In order to do so, open the dropdown menu highlighted in the above screenshot.
You'll get the following options:
* 自動設定 (jidou settei) - Autoset
* 日本語 (nihong) - Japanese
* 英語 (eigo) - English

Select the third option, hit okay, then re-open the Properties window to get the following view:
![Step 3](https://raw.githubusercontent.com/Elvaron/fwime/master/screen3.png)

Now that we know what we're dealing with, you can make changes to all these properties as you see fit. Feel free to experiment.
You can reset your changes on the tab General if you make things worse.

To get to the same screen in Windows 10, select the Japanese keyboard and click on options:
![Step 4 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/4.png)
Then for the actual Microsoft IME click again on options:

![Step 5 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/5.png)
Scroll all the way down and click on _Open advanced settings_:
![Step 6 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/6.png)

In order to set up our workaround to the keyboard shortcut limitations in Windower v4, navigate to the Editing tab and click on Advanced next to the Key template dropdown.
The table shows the current key assignments. Yes, it looks confusing.
![Step 4](https://raw.githubusercontent.com/Elvaron/fwime/master/screen4.png)
For Windows 10, it's under the General tab. Click on _Advanced_ next under the group _Editing operation and behavior_:
![Step 7 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/7.png)

It also doesn't work like you'd expect.
Instead of double-clicking on a keyboard combination you want to set, and then assigning a function to it, you look for the function you want to assign, double click it's entry in the table - whatever it's current keyboard shortcut may be - and assign a new keyboard shortcut from a dropdown.

The function we're looking for, IME ON/OFF, is most likely assigned to a key that only physically exists on japanese keyboards:
![Step 8 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/8.png)

Let's assign it to something more useful, like Ctrl+F2:
![Step 9 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/9.png)
Once this assignment is in place, you can confirm the screen:
![Step 5](https://raw.githubusercontent.com/Elvaron/fwime/master/screen5.png)
![Step 10 Win 10](https://raw.githubusercontent.com/Elvaron/fwime/master/10.png)

Now close all these open windows by clicking OK.
Start windower-enabled FFXI, log into your character.
Bring up the console, load the IME plugin.
Switch your current keyboard to Japanese.
Open your chat prompt and try out your new keyboard shortcut.
If all works, congratulations!

You can read up on the general usage of the IME below.
If you use a newer operating system and find that additional steps were necessary to get it working, feel free to let us know so this guide can be improved.
