Credits to Alexays for developing the Waybar (https://github.com/Alexays/Waybar) and the media player support!

I have added a small integration to push the Spotify metadata as a Mattermost custom status.

## Features

For me it was important, that all metadata from various players are displayed in the Waybar but only in case of Spotify the metadata is set as Mattermost status.

![Playing song](images/mm-song-plays.png?raw=true "Playing song in Mattermost status")

![Paused song](images/mm-song-pause.png?raw=true "Paused song in Mattermost status")

When Spotify is closed, the custom status will be deleted.

## Configuration

Change the global variables mmserver and mmcookiedb inside the mediaplayer.py file to your own values.

