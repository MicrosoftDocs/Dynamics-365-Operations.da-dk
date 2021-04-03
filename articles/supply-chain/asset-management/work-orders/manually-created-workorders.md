---
title: Manuelt oprettede arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer manuelt i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b704699c5e04f38c3b79691f935287f8f9c24fba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263704"
---
# <a name="manually-created-work-orders"></a>Manuelt oprettede arbejdsordrer

[!include [banner](../../includes/banner.md)]


Du kan oprette arbejdsordre manuelt på to måder:

- På siden **Alle arbejdsordrer** eller **Aktive arbejdsordrer** 
- På siden **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder** 

## <a name="create-work-order"></a>Opret arbejdsordre

1. Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg **Ny**.

3. I dialogboksen **Opret arbejdsordre** skal du vælge en arbejdsordretype i feltet **Arbejdsordretype**.

4. Vælg evt. en **Beskrivelse**.

5. Vælg aktivet i feltet **Aktiv**.

>[!NOTE]
>Når du vælger et aktiv, kan der være tre faner tilgængelige i rullemenuen **Aktiv**: 

- **Aktive aktiver** - Denne fane indeholder en liste over alle aktiver med status som "Aktiv" for aktivets livscyklustilstand. 
- **Aktiv visning** - Denne fane har en trævisning af arbejdssteder og de aktiver, der er installeret på dem.
- **Mine aktiver** - Denne fane indeholder aktiver, der er relateret til de arbejdssteder, som du (den arbejder, der er logget på systemet), kan blive allokeret til. Du kan finde oplysninger om opsætningen under [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md). Hvis der ikke er konfigureret nogen arbejdssteder i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md), er fanen **Mine aktiver** ikke tilgængelig. 

6. Vælg en vedligeholdelsesjobtype for arbejdsordren i feltet **Vedligeholdelsesjobtype**.

7. Vælg om nødvendigt **Vedligeholdelsesjobtypevariant** og **Fag**.

8. Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.

9. Vælg **Forventet startdato** og **Forventet slutdato** i de relaterede felter.

10. Klik på **OK** for at oprette arbejdsordren.

11. På siden **Alle arbejdsordrer** kan du redigere arbejdsordren, som du har brug for.

Vær opmærksom på følgende punkter:

- I detaljevisningen på listesiden **Alle arbejdsordrer** kan du føje flere aktiver til en arbejdsordre ved at tilføje linjer i oversigtspanelet **Vedligeholdelsesjob for arbejdsordrer**. I et aktiv kan du kun vælge de vedligeholdelsesjobtyper, der er defineret i den aktivtype, der er valgt på aktivet.  

- Hvis du ændrer et aktivserviceniveau eller en aktivkritikalitet, efter at du har brugt aktivet på en arbejdsordre, opdateres serviceniveauet eller kritikaliteten ikke på arbejdsordren i overensstemmelse hermed. Du kan finde flere oplysninger om serviceniveauer og kritikaliteter under [Serviceniveauer for aktiv](../setup-for-objects/object-priorities.md) og [Kritikalitetstyper for aktiver](../setup-for-objects/object-criticalities.md).

- Kritikaliteten på en arbejdsordre genberegnes, hver gang et arbejdsordrejob føjes til eller slettes fra arbejdsordren.

- I detaljevisningen **Alle arbejdsordrer** > fanen **Hoved** > oversigtspanelet **Tidsplan** kan du vælge en ansvarlig vedligeholdelsesarbejdergruppe eller en ansvarlig vedligeholdelsesarbejder i feltet **Ansvarlig gruppe** eller **Ansvarlig**. Disse indstillinger kan ændres, mens arbejdsordren er aktiv. De kan f.eks. ændres, når livscyklustilstanden for arbejdsordren ændres. Det automatiske valg, der foretages under oprettelsen af en arbejdsordre, baseres på opsætningen på siden **Ansvarlige vedligeholdelsesarbejdere**. Hvis du tilføjer eller fjerner arbejdsordrejob, efter at du har oprettet en arbejdsordre, og hvis felterne **Ansvarlig gruppe** og **Ansvarlig** er tomme, når du opdaterer arbejdsordren, søger funktionen Styring af aktiver efter et en ansvarlig vedligeholdelsesarbejdergruppe eller en ansvarlig vedligeholdelsesarbejder på opsætningssiden. Hvis feltet **Ansvarlig gruppe** eller **Ansvarlig** allerede er udfyldt, når du opdaterer arbejdsordren, foretages der ingen ændringer. Du finder flere oplysninger om ansvarlige vedligeholdelsesarbejdere og arbejdergrupper i [Ansvarlige vedligeholdelsesarbejdere](../setup-for-maintenance-requests/responsible-workers.md).

