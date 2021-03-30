---
title: Oprette en rekvisition, der bruger en tilbudsanmodning
description: Dette emne forklarer, hvordan du føjer pris- og leverandøroplysninger til en indkøbsrekvisition fra en tilbudsanmodningsproces.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e67dafd02a3b2a38832d8a4f0e9809adffcbb80
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211832"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Oprette en rekvisition, der bruger en tilbudsanmodning

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du føjer pris- og leverandøroplysninger til en indkøbsrekvisition fra en tilbudsanmodningsproces. Eksemplet i denne vejledning kan bruges i USMF-demodatafirmaet, og du skal være logget på som administrator for at fuldføre alle trin. Opgaverne i denne vejledning udføres normalt af indkøbsmedarbejderne.


## <a name="create-a-requisition"></a>Opret en rekvisition
1. Gå i navigationsruden til **Moduler > Indkøb og forsyning > Indkøbsrekvisitioner > Indkøbsrekvisitioner, der er udarbejdet af mig**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Navn**.
4. Angiv en dato i feltet **Ønsket dato**.
5. Angiv en dato i feltet **Regnskabsdato**.
6. Vælg **OK**.
7. Indtast eller vælg en værdi i feltet **Årsag**.
8. Vælg **Tilføj linje**.
9. Vælg en kategori i træet i feltet **Indkøbskategori**, og vælg derefter **OK**.
10. Skriv en værdi i feltet **Produktnavn**.
11. Angiv et tal i feltet **Antal**.
12. Indtast eller vælg en værdi i feltet **Enhed**.
13. Vælg **Gem**.
14. Vælg **Arbejdsgang** for at åbne dialogboksen.
15. Vælg **Send**.
16. Luk siden.
17. Vælg **Send**.

## <a name="reassign-a-workflow-task"></a>Tildel en opgave i en arbejdsgang til en anden
Den næste opgave er at oprette en tilbudsanmodning for at få tilbud på produktet fra leverandører. I demodataene for USMF er arbejdsgangen for indkøbsrekvisitionen konfigureret med en regel, at hvis en leverandør ikke er markeret, eller hvis prisen er 0 for en linje, tildeles der en opgave til en bestemt arbejder om at oprette en tilbudsanmodning. For at fortsætte med denne vejledning skal du gentildele opgaven til en anden bruger (dig selv). Det kan du kun gøre, hvis du er logget på som administrator.  

1. Vælg **Arbejdsgang** for at åbne dialogboksen.
2. Vælg **Vis historik**.
3. Opdater siden.
4. Udvid sektionen **Sporingsdetaljer**.
5. Vælg den linje, der starter med "Arbejdsgang for linjeelement aktiveret den" i træet.
6. Vælg **Vis detaljer for arbejdsgang**.
7. Udvid sektionen **Workflowopgaver**.
8. Vælg **Tildel igen**.
9. Vælg **Administrator** i feltet **Bruger**.
10. Vælg **Tildel igen**.
11. Luk de to sider.

## <a name="create-an-rfq"></a>Opret en tilbudsanmodning

1. Opdater siden.
2. Vælg **Tilbudsanmodning**.
3. Vælg **USMF** i feltet **Juridisk indkøbsenhed**. Du skal vælge den samme juridiske enhed som den, der er på rekvisitionslinjen.  
4. Markér den valgte række på listen. Hvis du havde flere linjer på indkøbsrekvisitionen, kan du vælge alle de linjer, du vil føje til tilbudsanmodningen.  
5. Vælg **OK**.
6. Opdater siden.
7. Åbn faktaboksen, og udvid derefter sektionen **Relaterede dokumenter**.
8. Vælg linket i feltet **Tilbudsanmodning** for at åbne den tilbudsanmodning, der netop er blevet oprettet.
9. Vælg **Hoved**.
10. Vælg **Tilføj**.
11. Indtast eller vælg en værdi i feltet **Kreditorkonto**.
12. Vælg **Tilføj**.
13. Indtast eller vælg en værdi i feltet **Kreditorkonto**.
14. Vælg **Send**.
15. Vælg **OK**.
16. Vælg **Indtast svar**.
17. Vælg **Svar** i handlingsruden.
18. Vælg **Kopiér data til svar**. Derved kopieres data, f.eks. antal og datoer, fra tilbudsanmodningen til svaret.  
19. Angiv et tal i feltet **Enhedspris**. Det er den pris, du har modtaget fra leverandøren. Du kan også angive yderligere oplysninger fra leverandøren.  
20. Vælg **Accepter**.
21. Vælg **OK**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Kontrollér, at leverandøren og prisen er blevet overført til rekvisitionen
1. Luk siden.
2. Vælg **Linjer**.
3. Vælg **Relaterede oplysninger**.
4. Vælg **Indkøbsrekvisition**.
5. Vælg den linje, der blev overført til tilbudsanmodningen. Kontrollér, at prisen og leverandøren er blevet kopieret til rekvisitionen.  
6. Vælg **Arbejdsgang** for at åbne dialogboksen.
7. Vælg Fuldfør.
8. Vælg siden.
9. Vælg Fuldfør.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]