---
title: Faktureringsklassifikationer og faktureringskoder i den offentlige sektor
description: Offentlige organisationer kan bruge faktureringsklassificeringer og faktureringskoder til at administrere fritekstfakturaer.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustBillingClassification, CustBillingCode, CustCustomField
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19491
ms.assetid: 47624566-0b4c-41dc-9cd4-801e213b5da3
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: d64f9228c538a08a2fc938bc6ff4ce11278b6fed
ms.openlocfilehash: 0087c390eba7cae0cbbefd95a50cd3beb6e9f6d6
ms.lasthandoff: 03/31/2017


---

# <a name="billing-classifications-and-billing-codes-in-the-public-sector"></a>Faktureringsklassifikationer og faktureringskoder i den offentlige sektor

Offentlige organisationer kan bruge faktureringsklassificeringer og faktureringskoder til at administrere fritekstfakturaer. 

<a name="billing-classifications"></a>Faktureringsklassifikationer
-----------------------

Faktureringsklassifikationer bruges til at gruppere ensartede fritekstfakturaer til behandling og visning. Eksempelvis kan et forsendelsesbureau leje plads i hver forsendelsesstation til små cafeer og andre forhandlere. Ved at oprette en faktureringsklassifikation til udlejninger kan bureauet automatisk anvende de samme betalingsbetingelser og bruge den samme rækkefølge af rykkere for alle udlejninger. Bureauet kan også få vist fakturaer for alle udlejninger sammen, selvom udlejningerne ikke deler de samme økonomiske dimensioner. Faktureringsklassifikationer omfatter følgende oplysninger:

-   Faktureringsklassifikationskode (op til 15 alfanumeriske tegn)
-   Beskrivelse (op til 60 tegn)
-   Betalingsbetingelser
-   Renteoplysninger
-   Nummerserien for fakturanummeret
-   Nummerserien for kreditnotaer
-   Nummerserien for rykkere
-   Faktureringskoder, der kan tildeles fakturaer, der bruger denne faktureringsklassifikation

Du kan bruge faktureringsklassifikationer til at styre udligningsprioriteten over fritekstfakturaer. Du kan få flere oplysninger i [Udligningsprioritet i den offentlige sektor](settlement-priority-public-sector.md). En faktureringsklassifikation kan indeholde mange faktureringskoder, men hver faktureringskode kan kun tildeles én faktureringsklassifikation. Når du vælger en faktureringsklassifikation på en fritekstfaktura, er kun de faktureringskoder, der er angivet på faktureringsklassifikationen, tilgængelige for fakturaen. Før du konfigurerer faktureringsklassifikationer, skal du sørge for, at du har oprettet vilkårene for betaling, rentekoder, posteringsprofiler, rykkerforløb, nummerserier og faktureringskoder, du planlægger at bruge på faktureringsklassifikationerne.

## <a name="billing-codes"></a>Faktureringskoder
Faktureringskoder indeholder et sæt standardfaktureringsværdier og -satser for en defineret type ydelse eller gebyr. De værdier, du definerer for hver enkelt faktureringskode, angives automatisk på fritekstfakturalinjen, når faktureringskoden vælges. En afdeling for affaldshåndtering kan f.eks. fakturere visse debitorer for nye beholdere. De vil have en betalingskode for "ny objektbeholder", der indeholder faktureringsoplysninger for disse beholdere. Når afdelingen opretter en fritekstfaktura og vælger faktureringskoden "Ny beholder" på en fakturalinje, angives standardværdierne fra faktureringskoden automatisk. Faktureringskoder omfatter følgende oplysninger:

-   Faktureringskode (op til 10 alfanumeriske tegn)
-   Beskrivelse (op til 60 tegn, det udskrives på fakturaen)
-   Ikrafttrædelses- og en udløbsdato
-   Momsoplysninger
-   Renteoplysninger
-   Regnskabsfordeling
-   Rateoplysninger
-   Projektoplysninger (hvis aktiveret på siden Debitorparametre)
-   Brugerdefinerede felter

Generelt kan standardværdierne fra faktureringskoden ændres på fritekstfakturaen. Du kan dog angive faktureringskoden for at tillade eller forhindre ændringer af bestemte felter. Du kan få flere oplysninger i Fritekstfakturaer i den offentlige sektor. Faktureringskoder kan også tilknyttes flere bogføringsdefinitioner. Når der bruges en faktureringskode på en fakturalinje, bruges den bogføringsdefinition, der er knyttet til den faktureringskode, til at bogføre posteringen til Finans. Hvis du vil vide mere om bogføringsdefinitioner, skal du se [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).

