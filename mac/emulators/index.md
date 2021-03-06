---
layout: page
title: Apple Macintosh Emulators
---

*Simon N. Goodwin emulates three generations of 'insanely great' Macs.*

Notwithstanding our enthusiasm for Linux, and the number of Windows systems heating other Future offices, Linux Format magazine and dozens more is designed and laid out on Apple Macintosh systems. This is partly because the Mac excels in publishing and print applications, but it also stems from the strengths of MacOS itself. Uniquely among computer designs, the Macintosh 'Operating System' deserves that title.Notwithstanding our enthusiasm for Linux, and the number of Windows systems heating other Future offices, Linux Format magazine and dozens more is designed and laid out on Apple Macintosh systems. This is partly because the Mac excels in publishing and print applications, but it also stems from the strengths of MacOS itself. Uniquely among computer designs, the Macintosh 'Operating System' deserves that title.

![Basilisk-MacCD.png](/mac/emulators/Basilisk-MacCD.png)

The surprising thing is how little you need to learn in order to use a Mac, and how soon you find yourself discovering and using new things by experiment, rather than scouring MAN pages or online HTML. Rather than the toolkit chaos of Linux, with GTk, KDE, Motif and dozens of window managers offering more options than anyone can grasp, Mac applications build on one elegant toolbox of shared code and concepts, preloaded in ROM. This makes them relatively simple, small, consistent and capable.

This makes a Mac a disappointment for someone who actually likes tweaking configurations, but a boon for those who have a job to do and see the computer as a means to an end, rather than an end in itself. A Mac is an appliance - a tool for work, or play - rather than the time-waster Windows or Unix systems can become, with their endless demands for tweaks and housekeeping. It's worth trying a Mac emulator just to see the subtle but important edge 'conceptual integrity' can give, and how shallow the learning curve for new packages can be.

The good news is that Linux systems can emulate Macs - running that system and the applications that go with it - and Macs can run Linux. There are five Macintosh emulators for Linux: two for the contemporary PowerMac range, two which run original 'Classic Mac' software, and two that emulate the intervening Mac II products. The one with its foot in two camps is Basilisk II, which can run Classic as well as Mac II systems and software.

### Mac history

The usability of modern desktop computers owes more to Xerox, and their followers at Apple, than it does to Unix or Microsoft. Xerox came up with the WIMP concepts - Windows, Icons, Mice and Pointers - at their California PARC research centre in the late 1970s, but failed to make a commercial success of them.

Apple founder Steve Jobs picked up on these ideas and put together a team to build an 'insanely great' computer. His staff selection criteria were eccentric, favouring left-handed acid-droppers, but they learnt from the hard work of the premature Lisa project, and bust their guts in a bid to change the world which few revolutionaries have matched.

The Mac team's effort and influence pervades modern computers, to the point where it's hard to see how another jump so great could be made. Gnome, KDE, BeOS, Win32 and NextStep systems all have more in common with the Mac design than they do with previous computers, with the honourable exception of the stillborn Xerox Star and Apple Lisa systems.

Macintosh concepts have so influenced Windows and Linux, and vice versa, over the last 18 years, that it's no longer obvious what's special about the Mac system. You need to use a Mac, or a good emulator, to realise that the elegance is more than superficial. More than any computers, before or since, the Mac is designed as a system, where the hardware plays a relatively minor part, and applications work together, co-operatively rather than competitively.

![Executor-Credits.png](/mac/emulators/Executor-Credits.png)

As with any complex product developed over decades, there are a few things you need to know to use a Mac, and not all are obvious at first, even if you've grown up with other WIMP environments. This article explains the basics, particularly where emulated Macs differ from Linux or real Mac conventions.

### Beyond Intel

Linux started out as a cure for the misfeatures of IBM and Microsoft, but it runs on more than just Intel systems, and Linux Format is as much for Motorola, Alpha and other processor devotees as it is for those looking to redeem the x86 architecture. Mac emulation is one arena when having a non-Intel processor may be an advantage rather than a handicap.

