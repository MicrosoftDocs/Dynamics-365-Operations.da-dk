--- 
title: Konfigurere kompensationsgitre
description: "Kompensationsgitre bruges til at definere og vedligeholde lønstrukturerne for fast løn-planer."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 33a95e4366dc352f28202155be7fc0b8f4c99e4a
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-compensation-grids"></a>Konfigurere kompensationsgitre

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kompensationsgitre bruges til at definere og vedligeholde lønstrukturerne for fast løn-planer. Kompensationsgitre kan deles mellem flere planer eller kopieres, når du opretter en ny lønstruktur.  Før du opretter et kompensationsgitteret, skal niveauer og referencepunkter konfigureres. I dette eksempel oprettes der en ny klassetype for kompensationsgitteret ved hjælp af demodata for niveauerne og referencepunkter. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Konfigurer oplysninger om kompensationsgitteret
1. Gå til Personale > Kompensation > Fast løn > Kompensationsgitre.
2. Klik på Ny.
3. Skriv en værdi i feltet Gitter.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg en indstilling i feltet Type.
6. Indtast eller vælg en værdi i feltet Opsætning af reference.
7. Indtast eller vælg en værdi i feltet Valuta.
8. Skriv en værdi i feltet Valuta.
9. Angiv en dato i feltet Ikrafttrædelsesdato.

## <a name="add-levels-to-the-compensation-structure"></a>Føje niveauer til kompensationsstrukturen
1. Klik på Kompensationsstruktur.
2. Markér den valgte række på listen.
3. Indtast eller vælg en værdi i feltet Niveau.
4. Klik på Ny.
5. Markér den valgte række på listen.
6. Indtast eller vælg en værdi i feltet Niveau.
7. Klik på Ny.
8. Markér den valgte række på listen.
9. Indtast eller vælg en værdi i feltet Niveau.
10. Klik på Ny.
11. Markér den valgte række på listen.
12. Indtast eller vælg en værdi i feltet Niveau.
13. Klik på Ny.
14. Markér den valgte række på listen.
15. Indtast eller vælg en værdi i feltet Niveau.

## <a name="fill-in-the-compensation-structure-with-values"></a>Udfyld kompensationsstrukturen med værdier
1. Markér den valgte række på listen.
    * På dette tidspunkt kan kompensationsværdier manuelt indtastes i hvert felt i tabellen, eller masseændringsfunktionen kan bruges til nemt at udfylde flere felter og udføre grundlæggende beregninger.  
2. Klik på Masseændring.
    * For dette gitter vil vi først anvende værdien af midtpunktet på første niveau på alle felter i tabellen. Dette er grundlaget for kompensationsmatrixen.  
3. Vælg en indstilling i feltet Reguleringstype.
4. Indtast et tal i feltet Justeringsbeløb.
5. Markér eller fjern markeringen af alle rækker på listen.
6. Klik på Anvend på gitter.
    * Nu bruger vi masseændringsfunktionen til at forøge beløbene i hvert efterfølgende niveau med en bestemt procentdel eller et beløb. I dette eksempel har hver lønklasse et 12,5% opslag mellem sine midtpunkter.  
7. Vælg en indstilling i feltet Reguleringstype.
8. Indtast et tal i feltet Justeringsbeløb.
9. Find og vælg den ønskede post på listen.
10. Find og vælg den ønskede post på listen.
11. Find og vælg den ønskede post på listen.
12. Find og vælg den ønskede post på listen.
13. Klik på Anvend på gitter.
14. Find og vælg den ønskede post på listen.
15. Find og vælg den ønskede post på listen.
16. Find og vælg den ønskede post på listen.
17. Klik på Anvend på gitter.
18. Find og vælg den ønskede post på listen.
19. Find og vælg den ønskede post på listen.
20. Klik på Anvend på gitter.
21. Find og vælg den ønskede post på listen.
22. Klik på Anvend på gitter.
    * Nu skal vi bruge masseændringsfunktionen til at justere minimum og maksimumreferencepunkter for hvert niveau. I dette eksempel bruger vi et opslag med 50%, så minimumreferencepunktet reguleres -20% og maksimumopslaget bliver reguleret +20%.  
23. Indtast et tal i feltet Justeringsbeløb.
24. Indtast eller vælg en værdi i feltet Referencepunkt.
25. Markér eller fjern markeringen af alle rækker på listen.
26. Klik på Anvend på gitter.
27. Indtast et tal i feltet Justeringsbeløb.
28. Indtast eller vælg en værdi i feltet Referencepunkt.
29. Markér eller fjern markeringen af alle rækker på listen.
30. Klik på Anvend på gitter.


