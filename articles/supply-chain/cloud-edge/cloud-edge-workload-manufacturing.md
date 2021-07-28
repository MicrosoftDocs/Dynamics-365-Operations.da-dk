---
title: Produktionsarbejdsbyrder for sky- og kantskalaenheder
description: Dette emne beskriver, hvordan produktionsarbejdsbyrder virker sammen med sky- og kantskalaenheder.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: da19066f647c17e934a11e4dab7cb370baabfb5c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352730"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Arbejdsbelastninger i forbindelse med produktionsudførelse for sky- og edge-skaleringsenheder

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Arbejdsbyrden for produktionsudførelse er tilgængelig i forhåndsversion på nuværende tidspunkt.
> Nogle forretningsfunktioner understøttes ikke fuldt ud i den offentlige prøveversion, når der anvendes skalaenheder for arbejdsbyrder.

I produktionsudførelse giver skalaenheder følgende egenskaber:

- Maskinoperatører og tilsynsførende kan få adgang til den operationelle produktionsplan.
- Maskinoperatører kan holde planen opdateret ved at køre diskrete og procesproduktionsjob.
- Den tilsynsførende kan justere driftsplanen.
- Arbejderne kan få adgang til fremmøde og indstemplings- og udstemplingstid på kanten for at sikre en korrekt beregning af arbejderes løn.

Dette emne beskriver, hvordan produktionsarbejdsbyrder virker sammen med sky- og kantskalaenheder.

## <a name="the-manufacturing-lifecycle"></a>Livscyklussen for produktion

Når følgende illustration vises, er produktions livscyklussen opdelt i tre faser: *Planlæg*, *Udfør* og *Færdiggør*.

