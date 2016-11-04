Git development began in April 2005, after many developers of the Linux kernel gave up access to BitKeeper, a proprietary source control 
management (SCM) system that they had previously used to maintain the project.[13] The copyright holder of BitKeeper, Larry McVoy, had 
withdrawn free use of the product after claiming that Andrew Tridgell had reverse-engineered the BitKeeper protocols.[14]

Linus Torvalds wanted a distributed system that he could use like BitKeeper, but none of the available free systems met his needs, 
particularly in terms of performance. Torvalds cited an example of a source-control management system requiring 30 seconds to apply a 
patch and update all associated metadata, and noted that this would not scale to the needs of Linux kernel development, where syncing 
with fellow maintainers could require 250 such actions at a time. For his design criteria, he specified that patching should take no 
more than three seconds,[8] and added three additional points:

Take Concurrent Versions System (CVS) as an example of what not to do; if in doubt, make the exact opposite decision[10]
Support a distributed, BitKeeper-like workflow[10]
Include very strong safeguards against corruption, either accidental or malicious[9]
These criteria eliminated every then-existing version-control system except Monotone. Performance considerations excluded this, too.[10] 
So immediately after the 2.6.12-rc2 Linux kernel development release, Torvalds set out to write his own system.[10]

The name "git" was given by Linus Torvalds when he wrote the very
first version. He described the tool as "the stupid content tracker"
and the name as (depending on your mood):

  - random three-letter combination that is pronounceable, and not
  actually used by any common UNIX command.  The fact that it is a
  mispronunciation of "get" may or may not be relevant.
  - stupid. contemptible and despicable. simple. Take your pick from the
  dictionary of slang.
  - "global information tracker": you're in a good mood, and it actually
  works for you. Angels sing, and a light suddenly fills the room.
  - "goddamn idiotic truckload of sh*t": when it breaks
