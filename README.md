# Fuckdisk - translucent storage

Ia a translucent temp-disk with self-destroy feature, will keep your files for 24 hours. Fdisk is a manifest rather that project or startup. At this moment fuckdisk allows to store 100mb files, we're planning to increase this limits but at this moment we concerned on building infrastructure and increasing capacity.

Initially fuckdisk was an internal service for serving internal needs, helped to store files securely, prevent unauthorised access and kick-ass tool for freelancers who has "confirmed" something.

## What makes fdisk secure?
AES256 and it doesn't, because everything is relative. All files getting encrypted with AES256 algorithm with random key which generates around 3.9722397531317123e+21 different combinations. Theoretically it makes impossible to decrypt file without key in next 10 million years. 

## Can someone take the file outside?
At this moment I'm working on client-side encryption which will make file more stronger however for daily needs - SSL plus my word - should cover.

## When source code will be available?
Once I'll be ready.

## How it Works
Just imagine, you need to share important file with abstract person but you wish to make it visible from outside and prevent further access to file. We store your files encrypted for 24 hours, even if someone can get this file - only you know the key which allows you to download.

We are not FBI, and we not interested in things you do, we don't need to keep secret key, or physical copies.

You upload file
- API generate keys for uploaded files.
- API also encrypt your file using secret key and provide download URL
- API checking file timestamp and remove everything older than 24 hours time frames.

## FAQ
#### Can I restore and download the file in case if I forgot the key?
— No. We don't keep any copies and secrets.

#### Does self-destroy files will live longer than 24h?
— No. Actually file will be removed in two cases - file has been downloaded (1), file reached 24h frames (2).

#### I've asked freelancers to do some work for me and uploaded sources with fuckdisk, unfortunately freelancer said that he cannot decode this file.
— Two options - you've sent wrong key (1), freelancer is liar and not downloaded this file in terms, consider to hire another (2).

#### Do you open for partnership at this moment? I just interested to please some ads on your site.
— No. At this moment we giving a try for everyone to be a part of this service by supporting this project.
