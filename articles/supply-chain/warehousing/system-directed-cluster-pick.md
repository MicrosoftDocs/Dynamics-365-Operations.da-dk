---
title: Systembaseret klyngepluk
description: Dette emne indeholder en oversigt over systembaseret klyngeplukning i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c3b23a5d3b77bae89e4845bdff4ab20f95c46497
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917850"
---
# <a name="system-directed-cluster-picking"></a>Systembaseret klyngepluk

[!include [banner](../includes/banner.md)]

Klyngeplukning er en stykplukproces, der giver dig mulighed for at plukke varer til flere ordrer på samme tid ved at klynge dem til plukklynger. Du skal derefter kun besøge afhentningsstedet én gang. Denne funktionalitet bruges typisk med små ordrepluk eller mængder, der er mindre end sagsmængder.

Når systembaseret klyngeplukning er konfigureret, kan du klyngeplukke opgaveoverskrifter på basis af en systemgenereret klynge. Systemklyngen plukker ordrer op til det antal stillinger, der er angivet i klyngeprofilen. Derfor kan du plukke flere ordrer på samme tid uden at skulle oprette en klynge manuelt.

Systembaseret klyngeplukning tilbyder et alternativ til manuel klyngeopbygning, hvor en klyngeprofil bruges til at oprette en klynge. Der skal defineres flere opsætningsrelaterede linjer i klyngeprofilen, før den bruges:

- **Antallet af stillinger** svarer til antallet af ordrer, der vil blive lagt på en klynge. Derfor svarer det til antallet af totes.
- **Bryd klynge** bestemmer, hvornår klyngen skal brydes.
- **Generer klynge-ID** kontrollerer, om klynge-ID'et skal genereres af systemet eller indtastes af brugeren.
- **Sorteringsverfikationstypen** bestemmer, om der kræves positionsverifikation.

Et nyt menupunkt til mobilenheder bruges til systembaseret klyngeplukning. Klyngeprofil-ID'et skal angives for indstillingen **Baseret på**. Desuden kan den systembaserede forespørgselsrækkefølge gruppere ordrer baseret på firmaspecifikke kriterier. Derfor kan du yderligere optimere tildelingen af arbejdsordrer ved at angive tilpassede sorteringskriterier i den systembaserede forespørgselsrækkefølge.

Når systembaserede klyngeplukning er udført, vises lagerarbejderne med en klynge, hvor plukordrer er blevet forudtildelt klyngeplaceringer. Derfor kan arbejdere begynde at plukke en vare til flere arbejdsordrer ved kun at besøge plukplaceringen én gang. Plukprocessen for systembaseret klyngeplukning er den samme som processen for brugerbaseret klyngeplukning.

## <a name="set-up-system-directed-cluster-picking"></a>Opsætning af systembaseret klyngepluk

### <a name="create-cluster-profiles"></a>Opret klyngeprofiler

Klyngeprofiler styrer, hvordan systemet opretter hver klynge. Hvis der kræves forskellige klynger, skal der oprettes en anden klyngeprofil for hvert menupunkt på mobilenheden.

1. Gå til **Lokationsstyring \> Opsætning \> Mobilenhed \> Klyngeprofiler**.
2. Vælg **Ny**.
3. I feltet **Klyngeprofil-ID** skal du angive **2. position**.
4. I feltet **Navn** skal du skrive **2. position**.
5. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Generer klynge-ID:** Angiv denne indstilling til **Ja**. Denne indstilling bestemmer, om klynge-ID'et oprettes automatisk af systemet, eller om brugeren skal oprette det i starten af pluk.
    - **Aktivér positioner:** Angiv denne indstilling til **Ja**. Denne indstilling bestemmer, om positions navnene genereres automatisk ud fra opsætningen af stillingsnavnet. Hvis denne indstilling er angivet til **Nej**, bruges nummerplade-ID'et for placeringen.
    - **Antal stillinger:** Indtast **2**. Dette felt angiver det maksimale antal stillinger, som klyngen kan have (det er det maksimale antal bokse, toter osv.).
    - **Positions navn:** Vælg **Numerisk**, så positionerne navngives ved hjælp af fortløbende numre. Hvis du vælger **Alfabetisk**, er positionerne blevet navngivet i alfabetisk rækkefølge.
    - **Bryd klynge på:** Vælg **Læg på lager**. Dette felt bestemmer, hvornår klyngen er brudt.
    - **Sorter verifikationstype:** Vælg **Positionsscanning**. Dette felt bestemmer, om læg-til-stilling-trinnet er verificeret.

6. I oversigtspanelet **Klyngesortering** kan du definere sorteringskriterier ved at oprette en ny linje og angive følgende felter:

    - **Sekvensnummer:** Dette felt bestemmer den sekvens, som systemet sorterer efter. En værdi indtastes automatisk, men du kan ændre den efter behov.
    - **Feltnavn:** Vælg **WMSLocationId**. Dette felt angiver det felt, som linjen bruger til sorteringskriterier.
    - **Sortering:** Vælg **Stigende**. Dette felt definerer, om sorteringen udføres i stigende eller faldende rækkefølge.

### <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed

