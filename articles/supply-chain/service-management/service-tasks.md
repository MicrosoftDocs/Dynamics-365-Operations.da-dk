---
title: Oversigt over serviceopgaver
description: Du kan bruge serviceopgaver, når du skal beskrive den opgave, der skal fuldføres i forbindelse med en serviceordre. Både teknikere og kunder ser disse oplysninger.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b5bf87fbe5ecb711f641a006d56c94d6e679944
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338369"
---
# <a name="service-tasks-overview"></a>Oversigt over serviceopgaver

[!include [banner](../includes/banner.md)]

Du kan bruge serviceopgaver, når du skal beskrive den opgave, der skal fuldføres i forbindelse med en serviceordre.
Både teknikere og kunder ser disse oplysninger.

Du opretter serviceopgaver på siden **Serviceopgaver**, og du kan knytte serviceopgaver til en bestemt serviceaftale eller serviceordre ved at oprette serviceopgaverelationer. Hver gang du opretter en serviceopgaverelation, kan du oprette følgende:

-  Interne noter til opgaven, f.eks. detaljerede oplysninger om tekniske krav til opgaven, som det er vigtigt, at teknikeren kender til.

-  Eksterne noter, der kan ses af kunden. Det kan f.eks. være en knap så teknisk beskrivelse af den opgave, der udføres i overensstemmelse med aftalen mellem kunden og servicefirmaet.

Når du har oprettet en serviceopgaverelation mellem en serviceopgave og en serviceordre eller serviceaftale, kan du angive denne serviceopgave, når du opretter serviceordrelinjer eller serviceaftalelinjer til den aktuelle serviceordre eller serviceaftale.

Når du genererer serviceordrer fra en serviceaftale, kan du gruppere serviceordrelinjer i serviceordrer på basis af de serviceopgaver, der er tildelt de enkelte aftalelinjer.

## <a name="create-a-service-task"></a>Oprette en serviceopgave

1. Klik på **Servicestyring** \> **Opsætning** \> **Serviceopgaver**.
2. Opet en ny linje.
3. Angiv service-id og beskrivelse.

## <a name="example"></a>Eksempel

En tekniker skal udføre to job på en gearkasse (serviceobjekt GB-1234) hos en kunde. Der oprettes en serviceaftale til kunden, og flere konteringer knyttes til disse job. Der er følgende serviceaftale og serviceaftalelinjer for de to job:

### <a name="service-agreement"></a>Serviceaftale

| Project | Serviceaftale | Beskrivelse                                  | Multi   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Eftersyn og rutinemæssig udskiftning – GB-1234 | Løntillæg |

### <a name="service-agreement-lines"></a>Serviceaftalelinjer

| Beskrivelse             | Posteringstype | Seriviceobjekt | Serviceopgave |
|-------------------------|------------------|----------------|--------------|
| Eftersyn og rensning | Time             | GB-1234        | I/C - GB1234 |
| Transport                  | Expense          | GB-1234        | I/C - GB1234 |
| Materialer               | Post             | GB-1234        | I/C - GB1234 |
| Rutinemæssig udskiftning     | Time             | GB-1234        | RR - GB1234  |
| GR-1                    | Post             | GB-1234        | RR - GB1234  |
| GR-5                    | Post             | GB-1234        | RR - GB1234  |

Serviceaftalelinjerne for de to job har to tilknyttede serviceopgaver. Serviceopgaverne bestemmer, hvilke transaktioner der er forbundet med hvert job. I det første tilfælde identificerer serviceopgaven I/C - GB1234 alle de serviceaftalelinjer, der indgår i eftersynet og rensningen af objektet GB-1234. I det andet tilfælde identificerer serviceordren R - GB1234 alle de serviceaftalelinjer, der indgår i fuldførelse af en rutinemæssig udskiftning.

Følgende serviceopgaverelationer udgør forbindelsen mellem serviceopgaverne og den bestemte aftale:

### <a name="service-tasks"></a>Serviceopgaver

| Serviceopgave | Beskrivelse                             | Intern note                                                                                                                 | Ekstern note                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Eftersyn af gearkasse GB-1234           | Visuelt og mekanisk eftersyn og rensning af gearkasse GB-1234                                                              | Rutinemæssigt eftersyn af gearkasse |
| RR - GB1234  | Rutinemæssig udskiftning af dele i GB-1234 | Rutinemæssig udskiftning af komponenterne GR-1 GR-5 (i gearkasser, der er produceret før 2002, skal komponenten GR-2 også udskiftes) | Rutinemæssig udskiftning af dele  |

## <a name="group-service-orders"></a>Gruppere serviceordrer

Når der oprettes serviceordrer automatisk, kan du bruge serviceopgaver som grupperingskriterium. Hvis du vil gruppere serviceordrer efter serviceopgaver, skal det angives i serviceaftalen, at serviceordrer, der er baseret på serviceaftalen, skal grupperes efter serviceopgavens id som første grupperingskriterium.

**Gruppere efter serviceopgave**

1. Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.
2. Under fanen **Opsætning** skal du vælge **Efter serviceopgave** i feltet **Kombinere serviceordrer**.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]