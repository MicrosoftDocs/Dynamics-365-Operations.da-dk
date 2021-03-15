---
title: Validere et produktionsflow og en version
description: Denne procedure viser, hvordan du opretter et nyt produktionsflow og en første version af lean manufacturing.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cc8465fb56239f91982db15601cf87e3c00d3fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980950"
---
# <a name="validate-a-production-flow-and-version"></a>Validere et produktionsflow og en version

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter et nyt produktionsflow og en første version af lean manufacturing. Forudsætninger: Produktionsparametre for lean manufacturing og måleenheder for klassen Tid skal defineres. Du skal definere en værdistrøm og en produktionsgruppe. Se hvidbøgerne om Lean manufacturing for at blive fortrolig med begreberne produktionsflow og -aktiviteter. Denne procedure refererer til den juridiske enhed USMF i demodata. Forudsat at den juridiske enhed er konfigureret for Lean manufacturing, kan andre juridiske enheder imidlertid også bruges.


## <a name="create-a-production-flow"></a>Oprette et produktionsflow
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på rullelisten i feltet Navn for at åbne opslaget.
6. Klik op linket i den valgte række på listen.
    * En værdistrøm er en driftsenhed, der spænder over alle værdistrømmens aktiviteter og flow.   På dette stadium er driftsenheder begrænset til en juridisk enhed og har ikke yderligere funktionalitet.  
7. Klik på rullelisten i feltet Produktionsgruppe for at åbne opslaget.
8. Klik op linket i den valgte række på listen.
    * Produktionsgrupper giver mulighed for definition af materiale, arbejdskraft og IGVF-konti for en produktionsproces. For at knytte regnskabskonteksten til et produktionsflow skal der vælges en produktionsgruppe.  
9. Klik på Gem.

## <a name="create-a-production-flow-version"></a>Oprette en produktionsflowversion
1. Klik på Tilføj.
2. Angiv dato og klokkeslæt i feltet Udløbsdato.
    * Du kan opdatere udløbsdatoen for versionen til enhver tid, selv for aktive versioner. Brug udløbet af versionen til at planlægge en udfasning af en version.  
3. Klik på OK.
4. Markér den valgte række på listen.
5. Skriv en værdi i feltet Enhed.
6. Vælg Taktenhed.
7. Angiv et tal i feltet Gennemsnitlig takttid.
    * Definer en gennemsnitlig takttid for taktstyring af produktionsflowversionen.   Takten defineres som antal pr. periode.  I det givne eksempel er takttiden 0,2 timer pr. 10 styk. Dette svarer til en daglig gennemløbskapacitet på 400 styk for en arbejdstid på 8 timer.  
8. Skriv et tal i feltet Antal pr. cyklus.
9. Udvid eller skjul afsnittet Versionsdetaljer.
10. Angiv et tal i feltet Mimimumtakttid.
    * Minimumtakttiden skal være mindre end eller lig med den gennemsnitlige takttid.  
11. Angiv et tal i feltet Maksimumtakttid.
    * Maksimumtakttiden skal være større end eller lig med den gennemsnitlige takttid.  
12. Angiv et antal dage i Periode for faktisk procestid
    * Periode for faktisk procestid er det antal dage, hvor jobs aggregeres, fra det faktiske minut bagud for at beregne den faktiske procestid. Værdien kan ændres når som helst og bruges kun til beregning af de faktiske procestider.  
13. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]