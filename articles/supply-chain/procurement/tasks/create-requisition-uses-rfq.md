--- 
title: Oprette en rekvisition, der bruger en tilbudsanmodning
description: "Denne vejledning viser, hvordan du føjer pris- og leverandøroplysninger til en indkøbsrekvisition fra en tilbudsanmodningsproces."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d97ccd15031b2f7398486eee4a716ecef5e9dafd
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Oprette en rekvisition, der bruger en tilbudsanmodning

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne vejledning viser, hvordan du føjer pris- og leverandøroplysninger til en indkøbsrekvisition fra en tilbudsanmodningsproces. Eksemplet i denne vejledning kan bruges i USMF-demodatafirmaet, og du skal være logget på som administrator for at fuldføre alle trin. Opgaverne i denne vejledning udføres normalt af indkøbsmedarbejderne.


## <a name="create-a-requisition"></a>Opret en rekvisition
1. Gå til Indkøb og Forsyning > Indkøbsrekvisitioner > Indkøbsrekvisitioner, der er udarbejdet af mig.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Angiv en dato i feltet Ønsket dato.
5. Angiv en dato i datofeltet Regnskab.
6. Klik på OK.
7. Indtast eller vælg en værdi i feltet Årsag.
8. Klik på Tilføj linje.
9. Vælg en kategori i træet i feltet Indkøbskategori, og klik derefter på OK.
10. Skriv en værdi i feltet Produktnavn.
11. Angiv et tal i feltet Antal.
12. Indtast eller vælg en værdi i feltet Enhed.
13. Klik på Gem.
14. Klik på Arbejdsgang for at åbne dialogboksen.
15. Klik på Send.
16. Luk siden.
17. Klik på Send.

## <a name="reassign-a-workflow-task"></a>Tildel en opgave i en arbejdsgang til en anden
    * Den næste opgave er at oprette en tilbudsanmodning for at få tilbud på produktet fra leverandører. I demodataene for USMF er arbejdsgangen for indkøbsrekvisitionen konfigureret med en regel, at hvis en leverandør ikke er markeret, eller hvis prisen er 0 for en linje, tildeles der en opgave til en bestemt arbejder om at oprette en tilbudsanmodning. For at fortsætte med denne vejledning skal du gentildele opgaven til en anden bruger (dig selv). Det kan du kun gøre, hvis du er logget på som administrator.  
1. Klik på Arbejdsgang for at åbne dialogboksen.
2. Klik på Vis historik.
3. Opdater siden.
4. Udvid sektionen Sporingsdetaljer.
5. Vælg 'den linje, der starter med "Arbejdsgang for linjeelement aktiveret den"' i træet.
6. Klik på Vis detaljer for arbejdsgang.
7. Udvid sektionen Workflowopgaver.
8. Klik på Tildel igen.
9. Vælg Administrator i feltet Bruger.
10. Klik på Tildel igen.
11. Luk siden.
12. Luk siden.

## <a name="create-an-rfq"></a>Opret en tilbudsanmodning
1. Opdater siden.
2. Klik på Tilbudsanmodning.
3. Derefter skal du vælge USMF i feltet Juridisk indkøbsenhed.
    * Du skal vælge den samme juridiske enhed som den, der er på rekvisitionslinjen.  
4. Markér den valgte række på listen.
    * Hvis du havde flere linjer på indkøbsrekvisitionen, kan du vælge alle de linjer, du vil føje til tilbudsanmodningen.  
5. Klik på OK.
6. Opdater siden.
7. Åbn faktaboksen, og udvid derefter sektionen Relaterede dokumenter.
    * Du har måske allerede åbnet faktaboksen. Se efter ikonet med en pil, til højre for til/fra-knapperne Linjer/Sidehoved. Hvis pilen peger mod højre, er faktaboksen allerede åben. Hvis pilen peger mod venstre, skal du klikke på den for at åbne faktaboksen.  
8. Klik på linket i feltet Tilbudsanmodning for at åbne den tilbudsanmodning, der netop er blevet oprettet.
9. Klik på Overskrift.
10. Klik på Tilføj.
11. Indtast eller vælg en værdi i feltet Kreditorkonto.
12. Klik på Tilføj.
13. Indtast eller vælg en værdi i feltet Kreditorkonto.
14. Klik på Send.
15. Klik på OK.
16. Klik på Indtast svar.
17. Klik på Svar i handlingsruden.
18. Klik på Kopiér data til svar.
    * Derved kopieres data, f.eks. antal og datoer, fra tilbudsanmodningen til svaret.  
19. Angiv et tal i feltet Enhedspris.
    * Det er den pris, du har modtaget fra leverandøren. Du kan også angive yderligere oplysninger fra leverandøren.  
20. Klik på Acceptér.
21. Klik på OK.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Kontrollér, at leverandøren og prisen er blevet overført til rekvisitionen
1. Luk siden.
2. Klik på Linjer.
3. Klik på Relaterede oplysninger.
4. Klik på Indkøbsrekvisitionslinjer.
5. Vælg den linje, der blev overført til tilbudsanmodningen.
    * Kontrollér, at prisen og leverandøren er blevet kopieret til rekvisitionen.  
6. Klik på Arbejdsgang for at åbne dialogboksen.
7. Klik på Fuldført.
8. Luk siden.
9. Klik på Fuldført.


