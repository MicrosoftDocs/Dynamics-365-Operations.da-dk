---
title: Oprettelse af udlånsemner
description: Udlånsemner er poster, der hjælper dig med at holde styr på fysiske emner, som f.eks. telefoner eller computere, som virksomheden udlåner til arbejdere.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21127c46615015c30e06465b390f67b835e746cb
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068128"
---
# <a name="create-loan-items"></a>Oprettelse af udlånsemner


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Udlånsemner er poster, der hjælper dig med at holde styr på fysiske emner, som f.eks. telefoner eller computere, som virksomheden udlåner til arbejdere. Alle fysiske emner skal have et tilknyttet udlånsemne. Alle udlånsemneposter skal beskrive, hvad der udlånes, hvem der er ansvarlig for udlånet, og det antal dage, emnet kan udlånes. Du kan oprette flere udlånsemner f.eks. nøgler, adgangskort og uniformer, på samme tid. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-loan-types"></a>Opret udlånstyper
1. Gå til **Human Resources** > **Arbejdere** > **Udlånsemner** > **Udlånstyper**.
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Udlånstype**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Angiv det antal dage, som emner, der er knyttet til denne udlånstype, kan være overskredet med. 
6. Klik på **Gem**.
7. Luk siden.
8. Opdater siden.

## <a name="create-loan-items"></a>Opret Udlånsemner
1. Gå til **Human Resources** > **Arbejdere** > **Udlånsemner** > **Udlånsemner**.
2. Klik på **Opret udlånsemner**.
3. I feltet **Antal** skal du angive et tal.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Klik på rullemenuen i feltet **Udlånstype** for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Angiv antal dage, emnet kan lånes.
    * Standardværdien i feltet Planlagt retur på siden Lånt udstyr beregnes som den aktuelle dato plus dette tal.  
9. Klik på rullelisten i feltet **Ansvarlig** for at åbne opslaget.
10. Klik på **Vælg**.
11. Indtast et tal i feltet **Startværdi**.
12. Angiv et tal i feltet **Interval**.
13. Skriv en værdi i feltet **Format**.
    * Hvis det startnummeret for et udlånsemne f.eks. er 10, skal du skrive to talsymboler i feltet **Format**.  
14. Klik på **OK**.
15. Opdater siden.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
