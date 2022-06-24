---
title: Overvejelser om optimering af søgeprogram (SEO) for webstedet
description: Denne artikel beskriver SEO-overvejelserne (søgemaskineoptimering) for dit websted fra udvikling til produktion.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 6747df3c56fb05248210f78ebf2176a56ce78329
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896895"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Overvejelser om optimering af søgeprogram (SEO) for webstedet


[!include [banner](includes/banner.md)]

Denne artikel beskriver SEO-overvejelserne (søgemaskineoptimering) for dit websted fra udvikling til produktion.

## <a name="a-site-that-is-under-development"></a>Et websted, der er under udvikling

For at sikre, at søgeprogrammet ikke indekserer et websted under udvikling, skal alle webstedssider have **noindex** og **nofollow** som metakoder. Det er en god ide at oprette et fragmentmodul baseret på [MetaTags-modulet](metatags-module.md), der indeholder følgende metakodepost, og sikre, at fragmentet føjes til HTML-afsnittet \<head\> for alle de skabeloner, der bruges på dit websted.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Blød start af et websted

Under en "blød start" stilles et websted til rådighed for et begrænset publikum eller marked, før hele lanceringen finder sted. Hvis du udfører en blød start af dit websted, skal du overveje at lade metakoderne for **noindex** være på plads. På denne måde er du med til at sikre, at blød lancering forbliver begrænset til den mindre målgruppe, du ønsker at nå.

## <a name="a-site-that-is-in-production"></a>Et websted, der er i produktion

Når et websted er i produktion, skal du sørge for, at alle webstedets sider er korrekt mærket. Microsoft Dynamics 365 Commerce bruger de oplysninger, der er angivet for en side, til at gengive alle SEO-oplysninger på den pågældende side. Følgende moduler indeholder denne funktionalitet: kategorisideoversigt, listesideoversigt og produktsideoversigt.

For at optimere indekseringen af søgemaskiner bruger gengivelsesstrukturen begge oplysninger fra de SEO-egenskaber, der er konfigureret i Dynamics 365 Commerce, og modulspecifikke oplysninger. For et websted, der er i produktion, skal du sørge for, at filen robots.txt giver mulighed for indeksering af hele webstedet, og at det indeholder links til det publicerede dokument til oversigten over webstedet. Du bør aktivere funktionaliteten for generering af webstedsoversigt under **Indstillinger for websted \> Oversigter over websted er aktiveret**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Indstillinger for side-SEO til interne prøveversioner, begrænset målgruppe og alle målgrupper

Da Dynamics 365 Commerce understøtter "what you see is what you get" (WYSIWYG) i godkendte eksempelvisninger i den visuelle sidegenerator, kan forfattere forberede deres sideindhold uden at være bange for, at oplysningerne bliver synlige for besøgende på webstedet. Hvis en side skal udgives, men eksponeringen skal være begrænset, skal den have metakoden **noindex**, så den ikke vil blive indekseret af søgemaskiner. Når siden er klar til alle målgrupper, skal alle grundlæggende SEO-metadata være til stede for at maksimere effektiviteten af søgeprogrammers indeksering. Derudover bør metakoden **nolimit** være fjernet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Administrere e-handelsbrugere og -roller](manage-ecommerce-users-roles.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)

[Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
