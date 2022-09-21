---
title: Oprette fakturalinjer, når du importerer kreditorfakturaer
description: Denne artikel beskriver funktionen til automatisk generering af fakturalinjer på kreditorfakturaer, når fakturaer importeres.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5cb2c1234de03e9777921c18e4cbb81eec7feef9
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462268"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Oprette fakturalinjer, når du importerer kreditorfakturaer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel beskriver funktionen til automatisk generering af fakturalinjer på kreditorfakturaer, når fakturaer importeres.

Kreditorfakturaer indeholder nogle gange begrænsede oplysninger, f.eks. modtageroplysninger og subtotaler. De indeholder dog ingen oplysninger om linjeelementer. Når du importerer fakturaer, genereres automatisk fakturalinjer baseret på oplysninger om den tilsvarende indkøbsordre.

Benyt følgende fremgangsmåde for at aktivere automatisk oprettelse af fakturalinjer.

1.  Gå til **Kreditor \> Opsætning \> Kreditorparametre**.
2.  Angiv indstillingen **Automatisk oprettelse af fakturalinjer** til **Ja** under **Automatisk linjeoprettelse for importerede fakturaer** under fanen **Automatisering af kreditorfaktura**. 
4.  Vælg det antal, der skal bruges til automatisk oprettelse af fakturalinjer, i feltet **Vælg standardmængde for automatisk oprettelse af fakturalinjer**:

    - **Bestilt antal** – Systemet genererer linjer fra indkøbsordrelinjer. Denne værdi er standardværdien.
    - **Antal produktkvitteringer** – Indkøbsordrenummeret bruges til at finde de relevante produktkvitteringer. Derefter bruges produktkvitteringsantallet til at generere fakturalinjer.

## <a name="data-entity-changes"></a>Ændringer af dataenhed

For at understøtte de funktioner, der er beskrevet i denne artikel, er dataenheden **Kreditorfakturahoved** blevet udvidet. Der er tilføjet tre felter:

- **HeaderOnlyImport** – Dette felt skal angives til **Ja** for at generere linjer til fakturahoveder.
- **PurchIdRange** – Listen over indkøbsordrenumre. Fakturanumrene kan være inden for et interval, f.eks. **PO0001..PO0009** (hvor to prikker adskiller start og afslutning af intervallet) eller adskilte værdier, f.eks. **PO0001, PO0003, PO0006**. Alle indkøbsordrer skal tilhøre samme kreditorkonto i fakturahovedet. Ellers vises følgende fejlmeddelelse: "Der kunne ikke oprettes fakturalinjer. Indkøbsordrer har forskellige kreditorkonti."
- **PackingslipRange** – Listen over produktkvitteringsnumre. Kreditorfakturalinjer kan oprettes ud fra produktkvitteringer. Produktkvitteringsnumre indgår dog ikke typisk på kreditorfakturaer. Du skal kun angive produktkvitteringsnumrene i dette felt, hvis du tydeligt kan identificere, hvilke produktkvitteringer der er specifikke fakturaer for. Fakturalinjer kan oprettes ud fra produktkvitteringer. Hvis dette felt bruges, ignoreres indstillingen af feltet **Vælg standardantal til automatisk oprettelse af fakturalinjer** på siden **Kreditorparametre**. 

**Begrænsning**: Hvis du angiver flere produktkvitteringsnumre, oprettes der flere ventende kreditorfakturaer med samme fakturanummer. Du skal konsolidere dem manuelt, før du behandler fakturaen yderligere. I fremtidige versioner planlægger vi at konsolidere fakturaerne automatisk, så begrænsningen fjernes.

Alle produktkvitteringer skal tilhøre samme kreditorkonto i fakturahovedet.

## <a name="result"></a>Resultat

Hvis der genereres linjer korrekt, logges følgende meddelelse i historikken for automatisk oprettelse af kreditorfakturaer: "Opret automatisk fakturalinjer: Fuldført".

Hvis der ikke genereres linjer, registreres følgende fejlmeddelelse: "Opret automatisk fakturalinjer: Mislykkedes".
