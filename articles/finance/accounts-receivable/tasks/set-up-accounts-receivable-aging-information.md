---
title: Opsætte og generere aldersfordelte oplysninger om debitorer
description: Denne guide hjælper dig med at oprette en definition af forældelsesperiode, aldersfordele kundesaldi og få vist saldi på listen Aldersfordelt saldo og siden Rykkere.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b21fe217aacd11821ff8d5cf7c7682b2181e36c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220077"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Opsætte og generere aldersfordelte oplysninger om debitorer

[!include [banner](../../includes/banner.md)]

Denne guide hjælper dig med at oprette en definition af forældelsesperiode, aldersfordele kundesaldi og få vist saldi på listen Aldersfordelt saldo og siden Rykkere. Denne registrering anvender demofirmaet USMF.


## <a name="create-an-aging-period-definition"></a>Opret en definition af forældelsesperioder
1. Gå til **Navigationsruden > Moduler > Kredit og inkasso > Opsætning > Definitioner af forældelsesperioder**.
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Definition af forældelsesperiode**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Klik på **Tilføj nedenfor** for at indsætte en ny forældelsesperiode.
6. Indtast en beskrivelse, der skal vises i rapporter over forældelse, i feltet **Periode**.
7. Indtast et tal i feltet **Enhed**.
8. Vælg en indstilling i feltet **Interval**. Finansperiode svarer til perioden til finanskalenderen. Dag, uge, måned, kvartal og år definerer størrelsen på intervallet efter datotype.. Ubegrænset vælger alle transaktioner før eller efter den forrige periode, alt efter om det er den første eller sidste periode.  
9. Vælg en indstilling i feltet **Aldersindikator**.
10. Vælg perioden øverst i gitteret. Opdater beskrivelsen for at beskrive den ældste periode i definitionen af forældelsesperioder
11. Angiv den nye beskrivelse af forældelsesperioden i feltet **Periode**.
12. Luk siden.

## <a name="age-the-balances"></a>Aldersfordel saldiene
1. Gå til **Kredit > Periodiske opgaver > Æld debitorsaldi**.
2. I feltet **Definition af forældelsesperiode** skal du vælge den definition på forældelsesperiode, du har oprettet.
    + Du kan have ét aktivt øjebliksbillede for hver definition af forældelsesperioder.  
    + Alle kunder behandles som standard. Du kan bruge denne udvælgelse til at beregne en enkelt samlings kundepulje.  
    + Vælg datoen fra den transaktion, du vil bruge til aldersfordelingen.  
    + Vælg en "pr."-dato for aldersfordeling. I dag er standard, men hvis du ændrer feltet til Valgt dato, kan du vælge den dato, du vil. Du kan bruge Dags dato til batchbehandling.  
3. Udvid området **Virksomhed**. Du kan vælge de firmaer, der skal medtages i øjebliksbilledet. Det aktuelle firma er valgt som standard.
4. Klik på **OK** for at behandle øjebliksbilledet. Det vil tage et stykke tid, så vent på, at skyderen forsvinder, og kontrollér, om der er en meddelelse i Meddelelsescenter.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Få vist saldi på listen aldersfordelte saldi og på siden Rykker
1. Gå til **Kredit > Rykkere > Aldersfordelte saldi**. Listesiden viser saldi for kunden. Ikonet for aldersfordeling viser forældelsesperioden for den ældste transaktion.  
2. Vælg en kunde med en saldo.
3. Udvid faktaboksen **Aldersfordeling** for at få vist de aldersfordelte saldi. Definitionen af forældelsesperioden for faktaboksen hentes fra den definition af standardforældelsesperiode, som er angivet i parametrene. Du kan ændre den ved hjælp af menuen Indsaml.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]