# To run your react native application

to open in expo go
Npm start
Or
Npx expo go

Gotcha:
You must be on the same network for both devices

In Android Studio
Open android Studio
(Small type in the middle of the page) -> More Actions -> Virtual Device Manager
Choose the device already created or “Create Device”
Choose “play” button.

Go to VS Code
Type “npn run android”
Note — on 3/28/23 I haven’t gotten this to work much. It seems more touchy than the expo emulator.

# JSON Server start up

Go to
~/Desktop/NucampFolder/json-server

check your json-server version:
json-server -v

Start up your json-server
json-server -H 0.0.0.0 --watch db.json -p 3001 -d 2000

# Gotcha: No data is showing up. Your IP has changed.

Get your IP address. On Mac the command is:
ipconfig getifaddr en0
That will echo your IP address for example:
192.168.202.223

Open up BaseUrl.js file in the /shared/ directory:
export const baseUrl = "http://192.168.202.223:3001/";
Replace the old IP with the new.

reload everything. That will probably work.
