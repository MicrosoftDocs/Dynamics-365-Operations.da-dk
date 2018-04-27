---
title: "Konfigurationsnøgler og dataenheder"
description: "Dette emne beskriver relationen mellem konfigurationsnøgler og dataenheder i Microsoft Dynamics 365 for Finance and Operations."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: f5b6ab35f65dbe325f2202ab2dda71152993359d
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="configuration-keys-and-data-entities"></a>Konfigurationsnøgler og dataenheder

[!INCLUDE [banner](../includes/banner.md)]

Før du kan bruge dataenheder til at importere eller eksportere data, anbefales det, at du først bestemmer virkningen af konfigurationsnøgler på de dataenheder, du planlægger at bruge. 

Yderligere oplysninger om konfigurationsnøgler i Finance and Operations, finder du i [Rapport for licenskoder og konfigurationsnøgler](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Tildelinger af konfigurationsnøgle
Konfigurationsnøgler kan tildeles til en eller flere af følgende genstande.
-   Dataenheder
-   Tabeller, der bruges som datakilde
-   Tabelfelter
-   Dataenhedsfelter

Tabellen nedenfor viser, hvordan konfigurationsnøgleværdier i de forskellige genstande, der ligger til grund for et objekt, ændrer den forventede funktionsmåde for objektet.

| Konfiguationsnøgleindstilling på dataenhed | Konfigurationsnøgleindstilling på tabel | Konfigurationsnøgleindstilling på tabelfelt | Konfiguationsnøgle på dataenhedsfelt | Forventet funktionsmåde                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------|-----------------------------|-----------------------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Deaktiveret                          | Ikke evalueret               | Ikke evalueret                     | Ikke evalueret                   | Hvis konfigurationsnøglen til dataenheden er deaktiveret, kan dataenheden ikke fungere. Det er ligegyldigt, om konfigurationsnøgler i de underliggende tabeller og felter er aktiveret eller deaktiveret.                                                                                                                                                                                                                                                                                                                                          |
| Slået til                           | Deaktiveret                    | Ikke evalueret                     | Ikke evalueret                   | Hvis konfigurationsnøglen til en dataenhed er aktiveret, kontrollerer datastyringen konfigurationsnøglen for hver af de underliggende tabeller. Hvis konfigurationsnøglen til tabellen er deaktiveret, er den pågældende tabel ikke tilgængelig til funktionel brug i dataenheden. Hvis en tabels konfigurationsnøgle er deaktiveret, evalueres konfigurationsnøgleindstillingerne for tabellen og dataenheden ikke. Hvis den primære tabel i enheden har konfigurationsnøglen deaktiveret, vil systemet fungere som om enhedens konfigurationsnøgle er deaktiveret. |
| Slået til                           | Slået til                     | Deaktiveret                          | Ikke evalueret                   | Hvis konfigurationsnøglen til en dataenhed er aktiveret, og konfigurationsnøglerne i de underliggende tabeller aktiveres, kontrollerer datastyringen konfigurationsnøglen på felterne i tabellerne. Hvis konfigurationsnøglen til et felt er deaktiveret, er feltet ikke tilgængeligt til funktionel brug i dataenheden, selv hvis det tilsvarende dataenhedsfelt har konfigurationsnøglen aktiveret.                                                                                                                                   |
| Slået til                           | Slået til                     | Slået til                           | Deaktiveret                        | Hvis konfigurationsnøglen er aktiveret på alle andre niveauer, men konfigurationsnøglen for enhedsfeltet ikke er aktiveret, vil feltet ikke være tilgængeligt til brug i dataenheden.                                                                                                                                                                                                                                                                                                                                                                          |

> [!NOTE]
> Hvis en enhed derefter en anden enhed som en datakilde, gælder ovenstående semantik på en rekursiv måde.

### <a name="entity-list-refresh"></a>Opdater liste over enheder
Når enhedslisten opdateres, opbygger datastyringen metadataene for konfigurationsnøgle metadataene til brug på kørselstidspunktet. Disse metadata er bygget ved hjælp af den logik, der er beskrevet ovenfor. Vi anbefaler, at du venter på, at opdateringen af enhedslisten er gennemført, før job og enheder i datastyringen anvendes. Hvis du ikke venter, er metadataene for konfigurationsnøglen måske ikke opdaterede, og det kan medføre uventede resultater. Når objektlisten opdateres, vises følgende meddelelse på enhedens listeside.

![Opdater liste over enheder](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Listeside for dataenhed
Dataenhedens listeside i arbejdsområdet Datastyring viser indstillingerne for konfigurationsnøglen for enhederne. Start fra denne side for at forstå virkningen fra konfigurationsnøgler på dataenheden.
Disse oplysninger vises ved hjælp af de metadata, der er opbygget under opdateringen af enheden. Kolonne Konfigurationsnøgle viser navnet på den konfigurationsnøgle, der er tilknyttet dataenheden. Hvis denne kolonne er tom, betyder det, at der ikke er nogen konfigurationsnøgle knyttet til dataenheden. Kolonnen Status for konfigurationsnøgle viser tilstanden for konfigurationsnøglen. Hvis den er markeret, betyder det, at nøglen er aktiveret. Hvis feltet er tomt, betyder det enten, at nøglen er deaktiveret, eller at der ikke er tilknyttet nogen nøgle.

![Listeside for enhed](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Målfelter
Det næste trin er at dykke ned i dataenheden for at få vist virkningen af konfigurationsnøgler i tabeller og felter. Formularen Målfelter for en dataenhed viser konfigurationsnøglen og statusoplysninger for nøglen for de relaterede tabeller og felter i dataenheden.  Hvis selve dataenheden har konfigurationsnøglen deaktiveret, vises en advarsel om, at tabellerne og felterne i formularen Målfelter for denne enhed ikke er tilgængelige, uanset status for deres konfigurationsnøgle.

![Målfelter](./media/Target_fields_1.png)

### <a name="child-entities"></a>Underordnede enheder 
Visse enheder har andre enheder som datakilder eller er sammensat dataenheder: vigtige konfigurationsoplysninger for disse enheder vises i formularen Underordnede enheder. Du kan bruge denne formular på lignende måde til listesiden over enheder, som beskrevet ovenfor. Formularen Målfelter for den underordnede enhed fungerer også, som det er beskrevet ovenfor.

![Målfelter](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Brug af dataenheder
Når du forstår den fulde virkning, hvis der er nogen, af konfigurationsnøgler på dataenheder, du vil bruge, kan du nu fortsætte med at bruge dataenhederne ved at føje dem til dataprojekter. 

### <a name="run-time-validations-for-configuration-keys"></a>Valideringer på kørselstidspunkt for konfigurationsnøgler
Ved hjælp af metadataene for konfigurationsnøglen, der er opbygget under opdatering af enhedsliste, udføres valideringer på kørselstidspunktet i følgende brugssituationer.

-   Når en dataenhed føjes til et job

-   Når brugeren klikker på 'valider' på enhedslisten

-   Når brugeren indlæser en datapakke i et dataprojekt

-   Når brugeren indlæser en skabelon i et dataprojekt

-   Når et eksisterende dataprojekt indlæses

-   Når en skabelon indlæses i et dataprojekt

-   Inden jobbet til eksport/import køres (batch, ikke-batch, tilbagevendende, Odata)

-   Når brugeren opretter en tilknytning

-   Når brugeren tilknytter felterne i brugergrænsefladen for tilknytning

-   Når brugeren kun tilføjer 'felter, der kan importeres'


### <a name="managing-configuration-key-changes"></a>Administration af ændringer i konfigurationsnøgle
Når du opdaterer konfigurationsnøgler på enheds-, tabel-eller feltniveau, skal enhedslisten i datastyringen opdateres. Denne proces sikrer, at systemet henter de nyeste konfigurationsnøgleindstillinger. Indtil enhedslisten opdateres, vises følgende advarsel på enhedens listeside. De opdaterede konfigurationsnøgleændringer træder i kraft, umiddelbart efter, at enhedslisten opdateres. Det anbefales, at du validerer eksisterende dataprojekter og job for at sikre, at de fungerer som forventet, når ændringerne i konfigurationsnøglerne sættes i kraft.

![Målfelter](./media/Target_fields_3.png)


