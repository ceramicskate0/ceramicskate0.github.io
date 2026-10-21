---
layout: default
---

# C# DLL Payloading 1

`UPDATE: I have been informed (literally before i published the blog post) that subtee (its always subtee...) has shown this in a example somewhere but it was no longer public.`

## The Problem

Stay with me here im doing this from memory from a long time ago when i was on PTO and on a ski trip. During my personal research time I needed to make a C# DLL (I think I was doing sysmon detections) that would run a shellcode when a standardized class name was called by the executing executable. Say a LOLBIN that runs C#. I knew how to do this in C and even C++ but not in C#. Documention by other red teamers at the time on this was sparse at best when i started looking into this topic.

## What I did

In the image below I used code like this to get the DLL to be run shellcode from the executing executable.
 
![CSharpDLLRunClasses](https://github.com/ceramicskate0/ceramicskate0.github.io/assets/6934294/15b3a1c8-660d-4538-8379-80a3a375ff9e)

With this class in the project

```
public class ExampleExportsClass
{
          [DllExport("RegisterServer", CallingConvention = CallingConvention.StdCall)]
          public static void RegisterServer()
          {
              Method();
          }
          [DllExport("UnregisterServer", CallingConvention = CallingConvention.StdCall)]
          public static void UnregisterServer()
          {
              Method();
          }
          //Example rundll32 entry point :)
          [DllExport("StartW", CallingConvention = CallingConvention.StdCall)]
          public static void StartW(IntPtr hwnd, IntPtr hinst, string lpszCmdLine, int nCmdShow)
          {
              Method();
          }
}
```
Now im not going to give you the how to run your shellcode and how to make the dll evade EDR. Thats (conveniently) out of scope for this post.
In case your wondering I did make it hard to copy paste this on purpose.

## Conclusion

I cant recall if it was `regsvcs` or `regasm` (might even work on `regsvr32`) that would run the DLL code above. But based on [this](https://lolbas-project.github.io/lolbas/Binaries/Regasm/) I think it might be `regasm`. Heck it might even run with `InstallUtil`.

## Credits/Refs/Notes

- SubTee
- Since some of this example code i wrote just now on the fly. Im not sure much goes here. Im sure its been done by people somewhere. If so send me a request to add.

## Detections

- DLL written to disk
- C# Usage logs
- Commandline for apps
- Detections for this and many more found in my [sysmon fork](https://github.com/ceramicskate0/sysmon-config)

[back](./)
