# THERAPIOTEON JAVA — hlavní plán projektu

## Základní pravidla
- Hra se jmenuje THERAPIOTEON JAVA.
- Veškeré rozhraní hry je česky.
- Hráči se nepřihlašují: žádný účet, heslo, e-mail ani registrace.
- Hráč si pouze zvolí herní jméno. GitHub slouží jen k vývoji a hráči ho nikdy nepotřebují.
- macOS není podporovaný.
- Cílové platformy: Windows PC, Android, iPhone, podporované konzole a Meta Quest 3S. Každá platforma potřebuje vlastní kompatibilní sestavení; dostupnost se nesmí předstírat.

## Hlavní nabídka
- THERAPIOTEON JAVA, pole „Tvoje herní jméno“.
- Tlačítka: HRA JEDNOHO HRÁČE, HRA VÍCE HRÁČŮ, NASTAVENÍ, UKONČIT HRU.
- Herní jméno lze změnit v nastavení.

## Režim 1: Hra jednoho hráče
- Vytvořit nový svět nebo načíst uložený svět.
- Nastavit název světa, obtížnost (Mírumilovná, Lehká, Normální, Těžká) a režim (Survival nebo Creative).
- Samostatné volby pro povolení příkazů a chatu podle nastavení hráče.
- Po potvrzení se svět načte; singleplayer má po instalaci fungovat offline.
- Světy se ukládají a lze je znovu načíst, přejmenovat či smazat. Při smazání zobrazit přesně: „Tento svět byl smazán.“

## Režim 2: Hra více hráčů
- Sekce FRIENDS: přátelé, žádosti a pozvánky.
- Vytvoření nebo připojení ke sdílenému světu.
- Při vytváření světa hostitel nastaví název, obtížnost, Survival/Creative a povolení příkazů a chatu.
- Skutečný multiplayer vyžaduje backend, síťovou synchronizaci, bezpečnou identitu hráče a hosting. Herní jméno není ověřená identita; unikátní ID a rezervace jména musí řešit server.
- Zprávy a oznámení o připojení/odpojení se zobrazují jen při skutečných událostech.
- Vlastní servery: zadá se název a požadovaná adresa je <název>.therapioteon-java.me. Adresa bude fungovat až po zajištění domény/DNS a serverového hostingu.
- Zda svět zůstane online, když hostitel odejde, je zatím nerozhodnuto.

## Herní svět a mechaniky
- 3D voxelový svět, pohyb, skok, pokládání a těžení bloků, hotbar, inventář, ukládání.
- Chunkové generování a načítání velkého světa; negenerovat celý svět předem.
- Survival: zdraví, hlad, sběr surovin, správné dropy, crafting, nástroje, odolnost a smrt/respawn.
- Creative: létání, neomezené bloky a stavění; hlad se nesnižuje.
- Bloky a předměty: hlína, tráva, kámen, písek, sklo, listí, rudy, prkna a různé druhy dřeva, pracovní stůl, dveře, schody, desky, ploty, tlačítka, cedule a další.
- Inventář klávesou E; funkční pracovní stůl, crafting a pece.
- Rudy: uhlí, železo, zlato, měď, diamant, emerald, lapis, redstone a další dle zvolené cílové verze; správné nástroje a tavení.
- Zbraně, brnění, štít, luky, šípy, kuše, opravy a enchantování.
- Jídlo, zdraví a hlad; mléko od krávy pomocí kbelíku, kbelík z železných ingotů.
- Vesnice, domy, cesty, farmy, studny, vesničané s profesemi a obchodováním za emeraldy, železný golem.
- Postele pouze červená a modrá; spánek a respawn.
- TNT: neomezené v Creative, vyrobitelné v Survival; zapalování a synchronizované poškození okolních bloků.
- Redstone prach, blok, pochodeň, páka, tlačítko, nášlapná deska a funkční mechanismy.
- Ender perla k teleportaci; Oko Enderu k hledání pevnosti, pokud je generována.
- Kompas, mapa, rybářský prut a rybaření, koleje a vozíky, koně a sedla, lektvary a vaření.
- Stromky, stromy a různé druhy dřeva; jeskyně a generované stavby.
- Pěstování: motyka, obdělání půdy, semínka, růst plodin, vliv vody a sklizeň.

## Čas, počasí a mobové
- Den 10 minut, noc 10 minut; celkem 20 minut.
- Slunce putuje k obzoru, při západu se objeví Měsíc a před úsvitem zmizí.
- Počasí: déšť, bouřky a sníh.
- Zvířata a pavouci se objevují přirozeně v rozumném množství, ne přeplněně.
- V noci zombie, kostlivci a zombie koně.
- Mírumilovná: zombie, kostlivci a pavouci se nespawnují; zombie koně mohou, vlci zůstávají v lesích.

## Ovládání a pomocné systémy
- PC klávesnice/myš; telefon dotyk; konzole gamepad; Meta Quest 3S VR ovladače a pohyb.
- T otevře chat; Enter odešle zprávu. Multiplayerové zprávy uvidí ostatní hráči.
- Připojení: „/Jméno hráče/ Se připojil do hry“; odpojení: „/Jméno hráče/ Se odpojil ze hry“.
- THERAPIOTEON konzole s historií a chybami; implementovat jen skutečně funkční příkazy, např. /give, /gamemode, /tp, /time, /weather.
- O otevře správce modů/pluginů; uživatel může nahrát soubor. Neznámé .jar soubory nejsou automaticky kompatibilní; nutná kontrola kompatibility a bezpečné oddělení.
- H otevře pomocníka s radami; nesmí sám měnit svět, soubory, nastavení ani mody. Vyžaduje internet a backend/API.
- B otevře nabídku tanečků; odemykají se pouze za herní diamanty, bez reálných plateb; ostatní hráči vidí animaci.
- Prohlížeč/Google přes L byl zrušen a nemá se přidávat.

## Dříve schválených 12 rozšíření
1. Kompas a mapa.
2. Postele a respawn (jen červená/modrá).
3. Brnění, štít a zbraně.
4. Luky, šípy a kuše.
5. Rybářský prut a rybaření.
6. Koleje, vozíky a redstone mechanismy.
7. Lektvary a vaření.
8. Truhly, sudy a pece.
9. Koně, sedla a jízda.
10. Stromky, stromy a různé druhy dřeva.
11. Déšť, bouřky a sníh.
12. Vesnice, jeskyně a generované stavby.

## Technické milníky a poctivé označování
- Aktuální stav je pouze počáteční webový prototyp a specifikace, nikoli hotová 3D hra.
- Další fáze: zvolit herní engine a cílovou verzi obsahu; postavit základ 3D světa; ukládání; Survival/Creative; síťový backend a friends; platformní sestavení; testování.
- Funkce se označují jako plánované, rozpracované, implementované nebo otestované. Nesmí se tvrdit, že multiplayer, platformní build nebo serverová doména fungují, dokud nejsou skutečně nasazeny a ověřeny.
