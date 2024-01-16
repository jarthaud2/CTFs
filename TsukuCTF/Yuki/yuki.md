# TsukuCTF 2023 - Yuki

![Yuki](https://tsukuctf.sechack365.com/files/b93fa5b83a93c069f413758f942deb32/Yuki.jpg?token=eyJ1c2VyX2lkIjo3MzIsInRlYW1faWQiOjQ3MiwiZmlsZV9pZCI6ODF9.Zab6TQ.kPgOIG5v10RG8YpEJ3LsY1-nbuw)

## Description:
Snow, silent, at window.

The flag format is TsukuCTF23{latitude_longitude}.
Latitude and longitude are rounded down to the fourth decimal place (note the precision).

## What I did

I started with using the entire image on yandex but this didnt really work. I then thought that maybe the bridge in the image was special so I tried looking into special bridges in northern Japan but that didnt yield any results either. 

I then tried to crop out the house with the red roof and use Yandex with that image instead. This pointed me to an area in Japan called Jozankei (Rather small city). After searching for the river and the 2 bridges seen in the image, the location was eventually found using the cropped yandex search. I decided to crop the red house in the image as its rather unique compared to the other houses seen in the image.

## Rabbit Holes

A snow pole can be seen on top of the bridge and I spent a too much time trying to figure out what part of japan uses that kind of snow pole. This was a waste of time, it could have been useful if it was a snow pole from hokkaido as they are unique to the area but this one isnt.


## Answer

Using the Yandex suggestion, I found out that this image was taken inside a cafe in the Jozankei View Hotel

TsukuCTF23{42.968_141.166}


