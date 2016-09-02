# Mignis-Compiler
=================

<pre>
Author: Alessio Zennaro
Supervisor: Prof. Riccardo Focardi
A.Y.: 2015/16
Version: 2.3

This is the new Mignis(+) compiler.
It has been created to perform a translation of a Mignis(+) configuration file
into a generic target firewall language (e.g. Netfilter/iptables, Juniper).

At the moment it supports only the translation into the Netfilter/iptables 
language, but the set of languages can be expanded rather easily.


In order to make this work:
1- Unzip the content of the archive and go to the "utils" directory
2- Issue the "make" command
3- Check if mignis.py and tcbin/target_compiler.py have both +x permissions
3- From the directory where mignis.py is located issue the command:
     ./mignis.py IPTABLES path/to/mignis_configuration_file

In /path/to/mignis_configuration_file will be created two folders:
1- compiled: inside this folder you can find all the files .config written in
   intermediate representation
2- final: inside this folder you can find all the files .iptables written in
   iptables language.


At the moment the syntax of Mignis+ is recognized by the parser but the
final translator does not implement its features.


Version 2.3 new features:
* Mignis and Mignis+ rulex cannot be used together
* Mignis+ configuration files must use only positive rules
* Established connection are not accepted by default:
  there is a new option 'established' that can be set to:
   1- off (default): if established connection are not to be accepted by default
   2- on: if established connection are to be accepted by default

2016-09-02

</pre>
