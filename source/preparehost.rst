====================
KVM Host vorbereiten
====================

Dieses Howto beschreibt, wie man auf einem frisch installierten Ubuntu
Server 16.04 64bit als Virtualisierungshost die nötigen Vorbereitung
vornimmt, um linuxmuster.net in virtuellen Clients einzurichten.


Wir gehen davon aus, dass bei der Installation mindestens "Ubuntu core
server" und "SSH Server" für die Paketinstallation ausgewählt wurde.

Der bei der Installation angelegt Benutzer (hier: ``linuxadmin``) hat
sudo-Rechte und man sollte sich von außerhalb per ssh auf dem
``serverhost`` über einen Schlüssel anmelden können.

Software installieren
=====================

Auf dem Virtualisierungshost müssen dann ein paar Pakete installiert
werden:

.. code-block:: console

   linuxadmin@serverhost:~$ sudo apt install qemu-kvm
   linuxadmin@serverhost:~$ sudo apt install libvirt-bin


Rechte für Benutzer anlegen
===========================

Damit der lokale Benutzer später Zugriff auf das
Virtualisierungsmanagement hat, fügt man ihn der Gruppe ``libvirtd``
hinzu.

.. code-block:: console

   linuxadmin@serverhost:~$ sudo adduser linuxadmin libvirtd

In meiner Installation reichte es aus, sich ab- und wieder
anzumelden. Das Hinzufügen geschah automatisch.


