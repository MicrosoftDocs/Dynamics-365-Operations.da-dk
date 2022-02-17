---
title: Konfigurere kompensationsgitre
description: Kompensationsgitre bruges til at definere og vedligeholde lønstrukturerne for fast løn-planer.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51b98320eac539e49787d352f32683efadc11f41
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071410"
---
# <a name="set-up-compensation-grids"></a>Konfigurere kompensationsgitre


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensationsgitre bruges til at definere og vedligeholde lønstrukturerne for fast løn-planer. Kompensationsgitre kan deles mellem flere planer eller kopieres, når du opretter en ny lønstruktur.  Før du opretter et kompensationsgitteret, skal niveauer og referencepunkter konfigureres. I dette eksempel oprettes der en ny klassetype for kompensationsgitteret ved hjælp af demodata for niveauerne og referencepunkter. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Konfigurer oplysninger om kompensationsgitteret
1. Gå til **Human Resources** > **Kompensation** > **Fast løn** > **Kompensationsgitre**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Gitter**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg en indstilling i feltet **Type**.
6. Indtast eller vælg en værdi i feltet **Opsætning af reference**.
7. Indtast eller vælg en værdi i feltet **Valuta**.
8. Angiv en dato i feltet **Ikrafttrædelsesdato**.

## <a name="add-levels-to-the-compensation-structure"></a>Føje niveauer til kompensationsstrukturen
1. Klik på **Kompensationsstruktur**.
2. Markér den valgte række på listen.
3. Indtast eller vælg en værdi i feltet **Niveau**.
4. Klik på **Ny**.
5. Markér den valgte række på listen.
6. Indtast eller vælg en værdi i feltet **Niveau**.
7. Klik på **Ny**.
8. Markér den valgte række på listen.
9. Indtast eller vælg en værdi i feltet **Niveau**.
10. Klik på **Ny**.
11. Markér den valgte række på listen.
12. Indtast eller vælg en værdi i feltet **Niveau**.
13. Klik på **Ny**.
14. Markér den valgte række på listen.
15. Indtast eller vælg en værdi i feltet **Niveau**.

## <a name="fill-in-the-compensation-structure-with-values"></a>Udfyld kompensationsstrukturen med værdier
1. Markér den valgte række på listen.
    * På dette tidspunkt kan kompensationsværdier manuelt indtastes i hvert felt i tabellen, eller masseændringsfunktionen kan bruges til nemt at udfylde flere felter og udføre grundlæggende beregninger.  
2. Klik på **Masseændring**.
    * For dette gitter vil vi først anvende værdien af midtpunktet på første niveau på alle felter i tabellen. Dette er grundlaget for kompensationsmatrixen.  
3. Vælg en indstilling i feltet **Reguleringstype**.
4. Indtast et tal i feltet **Justeringsbeløb**.
5. Markér eller fjern markeringen af alle rækker på listen.
6. Klik på **Anvend på gitter**.
    * Nu bruger vi masseændringsfunktionen til at forøge beløbene i hvert efterfølgende niveau med en bestemt procentdel eller et beløb. I dette eksempel har hver lønklasse et 12,5% opslag mellem sine midtpunkter.  
7. Vælg en indstilling i feltet **Reguleringstype**.
8. Indtast et tal i feltet **Justeringsbeløb**.
9. Find og vælg den ønskede post på listen.
10. Klik på **Anvend på gitter**.
    * Nu skal vi bruge masseændringsfunktionen til at justere minimum og maksimumreferencepunkter for hvert niveau. I dette eksempel bruger vi et opslag med 50%, så minimumreferencepunktet reguleres -20% og maksimumopslaget bliver reguleret +20%.  
11. Indtast et tal i feltet **Justeringsbeløb**.
12. Indtast eller vælg en værdi i feltet **Referencepunkt**.
13. Markér eller fjern markeringen af alle rækker på listen.
14. Klik på **Anvend på gitter**.
15. Indtast et tal i feltet **Justeringsbeløb**.
16. Indtast eller vælg en værdi i feltet **Referencepunkt**.
17. Markér eller fjern markeringen af alle rækker på listen.
18. Klik på **Anvend på gitter**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
