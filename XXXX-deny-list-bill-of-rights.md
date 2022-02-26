# HIP Template

- Author(s): pilotdeveloper /// proslasher#2590
- Start Date: 2022-02-25
- Category: Economic
- Original HIP PR: <!-- leave this empty; maintainer will fill in ID of this pull request -->
- Tracking Issue: <!-- leave this empty; maintainer will create a discussion issue -->

# Summary
[summary]: #summary

This HIP aims to clearly define a "bill of rights."  In otherwords, this will clearly define why a hotspot will be added to a deny list and provide a set of guidelines for all.

# Motivation
[motivation]: #motivation

Currently, there's confusion in the community as to what constitutes acceptable versus unacceptable behavior. We need a clear definition of "deny list activities" that will have someone added, along with the appeal process if the violation is not severe.

# Stakeholders
[stakeholders]: #stakeholders

* Who is affected by this HIP?
All hotspot owners should be able to weigh in on this HIP. This will have no impact to anyone who's using the network honestly; however, it will define a set of guidelines and rules so that all can follow.

* How are we soliciting feedback on this HIP from these stakeholders? 
This will actively be communicated in all channels including github, discord, reddit, and potentially the helium app. 

# Detailed Explanation
[detailed-explanation]: #detailed-explanation

For the following section, we will break out some of the reasons as to why one will be added to the deny list. 

## Deny List Activities

### 1. Packet Manipulation

**Severity:** High

**Description:** 
Packet manipulation is when a user is modifying LoRaWan packet data such as RSSI, SNR, or other metadata that the radio generates about the LoRaWan packet. 

**Punishment** Immediate addition to deny list, minimum 60 days before it can be re-evaluated

**Appealable:** Yes - after sixty days and with demonstration that the firmware has been corrected to the factory settings, the owner may appeal with the appeal process. The owner must pay for the review ($50 paid in HNT) and will be on probation for life after removal. 

**Two Strikes** If an owner is caught doing this again after the appeal was approved, the hotspot will be permanently denied and never removed. 


### 2. Farming
**Severity:** High

**Description:** 
Farming is defined as someone intentionally running a large number of hotspots that are co-located within the same room and intentionally asserting them so that it appears the hotspots are legitimate. 

**Punishment** Immediate addition of all hotspots involved with farming to deny list, minimum 45 days before it can be re-evaluated.

**Appealable:** Yes - after fourty-five days and with demonstration that the hotspots have been deployed in physical locations. The appeal process will require a full length video or call with someone before the appeal will be considreded. The owner must pay for the review ($50 paid in HNT per hotspot) and will be on probation for life after removal. 

**Two Strikes** If an owner is caught doing this again after the appeal was approved, all participating hotspots will be permanently denied and never removed. 

### 3. Replaying packets / Packet Flooding
**Severity:** Medium-High

**Description:** 
This attack occurs when miner A hears a packet and sends it to miner B. This attack allows one to have a better chance to be added to the 14 random witnesses because multiple miners are claiming to have heard the same packet. 

*Note on detection:* This is easily detectible and can be demonstrated by looking at months of data for hotspots.

**Punishment** Immediate addition of all hotspots involved with replaying packets to deny list, minimum 30 days before it can be re-evaluated.

**Appealable:** Yes - after thirty days and with demonstration that the hotspots have all been restored. The owner must pay for the review ($50 paid in HNT per hotspot) and will be on probation for life after removal. 

**Two Strikes** If an owner is caught doing this again after the appeal was approved, all participating hotspots will be permanently deny listed and never removed. 


### 4. Improper assertion
**Severity:** Low

**Description** 
A hotspot should be considered Improperly Asserted if a hotspot is asserted more than 2 KM from where it's actually located. 

*Note on detection:* This may be user submitted; however, the actual hotspot's location must be demonstrated using mapping techniques and RSSI calculations. 

**Punishment** Public accusation of incorrect assertion with 30 days for the owner to respond. If no actions are taken, hotspot will be added to the deny list.

**Appealable** If the owner acknowledges the accusation and relocates and/or reasserts the hotspot, they will not need to appeal this (and the case will be dropped). If the hotspot is added due to lack of response, the case may be appealed for a $20 fee (paid in the HNT equivalent). 

**Three Strikes** If the same hotspot is caught doing this more than three times, the hotspot will be added to the deny list permanently.

**Other note:** This violation is considered lower as long as a hotspot is participating in valid PoC activity by beaconing and witnessing within a reasonable tolerance. The severity is higher if a hotspot is receiving abnormally high amounts of traffic. 


## Edge Cases 

*What if I buy a hotspot from someone who was cheating and I didn't know it was on the deny list?* If a user can demonstrate that they made a purchase from an individual unknowingly, they will be allowed to have one chance after ensuring the firmware was corrected. The review will cost the same as the appeal fee above.

*What if I'm a hosting company and my users are doing this with my hotspots?* The same rules apply; however you need to do a better job at ensuring you vet your hosts.

*What if I was included in a farmer's location but I'm legit?* You will still need to go through the review process; however, if it's demonstrated that you're a legitimate miner, the HNT fee will be returned to you after the review. 


# Drawbacks
[drawbacks]: #drawbacks

- Why should we *not* do this?

# Rationale and Alternatives
[alternatives]: #rationale-and-alternatives

Adding this set of governing rules will allow us to be more transparent as to why hotspots are added to the deny list and allow individuals to better prepare their strategies. 

# Unresolved Questions
[unresolved]: #unresolved-questions

- Who is the governing body?

A grant is being proposed for DeWi to review and potentially fund to help establish a third party governing body. This grant will be used to fund the review body, the submission system, and the deny list management. This is a draft for the rules, the HIP for the governing body will be added later. 

# Deployment Impact
[deployment-impact]: #deployment-impact

Existing denylist members will be allowed to appeal under the rules above. 

# Success Metrics
[success-metrics]: #success-metrics

N/A
