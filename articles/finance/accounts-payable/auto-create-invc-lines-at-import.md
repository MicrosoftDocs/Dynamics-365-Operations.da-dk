---
title: Oprette fakturalinjer, når du importerer kreditorfakturaer
description: Dette emne beskriver funktionen til automatisk generering af fakturalinjer på kreditorfakturaer, når fakturaer importeres.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 87dec3c142ae296975ab98432421be4548085c80
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647879"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Oprette fakturalinjer, når du importerer kreditorfakturaer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne beskriver funktionen til automatisk generering af fakturalinjer på kreditorfakturaer, når fakturaer importeres.

Kreditorfakturaer indeholder nogle gange begrænsede oplysninger, f.eks. modtageroplysninger og subtotaler. De indeholder dog ingen oplysninger om linjeelementer. Når du importerer fakturaer, kan systemet automatisk generere fakturalinjer baseret på oplysninger om den tilsvarende indkøbsordre.

Benyt følgende fremgangsmåde for at aktivere automatisk oprettelse af fakturalinjer.

1.  Gå til **Kreditor \> Opsætning \> Kreditorparametre**.
2.  Angiv indstillingen **Automatisk oprettelse af fakturalinjer** til **Ja** under **Automatisk linjeoprettelse for importerede fakturaer** under fanen **Automatisering af kreditorfaktura**. 
4.  Vælg det antal, der skal bruges til automatisk oprettelse af fakturalinjer, i feltet **Vælg standardmængde for automatisk oprettelse af fakturalinjer**:

    - **Bestilt antal** – Systemet genererer linjer fra indkøbsordrelinjer. Denne værdi er standardværdien.
    - **Antal produktkvitteringer** – Systemet vil bruge indkøbsordrenumre til at finde de relevante produktkvitteringer. Derefter bruges produktkvitteringsantallet til at generere fakturalinjer.

## <a name="data-entity-changes"></a>Ændringer af dataenhed

For at understøtte de funktioner, der er beskrevet i dette emne, er dataenheden **Kreditorfakturahoved** blevet udvidet. Der er tilføjet tre felter:

- **HeaderOnlyImport** – Dette felt skal angives til **Ja**, for at systemet kan generere linjer til fakturahoveder.
- **PurchIdRange** – Listen over indkøbsordrenumre. Fakturanumrene kan være inden for et interval, f.eks. **INV0001. INV0009** (hvor to prikker adskiller start og afslutning af intervallet) eller adskilte værdier, f.eks. **INV0001, INV0003, INV0006**. Alle indkøbsordrer skal tilhøre samme kreditorkonto i fakturahovedet. Ellers vises følgende fejlmeddelelse: "Der kunne ikke oprettes fakturalinjer. Indkøbsordrer har forskellige kreditorkonti."
- **PackingslipRange** – Listen over produktkvitteringsnumre. Kreditorfakturalinjer kan oprettes ud fra produktkvitteringer. Produktkvitteringsnumre indgår dog ikke typisk på kreditorfakturaer. Du skal kun angive produktkvitteringsnumrene i dette felt, hvis du tydeligt kan identificere, hvilke produktkvitteringer der er specifikke fakturaer for. Fakturalinjer kan oprettes ud fra produktkvitteringer. Og hvis dette felt bruges, ignoreres indstillingen af feltet **Vælg standardantal til automatisk oprettelse af fakturalinjer** på siden **Kreditorparametre**. 

**Begrænsning**: Hvis du angiver flere produktkvitteringsnumre, oprettes der flere ventende kreditorfakturaer med samme fakturanummer. Du skal konsolidere dem manuelt, før du behandler fakturaen yderligere. I fremtidige versioner planlægger vi at aktivere systemet til automatisk konsolidering af fakturaerne, så begrænsningen fjernes.

Alle produktkvitteringer skal tilhøre samme kreditorkonto i fakturahovedet.

## <a name="result"></a>Resultat

Hvis systemet genererer linjer, logges følgende meddelelse i historikken for automatisk oprettelse af kreditorfakturaer: "Opret automatisk fakturalinjer: Fuldført".

Hvis der ikke genereres linjer i systemet, registreres følgende fejlmeddelelse: "Opret automatisk fakturalinjer: Mislykkedes".
