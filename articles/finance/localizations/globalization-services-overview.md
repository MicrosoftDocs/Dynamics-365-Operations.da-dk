---
title: Dynamics 365-globaliseringstjenester
description: Dette emne giver en oversigt over Microsoft Dynamics 365-globaliseringstjenester.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8fa82f741471a8314d01972b3ae3393eea4fd6b47bde647bf4ecdaebfea814a3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775064"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365-globaliseringstjenester

[!include [banner](../includes/banner.md)]

Følgende globaliseringstjenester kan konfigureres til at udvide de egenskaber, der findes i nogle Microsoft Dynamics 365-onlinetjenester:

- **RCS (Regulatory Configuration Service)** understøtter konfigurationen af forskellige typer elektroniske dokumenter og rapporter. RCS leverer en udvidet version af ER-designeren (elektronisk rapportering), hvor konfigurationslageret er en enkeltstående tjeneste. Du kan finde flere oplysninger under [Regulatory Configuration Service](rcs-overview.md).
- **Elektronisk fakturering** samler konfigurerbare formater for transformationer, digitale signaturer og konfigurerbare integrationer for forbindelse til eksterne webtjenester, herunder certificering og håndtering af svar. Du kan finde flere oplysninger i [Elektronisk fakturering](e-invoicing-service-overview.md).
- **Momsberegning** giver større fleksibilitet ved at understøtte flere moms-id'er, bestemmelse af momskode, designeren til momsberegning og et kørselsprogram for at overholde komplekse momsregler på globalt plan. Du kan finde flere oplysninger under [Momsberegning](global-tax-calcuation-service-overview.md).

Disse globaliseringstjenester leverer standardintegration med følgende Dynamics 365-onlinetjenester.

| Onlinetjeneste | RCS | Elektronisk fakturering | Momsberegning (prøveversion) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Ja | Ja | Ja | 
| Dynamics 365 Supply Chain Management | Ja | Ja | Ja | 
| Dynamics 365 Project Operations | Ja | Ja | Ikke anvendelig | 
| Dynamics 365 Commerce | Ja | Ikke anvendelig | Ikke anvendelig | 

> [!NOTE]
> På grund af forskelle i tilgængeligheden af Azure-geografiske steder (geolokationer) for RCS kan konfiguration af denne tjeneste bevirke, at der overføres kundedata uden for det geografiske område, der er valgt for den relevante Dynamics 365-onlinetjeneste. Du kan finde flere oplysninger i [Dynamics 365 og Power Platform : Tilgængelighed, dataplacering, sprog og lokalisering](https://aka.ms/rcs/D365Productavailabilityguide).