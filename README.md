**FUSE Filesystem 4 Dropbox** is a FUSE plugin whichs allows a local mount of your
global Dropbox or jailed application folder.

To improve the browsing experience of your Dropbox content this plugin will cache
the structure for a certain amount of time. This python script uses **libfuse** to
provide FUSE function to the operating system.

### Donation

Since I'm developing in my free time I'd like to ask you to support my work.
You can do it by contributing 5 EUR via paypal. This will give me motivation
to keep on coding and fixing bugs.

Thanks in advance: [DONATE NOW VIA PAYPAL](https://www.paypal.com/cgi-bin/webscr?no_note=0&lc=US&business=realriot%40realriot.de&item_name=GitHub+-+ff4d&cmd=_donations&currency_code=USD)

### Requirements

There are some requirements which have to be fulfilled to make this plugin work.
* [FUSE](http://fuse.sourceforge.net/) has to be installed. On Debian you can install FUSE with
 `apt-get install libfuse2`
* Python pkg-resources must be installed.
* Install [fusepy](https://github.com/fusepy/fusepy). On debian you can use `apt-get install python-fuse`, otherwise `pip install python-fuse`.
* The user must have the permission to mount FUSE filesystems. On debian (before Jessie release) systems the user must belong to the group "fuse".
 adduser <user> fuse
* Install dropbox module with for Python `pip install dropbox`

### Compatible systems

I've tested this script running on:

* Linux X86
* Linux X64
* Mac OS X
* Raspberry Pi

Other systems may work...

### Authorize access

Go to the [Dropbox developer home](https://www.dropbox.com/developers) and create a new app.
Then generate an OAuth token and store in a `ff4d.config`.

**Please secure your access token. NOBODY may know it! This token allows full access
to your configured dropbox space.**

### Usage

Quick start:

`./ff4d.py <mount folder>`

The accesstoken can optionally supplied via commandline. Normaly the plugin will ask you just one time
and saves it to a configuration file.

You can see all the mighty arguments by showing the help:

`./ff4d.py -h`

Greets and have fun with this little goodie... _Sascha Schmidt_
