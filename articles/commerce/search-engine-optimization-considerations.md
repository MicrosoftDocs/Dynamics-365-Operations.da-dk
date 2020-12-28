---
title: Overvejelser om optimering af søgeprogram (SEO) for webstedet
description: I dette emne beskrives SEO-overvejelserne (søgemaskineoptimering) for dit websted fra udvikling til produktion.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6ffc772addb330abe7205007662a3f3e08a3e47f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411163"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Overvejelser om optimering af søgeprogram (SEO) for webstedet


[!include [banner](includes/banner.md)]

I dette emne beskrives SEO-overvejelserne (søgemaskineoptimering) for dit websted fra udvikling til produktion.

## <a name="a-site-that-is-under-development"></a>Et websted, der er under udvikling

Mens et websted er under udvikling, skal alle websider have metakoderne **NOINDEX** og **NOFOLLOW**, så søgemaskinerne ikke indekserer siderne og gemmer udviklingsversionerne af webstedet i cachen. For at kunne foretage denne konfiguration skal du føje standardmetakodemodulet til webstedets sideskabelon. Standardegenskaberne for metakoder vil derefter være tilgængelige i området for SEO-egenskaber i sideeditoren. Du kan bruge disse egenskaber til at administrere metakoderne.

## <a name="soft-launch-of-a-site"></a>Blød start af et websted

Under en "blød start" stilles et websted til rådighed for et begrænset publikum eller marked, før hele lanceringen finder sted. Hvis du udfører en blød start af dit websted, skal du overveje at lade metakoderne for **NOINDEX** være på plads. På denne måde er du med til at sikre, at blød lancering forbliver begrænset til den mindre målgruppe, du ønsker at nå.

## <a name="a-site-that-is-in-production"></a>Et websted, der er i produktion

Når et websted er i produktion, skal du sørge for, at alle webstedets sider er korrekt mærket. Microsoft Dynamics 365 Commerce bruger de oplysninger, der er angivet for en side, til at gengive alle SEO-oplysninger på den pågældende side. Følgende moduler indeholder denne funktionalitet: kategorisideoversigt, listesideoversigt og produktsideoversigt.

For at optimere indekseringen af søgemaskiner bruger gengivelsesstrukturen begge oplysninger fra de SEO-egenskaber, der er konfigureret i Dynamics 365 Commerce, og modulspecifikke oplysninger. For et websted, der er i produktion, skal du sørge for, at filen robots.txt giver mulighed for indeksering af hele webstedet, og at det indeholder links til det publicerede dokument til oversigten over webstedet. Du bør aktivere funktionaliteten for generering af webstedsoversigt under **Indstillinger for websted \> Oversigter over websted er aktiveret**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Indstillinger for side-SEO til interne prøveversioner, begrænset målgruppe og alle målgrupper

Da Dynamics 365 Commerce understøtter "what you see is what you get" (WYSIWYG) i godkendte eksempelvisninger i den visuelle sidegenerator, kan forfattere forberede deres sideindhold uden at være bange for, at oplysningerne bliver synlige for besøgende på webstedet. Hvis en side skal udgives, men eksponeringen skal være begrænset, skal den have metakoden **NOINDEX**, så den ikke vil blive indekseret af søgemaskiner. Når siden er klar til alle målgrupper, skal alle grundlæggende SEO-metadata være til stede for at maksimere effektiviteten af søgeprogrammers indeksering. Derudover bør metakoden **NOLIMIT** være fjernet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Administrere e-handelsbrugere og -roller](manage-ecommerce-users-roles.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)

[Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md)
