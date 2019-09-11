---
title: Manuelt oprettede arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer manuelt i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875566"
---
# <a name="manually-created-work-orders"></a>Manuelt oprettede arbejdsordrer

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Du kan oprette arbejdsordre manuelt på to måder:

- i **Alle arbejdsordrer** eller **Aktive arbejdsordrer**  
- i **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder**.  

## <a name="create-work-order"></a>Opret arbejdsordre

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Klik på knappen **Nyt**.

3. Vælg en arbejdsordretype på rullelisten **Opret arbejdsordre**.

4. Vælg evt. en beskrivelse.

5. Vælg aktivet for arbejdsordren samt en vedligeholdelsesjobtype.

>[!NOTE]
>Når du vælger et aktiv, er der som regel tre tilgængelige faner: Fanen **Mine aktiver** indeholder aktiver, der er relateret til de arbejdssteder, som du (den vedligeholdelsesarbejder, som er logget på systemet) kan allokeres til (konfigureres i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md)). Hvis der ikke er konfigureret noget arbejdssted for en arbejder i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md), er fanen **Mine aktiver** ikke synlig. Fanen **Aktive aktiver** indeholder en liste over alle aktiver med status som "Aktiv" for aktivers livscyklus. Fanen **Aktiv visning** viser en trævisning af arbejdssteder og aktiver, der er installeret på disse steder.

6. Vælg om nødvendigt **Vedligeholdelsesjobtypevariant** og **Fag**.

7. Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.

8. Vælg de forventede start- og slutdatoer i de relaterede felter.

9. Klik på **OK** for at oprette en ny arbejdsordre.

10. Rediger evt. arbejdsordren i **Alle arbejdsordrer**.

- I **Alle arbejdsordrer** kan du føje flere anlægsaktiver til en arbejdsordre i visningen Detaljer ved at tilføje linjer i oversigtspanelet **Vedligeholdelsesjob for arbejdsordrer**. I et anlægsaktiv kan du kun vælge de vedligeholdelsesjobtyper, der er defineret i den aktivtype, der er valgt for aktivet.  
- Hvis du har ændret et aktivs serviceniveau eller et aktiv kritisk, efter at du har brugt dem i en arbejdsordre (se [Serviceniveauer for aktiv](../setup-for-objects/object-priorities.md) og [Kritikaliteter for aktiver](../setup-for-objects/object-criticalities.md)), opdateres serviceniveauet eller kritikaliteten for arbejdsordren ikke tilsvarende.
- Kritikaliteten på en arbejdsordre genberegnes, hver gang en arbejdsordrelinje føjes til eller slettes fra arbejdsordren.
- I detaljevisningen **Alle arbejdsordrer** > visningen **Hoved** > oversigtspanelet **Tidsplan** kan du vælge en ansvarlig medarbejdergruppe eller en ansvarlig vedligeholdelsesarbejder i feltet **Ansvarlig gruppe** eller **Ansvarlig**. Disse indstillinger kan ændres, så længe arbejdsordren er aktiv, f.eks. når livscyklustilstanden for arbejdsordren ændres. Det automatiske valg, der foretages under oprettelsen af en arbejdsordre, baseres på opsætningen af **Ansvarlige vedligeholdelsesarbejdere**. Hvis du tilføjer eller fjerner arbejdsordrejob, efter at du har oprettet en arbejdsordre, og feltet **Ansvarlig gruppe** og feltet **Ansvarlig** er tomme, når du opdaterer arbejdsordren, søger funktionen til administration af aktiver efter et muligt match i opsætningsformularen for en ansvarlig medarbejdergruppe eller en ansvarlig vedligeholdelsesarbejder. Hvis feltet **Ansvarlig gruppe** eller feltet **Ansvarlig** allerede er udfyldt, når du opdaterer arbejdsordren, foretages der ingen ændringer. 

- I **Vedligeholdelsesstatus** kan du foretage en beregning for at få en oversigt over arbejdsbyrder i forbindelse med indgående og fuldførte arbejdsordrer.  

- I oversigtspanelet **Linjedetaljer** kan du bruge felterne **Breddegrad** og **Længdegrad** til at tilføje geografiske koordinater for det aktiv, der er valgt i arbejdsordrejobbet.  

## <a name="create-related-work-order"></a>Opret relateret arbejdsordre

Du kan oprette en relateret arbejdsordre til en eksisterende arbejdsordre, hvis du f.eks. vil arbejde med primære og sekundære arbejdsordrer. En ny arbejdsordre er baseret på et arbejdsordrejob fra en eksisterende arbejdsordre.

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg den arbejdsordre, som du vil oprette en relateret arbejdsordre for.

3. Klik på **Relateret ordre**.

4. I rulledialogboksen **Opret relateret arbejdsordre** skal du vælge det arbejdsordrejob, som du vil oprette en relateret arbejdsordre for, i feltet **Arbejdsordrejob**.

