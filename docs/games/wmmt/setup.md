# Wangan Midnight Maximum Tune 5DX+/6/6R/6RR
<img src="/img/wmmt/wmmt6rr.png">

!!! danger "Please make sure you downloaded your data from an appropriate source.<br>This guide is unable to troubleshoot any problems related to bad or poorly managed data."

!!! danger "If you plan to play on a remote network, chances are they will have their own steps of setting up the game. You should stop reading this guide and refer to your network for their respective setup guides.<br>This guide will only cover the basic steps on how to setup and run the game in offline mode."

!!! danger "If you're here just to setup VS Battles, head over to [VS Battle Setup](c2c.md)."

---
### Preparing Data

!!! tip ""

	WMMT is generally distributed as a single folder. For 6RR, this will be `SBWJ 05.03`. The game folder should contain an `AMCUS`, `data` and `data_jp` folder. If you're trying to setup WMMT5, the `AMCUS` folder might not be present.

<img src="/img/wmmt/1.png">

!!! info "NAMCO data is also distributed as `.VHDX` and `.VHD` files. These files are useful for archival purposes, but are not required to run the game. Always download the unpacked data for home use."

!!! danger "If your data comes with Jconfig files, you will NOT be able to use this guide as this guide is meant for TeknoParrot setup. Redownload a clean data from another source then come back here."

---
### Networks

!!! danger "Please choose one of the two solutions, not both!"

