---
title: Konfiguration af kreditstyring
description: I dette emne beskrives den konfiguration, der kræves til kreditstyring.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9e756b678786d2c5a8c5bb9e890ce988090c09
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753659"
---
# <a name="credit-management-setup"></a>Konfiguration af kreditstyring 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Arbejdsgange for kreditstyring

Gå til **Kredit og inkasso \> Konfiguration \> Arbejdsgange for kreditstyring** for at definere de arbejdsgange, der skal bruges til at administrere reguleringer af kreditmaks.

- Du kan oprette en arbejdsgang, der giver dig mulighed for at godkende et batch af kreditmaks.reguleringer via en enkelt godkendelse.
- Du kan tilføje en arbejdsgang på linjeniveau, så reguleringer af kreditmaks. kan godkendes individuelt.
- Du kan oprette en arbejdsgang for frigivelse, der automatisk sender hold til en arbejdsgangsproces.

## <a name="blocking-rules"></a>Blokeringsregler

### <a name="ranking-payment-terms"></a>Rangere betalingsbetingelser

Du kan sætte en salgsordre på hold, hvis betalingsbetingelserne i ordren ikke stemmer overens med standardbetalingsbetingelserne for kunden. Betalingsbetingelserne er dog nogle gange forskellige, men tilstrækkeligt ens til, at du ikke ønsker at sætte ordren på hold. Du kan rangere betalingsbetingelser, så nogle af dem har samme rangering, mens andre har en højere eller lavere rangering.

Hvis rangeringerne for betalingsbetingelserne er aktive, og hvis betalingsbetingelserne for ordren har en højere rangering end standardbetalingsbetingelserne for kunden, sættes salgsordren på hold.

Når du vil konfigurere rangeringen af betalingsbetingelser, skal du gå til **Kredit \> Konfiguration \> Konfiguration af kreditstyring \> Ranger betalingsbetingelser**  

### <a name="ranking-settlement-discounts"></a>Rangere afregningsrabatter

Du kan sætte en salgsordre på hold, hvis kasserabatten i ordren ikke stemmer overens med standardkasserabatten for kunden. Kasserabatterne er dog nogle gange forskellige, men tilstrækkeligt ens til, at du ikke ønsker at sætte ordren på hold. Du kan rangere kasserabatter, så nogle af dem har samme rangering, mens andre har en højere eller lavere rangering.

Hvis rangeringerne for kasserabatterne er aktive, og hvis kasserabatten for ordren har en højere rangering end standardkasserabatten for kunden, sættes salgsordren på hold.

Når du vil konfigurere rangeringen af betalingsbetingelser, skal du gå til **Kredit \> Konfiguration \> Konfiguration af kreditstyring \> Ranger udligningsrabatter**  

## <a name="reasons"></a>Årsager

Der bruges flere forskellige årsagstyper i kreditstyring:

- Årsager til hold angiver, hvorfor en salgsordre er sat på hold.
- Årsager til frigivelse føjes til en ordre, når den frigives fra hold.
- Statusårsager angiver, hvorfor en kontostatus er tildelt en kunde.

Du kan konfigurere årsager på siden **Kreditstyringsårsager** (**Kredit \> Konfiguration \> Konfiguration af kreditstyring \> Kreditstyringsårsager**).

1. Vælg årsagstypen i feltet **Årsagstype**: **Hold**, **Frigiv** eller **Status**.
2. Angiv et navn på årsagen i feltet **Årsag**.
3. Angiv en beskrivelse af årsagskoden i feltet **Beskrivelse**.

## <a name="credit-management-groups"></a>Kreditstyringsgrupper

Kreditstyringsgrupper bruges til at identificere kunder eller kundegrupper, der har samme kreditstyringsegenskaber. Kreditstyringsgrupper kan f.eks. bruges til at bestemme blokerings- og udelukkelsesregler for kreditstyring for kunder.

Du kan konfigurere kreditstyringsgrupper på siden **Kreditstyringsgrupper** (**Kredit \> Konfiguration > Konfiguration af kreditstyring \> Kreditstyringsgrupper**).