5. Vælg en vedligeholdelsesjobtype feltet **Vedligeholdelsesjobtype** og, hvis det er nødvendigt, en relateret variant af vedligeholdelsesjobtypen og -faget i felterne **Vedligeholdelsesjobtypevariant** og **Fag**.

6. Hvis dette er den første relaterede arbejdsordre, du opretter, skal du klikke på alternativknappen **Ny arbejdsordre**.

7. Vælg en **Arbejdsordretype** og en **Beskrivelse** i de relaterede felter.

8. Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.

9. Indsæt de forventede start- og slutdatoer i de relaterede felter.

10. Klik på **OK**. Den nye relaterede arbejdsordre vises på listen **Alle arbejdsordrer**.

11. Hvis du opretter en relateret arbejdsordre på en arbejdsordre, der allerede har relaterede arbejdsordrer, kan du føje arbejdsordrejobbet til en allerede relateret arbejdsordre. Dette gøres ved at klikke på alternativknappen **Føj til relateret arbejdsordre** i trin 6. Derefter skal du vælge den relaterede arbejdsordre, som du vil føje et nyt arbejdsordrejob til. Rediger felterne **Serviceniveau**, **Forventet startdato** og **Forventet slutdato** efter behov, og klik på **OK**. Arbejdsordrejobbet føjes til den eksisterende relaterede arbejdsordre.


![Figur 1](media/03-work-orders.png)

**Bemærk!** Hvis du har oprettet en relateret arbejdsordremaske i **Parametre til aktivstyring** > **Arbejdsordrer**-linket > feltet **Relateret arbejdsordremaske**, oprettes arbejdsordre-id'er i overensstemmelse med maskeopsætningen. Hvis der ikke er konfigureret nogen tilknyttet arbejdsordremaske, bruges det næste tilgængelige ordre-id til relaterede arbejdsordrer.

## <a name="copy-work-order"></a>Kopiér arbejdsordre

Det er muligt hurtigt at oprette en ny arbejdsordre ud fra en eksisterende arbejdsordre. Denne måde at arbejde med arbejdsordrer på er ikke den samme, som når du opretter arbejdsordrer på basis af vedligeholdelsesplaner. Den er nyttig, hvis du f.eks. har en arbejdsordre, der indeholder mange arbejdsordrejob med forskellige job på forskellige aktiver, der skal udføres med jævne mellemrum.

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg den arbejdsordre, du vil kopiere indhold fra.

3. Klik på **Kopiér arbejdsordre**. Arbejdsordreopsætningen fra den valgte arbejdsordre vises. Hvis det er nødvendigt, kan du redigere nogle af felterne.

4. Klik på **OK** for at oprette den nye arbejdsordre.

5. Rediger evt. arbejdsordren i **Alle arbejdsordrer**.

>[!NOTE]
>Når den nye arbejdsordre oprettes, kopieres nogle oplysninger direkte fra den eksisterende arbejdsordre. Oplysninger om prognoser, værktøjer, vedligeholdelsestjeklister, arbejdssted, adresser og planlægning kopieres ikke, men initialiseres fra den aktuelle opsætning i Styring af aktiver. Det betyder, at hvis der er foretaget ændringer i disse data fra tidspunktet for oprettelsen af den første arbejdsordre, indtil du tog en kopi af arbejdsordren, medtages disse ændringer i den nye arbejdsordre, du har oprettet. Eksempler er ændringer i prognoser eller opdaterede vedligeholdelsestjeklister.


![Figur 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Oprette en arbejdsordre baseret på en vedligeholdelsesanmodning

1. Klik på **Styring af aktiver** > **Almindeligt** > **Vedligeholdelsesanmodninger** > **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.

2. Vælg de vedligeholdelsesanmodninger, du vil oprette en arbejdsordre for, og klik på **Rediger**.

3. I **Alle anmodninger** skal du klikke på **Arbejdsordre**.

4. Udfyld rullelisten **Arbejdsordre**. Hvis der er valgt en vedligeholdelsesjobtype i vedligeholdelsesanmodningen, kan du vælge en anden type vedligeholdelsesjob, hvis det er nødvendigt, når du opretter arbejdsordren.

5. Klik på **OK**. Der vises en meddelelse om, at arbejdsordren er blevet oprettet.

6. Hvis du vil se, hvilke arbejdsordrer der er knyttet til en vedligeholdelsesanmodning, skal du vælge vedligeholdelsesanmodningen på listen **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** og klikke på knappen **Arbejdsordrer**.


![Figur 3](media/05-work-orders.png)


>[!NOTE]
>Du kan også oprette arbejdsordrer automatisk ved at planlægge vedligeholdelsesplanjob eller ved at konfigurere "Automatisk oprettelse" af vedligeholdelsesplaner eller vedligeholdelsesrunder for et aktiv. Arbejdsordrer, der er oprettet ud fra vedligeholdelsesanmodninger i **Vedligeholdelsestidsplan**, oprettes med de vedligeholdelsesjobtyper, der er valgt i vedligeholdelsesanmodningerne.

