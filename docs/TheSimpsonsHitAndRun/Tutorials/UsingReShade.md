---
title: "Using ReShade"
description: "Tutorial for how to use ReShade with The Simpsons: Hit & Run."
authors: [ 2 ]
---

This is a tutorial for how to use [ReShade](https://reshade.me/#download) with The Simpsons: Hit & Run.

# Requirements
* A PC copy of The Simpsons: Hit & Run
  * You may want to make a copy of your game install, but this is up to you.
* [Project:6]
* [ReShade](https://reshade.me/#download)

# Steps
## Step 1: Run ReShade Setup
Once you've downloaded `ReShade_Setup_6.X.X.exe` from the link in the [Requirements](#requirements) section above, run it.

This should give you this dialog:
![ReShade Setup window](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step1.png)

## Step 2: Browse for The Simpsons: Hit & Run
Click the **Browse** button on the ReShade Setup window:
![A cursor hovering over the ReShade Setup window's browse button](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step2_Browse.png)

Then browse to your game install (typically located in `C:\Program Files (x86)\Vivendi Universal Games\The Simpsons Hit & Run`), choose `Simpsons.exe` and click **Open**:
![A Windows file browse dialog navigated to the game's install directory with Simpsons.exe selected](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step2_Choose.png)

And then click **Next** on the ReShade Setup window:
![A cursor hovering ovver the ReShader Setup window's Next button](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step2_Next.png)

## Step 3: Select Rendering API
The ReShade Setup will now prompt you to choose a rendering API. For this game, check **Microsoft DirectX 9** and then click **Next**:
![The ReShade Setup's rendering API selection with a cursor hovering over the Next button](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step3.png)

## Step 4: Choose Effects
The ReShade Setup will now ask you to choose effects or select a preset `.ini` file:
![The ReShade Setup's effects selection](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step4_Effects.png)

Feel free to peruse the options, or just leave the defaults. Either way, when you're ready, click **Next** to install ReShade.

Installation will probably only take a few seconds and, once it is done, just click **Finish**:
![The ReShade Setup's success dialog with a cursor hovering over the Finish button](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step4_Finish.png)

## Step 5: Mod Launcher Setup
Now that ReShade is installed, you just need to do a little bit of setup in [Project:6].

{{ tabs }}
{{ tab LML 1.27 and Newer }}
Open the Mod Launcher and then click **File** and choose **Launcher Settings...**:
![The Mod Launcher's File menu with a cursor hovering over the Launcher Settings option](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step5_OpenLauncherSettings_1.27.png)
{{ endtab }}
{{ tab LML 1.26.1 and Older }}
Open the Mod Launcher and then click **Open...** and choose **Launcher Settings...**:
![The Mod Launcher's Open button menu with a cursor hovering over the Launcher Settings option](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step5_OpenLauncherSettings_1.26.1.png)
{{ endtab }}
{{ endtabs }}

Once you're in **Launcher Settings**, go to the **Game** tab and click **Browse** next to **Executable Path**:
![The Game tab of the Mod Launcher's settings with a cursor hovering over the Browse button](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step5_Browse.png)

Now simply choose the same `Simpsons.exe` you chose in **Step 2** and click **Open**:
![A Windows file browse dialog navigated to the game's install directory with Simpsons.exe selected](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step5_Choose.png)

And finally, just click **OK** on the **Launcher Settings** window:
![The Game tab of the Mod Launcher's settings with a cursor hovering over the OK button](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step5_OK.png)

## Step 6: Enable Direct3D 9
To use your ReShade installation, you now just need to enable the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/Direct3D9.md]] hack on the **Settings** page of the mods list:
![The Settings page of the Mod Launcher's mods list with the Direct3D 9 hack enabled](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step6.png)

## Step 7: Launch the Game
Now launch the game and you should get an overlay from ReShade, indicating it's working and ready to use:
![The Settings page of the Mod Launcher's mods list with the Direct3D 9 hack enabled](/img/TheSimpsonsHitAndRun/Tutorials/UsingReShade/Step7.png)