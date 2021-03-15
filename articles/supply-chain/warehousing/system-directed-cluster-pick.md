---
title: Systembaseret klyngepluk
description: Dette emne indeholder en oversigt over systembaseret klyngeplukning i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkCluster, WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fa737f61bfd5bd71ba6d76e75e57c8e2d682cda3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965671"
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

Et nyt menupunkt til mobilenheder bruges til systembaseret klyngeplukning. **Klyngeprofil-id'et** skal være specificeret for den valgte indstilling **Ledet af**. Desuden kan de systembaserede arbejdssekvensforespørgsler gruppere ordrer baseret på firmaspecifikke kriterier. Derfor kan du yderligere optimere tildelingen af arbejdsordrer ved at angive tilpassede sorteringskriterier ved hjælp af de systembaserede arbejdssekvensforespørgsler.

Når systembaseret klyngeplukning er aktiveret, vises lagerarbejderne med en klynge, hvor plukordrer er blevet forudtildelt klyngeplaceringer. Derfor kan arbejdere begynde at plukke en vare til flere arbejdsordrer ved kun at besøge plukplaceringen én gang. Plukprocessen for systembaseret klyngeplukning er den samme som processen for brugerbaseret klyngeplukning.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Aktivere systembaseret klyngeplukningsfunktion

