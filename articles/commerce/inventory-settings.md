---
title: Anvendelse af lagerindstillinger
description: Dette emne dækker lagerindstillinger og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfa8b2bdc03e3698feda26932db757421097140d
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517058"
---
# <a name="apply-inventory-settings"></a>Anvendelse af lagerindstillinger

[!include [banner](includes/banner.md)]

Dette emne dækker lagerindstillinger og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Lagerindstillinger angiver, om lageret skal kontrolleres, før produkterne føjes til indkøbsvognen. De definerer også lagerrelaterede marketingsmeddelelser, f.eks. "på lager" og "kun et par tilbage". Disse indstillinger sikrer, at et produkt ikke kan købes, hvis det ikke er på lager.

Dynamics 365 Commerce giver skøn over den disponible tilgængelighed for produkter. Du kan finde oplysninger om, hvordan det forkalkulerede disponible antal beregnes, i afsnittet [Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md).

I Commerce Site Builder kan der defineres lagergrænseværdier og -intervaller for et produkt eller en kategori. De bestemmer, om lagerbeholdningen kan klassificeres som på lager, lav lagerbeholdning eller udsolgt. Yderligere oplysninger finder du under [Konfigurere lagerbuffere og lagerniveauer](inventory-buffers-levels.md).

> [!NOTE]
> Understøttelse af lagergrænseværdier og -områder er tilgængelige i Dynamics 365 Commerce version 10.0.12.

## <a name="inventory-settings"></a>Lagerindstillinger

I Commerce er lagerindstillingerne defineret i **Indstillinger for websted \> Udvidelser \> Lagerstyring** i webstedsgeneratoren. Der er fire lagerindstillinger, hvoraf en er forældet (frarådes):

- **Aktivér kontrol af lagerbeholdning i app** – Denne indstilling slår kontrol af et produktlager til. Modulerne købefelt, indkøbsvogn og afhentning i butik kontrollerer derefter produktlageret og tillader kun, at der føjes et produkt til indkøbsvognen, hvis lageret er tilgængeligt.
- **Lagerniveau baseret på** – Denne indstilling definerer, hvordan lagerniveauer beregnes. De tilgængelige værdier er **I alt disponibelt**, **Fysisk disponibelt** og **Grænse for udsolgt**. I Commerce kan der defineres lagergrænseværdier og -intervaller for de enkelte produkter eller kategorier. Lager-API'erne returnerer produktlageroplysninger for både egenskaben **I alt disponibelt** og egenskaben **Fysisk disponibelt**. Forhandleren bestemmer, om værdien for **I alt disponibelt** eller **Fysisk disponibelt** skal bruges til at bestemme lageroptællingen og de tilsvarende intervaller for statusserne på lager og udsolgt.

    Værdien **Grænse for udsolgt** for indstillingen **Lagerniveau baseret på** er en gammel (ældre), forældet værdi. Når den er valgt, bestemmes lageroptællingen ud fra resultaterne af værdien **Disponibelt i alt**, men grænsen defineres af den numeriske indstilling **Grænse for udsolgt**, der beskrives senere. Tærskelindstillingen gælder for alle produkter på tværs af et e-handelswebsted. Hvis lagerbeholdningen ligger under tærskelantallet, anses et produkt for at være udsolgt. Ellers betragtes det som værende på lager. Mulighederne for værdien **Grænse for udsolgt** er begrænsede, og det anbefales ikke, at du bruger værdien i version 10.0.12 og senere.

- **Lagerintervaller** – Denne indstilling definerer de lagerintervaller, som der vises meddelelser for i webstedsmoduler. Den kan kun anvendes, hvis enten værdien **I alt disponibelt** eller værdien **Fysisk disponibelt** er valgt for indstillingen **Lagerniveau baseret på**. De tilgængelige værdier er **Alle**, **Lav lagerbeholdning og udsolgt** og **Udsolgt**.

    - Når du vælger **Alle**, vises meddelelser for alle lagerintervaller, fra på lager (meddelelsen "Tilgængelig") til udsolgt (meddelelsen "Udsolgt").
    - Når du vælger **Lav lagerbeholdning og udsolgt**, vises meddelelser for alle lagerintervaller med undtagelse af på lager (meddelelsen "Tilgængelig").
    - Når du vælger **Udsolgt**, vises kun meddelelsen "Udsolgt".

- **Grænse for udsolgt** – Denne gamle numeriske indstilling træder kun i kraft, hvis du vælger værdien **Grænse for udsolgt** for indstillingen **Lagerniveau baseret på**.

> [!IMPORTANT] 
> Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.12. Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt. Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Moduler, der bruger lagerindstillinger

Modulerne købefelt, ønskeliste, butiksvælger, indkøbsvogn og indkøbsvognikon bruger lagerindstillinger til at vise lagerintervaller og -meddelelser.

Følgende billede viser et eksempel på en side med produktdetaljer (PDP), der viser en på lager-meddelelse ("Tilgængelig").

![Eksempel på et PDP-modul, der har en på lager-meddelelse](./media/pdp-InStock.png)

Følgende billede viser et eksempel på en side med produktdetaljer (PDP), der viser en udsolgt-meddelelse ("Udsolgt").

![Eksempel på et PDP-modul, der har en udsolgt-meddelelse](./media/pdp-outofstock.png)

Følgende billede viser et eksempel på en indkøbsvogn, der viser en på lager-meddelelse ("Tilgængelig").

![Eksempel på en indkøbsvognmodul, der har en på lager-meddelelse](./media/cart-instock.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Konfigurere lagerbuffere og lagerniveauer](inventory-buffers-levels.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Boksmodul til køb](add-buy-box.md)

[Kontostyringssider og -moduler](account-management.md)

[Butiksvælgermodul](store-selector.md)

[Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)