Design-conscious Apple engineers picked Motorola's 16/32 bit 68000 processor for the original Mac and Lisa systems, dismissing Intel's already creaky x86 and abandoning the eight bit 6502 in earlier Apples. The Classic Mac begat the Macintosh II when it was redesigned for the full 32 bit architecture of 68020, 68030 and 68040 chips Collectively these are known as the 68K range, as chips compatible with Intel's even older 8086 are labelled 'x86' models.

En route from Classic to Mac II Apple added colour, multitasking, virtual memory and expansion slots. It may be surprising how well the Classic models did without those, unless you realise how much trouble they caused primitive rivals. The original thinking was that you don't buy add-ons for your TV or telephone, so why should you for a Mac appliance? The Classic Macs had the same footprint as a desk calculator.

This necessary complication was a mixed blessing. Macs, like most micros, are far more complex and less stable than older computers, though they can do more. Applications on Mac System 6 and System 7 are solid, at least compared with Windows, and far easier to install and with fewer dependencies than most Linux packages.

When the programmer-friendly intricacies of the 68K family began to limit its performance, Apple jumped ship to the PowerPC, a speedy design born out of early IBM RISC research. The PPC instruction set is quite unlike CISC code, so PowerMacs came with an emulator to run the legacy 68K programs, and still do - indeed for years the system relied on that for some less time-critical parts of its own code.

### PowerMacs

It may surprise you that no one has yet released a viable interpreter or dynamic compiler for PPC code. The speed demands of native PowerPC software make this problematic, and the double-penalty of emulating an emulator for 68K compatibility could bring even an Alpha to its knees. The PearPC project, noted at the end of this updated article, accurately emulates a PowerMac on the fastest Intel systems, but it is still too slow for many purposes.

So, if you want to run PowerMac software, you need a computer with a chip from the same family - this could be a PowerMac with LinuxPPC, Yellow Dog, Suse, Debian or similar builds. That might be perverse unless you need Linux open-source, stability and networking more than PowerMac applications.

In fact Apple's latest server OS X is a hybrid of BSD Unix and Mac concepts, and an x86 build of this was announced in 2005, so things are getting more complicated - the best way to run future x86 MacOS software might be via an API redirection system such as WINE, rather than an emulator. For the time being you can do a good job of emulating earlier 68K Mac software on most PC-hosted Linux systems, and PowerPC users have the optimal choice - access to fast current MacOS software, and full-speed Linux via GCC's repectable PowerPC code generation.

The PPC Mac emulators are most likely to be used on a PowerMac, BeBox or accelerated Amiga. While those have elegant native systems of their own, far more new programs are developed for Linux and MacOS. The best of both worlds offered by LinuxPPC with MacOnLinux or SheepShaver may be irresistable, and it's certainly worth knowing about.

### MacOS versions

MacOS has gone through many revisions, some of which are obsolete and not worth emulating. The peak of compatibility and capability was reached during MacOS 6 development. This runs a lot of applications, but only one at a time, though you can switch between several loaded at once. OS 6 lacks multitasking and multimedia extensions which were a focus of 7.x development.

Support for 68000-based Classic Macs stopped at version 7.5.1. Versions 7.5.5 or 7.6 are best-suited to Mac II emulators. Those can use MacOS 8, but that carries a lot of PowerPC baggage, in the form of 'fat binary' files which hold code for both processors. These add bulk but no benefit for 68K macs or emulators.

Fat binaries are still common, and welcome as they allow developers to support both 68K and PPC Mac users, but it's worth running a 'fat stripper' over them to tailor programs for your emulator, especially if you're short of disk space.

![MOL_OSX.gif](/mac/emulators/MOL_OSX.gif)

Even though MacOS 8 piled on PPC code it was not till MacOS 9 that the full power of a PPC system was delivered without emulation. If you want to emulate a Power Mac, 7.5.2 is the first PPC version and 8.1 is the first really solid PPC release.

MacOS 7.5 can be downloaded from Apple's web page, though 7.0.1 is the last genuinely free version. Early MacOS 8 CDs sell for just a few pounds, but you also need a Mac ROM image to make them useful.

