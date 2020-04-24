---
title: Arbejdsordrepuljer
description: I dette emne beskrives, hvordan du kan arbejde med arbejdsordrepuljer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: debff2d6ec9c9e3ba711f62ffefab0546dbd2346
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208863"
---
# <a name="work-order-pools"></a>Arbejdsordrepuljer

[!include [banner](../../includes/banner.md)]


Du kan bruge arbejdsordrepuljer til at gruppere arbejdsordrer, der har noget fælles. Her er nogle eksempler på ting, du kan oprette arbejdsordrepuljer til:

- Arbejdshold, f.eks. Vedligeholdelseshold A eller Vedligeholdelseshold B  

- Faglige kompetencer, f.eks. elektrikere eller VVS-folk  

- Fysiske adresser  

- Tidsplaner, f.eks. uger eller andre perioder  

Når du har brug for det, kan du anbringe én arbejdsordre i flere arbejdsordrepuljer.


## <a name="create-a-work-order-pool"></a>Oprette en arbejdsordrepulje

På siden **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer** kan du få en oversigt over dine arbejdsordrepuljer og oprette nye puljer.

1. Vælg **Styring af aktiver** > **Almindelig** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer**.

2. Vælg **Ny**.

3. Angiv et id for arbejdsordrepuljen i feltet **Pulje**.

4. Indtast et navn i feltet **Navn**.

5. Indstil **Aktiv** til **Ja** for at angive, at arbejdsordrepuljen er aktiv.

6. Indstil **Slet arbejdsordrerelationer** til **Ja**, hvis arbejdsordrer automatisk skal fjernes fra arbejdsordrepuljen.

7. I feltet **Slet livscyklustilstand** skal du vælge livscyklustilstanden for arbejdsordren. For eksempel kan livscyklustilstanden for færdiggørelse af en arbejdsordre indstilles til automatisk at slette relationer til arbejdsordrepuljer.

    Du kan begynde at føje arbejdsordrer til din arbejdsordrepulje med det samme.

8. Vælg **Tilføj linje** i oversigtspanelet **Arbejdsordrer**.

9. I feltet **Arbejdsordre** skal du vælge en arbejdsordre. De relaterede felter opdateres automatisk.

10. Gentag trin 8 til 9 for at tilføje flere arbejdsordrer.

11. Hvis de arbejdsordrer, du har tilføjet, skal udføres i en bestemt rækkefølge, kan du i feltet **Sorteringsrækkefølge** angive numrene **1**, **2**, **3** osv. for at angive den pågældende rækkefølge.

12. Hvis du vil have vist en liste over alle de arbejdsordrer, der er medtaget i arbejdsordrepuljen, skal du vælge **Arbejdsordrer** i gruppen **Vis relateret til arbejdsordrepulje** under fanen **Arbejdsordrepulje** i handlingsruden for at åbne siden **Alle arbejdsordrer**.

13. Hvis du vil beregne og se kapacitetsbelastningen for vedligeholdelsesplanen, ikke-planlagte arbejdsordrer og planlagte arbejdsordrer, skal du i handlingsruden under fanen **Arbejdsordrepulje** i gruppen **Vis relateret til arbejdsordrepulje** vælge **Kapacitetsbelastning** for at åbne dialogboksen **Beregn kapacitetsbelastning**.

14. Hvis du vil beregne og se prognoser for varer (reservedele og andre påkrævede varer), der er relateret til vedligeholdelsesplanen, ikke-planlagte arbejdsordrer og planlagte arbejdsordrer, skal du i handlingsruden under fanen **Arbejdsordrepulje** i gruppen **Vis relateret til arbejdsordrepulje** vælge **Varebudget** for at åbne dialogboksen **Beregn varebudget**.

15. Hvis du vil have vist en liste over indkøbsrekvisitioner, der er relatere til arbejdsordrer i arbejdsordrepuljen, skal du vælge **Indkøbsrekvisition for arbejdsordre** i gruppen **Indkøb** under fanen **Arbejdsordrepulje** i handlingsruden for at åbne siden **Indkøbsrekvisition for arbejdsordre**.

16. Hvis du vil have vist en liste over indkøbsordrer, der er relatere til arbejdsordrer i arbejdsordrepuljen, skal du vælge **Arbejdsordreindkøb** i gruppen **Indkøb** under fanen **Arbejdsordrepulje** i handlingsruden for at åbne siden **Arbejdsordreindkøb**.

>[!NOTE]
>Når en arbejdsordrepulje ikke længere er relevant for din arbejdsplanlægning, skal du indstille **Aktiv** til **Nej** for den pågældende pulje i listevisningen på siden **Arbejdsordrepulje**.

Hvis du vil slette alle linjer i en arbejdsordre, skal du angive indstillingen **Slet arbejdsordrerelationer** til **Ja**. Denne indstilling er nyttig, hvis du f.eks. vil oprette en tom pulje, som du senere kan bruge til andre arbejdsordrer. Husk at indstille **Slet arbejdsordrerelationer** til **Nej**, hvis du vil bruge arbejdsordrepuljen til at oprette nye arbejdsordrerelationer på et senere tidspunkt.

I illustrationen herunder vises et eksempel på listesiden **Arbejdsordrepulje**.

![Figur 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Føje en arbejdsordre til en arbejdsordrepulje

Som beskrevet i ovenstående afsnit kan du føje arbejdsordrer til en arbejdsordrepulje, når du opretter puljen. Du kan også føje arbejdsordrer til en arbejdsordre pulje på listesiden **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

1. Vælg arbejdsordren, og vælg derefter **Arbejdsordrepulje** i gruppen **Vedligehold** under fanen **Arbejdsordre** i handlingsruden.

2. Vælg arbejdsordren på listen, og klik på **Arbejdsordrepulje**.

3. Vælg **Tilføj** i feltet **Tilføj/fjern** i dialogboksen **Vedligehold arbejdsordrepulje**.

4. Vælg arbejdsordrepuljen i feltet **Pulje**.

5. Vælg **OK**.

6. Hvis du vil placere den arbejdsordre, du har tilføjet, i en bestemt rækkefølge i arbejdsordrepuljen, skal du vælge puljen på listesiden **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer** og derefter vælge **Rediger**. Brug derefter feltet **Sorteringsrækkefølge** i oversigtspanelet **Arbejdsordrer** på siden **Arbejdsordrepulje** til at justere sorteringsrækkefølgen af de arbejdsordrer, der skal medtages i puljen.

Hvis du vil fjerne en arbejdsordre fra en arbejdsordrepulje, skal du gentage disse trin, men vælge **Fjern** i trin 3.

