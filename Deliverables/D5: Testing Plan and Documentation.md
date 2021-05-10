# D5: Testing Plan and Documentation

0. I want to use this space to add references to the community fixes I'm using to get the game to work well. THESE FIXES DO NOT DIRECTLY EFFECT MY PROJECT, THEY ONLY EFFECT THE GAME ITSELF.

xNVSE- https://github.com/xNVSE/NVSE
NVAC- https://www.nexusmods.com/newvegas/mods/53635
NVTF- https://www.nexusmods.com/newvegas/mods/66537
Mod Limit Fix- https://www.nexusmods.com/newvegas/mods/68714

1. a) I plan on conducting the ad hoc and unit testing tests.
   b) These tests are best suited for my project because my project relies on usability and proper system intergration. The ad hoc testing will allow other players to attempt to play and find issues with my project while unit testing will make sure that all of the dialogue and quest scripting plays out as wanted.
2. My objectives with these tests are as follows: For unit testing, I want to make sure that the quest, scripting, and dialogue work as intended. To do that, I must interact with the NPCs, their scripting, and quest objectives to insure they work as intended. For ad hoc testing, I want the player to be able to complete the quest and be able to use Mario as a companion, regardless of any encountered bugs. Of course, I will encourage my testers to attempt to break my project so I can fix it.
3. Tests
# Unit Testing

## Dialogue
The major testing I had to do in this category was related to the dialogue for the optional objectives, doing chores for Ryle and returning items to him. When I initially created these dialogue options, the dialogue would appear before the quest was started, as long as you had the items Ryle wanted. You could also reaccess the dialogue after completing the objective tied to it. After verifying this bug in the game, I went back into the tool and added the proper conditionals for the dialogue options to get them to show up when necessary. Unfortunately, this means that these optional objectives must be done in a linear fashion, otherwise the aforementioned issues resurface. To make sure that the objectives can't be completed repeatedly, I have set conditionals that checks to see if the items are already present in Ryle's inventory.

Initially with some of Mario's dialogue pertaining to his companion functions, they did not act as intended. For example, when I would hire Mario, he would not switch to the hired package. This was remedied by adding "set MarioQuest.Status to 1" and "MarioREF.evp" to the dialogue's result script. The line "set MarioQuest.Status to 1" changes the Mario Quest's status to one, the variable it needs to be to set Mario to his "hired" AI package. "MarioREF.evp" tells Mario in the game to check which AI package he is using, since evp stands for evaluate script package. I followed this process for Mario's waiting and fired dialogue as well.


