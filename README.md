# NTG artikel

Dit project bevat de volgende onderdelen:

the-introduction
:   Een introductie van de auteur (Erik Nijenhuis).

the-article
:   Het artikel met een demo over `lua-placeholders` en GinVoice.

invoice-template
:   Een voorbeeld uit de demo map

invoice-001
:   Een voorbeeld van Grapefruit Inc. uit de demo map

invoice-002
:   Een voorbeeld van Xerdi uit de demo map

invoice2-template
:   Een voorbeeld van Grapefruit Inc. uit de demo-splitted map.

Er zijn nog meer voorbeelden te genereren, echter worden die niet als bijlage in het artikel gebruikt.

## Uitvoer
Om de voorbeelden te kunnen compileren heb je `lua-placeholders` versie 1.0.2 nodig.
Deze is momenteel nog niet uitgebracht en is dus alleen via [GitHub](https://github.com/Xerdi/lua-placeholders) te krijgen in de tussentijd.
Verder zijn er 3 Makefiles:
 - src/Makefile
 - src/demo/Makefile
 - src/demo-splitted/grapefruit/Makefile

Om de onderdelen te compileren.
Deze Makefiles zijn geschikt gemaakt voor Windows 10 en Ubuntu met een recente TeX Live distribute (dus niet uit apt).

Om alle standaard onderdelen te compileren kun je `make all` uitvoeren in de `src/` map.
