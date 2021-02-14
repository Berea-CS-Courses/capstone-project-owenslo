# Project Specification Document

## Overview

The intent of this project is to create a Mario Nakazawa as an interactive companion in *Fallout: New Vegas* with voice acting and a quest. The purpose is to fill a void that there is in when it comes to what kind of companions are available in *Fallout: New Vegas* and the modding community around the game. I would also like to test and expand my skills that I have been gaining during my tenure as a student at Berea College. This will all be possible thanks to the **Garden of Eden Creation Kit**, or **G.E.C.K.**, and all the access and opportunities the tool provides when it comes to adding or changing things in the game.

## Concepts

The scope of this project is to create a NPC in *Fallout: New Vegas* that serves as a quest giver an interactive companion. The companion will resemble, to the best of my abilities and the face design tool's ability, the person the companion is based on. The companion will give a fully functional quest that will involve finding items and giving them to the correct people for the benefit of the player and quest giver. The companion will have dialogue for all of their lines. The scripting for the companion will be able to switch between three different companion states: hired, fired, and waiting. The companion will be able to detect when they are in specific areas, so they can give comments about what they think of the area. The companion should be given a "faction," an identifier that manages who is a member of what group and how that group should interact with other groups, on a scale of "hostile," "neutral," "friendly," and "ally," from worst to best. That faction should be considered a "friend" or "ally" to the player faction. The companion will have their own faction as a way to circumvent potential bugs I have encountered from directly adding NPCs to the player faction, like helping anyone who was a member, ally, or friend of the player faction instead of just helping the player.

Outside of the scope would be making this available for the console versions of *Fallout: New Vegas*, as modding is only officially supported for the PC version of the game. Modifying the game's central story is also out of scope, since there would be hundreds of scripts, NPCs, dialogues, and quests that would also need altered.

## Software Requirements Specification

 - Software must keep track of state of companion (hired, fired, waiting)
 - Software must work with PC version of *Fallout: New Vegas*
 - Software must track current state of companion quest (in progress, completed, failed)
 - Software must feature a working companion system
 - Software must take into account companion location
 - Software must be able to access and play audio files on command
 - Software must contain a companion who resembles who they are modeled after
 - Software must allow the companion's faction to be considered a "friend" or "ally" of the player faction.

