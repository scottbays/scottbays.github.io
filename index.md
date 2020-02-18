# WolverineSoft Studio Dev Blog
## Dev Blog 2/3 - 2/17

This sprint started with studio members learning our pod assignments. I was fortunate enough to be assigned to the player pod, which was the pod I indicated I was most interested in. The player pod lead and I are the two designers working on the movement and combat of the main character Io. In addition, we also are responsible for designing mechanics that directly impact the main character such as items. 

The first design task I was assigned on Jira was to outline a new collectible item and assess its viability. The idea was that there would be an item that players could find and collect that would increase the length of time the player could stay in a state of slow motion while aiming. The first thing I did when considering this mechanic was to discuss with the player pod lead two broad directions for the implementation of such an item. The first I discussed was a singular pickup that the player would find on the critical path (i.e. you can’t miss it) of the game that constitutes a significant boost in the pool of slow-mo time. This pickup would represent significant progression of the player’s power and future challenges could be designed with this new larger slow-mo pool in mind. The second option I proposed was to have many items that are either hidden or gated behind small platforming or combat challenges. Each time the item was collected the player would get an incremental, quality of life increase to their slow-mo meter. Of course, because obtaining these upgrades would be optional, enemy and level designers would always have to consider the player may have the default slow-mo meter capacity.

The pod lead and I both agreed that the first option did not sound interesting enough to be a ‘big’ upgrade, while the second option with multiple smaller upgrades allowed for more opportunities to design interesting challenges for the player. 
From this point I wrote [a document](https://docs.google.com/document/d/1KUtRRBMq8uqpyk0kP86IlGxvxjnUNe4FZTW7grFuLh8/edit?usp=sharing) that answered a set of question the pod lead had prepared regarding the proposed mechanic. In addition, I enumerated a handful of concerns I had regarding this proposed mechanic. I discussed these concerns with the pod lead in the comments of the document. One concern I had was that the players that were skilled enough to complete optional challenges would in turn be rewarded with an item that makes the game slightly more forgiving. This positive feedback loop could reasonably compound to the point where if some players receives multiple noticeable upgrades to their slow-mo meter by the end of the game and others don’t, the game may be noticeably harder for players that struggled to get upgrades earlier in the game. 

The counterfactual here is that if every upgrade to the slow-mo meter was not noticeable and the only aggregate result of collecting every upgrade was noticeable, there would be a minimal positive feedback loop. But if there is no noticeable mechanical progression the players would probably get the same fulfillment of getting a text pop-up that said, “Found Secret 5/7”. At this point I wondered: Why have the item increase your meter at all?

Of course, most games give rewards for good play rather than bad play, but the real problem I ran into was coming up with a system that was incrementally noticeable but didn’t trivialize gameplay in aggregate. This led me to consider if there were more interesting ways to engage with the slow-mo and teleport mechanics. 

I came up with an idea that was inspired by the air-dash reset item from Doom Eternal. The concept I developed was nearly identical to an idea that leads from other pods came up with independently. I proposed an item that would be scattered around platforming areas that would reset the slow-mo meter and the ability to teleport so players could teleport to these items in order to chain their teleports together. Ultimately it was decided to scrap the original idea outlined in the document in lieu of this new idea.

![Doom Eternal Pre-Release Image](https://i.imgur.com/PEkC3QJ.jpg)

Another thing I did for this sprint was clone the Git repo and start playing with the Player Movement prototype scene to get a feel for the controls and the intricacies of the movement as it was currently implemented. After doing this I contacted my pod lead with a couple suggestions about controls and movement mechanics. I also played two good feeling (yet quite different) 2D platformers, Dead Cells and Hollow Knight, as references to see what choices they made and where we could learn from them. This led to some changes that I felt made the platforming more intuitive particularly in sections where precise wall jumps were required. See the GIFs below for a comparison of the changes.

Old:
![Old](https://i.imgur.com/tTe9YcT.gifv)

New:
![New](https://i.imgur.com/dD3K0nY.gifv)
