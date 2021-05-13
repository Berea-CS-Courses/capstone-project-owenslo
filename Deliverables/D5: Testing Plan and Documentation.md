# D5: Testing Plan and Documentation

0. I want to use this space to add references to the community fixes I'm using to get the game to work well. THESE FIXES DO NOT DIRECTLY EFFECT MY PROJECT, THEY ONLY EFFECT THE GAME ITSELF.

xNVSE- https://github.com/xNVSE/NVSE
NVAC- https://www.nexusmods.com/newvegas/mods/53635
NVTF- https://www.nexusmods.com/newvegas/mods/66537
Mod Limit Fix- https://www.nexusmods.com/newvegas/mods/68714

1. a) I plan on conducting the ad hoc and unit testing tests.
   b) These tests are best suited for my project because my project relies on usability and proper system intergration. The ad hoc testing will allow other players to attempt to play and find issues with my project while unit testing will make sure that all of the dialogue and quest scripting plays out as wanted.
2. My objectives with these tests are as follows: For unit testing, I want to make sure that the quest, scripting, and dialogue work as intended. To do that, I must interact with the NPCs, their scripting, and quest objectives to insure they work as intended. For ad hoc testing, I want the player to be able to complete the quest and be able to use Mario as a companion, regardless of any encountered bugs. Of course, I will encourage my testers to attempt to break my project so I can fix it.
3. Tests:

# Unit Testing

## Dialogue
The major testing I had to do in this category was related to the dialogue for the optional objectives, doing chores for Ryle and returning items to him. When I initially created these dialogue options, the dialogue would appear before the quest was started, as long as you had the items Ryle wanted. You could also reaccess the dialogue after completing the objective tied to it. After verifying this bug in the game, I went back into the tool and added the proper conditionals for the dialogue options to get them to show up when necessary, with the conditionals being tied to if the stage of the quest was the one the dialogue satisfied (the dialogue to return an item is only available during the stage when the player is asked to return it). Unfortunately, this means that these optional objectives must be done in a linear fashion, otherwise the aforementioned issues resurface. To make sure that the objectives can't be completed repeatedly, I have set conditionals that checks to see if the items are already present in Ryle's inventory. I have done this process, or at least one similar, with all the dialogue that involved conditionals.

Initially with some of Mario's dialogue pertaining to his companion functions, they did not act as intended. For example, when I would hire Mario, he would not switch to the hired package. This was remedied by adding "set MarioQuest.Status to 1" and "MarioREF.evp" to the dialogue's result script. The line "set MarioQuest.Status to 1" changes the Mario Quest's status to one, the variable it needs to be to set Mario to his "hired" AI package. "MarioREF.evp" tells Mario in the game to check which AI package he is using, since evp stands for evaluate script package. I followed this process for Mario's waiting and fired dialogue as well.

## Scripting/Packaging
There are two major scripts in this mod, the one that handles variables that set which AI package Mario is supposed to use and the one that manages the initial meeting between Mario and the player. For both scripts, the tool will not let you compile a script that is syntactically incorrect, so the scripts had to be correct in that way. Attaching the scripts to what they need to be attached to is a different beast.

When creating the script that handles Mario's AI packages, the proper variable had to be set as a conditional for all three of the major AI packages (hired, fired, waiting). Some of my initial issues with hiring Mario were related to not having the correct variables assigned to the correct packages, meaning that you could select the dialogue to fire Mario and he would start following you. This was fixed by changing the variables to the correct ones in the conditional statements in the AI packages. This script also needed to be added to the correct quest, which was done via drop-down menu in the quest's menu.

For the script that manages Mario's initial interaction with the player, it had to be associated with an object called an "activator." Once the script was created, I attached the script to an activator. When I tried to add the activator to the game, I found that I could not. This was because I was trying to copy and paste a preexisting activator, standard practice for many other objects in the GECK. This, of course, did not work in-game. I had to manually create a new activator, called "000MarioDialogueTrigger," and add the script, named "MarioTriggerScript," to the activator. After this, I was able to add and manipulate the activator in the tool. This was shown in a screenshot in the D4 document, along with the scripts I have been mentioning. After I went through the process this way. I was able to get the activator to work, meaning that Mario approaches the player and asks for help. One side effect of this is that Mario will continue to follow the player until they have the initial dialogue Mario is programmed to have with the player. This means that Mario will continuously follow the player until that dialogue is had.


# Ad Hoc Testing

For my ad hoc testing, I had two different people, Brian Cox and Cora Wright, play test my project. Since Brian has played the game before, I tasked him with finding any bugs or issues that he could while playing the mod to completion. This is so I can see how a veteran player would play through my mod and also to document any bugs or issues found in my project. Since Cora has never played the game before, I wanted them to play the quest of the mod how they naturally would. This is so I can have a gauge of how a new player might approach my project. I have linked the videos to both of the recordings below.

https://youtu.be/zoAGoz7w4oU

https://www.youtube.com/watch?v=5ZJ5sVAbk-0



