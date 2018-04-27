---
title: Oprette og behandle en overensstemmelse
description: "Brug denne procedure til at udføre uoverensstemmelsesstyring baseret på en eksisterende kvalitetsordre."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-process-a-conformance"></a>Oprette og behandle en overensstemmelse

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Brug denne procedure til at udføre uoverensstemmelsesstyring baseret på en eksisterende kvalitetsordre. Du kan køre denne registrering i demofirmaet USMF, og du kan bruge de foreslåede værdier. Denne procedure udføres typisk af en kvalitetsmedarbejder.  Som en forudsætning skal du køre opgaveregistreringen "Inspicer kvaliteten af varer". For at behandle godkendelse af en uoverensstemmelse skal den bruger, der kører opgavregistreringen, have en "Navn"-værdi tildelt på siden Brugere. For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.


## <a name="select-a-quality-order"></a>Vælg en kvalitetsordre
1. Gå til Kvalitetsordrer.
2. Markér den valgte række på listen.
    * Vælg den kvalitetsordre, der blev oprettet ud fra opgaveregistreringen "Kontrollere kvaliteten af varer".  

## <a name="create-a-nonconformance"></a>Oprette en uoverensstemmelse
1. Klik på Forespørgsler.
2. Klik på Uoverensstemmelser.
3. Klik på Ny.
4. Klik på rullelisten i feltet Problemtype for at åbne opslaget.
    * Vælg det problem, der blev fundet under inspektionsprocessen.  
5. Klik på rullelisten i feltet Problemtype for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på OK.

## <a name="approvereject-a-nonconformance"></a>Godkende/afvise en uoverensstemmelse
1. Klik på Funktioner.
2. Klik på Godkend uoverensstemmelsen.
    * I dette eksempel skal du godkende uoverensstemmelsen. Godkendte uoverensstemmelser kan være tilknytte til relaterede operationer at registrere arbejde, der udføres som en del af håndteringen af uoverensstemmelsen og, som i denne opgaveregistrering, behandlingen af korrektionshåndtering.  
3. Klik på Ja.

## <a name="create-a-correction-action"></a>Opret en korrektionshandling
1. Klik på Rettelser.
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Klik på rullelisten i feltet Personalenummer for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
6. Klik på Vælg.
7. Klik på Vedhæft.
    * Oprette en note om korrektionen. I dette eksempel er handlingen at kontakte leverandøren for at diskutere uoverensstemmelsen.  
8. Klik på Ny.
9. Klik på Notat.
    * Bemærk, at afhængigt af opsætningen af rapporten kan forskellige dokumenttyper udskrives på de rapporter, der er relateret til uoverensstemmelsesstyring.  
10. Skriv en værdi i feltet Beskrivelse.
11. Luk siden.

## <a name="maintain-a-correction"></a>Vedligehold en korrektion
1. Klik på Marker som fuldført.
2. Klik på OK.
3. Luk siden.

## <a name="close-a-nonconformance"></a>Luk en uoverensstemmelse
1. Klik på Funktioner.
2. Klik på Luk uoverensstemmelsen.
3. Klik på Ja.
4. Luk siden.
5. Luk siden.

