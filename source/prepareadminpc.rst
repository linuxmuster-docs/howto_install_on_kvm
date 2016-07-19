==================================================
 Einen Arbeitsplatz zur Administration einrichten
==================================================

Um KVM mit der grafischen Oberfläche "virt-manager" administrieren zu
können, kann man auf dem Virtualisierungshost einen X-Server laufen
lassen und dann vor Ort dem Host-PC arbeiten.  Aus Sicherheitsgründen
macht man das normalerweise nicht und installiert das Programm auf
einem separaten PC. Über eine ssh-Verbindung wird dann der Host-PC
gesteuert.


Virt-manager installieren
=========================

Installieren Sie mit Administratorrechten (hier hat der Benutzer
"user" sudo-Rechte) die Programme ``virt-manager`` und
``ssh-askpass-gnome`` auf einem Arbeitsplatz (hier: ``admin-pc``):

.. code-block:: console

   user@admin-pc~$ sudo apt install virt-manager ssh-askpass-gnome

Remoteverbindung herstellen
===========================
   
Stellen Sie fest, ob Sie sich mit dem Benutzer vom Administrations-PC
aus auf dem Host-PC einloggen können:

.. code-block: console

   
