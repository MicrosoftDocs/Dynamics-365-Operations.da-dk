---
title: Oversigt over elektronisk fakturering
description: Denne artikel indeholder en oversigt over elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 4ce5776216855fc664b9beba68036d41920ae602
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861290"
---
# <a name="electronic-invoicing-overview"></a>Oversigt over elektronisk fakturering

[!include [banner](../includes/banner.md)]

Elektronisk fakturering til Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management er en hyperskalerbar tjeneste til flere lejere, der giver mulighed for konfigurerbar behandling af elektroniske fakturaer og konfigurerbar dokumentudveksling. Reglerne for behandling og integration er fuldt konfigurerbare, og logikken køres uden for Finance og Supply Chain Management. Denne tjeneste anvendes primært til behandling af elektroniske fakturadokumenter i virksomhed-til-myndighed-scenarier. Den kan dog konfigureres brugerdefineret til andre formål, f.eks. business-to-business-scenarier for forskellige typer dokumenter.

Elektronisk fakturering kan hjælpe dig med at opnå følgende mål:

- Hurtig og nem implementering af lande-/områdespecifikke krav
- Standardiserede implementeringer af en løsning til elektronisk fakturering
- Forbedret sporing af dokumenthistorik
- Kortere implementeringscyklus
- Reducerede samlede ejeromkostninger (TCO)
- Konfigurationer, der nemt kan justeres uden behov for kodeændringer
- Enklere konfigurationspakke
- Indbygget eksport, import og integration samt nemme udvidelsesmuligheder i behandlingen af elektroniske fakturadokumenter
- Nem genbrug af de samme konfigurationer for eksport, import og integration på tværs af virksomheder

## <a name="service-availability"></a>Tilgængelighed af tjeneste

Funktionen til elektronisk fakturering er i øjeblikket tilgængelig for kunder med Finans og Supply Chain Management. Du kan finde flere oplysninger i vilkår og betingelser for licensaftalen til programmet.

Da funktioner, der adresserer lande/områdespecifikke krav, kan være begrænset i forskellige faser af udgivelsen, skal du altid gennemgå den nyeste dokumentation, der fremhæver dækningen og omfanget af understøttede lande-/områdespecifikke løsninger.

Elektronisk fakturering er udrullet i følgende geografiske Azure-områder:

- USA
- Europa
- Asien

> [!NOTE]
> Elektronisk fakturering understøtter ikke udrulninger i det lokale miljø.

## <a name="feature-highlights"></a>Fremhævning af funktioner

- Køreklar integration med Finans og Supply Chain Management
- Ensartet brugeroplevelse i forbindelse med konfiguration og overvågning af elektronisk fakturaproces for alle lande og områder
- Hurtigere, nemmere og mere økonomisk implementering af løsninger til elektronisk fakturering i nye lande eller områder
- Konfiguration af tjenesten ved hjælp af RCS (Regulatory Configuration Service) og funktionsopsætninger for globalisering
- Transformation af forretningsdata til flere elektroniske fakturaformater (XML, JavaScript Object Notation \[JSON\], TXT og kommaseparerede værdier \[CSV\]) ved hjælp af de konfigurationer, der er defineret i RCS:

    - Elektroniske rapporteringsformater (ER), der er tilgængelige for lande og områder, hvor det ikke er muligt at konfigurere en transformation af elektroniske fakturaer

- Konfigurerbar indsendelse af elektroniske fakturaer til eksterne webtjenester, herunder certificeringshåndtering via digitale signaturer:

    - Indbygget og konfigurerbar integration, der nemt kan udvides, med yderligere indhold til flere lande og områder

- Håndtering af svar fra webtjenester, herunder konfigurerbar håndtering af undtagelsesmeddelelser
- Understøttelse af elektroniske signaturer (f.eks. elektroniske signaturer, der bruger XMLDSig-signeringsalgoritmen)
- Den egenskab, der gør det muligt at sende dokumenter til mails og gemme dem i SharePoint
- Batchbehandling af elektroniske fakturameddelelser
- Konfigurerbar transformation af indgående dokumenter og behandling af disse dokumenter i Finans og Supply Chain Management
- Den egenskab, der gør det muligt at modtage indgående dokumenter fra kanaler som f.eks. e-mail og SharePoint

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Aktivering og brug af elektronisk fakturering kræver måske, at der sendes begrænsede data. Disse data omfatter organisationens momsregistrerings-id. Disse data vil blive overført til tredjepartsorganer, der er godkendt af skattemyndighederne, med det formål at sende elektroniske fakturaer i de foruddefinerede formater, der kræves til integration med myndighedernes webtjenester. Data, der importeres fra disse eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132). Yderligere oplysninger finder du i sektionen "Erklæring om beskyttelse af personlige oplysninger" i dokumentationen til den lande- eller områdespecifikke funktion.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
