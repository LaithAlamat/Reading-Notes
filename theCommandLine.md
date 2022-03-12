<h1>The Command Line</h1>
A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

- <h1>opening a terminal</h1>
You just need a SSH client

- <h1>The Shell, Bash</h1>
is a responsible for how the responses looks and appear after writing commands

- <h1>So where are we and What's in Our Current Location</h1>
we can use ***pwd*** to show our working directory and we can use ***LS*** to show the content of the current location

- <h1>paths</h1>
- relative path: relative to our current location
- absolute path: dependant on the root directory
- ~ (tilde) - This is a shortcut for your home directory
- . (dot) - This is a reference to your current directory. 
- .. (dotdot)- This is a reference to the parent directory.

- <h1>changing directory</h1>
we can use ***cd*** to change the directory 

- <h1>More About Files</h1>
everything is case sensitive so we have to be sure of the captilization, spaces are also something we need to take note on, we have to use quotes ("") or backslash ( \ ) for names with spaces so we can use them properly and for linux to understand it, we can check for hiddin files using ls -a
List the contents of a directory, including hidden files.

- <h1>Manual Pages</h1>
man <command>
Look up the manual page for a particular command.
man -k <search term>
Do a keyword search for all manual pages containing the given search term.
/<term>
Within a manual page, perform a search for 'term'
n
After performing a search within a manual page, select the next found item.

- <h1>File Manipulation</h1>
mkdir
Make Directory - ie. Create a directory.
rmdir
Remove Directory - ie. Delete a directory.
touch
Create a blank file.
cp
Copy - ie. Copy a file or directory.
mv
Move - ie. Move a file or directory (can also be used to rename).
rm
Remove - ie. Delete a file.

there is no undo in linux so we have to be careful about this.


