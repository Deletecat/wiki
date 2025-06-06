---
lang: hu-HU
layout: faq
section: twilightmenu
title: GYIK & hibaelhárítás
long_title: TWiLight Menu++ GYIK & hibaelhárítás
description: TWiLight Menu++ GYIK és hibaelhárítás
---

További GYIK-ért látogassa meg a [GBAtemp üzenetszálat](https://gbatemp.net/threads/ds-i-3ds-twilight-menu-gui-for-ds-i-games-and-ds-i-menu-replacement.472200/).
{:.alert .alert-info}

#### Miért történik, hogy a 3DS eszközöm, fekete képernyőn ragad, összeomlik, kikapcsol, stb. amikor elindítom a TWiLight Menu++-t?
A TWL_FIRM elképzelhető, hogy valahogy megsérült. Kövesd ezt az útmutatót a hiba javításához: <https://3ds.hacks.guide/troubleshooting#dsi--ds-functionality-is-broken-after-completing-the-guide>

#### Hogyan javítom, ha fehér képernyőt kapok a TWiLight Menu++ bootolásakor?
- Indítsd újra a konzolt
- Ha ez nem működik, formázd az SD kártyádat FAT32-re 32 KB cluster/foglalási mérettel
    - Tekintsd meg a [dsi.cfw.guide oldalt](https://dsi.cfw.guide/sd-card-setup.html) az ajánlott eszközökért
- Ha ez sem működik, próbálj egy másik SD kártyát

#### Hogyan javíthatom, ha az érintő képernyő nem működik egy játék indítását követően?
- Ha cartridge-et futtatsz, legyél biztos benne, hogy `Slot-1 Érintés mód` `DS mód`-ra beállított
- Ha a probléma továbbra is fennáll, vagy ha ROM-ot használsz helyette, akkor kövesd ezt az útmutatót: https://gbatemp.net/threads/recover-ds-mode-after-an-nvram-brick-eg-after-using-a-ds-bricker.516444/

#### Hogyan javítom azt, ha a TWiLight Menu++ újraindul, vagy Guru Meditation Error hibát ad, amikor egy játékot indítok?
Menj a TWLMenu++ beállításaiba és kapcsold ki a `Utoljára játszott lista frissítés` opciót.

#### Miért kapok fehér képernyőt, ha megpróbálok betölteni egy DS játékot az SD kártyáról?
Lásd a [Problémáim vannak a ROM(ok)-mal, mit tegyek?](../nds-bootstrap/faq?faq=im-having-issues-with-my-roms-what-should-i-do) fejezetet az nds-bootstrap GYIK oldalon.

#### Hogyan használhatom a csalásokat?
Szükséged van egy csalás adatbázisra a `usrcheat.dat` fájl formájában, az `sd:/_nds/TWiLightMenu/extras/` mappában. A leginkább frissített csalás adatbázis [DeadSkullzJr NDS(i) Cheat Databases](https://gbatemp.net/threads/488711/) adatbázisa.
- A 3DS-en az az adatbázis elérhető az Universal Updater appban, mint "NDS(i) Cheat Databases". Ez automatikusan telepíti azt a szükséges helyre.

Alternatívaként használhatod az [r4cce](https://web.archive.org/web/20241130133125/http://hp.vector.co.jp/authors/VA013928/soft_en.html)-t, hogy létrehozd a saját csalás adatbázisod.

Ha már van cheat DB-d, akkor a csalásokat a TWiLight menüben a <kbd class="face">Y</kbd> megnyomásával engedélyezheted, ami a játékonkénti beállításokat nyitja meg, majd a <kbd class="face">X</kbd> gombbal nyitohatod meg a csalások menüt.

#### Hogyan jelenítek meg egy egyedi képet a felső képernyőn a DSi témában? El is rejthetem helyette?
Egy véletlen `.png` kép az `sd:/_nds/TWiLightMenu/dsimenu/photos/` mappából kerül megjelenítésre minden alkalommal, amikor a menü betöltésre kerül. Ha nincsennek használható képek, akkor az nds-bootstrap által készített képernyőképek kerülnek felhasználásra.

- A kép(ek) felbontása nem lehet nagyobb, mint 208x156
- Ha hibát tapasztalsz, az leginkább a képméret hiba. Használd a [tinypng](https://tinypng.com)-t a méret csökkentéséhez

A kép elrejtéséhez a `theme.ini` fájlt kell szerkesztened, amely a `sd:/_nds/TWiLightMenu/dsimenu/themes/[téma mappa]/` mappában található. Nyisd meg a fájlt egy szövegszerkesztővel, módosítsd a `RenderPhoto` sort `1` -ről `0-ra`, majd mentsd el a fájlt.

#### Hogyan szerezhetek játékokat?
Homebrew játékokat az [Universal-DB](https://db.universal-team.net/ds)-ből és a [GameBrew](https://www.gamebrew.org/wiki/List_of_all_DS_homebrew#Games)-ról tölthetsz le. Ahhoz, hogy hivatalosan kiadott játékot szerezz, dump-ként kell azokat beszerezned vagy egy fizikai cartridge-ről, vagy egy másik konzolról:
- DS-en használhatod a [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases)-t a GBA játékaid dumpolásához, illetve ha van Slot-2 flashcart-od, DS játékokra. Ha csak Slot-1 flashcard-od van és szeretnél dumpolni egy DS játékot, használhatod a [Wooddumper](https://digiex.net/attachments/wooddumper_r89-zip.14735/)-t, amihez szükség van egy Wi-Fi kompatibilis DS-re és egy FTP kliensre egy független eszközön a ROM fogadásához
- DSi-n használhatod a [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases)-t a DS játékaid és a DSiWare dumpolásához
- 3DS-n használhatod a [GodMode9](https://github.com/d0k3/GodMode9/releases)-t a DS játékaid, DSiWare és Virtual Console címek dumpolásához

#### A játék kártyákból a mentéseimet ki tudom rakni az SD kártyámra és visszafelé?
Igen. Használhatod erre a [Checkpoint](https://github.com/FlagBrew/Checkpoint/releases)-ot 3DS-en vagy a [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases) DSi-n / 3DS-en.

#### Hogyan állítom be a TWiLight Menu++-ban a nyelvet?
1. Nyisd meg a TWiLight Menu++ beállításokat, ezt a <kbd>SELECT</kbd> gomb nyomvatartásával tudod megtenni, a TWiLight Menu++ betöltésekor
1. Módosítsd az első opciót, amíg nem látod a nyelvet, amit szeretnél, majd lépj ki a beállításokból
    - Elképzelhető, hogy módosítanád az első három opciót, az nds-bootstrap beállítások oldalon, ami a DS játékok és címeik nyelvét és régióját befolyásolja a a TWiLight Menu++-ban

#### Ez egy DS(i) emulátor?
Nem, ez nem egy emulátor. A menü és a DS játékok (nds-bootstrap-en keresztül betöltve) natívan futnak a konzol DS/DSi módjában. Csak a korábbi idők konzoljai kerülnek emulálásra, illetve részben a GBA (mivel egy része vagy az összes, mint például a grafika natívan fut).

#### Milyen rendszereket támogat a TWiLight Menu++?
Tekintsd meg [TWiLight Menu++ által támogatott rendszerek listáját](../ds-index/emulators#list-of-supported-systems-by-twilight-menu).

#### A Slot-1 játékok exploitjai be tudják tölteni TWiLight Menu++-t?
Nem. Az SD kártyához hozzáférés csak a DSiWare alkalmazások számára biztosított, így a Slot-1 játékok nem tudják elindítani (vagy egyáltalán elérni) a TWiLight Menu++-t.

#### Miért nem találom/látom a játékaimat?
Több oka lehet, hogy nem találod őket.
- Az `_nds` mappa, amely az SD kártya gyökerében található, nem a TWiLight Menu++ segítségével elérhető alkalmazások számára készült, mivel a mappa a funkcionalitáson alapuló fájloknak (témák, konfiguráció, képek, emulátorok stb.) fenntartott. Ha ide raktad a címeid, kérjük, helyezd át őket egy másik helyre.
- Ha több mint 39 játékod van egy mappában és minden slot a menüben foglalt a játékod lehet, hogy a következő oldalon van. Használd az <kbd class="l">L</kbd>/<kbd class="r">R</kbd> vagy <kbd>SELECT</kbd> + <kbd>Bal</kbd> /<kbd>Jobb</kbd> gombokat az oldalak lapozásához
- Ha a játék mappád láthatatlan, be kell kapcsolnod a láthatatlan fájlok megjelenítését a TWiLight Menu++'s GUI beállításai között
- Ha a játékod egy archív fájlban van (`zip`, `rar`, `7z`, stb.), nem használható a TWiLight Menu++ által. Csomagold ki a játékot az archívumból a használatához
- Ha a játékod nem a [támogatott kiterjesztéseket](../ds-index/emulators#list-of-systems-supported-by-twilight-menu) használja, szükséges lehet, hogy módosítsd a kiterjesztést a fájl átnevezésével

#### Hogyan érem el a TWiLight Menu++ beállításait?
A TWiLight Menu++ beállításainak elérési módja a konfigurációtól függő.
- **DS Classic Menu:** Éríntsd meg a DS ikont a az alsó képernyő alján
- **Nintendo DSi/SEGA Saturn/Homebrew Launcher témák: a SELECT Menu használatával:** Nyomd meg a <kbd>SELECT</kbd> gombot, majd indítsd el a Beállítások Applet-et (használd a D-PAD-et az opciók kijelöléséhez)
- **Nintendo DSi/SEGA Saturn/Homebrew Launcher témák, amik nem használják a SELECT Menu-t:** A <kbd>SELECT</kbd> megnyomása a DS Classic Menu-be visz
- **Nintendo 3DS téma:** Érintsd meg a csavarkulcs ikont az alsó képernyőn
- **R4 Eredeti téma:** Nyomd meg a <kbd>START</kbd> gombot (ha a fájlböngészőben vagy), majd nyomd meg a <kbd>SELECT</kbd> gombot
- **Wood UI téma:** A <kbd>START</kbd> gomb megnyomása a DS Classic Menu-be visz

Továbbá nyomva tarthatod a <kbd>SELECT</kbd> gombot a TWiLight Menu++ indításakor, ami közvetlenül a beállításokhoz visz.

#### Hagyan használhatok egyéni ikonokat/bannereket a játékokhoz?
Egyedi bannereker PNG vagy DS banner.bin formátumban úgy használhatsz, hogy berakod az `sd:/_nds/TWiLightMenu/icons` mappába a ROM vagy a mappa nevén (beleértve a kiterjesztést) + `.png` vagy `.bin`.

A PNG bannerekhet egy PNG fájlra van szükséged 15 vagy kevesebb színnel és maximum 32x32 felbontással. A teljes átlátszóság működik, és nem számít bele a 15 színbe, de a félig átlátszóság nem működik.

A banner.bin típusú bannerek animálhatók, és lehetővé teszik a TWiLight Menu++-ban megjelenő cím cseréjét. Ezek létrehozhatók az [NDS Banner Editor](https://github.com/TheGameratorT/NDS_Banner_Editor/releases) segítségével.

Előre lekésztett bannerek találhatók az [ikonok szekciójában a TWiLight Menu++ témák oldalon](https://skins.ds-homebrew.com/icon/) és ha készítesz egyet, azok meg is oszhatók ott.

#### Hogyan telepítek egyéni témákat a TWiLight Menu++-ba?
Egyedi szkinek a témákhoz beszerezhetők [a hivatalos téma oldalról](https://skins.ds-homebrew.com/), amely számos közösségi készítésű témának ad otthont felhasználásra készen. Egyedi témákat is készíthetsz a Nintendo 3DS és Nintendo DSi témákhoz [ezen útmutató](https://wiki.ds-homebrew.com/twilightmenu/custom-dsi-3ds-themes) alapján. A **Homebrew Launcher**, a **Sega Saturn** ésd **Game Boy Color** témák _**nem**_ módosíthatók.

Miután beszereztél egy egyéni témét, telepíteni úgy tudod, hogy a megfelelő útvonalra rakod, ami függ attól, hogy az melyik felülethez készült a téma.
- A témák a Nintendo DSi felülethez az `sd:\_nds\TWiLightMenu\dsimenu\themes\` mappába kell kerüljenek
- A témák a Nintendo 3DS felülethez az `sd:\_nds\TWiLightMenu\3dsmenu\themes\` mappába kell kerüljenek
- A témák az R4 Original felülethez az `sd:\_nds\TWiLightMenu\r4menu\themes\` mappába kell kerüljenek
- A témák a Wood felülethez az `sd:\_nds\TWiLightMenu\akmenu\themes\` mappába kell kerüljenek

Ha a 3DS csláadba tartozó konzolt használsz, az egyedi témák telepíthetők az [Universal-Updater](https://github.com/Universal-Team/Universal-Updater/releases) használatával. Menj az Universal-Updater beállításaiba, majd `UniStore választás...`, `+`, `TWiLight Menu++ Themes`.

Az egyedi témák beállításához hozzá kell férned a TWiLight Menu++ beállításaihoz.
1. A `GUI beállítások` oldalon navigálj a `Felhasználói felület` opcióhoz, majd válaszd ki a témát a D-Pad bal és jobb gombjával.
1. Ha a cél felület kiválasztásra került, menj az `Egyéni téma`opcióhoz, majd nyomd meg az A gombot, hogy választhass a telepített témák közül.
1. A D-Pad fel-le gombjaival jelöld ki a kívánt témát, majd nyomd meg az A gombot a kiválasztásához.
1. Alkalmazd a beállításokat a B gomb megnyomásával és hogy vissza kerülj a TWiLight Menu++-ba.

A TWiLight Menu++-nak mostantól egyéni megjelenést (és zenét, ha a kiválasztott téma támogatja és engedélyezve van a beállításokban) kell kapnia.

#### Van 3DS emulátor a DS(i)-re?
Nem, nincs. A 3DS-t nem lehet emulálni a DS(i)-en, mivel a 3DS újabb hardvert használ.
