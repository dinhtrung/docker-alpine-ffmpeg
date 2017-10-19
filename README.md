# docker-alpine-ffmpeg

## Rename File

The image contain Perl rename script. To rename file, use the following commands:

~~~
rename.pl 'y/A-Z/a-z/' *
rename.pl 's/(\s+)/-/g' *
rename.pl 's/(-+)/-/g' *
rename.pl 's/[^a-z0-9_\-\.]//g' *
~~~

## Extract FFMPEG thumbnailer

To extract whole folder content

~~~
for i in `ls *.mp4`; do j=`basename $i mp4`png; echo "$i ---> $j"; ffmpegthumbnailer -i $i -s 0 -o $j; done
~~~
