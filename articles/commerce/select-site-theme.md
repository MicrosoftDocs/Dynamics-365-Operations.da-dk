---
title: Vælge et tema for webstedet
description: Denne artikel indeholder en beskrivelse af, hvordan du kan angive eller ændre webstedets tema i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b038dc996c571d54dce3f2aec679f7af8af85074
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900380"
---
# <a name="select-a-site-theme"></a>Vælge et tema for webstedet

[!include [banner](includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du kan angive eller ændre webstedets tema i Microsoft Dynamics 365 Commerce.

Layout og typografi til et websted (f.eks. skrifttyper, størrelser og farver) defineres af det tema, du vælger, og gælder for webstedet. Et tema oprettes og implementeres af en udvikler i firmaet. Du kan finde en oversigt over temaer under [Oversigt over temaer](e-commerce-extensibility/theming.md). Du kan finde flere oplysninger om, hvordan du opretter og anvender temaer, under [Oprette et nyt tema](e-commerce-extensibility/create-theme.md).

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

[Tilføje et logo](add-logo.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføje en favicon](add-favicon.md)

[Tilføje en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)

[Oversigt over temaer](e-commerce-extensibility/theming.md)

[Opret et nyt tema](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
