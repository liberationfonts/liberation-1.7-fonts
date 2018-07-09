Introduction
############

The Liberation(tm) Fonts is a font family which aims at metric compatibility with Arial, Times New Roman, and Courier New. It is sponsored by Red Hat


History
#######

+ "On May 9, 2007, Red Hat announced the initial public release of these fonts under the trademark LIBERATION at the Red Hat Summit. There are three sets: Sans (a substitute for Arial, Albany, Helvetica, Nimbus Sans L, and Bitstream Vera Sans), Serif (a substitute for Times New Roman, Thorndale, Nimbus Roman, and Bitstream Vera Serif) and Mono (a substitute for Courier New, Cumberland, Courier, Nimbus Mono L, and Bitstream Vera Sans Mono)." 

+ Red Hat, Inc. (2007), [Online], `Available: <https://www.redhat.com/promo/fonts/>`_ [11 May 2010].*

+ "On Jul 18, 2012, Liberation fonts 2.00.0 version is released based on croscore fonts to resolve long standing licensing problem and also get more coverage present in croscore fonts."

+ Liberation 1.07.* has a bytecode hinting instructions and Liberation 2.00.* has automated hinting instruction. Though shapes are same due to hinting instruction, it gives different rendering experience. Many users still like liberation 1.07. Now liberation has 3 repos 1. Liberation 1.07, 2 Liberation Narrow and 3. Liberation in at `<https://github.com/liberationfonts>`_


License
#######


#. The Liberation(tm) version 2.00.0 onward are Licensed under the SIL Open Font License, Version 1.1.
#. Older versions of the Liberation(tm) Fonts is released as open source under the GNU General Public License version 2 with exceptions. `<https://fedoraproject.org/wiki/Licensing/LiberationFontLicense>`_



Download
########


Current Release 
***************

+ Binary (ttf): `liberation-fonts-ttf-1.07.4.tar.gz <https://releases.pagure.org/liberation-fonts/liberation-fonts-2.00.1.tar.gz>`_
+ Source (sfd): `liberation-fonts-1.07.4.tar.gz <https://releases.pagure.org/liberation-fonts/liberation-fonts-1.07.4.tar.gz>`_


This release includes a source tarball also so it is easy to build the
ttf files from sources.


Previous Releases
*****************

+ Binary (ttf): `liberation-fonts-ttf-1.07.3.tar.gz <https://releases.pagure.org/liberation-fonts/liberation-fonts-2.00.0.tar.gz>`_
+ Source (sfd): `liberation-fonts-1.07.3.tar.gz <https://releases.pagure.org/liberation-fonts/liberation-fonts-1.07.3.tar.gz>`_


Source and TrueType archives are available at `<https://releases.pagure.org/liberation-fonts/>`_.


Distribution
############

The Liberation(tm) Fonts are packaged for a wide range of Linux distributions:


+ Fedora : liberation-fonts is included in Fedora and installed by
  default. The Fedora package can be checked `here <http://koji.fedoraproject.org/koji/packageinfo?packageID=liberation-fonts>`_.
+ RHEL : liberation-fonts is available for Red Hat Enterprise Linux from RHN.
+ Debian : ttf-liberation has been added to Debian. The Debian package can be checked `here <http://packages.debian.org/search?keywords=ttf-liberation&searchon=names&suite=all&section=all>`_.
+ Ubuntu : ttf-liberation has been added to Ubuntu. The Ubuntu package can be checked `here <http://packages.debian.org/search?keywords=ttf-liberation&searchon=names&suite=all&section=all>`_.



Feedback
########

Please reports bugs or requests for enhancements at `Red Hat Bugzilla <https://bugzilla.redhat.com/enter_bug.cgi?product=Fedora&component=liberation-fonts>`_. When filing a bug please mention the version of liberation-fonts and the OS.


Development
###########

You can get the current source using the following commands:

Anonymous GIT access

::
	
	$ git clone `<https://github.com/liberationfonts/liberation-1.7-fonts.git>`_

Read and Write Url
 
::

	$ git clone `<git@github.com:liberationfonts/liberation-1.7-fonts.git>`_

Other Requirements
******************

Install fontforge `<http://fontforge.sourceforge.net>`_

Installation
************
Decompress tarball
==================
You can extract the files by following command:

::

	$ tar zxvf liberation-fonts-[VERSION].tar.gz

Build from the source
=====================
Change into directory liberation-fonts-[VERSION]/ and build from sources by following commands:

::

	$ cd liberation-fonts-[VERSION]
	$ make

The built font files will be available in 'build' directory.

Install to system
=================

For Fedora, you could manually install the fonts by copying the TTFs to ~/.fonts for user wide usage, or to /usr/share/fonts/truetype/liberation for system-wide availability. Then, run "fc-cache" to let that cached.

For other distributions, please check out corresponding documentation.

Usage
=====

Simply select preferred liberation font in applications and start using.

Discussion about the fonts can be made on `Fedora Fonts List <https://lists.fedoraproject.org/mailman/listinfo/fonts>`_.

For Maintainers
===============

Before packaging a new release based on a new source tarball, you have to update the version suffix in the Makefile:

    VER = [VERSION]

Make sure that the defined version corresponds to the font software metadata which you can check with ftinfo/otfinfo or fontforge itself. It is highly recommended that file 'ChangeLog' is updated to reflect changes.

Create a tarball with the following command:

::

    $ make dist

The new versioned tarball will be available in the dist/ folder as 'liberation-fonts-[NEW_VERSION].tar.gz'.


Developers
########## 


+ Pravin Satpute - current maintainer
+ Herbert Duerr - contributed SansNarrow
