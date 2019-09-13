---
title: Arbejdsordrepuljer
description: I dette emne beskrives, hvordan du kan arbejde med arbejdsordrepuljer i Styring af aktiver.
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
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875568"
---
# <a name="work-order-pools"></a>Arbejdsordrepuljer


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Du kan bruge arbejdsordrepuljer til at gruppere arbejdsordrer, der har noget fælles. Du kan f.eks. oprette arbejdsordrepuljer for

- arbejdshold, f.eks. Vedligeholdelseshold A, Vedligeholdelseshold B  

- fagligt kvalificerede, f.eks. elektrikere eller VVS-folk  

- fysiske placeringer  

- tidsplaner, f.eks. uger eller andre perioder  


Hvis det er nødvendigt, kan én arbejdsordre placeres i mange arbejdsordrepuljer.


## <a name="create-work-order-pool"></a>Oprette arbejdsordrepulje

I **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer** kan du få en oversigt over dine arbejdsordrepuljer og oprette nye puljer.

1. Klik på **Styring af aktiver** > **Almindelig** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer**.

2. Klik på **Ny**.

3. Indsæt et arbejdsordrepulje-id i feltet **Pulje** og et navn i feltet **Navn**.

4. Vælg "Ja" på **Aktiv**-til/fra-knappen for at angive, at arbejdsordrepuljen er aktiv.

5. Vælg "Ja" på til/fra-knappen **Slet arbejdsordrerelationer**, hvis du ønsker, at arbejdsordrer automatisk skal fjernes fra arbejdsordrepuljen.

6. I feltet **Slet livscyklustilstand** skal du vælge livscyklustilstanden for arbejdsordren. For eksempel kan livscyklustilstanden for færdiggørelse af en arbejdsordre indstilles til automatisk at slette relationer til arbejdsordrepuljer.

7. Du kan begynde at føje arbejdsordrer til din arbejdsordrepulje med det samme. Klik på **Tilføj linje** i oversigtspanelet **Arbejdsordrer**.

8. I feltet **Arbejdsordre** skal du vælge en arbejdsordre. De relaterede felter opdateres automatisk.

9. Gentag trin 7-8, hvis du vil tilføje flere arbejdsordrer.

10. I feltet **Sorteringsrækkefølge** kan du angive, om arbejdsordrerne skal udføres i en bestemt rækkefølge. Indsæt nummer 1, 2, 3 osv. for at angive en bestemt rækkefølge for de valgte arbejdsordrer.

11. Klik på knappen **Arbejdsordrer** for at få vist en liste over alle de arbejdsordrer, der er inkluderet i arbejdsordrepuljen.

12. Klik på knappen **Kapacitetsbelastning** for at åbne **Kapacitetsbelastning** og beregne og få vist kapacitetsbelastningen for vedligeholdelsesplanen, ikke-planlagte arbejdsordrer og planlagte arbejdsordrer.

13. Klik på knappen **Varebudget** for at åbne **Varebudget** og beregne og få vist budgetter for varer (reservedele og andre påkrævede varer), der er relateret til vedligeholdelsesplanen, ikke-planlagte arbejdsordrer og planlagte arbejdsordrer.

14. Klik på knappen **Indkøbsrekvisition i arbejdsordre** for at åbne listen **Indkøbsrekvisition i arbejdsordre** for at få vist en liste over indkøbsrekvisitioner, der er relateret til arbejdsordrerne i arbejdsordrepuljen.

15. Klik på knappen **Indkøb i arbejdsordre** for at åbne listen **Indkøb i arbejdsordre** og få vist en liste over indkøbsordrer, der er relateret til arbejdsordrerne i arbejdsordrepuljen.

>[!NOTE]
>Når en arbejdsordrepulje ikke længere er relevant for din arbejdsplanlægning, skal du vælge "Nej" i afkrydsningsfeltet **Aktiv** for den pågældende pulje i listevisningen **Arbejdsordrepulje**.

Marker afkrydsningsfeltet **Slet arbejdsordrerelationer**, hvis du vil slette alle arbejdsordrelinjer, f.eks. for at oprette en tom pulje, som du senere kan bruge til andre arbejdsordrer. Husk at fjerne markeringen i afkrydsningsfeltet **Slet arbejdsordrerelationer**, hvis du vil bruge arbejdsordrepuljen til at oprette nye arbejdsordrerelationer på et senere tidspunkt.


![Figur 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Føje en arbejdsordre til en arbejdsordrepulje

Som beskrevet i ovenstående afsnit kan du føje arbejdsordrer til en arbejdsordrepulje, når du opretter puljen. Du kan også føje en arbejdsordre til en arbejdsordrepulje fra en af **Alle arbejdsordrer** på listen.

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren på listen, og klik på **Arbejdsordrepulje**.

3. Vælg "Tilføj" i feltet **Tilføj/fjern**.

4. Vælg arbejdsordrepuljen i feltet **Pulje**.

5. Klik på **OK**.

6. Når du har føjet en arbejdsordre til en arbejdsordrepulje, og du vil placere arbejdsordren i en bestemt rækkefølge i puljen: Åbn en af listesiderne for arbejdsordrepuljer, vælg puljen, og klik på **Rediger**, og juster sorteringsrækkefølgen for arbejdsordrerne i puljen i formularen **Arbejdsordrepulje** > oversigtspanelet **Arbejdsordrer** > feltet **Sorteringsrækkefølge**.

Hvis du vil fjerne den valgte arbejdsordre fra en arbejdsordrepulje, skal du vælge "Fjern" i trin 3.

