Statement of Condemnation from the Anthon Open Source Community Regarding the Inappropriate Behaviors of the Linux Foundation and its Employees
===

Yesterday (October 23, 2024) was undoubtedly a day of disgrace and despair. We witness the attack, humiliation, and slander of our community's contributors.

Last Sunday, a trust-destroying and shameful commit was silently merged. With that commit, tens of Linux kernel contributors and subsystem maintainers of Russian nationality were stripped of their maintainer status.[^1] Along with many contributors and followers of the Linux kernel, some of our community members questioned and voiced their severe criticism towards the commit.[^2][^3] At the time of writing, it was not only the Linux Foundation that had failed to publish any public statement explaining their positions. Linux Torvalds, the founder and one of the core maintainers of the Linux kernel project, along with Greg Kroah-Hartman, the maintainer of the [linux-stable](https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux.git) tree had both chosen to conspire with the Linux Foundation in this extremely discriminating witch-hunting.

Before we continue with our statement of condemnation, it might be helpful to reference the following report assembled by our community contributors:

> Several days ago, Greg Kroah-Hartman (hereafter Greg K-H), one of the main maintainers of the Linux kernel submitted an unusual ["documentation update"](https://github.com/torvalds/linux/commit/6e90b675cf942e50c70e8394dfb5862975c3b3b2), removing numerous maintainers using email addresses with the <.ru> top domain name, along with one known maintainer of Russian nationality from the MAINTAINERS (a record of kernel maintainers) file.
>
> This commit had been merged by Linus Torvalds as part of the 6.12-rc4 code.
> 
> Greg K-H did not explain the specific motives behind this commit. Rather, he vaguely referred to "various compliance requirements" and that the affected individuals may "come back in the future if sufficient documentation is provided."
>
> The process Greg K-H took to remove the relevant maintainers was quite crude. For instance, with subsystems where the sole maintainer held an e-mail address with a <.ru> top-level domain, the whole subsystem was removed from the MAINTAINERS file. This includes many important and widely-used subsystems such as the UFS filesystem and PPTP drivers. As  the Linux kernel's development process takes part solely on the mailing lists, should a maintainer get removed from the MAINTAINERS file, they would no longer automatically receive subsystem patches and communications in their inbox or even relevant mailing lists. This may cause many patches to fall into the ether and, if the maintainers fail to keep up with subsystem maintenance due to this lapse in communication, it is only a matter of time that a subsystem would get dropped out from the kernel tree.
> 
> Generally, patches for the Linux Kernel were sent to the relevant mailing lists, copying relevant individuals (such as subsystem maintainers and active contributors). Said patches would also undergo discussions and reviews before they were pulled in and merged. However, Greg K-H seemed to have deliberately bypassed this procedure, sending the patch to the busy and often overlooked [patches@lists.linux.dev](https://lore.kernel.org/linux-patches/?t=20241018113153) list; just two days later, he submitted a pull request to Linus Torvalds, with the latter merging the commit without any comment or question.
>
> Considering the fact that both Linus Torvalds and Greg K-H are employed at the Linux Foundation, a501(c)(6) organization in the United States of America, it is easy to deduce what they referred to as "various compliance requirements."
>
> At the time of writing, Greg K-H is yet to respond to any questioning from the mailing list. No matter how this incident would end, this is one of the most shameful commits the Linux kernel community had witnessed in history.

Soon after the incident unfolded, Ke Xiaoyu (柯晓宇) bravely submitted a revert patch and voiced her discontent and doubt.[^4] At the same time, our fellow community contributors watched intently, hoping that Greg Kroah-Hartman and Linus Torvalds's actions might have been driven by under unspeakable political pressure.

Unfortunately, we would soon see Greg Kroah-Hartman violating the [Notes about Netiquette](https://people.kernel.org/tglx/notes-about-netiquette-qw89) and communicated in private with multiple individuals who partook discussion on the mailing list.[^5] Even more so, Linus Torvalds took the most despicable means to respond to questioning - by attacking, humiliating, and slandering our community contributors[^6]：

> It's entirely clear why the change was done, it's not getting reverted, and using multiple random anonymous accounts to try to "grass root" it by Russian troll factories isn't going to change anything.

Linus Torvalds added that "innocent bystanders" should have understood that the "compliance requirements" that Greg Kroah-Hartman cited were not specific to the United States. He added that those who were not familiar with the current sanctions against Russia should "read the news some day."

Then, Linus Torvalds turned to attack Ke Xiaoyu's revert patch:

> As to sending me a revert patch - please use whatever mush you call brains. I'm Finnish. Did you think I'd be *supporting* Russian aggression? Apparently it's not just lack of real news, it's lack of history knowledge too.

With the present day's extremely tense geopolitical circumstances, we find Linus Torvalds' attempt to equate political opinions with nationalities extremely irresponsible. This is not to mention his slandering of opposing opinions from the community as "Russian trolls" and results of absorbing 
"Russian state-sponsored spam." Linus Torvalds' statements have done irreparable damage to the mutual trust in the Linux kernel community and the international open source communities at large - not to mention the free and open source software movement partaken by all of mankind around the globe.

Given all of the above, we hereby voice our strong protest and condemnation of the inappropriate actions taken by the employees at the Linux Foundation, as well as by the Foundation itself. We demand that the Linux Foundation explain itself for Linus Torvalds and Greg Kroah-Hartman's actions. We also ask the Foundation to apologize and rehabilitate all affected in this incident.

[^1]: https://lore.kernel.org/all/2024101835-tiptop-blip-09ed@gregkh/
[^2]: https://lore.kernel.org/all/a08dc31ab773604d8f206ba005dc4c7a@aosc.io/
[^3]: https://lore.kernel.org/all/20241023080935.2945-2-kexybiscuit@aosc.io/
[^4]: https://lore.kernel.org/all/20241023080935.2945-2-kexybiscuit@aosc.io/
[^5]: Mingcong Bai, one of our community's contributors decided to publish Greg Kroah-Hartman's private conversation, having found humiliation and little sincerity in the communication, https://lore.kernel.org/all/444fa53bdfdee75522a1af41655a99b0@aosc.io/
[^6]: https://lore.kernel.org/all/CAHk-=whNGNVnYHHSXUAsWds_MoZ-iEgRMQMxZZ0z-jY4uHT+Gg@mail.gmail.com/
