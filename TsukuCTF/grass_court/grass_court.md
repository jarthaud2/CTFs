# TsukuCTF 2023 - grass_court

![grass_court](https://tsukuctf.sechack365.com/files/4c52b905257a6ce0c6d43a4e1e94c072/tennis.jpg?token=.eJyrViotTi2Kz0xRsjI3NtJRKklNzAXzTMyBvLTMnFSoXC0AHngM-A.Zab8tg.yo_lqJIUrTNTL8miXhwbfsIThwU)

## Description:
しばらく使われていないテニスコートのようだ。
この日本にあるテニスコートの場所はどこだろう。
フラグの形式は TsukuCTF23{緯度_経度}です。
小数点以下5位を切り捨てて、小数点以下4桁で答えてください。

Looks like a tennis court that hasn't been used for a while.
Where is the location of this tennis court in Japan?
The format of the flag is TsukuCTF23{latitude_longitude}.
Round down to 5 decimal places and submit your answer to 4 decimal places.


## What I did

At first glance there is really not much information available. But zooming in behind the trees we can see that there are 2 large satellite dishes in the background.

I started by searching for all the large satellite dishes in Japan but was not really getting anywheres. 

A friend I was working with this on eventually found this [article](https://www.inamori-f.or.jp/en/211117) related to the visualization of a blackhole. Reading through the article I thought that maybe it wouldn't be a bad idea to check where these satellites in the article are located as there were 2 of them and the trees seemed to match up slightly. ![satellites](https://www.inamori-f.or.jp/wp-content/uploads/2021/08/20170314-vera-2000.jpg) 


And luckily enough, these were the satellites we had been searching for. When checking google maps, there is a tennis court as well as the triangle shaped tree line found in the original image.

The image was taken at the VLBI Astronomical Observatory 

## Rabbit Holes

I spent some time trying to figure out what the little cardboard cutouts on the trees were but couldn't find anything.

I also tried searching for the model of the A.C units found behind the tennis court to see if I could narrow down the area at all.


## Answer

TsukuCTF23{39.1349_141.1325}


