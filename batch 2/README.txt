Project PHaEDRA - Annie Jump Cannon - Annie Cannon Notebooks #126

https://transcription.si.edu/project/50684

-----------------

Method

```
Manually browse to https://transcription.si.edu/project/50684?status=transcription

save html file

copy to links-2.txt and delete all except entries with references to download images

copy to links-3.txt and format as wget input file

wget -i links-3.txt

mkdir images
mv *jpg images
cd images
ls -1 | awk '{print "mv " $0 " phraeda-" $0}'|bash

sudo apt-get install img2pdf # https://github.com/myollie/img2pdf from https://askubuntu.com/a/1524443/543234

img2pdf images/*jpg -o "phaedra-2208 to_transcribe (all).pdf"

ls -1 images | head -n3
img2pdf images/phraeda-0002208.039.jpg images/phraeda-0002208.050.jpg images/phraeda-0002208.053.jpg -o "phaedra-2208 to_transcribe (first 3).pdf"


img2pdf images/phraeda-0002208.0*.jpg -o "phaedra-2208 to_transcribe (before 100).pdf"

img2pdf images/phraeda-0002208.1*.jpg -o "phaedra-2208 to_transcribe (100's).pdf"
```

Upon feedback:

- copy-paste transcript edited remotely
- check diff: `git diff --word-diff-regex=.`
- edit to match
- add fields to each page header in the txt file: Link, Logs
