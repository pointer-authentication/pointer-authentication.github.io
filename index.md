---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Pointer Authentication
---

This page contains projects related to the
ARMv8.3-PAuth memory protection extension. These works are part of the
[hardware-assisted runtime
protection](https://ssg.aalto.fi/research/projects/harp) efforts of the Secure
Systems Group at [University of
Waterloo](https://crysp.uwaterloo.ca/research/SSG) in Canada and [Aalto
University](https://ssg.aalto.fi) in Finland.

# PARTS

> Run-time attacks against programs written in memory-unsafe programming languages (e.g., C and C++) remain a prominent threat against computer systems. The prevalence of techniques like return-oriented programming (ROP) in attacking real-world systems has prompted major processor manufacturers to design hardware-based countermeasures against specific classes of run-time attacks. An example is the recently added support for pointer authentication (PA) in the ARMv8-A processor architecture, commonly used in devices like smartphones. PA is a low-cost technique to authenticate pointers so as to resist memory vulnerabilities. It has been shown to enable practical protection against memory vulnerabilities that corrupt return addresses or function pointers. However, so far, PA has received very little attention as a general purpose protection mechanism to harden software against various classes of memory attacks. In this paper, we use PA to build novel defenses against various classes of run-time attacks, including the first PA-based mechanism for data pointer integrity. We present PARTS, an instrumentation framework that integrates our PA-based defenses into the LLVM compiler and the GNU/Linux operating system and show, via systematic evaluation, that PARTS provides better protection than current solutions at a reasonable performance overhead 

**PAC  it  up:  Towards  Pointer  Integrity  using ARM Pointer Authentication** (2019)  
*Hans Liljestrand*,
*Thomas Nyman*,
*Kui Wang*,
*Carlos Chinea Perez*,
*Jan-Erik Ekberg*,
*N. Asokan*  
[USENIX Security '19](https://www.usenix.org/conference/usenixsecurity19/presentation/liljestrand)

## Source code

Source code for the LLVM PARTS implementation is available at
[github.com/pointer-authentication/parts-llvm](https://github.com/pointer-authentication/parts-llvm).

# PACStack

> A popular run-time attack technique is to compromise the control-flow integrity of a program by modifying function return addresses on the stack. So far, shadow stacks have proven to be essential for _comprehensively preventing_ return address manipulation. Shadow stacks record return addresses in integrity-protected memory secured with hardware-assistance or software access control. Software shadow stacks incur high overheads or trade off security for efficiency. Hardware-assisted shadow stacks are efficient and secure, but require the deployment of special-purpose hardware.
>
> We present _authenticated call stack_ (ACS), an approach that uses chained message authentication codes (MACs). Our prototype, PACStack, uses the ARM general purpose hardware mechanism for pointer authentication (PA) to implement ACS. Via a rigorous security analysis, we show that PACStack achieves security comparable to hardware-assisted shadow stacks _without requiring dedicated hardware_. We demonstrate that PACStack's performance overhead is small (~3%).

**PACStack: an Authenticated Call Stack** (2021)  
*Hans Liljestrand*,
*Thomas Nyman*,
*Lachlan J. Gunn*,
*Jan-Erik Ekberg*,
*N. Asokan*  
[arXiv:1905.10242 \[cs.CR\]](https://arxiv.org/abs/1905.10242)  
(accepted to USENIX Security '21)

[Poster](/assets/pdfs/PACStack.DAC56-LBR-poster.pdf) **Late Breaking Results: Authenticated Call Stack** (2019)  
*Hans Liljestrand*,
*Thomas Nyman*,
*Jan-Erik Ekberg*,
*N. Asokan*  
ACM DAC '19  
[DOI:10.1145/3316781.3322469](http://doi.acm.org/10.1145/3316781.3322469)

## Source code

Source code for the LLVM PACStack implementation is available at
[github.com/pacstack/pacstack-llvm](https://github.com/pointer-authentication/pacstack-llvm).

# PCan

> Stack canaries remain a widely deployed defense against memory corruption attacks. Despite their practical usefulness, canaries are vulnerable to memory disclosure and brute-forcing attacks. We propose PCAn, a new approach based on ARMv8.3-A pointer authentication (PA), that uses dynamically-generated canaries to mitigate these weaknesses and show that it provides more fine-grained protection with minimal performance overhead.

**Protecting the stack with PACed canaries**  
*Hans Liljestrand*,
*Zaheer Gauhar*,
*Thomas Nyman*,
*Jan-Erik Ekberg*,
*N. Asokan*  
SysTex '19  
[DOI:10.1145/3342559.3365336](https://doi.org/10.1145/3342559.3365336)

## Source code

Source code for the LLVM PCan implementation is available at
[github.com/pointer-authentication/pcan-llvm](https://github.com/pointer-authentication/pcan-llvm).
