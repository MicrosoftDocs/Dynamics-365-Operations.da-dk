--- 
title: "Opsætte og generere aldersfordelte oplysninger om debitorer"
description: "Denne guide hjælper dig med at oprette en definition af forældelsesperiode, aldersfordele kundesaldi og få vist saldi på listen Aldersfordelt saldo og siden Rykkere."
author: mikefalkner
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2e9f393acaa47d485a583b99ace459474f30be6a
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Opsætte og generere aldersfordelte oplysninger om debitorer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne guide hjælper dig med at oprette en definition af forældelsesperiode, aldersfordele kundesaldi og få vist saldi på listen Aldersfordelt saldo og siden Rykkere. Denne registrering anvender demofirmaet USMF.


## <a name="create-an-aging-period-definition"></a>Opret en definition af forældelsesperioder
1. Gå til Kredit > Opsætning > Definitioner af forældelsesperioder.
2. Klik på Ny.
3. Indtast en værdi i feltet Definition på forældelsesperiode.
4. Indtast en værdi i feltet Beskrivelse.
5. Klik på Tilføj under for at indsætte en ny forældelsesperiode.
6. Indtast en beskrivelse, der skal vises i rapporter over forældelse, i feltet Periode.
7. Indtast et tal i feltet Enhed.
8. Vælg en indstilling i feltet Interval.
    * Finansperiode svarer til perioden til finanskalenderen. Dag, uge, måned, kvartal og år definerer størrelsen på intervallet efter datotype.. Ubegrænset vælger alle transaktioner før eller efter den forrige periode, alt efter om det er den første eller sidste periode.  
9. Vælg en indstilling i feltet Aldersindikator.
10. Vælg perioden øverst i gitteret. Opdater beskrivelsen for at beskrive den ældste periode i definitionen af forældelsesperioder
11. Angiv den nye beskrivelse af forældelsesperioden i feltet Periode.
12. Luk siden.

## <a name="age-the-balances"></a>Aldersfordel saldiene
1. Gå til Kredit > Periodiske opgaver > Æld debitorsaldi.
2. I feltet Definition på forældelsesperiode skal du vælge den definition på forældelsesperiode, du har oprettet.
    * Du kan have ét aktivt øjebliksbillede for hver definition af forældelsesperioder.  
    * Alle kunder behandles som standard. Du kan bruge denne udvælgelse til at beregne en enkelt samlings kundepulje.  
    * Vælg datoen fra den transaktion, du vil bruge til aldersfordelingen.  
    * Vælg en "pr."-dato for aldersfordeling. I dag er standard, men hvis du ændrer feltet til Valgt dato, kan du vælge den dato, du vil. Du kan bruge Dags dato til batchbehandling.  
3. Udvid området Firma. Du kan vælge de firmaer, der skal medtages i øjebliksbilledet. Det aktuelle firma er valgt som standard.
4. Klik på OK for at behandle øjebliksbilledet. Det vil tage et stykke tid, så vent på, at skyderen forsvinder, og kontrollér, om der er en meddelelse i Meddelelsescenter.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Få vist saldi på listen aldersfordelte saldi og på siden Rykker
1. Gå til Kredit > Rykkere > Aldersfordelte saldi.
    * Listesiden viser saldi for kunden. Ikonet for aldersfordeling viser forældelsesperioden for den ældste transaktion.  
2. Vælg en kunde med en saldo.
3. Udvid faktaboksen Aldersfordeling for at få vist de aldersfordelte saldi.
    * Definitionen af forældelsesperioden for faktaboksen hentes fra den definition af standardforældelsesperiode, som er angivet i parametrene. Du kan ændre den ved hjælp af menuen Indsaml.  