1. Vælg **Ny** for at oprette en ny linje.
2. Angiv et id for gruppen. Id'et kan indeholde op til 10 tegn.
3. Angiv et navn på gruppen i feltet **Beskrivelse**. Navnet kan indeholde op til 60 tegn.

Kreditstyringsgruppen knyttes til en kunde på oversigtspanelet **Kredit og inkasso** på siden **Alle kunder** (**Debitor \> Kunder \> Alle kunder**).

## <a name="account-statuses"></a>Kontostatusser

Du kan oprette kontostatusser for at identificere den udestående kredit for kundekonto. Du kan definere en status og dens effekt på de fakturerings- og leveringsprocesser, der er på hold. Kontostatusser kan også bruges til at bestemme blokeringsregler for en kunde.

Du kan oprette kontostatusser på siden **Kontostatusser** (**Kredit \> Konfiguration > Konfiguration af kreditstyring \> Kontostatusser**).

1. Tilføj en kontostatus, og angiv en beskrivelse, der repræsenterer den udestående kredit for en kunde. Du kan f.eks. bruge **Normal** til at angive, at en kunde ikke har noget udestående, og at åbne ordrer indgår i standardkreditstyringsbehandlingen.
2. I felterne **Fakturering** og **Levering på hold** skal du vælge den type hold, der skal indtræde for kunder, der har denne kontostatus. Du kan sætte al behandling på hold, kun sætte fakturabehandling på hold eller ikke sætte nogen behandling på hold, når reglerne for kreditmaks. anvendes.

## <a name="scoring-groups"></a>Scoregrupper

Du kan konfigurere resultatgrupper for at definere risikofaktorer og de kriterier, der bruges til at måle dem. Når oplysninger om en kunde knyttes til en resultatgruppe, beregnes der et resultat for hver risikofaktor, og dette bruges til at anbringe kunden i en risikogruppe. Risikogruppen kan bruges til at identificere kreditværdighed og beregne automatisk kreditmaks.

Du kan oprette resultatgrupper på siden **Resultatgrupper** (**Kredit \> Konfiguration \> Konfiguration af kreditstyring \> Risiko \> Resultatgrupper**).

1. Opret en resultatgruppe, og giv den et navn.
2. Angiv en beskrivelse for yderligere at beskrive resultatgruppen.
3. Vælg en gruppetype. Der findes otte foruddefinerede typer. Du kan også vælge **Brugerdefineret** for at definere en gruppetype, der passer bedre til din organisation.
4. Vælg en resultattype for at definere, hvordan resultatgruppen beregner risikovurderingen. Der findes følgende indstillinger:

    - **Interval** – Brug denne indstilling til at definere et intervallet af værdier, der skal bruges til at beregne et resultat.
    - **Brugerdefineret** – Brug denne indstilling til manuelt at definere en liste over værdier, der skal bruges til resultatet.

5. Hvis du har valgt **Interval** som resultattype, kan du tilføje linjer for at definere intervallet af værdier og de tilsvarende resultater.

    1. Angiv den laveste værdi i intervallet i feltet **Fra værdi**.
    2. Angiv den højeste værdi i intervallet i feltet **Til værdi**.
    3. I feltet **Resultat** skal du angive det resultat, der skal tildeles, når den angivne værdi ligger i "fra"/"til"-intervallet.

    Hvis du har valgt **Brugerdefineret** som resultattype, kan du tilføje linjer for at definere de brugerdefinerede værdier og de tilsvarende resultater.

    1. I feltet **Værdi** skal du angive den brugerdefinerede værdi, der skal angives fra kundeoplysningerne.
    2. I feltet **Resultat** skal du angive det resultat, der skal tildeles, når den angivne værdi ligger i "fra"/"til"-intervallet.

## <a name="risk-classification"></a>Risikoklassifikation