### <a name="custom-fields"></a>Brugerdefinerede felter

Du kan oprette brugerdefinerede felter for faktureringskoder. Disse felter bruges til at indsamle data, der er relateret til bestemte faktureringsgebyrer. Afdelingen for dyrekontrol i en by kunne for eksempel bruge brugerdefinerede felter til registrering af typer af dyr og datoen for dens sidste vaccination for rabies. Da du tildeler brugerdefinerede felter til faktureringskoder, skal du oprette dine brugerdefinerede felter, før du opretter faktureringskoder. Der er seks typer brugerdefinerede felter. Du kan angive en standardværdi for et hvilket som helst brugerdefineret felt. Standardværdier kan ændres på fritekstfakturaen.

-   **Valuta** – valutafelter accepterer kun tal med to decimaler. Du kan angive de minimale og maksimale værdier for feltet.
-   **Decimal** – decimalfelter accepterer kun decimaltal med fire decimaler. Du kan angive de minimale og maksimale værdier for feltet.
-   **Tekst** – Tekstfelter kan indeholde al slags tekst og alt, hvad der angives i dem, betragtes som tekst. Du kan angive en maksimale feltlængde for feltet.
-   **Heltal** – heltalsfelter accepterer kun heltal. Du kan angive de minimale og maksimale værdier for feltet.
-   **Boolesk** – booleske felter giver mulighed for valg af Ja/Nej.
-   **Dato** – datofelter accepterer kun datoer. Datoen gemmes som mm/dd/åååå.

## <a name="do-i-have-to-use-billing-classifications"></a>Behøver jeg at bruge faktureringsklassifikationer?
Selvom du ikke behøver at aktivere faktureringsklassifikationer, anbefales det, at du gør det. Mange af de offentlige funktioner i appen Debitor er kun tilgængelige, når faktureringsklassifikationer er aktiveret. Når du har aktiveret faktureringsklassifikationer, er faktureringsklassifikationen et obligatorisk felt på fritekstfakturaer. Du kan få flere oplysninger om faktureringsklassifikationer og faktureringskoder på fritekstfakturaer i [Fritekstfakturaer i den offentlige sektor](free-text-invoices-public-sector.md).

## <a name="how-do-i-enable-billing-classifications"></a>Hvordan aktiverer jeg faktureringsklassifikationer?
Du kan aktivere faktureringsklassifikationer på siden **Debitorparametre**. I afsnittet **Generelt** på oversigtspanelet **Salgopsætning** skal du vælge **Brug faktureringsklassifikationer**. De sider, hvor du opretter faktureringsklassifikationer og faktureringskoder, er tilgængelige, før du aktiverer faktureringsklassifikationer. Du skal angive alle faktureringsklassifikationer og faktureringskoder, før du aktiverer dem. Når du har aktiveret faktureringsklassifikationer, skal alle fritekstfakturaer have en faktureringsklassifikation. **Bemærk**! Hvis du planlægger at bruge faktureringsklassifikationer til at bestemme udligningsprioriteten af fritekstfakturaer, skal du aktivere attributten **Fakturering** på siden **Udligningsprioritet**, når du har aktiveret faktureringsklassifikationer. Du kan få flere oplysninger i [Udligningsprioriteter i den offentlige sektor](settlement-priority-public-sector.md).

## <a name="do-i-have-to-create-new-billing-codes-when-billing-rates-change"></a>Behøver jeg at oprette nye faktureringskoder, når fakturerbare satser ændres?
Når faktureringskoder skal opdateres, skal du ikke oprette nye faktureringskoder. I stedet kan du oprette flere versioner af faktureringskoden med ikrafttrædelses- og slutdatoer for hver version. På ikrafttrædelsesdatoen starter systemet automatisk med at bruge den opdaterede version.

## <a name="can-i-assign-the-same-billing-code-to-more-than-one-billing-classification"></a>Er det muligt at tildele den samme faktureringskode til mere end én faktureringsklassifikation?
Nej, men der er en måde at få de resultater, du skal bruge, alligevel. Lad os antage, at din organisation bruger en separat faktureringsklassifikation for hver afdeling. Tre af afdelingerne skal have en faktureringskode til licensaftaler. Du kan ikke tildele en enkelt faktureringskode for "Licensaftale" til tre faktureringsklassifikationer, men du kan oprette et sæt af tre identiske faktureringskoder og tildele én til hver afdeling.