The Unix-based MacOS X runs on MacOnLinux and PearPC, but not on the earlier emulators. It's relatively slow, even on the initial Mac hardware expected to run it, and less responsive than Classic MacOS, though more stable than later versions which became increasingly gummed-up by compatibility baggage, lack of memory management to prevent unwanted task interference, and the retrofitting of pre-emptive multi-tasking in place of the original very safe - but design-intensive - co-operating scheduling of processes.

MacOS X can run most programs for earlier versions of MacOS through a virtualisation layer - a bit like MacOnLinux - though it may struggle with hardware-optimised applications, games and device-drivers. The old MacOS runs as a protected process on the Unix/OS X kernel, so even if it falls over, the Unix system should be safe.

### The ROM stuff

The authentic Mac experience demands an 'image' of the Mac Toolbox, the proprietary ROM core of Apple's system. Half the emulators won't even start without this vital file. It's typically 64K or 128K in size for Classic Mac systems, from 256K to 1024K for Mac II emulation, and several megabytes for PowerMacs. This image has to be saved from a real Mac, unless you have loose chips and some way to read them. The ROM is copyright Apple and jealously guarded, so don't expect them to sell it on its own or to be able to download it from any legitimate internet site.

A second hand Mac is the best way to get a legal ROM set. A redundant Mac LC, the low-cost Pizza-box Mac II, should only set you back a few quid. Make sure you get the mouse and keyboard, as these use Apple's proprietary ADB desktop bus. PS/2 devices have similar plugs, but won't work with a Mac. The video connector is a standard D15 rather than the miniature SVGA type, but can drive VGA monitors via a dumb adapter.

Most emulators come with Mac programs to read the ROM, but you'll need a Mac with a SuperDrive, supporting 1.44M MFM HD media, rather than the old PC-incompatible 800K DD GCR format which divides the disk into zones spun and read at varying speeds.

Otherwise, use a serial connection, and terminal software at both ends. Macs have good serial ports, though you'll need to make up a Mini-DIN to D-type cable to link them to a standard D25 or D9 socket. Wiring details are on the CD.

Regular toolbox changes led Apple to include the ROM image as a file on system CDs from OS 8.6 onwards; these are ideal for PPC Mac emulation, as you don't need a ROM file and can install and run entirely from an Apple System CD.

### Special Files

The organisation of files on a Mac is subtly unlike that on other computers. All drives appear in a metafolder called 'Desktop', and deleted files appear in a folder called 'trash', common to all drives, even though they are not actually removed from the original disk till you use the 'empty trash' menu option.

![Basilisk-UnixFiles.gif](/mac/emulators/Basilisk-UnixFiles.gif)

A 'System Folder' on the startup disk contains the loadable part of the operating system such as the kernel and the desktop or 'Finder' application that brings the ROM toolbox to life. Subsidiary folders, akin to sub-directories, hold fonts, preference data, 'control panel' applications to configure the system, and 'extensions' linked in at boot time, rather like Linux loadable modules.

File icons dropped on the system folder are automatically directed to the right sub-folder. Rogue extensions can make booting problematic, but holding the shift key down during startup will prevent any of them loading.

Real Macs have only one mouse button, which eliminates a lot of guesswork, but make up for it with two special meta keys. The Option key, marked with a two-fingered fork, is roughly the equivalent of ALT. The command key, often called, splat, pretzel or clover after its symbol - a box with hoops at each corner - is used for menu short-cuts. These are well-defined, so Splat S saves and Splat Q quits just about any application. If a program gets stuck Splat Option Esc will usually get you out. Splat Shift 3 saves a snapshot of the screen, and so on.

### Media Concepts

Unlike the conventional row-of-bytes approach, Mac files are divided into two parts or 'forks', for 'data' and 'resources' respectively. The 'data' part is usually user-generated - raw samples, graphics or text, for example, while the resource fork tells the Mac how to use it. The Resource fork may contain code, easily configurable interface attributes, or references to other resources.

