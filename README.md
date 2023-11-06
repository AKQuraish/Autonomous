# Autonomous
OSINT
--------------

# DESCRIPTION:

Under the Saudi Telecom Company JSC network there are around 2300 sytems facing an issue. Can you find the category of that vulnerability?

----------------------------------------------------------------------------------------------

To start investigating we first need to find the Autonomous System Number of the Saudi Telecom Company JSC:

We can find all ASN numbers in Saudi Arabia in https://ipinfo.io/countries/sa#section-summary

<img width="610" alt="image" src="https://github.com/AKQuraish/Autonomous/assets/85708032/4351599d-f905-47a0-97c6-344ff77f5c0f">

Here we see two ASN numbers related to STC, we can try both but we will go with the first one :D.

----------------------------------------------------------------------------------------------

# AN25019

To look into the ASN we will be using Shodan IO

----------------------------------------------------------------------------------------------

# Shodan IO:

![image](https://github.com/AKQuraish/Autonomous/assets/85708032/1595e5b2-d2f6-47b4-8b97-a9a919dab2a8)

What is Shodan IO used for?
Shodan (Sentient Hyper-Optimised Data Access Network) is a search engine designed to map and gather information about internet-connected devices and systems. Shodan is sometimes referred to as a search engine for the internet of things (IoT).

Shodan is a search engine that lets users search for various types of servers connected to the internet using a variety of filters. Some have also described it as a search engine of service banners, which are metadata that the server sends back to the client.

<img width="1068" alt="image" src="https://github.com/AKQuraish/Autonomous/assets/85708032/36bcdbdf-85ca-45f8-a8e0-872b721fa6e5">

----------------------------------------------------------------------------------------------

# Shodan Queries:


Shodan Io uses queries for searching, so for us to look up Autonomous Systems we need a query for it:

<img width="449" alt="image" src="https://github.com/AKQuraish/Autonomous/assets/85708032/a820174e-8da0-4aee-87a1-a7513047f341">

----------------------------------------------------------------------------------------------

# asn:ASN25019

We use the previous query in the search box to have a detailed view of the Network:

<img width="1067" alt="image" src="https://github.com/AKQuraish/Autonomous/assets/85708032/9733788e-f161-45f1-bb97-962b5c7e2597">

*YOU MAY BE REQUIRED TO SIGN UP FOR A FREE ACCOUNT*

From here we go into the "View Report" page to look into more information.

# Here you'll find the vulnerabilities in the network of STC

<img width="279" alt="image" src="https://github.com/AKQuraish/Autonomous/assets/85708032/91b32820-66af-4bd9-a722-6d02fc4a72f5">

Here we can also see a CVE type affecting around 2300 systems.

----------------------------------------------------------------------------------------------

# CVE-2022-32548

Now we just need to look up into this CVE type.

We will be using https://www.cvedetails.com

<img width="1069" alt="image" src="https://github.com/AKQuraish/Autonomous/assets/85708032/85b2dfd3-0c27-45e6-bad8-5ca9d04dcaf8">

After we enter the CVE into the search bar we will see a detailed report about this vulnerability.

From here we can also see the category:

<img width="462" alt="image" src="https://github.com/AKQuraish/Autonomous/assets/85708032/0da37f68-52a3-4713-832d-e5bb0a800d21">

----------------------------------------------------------------------------------------------

# Flag 

So the flag would be: UJCYC{overflow} .





