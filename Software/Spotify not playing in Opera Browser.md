## Spotify not playing in Opera Browser

### Error:

When playing spotify or netflix content the player is no working.

### Explanation:

It is because the old versions cannot play DRM content.

### Solve (Both Linux & Windows):

1. Upgrade your opera browser.
2. If problems remains the same after upgrading, then go to your browser address bar and type <code>opera://about</code> and hit enter.
3. Scroll down to <b>Paths</b> option and copy the installation path of opera.
4. Go to this github page <code>https://github.com/nwjs-ffmpeg-prebuilt/nwjs-ffmpeg-prebuilt/releases</code> and download the new releases of <code>libffmpeg.so</code> file.
5. Copy the <code>libffmpeg.so</code> file and paste it to the install path of Opera.\

- For <b>Linux</b>: Open <b>Terminal</b> in your download folder and paste this command<code>sudo cp libffmpeg.so {your copied installed path}</code> and hit Enter.
- For <b>Windows</b>: Just copy the file and go to the installed path and paste it. It will ask for administrator permission and click yes.

6. After step 5, restart your browser and now you can play spotify music seaminglessly!

Happy Enjoying!!!
