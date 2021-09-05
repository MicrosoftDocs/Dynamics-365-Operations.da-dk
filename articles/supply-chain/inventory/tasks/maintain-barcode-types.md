---
title: Vedligeholde stregkodetyper
description: Denne procedure viser, hvordan du opretter en ny stregkodedefinition, som derefter kan bruges som en del af pluklisterapporten.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 052311e15aeb20b927cbed217a2bda600dad60a5
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345644"
---
# <a name="maintain-bar-code-types"></a>Vedligeholde stregkodetyper

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en ny stregkodedefinition, som derefter kan bruges som en del af pluklisterapporten. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Hvis du bruger USMF, kan du bruge eksempelværdier, der vises. Disse opgaver udføres normalt af en lagerchef.

1. Gå til **Stregkoder**.
1. Vælg **Ny**.
1. Skriv en værdi i feltet **Stregkodeopsætning**.
1. Indtast en værdi i feltet **Beskrivelse**.
1. Vælg en indstilling i feltet **Stregkodetype**.
    * Hvis du bruger USMF, kan du vælge "Kode 39".  
1. Angiv et tal i feltet **Størrelse**.
1. Angiv et tal i feltet **Maksimumlængde**.
1. Vælg **Gem**.
1. Luk siden.
1. Gå til **Parametre til lager- og lagerstedsstyring**.
1. Indtast eller vælg en værdi i feltet **Stregkodeopsætning**.
    * Vælg den stregkodeopsætning, som du oprettede før, men vær opmærksom på, at stregkodeformatet skal svare til formatet for det entydige id for den posttype, der bruges i processen. For eksempel bør stregkodeformatet til plukruter være samme format som til plukrutereferencen, der typisk er en nummerserie.  
1. Vælg **Gem**.
1. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]