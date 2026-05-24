---
name: personal-productivity
description: Pouzi ked pouzivatel chce vytvorit alebo upravit osobne pravidla, pravidla pre triedenie mailov, pripravu meetingov, denne alebo tyzdenne rutiny, task workflowy alebo osobny AgeVolt produktivny system. Toto je public bootstrap skill, ktory najprv najde lokalny SharePoint AI Agent root a potom pouzije interne pravidla z modulu personal-productivity.
---

# Personal Productivity Bootstrap

Toto je public bootstrap skill. Neobsahuje internu knowledge base.

## Najdi AI Agent Root

Najdi lokalny root v tomto poradi:

1. `AGEVOLT_AI_AGENT_ROOT`, ak existuje.
2. `%USERPROFILE%\OneDrive - AgeVolt Slovakia, s.r.o\Dokumenty - Produkt\AI Agent`.
3. Aktualny workspace alebo jeho rodic, ak sa vola `AI Agent`.

Ak root nevies najst, poziadaj pouzivatela o cestu k SharePoint priecinku `AI Agent`.

## Nacitaj Interne Pravidla

Ak root existuje, citaj podla potreby:

1. `core/governance.md`
2. `core/module-contract.md`
3. `modules/personal-productivity/module.yaml`
4. `modules/personal-productivity/README.md`
5. `modules/personal-productivity/rules/personal-rules-governance.md`
6. `modules/personal-productivity/templates/mail-triage-rules-template.md`

Ak subor chyba, povedz to a pouzi najblizsie dostupne pravidla.

## Scope

Pomahaj hlavne s:

- osobnymi pravidlami pre jedneho cloveka,
- triedenim mailov a rozhodovanim, co je akcia,
- meeting prep rutinami,
- dennymi a tyzdennymi prehladmi,
- osobnymi task workflowmi.

## Bezpecnost

- Bez explicitneho suhlasu neodosielaj maily, nemen tasky, nevytvaraj udalosti a nerob zapisy do zivych systemov.
- Pri nejasnej poziadavke navrhni osobny rule candidate, nie firemny skill.
- Firemne pravidla v `modules/` upravuj iba pri explicitnej poziadavke a zapis `revision-history.md`.
- Osobne pravidla ukladaj pod `personal/<person-slug>/rules/`.

## Minimalny Vystup

Pri tvorbe osobnych pravidiel vrat:

1. kratky nazov pravidla,
2. kedy sa ma pouzit,
3. vstupy, ktore agent potrebuje,
4. co moze urobit automaticky,
5. co ma iba navrhnut,
6. stop podmienky,
7. testovaci priklad.
