---
title: Konfigurere elektronisk fakturering
description: Denne artikel indeholder en oversigt over processen til opsætning og konfigurering af elektronisk fakturering.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272173"
---
# <a name="electronic-invoicing-setup"></a>Konfigurere elektronisk fakturering

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over processen til opsætning og konfigurering af elektronisk fakturering. Du skal udføre opsætningstrinnene i den rækkefølge, der er angivet her. Hvis et trin er obligatorisk, men du springer det over, vil funktionen ikke virke korrekt, og der vil forekomme flere fejl i de efterfølgende trin, eller når du bruger funktionen. 

Før du går i gang, skal du sikre dig, at alle hovedkomponenter er konfigureret korrekt, at du har tilmeldt dig RCS (Regulatory Configuration Service) og har en forekomst af RCS, og at tilføjelsesprogrammet Elektronisk fakturering er installeret for dit Microsoft Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management-miljø. Du kan finde flere oplysninger i [Tilmelde og installere elektronisk fakturering](e-invoicing-install-add-in-microservices-lcs.md).

Konfigurer derefter de Azure-ressourcer, som elektronisk fakturering kræver for at kunne fungere. Du kan finde flere oplysninger i [Konfigurere Azure-ressourcer til elektronisk fakturering](e-invoicing-set-up-azure-resources.md).

Når hovedkomponenterne er konfigureret, skal du arbejde sammen med RCS om at konfigurere de vigtigste logiske komponenter i elektronisk fakturering. Definer først antallet af servicemiljøer, du vil vedligeholde. På denne måde kan du definere den logiske data- og konfigurationspartitionering for at sikre, at du har en grænse mellem et udviklings- eller testmiljø og produktionsmiljøerne. Hvis udviklingsprocessen skal konfigureres på en fleksibel måde, kan der være brug for flere forskellige udviklings- og testmiljøer. Udover at definere servicemiljøer skal du angive et link til virksomhedsprogrammer, f.eks. Finans eller Supply Chain Management, direkte fra RCS for at konfigurere de parametre, der kræves for at kunne bruge elektronisk fakturering korrekt. Du kan finde flere oplysninger om miljøer under [Tjenestemiljøer](e-invoicing-service-environments.md).

Når alt er konfigureret, kan du oprette dine egne globaliseringsfunktioner, der definerer forskellige scenarier for behandling af elektroniske dokumenter og transformering af data eller for import af dokumenterne fra det globale lager. Du kan finde flere oplysninger om, hvordan du arbejder med globaliseringsfunktioner, i [Arbejde med globaliseringsfunktioner](e-invoicing-working-globalization-features.md).

Hvis dine scenarier kræver integration med e-mail eller SharePoint for at behandle indgående elektroniske dokumenter, skal du se [Behandling af indgående elektroniske dokumenter](e-invoicing-process-incoming-electronic-documents.md) for at få oplysninger om, hvordan du opretter og bruger disse kanaler.
