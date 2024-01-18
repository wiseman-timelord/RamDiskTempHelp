# RamDiskTempHelp-Ba

### STATUS: WORKING
The scripts work, if I get any more, tips or script, they will be here.

## DESCRIPTION
Some scripts to assist with running Temp/Tmp directories from RamDisk on Windows, and some tips in the NOTATION below. 
1. `CcAutoWash.Bat` - RamDisks will always be cut fine, as they need not eat system ram, obviously this is intended for people whom put their, TEMP and TMP, on a RamDisk loaded from image, and are intending to have their computer on for longer periods. To clean a ramdisk, this requires a certain delay after the user logon, in order to process the cleaning, yes I'm sure task manager can delay it, but, its good to have it a little longer and I want it running from the start menu, the start menu is the last location it checks, and the user is required to logon.
2. `TempEnviRun.Bat` - There is apparently no general way to specify the cache location used by the libraries "GPT: Many Python libraries use the OS temporary dir for caching. This is often hardcoded into the library.", however, it is possible in an environment "GPT:  Set the TMPDIR, TEMP, or TMP environment variables within the activation script of the virtual environment. export TEMP=/path/to/your/temp", this would then point to a temp location on your SSD drive. Thus, with a little editing of `TempEnviRun.Bat`, you too can still do things like run PACT on your Fallout 4 mods.  
3. Install [TetraCopy](https://www.codesector.com/teracopy), to copy files directly through memory instead of using cache, this means you can then copy data larger than the RamDrive between directories.
4. Regardless of the program, I had to keep the RamDisk under a certain size in order for Windows not to timeout on boot, even loading from mSATA, it was about 6144MB (4096 + 2048), 4096MB is a safe value. If you are looking for RamDisk software, then I can suggest [ImDisk](https://github.com/LTRData/ImDisk) for a free one limited to one drive.

### PREVIEW
CcAutoWash.Bat, doing its thing...
```

Script Initialized...


CcAutoWash In 10s..
..Executing CCleaner..
..Cleaning Complete.


...Script Complete.

```
TempEnviRun.Bat, For example, PACT will now load...
```

Script Initialized...


Setting Temporary Dirs..
..Temporary Directories Set.

Launching Target Program..
...Executing PACT_Interface.exe...
Hello World! | Plugin Auto Cleaning Tool (PACT) | Version 1.75 | FNV, FO4, SSE
MAKE SURE TO SET THE CORRECT LOAD ORDER AND XEDIT PATHS BEFORE CLEANING PLUGINS
===============================================================================
-----
SET YOUR LOAD ORDER FILE AND XEDIT EXECUTABLE TO ENABLE CLEANING
     (MOD ORGANIZER 2 USERS ALSO NEED TO SET MO2 EXECUTABLE)

PRESS 'START CLEANING' BUTTON TO CLEAN ALL ACTIVE GAME PLUGINS
(IF REQUIRED FILES ARE SET, IT WILL ENABLE ITSELF IN 3 SECONDS)
-----
```

## INSTRUCTION
- For `CcAutoWash.Bat`
1. Put batch into same dir as `CCleaner64.exe`.
2. Create a shortcut to it in `C:\Users\(YourUserName)\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup`.
3. Restart computer, no errors is good.
- For `TempEnviRun.Bat`
1. Put in same dir as target program.
2. Edit appropriate highlighted lines in script.
3. Run script, program runs.

### REQUIREMENTS
- CCleaner (64bit).
- Batch file support.
- Temp/Tmp folders on a RamDisk loaded from image.
- RamDisk software.
- Programs non-native to Windows, that dont run well.

### NOTATION
- I tried to do some complicated method of stats going through TEMP/TMP path, as no way of knowing pre-defined RamDisk letter, but, ran into path lengh issues, so kept it simple.
 
## DISCLAIMER
This software is subject to the terms in License.Txt, covering usage, distribution, and modifications. For full details on your rights and obligations, refer to License.Txt.