Før du kan bruge denne funktion, skal den aktiveres i dit system. Administratorer kan bruge siden [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt. Her er funktionen angivet som:

- **Modul** – Lokationsstyring
- **Funktionsnavn** – Systembaseret klyngeplukning

Denne funktion kræver også aktivering af en afhængig funktion. Den afhængige funktion er:

- **Modul** – Lokationsstyring
- **Funktionsnavn** – Systembaseret arbejdsrækkefølge for hele virksomheden

## <a name="set-up-system-directed-cluster-picking"></a>Opsætning af systembaseret klyngepluk

### <a name="create-cluster-profiles"></a>Opret klyngeprofiler

Klyngeprofiler styrer, hvordan systemet opretter hver klynge. Hvis der kræves forskellige klynger, skal der oprettes en anden klyngeprofil for hvert menupunkt på mobilenheden.

1. Gå til **Lokationsstyring \> Opsætning \> Mobilenhed \> Klyngeprofiler**.
2. Vælg **Ny**.
3. I feltet **Klyngeprofil-ID** skal du angive **2. position**.
4. I feltet **Navn** skal du skrive **2. position**.
5. I oversigtspanelet **Generelt** skal du angive følgende oplysninger:

    - **Generér klynge-ID** – Vælg **Ja**. Denne indstilling bestemmer, om klynge-ID'et oprettes automatisk af systemet, eller om brugeren skal oprette det i starten af pluk. 
    - **Aktivér stillinger** – Vælg **Ja**. Denne indstilling bestemmer, om positions navnene genereres automatisk ud fra opsætningen af stillingsnavnet. Hvis denne indstilling er angivet til **Nej**, bruges nummerplade-ID'et for placeringen.
    - **Antal stillinger:** – Vælg **2**. Dette felt angiver det maksimale antal stillinger, som klyngen kan have (det er det maksimale antal bokse, toter osv.).
    - **Positionsnavn** – Vælg **Numerisk**, så positionerne navngives ved hjælp af fortløbende numre. Hvis du vælger **Alfabetisk**, er positionerne blevet navngivet i alfabetisk rækkefølge.
    - **Bryd klynge på:** – Vælg **Læg på lager**. Dette felt bestemmer, hvornår klyngen er brudt. 
    - **Sorter verifikationstype** – Vælg **Positionsscanning**. Dette felt bestemmer, om læg-til-stilling-trinnet er verificeret.
        
6. I oversigtspanelet **Klyngesortering** kan du definere sorteringskriterier ved at oprette en ny linje og angive følgende oplysninger:

    - **Sekvensnummer** – Vælg **1**. Dette felt bestemmer, hvilken rækkefølge systemet sorterer efter. En værdi indtastes automatisk, men du kan ændre den efter behov.
    - **Feltnavn:** – Angiv **WMSLocationId**. Dette felt angiver det felt, som linjen bruger til sorteringskriterier.
    - **Sortering:** – Vælg **Stigende**. Dette felt definerer, om sorteringen udføres i stigende eller faldende rækkefølge.

### <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed

Hvis du vil oprette et nyt menupunkt på mobilenheden til systembaseret klyngepluk og sammenkæde klynge profil-ID'et med menupunktet på mobilenheden, skal du følge disse trin.

1. Gå til **Lokationsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed**.
1. Vælg **Ny**.
1. Angiv følgende oplysninger i overskriftssektionen:
    - **Menupunktnavn** – SD-klynge
    - **Titel** – SD-klynge
    - **Tilstand** – Arbejde
    - **Brug eksisterende arbejde** – Ja

1. I oversigtspanelet **Generelt** skal du angive følgende oplysninger:
    - **Ledet af** – Systembaseret klyngeplukning
    - **Generér nummerplade** – Ja
    - **Klyngeprofil-id** – 2 Position

1. I oversigtspanelet **Arbejdsklasser** skal du angive den gyldige arbejdsklasse for menupunktet mobilenhed ved at konfigurere følgende felter:
    - **Arbejdsklasse-id** – Salg
    - **Arbejdsordretype** – Salgsordrer

1. I handlingsruden **Menupunkter i mobilenhed** skal du vælge **Systembaserede arbejdssekvensforespørgsler** og følge disse trin for at angive en ny systembaseret arbejdssekvensforespørgsel:
    - Vælg **Ny** i handlingsruden.
    - **Sekvensnummer** – 1
    - **Beskrivelse** – Arbejdsprioritet – Arbejds-id

1. Vælg **Rediger forespørgsel** i handlingsruden
1. Vælg fanen **Sortering**
1. Vælg **Tilføj** for at tilføje en ny linje, og angiv derefter følgende:
    - **Tabel** – Arbejde
    - **Afledt tabel** – Arbejde
    - **Felt** – Arbejdsprioritet
    - **Søgeretning** – Stigende
1. Vælg **Tilføj** for at tilføje en anden linje, og angiv derefter følgende:
    - **Tabel** – Arbejde
    - **Afledt tabel** – Arbejde
    - **Felt** – Arbejds-id
    - **Søgeretning** – Stigende

1. Systemet vil nu sortere arbejds-ID'er i klyngen, først efter arbejdsprioritet og derefter efter arbejds-ID.

### <a name="set-up-a-mobile-device-menu"></a>Opsætning af en mobilenhedsmenu

1. Gå til **Lokalitetsstyring > Opsætning > Mobilenhed > Menu i mobilenhed.**.
1. Tilføj menupunktet **SD-klynge**, som du lige har oprettet til en menu i mobilenheden.
1. Vælg menuen **Udgående**.
1. Vælg **Rediger** i handlingsruden.
1. Rul, indtil du finder **SD-klynge**.
1. Vælg **SD-klynge**. Pilen, der peger på listen **Menustruktur**, bliver aktiveret.
1. Vælg **pileknappen** for at flytte menupunktet **SD-klynge** til menustrukturen **Udgående**.
1. Vælg **SD-klynge** på listen **Menustruktur**, og vælg derefter pilene **OP** eller **NED** for at flytte menupunktet til den ønskede placering i menuen i mobilenheden.

## <a name="scenario"></a>Scenario

### <a name="create-picking-work"></a>Opret plukarbejde

Før du kan konfigurere systembaseret klyngepluk, skal du oprette kvalificeret udgående arbejde. Den klyngeprofil, du oprettede tidligere, angiver to klyngeplaceringer. Du skal derfor oprette mindst to arbejds-ID'er. I dette scenarie skal du oprette to salgsordrer, reservere lager, frigive salgsordrerne til lageret og derefter behandle bølgen manuelt.

1. Gå til **Salg og marketing > Salgsordrer > Alle salgsordrer**.
1. Vælg **Ny** i handlingsruden, hvis du vil oprette den første salgsordre.
    - Menuen **Opret salgsordre** åbnes. Angiv følgende oplysninger:
        - I oversigtspanelet **Debitor** skal du angive **Debitorkonto** - **US-004**.
        - I oversigtspanelet **Generelt** skal du angive **Lagersted** - **62**.
        - Vælg **OK** for at lukke menuen og oprette salgsordren..
    - I oversigtstabellen **Salgsordrelinjer** skal du vælge **Tilføj linje**, hvis der ikke automatisk tilføjes en ny linje, og angive følgende:
        - **Varenummer** – A0001
        - **Antal** – 1
        - Vælg **Tilføj linje** for at tilføje en anden linje.
        - **Varenummer** – A0002
        - **Antal** – 3
    - Reserver lager for begge de linjer, du netop har oprettet.
        - Vælg **Linje 1**.
        - I handlingsruden **Salgsordrelinjer** skal du vælge **Lager** og derefter **Reservation** på listen.
        - I formularen **Reservation** skal du vælge **Reserver parti** for at reservere lageret.
        - Luk formularen **Reservation**, når reservationen er fuldført.
        - Gentag disse trin for at reservere lager for **linje 2**.
1. Vælg **Ny** i handlingsruden, hvis du vil oprette den anden salgsordre
    - Menuen **Opret salgsordre** åbnes. Angiv følgende oplysninger:
        - I oversigtspanelet **Debitor** skal du angive **Debitorkonto** - **US-005**.
        - I oversigtspanelet **Generelt** skal du angive **Lagersted** - **62**.
        - Vælg **OK** for at lukke menuen og oprette salgsordren
    - I oversigtstabellen **Salgsordrelinjer** skal du vælge **Tilføj linje**, hvis der ikke automatisk tilføjes en ny linje, og angive følgende oplysninger:
        - **Varenummer** – A0001
        - **Antal** – 4
        - Vælg **Tilføj linje** for at tilføje en anden linje.
        - **Varenummer** – A0002
        - **Antal** – 2
    - Reserver lager for begge de linjer, du netop har oprettet.
        - Vælg **Linje 1**.
        - I handlingsruden **Salgsordrelinjer** skal du vælge **Lager** og derefter **Reservation** på listen.
        - I formularen **Reservation** skal du vælge **Reserver parti** for at reservere lageret.
        - Luk formularen **Reservation**, når reservationen er fuldført.
        - Gentag disse trin for at reservere lager for **linje 2**.
    - Luk salgsordren og gå tilbage til listesiden **Alle salgsordrer**.
1. Find de to salgsordrer, du lige har oprettet (det kan være nødvendigt at opdatere siden). I tabellen skal du vælge begge salgsordrer ved hjælp af sektionmærket.
    - I handlingsruden skal du i **Alle salgsordrer** vælge fanen **Lagersted**.
    - I gruppen **Handlinger** skal du vælge **Frigiv til lagersted** for at frigive salgsordrer til lagerstedet.
1. Når frigivelsen til lagerstedsprocessen er fuldført, vises der en meddelelse med oplysninger.
    - Der oprettes forsendelser for hver salgsordre.
    - Der oprettes en bølge, og begge forsendelser tildeles bølgen. Notér dig **Bølge-id**.
1. Gå til **Lokationsstyring > Udgående bølger > Forsendelsesbølger > Alle bølger**.
    - På listen **Alle bølger** skal du finde og vælge det **Bølge-id**, du oprettede i forrige trin.
    - I handlingsruden skal du vælge fanen **Bølge**,
    - I gryppen **Bølge** skal du vælge **Proces** for at behandle bølgen og oprette **Arbejde**.
    - Der genereres oplysningsmeddelelser, når behandlingen er udført, hvilket angiver, at der er oprettet arbejde, og at bølgen er blevet bogført.
1. **Valgfrit**: Gå til **Lokationsstyring > Arbejde > Arbejdsoplysninger** for at få vist det oprettede arbejde. Der oprettes to forskellige arbejds-ID'er. Hvert arbejds-ID har to pluklinjer.

### <a name="run-the-mobile-device-flow"></a>Kør mobilenhedsprocessen

1. Log på mobilenheden for en bruger på lagerstedet **62**.
1. I **Hovedmenuen** skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **SD-klynge** for at starte plukningen.
    - Der oprettes en klynge, og de to arbejds-id'er, du har oprettet tidligere, tilknyttes. Hvis du har oprettet mere end to arbejds-ID'er, føjes kun de første to til klyngen. Bemærk, at arbejds-ID'erne føjes til klyngen i stigende rækkefølge, som du angav i forespørgselsopsætningen.

    > [!NOTE]
    > Den nye klynge oprettes kun automatisk, hvis der tidligere er oprettet nok ekstra arbejds-ID'er. Ellers vises følgende meddelelse: "Der kan ikke findes nok arbejde for klyngen".

    - Når du har valgt menuen, vises det første pluk-skærmbillede. Systemet samler alle matchende pluklinjer fra de to arbejds-ID'er og dirigerer dig til at besøge plukstedet én gang, så du kan opfylde begge ordrer ved at bruge ét pluk. Denne proces udføres på samme måde som processen for brugerbaseret klyngeplukning.

1. Bekræft den første plukplads og vare ved at vælge **OK**.
    - Plukantallet vil være totalen for den vare, der vises på salgsordrerne i klyngen.
1. Angiv stillingsnavnet (numerisk eller alfabetisk) for at bekræfte, at det vareantal, der er plukket til stillingen, blev indsat på den korrekte position.
1. Gentag denne proces, indtil alle vareantal er plukket og sat i den korrekte position.
1. Det sidste trin på mobilenheden er at **Lægge** klyngen på lager i den endelige stilling. Vælg **OK**
    - Når læg på lager-handlingen er bekræftet, lukkes og brydes klyngen på basis af den værdi, du har angivet for feltet **Bryd klynge ved** i klyngeprofilen. Arbejds-ID'er lukkes også.
1. Meddelelsen "Klynge fuldført" vises på mobilenheden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]