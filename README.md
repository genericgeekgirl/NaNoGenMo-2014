NaNoGenMo-2014
==============

Adri's NaNoGenMo-2014 entry

The following commands create a "novel" of about 65K words, using the 2013 NightFloyd transcripts as a corpus. Lines consist of commands given to Floyd in the toyshop, comings and goings of players, and chatter on the channel #ClubFloyd. Not included are the replies from Floyd. Transcripts were originally downloaded from http://www.allthingsjacq.com/interactive_fiction.html#clubfloyd.

Use this command to download the transcripts:

`curl http://www.adriandaleksey.com/NaNoGenMo-2014/interactive_fiction.html | sed 's/"/\n/g' | grep -P "2013\d*-NF" | sed 's/^/http:\/\/www\.adriandaleksey\.com\/NaNoGenMo-2014\//' | xargs curl | grep '<td class="interlude">' | sed -e 's/<[^\>\<]*>//g;s/[LINK]//g;s/\t//g;s/  / /g' > corpus`

And now you can generate novels to your heart's content using sort. Try whatever arguments you like.

`sort -uR > novel`

I'm sure all of this could be done more cleanly, but eh. It works :D
