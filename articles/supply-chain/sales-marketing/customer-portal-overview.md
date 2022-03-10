---
title: Kundeportal til Dynamics 365 Supply Chain Management-oversigt (indeholder video)
description: Dette emne introducerer kundeportalen og forklarer, hvem der skal bruge den, og hvordan den fungerer.
author: Henrikan
ms.date: 06/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 50bdbe6c5f5d23f49bdf8040f2c7811a28da3f32
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062003"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Kundeportal til Dynamics 365 Supply Chain Management-oversigt

[!include [banner](../includes/banner.md)]


## <a name="what-is-the-customer-portal"></a>Hvad er kundeportalen?

Moderne forsyningskædesystemer er baseret på integration. De kræver, at lager, kundebehov og salgsafdelinger integreres i stedet for at være placeret i separate siloer. Kundeportalen hjælper organisationer, der kører Microsoft Dynamics 365 Supply Chain Management, med at forbedre denne integration og mere effektivt holde deres kunder informeret.

Kundeportalen er en [Power Apps-portaler](/powerapps/maker/portals/overview) skabelon, der giver virksomheder mulighed for at oprette et udadvendt business-to-business-websted (B2B) til scenarier, der er relateret til salgsordrebehandling. Skabelonen bruger [dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md), Supply Chain Management og Power Apps-portaler til at give eksterne virksomhedskunder mulighed for at få vist og oprette data fra firmaets Dynamics 365-miljø.

Kundeportalskabelonen har alle de tilpasningsmuligheder, som Power Apps-portalfunktionen tilbyder. Skabelonen kan nemt ændres, så den repræsenterer firmaets varemærke. Den tilføjer desuden øget funktionalitet og ændrer brugeroplevelsen. Alle de funktioner, der findes i skabelonen fra starten, kan ændres efter behov.

> [!IMPORTANT]
> Skabelonen forventes ikke at være fuldt funktionel. Den giver blot kunder, der ønsker at oprette et udadvendt websted, mulighed for, at virksomhedskunder kan bruge data fra Supply Chain Management.

> [!NOTE]
> Dokumentationen for kundeportalen henvender sig til administratorer, programmører og systemintegratorer, der skal konfigurere kundeportalen til en Supply Chain Management-installation. Den bruger termer som _kunde_ og _bruger_ til at beskrive personer, som er kunder hos den organisation, der kører Supply Chain Management, og som selv skal bruge den endelige portal.

## <a name="video"></a>Video

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

Videoen [Oversigt over kundeportalskabelonen i Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) (vist ovenfor) er inkluderet i den [Finans- og driftsafspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

## <a name="who-should-use-it"></a>Hvem skal bruge den?

Kundeportalen er designet til virksomheder, der kører Supply Chain Management, og som har følgende karakteristika:

- De vil opbygge et udadvendt websted, som kommunikerer oplysninger om ordrebehandling (f.eks. ordrestatus eller kontooplysninger) direkte fra deres Supply Chain Management til erhvervskunder.
- De er ved at skifte fra Dynamics AX 2012 til Supply Chain Management og brugte tidligere [AX 2012 Customer Self Service-portalen](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Følgende organisationstyper er **ikke** velegnede kandidater til implementering af kundeportalen:

- Virksomheder, der vil opbygge et websted til kunder, der ikke er virksomhedskunder. Disse virksomheder skal overveje at oprette et [Dynamics 365 Commerce-e-handelswebsted](../../commerce/create-ecommerce-site.md).
- Virksomheder, der allerede bruger et eksisterende websted for Power Apps-portaler til et lignende formål. Disse virksomheder får ikke flere fordele ved at bruge kundeportalen. Kundeportalen leveres som en skabelon, der fungerer som en guide og et udgangspunkt for kunder, der vil "forbinde punkterne" mellem dobbeltskrivning, Supply Chain Management og Power Apps-portaler. Hvis du allerede har konfigureret et websted, der tjener dette formål, får du måske ikke den samme gavn af brugen af kundeportalskabelonen til fornyet klargøring af det pågældende websted.

## <a name="how-does-it-work"></a>Hvordan fungerer det?

Kundeportalen leveres som en skabelon til Power Apps-portaler. Den er afhængig af Power Apps-portaler og dobbeltskrivning.

[Power Apps-portaler](/powerapps/maker/portals/overview) er en funktion, der giver brugerne mulighed for at oprette et udadvendt websted, som personer uden for organisationen kan logge på. Der kræves ingen kodning for at lave portaler. Kundeportalen er en af de mange [Dynamics 365-portalskabeloner](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365), der er tilgængelige hos Microsoft.

[Dobbeltskrivning](/powerapps/maker/portals/overview) er et indbygget infrastrukturprodukt, der giver næsten realtidsinteraktion mellem kundeengagementapps og Finans- og driftsapps. Dobbeltskrivning giver en tovejsintegration mellem Finans- og driftsapps og Microsoft Dataverse. Det giver derfor en integreret brugeroplevelse på tværs af appsene. Kundeportalen er afhængig af tabeller, der synkroniseres med dobbeltskrivning. Før data fra Supply Chain Management kan placeres i kundeportalen, skal dobbeltskrivning være aktiveret for alle de relevante tabeller.

![Kundeportalafhængigheder.](media/customer-portal-elements.png "Kundeportalafhængigheder")

Kundeportalen fungerer som udgangspunkt for organisationer, der vil bruge Power Apps-portaler til at opbygge et udadvendt websted, der bruger data fra deres Supply Chain Management-installation. Den hjælper organisationer med at forbinde dobbeltskrivning, Supply Chain Management og Power Apps-portaler.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]