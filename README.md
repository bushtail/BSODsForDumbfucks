# BSODs For Dumbfucks
## Why was this article written?
If you're like me, you've experienced a few bluescreens in your time - whether it's a client's computer or your own. This is meant to be an exhaustive, in-depth list of Blue Screens of Death (BSODs) and what they mean. Some bluescreens are vague - these will be explained in as much depth as possible while still providing a layman's explanation, however these problems are mostly dependent on the content in the problem reports and dumps provided by Windows. This list is relevant to Windows 10 only, if you're using a different operating system, i.e. Windows XP or 7 (or, God help you, Windows 9x) information may or may not differ. The bluescreens will be sorted by their STOP Code, not alphabetically - however the section names will contain the error message for easier access.

## What is a Blue Screen of Death?
A Blue Screen of Death (BSOD) is a fatal error similar to UNIX-like's Kernel Panic. A fatal error does not mean your computer is dead - a fatal system error is when an error in Windows' kernel (the core operating system program) causes the machine to halt, ending in a reboot. A BSOD may be recurring, and may even happen during the system's start up procedure, causing an infinite boot-loop. Knowing what the bluescreen means, or at least, narrowing down what it *could* mean, is the first step towards an effective diagnosis of computer issues.

## Table of Contents
1.

### 0x00000001 - APC_INDEX_MISMATCH
#### Microsoft's Definition
"The APC_INDEX_MISMATCH bug check has a value of 0x00000001. This indicates that there has been a mismatch in the asynchronous procedure calls (APC) state index."

#### Layman's Explanation
This bluescreen means that a **driver** is using these "APCs" incorrectly, so the computer halts. To fix this, make sure you update all device drivers on your system, and, in the case of newly-installed hardware, make sure the bluescreen only happens with the new hardware installed.

Another cause of this bluescreen is an issue with corrupted system files. In an elevated (run as administrator) command prompt, using the command `sfc /scannow` is usually the best first course of action. This command will be explained in the glossary section of this article.