When you mount a Mac medium in Linux you'll normally only see the data forks. You can tell Linux to expect a Mac directory structure with the switch '-t hfs' in the mount command for /cdrom, /floppy, or whatever.

Lines of text in Mac files are terminated with carriage returns, code 13, rather than the linefeed, code 10, normal in Linux, or the belt-and braces CR/LF pairs of MSDOS, Windows and CP/M. This doesn't bother Emacs, but other utilities like 'less' and 'more' will make a mess of Mac texts unless you filter the control codes.

The Mac HFS Heirarchical File System automatically associates the forks of a file with names of arbitrary length. Obscure characters in names have to be escaped with a backslash or converted to hexadecimal with a colon prefix so that Linux can easily stomach them. MacOS has no command line, so symbols and spaces that would be a pain to type in a shell are common in Macintosh directories.

### Forked files

File transfer protocols are designed for blocks or streams of bytes, rather than Mac forked files, so Mac software for download is almost always packed into files with '.sit' or '.hqx' suffixes. The first stands for Stuffit, a Mac-specific compressed binary file format. The second is equivalent to Base64 or UUencoding, and renders binary as printable characters that can safely be emailed or sent over links designed for text.

The key to unpacking these formats is the unrestricted Shareware application 'Stuffit Expander', which was on the LXF CD in a floppy disk image and is bundled in the Executor demo package. Like most Mac applications, this springs to life as soon as you drop a suitable file on its icon. In fact most data files run the relevant application as soon as you double-click on them, but this is not possible for a file without a resource fork. You may find '.sit' files on Mac media. These are self-extracting archives and unpack themselves automatically when you double-click on them.

### vMac

vMac emulates a 1985 vintage Macintosh Plus. The display is black and white at the Classic Mac's meagre 512 by 342 resolution. The emulated memory size can be 1, 2 or 4M. The default is one megabyte but you need more to run MacOS 7. You'll also need an old system ROM - vMac was happy with a 128K ROM image but rejected the 256K and 512K ROMs from my Mac LC and Mac FX.

![vmac-system.png](/mac/emulators/vmac-system.png)

vMac supports three drives by direct reference to '/dev/fd' Linux devices, or equivalent 1.4M disk images. In theory it will work with larger files, or whole partitions, treating them as big floppies, but the brief documentation barely hints at how you might do this.

VMac works but it's hard to find programs to run on it. The lack of colour, sound and hard disk support make it authentic, but more of a toy than a useful environment for work or play.

### Basilisk II

Basilisk II is the latest in a series of Mac emulators by Christian Bauer, who also wrote Frodo, the C64 emulator reviewed in LXF15 and Part 3 of this series. Basilisk runs natively on Linux 68K and Amiga systems, and uses the UAE emulation engine on BeOS, NT4 and several flavours of Unix.

Basilisk can emulate a Mac II or any platform, or a Classic Mac as long as you're using the emulating core. The emulation relies on programs calling the operating system. Unlike vMac or Bauer's earlier ShapeShifter, it does not attempt to emulate Mac hardware; instead it provides replacement drivers for the new host.

This approach is more flexible and potentially more efficient, but it does limit compatibility with optimised programs that access drives and displays directly. Real Macs can change their display resolution and colour depth on the fly, but Basilisk only delivers the screen-size selected when you start it up, in an X window or full-screen using the XFree86 DGA extension, and only supports the colour depth of the underlying X display. You must restart the emulator, or even X, to run programs that expect a different resolution or colour depth for their pre-computed graphics.

![Basilisk-CD+QT1.gif](/mac/emulators/Basilisk-CD+QT1.gif)

Basilisk II is neatly written, mostly in C++, and intelligently documented, with a view to portability and extendability. Most of the device drivers are written in two layers, one logical and Mac-related, the other tailoring that to each specific host. It supports direct CD access, for audio as well as data, and even handles disk changes like a real Mac, opening the drive when you drop a CD icon on the trashcan, and popping up the icon automatically when a fresh CD is inserted.

Floppy handling is not so elegant, in the absence of drives with software locks and powered ejection, but no problem if you're used to Linux. Instead of 'mount' and 'umount' commands you must press CTRL F1 to tell Basilisk to look for a changed disk, and remember to drop the icon on the trashcan before you eject it manually.

