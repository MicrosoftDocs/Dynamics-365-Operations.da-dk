---
title: Batchbehandling af påmindelser
description: Dette emne indeholder oplysninger om batchafvikling af påmindelser.
author: tjvass
manager: AnnBe
ms.date: 09/10/2010
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a06ca45de3a7bb6d65a8ed5466cd6591d4e0820f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180800"
---
# <a name="batch-processing-of-alerts"></a>Batchbehandling af påmindelser

[!include [banner](../includes/banner.md)]

Påmindelser afvikles af funktionen til batchafvikling. Du skal konfigurere batchbehandling, før påmindelser kan leveres.

Der understøttes to typer hændelser:

- Hændelser, der udløses af ændringsbaserede hændelser. Disse hændelser, der også kaldes oprette-/slette- og opdateringshændelser.
- Hændelser, der udløses af forfaldsdatoer.

Du kan oprette batchafviklinger for hver af disse hændelsestyper.
        
## <a name="batch-processing-for-change-based-events"></a>Batchbehandling af ændringsbaserede hændelser

Systemet læser alle ændringsbaserede hændelser, der er indtruffet efter batchafvikling sidst blev kørt. Ændringsbaserede hændelser omfatter opdateringer af felter, sletning af poster og oprettelse af poster. Disse hændelser sammenlignes med de betingelser, der er angivet i påmindelsesreglerne. Hvis en hændelser matcher betingelserne i en regel, udløser batchprocessen en påmindelse.

### <a name="frequency-for-change-based-events"></a>Frekvens for ændringsbaserede hændelser

For ændringsbaserede hændelser kan du oprette et batchjob, der udløser afviklingen af en hændelse, lige efter at hændelse er logget af systemet. Hvis du konfigurerer, at batchjobbet skal gentages oftere, modtager brugerne deres påmindelser hurtigere, når der opstår ændringer. Men en høj frekvens til batchbehandling kan påvirke systemets ydeevne negativt.

På den anden side kan et batchjob, der skal gentages mindre hyppigt, og som der er planlagt til tidspunkter, hvor systembelastningen er lav, hjælpe med til at forbedre systemets ydeevne. En lav frekvens for batchbehandling kan imidlertid ikke opfylde brugernes behov for rettidig beskeder.

Så når frekvensen for de ændringsbaserede hændelsesbatches angives, skal du være opmærksom på balancen mellem det tidsmæssige behov for påmindelser og ydeevnen for hele systemet. Jo flere brugere, der opretter påmindelsesregler, desto mere relevant er disse overvejelser. Hyppigheden påvirker ikke antallet af hændelser, der skal behandles. Men hvis flere brugere opretter regler, skal der udføres flere kontroller. Denne type af dataudveksling kan have indflydelse på systemets ydeevne.

#### <a name="the-risks-of-low-batch-frequency"></a>Risiciene ved en lav batchfrekvens

Hvis du har angivet en lav frekvens for batchbehandling af ændringsbaserede hændelser, kan data, der er relevante for betingelserne for påmindelsesregler, muligvis være ændret før afviklingen af batchen. Derfor kan du miste påmindelser.

Der er f.eks. konfigureret en påmindelsesregel, der skal udløse en påmindelse, når hændelsen er **ændringer for kundekontakt**, og betingelsen er **kunde = BB**. Når der opstår ændringer for kundekontakten for kunde BB, logføres hændelsen med andre ord. Batchafviklingssystemet er dog konfigureret sådan, at batchafvikling optræder mindre hyppigt end dataindtastning. Hvis kundenavnet ændres fra **BB** til **AA**, før hændelsen er behandlet, svarer dataene i databasen ikke længere til betingelsen i reglen **kunde = BB**. Derfor genereres der ingen påmindelse, når hændelsen er endelig afvikles.

### <a name="set-up-processing-for-change-based-alerts"></a>Konfigurere behandlingen af ændringsbaserede påmindelser

1. Gå til **Systemadministration** &gt; **Periodiske opgaver** &gt; **Påmindelser** &gt; **Ændringsbaserede påmindelser**.
2. I dialogboksen **Ændringsbaserede påmindelser** skal du angive de relevante oplysninger.

## <a name="batch-processing-for-due-date-events"></a>Batchbehandling af forfaldsdatohændelser

Systemet registrerer alle hændelser, der udløses af forfaldsdatoer, hvorefter disse hændelser sammenlignes med de betingelser, der er angivet i påmindelsesreglerne. Hvis en hændelser matcher betingelserne i en regel, udløser batchprocessen en påmindelse.

### <a name="frequency-for-due-date-events"></a>Frekvens for forfaldsdatohændelser

For forfaldsdatohændelser kan det være en god idé at angive de batchjob, der skal køres i løbet af natten eller på bestemte tidspunkter af dagen for at afbalancere belastningen af systemet. Det anbefales, at du konfigurerer batchjobbet, så det kører mindst én gang om dagen. Hvis påmindelser skal sendes så tidligt som muligt, skal batchbehandlingen konfigureres til at afvikles straks efter, at systemdatoen skifter. Hvis du vil generere påmindelser fra forfaldsdatohændelser, der finder sted, efter at et batchjob har behandlet påmindelser, kan du køre batchjobbet igen den samme dag.

For eksempel er et batchjob blevet kørt på en bestemt dag. Derefter opretter du en indkøbsordre med en forfaldsdato, der bør udløse en påmindelse på samme dag. Hvis du vil modtage påmindelsen på den pågældende dag, skal du køre batchjobbet igen, efter at indkøbsordren er oprettet. Hvis du til gengæld ikke kører batchjobbet igen på den pågældende dag, registrerer den næste dags batchjob alle forfaldsdatohændelser, der ikke blev behandlet de foregående dage.

> [!NOTE]
> Selvom batchprocessen køres mere end én gang om dagen, duplikeres påmindelser ikke for den samme forfaldsdatohændelse og de samme betingelser. Beskeder oprettes kun for datoer, der er blevet behørigt på grund af ændringer, der er opstået i systemet efter den seneste kørsel blev kørt.

### <a name="batch-processing-window"></a>Batchafviklingsvindue

Behandlingen af påmindelsesregler i en virksomhed kan stoppes af flere grunde. Disse årsager omfatter ferier, systemfejl eller andre problemer, der forhindrer batchjob i, at blive kørt i et stykke tid.

For at forhindre at forfaldsdatopåmindelser bliver overflødige, fordi batchjobbet ikke er kørt i flere dage, kan du konfigurere et batchbehandlingsvindue. Batchbehandlingsvinduet kan bruges til at forhindre, at et batchjob køres i et bestemt antal dage.

Hvis du konfigurerer et batchbehandlingsvindue, sendes der en påmindelse, når påmindelsesreglen behandles, også selvom påmindelsen overskrider den tidsgrænse, der er defineret kriterierne for forfaldsdato. Der sendes fortsat en påmindelse, så længe den periode, der er defineret af denne frist plus batchbehandlingsvinduet, ikke overskrides. Når den periode, der er defineret af fristen samt batchafviklingsvinduet overskrides, sendes der ikke længere en påmindelse.

### <a name="set-up-processing-for-due-date-alerts"></a>Konfigurere behandlingen af påmindelser udløst af forfaldsdato

1. Gå til **Systemadministration** &gt; **Periodiske opgaver** &gt; **Påmindelser** &gt; **Påmindelser udløst af forfaldsdato**.
2. I dialogboksen **Påmindelser udløst af forfaldsdato** skal du angive de relevante oplysninger.
