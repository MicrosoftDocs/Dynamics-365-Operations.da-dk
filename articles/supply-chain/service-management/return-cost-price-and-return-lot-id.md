---
title: Returkostpris og returparti-id
description: "I visse tilfælde ønsker du muligvis, at kostprisen for de returnerede produkter er lig med kostprisen for produkterne på det tidspunkt, da du solgte produkterne til kunden. Du kan gøre dette ved hjælp af **Returparti-id**."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: aeba56128ab6c9ab7d244bdf153faba8e96069d6
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="return-cost-price-and-return-lot-id"></a>Returkostpris og returparti-id        

[!include [banner](../includes/banner.md)]



De kostpriser for produkter, der returneres til lageret, beregnes ved hjælp af de aktuelle kostpriser for produkterne. I visse tilfælde ønsker du, at kostprisen for de returnerede produkter er lig med kostprisen for produkterne på det tidspunkt, da du solgte produkterne til kunden. Du kan gøre dette ved hjælp af feltet **Returparti-id** i oversigtspanelet **Linjedetaljer** i formularen **Salgsordre**.

Overvej f.eks. følgende scenario. Du fakturerer en kunde. Kunden returnerer derefter de leverede produkter til dig. Du returnerer produkterne til lageret. Når du krediterer kunden for de returnerede produkter, beregnes kostpriserne for de pågældende produkter i dette tilfælde ved hjælp af de aktuelle kostpriser for produkterne. Men hvis du bruger feltet **Returparti-id**, beregnes kostprisen for de returnerede produkter ved hjælp af kostprisen på fakturaen for det oprindelige salg til kunden.

Hvis du vil bruge en anden kostpris end den aktuelle kostpris for returvarer fra en kunde, skal du bruge en af følgende metoder.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Metode 1: Angiv returkostprisen manuelt

Når du føjer varer til en returordre, returneres varerne som standard til lageret til den aktuelle kostpris. Følg disse trin for at angive en anden returkostpris.

1.  Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.

2.  Klik på **Returordre** i gruppen **Ny** i **handlingsruden**.

3.  I formularen **Opret returordre** skal du vælge en debitorkonto og derefter klikke på **OK**.

4.  I formularen **Returordre - RMA-nummer: %1, %2** skal du markere en vare og derefter angive et negativ antal feltet **Antal**.

5.  Klik på oversigtspanelet **Linjedetaljer**.

6.  Angiv en værdi i feltet **Returkostpris** under fanen **Generelt**. Denne værdi bruges, når varerne returneres til lager. Hvis du ikke angiver en værdi, bruges den aktuelle kostpris, når varerne returneres til lager.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Metode 2: Automatisk generere kostprisen på baggrund af debitorfakturalinjen

Dette er den foretrukne metode til at oprette returlinjer. Hvis du vil bruge den kostpris for produkterne, der var aktuel på det tidspunkt, hvor du solgte produkterne til kunden, skal du oprette en returordre og angive en salgslinje, der skal returneres.

1.  Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.

2.  Klik på **Returordre** i gruppen **Ny** i **handlingsruden**.

3.  I formularen **Opret returordre** skal du vælge en debitorkonto og derefter klikke på **OK**.

4.  I formularen **Returordre - RMA-nummer: %1, %2** i **Handlingsrude** skal du klikke på **Find salgsordre**.

5.  Vælg den fakturalinje, der skal returneres, i formularen **Find salgsordre**, og klik derefter på **OK**.
    
    Værdien fra den oprindelige salgslinje vises i feltet **Returparti-id** under fanen **Generelt** i oversigtspanelet **Linjedetaljer**. Desuden vises kostprisværdien fra den oprindelige salgslinje i feltet **Returkostpris**.

## <a name="cost-calculation-example"></a>Eksempel på beregning af kostpris

Når du bruger feltet **Returvare-id** på en returordrelinje til at angive returkostprisen, bruges kostprisen på returordrelinjen. Hvis du kører funktionen til lagerlukning eller genberegning, justeres kostprisen på den oprindelige salgslinje. Kostprisen på returordrelinjen justeres automatisk til at afspejle samme kostpris pr. styk.

1.  Opret og frigiv et produkt, der kaldes Test. I formularen **Frigivne produktdetaljer** skal du angive følgende oplysninger:
    
    1.  På oversigtspanelet **Administrer omkostninger** skal du i feltet **Varegruppe** vælge gruppen **Dele**.
    
    2.  I oversigtspanelet **Generelt** i feltet **Varemodelgruppe** skal du vælge **DEF**.
    
    3.  Angiv 10,00 som varens kostpris i feltet **Pris** i oversigtspanelet **Køb**.
    
    4.  Klik på **Dimensionsgrupper** i **handlingsruden**. I feltet **Lagringsdimensionsgruppe** skal du vælge **Kun lokation og lagersted**. I feltet **Sporingsdimensionsgruppe** skal du vælge **Ingen aktive sporingsdimensioner**.

2.  Opret en indkøbsordre på 10 stk. af testvaren til 6,00 pr. stk., og bogfør derefter en faktura for indkøbsordren.
    
    Opret en anden indkøbsordre på 10 stk. af testvaren til 8,00 pr. stk., og bogfør derefter en faktura for indkøbsordren.

3.  Bogfør en faktura for en salgsordre for at sælge fem stk. af testvaren.
    
    I dette tilfælde er salgsordrelinjen efterkalkuleret til 35,00 (5 stk. \* 7,00, som er den gennemsnitlige kostpris pr. stk.).

4.  Opret en returordre for debitoren. Vælg fakturalinjen i formularen **Find salgsordre**, og klik derefter på **OK**.

5.  I formularen **Returordre - RMA-nummer: %1, %2** skal du kontrollere, at der genereres en returordre for at returnere testvaren. Antallet på returordren er angivet til -5,00.
    
    Feltet **Returparti-id** viser et parti-id. Dette parti-id er hentet fra den oprindelige salgsordre for den vare, der blev solgt til kunden. Kostprisværdien fra den oprindelige salgslinje vises i feltet **Returkostpris**.

6.  Registrer modtagelsen af de returnerede varer.

7.  Bogfør en følgeseddel for de returnerede varer.

8.  Bogfør en faktura for returordren. Vælg en salgsordre, hvor ordretypen er **Returordre**, på listesiden **Alle salgsordrer**.

9.  Åbn formularen **Lagertransaktioner**. Kontrollér, at returneringen efterkalkuleres til 7,00 pr. stk. ved hjælp af værdien i feltet **Returkostpris**, så totalen er 35,00 i feltet **Kostbeløb**. Du kan åbne formularen **Lagertransaktioner** fra formularen **Returordre - RMA-nummer: %1, %2**. Klik på **Lager** \> **Transaktioner** i gitteret **Linjer**.

10. I Lager- og lokalitetsstyring skal du bruge formularen **Lukning og regulering** til at køre proceduren **3. Luk**.
    
    Denne handling justerer kostprisen på den oprindelige salgslinje, som blev efterkalkuleret fra -35,00 (5 stk. \* 7,00) til -30,00 (5 stk. \* 6,00). Dette skyldes, at lagermodelgruppen bruger FIFO (First In, First Out), og 6,00 pr. stk. er FIFO-kostprisen fra den første indkøbsordre. Desuden justerer handlingen kostprisen på retursalgslinjen, så den svarer til kostprisen pr. stk. på den oprindelige salgslinje. Kostprisen på returlinjen justeres derfor fra 35,00 til 30,00.