Serial ports work fine; Macs never bothered with parallel ones, and real Mac serial ports outrun most hosts even today. Basilisk can also use Ethernet as long as you're using a later, Mac II ROM. This part is clever, and thankfully well-documented.

Two approaches are possible. You can dedicate a real Ethernet card to the emulator, so its 'sheep_net' driver talks directly to 'eth0' or a similar device. The emulated Mac can then share proprietary Mac protocols like Appletalk, as well as TCP/IP, with any other machine on the network.

The alternative allows the Mac to use Linux network routing, but requires a host kernel compiled and configured to support the 'ethertap' device. Basilisk then talks TCP/IP to the 'tap0' and can share internet and other connections routed through Linux, but Mac to Mac communication then requires extra TCP/IP layers at both ends.

![Basilisk-Settings.png](/mac/emulators/Basilisk-Settings.png)

We tested two versions of Basilisk for Linux - both at version 0.9. One is a conventional interpreter, and runs on any processor supported by GCC, though as with all interpreting emulators the overhead is large - typically 50 host instructions for every one emulated. The other is a dynamic cross-compiler, from 68K to x86 code, again derived from the UAE Unix Amiga Emulator project.

The experimental compiling emulator needs more memory to store the x86 code it generates as it encounters and translates blocks of original 68K instructions. At least 256K is needed. If you can afford to allocate megabytes you'll probably find the emulation faster because it can spend more time running pre-translated code, and less re-compiling sections.

This depends on the size of the program. When you're running tiny benchmark loops, a small translation buffer will suffice. Large compiled applications demand more, and the translations and associated tables are typically several times bigger than the code they replace.

If the program you run is self-modifying, you might be better off with the interpreter, as programs that change their own code will force the compiler to churn to the extent that extra book-keeping may be counterproductive. Self-modifying code is sometimes used to save time and space in old 68000 programs, but it's rare on later processors because it interacts adversely with the CPU cache, even for native code.

For most purposes, the trade-off leaves the compiler a long way ahead. It's far more complicated internally, so bugs are more likely, but I found it solid once I got it configured.

The compiler will currently only emulate a Mac with a 68040 processor. If you select any other configuration in the initial startup screens Basilisk will open a window and then hang up. The ROM version may also be an issue - one megabyte Quadra ROMs were designed for 68040s. Smaller Mac II ROMs don't fully support the extended architecture and caches.

### Executor

Executor takes a fascinating approach to emulation. It can run a lot of Mac II software without using a Mac ROM or any Apple system files. It's a commercial product, but the demo version was unrestricted apart from a 30 day timeout and some missing keyboard short-cuts. This makes it worth a whirl for anyone with Linux on an x86, and access to Mac applications. Early in 2006 it was freely available, though only via a slow FTP site, with the following notice:

*The key expires at the end of December, 2006. By that time, all of ARDI's software technology will probably either be sold or released under an Open Source license. There is no technical support available for Executor.*

![Executor-Logo.png](/mac/emulators/Executor-Logo.png)

Executor started out as a research project, aiming to make a fast emulator to run 68040 code on Intel architectures. Later developers ARDI added a replacement for the Mac system software and hardware drivers, turning the engine into a viable platform for Windows and Unix devotees. In 2005, with Apple's announcement of a gradual shift to x86 processors, ARDI stopped selling Executor and made it an unsupported free download available on their webpage, via BitTorrent.

The CPU emulation core is fast but not quite state-of-the-art. On a 500 MHz AMD K6-2 it runs processor-bound application code almost six times faster than the 32 bit 68030 in a Mac LC3. This is impressive - more than a match for a real Mac II - although the compiling Basilisk is more than twice as fast again.

Yet Executor gains extra speed because the system toolbox and desktop routines are running natively on the x86, with no translation at all. Since this code can be compiled and optimised en masse, it's much tighter and faster than any Just In Time compiler could manage.

