---
title: Elektroniske meddelelser
description: Denne artikel indeholder en oversigt og oplysninger om opsætning for elektroniske meddelelser i Microsoft Dynamics 365 Finance.
author: AdamTrukawka
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3e2fe6a70d449adea07f5aa0db9e625f0378d8c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283448"
---
# <a name="electronic-messaging"></a>Elektroniske meddelelser

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt og oplysninger om opsætning for **elektroniske meddelelser** (EM).

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

## <a name="security-privileges"></a>Sikkerhedsrettigheder

Følgende sikkerhedsrettigheder er tilgængelige for elektroniske meddelelser.

| Sikkerhedsrettighed           | Adgangsniveau | Tilknytning |
|------------------------------|--------------|-------------|
| Vedligehold elektroniske meddelelser | Denne rettighed giver fuld adgang til EM-funktionaliteten. Hvis du har denne rettighed, kan du konfigurere elektroniske meddelelser og køre al behandling. | Denne rettighed er inkluderet i sikkerhedsafgiften **Vedligehold momstransaktioner**. Denne opgave er til gengæld en del af sikkerhedsrollen **Bogholder**. |
| Vis elektroniske meddelelser     | Denne rettighed giver skrivebeskyttet adgang til EM-funktionaliteten. Hvis du har denne rettighed, kan du se de elektroniske meddelelsesindstillinger og meddelelser. Du kan dog ikke konfigurere eller køre noget. | Denne rettighed er inkluderet i sikkerhedsafgiften **Anmod om status for momstransaktioner**. Denne opgave er til gengæld en del af følgende sikkerhedsroller:<ul><li>Opkrævningschef</li><li>Debitorassistent</li><li>Debitorchef</li><li>Momsbogholder</li><li>Bogholder</li><li>Regnskabschef</li><li>Regnskabsansvarlig</li><li>Salgsdirektør</li><li>Kreditorassistent</li></ul> |
| Udfør handling på elektroniske meddelelser  | Denne rettighed giver kun adgang til siderne **Elektroniske meddelelser** og **Elektronisk meddelelseselementer**. Hvis du har denne rettighed, kan du køre alle de behandlinger, der kaldes fra disse sider. | Denne rettighed er inkluderet i sikkerhedsafgiften **Udfør elektroniske meddelelser**. Denne opgave er til gengæld en del af sikkerhedsrollen **Elektronisk meddelelsesoperatør**. |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Landespecifikke lovmæssige funktioner, der understøttes af EM-funktionaliteten

Følgende tabel indeholder oplysninger om nogle landespecifikke lovmæssige funktioner, der understøttes af EM-funktionaliteten.

| Land/område     | Funktionsnavn | Demoregistrering af funktioner |
|-------------|--------------|------------------------|
| Spanien       | [Direkte levering af momsoplysninger (Sumoistro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungarn     | [Onlinefaktureringssystem](../localizations/emea-hun-online-invoicing.md) | |
| Storbritannien | [Momsdigitalisering (MTD) - Indsendelse af momsangivelse](../localizations/emea-gbr-mtd-vat-integration.md) | [Finans og drift: Digital moms i Storbritannien - Momsopgørelse i Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litauen   | [i.SAF-rapportering](../localizations/emea-ltu-isaf.md) | |
| Polen      | [Momsopgørelse med registre (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK Momsafregningsregistre](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nederlandene | [Momsangivelse (Nederlandene)](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tjekkiet | [Momsopgørelse](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasilien      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rusland      | [Momsopgørelse](../localizations/rus-vat-declaration.md) | |
| Rusland      | [Regnskabsrapportering i elektronisk format](../localizations/rus-accounting-reporting.md) | |
| Rusland      | [Overskudsmomsopgørelse](../localizations/rus-profit-tax-declaration.md) | |
| Rusland      | [Opgjort momsopgørelse](../localizations/rus-assessed-tax-declaration.md) | |
| Rusland      | [Angivelse af transportmoms](../localizations/rus-transport-tax-declaration.md) | |
| Rusland      | [Grundskyldsopgørelse](../localizations/rus-land-tax-declaration.md) | |
| Norge      | [Momsopgørelse med direkte indsendelse til Altinn](../localizations/emea-nor-vat-return.md) | [Ny momsopgørelse med direkte overførsel til Altinn i Dynamics 365 Finance](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| Frankrig      | [Momsopgørelse (Frankrig)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| Østrig     | [Momsopgørelse (Østrig)](../localizations/emea-aut-vat-declaration-austria.md) | |
| Tyskland     | [Momsangivelse (Tyskland)](../localizations/emea-deu-vat-declaration-germany.md) | |
| Nederlandene | [Momsangivelse (Nederlandene)](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Sverige      | [Momsopgørelse (Sverige)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| Schweiz | [Momsopgørelse (Schweiz)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


