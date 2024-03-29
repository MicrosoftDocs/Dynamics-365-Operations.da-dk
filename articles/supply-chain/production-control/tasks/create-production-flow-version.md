---
title: Oprette en produktionsflowversion
description: Denne procedure fokuserer på oprettelse af en ny produktionsflow-version.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b72d6162edd0ae6ccbfdcfe3e63ecff30528454
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569254"
---
# <a name="create-a-production-flow-version"></a>Oprette en produktionsflowversion

[!include [banner](../../includes/banner.md)]

Denne procedure fokuserer på oprettelse af en ny produktionsflow-version. For denne procedure skal produktionsparametre for lean manufacturing og måleenheder for klassen Tid være defineret. Du skal også definere en værdistrøm og en produktionsgruppe. Du kan finde flere oplysninger om produktionsflows og aktiviteter inden for lean manufacturing i hvidbøgerne om lean manufacturing til Microsoft Dynamics AX. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-production-flow"></a>Oprette et produktionsflow
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på rullelisten i feltet Navn for at åbne opslaget.
6. Klik op linket i den valgte række på listen.
    * Vælg en driftsenhed af typen værdistrøm. En værdistrøm er en driftsenhed, der spænder over alle værdistrømmens aktiviteter og flow. På dette stadium er driftsenheder begrænset til en juridisk enhed og har ikke yderligere funktionalitet.  
7. Klik på rullelisten i feltet Produktionsgruppe for at åbne opslaget.
8. Klik op linket i den valgte række på listen.
    * Vælg en produktionsgruppe for produktionsflowet. Produktionsgrupper giver mulighed for definition af materiale, arbejdskraft og IGVF-konti for en produktionsproces. For at knytte regnskabskonteksten til et produktionsflow skal der vælges en produktionsgruppe.  
9. Klik på Gem.

## <a name="create-a-production-flow-version"></a>Oprette en produktionsflowversion
1. Klik på Tilføj.
2. Angiv dato og klokkeslæt i feltet Udløbsdato.
    * Hvis det er nødvendigt, kan du angive en udløbsdato for versionen. Du kan opdatere den til enhver tid, selv for aktive versioner. Du kan bruge den til at planlægge at udfase en version.  
3. Klik på OK.
4. Markér den valgte række på listen.
5. Skriv en værdi i feltet Enhed.
6. ResolveChanges er taktenheden.
7. Angiv et tal i feltet Gennemsnitlig takttid.
    * Definer den gennemsnitlige takttid for versionen. Definer en gennemsnitlig takttid for taktstyring af produktionsflowversionen. Takten defineres som antal pr. periode. I eksemplet er takttiden 0,2 timer pr. 10 styk. Dette svarer til en daglig gennemløbskapacitet på 400 styk for en arbejdstid på 8 timer.  
8. Skriv et tal i feltet Antal pr. cyklus.
    * Definer mængden pr. cyklus i forhold til den gennemsnitlige takttid.  
9. Slå udvidelsen af afsnittet Versionsdetaljer.
10. Angiv et tal i feltet Mimimumtakttid.
    * Definer minimumtakttiden. Minimumtakttiden skal være mindre end eller lig med den gennemsnitlige takttid.  
11. Angiv et tal i feltet Maksimumtakttid.
    * Maksimumtakttiden skal være større end eller lig med den gennemsnitlige takttid.  
12. Angiv et tal i feltet Periode for faktisk procestid (dage).
    * Angiv antallet af dage i Periode for faktisk procestid. Periode for faktisk procestid er det antal dage, hvor jobs aggregeres, fra det faktiske minut bagud for at beregne den faktiske procestid. Værdien kan ændres når som helst og bruges kun til beregning af de faktiske procestider.  
13. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]