Hvis du vil oprette et nyt menupunkt på mobilenheden til systembaseret klyngepluk og sammenkæde klynge profil-ID'et med menupunktet på mobilenheden, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
2. Vælg **Ny**.
3. I feltet **Navn på menupunkt** indtastes **SD-klynge**.
4. I feltet **Titel** indtastes **SD-klynge**.
5. Vælg **Arbejde** i feltet **Tilstand**.
6. Angiv indstillingen **Brug eksisterende arbejde** til **Ja**.
7. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Baseret på:** Vælg **Systembaseret**.
    - **Generer nummerplade:** Angiv indstillingen til **Ja**.
    - **Klynge profil-ID:** Vælg **2. position**.

8. I oversigtspanelet **Arbejdsklasser** skal du angive den gyldige arbejdsklasse for menupunktet mobilenhed ved at konfigurere følgende felter:

    - **Arbejdsklasse-ID:** Sørg for, at **Salg** er indtastet.
    - **Arbejdsordretype:** Sørg for, at **Salgsordre** er indtastet.

9. Følg disse trin for at angive en ny systembaseret arbejdssekvensforespørgsel:

    1. Vælg **Ny**.
    2. Angiv **1** i feltet **Løbenummer**.
    3. I feltet **Beskrivelse** skal du vælge **Arbejdsprioritet – Arbejds-ID**.

10. Vælg **Rediger forespørgsel** i menuen.
11. Angiv følgende felter under fanen **Sortering**:

    - **Tabel:** Vælg **Arbejde**.
    - **Afledt tabel:** Vælg **Arbejde**.
    - **Felt:** Vælg **Arbejdsprioritet**.
    - **Søgeretning:** Vælg **Stigende**.
    - **Tabel:** Vælg **Arbejde**.
    - **Afledt tabel:** Vælg **Arbejde**.
    - **Felt:** Vælg **Arbejds-ID**.
    - **Søgeretning:** Vælg **Stigende**.

Systemet vil nu sortere arbejds-ID'er i klyngen, først efter arbejdsprioritet og derefter efter arbejds-ID.

### <a name="set-up-a-mobile-device-menu"></a>Opsætning af en mobilenhedsmenu

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
2. Tilføj det menupunkt, du lige har oprettet, til den ønskede menu.

## <a name="example"></a>Eksempel

### <a name="create-picking-work"></a>Opret plukarbejde

Før du kan konfigurere systembaseret klyngepluk, skal du oprette noget kvalificeret udgående arbejde. Den klyngeprofil, du oprettede tidligere, angiver to klyngeplaceringer. Du skal derfor oprette mindst to arbejds-ID'er.

1. Gå til **Sales and MArketing \> Salgsordrer \> Alle salgsordrer**.
2. Vælg **Ny** for at oprette en ny salgsordre.
3. Vælg en kunde i feltet **Kundekonto**.
4. I oversigtspanelet **Generelt** skal du i feltet **Lagersted** vælge lagersted **62**.
5. Vælg **OK**.
6. I oversigtspanelet **Salgsoprdrelinjer** skal du vælge **Tilføj linje**.
7. Vælg **A0001** i feltet **Varenummer**.
8. Angiv **1** i feltet **Antal**.
9. Vælg **Tilføj linje** for at tilføje en anden linje.
10. Vælg **A0002** i feltet **Varenummer**.
11. Angiv **3** i feltet **Antal**.
12. Gentage trin 2 til og med 6.
13. Vælg **A0001** i feltet **Varenummer**.
14. Angiv **4** i feltet **Antal**.
15. Vælg **Tilføj linje** for at tilføje en anden linje.
16. Vælg **A0002** i feltet **Varenummer**.
17. Angiv **2** i feltet **Antal**.

Reserver lageret, og frigør det til lagerstedet. Der oprettes to forskellige arbejds-ID'er. Hvert arbejds-ID har to pluklinjer.

### <a name="run-the-mobile-device-flow"></a>Kør mobilenhedsprocessen

1. På mobilenheden skal du vælge den menu, der indeholder det nye mobilenhedsmenupunkt.
2. Vælg menupunktet **SD-klynge**, og start plukning. Der oprettes en klynge, og de to arbejds-ID'er, du har oprettet tidligere, er knyttet til den. Hvis du har oprettet mere end to arbejds-ID'er, føjes kun de første to til klyngen. Bemærk, at arbejds-ID'erne føjes til klyngen i stigende rækkefølge, som du angav i forespørgselsopsætningen.

    > [!NOTE]
    > Den nye klynge oprettes kun automatisk, hvis der tidligere er oprettet nok ekstra arbejds-ID'er. Ellers vises følgende meddelelse: "Der kan ikke findes nok arbejde for klyngen".

    Når du har valgt menuen, vises det første pluk-skærmbillede. Systemet samler alle matchende pluklinjer fra de to arbejds-ID'er og dirigerer dig til at besøge plukstedet én gang, så du kan opfylde begge ordrer ved at bruge ét pluk. Denne proces udføres på samme måde som proces for brugerbaseret klyngeplukning.

3. Bekræft første plukning. Du skal derefter indtaste positionsnavnet for at bekræfte, at varerne er sat til den korrekte position.
4. Gentag denne proces, indtil alle varer er plukket og sat til den korrekte position.
5. Det sidste trin på mobilenheden er at sætte klyngen til den endelige placering. Når denne læg på lager-handling er bekræftet, lukkes og brydes klyngen på basis af den værdi, du har angivet for feltet **Bryd klynge ved** i klyngeprofilen. Arbejds-ID'er lukkes også.
6. Meddelelsen "Klynge fuldført" vises på mobilenheden.
