---
name: agevolt-creator
description: Pouzi ked treba vytvorit alebo upravit AgeVolt AI Agent modul, skill, pravidlo, osobne pravidla, knowledge base alebo MCP. Toto je public bootstrap verzia, ktora najprv najde lokalny SharePoint AI Agent root a potom pouzije interne pravidla odtial.
---

# AgeVolt Creator Bootstrap

Toto je public bootstrap skill. Neobsahuje internu knowledge base. Jeho uloha je najst lokalne zosynchronizovany SharePoint priecinok `AI Agent` a nacitat skutocne AgeVolt Creator pravidla odtial.

Bootstrap update marker: `git-upgrade-pilot-001`.

## Najprv Najdi AI Agent Root

Pred kazdou pracou najdi lokalny root v tomto poradi:

1. Hodnota environment premennej `AGEVOLT_AI_AGENT_ROOT`, ak existuje.
2. `%USERPROFILE%\OneDrive - AgeVolt Slovakia, s.r.o\Dokumenty - Produkt\AI Agent`.
3. Aktualny workspace alebo jeho rodic, ak sa vola `AI Agent`.
4. Ak root nevies najst, poziadaj pouzivatela, aby zosynchronizoval SharePoint priecinok `Dokumenty - Produkt/AI Agent` cez OneDrive alebo ti dal cestu.

## Potom Nacitaj Interne Pravidla

Ak root existuje, pred tvorbou alebo upravou citaj:

1. `START_HERE.md`
2. `core/governance.md`
3. `core/module-contract.md`
4. `core/marketplace-strategy.md`
5. `modules/agevolt-creator/skills/agevolt-creator/SKILL.md`
6. `modules/agevolt-creator/rules/creator-governance.md`
7. `modules/agevolt-creator/rules/question-flow.md`

Ak niektory subor chyba, povedz to a pouzi najblizsie dostupne pravidla.

## Hlavne Bezpecnostne Pravidlo

Firemny modul, skill, rule, KB alebo MCP neupravuj bez explicitnej poziadavky pouzivatela. Pri nejasnej poziadavke vytvor navrh, rule candidate alebo osobne pravidla.

Explicitna poziadavka znie napriklad:

- "uprav firemny skill",
- "zmen tento modul",
- "dopln pravidlo do firemneho modulu",
- "vytvor MCP server".

Pri explicitnej firemnej zmene dopis `revision-history.md` v dotknutom module.

## Public Repo Pravidlo

Do tohto public Git marketplace neukladaj:

- internej knowledge base,
- customer data,
- secrets, tokeny, API kluce,
- firemne rozhodnutia, ktore nie su urcene na zverejnenie,
- exporty zo SharePointu, ClickUpu, mailov, Teams alebo SuperFaktury.

Tento repo je iba bootstrap/update kanal. Interny source of truth je SharePoint `AI Agent`.

## Otazkovy Loop

Pytaj sa postupne:

1. Co ma agent pomahat robit?
2. Kto to bude pouzivat?
3. Ukaz 3 realne priklady vstupu.
4. Co ma agent urobit automaticky?
5. Co ma iba navrhnut?
6. Kedy sa ma zastavit?
7. Kam sa ma vysledok zapisat?
8. Ako overime, ze pravidlo funguje?
