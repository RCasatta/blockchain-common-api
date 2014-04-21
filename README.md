# Blockchain Common API
This repo is intended to promote standard common API for block explorers. 

## Motivation
Improving availability, dependability, performance of API clients and those of the apps/services based on them.
This is achieved with failover and caching techniques that in a API client are a lot easier in a more standard enviroment.

## Organization
Directory structures reflects API calls endpoints. Inside the *common* directory there are common API endpoints that satisfy requirements and are available from at least 2 providers. Inside the *proposal* directory there are API endpoints that are good for API users that they would like be implemented by block explorers to be listed in common directory. Others directory contains examples from existing block explorers.

## Requirements for common
To be listed in the common directories, API calls must 
*   Share the same endpoint URL except from a prefix, ie *abc.io/q/addressbalance/BTCADDRESS* and *api.def.zw/v2/q/addressbalance/BTCADDRESS* 
*   Returns the same content type
*   JSON objects returned must have same properties names and values (formatted the same), or a subset of them.

## Requirements for proposal
Being proposed by API users

Open for comments
