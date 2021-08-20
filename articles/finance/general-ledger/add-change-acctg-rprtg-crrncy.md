---
title: Ændre regnskabs- eller rapporteringsvalutaen
description: I dette emne beskrives, hvordan du kan ændre regnskabs- eller rapporteringsvalutaen eller føje en rapporteringsvaluta til opsætningen af finansmodulet.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1fd641d4f60d8ff9710c89f43777f7fd8f378dbc6c73d773ac103f9d9f68e60e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770587"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Ændre regnskabs- eller rapporteringsvalutaen

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du kan ændre regnskabs- eller rapporteringsvalutaen eller føje en rapporteringsvaluta til opsætningen af finansmodulet.

## <a name="symptom"></a>Symptom

Du vil ændre regnskabs- eller rapporteringsvalutaen eller føje en rapporteringsvaluta til finansopsætningen. Det sker typisk i følgende scenarier:

- Den forkerte regnskabs- eller rapporteringsvaluta blev angivet, da en juridisk enhed blev konfigureret. Du vil nu ændre valutaen.
- Der blev angivet en rapporteringsvaluta, da en juridisk enhed blev konfigureret, men organisationen vil nu fjerne rapporteringsvalutaen.
- Organisationen opgraderer eller overflytter til Microsoft Dynamics 365 Finance og vil ændre regnskabs- eller rapporteringsvalutaen.

En organisation, der ikke tidligere brugte den dobbelte valutafunktion, vil nu begynde at bruge den. Denne fejl opstår typisk i følgende scenarier.

- Ingen rapporteringsvaluta blev angivet, da en juridisk enhed blev konfigureret. (En rapporteringsvaluta er valgfri). Nu vil du tilføje en rapporteringsvaluta.

## <a name="resolution"></a>Løsning

Det vigtigste er, om der er bogført transaktioner (faktisk eller budget) i den juridiske enhed for finansopsætningen. **Du kan ikke ændre regnskabs- eller rapporteringsvalutaen eller tilføje en rapporteringsvaluta, hvis der er bogført transaktioner (faktiske eller budget) i den juridiske enhed.** Følg trinnene i et af følgende afsnit, afhængigt af om der er bogført transaktioner.

### <a name="no-transactions-have-been-posted"></a>Der er ikke bogført nogen transaktioner

1. Gå til **Finans \> Finansopsætning \> Finans** i den juridiske enhed, du opdaterer valutaer for.
2. Vælg **Rediger** på siden **Finans**.
3. Vælg den regnskabsvaluta og den rapporteringsvaluta, der skal bruges for den juridiske enhed, i oversigtspanelet **Valuta**.
4. Vælg **Gem**.

Hvis felterne for regnskabsvalutaen og rapporteringsvalutaen ikke er tilgængelige på siden **Finans**, er en eller flere transaktioner (faktiske eller budget) blevet bogført i den juridiske enhed. Derfor kan valutaerne ikke ændres. Hvis det er tilfældet, skal du følge trinnene i næste afsnit.

### <a name="transactions-have-been-posted"></a>Transaktioner er bogført

**Hvis der er bogført transaktioner i den juridiske enhed, kan du kun ændre eller tilføje regnskabs- og rapporteringsvalutaer ved at oprette en ny juridisk enhed med de korrekte valutaer.** Du kan gøre processen lettere ved at bruge Datastyring i systemet til at kopiere opsætningsposter og masterposter fra den aktuelle juridiske enhed til en ny juridisk enhed.

Ændringer i regnskabs- og rapporteringsvalutaerne er omsiggribende. De påvirker ikke kun Finans, men også alle reskontro (Debitor, Kreditor, Lager, Projekt osv.), alle uafhængige softwareleverandører (ISV) og alle de forlængelser, du har foretaget til butikkernes beløb.

Der opstår fejl i processen til søgning efter og oversættelse af hvert beløb til en anden valuta. Teknikerteamet vil derfor ikke godkende et script, der ændrer eller tilføjer regnskabs- og rapporteringsvalutaer. Selvom et værktøj, der var tilgængeligt for Microsoft Dynamics AX 2012, giver dig mulighed for at ændre eller tilføje regnskabs- og rapporteringsvalutaer, blev dette værktøj frarådet for AX 2012 R3 og Finance.

Benyt disse trin for at kopiere opsætningen og masterdataene fra den aktuelle juridiske enhed til en ny juridisk enhed.

1. Gå til **Arbejdsområder \> Dataadministration**.
2. Vælg **Skabeloner** under gruppen **Import/eksport**.
3. Kontrollér, at skabelonerne er tilgængelige. Hvis der ikke er tilgængelige skabeloner, skal du vælge **Indlæs standardskabeloner** og vente på, at skabelonerne oprettes.
4. Vend tilbage til arbejdsområdet **Dataadministration**.
5. Vælg **Kopiér til juridisk enhed**.
6. Skriv et gruppenavn og en beskrivelse.
7. Vælg den juridiske enhed, du vil kopiere data fra, i feltet **Juridisk enhed for kilde**.
8. I oversigtspanelet **Juridiske enheder for destination** skal du vælge **Opret juridiske enheder** for at oprette en ny juridisk enhed, som du kan kopiere kildedataene for den juridiske enhed til. Vælg **Vælg eksisterende** for at kopiere data til en eksisterende juridisk enhed.
9. Valgfrit: Angiv feltet **Kopiér nummerserier** til **Ja**. (Dette trin anbefales, når du kopierer data.)
10. Vælg **Tilføj skabelon** i området **Valgte enheder**.
11. Vælg den skabelon, du vil bruge. Foreslåede skabeloner til en ny juridisk enhed omfatter **025 – Finans** og **Finans**. Vi anbefaler, at du gennemser alle de andre tilgængelige skabeloner for at finde ud af, om nogen af dem gælder for dine behov.
12. Vælg **Kopiér til juridisk enhed** for at starte en batchproces, der skal oprette de valgte enheder og kopiere dem til den juridiske destinationsenhed.
13. Når processen er fuldført, men før der bogføres transaktioner, skal du gå til finans og opdatere regnskabs- og rapporteringsvalutaerne som beskrevet tidligere i dette emne.

Hvis du har oprettet en ny juridisk enhed, så du kan ændre regnskabs- eller rapporteringsvalutaen, skal du kontrollere, at startsaldi er omsat fra valutaerne i den gamle juridiske enhed til de nye valutaer.

Du kan få vist en video, som viser de foregående trin, i [Kopiér til juridisk enhed](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