But that advantage is also a snag, because it freezes Executor a decade behind the times. Executor emulates a Mac II with System 6.0.7, missing out on the multitasking and multimedia extensions added in System 7. It makes no use of memory management or floating point hardware. The pre-cast monolithic replacement kernel is much less extensible than a real Mac system, so you can't bring it up to date by adding extensions and control panels from Apple or other developers.

ARDI's replacement for Apple's Finder looks superficially similar, with the bonus of toolbar buttons across the top, but it lacks drag and drop and other ergonomic icon management features of the real thing. As a directory navigator and program launcher it's OK, but it is inferior to Apple's Finder as a way of managing files, and the swapping and multi-tasking features of System 7's Multifinder are sorely missed.

![Executor-SYNDICATE0.png](/mac/emulators/Executor-SYNDICATE0.png)

It does allow direct access to the host filesystem, so you can use it to explore Linux as well as Mac directories. Basilisk can do this too, but only with MacOS 7.5.5 or later. Genuine Mac CDs and floppies work well, but there's no support for modem connections, so you can forget running dialup communications software on Executor. Apple's QuickTime animation engine, often used by CD packages, is not supported. Elsewhere, the story is mixed.

Users report good results with impressive programs such as Adobe Illustrator 5.5 and PhotoShop 4, and Claris Works up to version 3. Later versions are more likely to show problems, typically because they expect system 7 features. AppleWorks, Graphic Converter, ColorIt, FileMaker, Electronics Breadboard and Ultimate Solitaire were all quite usable under the emulation.

Mac Lemmings look and sound good, apart from jerky scrolling, in Executor. The Mac's definitive 3D shooter Marathon ran, but the colours in the main window were completely wrong, making the game unplayable. Marathon seems to take short cuts in its display output, as the system-strict emulator Basilisk II failed to update parts of the game screen and soon fell over completely. Executor is not as strict as Basilisk, but still works best on applications designed for maximum inter-Mac compatibility.

This highlights a general problem with programs, especially games, that bypass the MacOS. Emulators can hardly be expected to mimic the hardware exactly when the system-friendly approach works so well for most other applications.

### SheepShaver

SheepShaver is a Mac emulator for Linux systems running Power PC processors. Originally this was commercial software for BeOS, after Christian Bauer moved to that platform from the Amiga.

![SheepShaver_linux1.png](/mac/emulators/SheepShaver_linux1.png)

BeOS was something of a heroic failure, a new system written in C++ by ex-Apple engineers. Originally it ran on custom PPC computers, known as BeBoxes, but it has since been ported to x86. Alas BeOS failed to find a commercial niche, but it has already influenced LinuxPPC and it ain't dead yet.

The name SheepShaver is a twisted reference to ShapeShifter, the celebrated Amiga-hosted Mac emulator from the same author. It runs Mac OS versions from 7.5.2 to 8.6, and comes with a utility to extract a copy of the ROM image from a real Apple PowerMac, though you don't need this if you've got a MacOS 8.6 or later CD. Getting the right ROM is the biggest challenge if you'd like to run SheepShaver. The source supports 'Old World' (pre iMac) ROMs from some TNT, Alchemy, Zanzibar, Gazelle and Gossamer Apple motherboards, but not all are suitable. A 'New World' ROM image from a MacOS 9.0 iMac update download enabled LXF to get MacOS 9.0 running, in their August 2005 retest.

SheepShaver needs no CPU emulation, as it runs directly on the Power PC, so it can do processor-intensive work as fast as a real Mac with the same CPU. It can run on Amigas with PPC accelerators as well as BeBoxes, PowerMacs and generic PPC Linux systems.

### MacOnLinux

MacOnLinux is a Power Mac emulator written for the PPC versions of Linux from Yellow Dog, Suse and others - though not MkLinux. MacOnLinux is the brainchild of Samuel Rydh, a mathematical physics postgraduate at Stockholm University.

![MacOnLinuxLogo.gif](/mac/emulators/MacOnLinuxLogo.gif)

