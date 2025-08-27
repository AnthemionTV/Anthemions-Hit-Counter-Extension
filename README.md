# Anthemion's Hit Counter Extension
An extension for Streamer.bot 1.0+ that allows for "hit" tracking. 
<img width="1884" height="678" alt="image" src="https://github.com/user-attachments/assets/e41848a7-ac62-4fbe-8c89-efaaea52ff5b" />

## Requirements
- [Streamer.bot](https://streamer.bot/)
- Imagination

## Features
- UI for Configuration including split names, color changes, split content, and more.
- Run Timer
- Hot key support via Streamer.Bot "triggers"
- Access to split data for personalization such as splits with complex visuals, Hit/ PB specific events, autorunning/ closing predictions, automating split names for channel redeems, and more!
- HTML Overlay using Websockets
  
## Setup
1) Launch Streamer.Bot
2) Ensure Websocket is turned on (Servers/Clients > Toggle 'On') _Default is 127.0.0.1:8080_
3) Copy import string and paste into Streamer.Bot import window or drag import file into Streamer.Bot Import Window (this will not work if you are in administrator mode). 
4) Run "FIRST TIME SETUP" Action in the "Anthemion's Hit Counter Extension" actions group. This will create all of the necessary files for the extension to work within your Streamer.Bot folder. You can also find the location of these files within the configuration window itself.
5) Run "Configuration Action." This will open the configuration window in a browser where you can create your split design (click apply settings to committ changes), splits (apply table to Streamer.bot to commit changes, resize to set split number total), and start the time via UI. After configuring your splits to your liking using the provided preview window, be sure to save what you have made!
6) Under the run time, the first url provided is the location of your overlay, add this as a browser source within OBS, crop and resize to your liking (Note: The extra red colored text can be useful for trouble shooting).
7) Assign hot key "Triggers" to the following actions (Core > Inputs > Key Press):
   - [AHC] Add Boss Hit
   - [AHC] Add Run Hit
   - [AHC] Split Increase
   - [AHC] Reset Run 
8) Enjoy!

## Planned Features
- Split specific timers and other speed run overlay features (Sum of best, PB indicatirs, pace indicators)
- Overlay Font Selection
- Automated OBS Overlay Source Creation
- Quality of life customizations (set preferred browser, UI improvements)
- Run statistics Display (most common split first hit, highest hit, most consistent, etc..)
- Autosplitter functionality or Compatability
- Counter Type (e.g. split clear/ not clear) as opposed to numerical values.
- Renamable columns via UI
- Change order of splits (currently this may impact stored PBs or other values depending on how it is done)

## Advanced Split Making
- Tutorial Coming Soon
<img width="199" height="297" alt="image" src="https://github.com/user-attachments/assets/3ea92ed7-8776-4e8f-9d23-84d8f90b5a50" />



## Known Issues
- The hit counter still shows some debug information when first starting. This will be phased out over time. To display your hitcounter, a web socket request must be sent. Actions such as starting the run timer or reset run will display the overlay. 
- Too many quick changes to the UI can cause some inputs to be lost (this is in testing more rapid than is likely in typical use cases).
- Changing split order may result in losing some stored values specific to the profile (i.e. PBs). I recommend saveing to a new profile until feature is added to the UI to avoid data loss.
