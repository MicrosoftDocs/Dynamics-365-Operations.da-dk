---
title: Arbejdsgangshandlinger
description: I denne artikel beskrives de handlinger, som hver deltager i godkendelsen af en arbejdsproces kan foretage.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: adcb0443f5ad07ae7178e9fde963184951e6b8d9
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-actions"></a>Arbejdsgangshandlinger

I denne artikel beskrives de handlinger, som hver deltager i godkendelsen af en arbejdsproces kan foretage.

En arbejdsgang kan involvere flere persongrupper: igangsætteren, opgavemodtagere, beslutningstagere og godkendere. I arbejdsgangen for følgende udgiftsrapport er Søren igangsætter, medlemmerne af køen er opgavemodtagere, John er opgavemodtager og Henrik, Mette og Dorthe er godkendere.   [![Arbejdsgang for\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif) i følgende afsnit forklares de arbejdsganghandlinger, hver gruppe kan udføre.

## <a name="actions-that-an-originator-can-perform"></a>Handlinger, som igangsætteren kan udføre
Igangsætteren starter en arbejdsgangsforekomst ved at sende et dokument til behandling. Når Søren f.eks. vil sende sin udgiftsrapport, skal han klikke på knappen **Send** på siden **Udgiftsrapport**.

## <a name="actions-that-a-task-assignee-can-perform"></a>Handlinger, som en opgavemodtager kan udføre
En opgave kan tildeles til flere personer eller til en workflowopgavekø, som overvåges af flere personer. Men en opgave kan kun fuldføres af én person. Søren har f.eks. sendt en udgiftsrapport og har sendt sine kvitteringer til sin organisations udgiftsrapportafdeling til gennemsyn. Medlemmerne af udgiftsrapportafdelingen for Adventure Works overvåger køen. Julie, der er medlem af denne afdeling, har accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer. Hun kan nu udføre en af følgende handlinger: fuldføre, afvise, delegere, anmode om ændring, tildele eller frigive. **Bemærk!** Det vil variere, hvilke handlinger der er tilgængelige, afhængigt af hvordan softwareudvikleren har designet opgaven.

### <a name="complete"></a>Fuldføre

Når en bruger fuldfører en opgave, tildeles det dokument, der blev sendt til behandling, til den næste bruger i arbejdsgangen, hvis der er en næste bruger. Hvis opgaven ikke skal behandles yderligere, afsluttes arbejdsgangsprocessen. For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer. Når Julie har fuldført gennemsynet, tildeles John dokumentet til godkendelse.

### <a name="reject"></a>Afvis

Når en bruger afviser et dokument, afsluttes arbejdsgangsprocessen. For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer. Hvis Julie afviser udgiftsrapporten, afsluttes arbejdsgangsprocessen. Søren kan derefter sende udgiftsrapporten igen. Han kan foretage ændringer først, eller han kan sende den oprindelige version igen. Hvis Søren sender udgiftsrapporten igen, starter arbejdsgangsprocessen ved den manuelle gennemsynsopgave.

### <a name="delegate"></a>deleger

Når en bruger delegerer en opgave, tildeles opgaven til en anden bruger. For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer. Julie delegerer denne opgaven til sin assistent, Tim. Tim udfører derefter opgaven på vegne af Julie. Når Tim derfor har fuldført gennemsynsopgaven, bliver udgiftsrapporten tildelt John til godkendelse – ligesom hvis Julie havde fuldført opgaven.

### <a name="request-change"></a>Anmode om ændring

Når en bruger anmoder om en ændring af et dokument, der er sendt, sendes dokumentet tilbage til igangsætteren. For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer. Julie bemærker nogle fejl i udgiftsrapporten og anmoder om at måtte foretage ændringer. Udgiftsrapporten sendes tilbage til Søren. Søren kan sende udgiftsrapporten igen. Han kan foretage de ønskede ændringer først, eller han kan sende den oprindelige version igen. Hvis Søren sender udgiftsrapporten igen, skal et medlem af workflowopgavekøen gennemse udgiftsrapporten og kvitteringerne igen.

### <a name="reassign"></a>Tildel igen

Medlemmerne af en workflowopgavekø kan tildele de dokumenter, som er i køen, igen til en anden kø. For eksempel overvåger Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, køen. Hun kan udligne arbejdsbyrden ved igen at tildele udgiftsrapporten og de tilhørende kvitteringer til en anden kø.

### <a name="release"></a>Udlevering

Et medlem af en workflowopgavekø kan undertiden acceptere en opgave, men derefter indse, at han eller hun ikke kan fuldføre opgaven. I så fald kan den person, der har accepteret opgaven, frigive dokumentet tilbage til workflowopgavekøen. For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer. Hvis Julie beslutter, at hun ikke kan fuldføre opgaven, kan hun frigive dokumentet. Udgiftsrapporten returneres til køen, så andre medlemmer af udgiftsrapportafdelingen for Adventure Works kan fuldføre opgaven.

## <a name="actions-that-a-decision-maker-can-perform"></a>Handlinger, som en beslutningstager kan udføre
Når et dokument tildeles en beslutningstager, er det ofte fordi, der er et spørgsmål, som beslutningstageren skal besvare. Svaret på spørgsmålet er typisk **Ja** eller **Nej**, **Sand** eller **Falsk**. Hvis beslutningstageren ikke vælger et af disse svar, kan han eller hun uddelegere beslutningen.

### <a name="choice-1-or-choice-2"></a>\[Valg 1\] eller \[valg 2\]

En beslutningstager skal besvare et spørgsmål, der har relation til dokumentet. Svaret på spørgsmålet er typisk **Ja** eller **Nej**, **Sand** eller **Falsk**. Det svar, beslutningstageren vælger, bestemmer, hvilken gren i arbejdsgangen der bliver brugt til behandling af dokumentet. For eksempel er Sørens udgiftsrapport tildelt til John. John skal beslutte, om oplysningerne i dokumentet kræver et opkald til Sørens chef. Hvis John beslutter, at et opkald er nødvendigt, tildeles udgiftsrapporten til Agnete, som derefter skal ringe til Sørens chef. Hvis John beslutter, at et opkald ikke er nødvendigt, tildeles udgiftsrapporten til Henrik til godkendelse.

### <a name="delegate"></a>Delegere

Når en beslutningstager uddelegerer en beslutning, tildeles dokumentet til en anden bruger, som skal træffe beslutningen. For eksempel er Sørens udgiftsrapport tildelt til John. John uddelegerer beslutningen til sin assistent, Maria. Maria udfører derefter opgaven på vegne af John. Hvis Maria beslutter, at et opkald til Sørens chef er nødvendigt, tildeles udgiftsrapporten til Agnete, som derefter skal ringe til Sørens chef. Hvis Maria beslutter, at et opkald ikke er nødvendigt, tildeles udgiftsrapporten til Henrik til godkendelse.

## <a name="actions-that-an-approver-can-perform"></a>Handlinger, som godkenderen kan udføre
Når et dokument er tildelt en godkender, kan godkenderen udføre en af følgende handlinger: godkende, afvise, delegere eller anmode om ændring.

### <a name="approve"></a>Godkende

Når en godkender har godkendt et dokument, tildeles dokumentet til den næste bruger i arbejdsgangen, hvis der er en næste bruger. Hvis opgaven ikke skal behandles yderligere, afsluttes arbejdsgangsprocessen. For eksempel har Søren sendt en udgiftsrapport på kr. 6.000, og dette dokument er tildelt til Henrik. Hvis Henrik godkender dokumentet, tildeles det til Mette til godkendelse. Når Mette har godkendt udgiftsrapporten, er arbejdsgangsprocessen afsluttet.

### <a name="reject"></a>Afvis

Når en godkender afviser et dokument, afsluttes arbejdsgangsprocessen. For eksempel har Søren sendt en udgiftsrapport på kr. 12.000, og dette dokument er tildelt til Mette. Hvis Mette afviser udgiftsrapporten, afsluttes arbejdsgangsprocessen. Søren kan sende udgiftsrapporten igen. Han kan udføre ændringerne først, eller han kan sende den oprindelige version af udgiftsrapporten igen. Hvis Søren sender udgiftsrapporten igen, starter arbejdsgangsprocessen ved godkendelsesprocessen.

### <a name="delegate"></a>Delegere

Når en godkender delegerer et dokument, tildeles dokumentet til en anden bruger til godkendelse. For eksempel har Søren sendt en udgiftsrapport på kr. 12.000, og dette dokument er tildelt til Henrik. Henrik delegerer udgiftsrapporten til Dorthe. Dorthe udfører derefter opgaven på vegne af Henrik. Når Dorthe derfor godkender dokumentet, tildeles det til Mette til godkendelse – ligesom hvis Henrik havde godkendt det. Når Mette har godkendt dokumentet, sendes det til Dorthe til godkendelse.

### <a name="request-change"></a>Anmod om ændring

Når en godkender anmoder om en ændring i et dokument, sendes dokumentet tilbage til igangsætteren. For eksempel har Søren sendt en udgiftsrapport på kr. 12.000, og dette dokument er tildelt til Mette. Hvis Mette anmoder om en ændring, sendes dokumentet tilbage til Søren. Søren kan sende udgiftsrapporten igen. Han kan udføre de ønskede ændringer først, eller han kan sende den oprindelige version af udgiftsrapporten igen. Hvis Søren sender udgiftsrapporten igen, sendes den til Henrik til godkendelse, fordi Henrik er den første godkender i godkendelsesprocessen.


