# bac-tracker
A tracker for Blaze and Caves Minecraft advancement pack. The tracker manages and puts all advancements in a google spreadsheet.

# desclaimer
1. only works with sftp servers. does NOT work with ftp
2. this might or might not crash a lot ![Susge](https://cdn.discordapp.com/emojis/912653211607924736.webp?size=48&quality=lossless)

# Installation Instructions
Download bac-tracker.zip from [latest release](https://github.com/p1k0chu/bac-tracker-over-sftp/releases) OR build it yourself OR just download repo and install [python interpreter](https://www.python.org/downloads/)

1. Unzip `bac-tracker.zip` You should have a data folder, settings folder, and an exe
2. Get a credentials json by following the instructions [here](https://www.youtube.com/watch?v=KIAo3Lgsk_Q), you only need to watch until 1:40 in the video. The rest of the video is specific to reset-tracker.
3. Put that json into the settings folder
4. Rename that json to `credentials.json`
5. Make a copy of the [1.21 Template](https://docs.google.com/spreadsheets/d/1Gyp1atdQ7QLEWRHBQ2AQFaTcg38jzZFPvaCOE4OeJhI/edit?gid=37686975#gid=37686975)
6. Open `credentials.json`
7. Inside you will find a field called `"client_email"` copy the associated value, and share it with your spreadsheet.
8. Open `settings.json`
9. Copy the spreadsheet link and paste it in between the quotation marks for the `"spreadsheet-link"` field.
10. Navigate to your world file on the server and copy the full file path. (Ex: `/world`)
    a. Might be some cursed stuff like showing you "/home/container/world" but in sftp it ends up like "/world" be aware (my case)
11. Paste the file path into the `settings.json` value for `"path_on_remote"`
    a. Warning: back slashes are funky in strings, either convert all the slashes to forward slashes, or turn back slashes into double back slashes:
        - Acceptable: `.../saves/bac-world/` or `...\\saves\\bac-world\\`
        - Unacceptable: `...\saves\bac-world\`
    b. you should leave "path_to_world" empty, but if you want you can make a separate folder, its just a folder to put all downloaded world files.
12. Running ![YIPPEE](https://cdn.discordapp.com/emojis/1084539417861029938.gif?size=48&quality=lossless)
12.1 If you want to run it with python interpreter, set your working directory to `tracker` folder, create venv `python -m venv venv`, either run (every time you open new console window) `venv\Scripts\activate.bat` (windows) or `source venv/bin/activate` (linux), and run it with `python src/tracker.py`
12.2 or run compiled tracker.exe
13. ![Prayge](https://cdn.discordapp.com/emojis/1153599246759637023.webp?size=48&quality=lossless)
14. If you encounter any errors open issue on this repo or whatever.