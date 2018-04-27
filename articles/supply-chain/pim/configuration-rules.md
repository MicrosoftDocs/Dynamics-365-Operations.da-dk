---
title: Variantregler
description: Denne artikel indeholder generelle oplysninger om variantregler. Variantregler definerer relationer mellem elementer i en stykliste i styklisten for produkter, der bruger teknologien Dimensionsbaseret konfiguration.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bc8e606cdc0bc5a45321c67ce9b089059f226df2
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---

# <a name="configuration-rules"></a>Variantregler

[!INCLUDE [banner](../includes/banner.md)]

Denne artikel indeholder generelle oplysninger om variantregler. Variantregler definerer relationer mellem elementer i en stykliste i styklisten for produkter, der bruger teknologien Dimensionsbaseret konfiguration.

Variantregler er tilgængelige, når du definerer modeller for dimensionsbaseret konfiguration. Variantregler anvendes til enten at gennemtvinge eller forbyde specifikke varekombinationer på en stykliste. Når en stykliste er blevet oprettet, og de pågældende varer er blevet tildelt til deres respektive variantgrupper, kan der defineres en eller flere variantregler. Hvis to varer hører sammen, bruges operatoren **Vælg** til at sikre medtagelse. Hvis to varer gensidigt udelukker hinanden, bruges operatoren **Fravælg** til at sikre udelukkelse.  

**Bemærk!** Disse oplysninger gælder kun for produktmasters, der bruger teknologien til dimensionsbaseret konfiguration.  

Eksisterende varianter påvirkes ikke af efterfølgende ændringer af variantreglerne. Men det er vigtigt, at du opretter reglerne, før du definerer en ny variant, og at du kontrollerer reglerne, hvis du tror, at de er ændret.  

**Bemærk!** Metoden **Vælg** betyder, at den afledte variantgruppe, varenummer og variant vælges automatisk. Metoden **Fravælg** betyder, at den afledte variantgruppe, varenummer og variant ikke kan vælges.

<a name="see-also"></a>Se også
--------

[Dimensionsbaseret produktkonfiguration](dimension-based-product-configuration.md)