- På siden [Vedligeholdelsesstatus](../controlling-and-reporting/maintenance-status.md) kan du foretage en beregning for at få en oversigt over arbejdsbyrden for indgående og fuldførte arbejdsordrer.  

- Du kan bruge felterne **Breddegrad** og **Længdegrad** i oversigtspanelet **Linjedetaljer** i den detaljerede visning af siden **Alle arbejdsordrer** til at tilføje geografiske koordinater for det aktiv, der er valgt på arbejdsordrejobbet.  


## <a name="create-related-work-order"></a>Opret relateret arbejdsordre

Du kan oprette en arbejdsordre, der er relateret til en eksisterende arbejdsordre. Dette er nyttigt, hvis du f.eks. vil arbejde med primære og sekundære arbejdsordrer. En ny arbejdsordre er baseret på et arbejdsordrejob fra en eksisterende arbejdsordre.

1. Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg den arbejdsordre, du vil oprette en relateret arbejdsordre for.

3. Vælg **Relateret arbejdsordre** i gruppen **Ny** under fanen **Arbejdsordre** i handlingsruden.

4. I dialogboksen **Opret relateret arbejdsordre** skal du vælge det arbejdsordrejob, som du vil oprette en relateret arbejdsordre for, i feltet **Arbejdsordrejob**.

5. Vælg en vedligeholdelsesjobtype i feltet **Vedligeholdelsesjobtype**.

6. I felterne **Vedligeholdelsesjobtypevariant** og **Fag** skal du vælge den variant og det fag, der er relateret til vedligeholdelsesjobtypen.

7. Hvis denne arbejdsordre er den første relaterede arbejdsordre, der er oprettet for den valgte arbejdsordre, skal du følge disse trin:
    1. Vælg indstillingen **Ny arbejdsordre**.
    2. I feltet **Arbejdsordretype** skal du vælge en arbejdsordretype.
    3. Indtast en beskrivelse i feltet **Beskrivelse**.
    4. Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.
    5. Vælg start- og slutdatoerne i felterne **Forventet start** og **Forventet afslutning**.
    6. Vælg **OK**. Den nye relaterede arbejdsordre vises på listesiden **Alle arbejdsordrer**.  

8. Hvis den arbejdsordre, du opretter denne relaterede arbejdsordre for, allerede har relaterede arbejdsordrer, skal du udføre følgende trin for at føje et nyt arbejdsordrejob til en eksisterende relateret arbejdsordre:
    1. Vælg indstillingen **Føj til relateret arbejdsordre**.
    2. Vælg den relaterede arbejdsordre, som du vil føje et nyt arbejdsordrejob til, i feltet **Arbejdsordre**.
    3. Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.
    4. Ret start- og slutdatoerne eftr behov i felterne **Forventet start** og **Forventet afslutning**.
    5. Vælg **OK**. Arbejdsordrejobbet føjes til den eksisterende relaterede arbejdsordre.

I illustrationen herunder vises et eksempel på dialogboksen **Opret relateret arbejdsordre**.

![Figur 1](media/03-work-orders.png)

>[!NOTE]
>Hvis du har oprettet en relateret arbejdsordremaske i **Parametre til aktivstyring** > **Arbejdsordrer**-fanen > feltet **Relateret arbejdsordremaske**, oprettes arbejdsordre-id'er i overensstemmelse med maskeopsætningen. Hvis der ikke er konfigureret nogen tilknyttet arbejdsordremaske, bruges det næste tilgængelige arbejdsordre-id til relaterede arbejdsordrer.