??? tip "Online Hosted Servers (Recommended)"

	There are a few online hosted servers that support various versions of WMMT, however most of them are currently invite only. Ask your friends where they play, and maybe they'll invite you!

	**Project Asakura Server (WMMT6)**

	[Project Asakura](https://discord.gg/m5mdMY5uAu) is the only public WMMT6 server that has Online Profile support, with full fledged features like Ghost Battles, Time Attack Leaderboards and OCM.<br>If you with to play on Project Asakura, you should stop reading this guide, join their [Discord](https://discord.gg/m5mdMY5uAu) and follow the #setup-guide there!

??? tip "Self Hosted Local Servers (Complex)"

	If you wish to run the game locally, but with the ability to create and save a profile, you can run a server on the same computer you are playing the game on. This server will need to be running before you launch the game, however it can be shut down when you are no longer playing.  

    Any provided setup instructions are likely to become outdated rather quickly.  

    Please refer to the included setup instructions on each projects respective web page.

	- [Bayshore](https://github.com/ProjectAsakura/Bayshore) - A network service emulator for WMMT6. Setup can be complex, and you're pretty much on your own if you plan to go this route.

---
### Setting up the Game
#### Installing TeknoParrot (TP/TPUI)

!!! tip "TeknoParrot:"

	`TeknoParrot` is a loader and hardware emulator for various arcade games. It will allow us to launch games, as well as configure inputs and for some games, configure network settings. More information can be found at the [TeknoParrot Site](https://teknoparrot.com/).

	- Download [TPBootstrapper](https://teknoparrot.com/Home/Download) from the TeknoParrot Download page. Extract the archive into a folder of its own, and run `TPBootstrapper.exe`

	- Click `Browse`, choose a directory you want to install TeknoParrot to, and click `Full Install`.

	<img src="/img/wmmt/tpdownload.png">

	- If the installation is successful, you should get a prompt saying TP has downloaded successfully. If you get any errors, try running Full Install again.

	<img src="/img/wmmt/tpsuccess.png">

#### Configuring TeknoParrot

!!! tip ""

	If this is your first time running TeknoParrot, a pop-up telling you to set emulation settings will show. Click `OK` to proceed, and Accept the GDPR.

	<img src="/img/wmmt/tpfirstrun.png">

??? warning "If you have any Riot games installed (VALORANT, League of Legends) on your PC chances are you also have Vanguard Anti-Cheat installed. A pop-up will show saying that Vanguard AC is known to cause issues with TP.<br>As far as we have tested, Vanguard does not affect WMMT so you should be fine. If you're having any issues though, try disabling Vanguard AC."

	<img src="/img/wmmt/vanguard.png">

!!! tip ""

	- If you are prompted to setup your first game, click on `No`. Then click on the top left menu button, and click `Install Updates` if available and download all the updates.

	<img src="/img/wmmt/update.png">

	- Click on the top left menu button, and click `Add Game`. Scroll down and choose the version of WMMT you're setting up. For this example, we'll be using WMMT6.

	<img src="/img/wmmt/addgame.png">

!!! tip ""

	After adding the game to your TeknoParrot library, you can now configure your `Game Settings` and `Controller Setup` accordingly.

	??? tip "Game Settings"

		- `Game Executable (wmn6r.exe)`: Point this to `wmn6r.exe` in your game folder.
		- `Second Game Executable (amauthd.exe)`: Point this to `AMAuthd.exe` in the `AMCUS` folder.

	??? tip "General Settings:"
		- `Input API`: Choose based on your controller. If you use a keyboard/DualShock/steering wheel, use DirectInput. If you use a Xbox controller, use Xinput.
		- `Terminal Mode`: Boots the game in Wangan Terminal mode, used to customize your car data. BanaPassport required to use this feature.
		- `TerminalEmulator`: Runs the game with terminal connection enabled. Required if you're playing solo or if you're hosting a VS lobby.
		- `BanaPass Connection`: Does not work as far as I'm aware. If you want to play on a network, refer to the [Networks](#networks) section.
		- `WhiteScreenFix`: If your game boots into a white screen and freezes, try enabling this. You usually need this if there are camera(s) connected to your PC.
		- `Windowed`: Run the game in Windowed Mode.
		- `Enable Outputs`: This is meant for hooks if you have cab lights or LEDs. Leave this unticked unless you know what you're doing.
		- `SkipMovies`: Not used in WMMT, leave unticked.
		- `Use Keyboard/Button For Axis`: The game will only recognize analog input for Gas, Brake and Wheel. If you use a keyboard/controller that do not have analog triggers (Nintendo Switch controllers for example), you need this enabled.
		- `Keyboard/Button Axis Wheel Sensitivity`: If you use a keyboard or button controls, this changes your turning sensitivity. This has no effect if you use analog controls.
		- `Keyboard/Button Axis Pedal Sensitivity`: If you use a keyboard or button controls, this changes your Gas/Brake sensitivity. This has no effect if you use analog controls.
		- `CustomName`: Used to change the display name when in-game. This change is client-sided, and other players will see you as GUEST when playing in VS without a BanaPassport.
	
	??? tip "Other Settings:"
		- `Network - RouterIP`: Set this to your IPv4 address. Can be obtained with `ipconfig` in CMD. Usually it should be something like `192.168.x.x`.
		- `BanaPass - AccessCode`: Carding in does not work with official TPOnline, refer to the [Networks](#networks) section for more info.
		- `BanaPass - Card ID`: Carding in does not work with official TPOnline, refer to the [Networks](#networks) section for more info.
		- `Tune - Force Full Tune`: Forces your car to be fully tuned. As far as I'm aware, this only works for WMMT5, and does nothing for 6/6R.
		- `Tune - Force Neon`: Forces Neon lights dressup on your car. As far as I'm aware, this only works for WMMT5, and does nothing for 6/6R.
		- `Tune - Select Neon`: Changes the color of the Neon.
		- `Scores - Enable Submission`: Not used in WMMT, leave unticked.
		- `Scores - Enable GUI`: Not used in WMMT, leave unticked.
		- `Scores - Enable Capture`: Not used in WMMT, leave unticked.

	When you're done setting the Game Settings, click on `Save Settings`.

	??? tip "Controller Setup"
	
		Below are the required binds. The key bindings not mentioned below are optional.
		```
		- Test
		- Service
		- Coin (not needed if you use FreePlay)
		- Wheel Axis
		- Gas
		- Brake
		- Test Menu Up
		- Test Menu Down
		- Enter Switch
		- Perspective Switch Button (the green button on an actual cab)
		- Interruption Switch Button (the red button on an actual cab)
		```
		Once you have set your keybinds, click `Save Settings`.

---
#### Running the Game

!!! tip "The screenshots are taken from an English patched game, however the menu options will be in the same position."
	
	- After setting up `Game Settings` and `Controller Setup`, you can now click on `Launch Game`.
	- When the game launches, press the `Test` button to go into the Test/Service Menu. We'll need to do some calibrations first.
	<img src="/img/wmmt/gameoptions.png">

??? tip "Game Options:"

	- Go to `Game Options`.
	- Make sure all 3 options are `OFF`.
	<img src="/img/wmmt/gameoptions2.png"> 
	- After setting `Game Options`, click `Back`.

??? tip "I/O Test"

	- Navigate to `I/O Test` > `Go to I/O Interface Initialize`.
	- Make sure your controller/wheel's triggers/pedals/analog sticks are NOT pressed down. And press your `Enter Switch`.
	- If done correctly, all 3 values should show `000` when you're not pressing anything.
	- **The Gas/Brake values should be positive when pressed. If you get negative values when pressing them down, try enabling `Reverse Gas/Brake Axis` in TeknoParrot's top left menu settings.**
	- Choose `Continue Switch Test` when done.
	<img src="/img/wmmt/ioinitialize.png"> 

	- Test your input by turning max left/right, and pressing Gas/Brake to max. Make sure everything shows `OK`, then press `Up Switch` and `Enter Switch` at the same time to exit `I/O Test` mode.
	
	<img src="/img/wmmt/iotest.png"> 

	!!! info "The max left input value will be `+512`, and max right will be `+508`. This is normal."

	Press your `Test` key again to exit the Service menu. If the game loads into Attract Mode, you're good to go! 

---
### Troubleshooting

!!! warning "Have any other issues? Game wont run?"

	Check out the [Troubleshooting](troubleshooting.md) page.