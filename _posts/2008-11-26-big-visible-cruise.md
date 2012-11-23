---
layout: post
title: Big Visible Cruise++
excerpt: Using Big Visible Cruise and CruiseControl.NET as an information radiator.
---

Inspired by Jeffrey Palermo's recent post, I figured it was time to finish my post on our "information radiator" setup which has been in my drafts folder for about 6 months.

When we started using CruiseControl.NET for continuous integration a few years back, it didn't take long for us to decide we needed something more visible than CCTray to let us know when a build was broken. The first solution was an Ambient Orb and a customized version of CCTray running on one developer's machine. If the orb was green, all was well; pulsating yellow-to-orange meant a build was running; solid red meant something had gone wrong. It worked for a while, but as the team grew and we moved from one office to another, it became difficult to find a location for the orb which would allow it to be seen by everyone on the team. It was time to come up with another solution.

We were moving into a new space yet again back in May of this year when one of the devs on the team came across Big Visible Cruise. Since we work for an audio/video integration company, getting our hands on some spare LCD displays wasn't terribly difficult, and thus the "App Dev Display Wall" was born ("App Dev" being "Applications Development", the name of our department within the company).

![App Dev Display Wall](/images/display-wall-with-room.jpg)

The four displays are hooked up to a spare PC buried under the two desks seen in the photo above, and they are definitely visible from anywhere in the room. In the photo below, you can see that we're currently utilizing three of the four displays, with the bottom-right running Big Visible Cruise. The bottom-left is running a web browser pointing to an internal URL which displays a few metrics for some of our production applications. The top-left is also running a web browser and is currently configured to show a count-down to the next major release we have scheduled.

![App Dev Display Wall - Close-Up](/images/display-wall.jpg)

We also made a few minor modifications to the source of Big Visible Cruise, adding in such things as custom sorting (by last build date/time), number of minutes/hours since the last build and some tweaks to the styling of the individual boxes to make them a little prettier. (We have not yet submitted our changes back to the BVC project, but we're looking into doing so.)

![Big Visible Cruise](/images/display-wall-bvc.jpg)
