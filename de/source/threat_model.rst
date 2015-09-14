================
Bedrohungsmodell
================

.. contents::
   :local:

**************************
Unverschlüsselter Speicher
**************************

* CF-Card/SD-Card/SSD (depending on your model) is not yet encrypted
* Needs to be implemented
* Exposed information in case of seizure:
  * Your address book contacts
  * Your emails
  * Your cjdns private key
  * All passwords

**Abwehr:**

* Use pseudonym names in your address book for your contacts
* Set up a mailclient to receive emails so that they are not stored on the Enigmabox
* In case of seizure: get a new Enigmabox with a new IPv6 (the seized one may be bugged!)
* INFORM YOUR CONTACTS that your Box has been seized, they should remove you from their address book

*******************************************
Kein Passwort gesetzt nach dem ersten Start
*******************************************

This is needed to enable access to the Enigmabox at all.

Please set a password for the webinterface (http://box/passwords/).

**************************************
Benutzer verwendet schwache Passwörter
**************************************

Use strong passwords. Generate random chars::

    <code>tr -cd '[:alnum:]' < /dev/urandom | fold -w50 | head -n20</code>

...add some chars of your own to it. Keep it safe.

**********************************************************
0day exploits (Dienste sind innerhalb des LANs erreichbar)
**********************************************************

* Some services need to be accessible from the LAN port: Web, telephony, email, SSH
* This services can be attacked from the inside of your LAN

**Abwehr:**

* Use strong passwords
* Don't expose the LAN port of your Enigmabox to your whole network
* Use a computer with an operating system built on free software to access the Enigmabox

*****************************************************************************
Benutzer benutzt Windows und besucht Malware-verseuchte Fuudibildli-Webseiten
*****************************************************************************

When you visit a website, it may contain malware which infects your computer.

**Abwehr:**

* Don't use Microsoft Windows
* Don't use Internet Explorer
* Don't visit websites that may contain malware, e.g. porn sites, download sites (with many banners and "stuff")
* Use the proxy server provided by the Enigmabox (Privoxy, http://box/webfilter/)

**********************************************************************************************************************************
Benutzer loggt sich in Facebook ein. Netzwerkverkehr ist identifiziert, NSA lässt QUANTUM und FOXACID laufen und injiziert Malware
**********************************************************************************************************************************

http://sites.miis.edu/cyber/2013/10/08/quantum-and-foxacid-nsatao-mitming-tor-users/

* If you login into Facebook, Twitter, Linkedin, Gmail - *any* site that requires you to authenticate - your network traffic is identified and can be attacked
* QUANTUM is an NSA server that replies *faster* than the Facebook server - redirecting you to FOXACID servers
* FOXACID server impersonates Facebook and injects tailored malware into your computer

.. image:: images/image-583940-galleryv9-bsyq.jpg

**Abwehr:**

* The Enigmabox helps you in hiding IPv4_public
* You have to take care of the rest - do not login anywhere
* Use a separate computer to configure the Enigmabox - and use this Box only for telephony and email - those internal services never leave the encrypted network

***********************************************
Wanzen, andere Personen im Raum, Lasermikrofone
***********************************************

* Somebody planted a bug in your living room
* A laser microphone recording the vibrations of your window glasses
* Your neighbours can hear your shouting through the thin walls
* Listening to your talking, bypassing every encryption

.. image:: images/las_mic2_306x241.jpg

**Abwehr:**

* Get a bug scanner and scan your room
* Talk low-voiced
* Talk in a window-less room

*******************************************
Eingeschaltete Mobiltelefone im selben Raum
*******************************************

* Every powered on smartphone can be turned into a microphone
* Remotely
* Even if it's turned off

**Abwehr:**

.. image:: images/remove-battery.jpg

* Remove the battery from *all* of the smartphones in the room where you are talking
* Have no mobile phone at all, since your location can still be tracked - even if it's an "encrypted mobile phone"
