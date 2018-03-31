---
title: "Data Perfectionism is the Enemy"
author: "Tim"
date: 2016-04-28
slug: funes
---

Back in graduate school, my development economist professor assigned us a story by Jorge Luis Borges. In ["Funes the Memorious"](http://www4.ncsu.edu/~jjsakon/FunestheMemorious.pdf), the protagonist meets a teenage prodigy who has developed perfect memory due to a horseriding accident. For example the young boy could recall an entire's worth of memories, and spend an entire day reliving his thoughts from the previous day. 

As we discussed the story, a student remarked wow, what a cool ability! But I recognized the lesson right away. The boy's ability was a blessing but yet a curse, his perfectionist ability to get every single detail correct prevented him from thinking abstractly or broadly. Hence the relevence to a class on economics, as our professor was stressing the necessity of sacrificing a tiny bit of detail for more broader policy validity. Or something like that, I assumed that was his point. Sorry Jeff.

I've been working on aggregating all the primary results by congressional districts, and it's been increasingly frustrating when noting the disparity between state reporting methods. Tuesday's results in Pennsylvania is a fine example, for they only reported the [results by county](http://www.electionreturns.state.pa.us/ENR_New/Home/CountyBreakDownResults?officeId=1&districtId=1&ElectionID=54&ElectionType=P&IsActive=1). 

I messaged the Green Papers, and they pointed me towards an [AP press release for the Democrats](http://hosted.ap.org/dynamic/files/elections/2016/by_cd/PA_Dem_0426_VD.html?SITE=AP&SECTION=POLITICS) that was much more helpful. To attain their estimated delegate count, they told me their method was "to go from county to CD -- say, 30% of a county is in CDa, 60% in CDb and 10% in CDc: we take 30% of the county vote and apply it to CDa, 60% of the county vote and apply it to CDb, and 10% of the county vote and apply it to CDc. We did that for each county. We have found that the results much more usually end up pretty close to what the final delegate numbers per CD turn out to be".

It should be good enough for me. 

Sigh. Okay so there's 67 counties and 18 congressional districts in Pennsylvania. Some counties are entirely located in one district, some are split across more than one. But I now know that Precinct 1271 of Whitehall Dist 1 of Alleghany County in Pennsylvania (literally the smallest and atomic unit of political geography in the United States) is actually split into 2 Congressional Districts. 

<img src="http://timthoughts.com/Images/Election_Images/allegheny.png" width="350" height="350">

I know this because I'm going to every 67 county websites, downloading their data directly, and filtering it into R. I figured I can obtain which district a particular precinct belongs to if I check which Congressional race they're voting for. That's when I realized 1271 of Alleghany was voting for both candidates and delegates to the 14th and 18th district. When I checked 1272-1288, etc to see the rest of Whitehall 2-16's District, they're all in the 18th. You can double-check my results by Control + F "1271 Whitehall Dist 1" at this [website](http://apps.alleghenycounty.us/election/201604PRI/EL52.htm).

So that ONE particular precinct has a few people living in the 14th. Just to confirm, I made a phone call to Alleghany's elections department this morning, and they told me that because of some redistricting that occured during even-numbered years (when Congressional representatives are elected), a precinct such as 1271 may be split. It's literally the only one in the county. 

Aftering doing more online digging, I finally found an updated spreadsheet matching precincts to districts at the [state website](http://www.legis.state.pa.us/cfdocs/legis/home/findyourlegislator/pdf/2016_PrecinctDirectory_1451924263020.pdf). Considering the lesson of Funes and grad school, I will just recode 1271 a part of the 18th district and move on. Going for perfect granularity when you're dealing with election data is a sisyphean task that will be an endless timesuck. 

I just thought I should write a disclaimer, because while I theoretically accept and understand what I just wrote, it's still frustrating to know that there's incomplete data out there. Just learn to live with it, Tim.
