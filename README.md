<img width="960" height="179" alt="Wonder_Boy_in_Monster_World_Logo" src="https://github.com/user-attachments/assets/b7791c86-4401-4da5-b461-65f044178340" />

# Wonder Boy V (Boss Fix) v1.3

**Final boss patch for *Wonder Boy in Monster World* (Mega Drive / Genesis)**
by **Psicopompo**.

Restores the final boss fight in the western (UE) release to match the Japanese version: **no saw running across the floor and no conveyor belt pushing the player around**.

The lasers, their rail, the boss's armour and everything else **remain untouched**: they were already the same in both versions.

## What it changes

* **The saw does not appear.** The object is never created during the fight: it is not drawn, does not move and cannot hit the player.
* **The conveyor belt does not move and does not push the player.** Neither the animation nor the pushing effect remains.

The patch consists of 28 modified bytes in the game's code. Nothing else is added or removed: no graphics, text, tables or ROM size changes.

<img width="256" height="224" alt="Wonder Boy V (Boss Fix) v1 3-260918-172339" src="https://github.com/user-attachments/assets/562b82ea-51ca-4388-9c45-675903db3f43" />  <img width="256" height="224" alt="Wonder Boy V (Boss Fix) v1 3-260918-165818" src="https://github.com/user-attachments/assets/d41f0ce5-08d9-4748-bcdb-0db4d35e0c4c" /><br>
<sub>With and without the saw.</sub>

## What it does NOT change

* The lasers and their rail (they are also present in the Japanese version).
* The boss armour break animation (also present in the Japanese version).
* **The conveyor belt is still visible on the floor**, but remains stationary. Removing its graphics as well would require rebuilding the room's floor using the Japanese version's graphics, which would require examining that room in the Japanese release, where the floor is different. If anyone has a save file (or RetroArch savestate) at the final boss **in the Japanese version**, please share it. That would make it possible to investigate making the floor identical.

## Versions

The patch went through several versions because each fix uncovered something else. The history is included here in case anyone still has an older version:

* **v1.0** — the belt stopped moving visually, but still pushed the player.
* **v1.1** — the pushing was fixed during the fight, but it still occurred outside the fight.
* **v1.2** — the pushing was fixed at its source. However, the saw, while no longer being drawn, still existed and could still hit the player.
* **v1.3** — current version: the saw is properly disabled, and the belt neither moves nor pushes. **Use this version.**

## Files

Each version of the game has its own patch. There are two ROM versions: the original western release and the Spanish translation.

**Western ROM (UE)**

```
Wonder Boy V (Boss Fix) v1.3 (by Psicopompo).ips
Wonder Boy V (Boss Fix) v1.3 (by Psicopompo).bps
```

**Spanish ROM**

```
Wonder Boy V (Boss Fix) (ES) v1.3 (by Psicopompo).ips
Wonder Boy V (Boss Fix) (ES) v1.3 (by Psicopompo).bps
```

**IPS or BPS — which one should I use?** The **BPS** is recommended: it checks that the source ROM is the correct one and warns you if it is not. **IPS** does not perform any source check, but works equally well with the two ROM versions.

<img width="256" height="224" alt="Wonder Boy V (Boss Fix) v1 3-260918-170048" src="https://github.com/user-attachments/assets/caf3e435-d4bd-4f77-8e60-3a30ae94bd0e" /> <img width="256" height="224" alt="Wonder Boy V (Boss Fix) v1 3-260918-170007" src="https://github.com/user-attachments/assets/3e1246d4-0eb5-4836-a845-50465f6d4a81" />

## How to patch

With **Flips** (Windows, Linux, macOS), **Lunar IPS**, **MultiPatch** or any other patching tool:

1. Open the tool and choose “Apply Patch”.
2. Select the patch (.bps recommended).
3. Select your **unpatched** ROM (see checksums below).
4. Save the patched ROM.

With Flips, if you apply the wrong version of the patch (for example, the western patch to the Spanish ROM), it will warn you and refuse to patch it. That is the correct behaviour, not an error.

## Checksums

**Unpatched western ROM** (use this with the western patch)

```
Wonder Boy in Monster World (UE).bin          786,432 bytes
MD5     1391725cc50671be68fc9dd405e19ac8
CRC32   93153413
SHA-1   481c0a3a61607cefc642992cd3faa18974834c94
```

**Unpatched Spanish ROM** (use this with the Spanish patch)

```
Wonder Boy in Monster World (es).bin          786,432 bytes
MD5     4cd028dfcb2a4602ee6f6f3c13a28092
CRC32   4EC0A307
SHA-1   09bc1f04fa163459b780de65e4a55060791ed7b3
```

**Result with the western patch applied**

```
MD5     fa6d35457c9f3418be588c93379d3ff3
CRC32   8340E9FE
SHA-1   99f601d285dcfb7e0077a72bea59ae889954ea01
```

**Result with the Spanish patch applied**

```
MD5     a8c317d6fb7c70d3c53acb7328c830a7
CRC32   5E957EEA
SHA-1   6418d68ea27e2fa21a81fb8911146c44e38eba1a
```

## Notes

* The patch does not touch anything outside the boss room: when starting the game from scratch, the patched ROM and the original are pixel-for-pixel identical.
* The patch can be applied to a game already in progress; the changes become apparent when entering the boss room.
* If you test with a savestate made **inside the fight** using the unpatched ROM, the saw has already been created and stored in the savestate. Enter the room through normal gameplay (or from a regular save) to see the patch working correctly.

## Credits

* Patch and testing: **Psicopompo**.
* Spanish ROM translation: **Jackic**.
* *Wonder Boy in Monster World* is © **Sega** and **Westone**. This patch contains no copyrighted files, only instructions for modifying your own copy.
