## Video Platform Cloud

### ABOUT
C# application which utilises video platform PeerTube to store files. Local files are encoded into videos and uploaded to PeerTube using it's API. Videos can then be downloaded and decoded back into original files. In this project I explored working with video files, encoding and communicating with servers using protocols.

### BEFORE USE INSTRUCTIONS
1. Create an account and channel on some PeerTube instance (for example https://peertube.otakufarms.com)
2. Fill out url of your peertube instance and your channel name in the `files\peertube_channel_information.json` file
3. Fill out your username and password in the `files\peertube_credentials` file
4. Fill out path to the directory you want to have synchronised in the `files\sync_folder_path.json` file

### LAUNCH INSTRUCTIONS
This application was developed for the Windows operating system. After unzipping run the `RUNNER.bat` file.

### USING
After launching the application wait for the message `vid file synchronizer started` which means that logging into your peertube account was succesful.\
Command `vid status` outputs a message describing which files are and aren't synchronised with the server.\
Command `vid add` followed by a file name adds that file to a list of files waiting for synchronization.\
Command `vid remove` followed by a file name removes that file from the list of files waiting for synchronisation.\
Command `vid push` uploads files waiting for synchronisation to the server.\
Command `vid pull` downloads files which are not stored locally from the server.\
Command `vid delete` followed by a file name deletes the file both locally and also from the server.\
Commands `vid resolve local` and "vid resolve server" followed by a name of a conflicitng file keeps the local or server version of the file and discards the other version. 
