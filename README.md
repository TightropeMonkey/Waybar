# Waybar Spotify Mattermost Integration

Credits to Alexays for developing the Waybar (https://github.com/Alexays/Waybar) and the media player support!

I have added a small integration to push the Spotify metadata as a Mattermost custom status.

## Features

For me it was important, that all metadata from various players are displayed in the Waybar but only in case of Spotify the metadata is set as Mattermost status.

Playing song in Mattermost status:

![Playing Song](images/mm-song-plays.png?raw=true "Playing Song in Mattermost Status")

Paused song in Mattermost status:

![Paused Song](images/mm-song-pause.png?raw=true "Paused Song in Mattermost Status")

When Spotify is closed, the custom status will be deleted.

## Configuration

Change global variables `mmserver` and `mmcookiedb` inside the `mediaplayer.py` file to your own values.

![Mattermost Configuration](images/mm-config.png?raw=true "Mattermost Configuration")

## How is works

After both variables are set, the script will read out the Mattermost auth-token and csrf-token from the Mattermost cookies sqlite database. The database is will be opened as read-only.

The status is sent to the Mattermost API by using the endpoint `/api/v4/users/me/status/custom`.

A custom status emoji with name spotify was created inside of Mattermost. If you want to change it:

![Mattermost Custom Emoji](images/mm-config-emoji.png?raw=true "Mattermost Custom Emoji")



