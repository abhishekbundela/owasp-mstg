# Testing Code Quality

## Overview

[Describe what this chapter is about.]

## Test Cases

### OMTG-CODE-001: Testing for Debug Build 
Debugging is a technique where a hook is attached to a particular application code. Execution pauses once a particular piece of code is reached (break point), giving us the ability to analyze local variables, dump class values, modify values, and generally interact with the program state. A debug build allows therefore an attacker to attach a debugger to the application in order to analyze the behavior during runtime.

#### Detailed Guides

[Add links, e.g.:]

- [OMTG-CODE-001 Android](LINK#OMTG-CODE-001)
- [OMTG-CODE-001 iOS](0x02_OMTG-CODE_iOS.md#OMTG-CODE-001)

#### References

- OWASP MASVS: [NUMBER]: "QUOTE"
- CWE: [Link to CWE issue]

### OMTG-CODE-002: Testing for Exception Handling
[General description]

#### Detailed Guides

[Add links, e.g.:]

- [OMTG-CODE-002 Android](LINK#OMTG-CODE-002)
- [OMTG-CODE-002 iOS](0x02_OMTG-CODE_iOS.md#OMTG-CODE-002)

#### References

- OWASP MASVS: [NUMBER]: "QUOTE"
- CWE: [Link to CWE issue]

### OMTG-CODE-003: Testing for Secure Compiler Flags
Compilers such as CLANG and GCC support hardening options that add additional runtime security features and checks to the generated executables. While these hardening features don’t fix broken code, they do make exploitation of bugs such as buffer overflows more difficult, and should be activated as a defense-in-depth measure.

This test-case aim to check whether the following Flags are enabled whitin the mobile application's binary :

* Stack smashing protection : 
Stack smashing is the willful use of stack overflows to gain control of a system. There are different buffer overflow protectors available, include Stack Smashing Protector (SSP) for GNU's gcc, ProPolice for IBM's XLC, and Buffer Security Check for Microsoft's Visual compilers (option /GS). 
* PIE support :
Position-independent executables (PIE) are binaries that can be wholly relocated in memory. Building an app with PIE support makes it possible to apply Address Space Layout Randomization (ASLR) during runtime. ASLR aims to make exploitation of memory corruption vulnerabilities more difficult. As of Android 5.0, Android requires all dynamically linked executables to support PIE.
* ARC protection : 
Automatic Reference Counting (ACR) is a compile time protection technique introduced since iOS 5. It provide an additional layer of security at runtime by moving the responsibility of memory management (retains, releases, and autoreleases on Objective-C objects ) from the programmer to the compiler. 


#### Detailed Guides

- [OMTG-CODE-003 Android](0x06a_OMTG-CODE_Android.md#OMTG-CODE-003)
- [OMTG-CODE-003 iOS](0x06b_OMTG-CODE_iOS.md#OMTG-CODE-003)

#### References

- OWASP MASVS : [Link to MASVS]
- CWE : [Link to CWE issue]
