---
lang: pl-PL
layout: wiki
section: ds-index
category: reference
title: Emulatory na DS
description: Zbiór różnych emulatorów na DS
---

Istnieje wiele emulatorów dla DS i DSi. This page provides a comprehensive explanation on the many emulators and loaders bundled into **TW**i**L**ight Menu++.

### Lista systemów obsługiwanych przez TWiLight Menu++

| Format                    | Loader                                           | Rozszerzenia                           | Plik zapisu                                                                |
| ------------------------- | ------------------------------------------------ | -------------------------------------- | -------------------------------------------------------------------------- |
| ARGV[^1]                  | Natywny                                          | `.argv`                                |                                                                            |
| Atari 2600                | [StellaDS][stellads]                             | `.a26`                                 |                                                                            |
| Atari 5200                | [A5200DS][a5200ds]                               | `.a52`                                 |                                                                            |
| Atari 7800                | [A7800DS][a7800ds]                               | `.a78`                                 |                                                                            |
| Atari XEGS                | [A8DS][a8ds]                                     | `.xex`, `.atr`                         |                                                                            |
| ColecoVision              | [S8DS][s8ds], [ColecoDS][colecods]               | `.col`                                 |                                                                            |
| DS                        | [nds-bootstrap][ndsbs], flashcard kernel, native | `.nds`, `.dsi`, `.ids`, `.srl`, `.app` | `saves/[nazwa romu].sav`[^2]                                               |
| DSiWare                   | [Unlaunch][unlaunch], [nds-bootstrap][ndsbs]     | `.nds`, `.dsi`, `.ids`, `.srl`, `.app` | `saves/[rom name].pub`, `saves/[rom name].prv`, `saves/[rom name].sav`[^7] |
| DSTWO Plugin              | [DSTWO][dstwo][^3]                               | `.plg`                                 |                                                                            |
| Game Boy (Color)          | [GameYob][gameyob]                               | `.gb`, `.sgb`, `.gbc`                  | `[nazwa romu].sav`                                                         |
| Game Boy Advance          | [GBARunner2][gbarunner2][^4], native[^5]         | `.agb`, `.gba`, `.mb`                  | `[nazwa romu].sav`                                                         |
| Game Gear                 | [S8DS][s8ds]                                     | `.gg`                                  | `[nazwa romu].gg.sav`                                                      |
| Genesis / Mega Drive      | [jEnesisDS][jenesis], [PicoDriveTWL][pdtwl]      | `.gen`, `.md`                          | `[rom name].srm`[^6]                                                       |
| Intellivision             | [Nintellivision][nintellivision]                 | `.int`                                 |                                                                            |
| Master System             | [S8DS][s8ds]                                     | `.sms`                                 | `[nazwa romu].sms.sav`                                                     |
| MSX                       | [ColecoDS][colecods]                             | `.msx`                                 | ???                                                                        |
| Neo Geo Pocket (Color)    | [NGPDS][ngpds]                                   | `.ngp`, `.ngc`                         | `/data/ngpds/[nazwa romu].ngp.fla`                                         |
| FastVideoDS               | [FastVideoDSPlayer][fastvideodsplayer]           | `.fv`                                  |                                                                            |
| NES / Famicom             | [nesDS][nesds]                                   | `.nes`, `.fds`                         | `[nazwa romu].sav`                                                         |
| PC Engine / TurboGrafx-16 | [NitroGrafx][nitrografx]                         | `.pce`                                 |                                                                            |
| Rocket Video              | [Rocket Video Player][rvidplayer]                | `.rvid`                                |                                                                            |
| SG-1000                   | [S8DS][s8ds], [ColecoDS][colecods]               | `.sg`                                  |                                                                            |
| Sord M5                   | [ColecoDS][colecods]                             | `.m5`                                  |                                                                            |
| SNES                      | [SNEmulDS][snemulds]                             | `.smc`, `.sfc`                         | `[rom name].srm`[^8]                                                       |
| WonderSwan (Color)        | [NitroSwan][nitroswan]                           | `.ws`, `.wsc`                          | ???                                                                        |
| Xvid                      | [tuna-viDS][tunavids]                            | `.avi`                                 |                                                                            |

To są tylko rekomendowane emulatory i loadery, które są również dostępne w TWiLight Menu++. Istnieją także inne emulatory dostępne dla tych konsol (np. lolSnes, Gbaemu4ds itp.)

### Inne emulatory dla DS

| Format  | Loader         | Rozszerzenia | Plik zapisu |
| ------- | -------------- | ------------ | ----------- |
| Neo Geo | [neoDS][neods] | `.neo`       | (nieznane)  |

### BIOS usage

