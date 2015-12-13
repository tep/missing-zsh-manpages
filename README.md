
missing-zsh-manpages
====================

This is a simple workaround for the fact that Ubuntu Trusty does not include
the manpages for zsh. This issue was finally resolved for utopic and there was
talk of backporting to the LTS (as one would assume would happen) but, it looks
like that's not going to happen. :-(

You can read all about it on [bug #1242108](https://bugs.launchpad.net/ubuntu/+source/zsh/+bug/1242108)

The files under `man` are the original man pages for the zsh-5.0.2 that are
bundled w/ Trusty plus the original Zsh LICENSE file.

Setup
-----
  1. Install dependencies:

    `sudo apt-get install git makeself`
    
  2. Clone this repo:

    `git clone https://github.com/timpeoples/missing-zsh-manpages.git`


You can now use the `create-installer` script to generate a self-extracting
archive at `./install-zsh-manual` that can be used to install and setup the man
pages for you.  The `post-extract-script` is bundled inside the archive and is
executed when you run the installer (to, you know, install the files). This
installer must, of course, be executed as root (e.g. via sudo)

Once you create the installer, you should copy it to a `tools` folder and use
it in the future (when you next find yourself on a Trusty host without zsh
manuals).

License
-------
The `man/LICENSE-zsh` file covers all of the `man/zsh*.1` files, while the
`COPYING` file covers everything else.  You know the rules; do the right thing.


