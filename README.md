#Wraith-time-diff
This is a modified version of [wraith](https://github.com/BBC-News/wraith).
It is used to track daily changes for multiple urls on a single domain.

Look here first if you are trying to understand what's going on under the hood:
- `/Rakefile`
- `/lib/wraith/manager.rb`
- `/lib/wraith/wraith.rb`

This is where you can configure things:
- `/configs/config.yaml`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Change domain, fuzz, and other things.
- `/lib/wraith/javascript/snap.js`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Mess with timeout to fix situations when the screenshot is taken before page finishes loading.

Here are the commands:
- `rake cap`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Reads spider.txt and captures an image for each path found.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Moves images to a timestamped directory.

- `rake diff`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Uses imagemagick to compare the two most recent sets of images.


