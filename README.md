# Blockchain Common API
This repo is intended to promote standard common API for block explorers. 

## Motivation
Improving availability, dependability, performance of API clients and those of the apps/services based on them.
This is achieved with failover and caching techniques that in a API client are a lot easier in a more standard enviroment.

## Organization
Directory structures reflects API calls endpoints. Inside the **common** directory there are common API endpoints that satisfy requirements and are available from at least 2 providers. Inside the **proposal** directory there are API endpoints that are good for API users that they would like be implemented by block explorers to be listed in common directory. Others directory contains examples from existing block explorers.

## Requirements for common
To be listed in the common directories, API calls must 
*   Share the same endpoint URL except from a prefix, ie *abc.io/q/addressbalance/BTCADDRESS* and *api.def.zw/v2/q/addressbalance/BTCADDRESS* 
*   Returns the same content type
*   JSON objects returned must have same properties names and values (formatted the same), or a subset of them.

## Requirements for proposal
Being proposed by API users

## Open for comments, issues, feedback
If you are involved as an API developer or as API users we would like this process will be driven by you.

## Links
*   [bitcointalk thread](https://bitcointalk.org/index.php?topic=575651.0)
*   [Diff example](http://tlrobinson.net/projects/javascript-fun/jsondiff/#%7B%22d%22%3A%7B%22a%22%3A%22%7B%5Cn%20%20%5C%22block_hash%5C%22%3A%20%5C%2200000000000000004f0f6663c621ebb8ad47633e3da7ad71aacdacd39a8f6a99%5C%22%2C%5Cn%20%20%5C%22block_height%5C%22%3A%20295614%2C%5Cn%20%20%5C%22hash%5C%22%3A%20%5C%22c7d9e9c03cfb8c20faa85d3bb72feb47c58082f3677e456181e09d5b2ff7e2a5%5C%22%2C%5Cn%20%20%5C%22addresses%5C%22%3A%20%5B%5Cn%20%20%20%20%5C%221DiWBDy3eejMtUUPAvVLqWmPVsecbqbrSU%5C%22%2C%5Cn%20%20%20%20%5C%221G1qE1DuwAsGftmqK22u6hrmXs1w48erub%5C%22%5Cn%20%20%5D%2C%5Cn%20%20%5C%22total%5C%22%3A%2047295000%2C%5Cn%20%20%5C%22fees%5C%22%3A%2010000%2C%5Cn%20%20%5C%22received%5C%22%3A%20%5C%222014-04-13T13%3A01%3A50.656Z%5C%22%2C%5Cn%20%20%5C%22ver%5C%22%3A%201%2C%5Cn%20%20%5C%22lock_time%5C%22%3A%200%2C%5Cn%20%20%5C%22vin_sz%5C%22%3A%201%2C%5Cn%20%20%5C%22vout_sz%5C%22%3A%202%2C%5Cn%20%20%5C%22confirmed%5C%22%3A%20990%2C%5Cn%20%20%5C%22inputs%5C%22%3A%20%5B%5Cn%20%20%20%20%7B%5Cn%20%20%20%20%20%20%5C%22prev_hash%5C%22%3A%20%5C%227f0b662c4ce439130567155a8490a45c9feddd35ec13c9671ad9e237547b6a86%5C%22%2C%5Cn%20%20%20%20%20%20%5C%22output_index%5C%22%3A%201%2C%5Cn%20%20%20%20%20%20%5C%22script%5C%22%3A%20%5C%22483045022100b60a6f049e6a530f6821c5690ac138a8cc579eea8c99511d02ee54721e445b16022048e523cc0c3b6c2544b0cacaddd5a5d089c31be67c0f613314a06dad37170c05012102cafaf320abfcb744f04459f0fd5de67bbe8e3050f8eb6ebae04d9e1159c7ab78%5C%22%2C%5Cn%20%20%20%20%20%20%5C%22output_value%5C%22%3A%2047305000%2C%5Cn%20%20%20%20%20%20%5C%22addresses%5C%22%3A%20%5B%5Cn%20%20%20%20%20%20%20%20%5C%221DiWBDy3eejMtUUPAvVLqWmPVsecbqbrSU%5C%22%5Cn%20%20%20%20%20%20%5D%2C%5Cn%20%20%20%20%20%20%5C%22script_type%5C%22%3A%20%5C%22pay-to-pubkey-hash%5C%22%5Cn%20%20%20%20%7D%5Cn%20%20%5D%2C%5Cn%20%20%5C%22outputs%5C%22%3A%20%5B%5Cn%20%20%20%20%7B%5Cn%20%20%20%20%20%20%5C%22value%5C%22%3A%2050000%2C%5Cn%20%20%20%20%20%20%5C%22script%5C%22%3A%20%5C%2276a914a4b2246d71fc6372a294d8caf01ef3aa61c8f8a288ac%5C%22%2C%5Cn%20%20%20%20%20%20%5C%22addresses%5C%22%3A%20%5B%5Cn%20%20%20%20%20%20%20%20%5C%221G1qE1DuwAsGftmqK22u6hrmXs1w48erub%5C%22%5Cn%20%20%20%20%20%20%5D%2C%5Cn%20%20%20%20%20%20%5C%22script_type%5C%22%3A%20%5C%22pay-to-pubkey-hash%5C%22%5Cn%20%20%20%20%7D%2C%5Cn%20%20%20%20%7B%5Cn%20%20%20%20%20%20%5C%22value%5C%22%3A%2047245000%2C%5Cn%20%20%20%20%20%20%5C%22script%5C%22%3A%20%5C%2276a9148b7aeb410555eafe52f621d3cecc0e13b1ca2d5d88ac%5C%22%2C%5Cn%20%20%20%20%20%20%5C%22addresses%5C%22%3A%20%5B%5Cn%20%20%20%20%20%20%20%20%5C%221DiWBDy3eejMtUUPAvVLqWmPVsecbqbrSU%5C%22%5Cn%20%20%20%20%20%20%5D%2C%5Cn%20%20%20%20%20%20%5C%22script_type%5C%22%3A%20%5C%22pay-to-pubkey-hash%5C%22%5Cn%20%20%20%20%7D%5Cn%20%20%5D%5Cn%7D%22%2C%22b%22%3A%22%7B%5C%22double_spend%5C%22%3Afalse%2C%5C%22block_height%5C%22%3A295614%2C%5C%22time%5C%22%3A1397394019%2C%5C%22inputs%5C%22%3A%5B%7B%5C%22prev_out%5C%22%3A%7B%5C%22n%5C%22%3A1%2C%5C%22value%5C%22%3A47305000%2C%5C%22addr%5C%22%3A%5C%221DiWBDy3eejMtUUPAvVLqWmPVsecbqbrSU%5C%22%2C%5C%22tx_index%5C%22%3A54431222%2C%5C%22type%5C%22%3A0%2C%5C%22script%5C%22%3A%5C%2276a9148b7aeb410555eafe52f621d3cecc0e13b1ca2d5d88ac%5C%22%7D%2C%5C%22script%5C%22%3A%5C%2276a9148b7aeb410555eafe52f621d3cecc0e13b1ca2d5d88ac%5C%22%7D%5D%2C%5C%22vout_sz%5C%22%3A2%2C%5C%22relayed_by%5C%22%3A%5C%2262.210.146.89%5C%22%2C%5C%22hash%5C%22%3A%5C%22c7d9e9c03cfb8c20faa85d3bb72feb47c58082f3677e456181e09d5b2ff7e2a5%5C%22%2C%5C%22vin_sz%5C%22%3A1%2C%5C%22tx_index%5C%22%3A54437537%2C%5C%22ver%5C%22%3A1%2C%5C%22out%5C%22%3A%5B%7B%5C%22n%5C%22%3A0%2C%5C%22value%5C%22%3A50000%2C%5C%22addr%5C%22%3A%5C%221G1qE1DuwAsGftmqK22u6hrmXs1w48erub%5C%22%2C%5C%22tx_index%5C%22%3A54437537%2C%5C%22spent%5C%22%3Atrue%2C%5C%22type%5C%22%3A0%2C%5C%22script%5C%22%3A%5C%2276a914a4b2246d71fc6372a294d8caf01ef3aa61c8f8a288ac%5C%22%7D%2C%7B%5C%22n%5C%22%3A1%2C%5C%22value%5C%22%3A47245000%2C%5C%22addr%5C%22%3A%5C%221DiWBDy3eejMtUUPAvVLqWmPVsecbqbrSU%5C%22%2C%5C%22tx_index%5C%22%3A54437537%2C%5C%22spent%5C%22%3Afalse%2C%5C%22type%5C%22%3A0%2C%5C%22script%5C%22%3A%5C%2276a9148b7aeb410555eafe52f621d3cecc0e13b1ca2d5d88ac%5C%22%7D%5D%2C%5C%22size%5C%22%3A226%7D%22%7D%7D) of two API methods with same informational content but with different by format


## Donate
For the effort in this project
1DiWBDy3eejMtUUPAvVLqWmPVsecbqbrSU

