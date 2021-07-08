---
title: Lagerstedsordrer til sky- og kantskalaenheder
description: Dette emne indeholder oplysninger om lagerstedsordrefunktionaliteten, der bruges som en del af arbejdsbyrden for lagerstedsskalaenheden.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 080d45170c726cd0351ab344254aa36c1c56ba55
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271250"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Lagerstedsordrer til sky- og kantskalaenheder

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ikke alle forretningsfunktioner understøttes fuldt ud i den offentlige prøveversion, når der anvendes skalaenhed for arbejdsbyrder. Hvis du bruger skalaenheder, skal du sørge for kun at bruge de processer, som dette emne direkte beskriver som understøttede.

## <a name="what-are-warehouse-orders"></a>Hvad er lagerstedsordrer?

*Lagerstedsordrer* er en ordretype, der er oprettet for at understøtte implementering af lagersteders hub og skalaenhed. De giver dig mulighed for at modtage lager, når du kører en lagerstedsbelastning på en skalaenhed. De bruges i øjeblikket kun i forbindelse med indkøbsordrer.

Lagerstedsordrer bruges som en del af behandlingen af lokationsstyring, f.eks. når mobilappen Lokationsstyring bruges til at registrere fysisk lagerbeholdning under behandlingen af en indgående indkøbsordre. Lagerstedsordrer oprettes som en del af processen *Frigiv til lagersted*, der er tilgængelig for indkøbsordrer, som angiver et skalaenhedslagersted og varer, der er aktiveret til at bruge lokationsstyringsprocesser.

> [!IMPORTANT]
> Lagerstedsordrer er kun tilgængelige i installationer, hvor der bruges [sky- og kantskalaenheder til arbejdsbyrder i lokationsstyring](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Oprette en lagerstedsordre

Følg disse trin for at oprette en lagerstedsordre.

1. Log på forekomsten af Microsoft Dynamics 365 Supply Chain Management, der kører på hubben. (Du skal starte *Frigiv til lagersted*-processen, mens du er logget på hubben).
1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.
1. Hvis du vil se de tilknyttede ordrelinjer for lagerstedet, skal du åbne den relevante indkøbsordre, vælge en linje i sektionen **Indkøbsordrelinjer** og derefter vælge **Lagersted \> Ordrelinjer for lagersted**. Du kan få vist alle linjerne ved at gå til **Lokationsstyring \> Forespørgsler og rapporter \> Ordrelinjer for lagersted**.

Du kan også udløse processen *Frigiv til lagersted* fra et batchjob ved at gå til **Lokationsstyring > Frigiv til lagersted > Automatisk frigivelse af indkøbsordrer**. Når du konfigurerer batchjobbet, kan du vælge bestemte indkøbsordrelinjer baseret på en forespørgsel. Det vil typisk være at konfigurere et tilbagevendende batchjob, der frigiver alle de bekræftede indkøbsordrelinjer, der forventes at ankomme næste dag.

## <a name="cancel-a-warehouse-order"></a>Annullere en lagerstedsordre

Som en del af processen *Frigiv til lagersted* er lagertransaktioner for indkøbsordrer kædet sammen med lagerstedsordrer og låst, så de ikke opdateres af hubben. Hvis du ved en fejl har frigivet til lagerstedet, eller hvis du har en anden grund til at tilbageføre oprettelsen af ordrelinjer for lagerstedet, kan du anmode om at annullere lagerstedsordrelinjer.

Følg disse trin for at annullere en lagerstedsordrelinjer.

1. Log på den forekomst af Supply Chain Management, der kører på hubben.
1. Gå til **Lokationsstyring \> Forespørgsler og rapporter \> Ordrelinjer for lagersted**.
1. Vælg den relevante linje.
1. Vælg **Annuller lagerstedsordrelinjer** i handlingsruden.

> [!NOTE]
> Anmodningen om at annullere linjer afvises for linjer, der allerede afventer annullering, eller som behandles på et lagersted, hvor arbejdsbyrden køres i en skalaenhed.

## <a name="monitor-a-warehouse-order"></a>Overvåge en lagerstedsordre

I visningen **Lagerstedsordrelinjer** kan du overvåge status for indgående modtagelse ved at gennemse værdierne i kolonnen **Resterende antal til modtagelse**. Hvis du vil have vist detaljer, der er relateret til arbejde, der udføres ved hjælp af mobilappen Lokationsstyring, skal du følge et af disse trin.

- Gå til **Lokationsstyring \> Forespørgsler og rapporter \> Ordrelinjer for lagersted**, og brug filteret til at finde det, du leder efter.
- Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**, og åbn den relevante indkøbsordre. Vælg en eller flere linjer i sektionen **Indkøbsordrelinjer**, og vælg derefter **Lagersted \> Lagerstedstilgangsposter**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
