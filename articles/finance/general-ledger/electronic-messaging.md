---
title: Elektroniske meddelelser
description: Dette emne indeholder en oversigt og oplysninger om opsætning for elektroniske meddelelser i Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 191abc37b7c349aaf3c9e871fe2f1885eec9fc896271d6fac27e5caa0b0fe3b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768333"
---
# <a name="electronic-messaging"></a>Elektroniske meddelelser

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt og oplysninger om opsætning for **elektroniske meddelelser** (EM).

Offentlige myndigheder og lovgivende forsamlinger i forskellige lande og områder i hele verden har for nylig implementeret krav til rapportering for virksomheder, der er registreret i disse lande eller områder. Formålet med kravene er at gøre det muligt at få data fra disse virksomheder i elektronisk format direkte fra de systemer, hvor de er blevet bogført, gemt og behandlet.

EM-funktionen i Microsoft Dynamics 365 Finance understøtter forskellige elektroniske kommunikationsprocesser mellem Finance og de systemer, som offentlige myndigheder tilbyder til rapportering, afsendelse og modtagelse af officielle oplysninger.

EM-funktionen er integreret i modulet **Elektronisk rapportering** (ER). Du kan konfigurere ER-formater til elektroniske meddelelser. Du kan finde flere oplysninger under [Elektronisk rapportering (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>Grundlæggende koncepter for EM-funktionalitet

EM-funktionaliteten er baseret på følgende enheder:

- **Elektronisk meddelelse** – En rapport eller opgørelse, der skal rapporteres eller sendes internt, f.eks. en rapport, der sendes til skattemyndighederne.
- **Elektroniske meddelelseselementer** – Poster, der skal medtages i den meddelelse, der rapporteres.
- **Behandling af elektroniske meddelelser** – En kæde af handlinger, der skal køres for at indsamle de nødvendige data, generere rapporter, gemme data i Azure Blob-lageret, sende rapporter uden for systemet, modtage svar, der ikke kommer fra systemet, og opdatere databasen på grundlag af de modtagne oplysninger. Handlingerne i kæden kan enten være forbundne eller ikke-forbundne.

Følgende illustration viser EM-dataflowet.

![Dataflow for elektroniske meddelelser.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>Scenarier, der understøttes af EM-funktionaliteten

EM-funktionaliteten understøtter følgende scenarier:

- Manuel oprettelse af meddelelser og generering af rapporter, der er baseret på tilknyttede ER-formater til eksport af forskellige typer. Disse typer omfatter Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst og Microsoft Word.
- Automatisk oprettelse og behandling af meddelelser, som er baseret på oplysninger, der blev anmodet om og modtaget fra en myndighed via et tilknyttet ER-format til import.
- Indsamling og behandling af oplysninger fra en datakilde som meddelelseselementer. Datakilden er en Finance-tabel.
- Lagring af flere oplysninger og evaluering af forskellige værdier ved at kalde specifikt definerede eksekverbare klasser i forhold til meddelelser eller meddelelseselementer.
- Aggregering af oplysninger, der er indsamlet i meddelelseselementer, opdeling af disse oplysninger efter meddelelse og generering af rapporter, der er i tilknyttede ER-eksportformater.
- Afsendelse af rapporter, som er genereret til en webtjeneste ved hjælp af sikkerhedsoplysninger, der er gemt i Azure Key Vault.
- Modtagelse af svar fra en webtjeneste, fortolkning af svaret og opdatering af data i Finance efter behov.
- Lagring og gennemgang de rapporter, der genereres.
- Lagring og gennemgang af alle logoplysninger, der er knyttet til handlinger, der køres for en meddelelse eller et meddelelseselement.
- Styring af behandlingen via forskellige meddelelsesstatusser og meddelelseselementstatusser.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Landespecifikke lovmæssige funktioner, der understøttes af EM-funktionaliteten

Følgende tabel indeholder oplysninger om nogle landespecifikke lovmæssige funktioner, der understøttes af EM-funktionaliteten.

| Land/område     | Funktionsnavn | Demoregistrering af funktioner |
|-------------|--------------|------------------------|
| Spanien       | [Direkte levering af momsoplysninger (Sumoistro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungarn     | [Onlinefaktureringssystem](../localizations/emea-hun-online-invoicing.md) | |
| Storbritannien | [Momsdigitalisering (MTD) - Indsendelse af momsangivelse](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: UK Digital moms – momsopgørelse i Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litauen   | [i.SAF-rapportering](../localizations/emea-ltu-isaf.md) | |
| Polen      | [Momsopgørelse med registre (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK Vat Audit Registers](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nederlandene | [Momsangivelse (Nederlandene)](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tjekkiet | [Momsopgørelse](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasilien      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rusland      | [Momsopgørelse](../localizations/rus-vat-declaration.md) | |
| Rusland      | [Regnskabsrapportering i elektronisk format](../localizations/rus-accounting-reporting.md) | |
| Rusland      | [Overskudsmomsopgørelse](../localizations/rus-profit-tax-declaration.md) | |
| Rusland      | [Opgjort momsopgørelse](../localizations/rus-assessed-tax-declaration.md) | |
| Rusland      | [Angivelse af transportmoms](../localizations/rus-transport-tax-declaration.md) | |
| Rusland      | [Grundskyldsopgørelse](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

