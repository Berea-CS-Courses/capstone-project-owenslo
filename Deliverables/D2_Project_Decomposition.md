# D2 Project Decomposition

 - NPCS: *Non-player characters. Without these, the rest of the components are useless. All the other components of this mod will rely on the NPCs.*
		 
	 - Follower: *A follower is a specific type of NPC that accompanies the player on their adventures. These are, by nature, more complex than other NPCs, since they are expected to travel along with the player and assist them in their journeys.*
	 - FaceGen: *Short for "Face Generation. This is a subsection for each specific NPC in the G.E.C.K., and it allows for each NPC's face and hair can be modified.*
 - Narrative: *The story of the mod. Before I can begin setting up scripted events, I need to write a story for the npcs to be a part of.*
	 - Quest: *This is where the story is implemented into the mod. The quest will handle certain encounters and how events in the story need to be handled and in what order they need to be handled. The quest making part of the mod will also contain the dialogue.*
		 - Dialogue: *The dialogue of the mod will contain responses from NPCs involved in the quest and the player's response to them, if any. Some scripting is also handled in this phase, but nothing that would need its own script file. The dialogue I will create will be specifically for the NPCs in this mod, and will be set up to make sure only the NPCs of this mod use it.*
			 - Voiced Dialogue: *Voiced dialogue is handled in the same part of the G.E.C.K. as written dialogue, so before I can add voiced dialogue, I have to create the quest and the dialogue for it. The G.E.C.K. allows for audio files to be called upon during in-game conversation, which is how voiced dialogue works via the GetIsID command. For example, if a line of dialogue has the command "GetIsID 000Mario = 1, the NPC with the editor ID 000Mario is allowed to use the dialogue and no other NPC can, since editor IDs are unique to the NPC/item they are prescribed to.*
 - Scripts: *The coding of the mod. The major scripting for the mod will be how the follower acts to specific commands, specifically the fire, hire, and wait commands.*
 
 
	 - Packages: *Packages are used to tell NPCs what to do, when to do it, and where to do it. The packages I am creating will rely on the script to know when to switch between packages.*
 - Faction: *Factions are used to allow NPCs to know how they should react to other NPCs in the game. For example, if faction 1 is set to be hostile to faction 2, members of faction 1 will attack members of faction 2. Conversely, if faction 1 is allied to faction 2, members of faction 1 will assist members of faction 2 in combat. If faction 1 doesn't have a listing for faction 2 in their faction tab, their relationship defaults to neutral, meaning they will neither attack nor assist each other, unless another faction they are allied or hostile with is involved.*


I have ordered the components by how I perceived their importance. All the pieces of my project interact with one another. All of the components rely on *Fallout: New Vegas* and the G.E.C.K.
