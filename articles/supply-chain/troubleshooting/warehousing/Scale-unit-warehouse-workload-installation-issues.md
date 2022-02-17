---
title: Behandlingsproblemer opstår, når arbejdsbyrden for et lagersteds skalaenhed er installeret
description: I dette emne beskrives problemer, der kan forekomme, umiddelbart efter at arbejdsbyrden for et lagersteds skalaenhed er installeret, og giver råd til rettelse af dem.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071621"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Behandlingsproblemer opstår, når arbejdsbyrden for et lagersteds skalaenhed er installeret

I dette emne beskrives problemer, der kan forekomme, umiddelbart efter at arbejdsbyrden for et lagersteds skalaenhed er installeret, og giver råd til rettelse af dem.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>Problem 1: Fejl, efter at en last er frigivet fra et lastplanlægningspanel

### <a name="symptoms-of-issue-1"></a>Symptomer på fejl 1

Når du frigiver en last fra siden **Lastplanlægningspanel** eller **Udgående lastplanlægningspanel**, modtager du en fejlmeddelelse i følgende form:

> Der opstod en undtagelse under bogføring af lasten %1. Lasten kunne ikke frigives.
> 
> UPDATE WHSSHIPMENTTABLE SET ...
> 
> Kan ikke redigere en post i Forsendelser (WHSShipmentTable). Forsendelses-id: ...

Her er et faktisk eksempel med eksempeldata:

> Der opstod en undtagelse under bogføring af lasten USMF-000033. Lasten kunne ikke frigives.
session 5133 (Admin)
>
> UPDATE WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? WHERE ((RECID=?) AND (RECVERSION=?))  
> [Microsoft][ODBC-driver 17 til SQL Server][SQL-server]Skalaenhed @@ forsøgte at opdatere poster, der ejes af skalaenhed @A.  
> Azure-objektserver:
>
> Kan ikke redigere en post i Forsendelser (WHSShipmentTable). Forsendelses-id: USMF-000031, USMF-000033. SQL-databasen har registreret en fejl.

### <a name="cause-of-issue-1"></a>Fejlårsag 1

Dette problem kan forekomme, hvis følgende kombination af betingelser findes, når du installerer arbejdsbyrden for et lagersteds skalaenhed:

- Systemet indeholder en ikke-frigivet last, hvor flere linjer er knyttet til forskellige ordrer, og nogle lastlinjer ikke er knyttet til en forsendelse.
- Systemet er konfigureret til at bruge forsendelseskonsolidering.

I en installation af en distribueret hybridtopologi er hver enkelt last- og forsendelsespost markeret som ejet af en bestemt skalaenhed eller hub. Når du frigiver en last fra siden **Panelet Lastplanlægning**, ændrer systemet det tildelte ejerskab. På grund af de betingelser, der tidligere er angivet, kan systemet dog ikke løse ejerskabet af dataene. Derfor frigives lasten ikke til lagerstedet.

### <a name="resolution-of-issue-1"></a>Løsning på fejl 1

Opdel lasten i to mindre laster, før du frigiver den til lagerstedet.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>Problem 2: Fejl, mens der behandles en bølge på en skalaenhed

### <a name="symptoms-of-issue-2"></a>Symptomer på fejl 2

Når du behandler en bølge på en skalaenhed, modtager du en fejlmeddelelse i følgende form:

> Du kan ikke redigere lastlinjen med RecId = %1, last-id= %2, da den stadig ejes af virksomhedshubben. Kontrollér, at den tilsvarende udgående last er frigivet til en skalaenhed, og at der derved er oprettet ordrelinjer på lagerstedet.

Her er et faktisk eksempel med eksempeldata:

> Infolog for jobbet Udfør bølge USMF-000000012 (9223377668365210)  
> Infolog for opgaven Udfør bølge USMF-000000012 (9223377668370462)  
> Du kan ikke redigere lastlinjen med RecId = 68719478242, last-id= USMF-000034, da den stadig ejes af virksomhedshubben. Kontrollér, at den tilsvarende udgående last er frigivet til en skalaenhed, og at der derved er oprettet ordrelinjer på lagerstedet.

### <a name="cause-of-issue-2"></a>Fejlårsag 2

I en installation af en distribueret hybridtopologi er ejersjab af last- og forsendelsesdata tildelt til en bestemt skalaenhed eller hub. Som en del af bølgebehandlingen forventes det, at ejeren af dataene bliver tildelt til en skalaenhed.

Når du installerer en arbejdsbyrde for et lagersteds skalaenhed, kan systemet ikke styre ejerskabet af data, hvis en åben forsendelse er knyttet til en last og en bølge. Derfor mislykkes behandlingen af bølger på skalaenheden.

### <a name="resolution-of-issue-2"></a>Løsning på fejl 2

Frigiv lasten til lagerstedet fra hubben.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Foretage fejlfinding af problemer med at vise ejerskabet og destinationen for en post

I en installation af en distribueret hybridtopologi er mange posttyper markeret som ejet af en bestemt skalaenhed eller hub. Når du skifter til en distribueret hybridtopologi og/eller konfigurerer en ny lagerstedsbelastning for en skalaenhed, tildeler systemet ejerskabet til hver af de relevante poster. Denne proces kan undertiden give fejl og uventede resultater. Oplysningerne om en posts ejerskab og overførselsdestination kan derfor hjælpe dig med at fejlfinde problemer, der opstår, efter at du har foretaget de pågældende ændringer.

Følg disse trin for at få vist ejerskabet og overførselsdestinationen for en post.

1. Åbn den relevante post.
1. I handlingsruden under fanen **Indstillinger** skal du i gruppen **Postoplysninger** vælge **Vis alle felter**.
1. Den side, der vises, har værdier for alle de felter, der er tilgængelige for den valgte post. Gennemgå følgende felter:

    - **SYSSCALEUNITID** – I dette felt vises den aktuelle ejer af posten.
    - **SYSTARGETSCALEUNITID** – Dette felt viser skalaenheds-id'et for den hub eller skalaenhed, som posten vil blive overført til, når den aktuelle ejer er færdig med at arbejde med den. Værdien i dette felt bruges af batchjob, der administrerer denne procestype. Selvom dette felt ikke er direkte relateret til ejerskabet, kan ejerskabet ændres, når posten overføres. Dette felt er tomt i visse tilfælde.
