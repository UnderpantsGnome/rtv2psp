This script was based on the version done for windows, you can find info on it
at http://www.avsforum.com/avs-vb/showthread.php?t=554079

For updates, requests or to file a bug you can go to
http://trac.underpantsgnome.com/rtv2psp

The content below has been adapted form there.

The script is designed to work with ffmpeg, which is an open source video
transcoding program that is at the heart of the most popular open source
encoding tools like Handbrake and many others.

ffmpeg is included with this, if ou want to use a different version just edit
the script to point to the version you want.

If you have rtvtools installed and want the script to use them, you'll need to
update the script so it can find evtdump and rtvedit on your system.

You'll also need to update the directory you want logfiles to go and where you
want the PSP videos to be stored.

If you want the videos copied automatically to your PSP, you'll need to specify
the mount point it is assigned when you connect it to your Mac.

By default, the program will create medium quality PSP videos and will
automatically copy the files to your PSP.  It will not edit commercials by
default.  If your PSP is not connected, it will check for it once every 60
seconds.  As soon as it detects your PSP, the file copy will automatically
proceed.  The script insures the PSP filename is unique to prevent accidental
overwrites.

At medium quality, you should be able to store more than 90 minutes of video on
a 512MB Memory Stick Duo. At low quality, which isn't that bad, you should be
able to store more than 120 minutes.

You can use the script with DVArchive to process downloads automatically.
In DVArchive, goto Files|DVArchive properties|Downloads, in the
"Post Download Processing" section, put the path to rtv2psp. The script will
then run after every download finishes. You can also drag and drop videos from
your Local Guide directory to the script if you have it installed on your
desktop.

How long the entire process takes depends on the RTV recording quality
(High, Medium, or Standard), your DVArchive download speed and the speed of your
computer. Transcoding MPEG-2 to MPEG-4 taxes even the fastest Mac. The script
uses the two pass method to encode the video file, which takes twice as long,
but results in much smaller video files.  You can, however, safely disable the
second pass by commenting it out. It takes my 2.4GHz P4 about 90 minutes to do
two passes at medium quality on a 60 minute program, and results in a 260MB
file.

This script "should" work on any version of OS X, but of course your mileage may
vary.

By default, you can transcode multiple video files simultaneously, but if you
enable editing with rtvtools, you can only transcode one video at a time.
For some reason, rtvtools won't allow more than one copy of its programs to run
at a time.
