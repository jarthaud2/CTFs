# Reversing

## Unpacking
Before you enter the Oasis, you'll need to acquire top-of-the-line tech to give you the edge. You've ordered a brand-new X1 Haptic Bootsuit - now you just need to unpack it.

## Solution

This challenge came with a .zip to download. Afer having unzipped the file and running `file unpacking` on the file we find out that `unpacking` is executable file. Running this executable outputs the following:


    Congratulations on the purchase of your brand new X1 HTB (HapTic Bootsuit) To enjoy the most immersive experience the Oasis has to offer, follow these three steps: 

    1) Unpack this box (using your patented UPX (Ultimate Package Executor(™)) box cutting tool)
    2) Pull on the strings to unfold your brand new suit
    3) Log in and enjoy!

I was unsure what to initially do but because this was a reverse engineering problem I defaulted to using the `strings` command on the file first to see what text from the executable would show up, most of it was garbage but there was 2 things that caught my eye:

1. Firstly, there seemed to be a flag in the strings `HTB{T6-Ultimat.n-cker} sadly, this flag did not work and was not what I was looking for.
2. Secondly, the following was in the output: `$Info: This file is packed with the UPX executable packer http://upx.sf.net.` 

I decided to look into UPX more and ended up finding out that UPX also can decompress files, given that I just saw a possible flag and that the file was compressed with UPX I decided to try decompressing the file using the following command `upx -d unpacking`. And then running `strings` and upon inspection of the newly decompressed file the flag was found.

In hindsight, the output of the initial executable was extremely helpful.