## <a name="copy-a-work-order"></a>Kopiere en arbejdsordre

Du kan hurtigt at oprette en ny arbejdsordre ud fra en eksisterende arbejdsordre. Denne måde at arbejde med arbejdsordrer på er ikke den samme, som når du opretter arbejdsordrer på basis af [vedligeholdelsesplaner](../preventive-and-reactive-maintenance/maintenance-plans.md). Den er nyttig, hvis du f.eks. har en arbejdsordre, der indeholder mange arbejdsordrejob, og de forskellige job skal udføres på forskellige aktiver med jævne mellemrum.

1. Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg den arbejdsordre, du vil kopiere indhold fra.

3. Vælg **Kopiér arbejdsordre** i gruppen **Ny** under fanen **Arbejdsordre** i handlingsruden.

4. Arbejdsordreopsætningen fra den valgte arbejdsordre vises. Hvis det er nødvendigt, kan du redigere nogle af felterne.

5. Vælg **OK** for at oprette den nye arbejdsordre.

6. På siden **Alle arbejdsordrer** kan du redigere arbejdsordren, som du har brug for.

>[!NOTE]
>Når den nye arbejdsordre oprettes, kopieres nogle oplysninger direkte fra den eksisterende arbejdsordre. Oplysninger om budgetter, værktøjer, vedligeholdelsestjeklister, arbejdssted, adresser og planlægning kopieres ikke. De er i stedet initialiseret fra den aktuelle opsætning i aktivstyring. Hvis disse oplysninger derfor er ændret mellem det tidspunkt, hvor den første arbejdsordre blev oprettet, og det tidspunkt, hvor du oprettede en kopi af arbejdsordren, medtages ændringerne i den nye arbejdsordre. Eksempler er ændringer i prognoser og opdaterede vedligeholdelsestjeklister.

I illustrationen nedenfor vises et eksempel på dialogboksen **Kopiér arbejdsordre**.

![Figur 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Oprette en arbejdsordre baseret på en vedligeholdelsesanmodning

1. Vælg **Styring af aktiver** > **Almindeligt** > **Vedligeholdelsesanmodninger** > **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.

2. Vælg de vedligeholdelsesanmodninger, du vil oprette en arbejdsordre for, og klik på **Rediger**.

3. Vælg **Arbejdsordre** i gruppen **Ny** under fanen **Vedligeholdelsesanmodning** i handlingsruden.

4. Udfyld felterne i dialogboksen **Arbejdsordre**. Hvis der er valgt en vedligeholdelsesjobtype i vedligeholdelsesanmodningen, kan du vælge en anden type vedligeholdelsesjob, hvis det er nødvendigt, når du opretter arbejdsordren.

5. Vælg **OK**. Meddelelsen fortæller dig, at salgsordren er blevet oprettet.

6. Hvis du vil se de arbejdsordrer, der er knyttet til en vedligeholdelsesanmodning, skal du vælge vedligeholdelsesanmodningen på listen **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**. Vælg derefter **Arbejdsordrer** i gruppen **Vis** under fanen **Vedligeholdelsesanmodning** i handlingsruden.


I illustrationen nedenfor vises et eksempel på dialogboksen **Opret arbejdsordre**.

![Figur 3](media/05-work-orders.png)


>[!NOTE]
>Du kan også oprette arbejdsordrer automatisk ved at planlægge vedligeholdelsesplanjob eller ved at konfigurere "Automatisk oprettelse" af [vedligeholdelsesplaner](../preventive-and-reactive-maintenance/maintenance-plans.md) eller [vedligeholdelsesrunder](../preventive-and-reactive-maintenance/maintenance-rounds.md) for et aktiv. Arbejdsordrer, der er oprettet ud fra vedligeholdelsesanmodninger på siden **Hele vedligeholdelsestidsplanen**, har de vedligeholdelsesjobtyper, der er valgt i vedligeholdelsesanmodningerne.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]