#Wraith-time-diff
This is a modified version of [wraith](https://github.com/BBC-News/wraith).
It is used to track daily changes to multiple urls on a single domain.
The changes are visually tracked by taking screenshots and generating diff images.


####Look here first if you are trying to understand what's going on under the hood:
- `/Rakefile`
- `/lib/wraith/manager.rb`
- `/lib/wraith/wraith.rb`


####This is where you can configure things:
- `/configs/config.yaml`
Change domain, fuzz, and other things.

- `/lib/wraith/javascript/snap.js`
Mess with timeout to fix race conditions.

####Here are the commands:
- `rake cap`
Reads spider.txt and captures an image for each path found.
Moves images to a timestamped directory.

- `rake diff`
Uses imagemagick to compare the two most recent sets of images.


