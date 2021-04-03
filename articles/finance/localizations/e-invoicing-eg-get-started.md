---
title: Introduktion til tilføjelsesprogrammet til elektronisk fakturering for Egypten
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Egypten i Finans og Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592592"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Introduktion til tilføjelsesprogrammet til elektronisk fakturering for Egypten

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Egypten. Emnet fører dig gennem de konfigurationstrin, der er landeafhængige i RCS (Regulatory Configuration Services), og supplerer de trin, der er beskrevet i [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Den landespecifikke konfiguration til den egyptiske elektroniske faktura (EG) elektronisk fakturafunktion

Hvis du vil konfigurere funktionen egyptiske elektroniske fakturaer (EG) elektronisk fakturafunktion, skal du udføre nogle trin. Nogle af parametrene fra konfigurationerne er udgivet med standardværdier, så de skal gennemses og opdateres, så de passer bedre til din forretningsoperation.

### <a name="prerequisites"></a>Forudsætninger

Før du kan udføre proceduren i denne sektion, skal du:

- Oprette et digitalt certifikat, som det beskrives under Afsnittet **Opret digitalt certifikat** under [Kom i gang med administration af tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started-service-administration.md). Til testformål leverer de egyptiske skattemyndigheder specifikke test digitale certifikater, som kun skal bruges under test- og løsningsvalideringsfaser. Du kan finde flere oplysninger ved at gå til webstedet for de lokale skattemyndigheder ved hjælp af linket i [egyptisk e-fakturering SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
- Opret en egyptisk elektronisk faktura (EG) Funktionen Elektronisk fakturering i din organisation, som beskrevet i afsnittet **Opret en elektronisk fakturering under din organisationsudbyder** i [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
2. På siden **Funktioner for elektronisk fakturering** skal du kontrollere, at den **Egyptisk elektronisk faktura (EG)** elektroniske fakturafunktion, I har oprettet, er valgt.
3. Kontroller, at **Kladde**-versionen er valgt under fanen **Versioner**.
4. Vælg funktionsopsætningen **Salgsfaktura** i gitteret på fanen **Opsætninger**.
5. Vælg **Rediger**, og vælg fanen **Handlinger** i feltgruppen **Handlinger**, vælg **Underskriv json-dokument for egyptiske momsmyndigheder**.
6. I feltgruppen **Parametre** skal du vælge parameteren **Certifikatnavn** og vælge navnet på det digitale certifikat, der skal bruges sammen med funktionen Elektronisk fakturering.
7. I feltgruppen **Handlinger** skal du vælge **Integrer med egyptisk ETA-tjeneste**. Gentag dette trin for de to forekomster af denne handling.
8. I feltgruppen **Parametre** skal du vælge **URL-adresse til webtjeneste** og **URL-adresse til tjenesten Logon** og evt. gennemse URL-parametrene. Konsultér de egyptiske momsmyndigheders hjemmeside for at finde Url-adressen til test og produktion ved hjælp af linket i [egyptisk e-fakturering SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Vælg **Gem**, og luk siden.
10. Du kan konfigurere programopsætningen under [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landespecifik konfiguration af programopsætningen til funktionen fås af den egyptiske elektroniske faktura (EG) funktionen Elektronisk fakturering

Konfiguration af programopsætningen til **Egyptisk elektronisk faktura (EG)** funktionen elektroniske faktura kræver at de specifikke trin fuldføres. Du skal udføre disse trin, før du implementerer funktionen Elektronisk fakturering i dit servicemiljø for tilføjelsesprogram til elektronisk fakturering.

### <a name="prerequisites"></a>Forudsætninger

Før du fuldfører proceduren i dette afsnit, skal du oprette og starte en **Egyptisk elektronisk faktura (EG)** funktionen Elektronisk fakturering for at konfigurere ansøgningsopsætningen for **Egyptisk elektronisk faktura (EG)** funktionen Elektronisk fakturering, som beskrevet i afsnittet **Konfigurere opsætning af applikationen** i emnet [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
2. På siden **Funktioner for tilføjelsesprogrammet Elektronisk fakturering** skal du kontrollere, at den **Egyptisk elektronisk faktura (EG)** elektroniske fakturafunktion er valgt.
3. Kontroller, at **Kladde**-versionen er valgt under fanen **Versioner**.
4. På fanen **Opsætninger** skal du vælge **Opsætning af ansøgning** og i feltet **Tilsluttet ansøgning** skal du vælge den ansøgning, du vil installere.
5. Kontroller, at debitorfakturakladden er valgt, i feltet **Tabelnavn**.
6. Vælg **Svartyper**, og vælg derefter **Ny**.
7. Angiv "Svar" i feltet **Svartype**, og indtast "Beskrivelse" i feltet **Beskrivelse**.
8. Vælg **Afventer** i feltet **Indsendelsesstatus**.
9. I feltet **Modeltilknytning** skal du vælge **Modeltilknytning fra svarmeddelelse** med **(Forhåndsversion) Format til import af svarmeddelelse** og derefter vælge **Gem**.
10. Vælg **Ny** og i feltet **Svartype** skal du angive "ResponseData" som fast værdi. Indtast "Beskrivelse" i feltet **Beskrivelse**.
11. Vælg **Afventer** i feltet **Indsendelsesstatus**.
12. Vælg **Salgsfakturahoveder V2** i feltet **Navn på dataenhed**.
13. I feltet **Modeltilknytning** skal du vælge **Egyptisk import af svardata** med **(Forhåndsversion) Egyptisk import af svardata** og derefter vælge **Gem**.
14. Hvis du vil implementere funktionen Elektronisk fakturering, skal du se [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Aktivering af funktionen **Egyptisk elektronisk faktura (EG)** kan kræve, at der sendes begrænsede data, herunder organisationens momsregistrerings-id. Disse data vil blive overført til tredjepartsorganer, der er godkendt af skattemyndighederne, med det formål at sende elektroniske fakturaer til denne skattemyndighed i det foruddefinerede format, der kræves til integration med myndighedernes webtjeneste. En administrator kan aktivere og deaktivere funktionen ved at gå til **Organisationsadministration** > **Konfiguration** > **Parametre for elektroniske dokumenter**. Under fanen **Funktioner** skal du markere den række, der indeholder funktionen **Egyptisk elektronisk faktura (EG)** og derefter foretage de relevante valg. De data, der importeres fra disse eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132). Yderligere oplysninger finder du i sektionerne med Erklæring om beskyttelse af personlige oplysninger i dokumentationen for den lande- eller områdespecifikke funktion.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Tilføjelsesprogrammet til oversigt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Introduktion til tilføjelsesprogrammet til serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Introduktion til tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md)
- [Elektroniske fakturaer til kunder i Egypten](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
