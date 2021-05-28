---
title: Anvendelse af lagerindstillinger
description: Dette emne dækker lagerindstillinger og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ae0195f63b123a345b0cdcd4976bfd25b3b3d6d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019072"
---
# <a name="apply-inventory-settings"></a>Anvend lagerindstillinger

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne dækker lagerindstillinger og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.

Lagerindstillinger angiver, om lageret skal kontrolleres, før produkterne føjes til indkøbsvognen. De definerer også lagerrelaterede marketingsmeddelelser, f.eks. "på lager" og "kun et par tilbage". Disse indstillinger sikrer, at et produkt ikke kan købes, hvis det ikke er på lager.

Dynamics 365 Commerce giver skøn over den disponible tilgængelighed for produkter. Du kan finde oplysninger om, hvordan det forkalkulerede disponible antal beregnes, i afsnittet [Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md).

I Commerce Site Builder kan der defineres lagergrænseværdier og -intervaller for et produkt eller en kategori. De bestemmer, om lagerbeholdningen kan klassificeres som på lager, lav lagerbeholdning eller udsolgt. Yderligere oplysninger finder du under [Konfigurere lagerbuffere og lagerniveauer](inventory-buffers-levels.md).

> [!NOTE]
> Understøttelse af lagergrænseværdier og -områder er tilgængelige i Dynamics 365 Commerce version 10.0.12.

## <a name="inventory-settings"></a>Lagerindstillinger

I Commerce er lagerindstillingerne defineret i **Indstillinger for websted \> Udvidelser \> Lagerstyring** i webstedsgeneratoren. Der er fem lagerindstillinger, hvoraf en er forældet (frarådet):

- **Aktivér kontrol af lagerbeholdning i app** – Denne indstilling slår kontrol af et produktlager til. Modulerne købefelt, indkøbsvogn og afhentning i butik kontrollerer derefter produktlageret og tillader kun, at der føjes et produkt til indkøbsvognen, hvis lageret er tilgængeligt.
- **Lagerniveau baseret på** – Denne indstilling definerer, hvordan lagerniveauer beregnes. De tilgængelige værdier er **I alt disponibelt**, **Fysisk disponibelt** og **Grænse for udsolgt**. I Commerce kan der defineres lagergrænseværdier og -intervaller for de enkelte produkter eller kategorier. Lager-API'erne returnerer produktlageroplysninger for både egenskaben **I alt disponibelt** og egenskaben **Fysisk disponibelt**. Forhandleren bestemmer, om værdien for **I alt disponibelt** eller **Fysisk disponibelt** skal bruges til at bestemme lageroptællingen og de tilsvarende intervaller for statusserne på lager og udsolgt.

    Værdien **Grænse for udsolgt** for indstillingen **Lagerniveau baseret på** er en gammel (ældre), forældet værdi. Når den er valgt, bestemmes lageroptællingen ud fra resultaterne af værdien **Disponibelt i alt**, men grænsen defineres af den numeriske indstilling **Grænse for udsolgt**, der beskrives senere. Tærskelindstillingen gælder for alle produkter på tværs af et e-handelswebsted. Hvis lagerbeholdningen ligger under tærskelantallet, anses et produkt for at være udsolgt. Ellers betragtes det som værende på lager. Mulighederne for værdien **Grænse for udsolgt** er begrænsede, og det anbefales ikke, at du bruger værdien i version 10.0.12 og senere.

- **Lagerniveau for flere lagersteder** – Med denne indstilling kan lagerniveauet beregnes i forhold til standardlagerstedet eller flere lagersteder. Indstillingen **Baseret på individuelt lagersted** beregner lagerniveauerne ud fra standardlagerstedet. En e-handelslokation kan også pege på flere lagersteder for at lette opfyldningen. I dette tilfælde bruges indstillingen **Baseret på samling af lagersteder for forsendelse og afhentning** til at angive lagertilgængelighed. Når en kunde f.eks. køber en vare og vælger "forsendelse" som leveringsmåde, kan varen afsendes fra ethvert lagersted i den opfyldningsgruppe, der har en tilgængelig lagerbeholdning. Siden Produktdetaljer (PDP) viser en meddelelse "På lager" for forsendelse, hvis et tilgængeligt lagersted for forsendelse i opfyldningsgruppen har lager. 

> [!IMPORTANT] 
> Indstillingen **Lagerniveau for flere lagersteder** er tilgængelig fra frigivelsen af Commerce version 10.0.19. Hvis du opdaterer fra en ældre version af Commerce, skal du opdatere filen appsettings.json manuelt. Du kan finde instruktioner i [Opdateringer af SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Lagerintervaller** – Denne indstilling definerer de lagerintervaller, som der vises meddelelser for i webstedsmoduler. Den kan kun anvendes, hvis enten værdien **I alt disponibelt** eller værdien **Fysisk disponibelt** er valgt for indstillingen **Lagerniveau baseret på**. De tilgængelige værdier er **Alle**, **Lav lagerbeholdning og udsolgt** og **Udsolgt**.

    - Når du vælger **Alle**, vises meddelelser for alle lagerintervaller, fra på lager (meddelelsen "Tilgængelig") til udsolgt (meddelelsen "Udsolgt").
    - Når du vælger **Lav lagerbeholdning og udsolgt**, vises meddelelser for alle lagerintervaller med undtagelse af på lager (meddelelsen "Tilgængelig").
    - Når du vælger **Udsolgt**, vises kun meddelelsen "Udsolgt".

- **Grænse for udsolgt** – Denne gamle numeriske indstilling træder kun i kraft, hvis du vælger værdien **Grænse for udsolgt** for indstillingen **Lagerniveau baseret på**.

> [!IMPORTANT] 
> Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.12. Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt. Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Moduler, der bruger lagerindstillinger

Modulerne købefelt, ønskeliste, butiksvælger, indkøbsvogn og indkøbsvognikon bruger lagerindstillinger til at vise lagerintervaller og -meddelelser.

I eksemplet i følgende illustration viser en PDP en meddelelse for På lager ("Tilgængelig").

![Eksempel på et PDP-modul, der har en på lager-meddelelse](./media/pdp-InStock.png)

I eksemplet i følgende illustration viser en PDP en meddelelse for "Udsolgt".

![Eksempel på et PDP-modul, der har en udsolgt-meddelelse](./media/pdp-outofstock.png)

I eksemplet i følgende illustration viser en indkøbsvogn en meddelelse for På lager ("Tilgængelig").

![Eksempel på en indkøbsvognmodul, der har en på lager-meddelelse](./media/cart-instock.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Konfigurere lagerbuffere og lagerniveauer](inventory-buffers-levels.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Boksmodul til køb](add-buy-box.md)

[Kontostyringssider og -moduler](account-management.md)

[Butiksvælgermodul](store-selector.md)

[Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