| Format              | Loader                               | Path             | Required  |
| ------------------- | ------------------------------------ | ---------------- | --------- |
| Game Boy (Color)    | [GameYob][gameyob][^9]               | User-set         | No        |
| Game Boy Advance    | [GBARunner2][gbarunner2], native[^5] | `/_gba/bios.bin` | See [^10] |
| Famicom Disk System | [nesDS][nesds]                       | `/disksys.rom`   | Yes       |

- Footnotes -
{:footnotes}

## Uwagi dotyczące niektórych emulatorów

### Ramdyski
- In order for **jEnesisDS**, **SNEmulDS** (legacy version), or **neoDS** to work on the DSi SD card, you'll have to use a RAM disk with nds-bootstrap
    - A RAM disk maker for jEnesisDS and SNEmulDS (legacy version) is built into nds-bootstrap. Dla neoDS trzeba stworzyć ramdysk własnoręcznie. Zaglądnij do [Tworzenie Ramdysków](../twilightmenu/creating-ram-disks), żeby się dowiedzieć jak to zrobić
    - Potrzeba użycia ramdysków dla tych emulatorów, wynika z tego, że ich hooki ARM7 nie działają poprawnie

### Porównanie pomiędzy PicoDriveTWL i jEnesisDS
- **PicoDriveTWL**
    - Został stworzony dla DSi
    - Nie wymaga ramdysków nds-bootstrap
        - Jest obsługiwany zapis na karcie SD DSi
        - Szybsze czasy ładowania między TWiLight Menu++ a emulatorem na karcie SD DSi
    - Obsługuje argumenty
    - Limit is 3 MB on a **Flashcard**
        - Takes advantage of the DSi extra RAM or DS Memory Expansion Pak to extend this limit
    - Brak emulacji dźwięku
    - Niska ilość klatek na sekundę

- **jEnesisDS**
    - DS Mode
        - Wymaga ramdysku nds-bootstrap, by był używany na karcie SD DSi
        - Zapisywanie jest niedostępne dla kart SD DSi
    - Trochę długo się ładuje
    - Brak wsparcia argumentów
    - Limit wynosi 3 MB na wszystkich platformach (romy są ładowane do pamięci RAM)
        - No DS Memory Expansion Pak or DSi Extended Memory support
        - There is a patch for *Sonic 3 & Knuckles* that removes the multiplayer, getting the size count down
    - Emulacja dźwięku
    - Wysoka ilość klatek na sekundę


<!-- Links for tables -->
[^1]: Text files containing the path to a DS homebrew app and arguments to launch it with, see [nds-hb-menu's README](https://github.com/devkitPro/nds-hb-menu#passing-arguments) for more info
[^2]: Only for retail ROMs, homebrew do not have specific save files
[^7]: Only when running in B4DS mode
[^3]: Only works from a SuperCard DSTWO flashcard as it has additional processing power and RAM inside the flashcard
[^4]: When running in DSi Mode, it can use the DSP for better sound
[^5]: Requires a Slot-2 flashcart and thus only works on DS Phat and DS Lite
[^6]: jEnesis can only save when running from a flashcard, but PicoDriveTWL can save from SD and flashcard
[^8]: Saving requires a flashcard or a new version of the emulator (legacy version is used by default)
[^9]: Has a bug where the BIOS screen is not shown when starting a game via arguments
[^10]: Not required for native, required for a few games with GBARunner2, required for all games with GBARunner3

[a5200ds]: https://github.com/wavemotion-dave/A5200DS
[a7800ds]: https://github.com/wavemotion-dave/A7800DS
[a8ds]: https://github.com/wavemotion-dave/A8DS
[colecods]: https://github.com/wavemotion-dave/ColecoDS
[dstwo]: http://eng.supercard.sc
[fastvideodsplayer]: https://github.com/Gericom/FastVideoDSPlayer
[gameyob]: https://github.com/Drenn1/GameYob
[gbarunner2]: https://github.com/Gericom/GBARunner2
[jenesis]: https://www.gamebrew.org/wiki/JEnesisDS
[ndsbs]: https://github.com/DS-Homebrew/nds-bootstrap
[nesds]: https://github.com/DS-Homebrew/NesDS
[ngpds]: https://github.com/FluBBaOfWard/NGPDS
[nitrografx]: https://www.gamebrew.org/wiki/NitroGrafx
[nitroswan]: https://github.com/FluBBaOfWard/NitroSwan
[pdtwl]: https://github.com/DS-Homebrew/PicoDriveTWL
[rvidplayer]: https://gbatemp.net/threads/539163
[s8ds]: https://github.com/FluBBaOfWard/S8DS
[snemulds]: https://www.gamebrew.org/wiki/SNEmulDS
[stellads]: https://github.com/wavemotion-dave/StellaDS
[unlaunch]: https://problemkaputt.de/unlaunch.htm
[neods]: https://www.gamebrew.org/wiki/NeoDS
[nintellivision]: https://github.com/wavemotion-dave/NINTV-DS
[tunavids]: https://github.com/chishm/tuna-vids
