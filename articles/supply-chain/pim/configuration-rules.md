---
title: Variantregler
description: Denne artikel indeholder generelle oplysninger om variantregler. Variantregler definerer relationer mellem elementer i en stykliste i styklisten for produkter, der bruger teknologien Dimensionsbaseret konfiguration.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e70713fb25584e26f97bcb7c769da6954aa36b81
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424291"
---
# <a name="configuration-rules"></a>Variantregler

[!include [banner](../includes/banner.md)]

Denne artikel indeholder generelle oplysninger om variantregler. Variantregler definerer relationer mellem elementer i en stykliste i styklisten for produkter, der bruger teknologien Dimensionsbaseret konfiguration.

Variantregler er tilgængelige, når du definerer modeller for dimensionsbaseret konfiguration. Variantregler anvendes til enten at gennemtvinge eller forbyde specifikke varekombinationer på en stykliste. Når en stykliste er blevet oprettet, og de pågældende varer er blevet tildelt til deres respektive variantgrupper, kan der defineres en eller flere variantregler. Hvis to varer hører sammen, bruges operatoren **Vælg** til at sikre medtagelse. Hvis to varer gensidigt udelukker hinanden, bruges operatoren **Fravælg** til at sikre udelukkelse.  

**Bemærk!** Disse oplysninger gælder kun for produktmasters, der bruger teknologien til dimensionsbaseret konfiguration.  

Eksisterende varianter påvirkes ikke af efterfølgende ændringer af variantreglerne. Men det er vigtigt, at du opretter reglerne, før du definerer en ny variant, og at du kontrollerer reglerne, hvis du tror, at de er ændret.  

**Bemærk!** Metoden **Vælg** betyder, at den afledte variantgruppe, varenummer og variant vælges automatisk. Metoden **Fravælg** betyder, at den afledte variantgruppe, varenummer og variant ikke kan vælges.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oversigt over dimensionsbaseret produktkonfiguration](dimension-based-product-configuration.md)



