# Működési protokoll

## Átadási szabályok

- Minden átadás tartalmazzon rövid összegzést, bizonyítékot (fájl, parancs vagy teszt), kockázatot és nyitott kérdést.
- Egy agent csak a saját felelősségi körében módosítson fájlt. Átfedés esetén az orchestrator dönt a sorrendről.
- A reviewer és a verifier ne fogadja el az executor önértékelését bizonyíték nélkül.

## Biztonsági minimum

- Titkot, hozzáférési tokent, személyes adatot és teljes produkciós adatbázis-exportot ne írjanak logba, tesztadatba vagy dokumentációba.
- Külső inputot validálni kell; jogosultságot szerveroldalon kell ellenőrizni.
- Multi-tenant rendszernél minden lekérdezés és művelet tenant-hatókörét explicit módon rögzíteni kell.
- Visszafordíthatatlan adatváltoztatás előtt legyen mentési, migrációs vagy visszaállítási terv.

## Lezárási kapu

Egy feladat akkor kész, ha az elfogadási feltételek bizonyítottan teljesülnek, a releváns tesztek lefutottak, és nincs nyitott kritikus vagy magas súlyosságú review-megállapítás.
