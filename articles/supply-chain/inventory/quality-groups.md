---
title: Varekvalitetsgrupper
description: Dette emne beskriver, hvordan du kan bruge og oprette varekvalitetsgrupper til logisk gruppering af produkter, så de kan tildeles til kvalitetstilknytninger med henblik på automatisk generering af kvalitetsordrer.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022246"
---
# <a name="item-quality-groups"></a>Varekvalitetsgrupper

[!include [banner](../includes/banner.md)]

En kvalitetsgruppe repræsenterer almindelige testkrav til varer. Dette emne beskriver, hvordan du kan bruge og oprette varekvalitetsgrupper til logisk gruppering af produkter, så de kan tildeles til kvalitetstilknytninger med henblik på automatisk generering af kvalitetsordrer.

Hvis du vil konfigurere, redigere og have vist de varer, der er tildelt en kvalitetsgruppe, eller de kvalitetsgrupper, der er tildelt en vare, skal du gå til **Lagerstyring \> Opsætning \> Kvalitetsgrupper**. Når du har defineret testkravene på siden **Testgrupper**, kan du definere reglerne for automatisk generering af kvalitetsordrer. For at forenkle processen skal du undlade at definere regler for de enkelte varer. I stedet kan du definere regler for en kvalitetsgruppe på siden **Kvalitetstilknytninger**.

## <a name="example-of-an-item-quality-group"></a>Eksempel på en varekvalitetsgruppe

En produktionsvirksomhed indkøber forskellige råvarer, der har samme testkrav til indgående inspektion. Virksomheden definerer derfor en kvalitetsgruppe og tildeler derefter kvalitetsgruppen de varenumre, der er tilknyttet råmaterialer for den pågældende gruppe. Senere indkøber virksomheden en ny type råvarer med de samme testkrav. I stedet for at konfigurere nye testkrav til de nye råvarer føjer virksomheden varenummeret på de nye råvarer til den eksisterende kvalitetsgruppe.

Den samme virksomhed producerer desuden varer med de samme produktionstestkrav og leverer varer med de samme testkrav før forsendelse. Virksomheden definerer derfor yderligere to kvalitetsgrupper og tildeler derefter hver gruppe de relevante varenumre.

## <a name="create-a-quality-group"></a>Oprette en kvalitetsgruppe

Benyt denne fremgangsmåde for at oprette en kvalitetsgruppe.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetsgrupper**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Kvalitetsgruppe** – Angiv et entydigt id eller navn til kvalitetsgruppen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af kvalitetsgruppen.

1. Luk siden.

## <a name="manually-add-items-to-a-quality-group"></a>Tilføje varer manuelt til en kvalitetsgruppe

Hvis du vil føje varer manuelt til en kvalitetsgruppe, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetsgrupper**.
1. Vælg den kvalitetsgruppe, du vil føje varer til.
1. Vælg **Varer** i handlingsruden.
1. På siden **Varer i kvalitetsgruppe** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret. Derefter skal du for den nye række indstille feltet **Varenummer** til det varenummer, du vil tilføje.
1. Gentag forrige trin for hver ekstra vare, du vil tilføje.
1. Luk siderne.

## <a name="add-multiple-items-to-a-quality-group"></a>Tilføje flere varer til en kvalitetsgruppe

Hvis du vil føje flere varer til en kvalitetsgruppe, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetsgrupper**.
1. Opret eller vælg den kvalitetsgruppe, du vil føje varer til.
1. Vælg **Tilføj varer** i handlingsruden.
1. Angiv filtreringskriterierne for de varer, du vil tilføje, i dialogboksen **Forespørgsel**. Du kan f.eks. filtrere efter alle varer i en bestemt varegruppe.
1. Vælg **OK**.
1. I dialogboksen **Tilføj varer** vises alle de varer, der svarer til din forespørgsel. Gennemgå resultaterne.

    Hvis der kræves ændringer, skal du vælge **Vælg** at vende tilbage til dialogboksen **Forespørgsel** og justere forespørgslen.

1. Når resultaterne omfatter alle de varer, du vil tilføje, skal du vælge **OK**.
1. Luk siden.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Knytte en vare manuelt til en kvalitetsgruppe

Hvis du vil knytte en vare manuelt til en kvalitetsgruppe, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Varekvalitetsgrupper**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Varenummer** – Vælg det varenummer, du vil tilføje.
    - **Kvalitetsgruppe** – Vælg den kvalitetsgruppe, som varen skal tildeles.

1. Gentag det forrige trin for hver ekstra kombination af en vare og en kvalitetsgruppe, som du vil tilføje.
1. Luk siderne.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Tilføje en kvalitetsgruppe manuelt fra siden Frigivne produkter

Hvis du vil tilføje en kvalitetsgruppe manuelt fra siden **Frigivne produkter**, skal du benytte følgende fremgangsmåde.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg det produkt, som du vil tildele en kvalitetsgruppe.
1. I handlingsruden under fanen **Styr lager** skal du i gruppen **Kvalitet** vælge **Varekvalitetsgrupper**.
1. På siden **Varer i kvalitetsgruppe** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret. Derefter skal du for den nye række indstille feltet **Kvalitetsgruppe** til den kvalitetsgruppe, du vil tildele produktet.
1. Gentag det forrige trin for hver ekstra kvalitetsgruppe, du vil tildele produktet.
1. Luk siderne.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md)
- [Test for kvalitetsstyring](quality-tests.md)
- [Testgrupper for kvalitetsstyring](quality-test-groups.md)
- [Testvariabler for kvalitetsstyring](quality-test-variables.md)
- [Kvalitetstilknytninger](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
