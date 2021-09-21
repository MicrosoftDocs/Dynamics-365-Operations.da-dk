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
ms.openlocfilehash: 4102f8036c0aede7c8a2adcaa9b8799a71ac7ada
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441283"
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
1. Angiv i feltet **Maske-id** id for stregkodemasken. Stregkodemasker bruges til at oprette stregkoder og til hurtigt at identificere stregkoder, der er scannet ind i POS-systemet. Yderligere oplysninger finder du under [Opsætning af stregkodemasker](../../../commerce/set-up-bar-code-masks.md).
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
