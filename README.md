
Zynga's Jukebox
==============

The Jukebox is a component for playing sounds and music with the usage of sprites with a special
focus on performance and cross-device deployment. It is known to run even on Android 1.6+ devices
and needs very few resources compared to other solutions on the web.


Features
--------

* Targets low-end devices and mobile platforms
* HTML5 Audio
* Flash Audio as fallback (support for Android 1.6)
* Sound-Spritemap Entries for easier playback
* Multiple Jukeboxes for parallel playback

Important: iOS devices are known to allow only one Jukebox to run, no parallel playback possible.


**Jukebox Manager adds the following features:**

* Codec Detection
* Feature Detection
* Automatic Work Delegation for busy Jukeboxes
* Automatic Stream Correction (useful for slow implementations)
* Automatic Looping for Sound-Spritemap entries
* Playback of Background Music

**Using Jukebox without Jukebox Manager:**

It is not recommended to use Jukebox without the Jukebox Manager, but it's still possible.
The Jukebox Manager offers Codec and Feature detection - to determine which kind of audio codecs will playback properly in your Environment.
If you want to still use Jukebox without Jukebox Manager, you will have to set *resources* to an Array containing only one resource.


Known Issues
------------

There's the problem with asynchronous playback, which can't be avoided on the JavaScript-side of the implementation.
Delays were measured up to 820ms on initial playback. iOS has also a problem when falling into sleep mode, as iTunes will play back the sound
file afterwards without stopping it.

Additionally, iOS' security model prevents a website from playing sounds without prior user interaction. Thus, you will have to use a button
or similar that will call player.play('background-birds') or similar.


Documentation
-------------

There's a huge documentation with demos, examples and best practises.
Take a look at it! It's located in the /doc folder.


