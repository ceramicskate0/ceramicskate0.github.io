---
layout: default
---
![images](https://github.com/ceramicskate0/ceramicskate0.github.io/assets/6934294/3a854c99-f469-446b-a291-0f1d4fdae787)

Repo Link: https://github.com/ceramicskate0/SharpLeftOvers

## Background 
    So heres how this started...there i was doing Red team stuff minding my own business when...BAM! 
    i find bloodhound data and Kerberos tickets sitting on the disk of this box im on...of course im gonna use it...well after i look at it. 
    Turns out (and im sure you have run into this also) previous pentesters had not cleaned up. 
    Finding this kind of stuff makes tests go faster and well no need to redo the wheel. 
    So time to tool it. Since nothing gets fixed until you tool it. 
    Also i got the skeleton key idea from someones talk, i think it was red seige's.

# SharpLeftovers the story

## Ready...Start!

![start-bugs-bunny](https://github.com/ceramicskate0/ceramicskate0.github.io/assets/6934294/af00e53b-f809-41d5-af9b-89d41acafc4d)

So I assume you read the background by now. 

Also full disclosure this is my second time trying to create this blog and im hoping by tab wont crash and loose my blog. 

So when I found the left over artifacts from the previous tester I thought to my self how do I do this at scale. As you know speed and stealth are key on that short 3 month assesment.
As you know you might have many machine and all there is no way to know which of them might have key data on disk. 
Now we have tools for host recon sure we do. We have things like Seatbelt, trufflehog, etc.. But when I looked none of them focused on left over tester materials specifically.
I mean I get it, but really why not?!

It seems like we have all these tools to find things at scale on an operation but not sloopy testers left overs.

![nothing](https://github.com/ceramicskate0/ceramicskate0.github.io/assets/6934294/2f035b82-5551-4d79-9c64-851de5ec4359)

So when I decided I had to make a tool to fill this need. I started out by simply looking for things I found.

**FILES ON DISK!**

It also had to be run by C2 frameworks either `inline` or `fork & run` methods. This mean **NO** `Enviorment.Exit()` super annoying when i see a c# impant that does this.
So I started out by making some standard file search methods withing the tool. This became a interetsing issue taking me back to my Computer Science days...


## The Coding

![coding](https://github.com/ceramicskate0/ceramicskate0.github.io/assets/6934294/f5e50dfe-e91b-4527-a2b8-356657ef380e)



## {Conclusion}

## {Credits/Refs/Notes}

[back](./)
