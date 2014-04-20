blockchain-common-api
=====================

This repo is intended to promote standard common API for block explorers. 

**Motivation**
Improving availability, dependability, performance of API clients and those of the apps/services based on them.
This is achieved with failover and caching techniques that in a API client are a lot easier in a more standard enviroment.

**Organization**
Inside the common directory there are the proposed standards.
Others directory contains examples from existing block explorers.
Directory structures reflects API calls endpoints.

**Requirements**
To be listed in the common directories, API calls must 
*   Share the same endpoint URL except from a prefix, ie *abc.io/q/addressbalance/BTCADDRESS* and *api.def.zw/v2/q/addressbalance/BTCADDRESS* 
*   Returns the same content type
*   JSON objects returned must have same properties names and values (formatted the same), or a subset of them. 
