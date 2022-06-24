---
title: Ofte stillede spørgsmål om Indkøb
description: Denne artikel indeholder svar på ofte stillede spørgsmål om Supply Chain Management-funktionens indkøbsfunktionalitet
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 6e710b254638b255ce4aa3e0adde0dd23bf60f64
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869569"
---
# <a name="procurement-faq"></a>Ofte stillede spørgsmål om Indkøb

[!include [banner](../includes/banner.md)]

Denne artikel indeholder svar på ofte stillede spørgsmål om Supply Chain Management-funktionens indkøbsfunktionalitet.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kan jeg nøjes med at få vist de indkøbsordrer, jeg har oprettet?

Denne funktionalitet er ikke tilgængelig i øjeblikket.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kan jeg reservere en lagerbeholdning og oprette transaktioner mod registreret lager på en indkøbsordre?

### <a name="issue-description"></a>Problembeskrivelse

Selv når varer er i en *Registreret* tilstand på en indkøbsordre, kan du stadig reservere lageret. Du kan med andre ord oprette transaktioner mod det registrerede lager.

### <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. Oprette en indkøbsordre.
2. Registrér indkøbsordrelinjen.
3. Bemærk, at du kan generere reservationer eller transaktioner mod det registrerede lager.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet. Det forventes, at de registrerede varer er modtaget fysisk på lagerstedet eller lageret, og at de derfor er tilgængelige for reservation.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kan jeg finde den bruger, der har annulleret en indkøbsordre?

Disse oplysninger spores kun, hvis ændringsstyring er aktiveret for indkøbsordren. Hvis du bruger ændringsstyring, kan du se, hvem der har afsendt ændringen (annulleringen), og hvem der har godkendt den.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Hvorfor kan jeg ikke knytte en købsaftale til en eksisterende indkøbsordre?

En købsaftale skal knyttes til en indkøbsordre, når indkøbsordren oprettes. Ellers kan indkøbsordrelinjer ikke knyttes til købsaftalelinjer.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Hvilken kontrol aktiverer meddelelsen "Opdater priser og rabatter, der er angivet manuelt eller med et eksternt dokument"?

Når du ændrer afsendelsesdatoen, kan du få vist en meddelelse, der angiver "Opdater priser og rabatter, der er angivet manuelt eller med et eksternt dokument". Du modtager denne meddelelse, for hvis afsendelsesdatoen ændres, kan en anden samhandels- eller salgsaftale udløses og forårsage en prisændring. En ændring af afsendelsesdatoen kan også påvirke lagertidsplaner og andre relaterede oplysninger.

Meddelelsen udløses, hver gang en af datoerne eller andre parametre ændres. Formålet med meddelelsen er at sikre, at du er opmærksom på prisændringer, der kan forekomme på grund af disse ændringer.

Meddelelsen er anmodningen om evaluering af samhandelsaftalen. En fuldstændig beskrivelse finder du i [Politikker til evaluering af samhandelsaftale](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Hvorfor kan jeg ikke bogføre mere end én faktura på en indkøbsordrelinje, der har kategoribaserede varer?

Et antal skal angives, hvis du vil bogføre fakturaer. Hvis hele antallet på en linje kun er faktureret for et delvist beløb, kan du derfor ikke fakturere restbeløbet på en anden faktura.
