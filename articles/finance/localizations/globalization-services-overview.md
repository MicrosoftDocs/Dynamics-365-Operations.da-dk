---
title: Dynamics 365-globaliseringstjenester
description: Denne artikel giver en oversigt over Microsoft Dynamics 365-globaliseringstjenester.
author: kfend
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
ms.openlocfilehash: eebf74ab30a544f6561cf5782148d12b58d9c4b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278226"
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
| Dynamics 365 Project Operations | Ja | Ja | Ikke relevant | 
| Dynamics 365 Commerce | Ja | Ikke relevant | Ikke anvendelig | 

> [!NOTE]
> På grund af forskelle i tilgængeligheden af Azure-geografiske steder (geolokationer) for RCS kan konfiguration af denne tjeneste bevirke, at der overføres kundedata uden for det geografiske område, der er valgt for den relevante Dynamics 365-onlinetjeneste. Du kan finde flere oplysninger i [Dynamics 365 og Power Platform : Tilgængelighed, dataplacering, sprog og lokalisering](https://aka.ms/rcs/D365Productavailabilityguide).