Du kan definere risikovurderinger, der kan tilknyttes kunder på baggrund af deres risikovurdering. En risikovurdering beregnes ved at sammenligne kundeoplysninger med hver resultatgruppe. Resultaterne lægges sammen, og det samlede resultat sammenlignes med værdierne i konfigurationen af risikogrupper for at identificere den risikogruppe, som kunden tilhører. Risikogrupperesultatet bruges derefter til at definere blokerings- og udelukkelsesregler for kreditstyring for kunden.

Du kan oprette risikogrupper på siden **Risikovurderinger** (**Kredit \> Konfiguration \> Konfiguration af kreditstyring \> Risiko \> Risikoklassifikation**).

1. Angiv et risikogruppe-id.
2. Angiv en beskrivelse for yderligere at beskrive risikogruppen.
3. Angiv et interval af resultater, der bruges til at bestemme, hvilke kunder der hører til risikogruppen.
4. Vælg en risikogruppeindikator for at angive det symbol, der repræsenterer risikogruppen.

## <a name="guaranteeinsurance-types"></a>Garanti-/forsikringstyper

Du kan oprette garanti-/forsikringstyper på siden **Garanti-/forsikringstyper** (**Kredit \> Konfiguration \> Konfiguration af kreditstyring \> Forsikring og garantier \> Garanti-/forsikringstyper**).

1. Angiv en garanti- eller forsikringstype, der identificerer navnet på kautionisten eller forsikringsmægleren.
2. Angiv en beskrivelse for at beskrive kautionisten/forsikringsmægleren.

## <a name="coverage-types"></a>Dækningstyper

Dækningstyper kan bruges til yderligere at klassificere forsikringspolicer. De kan ikke bruges med garantier.

Du kan tilføje dækningstyper på siden **Dækningstyper** (**Kredit \> Konfiguration \> Konfiguration af kreditstyring \> Forsikring og garantier \> Dækningstyper**).

1. Angiv en dækningstype for at identificere den dækningstype , der skal tilføjes som forsikring eller garanti.
2. Angiv en kort beskrivelse for at beskrive dækningstypen.

## <a name="automatic-credit-limits"></a>Automatiske kreditgrænser

Du kan oprette kriterier for automatisk kreditmaks. på siden **Automatisk kreditmaks.** (**Kredit \> Konfiguration \> Konfiguration af kreditstyring \> Risiko \> Automatisk kreditmaks.**).

1. Vælg en risikogruppe, som den automatiske kreditmaks. skal tildeles.
2. Vælg valutaen for den automatiske kreditmaks. Du kan oprette flere automatiske kreditmaks. i forskellige valutaer for den samme risikogruppe.
3. Angiv indtægtsbeløbet, der repræsenterer den maksimale firmaindtægt, der kan bruges til dette automatiske kreditmaks. Når der oprettes kreditmaks., sammenlignes indtægtsbeløbet med en indtægtsværdi på siden **Finans** (**Debitor \> Alle kunder \> Vælg en kunde \> Generelt \> Statistikker \> Finans**). Systemet bruger den seneste værdi i sektionen **Oversigt**.

Udfør følgende trin for at tilføje linjer, der repræsenterer det kreditmaks., som genereres ud fra de valgte kriterier.

1. Vælg den resultatgruppe, der definerer de kundeoplysninger, der skal bruges til at beregne kreditmaks.
2. Vælg den sammenligningsoperator, der definerer, hvordan oplysningerne i resultatgruppen skal evalueres.
3. Angiv den værdi, der skal sammenlignes med den værdi, der er angivet for resultatgruppen.
4. Angiv det kreditmaks., der skal tildeles, hvis kundeoplysningerne svarer til den værdi, der er angivet for resultatgruppen. Du kan f.eks. oprette et automatisk kreditmaks. resultatgruppen **Lav**. Hvis det antal år, en virksomhed har været drevet i, tilhører en af resultatgrupperne, kan du definere én linje, der tildeler et kreditmaks. på 100.000, hvis kunden har drevet virksomhed i fem år, og en anden linje, der tildeler et kreditmaks. på 200.000, hvis kunden har drevet virksomhed i 10 år.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