[! [Produktionsudførelsesfaser, når der bruges et enkelt miljø](media/mes-phases.png "Produktionsudførelsesfaser, når der bruges et enkelt miljø."](media/mes-phases-large.png)

Fasen _Planlæg_ omfatter produktdefinition, planlægning, oprettelse og planlægning af ordrer og frigivelse. Frigivelsestrinnet angiver overgangen fra fasen _Planlæg_ til fasen _Udfør_. Når en produktionsordre frigives, vil produktionsordrejobbene være synlige i produktionen og være klar til udførelse.

Når et produktionsjob er markeret som fuldført, flyttes det fra fasen _Udfør_ til fasen _Færdiggør_. I fasen _Færdiggør_ går registreringerne fra fasen *Udfør* via en godkendelsesarbejdsproces, hvor de beregnes, godkendes og overføres. På dette tidspunkt er produktionsordren fuldført. Derfor genereres udgangspunktet for arbejderens løn.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Opdeling af udførelsesfasen i en separat arbejdsbyrde

Som følgende illustration viser er fasen _Udfør_ opdelt som en separat belastning, når der bruges skalaenheder.

[![Produktionsudførelsesfaser, når der bruges vægtenheder](media/mes-phases-workloads.png "Produktionsudførelsesfaser, når der bruges vægtenheder."](media/mes-phases-workloads-large.png)

Modellen går nu fra en installation med én forekomst til en model, der er baseret på hubben og skalaenhederne. Faserne _Planlæg_ og _Færdiggør_ kører som baggrundshandlinger på hubben, og arbejdsbyrden for produktionsudførelse kører på skalaenhederne. Data overføres asynkront mellem hubben og skalaenhederne.

Når en produktionsordre frigives på hubben, overføres alle de data, der er nødvendige for at behandle produktionsjob, til skalaenheden. Disse data omfatter produktionsordrer, produktionsruter, styklister og produkter. Data, der ikke er relateret til en produktionsordre (f.eks. indirekte aktiviteter, fraværskoder og produktionsparametre), overføres også fra hubben til skalaenheden. Som regel kan data, der kommer fra hubben og overføres til skalaenheden, kun oprettes eller opdateres på hubben. En ny fraværskode eller indirekte aktivitet kan f.eks. ikke oprettes på skalaenheden, og de kan kun bruges til registrering. De registreringer, der foretages på skalaenheden under udførelsen, overføres derefter til hubben, hvor tids og fremmødegodkendelse, lager og økonomiske opdateringer behandles.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Produktionsudførelsesopgaver, der kan køres på arbejdsbyrder

Følgende opgaver for produktionsudførelse kan i øjeblikket køres på arbejdsbyrder, når der bruges skalaenheder:

- Indstempling, login, udstempling og fravær
- Start job
- Bundte job
- Rapport i gang
- Rapportér spild
- Indirekte aktivitet
- Pause
- Færdigmeld og læg på lager (kræver, at du også kører arbejdsbyrden for lagerstedsudførelse på skalaenheden. Se også [Færdigmelde og lægge på lager på en skalaenhed](#RAF))

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Arbejde med arbejdsbelastninger i produktionsudførelse på hubben

De processer, der kræves for at køre arbejdsbelastninger for produktionsudførelse, kører som regel automatisk for at holde hubben og alle skalaenheder synkrone efter behov. Men hvis du har problemer, kan du manuelt udløse behandlingen af rå registreringer, der modtages fra arbejdsbyrder, og/eller kontrollere registreringsbehandlingsloggen.

### <a name="manually-process-raw-registrations"></a>Behandle rå registreringer manuelt

Et batchjob i Supply Chain Management kører automatisk for at behandle alle registreringer, der er modtaget fra arbejdsbyrderne. Dette job opretter de nødvendige produktionskladder og logbogsposter, når en registrering behandles for en fuldført opgave på arbejdsbyrden.

Selvom jobbet normalt køres automatisk, kan du køre det manuelt på et hvilket som helst tidspunkt ved at logge på hubben og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandle rå registreringer**.

### <a name="check-the-raw-registration-processing-log"></a>Kontrollere behandlingsloggen for rå registrering

Hvis du vil gennemgå registreringsbehandlingsloggen, skal du logge på hubben og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandlingslog for rå registrering**. På siden **Behandlingslog for rå registrering** vises en liste over behandlede rå registreringer og status for hver registrering.

![Siden Behandlingslog for rå registrering.](media/mes-processing-log.png "Siden Behandlingslog for rå registrering")

Du kan arbejde på enhver registrering på listen ved at markere den og derefter vælge en af følgende knapper i handlingsruden:

- **Proces** – Behandler den valgte registrering manuelt. Denne handling kan være nyttig, hvis jobbet _Behandle rå registreringer_ ikke er kørt, eller hvis det mislykkedes.
- **Annuller** – Annuller den valgte registrering.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Arbejde med arbejdsbelastninger i produktionsudførelse på en skalaenhed

De processer, der kræves for at køre arbejdsbelastninger for produktionsudførelse, kører som regel automatisk for at holde hubben og alle skalaenheder synkrone efter behov. Men hvis du har problemer, kan du kontrollere historikken for de ordrer, der er behandlet på en skalaenhed, eller manuelt køre jobbet _Meddelelsesprocessor for produktionshub til skalaenhed_.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Se historikken for de produktionsjob, der er behandlet på en skalaenhed

Hvis du vil gennemgå historikken for de produktionsjob, der er behandlet på en skalaenhed, skal du logge på skalaenhedens maskine og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandlingshistorik for produktionsjob**. Siden **Behandlingshistorik for produktionsjob** viser behandlingshistorikken for produktionsordrerne på skalaenheden. Du kan arbejde på enhver produktionsordre på listen ved at markere den og derefter vælge en af følgende knapper i handlingsruden:

- **Proces** – Behandler den valgte produktionsordre manuelt.
- **Annuller** – Annullerer den valgte produktionsordre.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Jobbet Meddelelsesprocessor for produktionshub til skalaenhed

Jobbet _Meddelelsesprocessor for produktionshub til skalaenhed_ behandler data fra hubben til skalaenheden. Dette job startes automatisk, når arbejdsbyrden for produktionsudførelse udrulles. Du kan dog køre den manuelt på et hvilket som helst tidspunkt ved at gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Meddelelsesprocessor for produktionshub til skalaenhed**.

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a>Færdigmelde og lægge på lager på en skalaenhed

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

I den aktuelle version understøttes færdigmeldings- og lagringsoperationer (for færdigvarer, samprodukter og biprodukter) af [arbejdsbyrden for lagerstedsudførelse](cloud-edge-workload-warehousing.md) (ikke arbejdsbyrden for produktionsudførelse). Hvis du vil bruge denne funktion, når den er knyttet til en skalaenhed, skal du derfor gøre følgende:

- Installer både arbejdsbyrden for udførelse af lagersteder og arbejdsbyrden for produktionsudførelse på din skalaenhed.
- Du kan bruge mobilappen Warehouse Management til at færdigmelde og behandle læg på lager-arbejdet. Grænsefladen til produktionsudførelse understøtter i øjeblikket ikke disse processer.

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
