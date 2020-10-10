---
title: Vælg et tema for webstedet
description: Dette emne indeholder en beskrivelse af, hvordan du kan angive eller ændre webstedets tema i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f92b31e870cbb4d3cc04870273693bed1378c5e
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817700"
---
# <a name="select-a-site-theme"></a>Vælg et tema for webstedet

[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan angive eller ændre webstedets tema i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Layout og typografi til et websted (f.eks. skrifttyper, størrelser og farver) defineres af det tema, du vælger, og gælder for webstedet. Et tema oprettes og implementeres af en udvikler i firmaet. Du kan finde en oversigt over temaer under [Oversigt over temaer](http://). Du kan finde flere oplysninger om, hvordan du opretter og anvender temaer, under [Oprette et nyt tema](http://).

Når du første gang opretter et websted, bruger det som standard et tema med navnet **Fabrikam**. Dette standardtema findes som en del af Commerce-modulbiblioteket. Når du har implementeret yderligere temaer for dit websted, kan du konfigurere webstedet, så det bruger et af dem i stedet.

## <a name="select-the-site-theme"></a>Vælge temaet for webstedet

Udfør følgende trin for at vælge det tema, der anvendes på webstedet.

1. Gå til dit websted i webstedets oprettelsesmiljø.
1. Gå til **Administration af websted** \> **Udvidelsesmuligheder**.
1. Vælg et tema i rullemenuen under **Tema**.
1. Vælg **Gem og udgiv** for at anvende det valgte tema på webstedet.

> [!NOTE]
> Det tema, du vælger, udgives på webstedet, så snart du vælger **Gem og udgiv** på siden **Udvidelsesmuligheder**. Hvis du vil se et tema på webstedet, før du anvender det, kan du bruge dit udviklings- eller sandkassemiljø.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføj et logo](add-logo.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en favicon](add-favicon.md)

[Tilføj en velkomstmeddelelse](add-welcome-message.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)
