# WolverineSoft Studio Dev Blog
## Dev Blog 3/23 - 4/6
This sprint started with me meeting twice to work together with my pod lead, who wrote the bulk of the character controller, to help me rework the amining controls, there were a few snags along the way, but we were able to implement the controls in the way I invisioned. The feedback we received from other studio members has been positive, some even say that the mouse+keyboard controls are now their prefered way to play the game.

The next thing I did was work on the next second stage of the windmill fort zone. For this stage I had a bit of a template to follow using the rough draft I was given. In its original incarnation it was quite horizontal, and flat than the other stages, which focused on long strigns of vertical windmill launches.

![Iteration 1](https://i.imgur.com/b1cOCzB.jpg)

Because this stage served as a transtion between two vertical segments I also thought it would be good to have this stage be a more combat focused interlude between the other two windmill-platforming focused stages. 

![Iteration 2](https://i.imgur.com/DQxQTTT.jpg)

At the end of the stage devlopment process all three of the windmill fort stages were unfortunately cut from the weeks build. Besides the presence of a lot of temp art and lack of refinement, the biggest issue was that playtesters new to the windmill launching mechanic were taking a very long time to learn how to pull off successful jumps with it. When I first played through the first iteration of the windmill fort at the beginning of this sprint I myself ran into similar issues, where it took me some time to discover the idiosyncrasies of the mechanic. Another problem that was paired with this steep learning curve was the difficulty. I found it nearly impossible to beat the last third of the first level where the windmills are introduced, even with spike damage disabled. 

As a result of these myriad issues, a downscoping of the zone was in order, and the second stage I had worked on was cut as it was the earliest along in the iteration process and didn't do as much to showcase the possibilites of the windmill mechanic. Going forward I was asssinged to work on making the windmill launch mechanic is more accessible and easy to pull off. And after that I will be focusing on the first windmill fort stage to add enemies, reduce platforming difficulty, remove temp art and above all ensure that the mechanics are effectively tutorialized for new players. I think the windmill launch is a really engaging mechanic and really want to see it fleshed out in the game so I'm excited to work towards ensuring that players can get the most out of this great mechanic.

New Tiles: 

![Tiles](https://i.imgur.com/8LaGWsN.jpg)

# Time Breakdown:
Meetings: 7hrs., Play testing: 1hr, Level Creation: 5 hrs, Level Iteration: 2hrs. 

## Dev Blog 3/2 - 3/23
For this sprint I found myself largely transitioning to a new role within the studio. At this time in the development process there is a bit of a bottleneck in terms of both asset generation and integration in areas such as art, music and level design. I now am starting to meet with the level design pod, in addition to the player pod, to give feedback, do play testing, design levels, and implement levels. 

The first thing I did was to familiarize myself with the tools that level designers have been using for Project Blue. This involved me throwing some tiles and secene trasition points around to see how everything fits together. There were a couple of hiccups I ran into but other people from the level-design pod were quite helpful on getting me up to speed. 

Next sprint I hope to get my hands dirty by designing content for the Windmill Forts zone of the game. This is the more non-linear of the two major zones featured in the game and I am excited to come up with levels that can encourage exploration without being aimless or frustrating. I also am looking forward to creating gameplay sequences using the mechanic of spinning on windmills to gain momentum and fling yourself off of them. I think there is a lot of potential for interesting platforming sequences using this mechanic and also am curious if enemies could be placed near the windmills to spice up the combat. Ofcourse, this could be a terrible idea but I think its worth considering.

Also after drafting up yet another prototype of mouse controls this week, complete with new annoyances, the player pod lead and I have determined that a complete rework of how aiming works in the game is inorder, currently it is done with a line renderer that originates from the player, but only the end is visible (see below). 

![Line](https://i.imgur.com/tVpHylm.jpg)

However now we are moving towards a new reticle design, (one potential canidate is below) and we are thinking that this, combined with our mouse difficulties, makes this the perfect time to stop using the line render.

![Reticle](https://i.imgur.com/uENb1GS.png)

#Time Breakdown:
Meetings and discussion: 7hrs., Mouse control refinements: 4hrs., Playtesting: 1hr, Level Design Familiarizing: 2hrs. 

## Dev Blog 2/17 - 3/2
This sprint started with me play testing the official build of Project Blue. I gave feedback on the build, focusing on feedback that was relevant to the player pod. I gave feedback to the animators about how exaggerated the idle animation was and the possibility of adding an animation that contrasts walking and running. I also gave feedback about how player movement sometimes felt imprecise.

I received feedback on the player controls which helped inform the work I did during this sprint. We are now weighing the benefit of adding a second control method, as players on split on how aiming should be handled. We currently have aiming and movement on the same stick (left) but other players want the precision of aiming with the right stick. Because important actions are bound to the face buttons we think that dual stick controls would require rebinding some inputs, like jump, to the bumpers.

The first thing I did to fix a concern that I came across while playtesting the build was to add a deadzone to the left stick. This was because the player could slowly drift in a direction at the slightest disturbance of the stick, even if it appeared to be in a neutral position.

The next thing I did was to protoype mouse controls. I used a couple of games as a reference point for possible mouse control schemes. The first was Flinthook, which has a radius around the player that bounds the max distance of the aiming reticle. The other was Enter the Gungeon, where the reticle is able to be moved anywhere on the screen when using a mouse. Finally I considered how the game works now with a controller, the aiming dot moves in a circle with a fixed radius. 

The next thing I did was read the aiming code in the Player Controller to try to understand how it works. I also read some documentation and talked to other studio members to get an idea of how Unity's Input Action system works and how use the Input Map. Then after wrestling with the code and with vector math, I attempted to implement the different schemes. Not all of my efforts were entirely successful, but after Spring Break I hope to get some help figuring out how to get the aiming to work the way I want it to.
(Also I want to post some GIFs of the reference games and my prototypes but I haven't had access to a computer for the first half of break)

#Time Breakdown:
Meetings and Playtesting : 3hrs., Keyboard and Controller rebinding: 1hr, Mouse Control Prototypes: 8hrs.


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

Old (note ability to gain height jumping up one wall but not when jumping between two)
![Old](https://i.imgur.com/tTe9YcT.gif)

New (note that jumping between walls now gains height rather than jumping up one wall)
![New](https://i.imgur.com/dD3K0nY.gif)
