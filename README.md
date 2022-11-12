# Reality Application

AR/VR Reality for Web, Desktop, Mobile, and beyond

There are two types of hardware displaying alternate realities, one is Arguments Reality or AR, and the other is Virtual Reality or VR.

This Repository aims to develop one application that will work in multiple Realities.

## Table of Content

* [Introduction](#Introduction)
* [Watchlist](#Watchlist)
* [UI](#UI)
* [Storage](#Storage)
* [Concepts](#Concepts)
* [Hardware](#Hardware)
* [Notes](#Notes)

# Introduction

I will design a Virtual Reality or VR headset and controllers, as a Do it Yourself or DIY project, with all the planes, my goal is to make a helmet that has two dropdown shields, the inter shield is see-through, and the shield makes up a video monitor that you can see-through for use as an AR system, while the outer shield will act as a blackout screen that will make it very dark inside the hood, it will require a face mask to be worn, this straps on to your head with an elastic strap, and goes over your nose, such that your nose is on the outside of the shield, so you can breathe, and it turns AR into VR.

I will use both the latest Unreal Engine and Unity for Game Engine, and for the applications, I will use Qt as well as .Net MAUI, to write the same app, to show you how you can write the same app using a different framework, to achieve the same thing in different realities.
VR Gear is not required to follow this project, the gear created here is purely experimental, and I do not have the money to buy the parts and the test equipment to test this design, but that is how a lot of projects get started, I will use off the shelf parts, that have well-known specs, and is suitable for the use of VR or AR, keep in mind these two technologies require different applications.

My goal is to show you in code how to write for both AR and VR while being compatible with Reality, and why I call this project a Reality Application because I plan on showing you how to build a system that can be easy to build, low-cost, and works.

We have to be able to write Applications using the latest Unreal Engine, Qt, MS Dot Net MAUI, which covers the Cross-Platform aspects of writing one Application that can run on Linux, Android, Mac, iOS, Windows, PI, and other Operations Systems, devices, and Machines, so I will show you how to do this in code, using Unreal Engine, Qt, and .Net MAUI latest.

This Application is a simple Project Manager that manages Books, and these books are in a specific format that this application can handle across multiple devices like Mobile devices, Smartphones, Tablets, as well as Laptops, Desktops, TV, and watches, I will cover all these topics in one working Application.

## Watchlist

* [Smart Contact lens](https://hackaday.com/2022/05/22/smart-contact-lenses-put-you-up-close-to-the-screen/)
* [VR Blue Light Lens](https://www.vr-wave.store/)

## UI

When we write a UI that needs to work across all devices, like Desktops, Laptops, Smartphones, Smart tv, Smart Watches, and so on, and the Web is another factor, so the common factor is that every control we have for one platform must work on all of them.

Using Qt 6, I would Qt Quick, using QML, where JavaScript is compiled like C, and this uses the Mobile Application look as the common denominator, now WebAssembly has a Web look, but if we want to deal with Data, we need a system everyone can use for Free, so this is what divides free from paid, and that is the storage of all your files.

Using .Net MAUI is similar, and currently, I am waiting for Linux support, and .Net 7, so that integration is already built in, and I do not have to migrate.

Unreal Engine has its look when it comes to data entry, and this is what this application must focus on, how to get all the same functionality from all the application controls I need.

Let me list all the controls we need in this application:

* Line Editor: This is a single line entry like User Name or Password where you see an asterisk when you type.
* Text Editor: This is a multiple-line entry like Description, and is limited to only text characters.
* Text Processor: This is like a Text Editor only it has full-Text styling like **bold**, *italic*, and ~~strike through~~
* List: Display a list of items.
* List/Detail view: List that on click, it has a detailed page.
* Links: Links to other like items, or internal methods
* Supported Document types: All Supported by Open Office, plus: Video, Audio, PDF, HTML, and other formats.
* Push Buttons: With actions
* Layout types: Stack, Flow, Grid, and other popular layouts
* Text to Speech or TTS: This will use the natively installed software to handle requests and processing
* Speech to Text or STT: This will use the natively installed software to handle requests and processing
* Email: IMAP, and limited POP3 on devices that support it
* SMS: Device dependent

The list goes on to what is a common control for all devices and OS

## Storage

File storage is device dependent, there is no magic when it comes to where you want to store your files, if you are on a device like a smartphone or a tablet, you might have limited storage, so a database, documents, video, audio, and other documents, take up resources, yet you need to store files for free, and there are options like [Google GDrive](https://drive.google.com/drive/my-drive), or [MS One Drive](https://www.microsoft.com/en-us/microsoft-365/onedrive/online-cloud-storage), and others, so this app must be able to know where to store files.

I will talk about a VPS or Virtual Personal Server, where you pay to have a Virtual Server like Linux, Windows, or Mac, and can run a website, or host files, which is what I will talk about here, and you will find that information in the [Wiki](https://github.com/Light-Wizzard/RealityApplication/wiki).

## Concepts

To write a cross-platform application, using Qt, and MS .Net MAUI, that runs on many devices, and also runs as a Game using Unreal Engine, and Unity, just so I can show the same thing using two different Game Engines.

I decided on a complete helmet over what is currently out there, the reason is simple, I plan on putting in speakers, 3 sets, forward, mid, and back of the head, these will be zones in the software, and will be used to give you a sense of distance. The two shields will switch you from AR to VR, so we reuse the hardware we have and repurpose it.

This device will use 3 types of connectivity:

• Network cable RJ-45
• Bluetooth
• WIFI

### Project-Manager

A Project Manager gives you a start and stop times, and you have tools to manage that time in between these two dates, to help you get that task done, and most software does this by giving you a To-do list, so we will do this, but I want to get beyond that and help you research things, and add links to things you found of use, and even copy and paste with situations and annotations, and now it sounds like we are writing a book, and what we will be doing.

What is a book, is a good question, what is a project, well that can be described in a book, so to make things easy, I will just make a Book Manager, that has a Project manager built in.

We will start off with the interface, in Game mode, we have an empty bookshelf, in the App, this can be an empty list, and now I will go back and forth from Game mode to App mode, so these are what we have:

•	Bookshelf (Open Office Document types, and Word DocX)
•	Video shelf
•	Audio shelf

The Book is stored in an SQLite Database, this is a common database that works well for Desktop, and Mobile, but on the Web, you have an issue as to where the database is located, so I will address that using a URL for all assets.

The concept of writing a book using this application goes like this:

You start with a concept, for this example, it is a dream about a Wizard that showed you a Crystal Time Recorder, I have a GitHub Project called the [The Stone Crystal Wizard](https://github.com/Light-Wizzard/The-Stone-Crystal-Wizard), so this is easy to follow, we have a title, so now we create the book.

Every book is made up of one or more works that will form a sentence, which is one Database entry in this application, now there are words that have a period in them, so we have a special character for those, thus an end of line period is also a special type of character, so you will find them on the toolbar. 

The reason why I use special characters for some punctions like a period is that there are many uses for it, .Net MAUI is one such case, as is the end of this subject. 

You take all your sentences and you put them in the order you want them to read in, and then you format them by grouping them into paragraphs, categorizing them, and subcategorizing them, so you can pick a paragraph style, one is a short style, this is good for mobile devices, what I have to do is make a list of paragraph names say introduction, this is normally one paragraph on a Desktop or book, but on a mobile device, you want it shorter, so you make a subcategory off of introduction and call it subject, details, conclusion, a very good structure for all categories so this is a pattern, and it makes it easy for the app to format documents that are free flowing, and need to be formatted in many ways.

A book starts off as a project, in my example, it is a dream I had, and I wanted to make technology similar to what I saw in a dream, so I have stuff that will not go into my book, and why Categories are so important to have, as are subcategories, and to go into more details, each has a context category that allows you to say this is a quote for a book, so it is used as a reference to include this quote where you call for it I the book, so the book has a way to link a quote in a book, with some sentence in this project, so I first list a sentence as a quote, and the whole sentence must be that quote, even if the quote is a paragraph, it is one item, but we can name our quotes, and our sentences, this makes referencing them very easy.

A sentence is one whole thought, whereas a Paragraph is a series of sentences, thus a Period has many forms, the one at the end of a sentence, the start of a word like .Net, or the end of a paragraph, and why you have to use special characters in this app.

This project is about managing this project with this app, managing the book, for whatever purpose it has, be it a document to show a proof of concept, so it is a Scientific paper and has a lot of notes, and that will be included in some papers, and not in others, in one book, and maybe you want multiple books out of this same project, it is not limited to one, so go for it.

To get this much flexibility, you created a category that will take care of this case.

I will make a category manager to manage this, the concept is there are types of output, a book, screenplay, stage play, theater play, movie trailer, movie, documentary about the movies, a series based on this movie, and so on. 

Each output category will depend on the formatting, in a screenplay you have characters, so this project will have a character manager, and this manager, will be the character you use in your Game, which is what this Game is all about, you are playing a Game to design the game you want to build because you have to design the environment your book needs to tell the story it needs to, such that the details from this book, are what we use to replace and add to an Unreal Engine or Unity Game Engine, so you can build a game around your story. 

I will write a Book using this App, to show off how it works, because you will have to write the book first, for the app to be able to use it to build all the different formats for output, one being a game.

This app is designed for those who what to document something, maybe their life, a diary, maybe a story they want to write, a product they want to sell, or something for work, or a corporation that wants a tool that does something far more than just play games, but let me put this storyline into a [Wiki]().

### Features

With helmets HUDs are humid due to sweating, requiring a fan on the top, and air holes in the padding of the material to allow air to flow through. 

Glasses will be required, and the displays you use will determine what you need to view this optimally, I guess that you will want to use your normal vision glasses, compared to reading glasses since AR would require them.

The built-in speakers are required to give you the feeling, as such, they are mounted in a way that transfers the sound waves into your head, and not via the open-air conduit, but physical contact, this concept is bone conductive hearing.
There is a built-in sensor pack that can be used to monitor your head orientation in real-time, so the software can detect movement, and there are hand, and feet controllers, that are used by the software to detect if you are moving something, so your hand and legs move when and where you move them, giving you more control over the character’s movement, and you are not required to walk or run, you can use gestures, to move forward to walk, you move both feet as if you are going to walk, and move them 3 times to set the pace, then you can stop, and your character will follow a path, in software, this path is sometimes set, in our software we will use all these new controllers, like hands and feet, to have a gesture library, to make all movements easier to program.

Gesture movements:

•	Idle
•	Walk
•	Run
•	Jump
•	Float-Water
•	Swim-Stroke
•	Swim-Backstroke
•	Swim-Underwater
•	Float-Air
•	Skydive-Flat
•	Skydive-Fast
•	Skydive-Parachute
•	Fly-Idle
•	Fly-Slow
•	Fly-Medium
•	Fly-Fast
•	Fly-Supersonic
•	Fly-Hypersonic




## Hardware

You need a modern CPU and GPU that will run Unreal or Unity Games if you want to run in a Game mode, or VR or AR mode, otherwise, you should be able to run the applications written in Qt or .Net MAUI, so you need to have these applications or SDK installed.

• CPU: Go for Core Count over speed
• System RAM: 32 GB Minimum, recommend 64 GB Minimum
• GPU: 8 GB RAM Minimum, recommend NVIDIA 3000 Series or above

## Reality

Reality is what we sense through visual sight, audible sounds, or touch, just 3 of our main senses, but we have senses for smell, and taste, but those are not functions we can program an environment to cover, we have no smell or taste controls, so our reality is limited to what controls we have now, but we can talk about building these controls because smell and taste are controls, we can add, but how they smell and taste will be up to you.

Not everyone can see or hear or might have an impairment, as I do, so this project is about multiple forms of presentation, a way of saying we have sight, sound, and touch, and that can include braille, so I will try to address how to create VR or AR gear for those with disabilities.

## Notes


I am using an NVIDIA 3060 with 12 GB RAM, on a XEON 10 Core with 20 Threads, and 32 GB RAM.

### Progress

I am working on the app and will get back to you when I am ready to post the code and explain it.


### End of File