At the time of our initial test MacOnLinux could run MacOS versions from 7.5.2 to 9.0.4, along with the file "Mac OS ROM" from the System Folder of a MacOS 8.6 or later CD, removing the need to copy a real PowerMac ROM. This makes installation trivial - install the RPM, copy the ROM, and your next command can set the Mac running. Since then MacOnLinux has been sporadicaly updated and it has since been persuaded to runs the Unix-based MacOS 10.2.8, designed for Apple G3 and G4 PowerMac systems.

![MacOnLinuxRunsOS9.gif](/mac/emulators/MacOnLinuxRunsOS9.gif)

MacOnLinux can use IDE and SCSI block devices, and either USB or ADB mice and keyboards. It can handle multiple Ethernet interfaces, and uses the Power PC memory management unit to optimise screen updates so that only the pages of the frame buffer that have actually been changed need to be updated on the X display.

Unlike the strictly system-legal approach of SheepShaver and Basilisk, MacOnLinux emulation is low-level enough to allow you to run a second copy of Linux inside the Mac emulation. This is as close as Linux gets to a PPC version of VMWare, and allows development in a sandbox or with hidden or redirected peripheral access, which may be useful for driver development and testing. MacOnLinux can also save and restore entire sessions, which are rather like 8bit emulator snapshots but a lot bigger, removing the need to reboot the emulated system each time you fire it up.

MacOnLinux requires a 2.2 Power PC Linux kernel and a patch for compatibility with PPC603 processors. It runs happily on the original PPC601, midrange 604, and later 750 and 7400 chips, also known as G3 and G4 processors. At the time of our review it did not yet support removable media, RS232 serial ports, or generic USB and SCSI devices such as scanners, but support for these was in the works.

Devices tend to be slower than on a real Power Mac, as hardware display acceleration is not available and file access is synchronous - the emulator waits for data to be transferred, rather than use async routines which would let it get on with other tasks in the meantime. Audio input is not supported and output is subject to a lag of up to half a second.

Despite some gaps, MacOnLinux is an impressive project, and makes ingenious use of the PPC hardware. What's more it's open source under the GPL, so further development is free and assured.

### PearPC

Since our original article was published Mac zealot Sebastial Biellas has come up with PearPC, a software emulation of the PowerPC in later Apple Macs which runs on typical x86-based Linux hardware. A review of this appeared in LXF69, describing it as 'still a little light on features' - it will run MacOS X but not MacOS 9, prefers hard files to real Mac hard disc images - though it can read HFS format CDs - and integrates the emulated Mac with the Linux host network by convincingly impersonating a RealTec PCI Ethernet controller.

PearPC uses a just-in-time compiler to translate PowerPC machine code into x86 code on the fly. You'd need a very fast PC - possibly one that has not been made yet - to run Mac code at the speed of a minimum spec OS X system, such as a late 90s G3 PowerMac. Nonetheless, it's already just about usable for some applications, and a most impressive feat of programming.

The future of PearPC might seem uncertain, given Apple boss Steve Jobs's summer 2005 announcement that future Mac systems would run on Intel x86 rather than Motorola 68K or PowerPC hardware. However the need for PPC emulation will remain - much as a 68K emulator remains in current versions of MacOS, to run all the old Mac software which people have often paid for or got used to and are unwilling to give up. Now IBM are focusing PowerPC hardware on servers and next-generation game systems. The PPC featured in the 3DO M2 game console early in its development (PPC602), and updates power the Nintendo GameCube as well as Sony PS3 and Microsoft Xbox 360 consoles. The demand for fast PowerPC emulation is not going to go away, so the PearPC SourceForge project is worth a look whether you're interested in the architecture, Mac software, or an emulation enthusiast keen to scale new heights.

### Mace

Mace is a project aiming to do for MacOS what WINE struggles to do for Windows - to run current applications without the need for proprietary system software they were coded to rely upon. So far there's little evidence that the protagonists understand the challenge they've taken on, but Mace deserves a mention as potentially one to watch if it gets some heavyweight coders on board, and the files on the MaceHQ site were updated as recently as June 2005 so there's life in the project yet, despite slow progress, and initial work and related tools can be downloaded under the LGPL.
