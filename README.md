# Tomb of Gurthaur
 A simple Roguelike created using the libtcod library: http://roguecentral.org/doryen/libtcod/
 
 
 Created using Roguebasin's complete roguelike tutorial: http://www.roguebasin.com/index.php?title=Complete_Roguelike_Tutorial,_using_python%2Blibtcod
 
 ChangeLog:  
 - v 1.4:
    - Room generation is now performed using the **Binary Space partitioning module(BSP)** included with the libtcod library. The dungeon's appearance can be changed by tweaking the value of the **FULL_ROOMS** constant:
        - A value of **True** will cause the rooms to fill their maximum node area. The dungeon will look more organized with no corridors.
        - Likewise, a value of **False** will create more natural dungeons with many corridors.
    - Added a **new icon** to the games executable file.
    (Credit for icon goes to Chanut is Industries(https://www.iconfinder.com/icons/2913098/creature_dragon_dragon_egg_egg_fantasy_monster_rpg_icon), used under Creative Commons license(https://creativecommons.org/licenses/by/3.0/legalcode))
    - Deleted the build folder as apparently it is only needed temporarily by py2exe for executable setup. 

 - v 1.3:
    - added the ability to create a binary executable of the game for Windows systems. The executable can be found as **Kings.exe** in the **dist** folder. Alternatively, you can build the binary yourself by running the **binary.py** file. 
 
 - v 1.2:
    - added a new **buff** system
        - Fighter class now has 5 new parameters; power_buff, defense_buff, hp_buff, buff_type and buff_charge
        - power_buff, defense_buff and hp_buff are buffs for power, defense and hp respectively, and are added to stats calculation for Fighter objects
        - buff_type provides the type of buff the fighter object currently has, or _None_ if the object is not buffed.
        - two new buff_types introduced: **'shield'** buff types lose buff_charge when the buffed object is attacked, while **'aura'** buff types lose buff_charge when the object moves. In both cases the buff is removed when buff_charge for that object hits 0
    - added a feature where the name of a spell/equipment that has not been picked up is *'??'* when the mouse is hovered over it. If the item is picked up and then dropped, the name of the item when hovered over is revealed.
    - added **scroll of Oakskin** spell which leverages new buff system; provides a 'shield' buff that increases the player's defense by 2. Lasts for 5 charges(5 hits from an enemy NPC)
    - added **helmet** equipment item; spawns at a lower level than the shield, increases defense by 1 when equipped. Equipped in the _head_ slot.
    - added prompt that tells the player to press X when standing on the stairs to go to the next level of the dungeon.
    - Minor grammar changes + QOL improvements
    
 - v 1.1:  
     - Added helmet item
     - Fixed bug where base hp, defense and power items were not associated with the player's stats; game would crash when player changes a stat during level up.
 - v 1.0: Initial commit 
