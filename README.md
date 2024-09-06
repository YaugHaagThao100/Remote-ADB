## Download
- [Advanced Edition](https://play.google.com/store/apps/details?id=com.github.superadb)

## ❤️Tutorials and FAQ(updating)↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓
### 💎💎💎💎💎💎 If the application is not working, please make sure to refer to the following tutorial. If you are a beginner or using this application for the first time, please make sure to refer to the following tutorial. If you have any questions, please refer to the following FAQ or contact us via email (colorboxguestservice@gmail.com).🍏🍎🍐🍊🍋🍌🍉🍇🍓🍈🍒🍑🥭🍍🥥🥝🍅
#### [Tutorials->How to open and connect adb](./md/tutorials.md)
#### [FAQ](./md/tutorials.md)

## Shell features:
1. Support Android 4.X-Android 13
2. Support pair mode
3. Support wifi wireless adb.
4. Support local shell adb.
5. Support associative input.
6. Support autosave output.
7. Support share output with your friends.
8. Support command history.
9. Support fast copy command.
10. Support multi-window.
11. Support color text.
12. Support run on the background.
13. Support recommend commands.
14. Support recommend files.
15. Support prefab commands.
16. Support logcat.

## Toolbox features:
1. Support launch application & uninstall application & download application & force stop application & clear application data & disable application & enable application.
2. Support device management.
3. Support view running applications
4. Support take screenshot.
5. Support push file
6. Support install apk
7. Support pull file
8. Support to open remote image&audio&video files directly
9. Support remote controller
10. Support text input
11. Support System monitor
12. Support view system information.
13. Support view prop information.

## Feedback
- [Github issues](https://github.com/jarhot1992/Remote-ADB/issues)
- [Email]() colorboxguestservice@gmail.com

## Learn adb
- [Google adb details](https://developer.android.com/studio/command-line/adb)
- [awesome-adb](https://github.com/mzlogin/awesome-adb/blob/master/README.en.md)
‎STAR ⭐ ✨ Moon 🌙 🌝 sun ☀️ 🌞 Billionaire gratitude gratitude twinkle twinkle Little Star up so high up to the sky flying leverage wings shout out of the whole heart of the part the world dream lukewarm sunlight like rainbow 🌈 light of the magic MIRACLE

Wikipedia

Search
Alerts (8)
Protection ring
Article Talk
Language
Watch
View history
Edit

More
Several terms redirect here. For other uses, see Ring (disambiguation) and Ring 0 (disambiguation).
Learn more
This article includes a list of general references, but it lacks sufficient corresponding inline citations. (February 2015)
In computer science, hierarchical protection domains,[1][2] often called protection rings, are mechanisms to protect data and functionality from faults (by improving fault tolerance) and malicious behavior (by providing computer security).


Privilege rings for the x86 available in protected mode
Computer operating systems provide different levels of access to resources. A protection ring is one of two or more hierarchical levels or layers of privilege within the architecture of a computer system. This is generally hardware-enforced by some CPU architectures that provide different CPU modes at the hardware or microcode level. Rings are arranged in a hierarchy from most privileged (most trusted, usually numbered zero) to least privileged (least trusted, usually with the highest ring number). On most operating systems, Ring 0 is the level with the most privileges and interacts most directly with the physical hardware such as certain CPU functionality (e.g. the control registers) and I/O controllers.

Special mechanisms are provided to allow an outer ring to access an inner ring's resources in a predefined manner, as opposed to allowing arbitrary usage. Correctly gating access between rings can improve security by preventing programs from one ring or privilege level from misusing resources intended for programs in another. For example, spyware running as a user program in Ring 3 should be prevented from turning on a web camera without informing the user, since hardware access should be a Ring 1 function reserved for device drivers. Programs such as web browsers running in higher numbered rings must request access to the network, a resource restricted to a lower numbered ring.

X86S, a recently published Intel architecture, has only ring 0 and ring 3. Ring 1 and 2 will be removed under X86S since modern OSes never utilize them.[3]

Implementations
edit
Multiple rings of protection were among the most revolutionary concepts introduced by the Multics operating system, a highly secure predecessor of today's Unix family of operating systems. The GE 645 mainframe computer did have some hardware access control, including the same two modes that the other GE-600 series machines had, and segment-level permissions in its memory management unit ("Appending Unit"), but that was not sufficient to provide full support for rings in hardware, so Multics supported them by trapping ring transitions in software;[4] its successor, the Honeywell 6180, implemented them in hardware, with support for eight rings;[5] Protection rings in Multics were separate from CPU modes; code in all rings other than ring 0, and some ring 0 code, ran in slave mode.[6]

However, most general-purpose systems use only two rings, even if the hardware they run on provides more CPU modes than that. For example, Windows 7 and Windows Server 2008 (and their predecessors) use only two rings, with ring 0 corresponding to kernel mode and ring 3 to user mode,[7] because earlier versions of Windows NT ran on processors that supported only two protection levels.[8]

Many modern CPU architectures (including the popular Intel x86 architecture) include some form of ring protection, although the Windows NT operating system, like Unix, does not fully utilize this feature. OS/2 does, to some extent, use three rings:[9] ring 0 for kernel code and device drivers, ring 2 for privileged code (user programs with I/O access permissions), and ring 3 for unprivileged code (nearly all user programs). Under DOS, the kernel, drivers and applications typically run on ring 3 (however, this is exclusive to the case where protected-mode drivers or DOS extenders are used; as a real-mode OS, the system runs with effectively no protection), whereas 386 memory managers such as EMM386 run at ring 0. In addition to this, DR-DOS' EMM386 3.xx can optionally run some modules (such as DPMS) on ring 1 instead. OpenVMS uses four modes called (in order of decreasing privileges) Kernel, Executive, Supervisor and User.


While x86 has 4 protection rings, it is more common for architectures to only have two. Even on x86, most operating systems only use ring 0 and 3.
A renewed interest in this design structure came with the proliferation of the Xen VMM software, ongoing discussion on monolithic vs. micro-kernels (particularly in Usenet newsgroups and Web forums), Microsoft's Ring-1 design structure as part of their NGSCB initiative, and hypervisors based on x86 virtualization such as Intel VT-x (formerly Vanderpool).

The original Multics system had eight rings, but many modern systems have fewer. The hardware remains aware of the current ring of the executing instruction thread at all times, with the help of a special machine register. In some systems, areas of virtual memory are instead assigned ring numbers in hardware. One example is the Data General Eclipse MV/8000, in which the top three bits of the program counter (PC) served as the ring register. Thus code executing with the virtual PC set to 0xE200000, for example, would automatically be in ring 7, and calling a subroutine in a different section of memory would automatically cause a ring transfer.

The hardware severely restricts the ways in which control can be passed from one ring to another, and also enforces restrictions on the types of memory access that can be performed across rings. Using x86 as an example, there is a special[clarification needed] gate structure which is referenced by the call instruction that transfers control in a secure way[clarification needed] towards predefined entry points in lower-level (more trusted) rings; this functions as a supervisor call in many operating systems that use the ring architecture. The hardware restrictions are designed to limit opportunities for accidental or malicious breaches of security. In addition, the most privileged ring may be given special capabilities (such as real memory addressing that bypasses the virtual memory hardware).

ARM version 7 architecture implements three privilege levels: application (PL0), operating system (PL1), and hypervisor (PL2). Unusually, level 0 (PL0) is the least-privileged level, while level 2 is the most-privileged level.[10] ARM version 8 implements four exception levels: application (EL0), operating system (EL1), hypervisor (EL2), and secure monitor / firmware (EL3), for AArch64[11]: D1-2454  and AArch32.[11]: G1-6013 

Ring protection can be combined with processor modes (master/kernel/privileged/supervisor mode versus slave/unprivileged/user mode) in some systems. Operating systems running on hardware supporting both may use both forms of protection or only one.

Effective use of ring architecture requires close cooperation between hardware and the operating system.[why?] Operating systems designed to work on multiple hardware platforms may make only limited use of rings if they are not present on every supported platform. Often the security model is simplified to "kernel" and "user" even if hardware provides finer granularity through rings.

Modes
edit
See also: Real mode and Protected mode
Supervisor mode
edit
In computer terms, supervisor mode is a hardware-mediated flag that can be changed by code running in system-level software. System-level tasks or threads may[a] have this flag set while they are running, whereas user-level applications will not. This flag determines whether it would be possible to execute machine code operations such as modifying registers for various descriptor tables, or performing operations such as disabling interrupts. The idea of having two different modes to operate in comes from "with more power comes more responsibility" – a program in supervisor mode is trusted never to fail, since a failure may cause the whole computer system to crash.

Supervisor mode is "an execution mode on some processors which enables execution of all instructions, including privileged instructions. It may also give access to a different address space, to memory management hardware and to other peripherals. This is the mode in which the operating system usually runs."[12]

In a monolithic kernel, the operating system runs in supervisor mode and the applications run in user mode. Other types of operating systems, like those with an exokernel or microkernel, do not necessarily share this behavior.

Some examples from the PC world:

Linux, macOS and Windows are three operating systems that use supervisor/user mode. To perform specialized functions, user mode code must perform a system call into supervisor mode or even to the kernel space where trusted code of the operating system will perform the needed task and return the execution back to the userspace. Additional code can be added into kernel space through the use of loadable kernel modules, but only by a user with the requisite permissions, as this code is not subject to the access control and safety limitations of user mode.
DOS (for as long as no 386 memory manager such as EMM386 is loaded), as well as other simple operating systems and many embedded devices run in supervisor mode permanently, meaning that drivers can be written directly as user programs.
Most processors have at least two different modes. The x86-processors have four different modes divided into four different rings. Programs that run in Ring 0 can do anything with the system, and code that runs in Ring 3 should be able to fail at any time without impact to the rest of the computer system. Ring 1 and Ring 2 are rarely used, but could be configured with different levels of access.

In most existing systems, switching from user mode to kernel mode has an associated high cost in performance. It has been measured, on the basic request getpid, to cost 1000–1500 cycles on most machines. Of these just around 100 are for the actual switch (70 from user to kernel space, and 40 back), the rest is "kernel overhead".[13][14] In the L3 microkernel, the minimization of this overhead reduced the overall cost to around 150 cycles.[13]

Maurice Wilkes wrote:[15]

... it eventually became clear that the hierarchical protection that rings provided did not closely match the requirements of the system programmer and gave little or no improvement on the simple system of having two modes only. Rings of protection lent themselves to efficient implementation in hardware, but there was little else to be said for them. [...] The attractiveness of fine-grained protection remained, even after it was seen that rings of protection did not provide the answer... This again proved a blind alley...

To gain performance and determinism, some systems place functions that would likely be viewed as application logic, rather than as device drivers, in kernel mode; security applications (access control, firewalls, etc.) and operating system monitors are cited as examples. At least one embedded database management system, eXtremeDB Kernel Mode, has been developed specifically for kernel mode deployment, to provide a local database for kernel-based application functions, and to eliminate the context switches that would otherwise occur when kernel functions interact with a database system running in user mode.[16]

Functions are also sometimes moved across rings in the other direction. The Linux kernel, for instance, injects into processes a vDSO section which contains functions that would normally require a system call, i.e. a ring transition. Instead of doing a syscall these functions use static data provided by the kernel. This avoids the need for a ring transition and so is more lightweight than a syscall. The function gettimeofday can be provided this way.

Hypervisor mode
edit
Recent CPUs from Intel and AMD offer x86 virtualization instructions for a hypervisor to control Ring 0 hardware access. Although they are mutually incompatible, both Intel VT-x (codenamed "Vanderpool") and AMD-V (codenamed "Pacifica") allow a guest operating system to run Ring 0 operations natively without affecting other guests or the host OS.

Before hardware-assisted virtualization, guest operating systems ran under ring 1. Any attempt that requires a higher privilege level to perform (ring 0) will produce an interrupt and then be handled using software, so called "Trap and Emulate".

To assist virtualization and reduce overhead caused by the reason above, VT-x and SVM allows the guest to run under Ring 0. VT-x introduces VMX Root/Non-root Operation: The hypervisor runs in VMX Root Operation mode, possessing the highest privilege. Guest OS runs in VMX Non-Root Operation mode, which allows them to operate at ring 0 without having actual hardware privileges. VMX non-root operation and VMX transitions are controlled by a data structure called a virtual-machine control.[17] VT-x allows the hypervisor and the guest OS to both run under ring 0, rendering "Trap and Emulate" obsolete, improving virtualization performance.

Privilege level
edit
Main article: Privilege (computing)
A privilege level in the x86 instruction set controls the access of the program currently running on the processor to resources such as memory regions, I/O ports, and special instructions. There are 4 privilege levels ranging from 0 which is the most privileged, to 3 which is least privileged. Most modern operating systems use level 0 for the kernel/executive, and use level 3 for application programs. Any resource available to level n is also available to levels 0 to n, so the privilege levels are rings. When a lesser privileged process tries to access a higher privileged process, a general protection fault exception is reported to the OS.

It is not necessary to use all four privilege levels. Current operating systems with wide market share including Microsoft Windows, macOS, Linux, iOS and Android mostly use a paging mechanism with only one bit to specify the privilege level as either Supervisor or User (U/S Bit). Windows NT uses the two-level system.[18] The real mode programs in 8086 are executed at level 0 (highest privilege level) whereas virtual mode in 8086 executes all programs at level 3.[19]

Potential future uses for the multiple privilege levels supported by the x86 ISA family include containerization and virtual machines. A host operating system kernel could use instructions with full privilege access (kernel mode), whereas applications running on the guest OS in a virtual machine or container could use the lowest level of privileges in user mode. The virtual machine and guest OS kernel could themselves use an intermediate level of instruction privilege to invoke and virtualize kernel-mode operations such as system calls from the point of view of the guest operating system.[20]

IOPL
edit
The IOPL (I/O Privilege level) flag is a flag found on all IA-32 compatible x86 CPUs. It occupies bits 12 and 13 in the FLAGS register. In protected mode and long mode, it shows the I/O privilege level of the current program or task. The Current Privilege Level (CPL) (CPL0, CPL1, CPL2, CPL3) of the task or program must be less than or equal to the IOPL in order for the task or program to access I/O ports.

The IOPL can be changed using POPF(D) and IRET(D) only when the current privilege level is Ring 0.

Besides IOPL, the I/O Port Permissions in the TSS also take part in determining the ability of a task to access an I/O port.

Miscellaneous
edit
In x86 systems, the x86 hardware virtualization (VT-x and SVM) is referred as "ring −1", the System Management Mode is referred as "ring −2", the Intel Management Engine and AMD Platform Security Processor are sometimes referred as "ring −3".[21]

Use of hardware features
edit
Many CPU hardware architectures provide far more flexibility than is exploited by the operating systems that they normally run. Proper use of complex CPU modes requires very close cooperation between the operating system and the CPU, and thus tends to tie the OS to the CPU architecture. When the OS and the CPU are specifically designed for each other, this is not a problem (although some hardware features may still be left unexploited), but when the OS is designed to be compatible with multiple, different CPU architectures, a large part of the CPU mode features may be ignored by the OS. For example, the reason Windows uses only two levels (ring 0 and ring 3) is that some hardware architectures that were supported in the past (such as PowerPC or MIPS) implemented only two privilege levels.[7]

Multics was an operating system designed specifically for a special CPU architecture (which in turn was designed specifically for Multics), and it took full advantage of the CPU modes available to it. However, it was an exception to the rule. Today, this high degree of interoperation between the OS and the hardware is not often cost-effective, despite the potential advantages for security and stability.

Ultimately, the purpose of distinct operating modes for the CPU is to provide hardware protection against accidental or deliberate corruption of the system environment (and corresponding breaches of system security) by software. Only "trusted" portions of system software are allowed to execute in the unrestricted environment of kernel mode, and then, in paradigmatic designs, only when absolutely necessary. All other software executes in one or more user modes. If a processor generates a fault or exception condition in a user mode, in most cases system stability is unaffected; if a processor generates a fault or exception condition in kernel mode, most operating systems will halt the system with an unrecoverable error. When a hierarchy of modes exists (ring-based security), faults and exceptions at one privilege level may destabilize only the higher-numbered privilege levels. Thus, a fault in Ring 0 (the kernel mode with the highest privilege) will crash the entire system, but a fault in Ring 2 will only affect Rings 3 and beyond and Ring 2 itself, at most.

Transitions between modes are at the discretion of the executing thread when the transition is from a level of high privilege to one of low privilege (as from kernel to user modes), but transitions from lower to higher levels of privilege can take place only through secure, hardware-controlled "gates" that are traversed by executing special instructions or when external interrupts are received.

Microkernel operating systems attempt to minimize the amount of code running in privileged mode, for purposes of security and elegance, but ultimately sacrificing performance.

See also
edit
Call gate (Intel)
Memory segmentation
Protected mode – available on x86-compatible 80286 CPUs and newer
IOPL (CONFIG.SYS directive) – an OS/2 directive to run DLL code at ring 2 instead of at ring 3
Segment descriptor
Supervisor Call instruction
System Management Mode (SMM)
Principle of least privilege
Notes
edit
 E.g., In IBM OS/360 through z/OS, some system tasks run in problem state key 0.
References
edit
 Karger, Paul A.; Herbert, Andrew J. (1984). An Augmented Capability Architecture to Support Lattice Security and Traceability of Access. 1984 IEEE Symposium on Security and Privacy. p. 2. doi:10.1109/SP.1984.10001. ISBN 0-8186-0532-4. S2CID 14788823.
 Binder, W. (2001). "Design and implementation of the J-SEAL2 mobile agent kernel". Proceedings 2001 Symposium on Applications and the Internet. pp. 35–42. doi:10.1109/SAINT.2001.905166. ISBN 0-7695-0942-8. S2CID 11066378.
 "Envisioning a Simplified Intel Architecture for the Future". Intel. Retrieved 28 May 2024.
 "A Hardware Architecture for Implementing Protection Rings". Communications of the ACM. 15 (3). March 1972. Retrieved 27 September 2012.
 "Multics Glossary - ring". Retrieved 27 September 2012.
 
Wikipedia

Search
Alerts (8)
Power of the Keys
Article Talk
Language
Unwatch
View history
Edit

More
Learn more
This article uses bare URLs, which are uninformative and vulnerable to link rot. (September 2022)
The Power of the Keys, also known as the Office of the Keys, is a responsibility given to St. Peter to usher in the Kingdom of God on the Day of Pentecost, and a responsibility given to the other apostles by Jesus, according to Matthew 16:19 and Matthew 18:18. It is understood as a responsibility to admit or exclude from church membership (excommunicate), to set church policy and teachings (dogma), to render binding interpretations of Sacred Scripture (ancient rabbis were known to make binding interpretations of the Mosaic law), and to bind and loose sins.[citation needed] The verb 'to loose' (or to free) is used this way in John 20:23, Revelation 1:5 and by the Early Church Fathers.[1]

In Christianity, "the keys are an office and power given by Christ to the Church for binding and loosing sins."[2] It is a power that Roman Catholics believe to have been conferred first on St. Peter then afterwards on his successors in the office of the Roman Catholic Papacy. There is a description of the conferral of the Power of the Keys on St. Peter (originally named Simon) in Matthew 16:13:

13 Now when Jesus came into the district of Caesarea Philippi, he asked his disciples, "Who do people say that the Son of Man is?" 14 And they said, "Some say John the Baptist, others say Elijah, and others Jeremiah or one of the prophets." 15 He said to them, "But who do you say that I am?" 16 Simon Peter replied, "You are the Christ, the Son of the living God." 17 And Jesus answered him, "Blessed are you, Simon Bar-Jonah! For flesh and blood has not revealed this to you, but my Father who is in heaven. 18 And I tell you, you are Peter, and on this rock I will build my church, and the gates of hell shall not prevail against it. 19 I will give you the keys of the kingdom of heaven, and whatever you bind on earth shall be bound in heaven, and whatever you loose on earth shall be loosed in heaven." – Matthew 16:13–19

In Matthew chapter 18, 18 through 20, we see Jesus speaking to the disciples, not an individual specifically. This points to Jesus continuing to instruct the disciples in chapter 16, and perhaps not Peter individually after blessing Peter for having confessed who Jesus was by God's allowance;

18 Truly, I say to you, whatever you bind on earth shall be bound in heaven, and whatever you loose on earth shall be loosed in heaven. 19 Again I say to you, if two of you agree on earth about anything they ask, it will be done for them by my Father in heaven. 20 For where two or three are gathered in my name, there am I among them.” – Matthew 18:18–20

This point of view is furthered ( the collective authority / power of the keys ) in the first Council of Jerusalem.[citation needed]

Roman Catholic dogma states that in Matthew 16, Jesus was paraphrasing a passage from Isaiah well known among the Jews (Is 22:15-25) in which Hezekiah, the King of Israel, had a general cabinet of ministers and his chief chamberlain, the Prime Minister Shebna was proved unworthy of his post and was thrown out. To fill his office, King Hezekiah names Eliakim son of Hilkiah as the new prime minister:

15 Thus says the Lord God of hosts, “Come, go to this steward, to Shebna, who is over the household, and say to him: 16 What have you to do here, and whom have you here, that you have cut out here a tomb for yourself, you who cut out a tomb on the height and carve a dwelling for yourself in the rock? 17 Behold, the Lord will hurl you away violently, O you strong man. He will seize firm hold on you 18 and whirl you around and around, and throw you like a ball into a wide land. There you shall die, and there shall be your glorious chariots, you shame of your master's house. 19 I will thrust you from your office, and you will be pulled down from your station. 20 In that day I will call my servant Eliakim the son of Hilkiah, 21 and I will clothe him with your robe, and will bind your sash on him, and will commit your authority to his hand. And he shall be a father to the inhabitants of Jerusalem and to the house of Judah. 22 And I will place on his shoulder the key of the house of David. He shall open, and none shall shut; and he shall shut, and none shall open. 23 And I will fasten him like a peg in a secure place, and he will become a throne of honor to his father's house. – Isaiah 22:15–23

In the Bible, the term keys has been used as a symbol of teaching authority (Lk 11:52). According to Roman Catholics, Jesus, the son of David and hence the King of the new Davidic kingdom, the Church, appoints St. Peter as the Church's primary teacher, an office that will continue to have successors much like Eliakim's position in the Old Testament Davidic kingdom. With these keys, like Eliakim, St. Peter the first Bishop of Rome and his successors are entrusted with Christ's own teaching authority over the new House of David, the Church here on earth (Rev. 1:18, 3:7). Through this office of the Papacy and the Magisterium, Roman Catholics believe that the Kingdom of Heaven governs the Church on earth to lead it to all truth in matters of faith and morals (1 Tim 3:15, Mt 28:20, Jn 16:13).[3] The Vatican's own claims to the Keys as a heraldic statement are limited to the 14th century.[4]

Many Christians point out that Jesus uses much the same language in John 20:23 and therefore conferred some or all of the same powers on all the Apostles. On this basis, Eastern Orthodox believe that the power of the keys is conferred on all bishops.[5] Similarly, Martin Luther and other reformers spoke of the "office of the Keys" as the power of church leaders to admit or exclude from church membership.[6] In the Lutheran Churches, the "Office of the Keys is the special authority which Christ has given to His Church on earth: to forgive the sins of the penitent sinners, but to retain the sins of the impenitent as long as they do not repent."[7] Lutheran doctrine cites John 20:22–23 as the basis for the sacrament of Confession and Absolution.[7]

The Methodist tradition holds that the office of the keys is exercised when the Church baptizes an individual and pronounces him/her saved.[8] The office of the keys is furthermore exercised in the Church "binding and loosing", being able to excommunicate individuals from the sacraments as "ordinarily, no one is saved outside the visible church".[8]

See also
edit
icon	Christianity portal
Keys of the kingdom
Keys of Heaven
References
edit
 Scott Hahn and Mitch Curtis, Ignatius Catholic Study Bible: Matthew (San Francisco: Ignatius Press, 2000)
 The Lutheran Witness, Volumes 9–11. English Evangelical Lutheran Synod of Missouri and Other States. 7 December 1892. p. 98.
 Hahn, Scott Hahn and Mitch Curtis, Ignatius Catholic Study Bible: Matthew (San Francisco: Ignatius Press, 2000.
 https://www.vatican.va/news_services/press/documentazione/documents/sp_ss_scv/insigne/sp_ss_scv_stemma-bandiera-sigillo_en.html#Stemma%20della%20Santa%20Sede
 "Power of the Keys". Catholic Encyclopedia.
 Kenneth A. Locke, The Church in Anglican Theology (Farnham, Surrey, England and Burlington, Vermont, USA: Ashgate Publishing, 2009), pp. 11-13
 Martin Luther. "Part 5: Office of the Keys and Confession". Evangelical Lutheran Synod. Retrieved 25 February 2022.
 Arnold, Johnathan (13 October 2021). "The Church's Authority and Responsibility to Forgive Sins". Holy Joys. Retrieved 31 January 2022.
This article incorporates text from a publication now in the public domain: Wood, James, ed. (1907). The Nuttall Encyclopædia. London and New York: Frederick Warne. {{cite encyclopedia}}: Missing or empty |title= (help)

Last edited 1 year ago by JJMC89 bot III
Related articles
Primacy of Peter
Position of preeminence attributed to Peter
Keys of Heaven
Metaphorical keys of Saint Peter
Keys of the kingdom
Christian concept of eternal church authority
Wikipedia
Content is available under CC BY-SA 4.0 unless otherwise noted.
Privacy policy Terms of UseDesktop
