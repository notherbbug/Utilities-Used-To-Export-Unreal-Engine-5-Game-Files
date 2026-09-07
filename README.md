# Utilities-Used-To-Access-Purchased-Unreal-Engine-5-Game-Files-
A resource detailing the utilities &amp; steps to access purchased Unreal Engine 5 game content

# Before We Start
- This is a personal guide detailing steps to access legally obtained content & simply explains which community tools were used & the steps implemented to access said content.
- I am NOT responsible for how you use the information catalogued within this guide.

# Software Requirements
- [Steamless](https://github.com/atom0s/Steamless/releases/tag/v3.1.0.0) - For Removing the SteamStub/Steam DRM Restrictions on the *Shipping.exe* .
- [FModel](https://fmodel.app) - You can use this too mod and view Assets your Games. You can find the *.pak* *.ucas* & *.utoc* files in the game folder usually within the *Content Folder*
- [AESDumpster](https://github.com/GHFear/AESDumpster) - For Finding AES Keys in the DRM-less *Shipping.exe* . (Just use the online tool for simplicity)
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) - For dumping *.usmap* from the game to rectify *"Package has unversioned properties but mapping file is missing, can't serialize"* in FModel. (Note: some games will need to be configured specifically to run this tool and obtain a usable *.usmap* dump. For example *The Blood of The Dawnwalker* won't generate the dump unless you use this specific version of [UE4SS](https://www.nexusmods.com/thebloodofdawnwalker/mods/55)

# Note:
- I heavily referenced this extremely well assembled [AES Key Extracting Guide](https://github.com/Cracko298/UE4-AES-Key-Extracting-Guide) to acquire the AES Key, created by [Cracko298](https://github.com/Cracko298) 
  
# Guide:
# Step 1 (Getting rid of the DRM restriction):
- Firstly open/run [Steamless](https://github.com/atom0s/Steamless/releases/tag/v3.1.0.0) to get rid of the DRM restrictions on your *Shipping.exe* file.
- To access your *Shipping.exe* file(s) go into "[Steam](https://store.steampowered.com) > Library > *Your Game*". Right click on *Your Game's Name* and go into "Manage > Browse Locale Files"
- The file explorer should have opened *probably in the background*. Go into "*Your Game Name Folder* > Binaries > Win64/32".
- Paste the directory link into [Steamless](https://github.com/atom0s/Steamless/releases/tag/v3.1.0.0), or find the *Shipping.exe* directory in the "browse" button.
- Hit the extract button in [Steamless](https://github.com/atom0s/Steamless/releases/tag/v3.1.0.0) it'll take a few second(s)/minute(s).
- The newly created *Your Game's Name.exe.unpacked.exe* file is the DRM-LESS game.

# Step 2 (Finding the AES Key)
- Either use [AESDumpster](https://github.com/GHFear/AESDumpster) or simply open the [AES Dumpster – Unreal Engine AES Key Scanner Online Tool](https://illusory.dev/aesdumpster/)
- Drag the *DRM-LESS* game *.exe* you created in __Step 1__ into the online tool.
- Copy the revealed __AES KEY__ as you will need to access the content in [FModel](https://fmodel.app)

# Step 3 (Dumping the .usmap from the game with UE4SS)
- Follow the installation instruction to install [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) to your game folder.

  __Note:__ For specific games ex. *The Blood of the Dawnwalker* follow the [relevant install instructions](https://www.nexusmods.com/thebloodofdawnwalker/mods/55) provided with specific configuration
- Navigate to the *game folder* where [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) is installed (same as *your game.exe*) and be sure to configure the keybind to dump the *.usmap* file once in the game main menu. You can set the keybind in the *UE4SS-settings.ini* file instructions are included within.

- Launch your game and when you get to the Main Menu activate the keybind you set to dump the *.usmap* file directly to the *game folder* .

# Step 4 (Exporting files with FModel)
- Open [FModel](https://fmodel.app) and Set the AES Key you copied in __Step 1__ under the Directory dropdown.

  <img width="172" height="132" alt="image" src="https://github.com/user-attachments/assets/9e4a996a-e085-4882-a70f-b587bd197964" />

- Set the directory containing *.pak* *.ucas* & *.utoc* files in the game folder usually within the *Content Folder*

  <img width="175" height="138" alt="image" src="https://github.com/user-attachments/assets/7e6e9d4c-8ba2-465d-af29-c58acc46871a" />

- Set the *.usmap* file in [FModel](https://fmodel.app) under *Settings* .

  __Note:__ If you are exporting audio files you may also want to check the Convert Audio During Export (.wav) to *Enabled*

  <img width="491" height="286" alt="image" src="https://github.com/user-attachments/assets/71078992-8590-4fc7-ab12-75a5010cb98e" />

- At this point you'd have to locate the specific files/content you wish to export > right click > export.
  The exported files will be in the same directory [FModel](https://fmodel.app) is installed in.
