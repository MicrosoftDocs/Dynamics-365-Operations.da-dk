---
title: Tilmelde og installere elektronisk faktureringstjeneste
description: Dette emne indeholder oplysninger om, hvordan du tilmelder og installerer tjenesten Elektronisk fakturering.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ab16652e4a50dd71a5d0b2b49b4dd79e327f7a8
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371554"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Tilmelde og installere elektronisk faktureringstjeneste

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om, hvordan du tilmelder og installerer tjenesten Elektronisk fakturering. Der er fire trin i denne proces. Trin 1 til og med 3 er obligatoriske, og trin 4 er valgfrit.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Trin1: Tilmelde dig Regulatory Configuration Service

Regulatory Configuration Service (RCS) leverer den konfiguration og design, der anvendes til konfigurering af Elektronisk fakturering. Ressourcer som f.eks. miljøer og funktioner til elektronisk fakturering oprettes, vedligeholdes og administreres i RCS. Når ressourcerne er klar, publiceres de til tjenesten Elektronisk fakturering.

Du kan finde flere oplysninger om RCS i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md).

Du kan tilmelde dig RCS fra siden [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Trin 2: Installere tilføjelsesprogrammet til mikrotjenester i Microsoft Dynamics Lifecycle Services

Tjenesten Elektronisk fakturering er et sæt mikrotjenester, der har Microsoft-datacentre som vært. Som standard har kunder med Dynamics 365 Finance og Dynamics 365 Supply Chain Management ikke adgang til den elektroniske faktureringsservice. Du skal installere den som et tilføjelsesprogram i Microsoft Dynamics Lifecycle Services (LCS). Når du installerer tilføjelsesprogrammet, registreres dit Finans- eller Supply Chain Management-miljø i registeret over programmer, der har tilladelse til at oprette forbindelse til tjenesten Elektronisk fakturering.

Se [Installere tilføjelsesprogrammet til mikrotjenester i Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md) for at fuldføre dette trin.

### <a name="step-3-set-up-rcs"></a>Trin 3: Konfigurere RCS

Du skal konfigurere integrationen mellem RCS og tjenesten Elektronisk fakturering. Du skal også konfigurere hovedkomponenterne.

Du kan fuldføre dette trin i [Konfigurere Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Trin 4: Microsoft Power Platform-plug-in-reference til administrator

Nogle scenarier kræver integration med Dataverse i området af Microsoft Power Platform.

I øjeblikket er denne opsætning obligatorisk, hvis du vil bruge elektroniske faktureringsløsninger til indonesiske scenarier med elektronisk fakturering. Det er dog valgfrit i forbindelse med elektroniske faktureringsscenarier til Saudi-Arabien. Du kan finde flere oplysninger i [Tilgængelighed af funktioner til elektronisk fakturering efter land eller område](e-invoicing-country-specific-availability.md).

Se [Microsoft Power Platform-plug-in-administratorreferencen](e-invoicing-power-platform-plug-in.md) for at udføre dette trin.
