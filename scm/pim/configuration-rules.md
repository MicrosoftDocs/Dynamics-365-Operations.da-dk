---
title: Variantregler
description: Denne artikel indeholder generelle oplysninger om variantregler. Variantregler definerer relationer mellem elementer i en stykliste i styklisten for produkter, der bruger teknologien Dimensionsbaseret konfiguration.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 74c8ffe4ab00e7afa1235e24327e18a65061636a
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="configuration-rules"></a>Variantregler

[!include[banner](../includes/banner.md)]


Denne artikel indeholder generelle oplysninger om variantregler. Variantregler definerer relationer mellem elementer i en stykliste i styklisten for produkter, der bruger teknologien Dimensionsbaseret konfiguration.

Variantregler er tilgængelige, når du definerer modeller for dimensionsbaseret konfiguration. Variantregler anvendes til enten at gennemtvinge eller forbyde specifikke varekombinationer på en stykliste. Når en stykliste er blevet oprettet, og de pågældende varer er blevet tildelt til deres respektive variantgrupper, kan der defineres en eller flere variantregler. Hvis to varer hører sammen, bruges operatoren **Vælg** til at sikre medtagelse. Hvis to varer gensidigt udelukker hinanden, bruges operatoren **Fravælg** til at sikre udelukkelse.  

**Bemærk!** Disse oplysninger gælder kun for produktmasters, der bruger teknologien til dimensionsbaseret konfiguration.  

Eksisterende varianter påvirkes ikke af efterfølgende ændringer af variantreglerne. Men det er vigtigt, at du opretter reglerne, før du definerer en ny variant, og at du kontrollerer reglerne, hvis du tror, at de er ændret.  

**Bemærk!** Metoden **Vælg** betyder, at den afledte variantgruppe, varenummer og variant vælges automatisk. Metoden **Fravælg** betyder, at den afledte variantgruppe, varenummer og variant ikke kan vælges.

<a name="see-also"></a>Se også
--------

[Dimensionsbaseret produktkonfiguration](dimension-based-product-configuration.md)




