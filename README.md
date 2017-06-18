This repository contains some [Alfred] workflows for productivity. At the moment the following workflows are included:

* [Focus Mode](#focusmode)
* [Screencap](#screencap)

See below for a detailed description of each.

---

## <a name="focusmode"></a> Focus Mode

_Focus Mode_ is designed to help getting into the zone, i.e. not being distracked from the work you want to get done. The keyword ist just `focus` - in order to start use `focus <min>` where `<min>` is the number of minutes you want to focus:

![Starting Focus Mode][focus_start]

The command will do the following:

1. Disable System Notifications
2. Check if [Slack] is running - if so it will set your status to _Focusing..._ as well as enable `/dnd` mode (using simulated keystrokes)
3. Start a delay in the background to automatically revert 1. and 2. again

After _Focus Mode_ has been enabled you can use `focus` again to show the remaining time and to easily cancel your focus mode prematurely.

![Stopping Focus Mode][focus_stop]

When disabling the workflow will wait 5 seconds before resetting [Slack] since this requires simulating keystrokes and you should just sit back and relax.

_Workflow Icon by Freepik from [www.flaticon.com](www.flaticon.com)._

---

## <a name="screencap"></a> Screencap

_Screencap_ allows to easily start and stop screen captures using _QuickTime Player_. Furthermore, instead of saving directly as a `.mov` file, it provides the ability to directly transform the screen capture and store it as `.gif`.

**Important**: When stopping _Screencap_ automatically cuts off a few seconds at the end - see the configuration variable `cutoffend`. For this as well as GIF transformation to work you need to have `ffmpeg` installed:

```bash
$ brew install ffmpeg
```

The usage is as follows:

1. Start the screen capture recording with `scr`:
  ![Start Screen Capture][screencap_start]
  It will allow you to select the captured area and start the recording by pressing _QuickTime's_ record button.
2. To stop the screen recording use one of the following:
    * `scs <filename>` to stop the recording and save the file as `<filename>.mov` inside your home folder
      ![Stop Screen Capture and save][screencap_stop]
    * `scg <filename>` to stop the recording and save the file as a GIF named `<filename>.gif` inside your home folder
      ![Stop Screen Capture and save as GIF][screencap_gif]

_Hint_: As you can probably guess - all GIFs embedded here were created using _Screencap_.

_Workflow Icon by Freepik from [www.flaticon.com](www.flaticon.com)._


[Alfred]: https://www.alfredapp.com
[Slack]: https://www.slack.com

[focus_start]: ./doc/focus_start.gif
[focus_stop]: ./doc/focus_stop.gif
[screencap_start]: ./doc/screencap_start.gif
[screencap_stop]: ./doc/screencap_stop.gif
[screencap_gif]: ./doc/screencap_gif.gif