# Lethal Fashion

### Wanna find scrap, but do it in **style**? 
#### Have all outfits for free instead of wasting your money on them!

A very simple mod that shouldn't interfere with other mods or break them.

The following suits will be unlocked and available immediately:
1. Green Suit
2. Hazard Suit
3. Pajama Suit

ONLY works if you are the host.
Clients (non-hosts) do NOT need this mod at all, it syncs via the host.

## Credits
Please check out:  
- [Mom_Llama's Lethal Company Enhancer Mod](https://thunderstore.io/c/lethal-company/p/Mom_Llama/Lethal_Company_Enhancer/) (Does a lot of cool stuff and also has the option to unlock the green and hazard suits. They helped me with the initial version of this mod immensely.)  
- [x753's More Suits Mod](https://thunderstore.io/c/lethal-company/p/x753/More_Suits/) (Adds a lot more suits and is pretty advanced!)    

## Manual Installation

Simply place the LethalFashion.dll into your game folder's BepInEx/plugins folder. For example, mine looks like:
D:\SteamLibrary\steamapps\common\Lethal Company\BepInEx\plugins\LethalFashion.dll

I've heard issues with people installing with R2Modman - I don't use this so I'm unsure what the problem is. Just make sure to put the LethalFashion.dll wherever the BepInEx plugin folder is. R2Modman might have a different location it's loading from.

## Changelog

### ***1.0.4**
- Works with newest update out of the box as far as I can tell, nothing should break. If it breaks, please check the LC Modding Discord and leave a message in the Lethal Fashion thread and I'll look into it.
- Removed debug code so it spams the console logs less
- Added Manual installation notes to this README on where the DLL goes
- Apparently there's issues with my mod when you install with R2Modman but I think it's a folder location issue. Please see manual installation notes.

### **1.0.3**   
- Fixed mod page formatting  
- Fixed an issue where if you quit a game and then went back into it, it would spawn duplicates of the suits and could push other suits off the rack
- Added more error handling and debugging code to make my life easier

### **1.0.2**   
- Fixed the suit disappearing issue.  
- Added logic to prevent the suits from spawning multiple times.  
- Added logic to handle when the game resets the ship (on loss; when you don't meet the quota and get fired)  
- Added logic to unlock existing suits that were spawned and reposition them on the rack  

### **1.0.1**  
- Fixed the folder structure, should now work with mod installer. Sorry for the mistake!  

### **1.0.0**
- Initial version, code reworked from my old bad implementation using a much better method from Mama Llama.  