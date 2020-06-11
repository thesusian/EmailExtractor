# EmailExtractor

A simple grep script used to extract emails from mbox files

This script works perfictly on linux systems and still not tested on other platforms

If you can't run this file use ```sudo chmod 777 EmailExtarctor.sh```

Note that this code is not perfect and will give some prsentage of rubbish but it will spare you a lot of work.

Just open this file with a text editor and coppy the command and modify it as you like.

All you have to do is replace (mboxfile.mbox) with the name of your file and (output.txt) with the name of the output file of your choise (don't forget to put txt at the end).

Here is the code if you don't want too bother opening the sh file

```grep -Po '(?<=(<)).*(?=>)' mboxfile.mbox | grep '@' | grep -v 'https' | grep "^.\{0,50\}$" > output.txt```
