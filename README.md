# Reality Application

AR VR Reality for Web, Desktop, Mobile, and beyond

This Repository aims to develop one application that will work in multiple Realities.

## Table of Content

* [Introduction](#Introduction)
* [Watchlist](#Watchlist)
* [UI](#UI)
* [Storage](#Storage)
* [Concepts](#Concepts)
* [Hardware](#Hardware)
* [](#)

# Introduction

I will design a Virtual Reality or VR headset and controllers, as a Do it Yourself or DIY project, with all the planes, and even some links to equipment that can test the optical systems this project has designed, such as 
[Radiant Vision Systems](https://www.radiantvisionsystems.com/products/imaging-colorimeters-photometers/ar/vr-lens), 
as well as others, so you can ensure the design you will use is tested.

The optical system I will be using is per eye monitor, so you will have a lens, this can be glass or plastic, without or witout a perscription, but I will make sure you can order these lens from any opical glass manufacture, or your eye doctor, I will make sure these are the same sizes as those for other gear, like the Quest system, or more expensive units.

My Goal is to design a wrap around glass, these have a band that go around your head, and tighten in the back, it has an optional strap that goes over your head, and another optoinal helment you put on, this is used for motorcycles, and uses an approved helment for legal use in any state, these will come in AR or Agumented Reality, where you can see through the glasses into your reality, and see well enough to legally drive on any highway, the interaction in drive mode, is to show you all your instruments on a Heads Up Display or HUD, you see your fuel level, and time till empty, and your speed, as well as the speed limit, and will show you in read when you go over that.

The software can be upgraded to include the manual for the vechel your driving, so it can show you how to troubleshoot, and fix things that can go wrong, and tell you when to call a tow truck, and even make that call for you, but you still have to talk to them, but it can pull up informaton about where you are, making it easier for them to find you.

I will use Qt as well as .Net MAUI, to write the same app, to show you how you can write the same app using a different framework, to achieve the same thing.

VR Gear is not required to follow this project, the gear created here is purly experimental, and I do not have the money to actually buy the parts and the test equipment to test this design, but that is how a lot of projects get started, I will use off the shelf parts, that have well known specs, and is suitable for the use of VR or AR, keep in mind these two technologies require different applications.

My goal is to show you in code how to write for both AR and VR while being compatible with Reality, and why I call this project a Reality Applicatoin.

We have to be able to write an Application in Unreal Engine 5 or greater, Qt, .Net MAUI, which covers the Cross-Platform aspects of writing a one Application that can run on Linux, Android, Mac, iOS, Windows, PI and other Operations Systems, devices, and Machines, so I will show you how to do this in code, using Unreal Engine 5, Qt 6, and .Net MAUI latest.

This Application is a simple Project Manager that manages Books, and these books are in a specific format that this applicaton can handle accross multiple devices like Mobile devices, Smartphones, Tablets, as well as Laptops, Desktops, TV, and watches, I will cover all these topics in one working Applicatoion.

## Watchlist

* [Smart Contact lens](https://hackaday.com/2022/05/22/smart-contact-lenses-put-you-up-close-to-the-screen/)
* [VR Blue Light Lens](https://www.vr-wave.store/)

## UI

When we write a UI that needs to work across all devices, like desktops, laptops, smartPhones, smartTv, smart Watches, and so on, and web is another factor, so the common factor is that every control we have for one platform must work on all of them.

Using Qt 6, I would Quick using QML, where JavaScript is compliled like C, and this uses the Mobile Application look as the common denuminator, now WebAssembly has its own look, but if we want to deal with Data, we need a system everyone can use for Free, so this is what divides free from paid, and that is storage of all your files.

Using .Net MAUI is similar, and currently, I am waiting for Linux support, and .Net 7, so that intergration is already built in, and I do not have to migrate.

Unreal Engine has its own look when if comes to data entery, and this is what this applicatoin must focus on, how to get all the same functionality from all my applicaction controls I need.

Let me list all the controls we need in this applacation:

* Line Editor: This is a single line entery like User Name or Passwork where you see astrics when you type.
* Text Editor: This is a multiple line entery like Discription, and is limited to only text characters.
* Text Processor: This is like a Text Editor only it has full Text styling like **bold**, *italic*, and ~~strike through~~
* List: Display a list of items.
* List/Detail view: List that on click, it has a detailed page.
* Links: Links to other like items, or internal methodes
* Supported Document types: All Supported by Open Office, plus: Videos, Audios, PDF, HTML, and other formats.
* Push Buttons: With actions
* Layout types: Stack, Flow, Grid, and other popular layouts
* Text to Speach or TTS: This will use the native installed software to handle requests and processing
* Speach to Text or STT: This will use the native installed software to handle requests and processing
* Email: IMap, and limited POP3 on devices that support it
* SMS: Device dependent
* The list goes on to what is a common control for all devices and OS

## Storage

File storage is device dependent, there is no magic when it comes to where you want to store your files, if you are on a device like a smartphone or tablet, you might have limited storage, so databases, documents, videos, audios, and other documents, take up resources, yet you need to store files for free, and there are options like [Google GDrive](https://drive.google.com/drive/my-drive), or [MS One Drive](https://www.microsoft.com/en-us/microsoft-365/onedrive/online-cloud-storage), and others, so this app must be able to know where to store files.

I will talk about a VPS or Virtual Personal Server, where you pay to have a Virtual Server like Linux, Windows, or Mac, and can run a Website, or host files, which is what I will talk about here, and you will find that informatoin in the [Wiki](https://github.com/Light-Wizzard/RealityApplication/wiki).

## Concepts

To write an applicaton that is cross-platform, usign Qt 6 and above, and the latest MS .Net MAUI, and runs on many devices, and also runs as a Game using Unreal Engine 5 and above, and Unitity, just so I can show the same thing using two differnt Game Engines.

## Hardware

You need a modern CPU and GPU that will run Unreal or Unitiy Games if you want to run in a Game mode, or VR or AR mode, otherwise, you should be able to run the appliations written in Qt 6 and above, or the lastest .Net MAUI, so you need to have these applications or SDK installed.

## Realitiy

Reality is what we sense through visual sight, audible sounds, or touch, just 3 of our main senses, but we have senses for smell, and taste, but those are not functions we can program an environment to cover, we have no smell or taste controls, so our reality is limited to what controls we have now, but we can talk about building these controls because smell and taste are controls we can add, but how they smell and taste will be up to you.

Not everyone can see or hear or might have an impairment, as I do, so this project is about multiple forms of presentation, a way of saying we have sight, sound, and touch, and that can include braille, so I will try to address how to create VR or AR gear for those with disabilities.

### End of File
