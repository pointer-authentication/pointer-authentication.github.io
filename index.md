---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

> Run-time attacks against programs written in memory-unsafe programming languages (e.g., C and C++) remain a prominent threat against computer systems. The prevalence of techniques like return-oriented programming (ROP) in attacking real-world systems has prompted major processor manufacturers to design hardware-based countermeasures against specific classes of run-time attacks. An example is the recently added support for pointer authentication (PA) in the ARMv8-A processor architecture, commonly used in devices like smartphones. PA is a low-cost technique to authenticate pointers so as to resist memory vulnerabilities. It has been shown to enable practical protection against memory vulnerabilities that corrupt return addresses or function pointers. However, so far, PA has received very little attention as a general purpose protection mechanism to harden software against various classes of memory attacks. In this paper, we use PA to build novel defenses against various classes of run-time attacks, including the first PA-based mechanism for data pointer integrity. We present PARTS, an instrumentation framework that integrates our PA-based defenses into the LLVM compiler and the GNU/Linux operating system and show, via systematic evaluation, that PARTS provides better protection than current solutions at a reasonable performance overhead 

**PAC  it  up:  Towards  Pointer  Integrity  using ARM Pointer Authentication** (2019)  
*Hans Liljestrand*,
*Thomas Nyman*,
*Kui Wang*,
*Carlos Chinea Perez*,
*Jan-Erik Ekberg*,
*N. Asokan*  
[USENIX Security '19](https://www.usenix.org/conference/usenixsecurity19/presentation/liljestrand) (to appear)   
[arXiv:1811.09189\[cs.CR\].arxiv.org/abs/1811.09189](https://arxiv.org/abs/1811.09189)

## Source Code

Initial PARTS/LLVM source code available on
[GitHub](https://github.com/pointer-authentication/PARTS-llvm). The current
source code is that which was used for evaluation presented in our **PAC it up:
Towards Pointer Integrity using ARM Pointer Authetnication** paper. We are
currently working on an updated version, which will be released at a later
date.

## About

This work is part of the [hardware-assisted runtime
protection](https://ssg.aalto.fi/research/projects/harp) efforts of the [Secure
Systems Group](https://ssg.aalto.fi) at the [Aalto
University](https://www.aalto.fi) in Espoo, Finland.
