# open_command_linux
Mac's open command made to work on linux.

Most Terminal users will know that

$ open .
will open the current working directory in a Finder window. 

Trivially, it cannot merely open the current working directory, but any path:

$ open ~/Library/Preferences
$ open /etc
$ open ../..

This can be used as a quick way to navigate to hidden directories.

You can also open multiple folders at once:

$ open ~/Documents ~/Desktop ~/Downloads
$ open ~/D*

open can also open files. In general you can think of open as the command line equivalent of double-clicking a file or folder in Finder.

$ open document.pdf
will open document.pdf in the current working directory with the default application for PDF files (usually Preview). You can use this against multiple files as well:

$ open ~/Desktop/Screen\ Shot\ *.png
will open all screenshot files (if any) in a viewer in the default application (Preview).

If you have changed the default application that handles a file type or want to override the default application, you can use the -a option:

$ open -a Preview ~/Desktop/Screen\ Shot\ *.png
$ open -a TextEdit web.html
You can specify just the name of an application or the full path, i.e. /Applications/Preview.app. If you need to be specific, you can also specify an application’s bundle identifier with -b com.apple.Preview.

If you want to open a document but keep the application and the new document window in the background, use the -g option.

$ open -g ~/Desktop/Screen\ Shot\ *.png

Finally there is one more useful thing you can open:

$ open https://scriptingosx.com   # default browser
$ open vnc://TestMac.local       # Screen Sharing
$ open x-man-page://open         # show man page in Terminal



Tested on: 
Elementery OS Juno
Ubuntu 18.04


INSTALL INSTRUCTIONS
1. Download the file.

2. chmod 777 open

3. cp open /bin/

4. Test it! 

