# LinuxHelp
Getting help for problems with linux

Linux has become enormously complex, with many different distributions and
support for legacy systems up to huge datacenters.  Many different
physical connectors and data protocols used to connect inernal and external
devices.  No single person understands every aspect of modern linux.  When
something doesn't work right, you need to bring this to the attention of 
the possibly small group of people who can help.

Remember that most people providing help for linux users are volunteers.  Be
respectful of their time and energy.  Do not monopolize their time, as they
may be working with other users who also need help.  If you are asked to 
provide additional information, do that promptly or let others know that 
there will be a delay in providing the requested information.  If your are
able to solve your problem, be sure to post the details so others with the 
same problem can benefit.

## General principles for posts in help forums

Posts should provide enough detail to allow others to reproduce the issue.   It is
also important to use a title that will attract the attention of people who can 
help.  Whenever appropriate, use text rather than images to explain problems, as
text can be indexed and searched.  Effort spent preparing a post saves time in 
back-and-forth messages to clarify your post and makes the post more useful to
the community.  For every person who reports a problem, there can be many others
who have the same problem but are unwilling to participate in the discussion.  
Every forum post should be considered an example that others may want to follow.

* language:
  Many forums use English.  If you are not confident with your English, you can
  use an online translator to produce English text. Consider including text
  in your preferred language so others can correct the translation.  If your
  post includes non-English error messages, offer a translation.
   
* hardware:
  It is often helpful to upload a [Linux Hardware Probe](https://linux-hardware.org)
  and include the link in your forum post.  For problems with devices connected by
  cables, verify that the problem can be reproduced using a different cable.

* wetware:
  Do you prefer navigation by touchscreen, mouse, keyboard,
  ...? Are you familiar with POSIX shell constructs?

* software:
  In order to maximize the number of users with similar
  software and avoid wasting energy on bugs that have already beed
  fixed, you should insure that your system fully updated, including
  flatpaks and firmware:

A classic article with guidance for reporting bugs that also applies to other problems is 
[How to Report Bugs Effectively by Simon Tatham](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html).
This article has translations to languages other than English.

## If you are not familiar with POSIX shell constructs

Linux troubleshooting often requires use of the command-line in a terminal.
One common class of failures that occur when upgrading linux is failure to
boot to the login screen.  In such cases, using ssh to connect in text mode
from another system or using a text console is often needed to collect error 
messages as well as to edit configuration files or install additional packages.
When seeking help in online forums, text is much more effective than images 
because it can be indexed and searched.

Online forums often include lengthy exchanges to help users who have never
learned to use the command-line.  Most people can learn basic command-line
usage after a few afternoons workign through a good introductory reference.
It is also necessary to learn a few distribution-specific commands to install
packages.  

The internet provides many "quick and easy" guides to the linux shell. The core
functionality of the linux shell programs is shared with legacy Unix and Apple MacOS.

The majority of internet easy guides to the shell plagerize other sites and often include 
misinformation.  One reliable resource with a long history and several tranlations is 
[LinuxCommand](https://linuxcommand.org).

Other reliable guides include include [Apple's Terminal User Guide](https://support.apple.com/en-ca/guide/terminal/welcome/mac)

## [Fedora Discussion](https://discussion.fedoraproject.org/)

* hardware
  Please include (as text using `</>`) the output from running `inxi -Fxxz` iin a terminal to provide a detailed overview with device ID's. 

* software
  To ensure that a system is fully updated:

```
# dnf update --refresh
# flatpak update
# fwupdmgr refresh --force
# fwupdmgr get-updates
# fwupdmgr update
```
