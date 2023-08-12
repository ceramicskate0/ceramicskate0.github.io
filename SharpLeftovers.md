---
layout: default
---

![images](https://github.com/ceramicskate0/ceramicskate0.github.io/assets/6934294/3a854c99-f469-446b-a291-0f1d4fdae787)

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

Also full disclosure this is my second time trying to create this blog and im hoping by tab wont crash. 

So when I found the left over artifacts from the previous tester I thought to my self how do I do this at scale. As you know speed and stealth are key on that short 3 month assesment. I know it sounds like a long time. Its really not in all cases. 
As you know you might have shells on many machines and all there is no way to know which of them might have key data on disk. 
Now we have tools for host recon sure we do. We have things like Seatbelt, trufflehog, etc.. But when I looked, none of them focused on left over tester materials specifically. I mean A/V and EDR find the tools themselves but not the left over artfiacts as much.
I mean I get it, but really why not?! Also since I had to review many many tools when I was doing red teaming that it was easy to add the artifacts into this tool as a workflow.

It seems like we have all these tools to find things at scale on an operation but not sloopy testers left overs.

![nothing](https://github.com/ceramicskate0/ceramicskate0.github.io/assets/6934294/2f035b82-5551-4d79-9c64-851de5ec4359)

So when I decided I had to make a tool to fill this need. I started out by simply looking for things I found.

**FILES ON DISK!**

It also had to be run by C2 frameworks either `inline` or `fork & run` methods. This mean **NO** `Enviorment.Exit()` super annoying when i see a C# project that does this. When it says it is desgined to be run `inline`.
So I started out by making some standard file search methods withing the tool. This became a interetsing issue taking me back to my Computer Science days...


## The Coding

![coding](https://github.com/ceramicskate0/ceramicskate0.github.io/assets/6934294/f5e50dfe-e91b-4527-a2b8-356657ef380e)

So when i started coding this. I had the same goals as always. Simple, easy to use, repeatable.
I decided to focus on files on disk. Since this is what I found. Now thats no 100% I know things in AD are statically set with some tools and that can be resued but thus far I have only focused on 1 of those.

When I started coding the project I had to find a way to get files on disk quickly (kinda failed there). Took me back to my old computer science days honestly. I originally wanted to use [Directory.EnumerateFiles Method](https://learn.microsoft.com/en-us/dotnet/api/system.io.directory.enumeratefiles?view=net-7.0) like I had seen in other tools that do recon on hosts at scale usingC C#...oh sorry CSharp...or Sharp* lol.

However, after some testing there are some issues with this approach that some of those authors might not have tested for. Namely what happens when that method runs across files that you dont have permissions to access. When I tried it that was when the search stopped. So it would end up missing eveything it had not already found by that point.

This means I had to use a little bit of a slower method if I wanted to keep this simple. 


## {Conclusion}

## Credits/Refs/Notes

- Repo Link: https://github.com/ceramicskate0/SharpLeftOvers

[back](./)
