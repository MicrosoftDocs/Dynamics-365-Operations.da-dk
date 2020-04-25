---
title: Frigive stykliste- og formellinjer til lagerstedet
description: I dette emne beskrives processen for frigivelse af råvarer til stykliste- og formellinjer til lagerstedet.
author: johanhoffmann
manager: tfehr
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: dd28e6f96f70c261edc9ba85a9356a704335382b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211186"
---
# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Frigive stykliste- og formellinjer til lagerstedet

[!include [banner](../includes/banner.md)]

I dette emne beskrives processen for frigivelse af råvarer til stykliste- og formellinjer til lagerstedet. Når du frigiver en stykliste- eller formellinje til lagerstedet, afgør systemet først, om materialet allerede findes på indlagringslokationen for produktionen i produktionsanlægget, hvor materialet skal forbruges i produktionsprocessen.

- Hvis materialet er tilgængeligt på produktionsindlagringslokationen, plukkes det fra samme lokation umiddelbart efter, at der er givet signal om frigivelse af materialet til lagerstedet.
- Hvis materialet ikke er tilgængeligt på produktionsindlagringslokationen, angiver materialefrigivelsen, at materiale skal flyttes fra lokationer på lagerstedet til indlagringslokationen. Materialet flyttes via lagerstedsarbejde til pluk af råvarer. Derfor skal lagerprocesser for pluk af råvarer konfigureres. Du kan finde flere oplysninger under [Oversigt over genopfyldning](../warehousing/replenishment.md) og [Styre lagerarbejde ved hjælp af arbejdsskabeloner og lokalitetsdirektiver](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Metoder til frigivelse af stykliste- og formellinjer

Du kan konfigurere frigivelsen af stykliste- og formellinjer, så den forekommer som en del af frigivelsen af en produktionsordre eller en batchordre. Frigivelsen kan også styres af et batchjob eller udføres som en manuel indgriben.

Hvilken metode der bruges til at frigive stykliste- og formellinjer styres af parameteren **Frigivelse af produktionslinje**. Du kan finde denne parameter på **Produktionsstyring** \> **Konfiguration** \> **Produktionsparametre**.

- **Frigiv stykliste- og formellinjer som en del af frigivelsen af produktions- eller batchordren** – Med denne metode frigives stykliste- og formellinjer for en produktions- eller batchordre som en del af processen med at frigive ordren. Normalt under frigivelsen af en produktions- eller batchordre frigives produktionsjob til arbejderne i produktionsanlægget, og der udskrives produktionspapirer. Under denne proces ændres status for ordren også til **Frigivet**.
- **Frigiv stykliste- og formellinjer via et batchjob eller som en manuel indgriben** – Med denne metode kan stykliste- og formellinjer kun frigives via batchjobbet **Automatisk frigivelse af stykliste- og formellinjer** eller via manuel indgriben. Hvis du vil frigive stykliste- og formellinjer manuelt, skal du vælge **Frigiv til lagersted** i handlingsruden Produktionsordre på listesiden eller detaljesiden for produktionsordren.

Du kan se en hurtig demonstration af, hvordan du frigiver stykliste- og formellinjer til produktion ved hjælp af et batchjob, i denne korte YouTube-video: [Frigive produktionspluk til lagerstedet i batch](https://www.youtube.com/watch?v=8urAJn50dQ8).

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>Frigive stykliste- og formellinjer ved hjælp af et batchjob

Batchjobbet **Automatisk frigivelse af stykliste og formellinjer** gennemgår valgte stykliste- og formellinjer, der har et restantal, der skal frigives. Batchjobbet finder kun ordrer, der har status **Frigivet**, **Startet** eller **Færdigmeldt**. Hvis der er et restantal, der skal frigives, for en stykliste- eller formellinje, frigiver jobbet op til det antal, der kan dækkes af det antal, der allerede er fysisk reserveret, og det antal, der er fysisk disponibelt.

### <a name="example-of-a-batch-job-release"></a>Eksempel på en batchjobfrigivelse

| Scenario | Resterende antal til frigivelse | Fysisk reserveret antal | Fysisk disponibelt antal | Antal, der er frigivet af batchjobbet |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Konfiguration af batchjob

I forespørgslen for batchjobbet **Automatisk frigivelse af stykliste og formellinjer**, du kan angive et filterkriterium for at angive, hvor mange dage i forvejen jobbet skal søge efter linjer, der har ikke-frigivne antal. I forespørgslen for jobbet i feltet **Råvaredato** skal du bruge funktionen **(LessThanDate())** som et filterkriterium.

I følgende illustration vises en produktionsordre, der har to job, 10 og 20, der dækker samling og emballage for produktionsordren. Hvert job er konfigureret til at bruge en mængde materiale. I denne illustration er tidshorisonten for frigivelsen, som er angivet af den grønne pil under tidslinjen, lig med antallet af dage, der er angivet i kriteriet **(LessThanDate())**. F.eks. angiver **(LessThanDate(2))**, at jobbet skal søge efter ikke-frigivne mængder inden for en tidshorisont på to dage.

![Eksempel på en produktionsordre, der har to batchjob](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Frigive materiale pr. operationsnummer eller i forhold til antallet af færdigvarer

Hvis du frigiver materialer ved hjælp af parameterindstillingen **Ved frigivelse af produktionsordre**, og du foretager en manuel frigivelse, har du to muligheder for at styre materialefrigivelsen:

- Frigive materiale pr. operationsnummer.
- Frigive materiale i forhold til antallet af færdigvarer.

### <a name="release-material-per-operation-number"></a>Frigive materiale pr. operationsnummer

Hvis du vil styre de operationer, som materialet skal frigives til, skal du bruge siden **Frigiv til lagersted**.

- Vælg **Produktionsstyring** \> **Produktionsordrer** \> **Alle produktionsordrer**, vælg en produktionsordre, og vælg derefter **Frigiv til lagersted** under fanen **Lagersted**. Brug derefter **Fra opr.nr.** og **Til opr.nr.** til at angive rækken af operationsnumre.

I følgende illustration vises en produktionsordre, der har to operationer, 10 og 20. Hvis du i dette eksempel begrænser frigivelsen til operation 10, frigives kun materiale M9203.

![Eksempel på frigivelse af materiale pr. operationsnummer](media/two-operations.PNG)

For en hurtig demonstration af, hvordan du frigiver materiale i forhold til mængden af færdige varer, kan du se denne korte YouTube-video om [forbedringer af frigivelsesprocessen for produktionsordrer](https://www.youtube.com/watch?v=Rm3ojAz6Zu0).

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Frigive materiale i forhold til antallet af færdigvarer

Du kan frigive råvarer for en del af færdigvarerne eller i en bestemt enhed.

- Hvis du vil frigive råvarer for en del af færdigvarerne, skal du vælge **Produktionsstyring** \> **Produktionsordrer** \> **Alle produktionsordrer**, vælge en produktionsordre og derefter vælge **Frigiv til lagersted** under fanen **Lagersted**. Derefter skal du angive et antal i feltet **Antal**.

    F.eks. er der oprettet og planlagt en produktionsordre for 1.000 stk. Den tilsynsførende planlægger produktionen af 100 stk. for det næste skift og ønsker kun at frigive materialer til dette skift. I dette tilfælde kan den tilsynsførende bruge feltet **Antal** til at frigive materialer til de 100 stk., der er planlagt for det næste skift.

- Hvis du vil frigive råvarer i en bestemt enhed, skal du vælge **Produktionsstyring** \> **Produktionsordrer** \> **Alle produktionsordrer**, vælge en produktionsordre og derefter vælge **Frigiv til lagersted** under fanen **Lagersted**. Brug derefter feltet **Enhed** til at vælge enheden for færdigvaren til at frigive materialet i.

    De enheder, der er tilgængelige, defineres i enhedens seriegruppe-id for færdigvaren.

    F.eks. har en færdigvare følgende enhedsomregningen mellem kilo (kg) og palle (PL) følgende: 1 PL = 100 kg. Hvis du vil oprette en produktionsordre på 10.000 kg af færdigvaren, kan du frigive råvarer til antallet af paller, du planlægger at producere. Vælg **PL** som enhed, og vælg derefter et tilsvarende antal i feltet **Antal**.
