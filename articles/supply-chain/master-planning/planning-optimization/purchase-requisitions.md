---
title: Indkøbsrekvisitioner
description: Dette emne beskriver, hvordan indkøbsrekvisitioner understøttes i Planlægningsoptimering.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 62a42e2403fe024bd7ea49bff5bef139964e944727a245a480bc240c112154cf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738981"
---
# <a name="purchase-requisitions"></a>Indkøbsrekvisitioner

Ved varedisponering kan godkendte indkøbsrekvisitioner genopfyldes. Derfor behøver brugerne ikke bruge en arbejdsproces til at oprette indkøbsordrer for at dække indkøbsrekvisitioner. Indkøbsrekvisitioner kan i stedet dækkes af varedisponeringen. På grund af denne funktion kan en indkøbsrekvisition oprette en indkøbsordre, en flytteordre eller en produktionsordre afhængigt af den **Ordreforslagstype**-værdi, der er angivet for det relaterede produkt.

## <a name="enable-master-plans-to-include-requisitions"></a>Gøre det muligt for behovsplaner at indeholde rekvisitioner

Du kan medtage rekvisitioner under beregningen af disponeringen for en behovsplan ved at følge disse trin.

1. Gå til **Varedisponering** \> **Opsætning** \> **Planer** \> **Behovsplaner**.
1. Opret eller vælg en behovsplan.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Medtag rekvisitioner** til *Ja*.
1. Gentag trin 2 og 3 for hver ekstra behovsplan, hvor du vil medtage rekvisitioner.

## <a name="approved-requisitions-time-fence"></a>Tidshorisont for godkendte rekvisitioner

*Tidshorisonten for godkendte rekvisitioner* fastlægger, hvor langt tilbage (i dage) en behovsplan vil medtage efterspørgsler fra godkendte genopfyldningsrekvisitioner. Du kan angive en tidshorisont for godkendte rekvisitioner på både disponeringsgruppeniveau og behovsplanniveau.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Angive tidshorisonten for godkendte rekvisitioner for en disponeringsgruppe

1. Gå til **Varedisponering** \> **Opsætning** \> **Dækning** \> **Dækningsgrupper**.
1. Opret eller vælg en disponeringsgruppe.
1. På oversigtspanelet **Andet** skal du angive **Tidshorisont (dage) for godkendte rekvisitioner** til det antal dage, der skal medtages i tidshorisonten.
1. Gentag trin 2 og 3 for hver ekstra disponeringsgruppe, hvor du vil angive en tidshorisont for godkendte rekvisitioner.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Angive tidshorisonten for godkendte rekvisitioner for forskellige behovsplaner

Når du angiver en tidshorisont for godkendte rekvisitioner for en enkelt behovsplan, tilsidesætter indstillingen tidshorisonten for alle relevante disponeringsgrupper.

1. Gå til **Varedisponering** \> **Opsætning** \> **Planer** \> **Behovsplaner**.
1. Opret eller vælg en behovsplan.
1. På oversigtspanelet **Tidshorisonter i dage** skal du angive **Tidshorisont (dage) for godkendte rekvisitioner** til det antal dage, der skal medtages i tidshorisonten.
1. Gentag trin 2 og 3 for hver ekstra behovsplan, hvor du vil angive en tidshorisont for godkendte rekvisitioner.

> [!IMPORTANT]
> **Kommer snart:** Tidshorisonter for godkendte rekvisitioner understøttes endnu ikke til Planlægningsoptimering. Indtil de understøttes, ignoreres alle de værdier, du angiver i feltet **Tidshorisont (dage) for godkendte rekvisitioner**.

## <a name="independent-supply-regardless-of-coverage-code"></a>Uafhængig forsyning, uanset disponeringskoden

Indkøbsrekvisitioner dækkes altid af uafhængige ordreforslag, uanset disponeringskoden. Denne funktionalitet sikrer klar sporing og klare arbejdsprocesser mellem indkøbsrekvisitioner og genopfyldningsordrer.

### <a name="example-1"></a>Eksempel 1

Et produkt er konfigureret til at have en **disponeringskodeværdi** på *min./maks.*. Det har følgende statusser for lager og rekvisitioner:

- Mængde disponibel lagerbeholdning = 10.
- Minimum lagerantal = 15.
- Maks. lagerantal = 20.
- Der findes en indkøbsrekvisition for ét styk. Den har en ønsket dato for dags dato.

Når varedisponering kører, oprettes der to ordreforslag: et på 10 styk for at genopfylde lageret med det maksimale antal, og et på ét styk for at genopfylde indkøbsrekvisitionen.

### <a name="example-2"></a>Eksempel 2

Et produkt er konfigureret til at have en **disponeringskodeværdi** på *min./maks.*. Det har følgende statusser for lager og rekvisitioner:

- Mængde disponibel lagerbeholdning = 17.
- Minimum lagerantal = 15.
- Maks. lagerantal = 20.
- Der findes en indkøbsrekvisition for ét styk. Den har en ønsket dato for dags dato.

Når varedisponering kører, oprettes der et ordreforslag for ét styk til genopfyldning af indkøbsrekvisitionen.

### <a name="example-3"></a>Eksempel 3

Et produkt er konfigureret til at have en **disponeringskodeværdi** for *Periode* og en periodelængde på syv dage. Den har følgende statusser for lager, salgsordre og rekvisition:

- Mængde disponibel lagerbeholdning = 0.
- Der findes en salgsordre på fem styk. Den har en forventet afsendelsesdato i dag plus én dag.
- Der findes en indkøbsrekvisition for tre styk. Den har en ønsket dato for dags dato plus tre dage.

Når varedisponering kører, oprettes der to ordreforslag: et på tre styk for at genopfylde indkøbsrekvisitionen og et på fem styk for at genopfylde salgsordrebehovet.

> [!NOTE]
> Når et ordreforslag, der er udlignet til en indkøbsrekvisition, er autoriseret, holder planlægningsprogrammet udligningen på indkøbsrekvisitionen. Hvis den autoriserede ordre senere viser sig at mangle et antal, der skal bruges til at opfylde indkøbsrekvisitionen, opretter systemet et nyt ordreforslag for differencen.

Du kan finde flere oplysninger om indkøbsrekvisitioner i [Oversigt over indkøbsrekvisitioner](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]