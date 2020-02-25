---
title: Ofte stillede spørgsmål om Dynamics 365 Commerce-prøveversionsmiljø
description: Dette emne indeholder svar på ofte stillede spørgsmål om miljøet til prøveversionen af Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 061a160380e500ea52afbc35f0a95fe84d971bcf
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024746"
---
# <a name="dynamics-365-commerce-preview-environment-faq"></a>Ofte stillede spørgsmål om Dynamics 365 Commerce-prøveversionsmiljø

[!include [banner](includes/banner.md)]

Dette emne indeholder svar på ofte stillede spørgsmål om miljøet til prøveversionen af Microsoft Dynamics 365 Commerce.

**Kan jeg overføre min invitation til miljøet til prøveversionen af Commerce til en anden lejer?**

Ja. I forbindelse med invitationsoverførsler kan du bruge [overførselsformularen Commerce-prøveversion](https://aka.ms/Dynamics365CommercePreviewTransferForm)

**Hvor lang tid tager invitationsoverførslen?**

Overførslen tager i gennemsnit ca. tre til fem hverdage. Der kan dog være visse undtagelser.

**Fungerer miljøet til prøveversionen af Commerce sammen med Dynamics 365 Finance eller Dynamics 365 Supply Chain-projekter?**

Nr. Miljøet til prøveversionen af Commerce fungerer kun sammen Dynamics 365 Retail-projekter.

**Kan vi bruge miljøet til prøveversionen af Commerce som en e-handel-butiksfacade for kunder, der i øjeblikket implementerer Retail?**

Nr. Miljøet til prøveversionen af Commerce er kun evalueringsmiljøet. Hvis du har brug for et miljø til en kunde, der implementerer Retail, skal du kontakte Microsoft.

**Kan miljøet til prøveversionen af Commerce bruges til at klargøre e-handel-funktionerne oven på et eksisterende program/miljø, der implementerer Retail?**

Nr. Miljøet til prøveversionen af Commerce er i øjeblikket kun tilgængeligt i nye miljøer, der er installeret på de Retail lagerenhed (SKU), der har demodata fra version 10.0.6.

**Hvilke omkostninger er der forbundet med implementeringen af miljøet til prøveversionen af Commerce på Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**

Retail er den eneste komponent, der hostes i dit abonnement. Andre komponenter såsom Retail Cloud Scale Unit (RCSU) og e-Commerce vil blive hostet i Microsoft-abonnementer. Du kan bruge [Azure prisberegneren](https://azure.microsoft.com/pricing/calculator/) til at anslå denne omkostning.

**Hvilke geografiske Azure-områder understøttes i øjeblikket for miljøet til prøveversionen af Commerce?**

Miljøet til prøveversionen af Commerce kan kun implementeres i det nordamerikanske område.

**Findes der en virtuel harddisk (VHD), der kan downloades, og som har den komplette indstilling for en virtuel maskine med én boks (VM)?**

Dynamics 365 Retail Cloud Scale Unit (RCSU) og e-Commerce er udelukkende Software som en service (SaaS) og skal være hostet i skyen.

**Hvor længe kan miljøet til prøveversionen af Commerce bruges?**

Miljøet til prøveversionen af Commerce har en frist på 30 dage fra datoen for klargøring af e-Commerce.

**Kan jeg forlænge fristen for mit miljø til prøveversionen af Commerce?**

Ja. Du kan kontakte supportteamet ved hjælp af formularen [formular til forlængelse af prøveversionen af Commerce](https://aka.ms/Dynamics365CommercePreviewExtensionForm).

**Kan vi anmode flere gange om et miljø til prøveversionen af Commerce?**

Vi tildeler en kvote på ét miljø til prøveversionen af Commerce for hver anmodning, der accepteres. Hvis du har brug for mere end ét prøveversionsmiljø, skal du kontakte Microsoft. Kontaktoplysninger er angivet i næste afsnit.

## <a name="dynamics-365-commerce-preview-environment-contact-information"></a>Kontaktoplysninger til miljø til prøveversion af Dynamics 365 Commerce

Hvis du har spørgsmål eller anmodninger, der er relateret til miljøet til prøveversionen af Commerce, kan du kontakte Microsoft ved at besøge [Microsoft Dynamics 365 Commerce Prøveversion Yammer-gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) for at få hjælp.

Hvis du oplever problemer, når du forsøger at få adgang til Yammer-gruppen, kan du kontakte Microsoft via e-mail på <Dynamics365Commerce@microsoft.com>. Denne e-mailadresse overvåges ikke aktivt. Du skal derfor regne med, at svaret vil blive forsinket.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce-prøveversionsmiljø](cpe-overview.md)

[Klargøre et Dynamics 365 Commerce-prøveversionsmiljø](provisioning-guide.md)

[Konfigurere et Dynamics 365 Commerce-prøveversionsmiljø](cpe-post-provisioning.md)

[Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-prøveversionsmiljø](cpe-optional-features.md)
