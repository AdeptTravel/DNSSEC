# DNSSEC
 Create DNSSEC certs/keys and sign zones for NSD zone files on FreeBSD.

DNSSEC is a simple tcsh script to generate DNSSEC certs/keys and sign NSD zones.  For this script to work you will need to do the following:

* The NSD conf directory should be located at /usr/local/etc/nsd
* There should be a directory /usr/local/etc/nsd/dnssec to hold certs/keys/ds files
* There should be a directory /usr/local/etc/nsd/zone for the zone files
* Zones should be named for the domain name with no extension after

This script will create the ZSK, KSK, and DS files and sign the zone file.  In NSD you will want to use the signed zone {domain name}.signed

The DS file contains the information you will need to share with the registrar.  The information you will submit to your registrar is in the last 4 columns which are: Key Tag, Algorithm, Digest Type, and Digest.

Note: When making changes to the zone file you don’t need to resubmit the DNSSEC information to the registrar unless you recreate your ZSK, KSK, and DS.

This script is provided by [The Adept Traveler](https://adept.travel/company/open-source).

The Adept Traveler is a travel agency that specilizies in making travel easier for everyone.  From the novice to the expert, from the able bodied to the disabled traveler, it is out belief that everybody deserves to travel well.

As you can see, we are a travel agency.  Don't expect any support from us using this project.  Best of luck!