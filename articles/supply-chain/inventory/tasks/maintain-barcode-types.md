---
title: Vedligehold stregkodetyper
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
ms.openlocfilehash: 937384f14d88dafd537888d862ee1e363ea20626
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809512"
---
# <a name="maintain-barcode-types"></a>Vedligehold stregkodetyper

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en ny stregkodedefinition, som derefter kan bruges som en del af pluklisterapporten. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Hvis du bruger USMF, kan du bruge eksempelværdier, der vises. Disse opgaver udføres normalt af en lagerchef.

1. Gå til Stregkoder.
2. Klik på Ny.
3. Skriv en værdi i feltet Stregkodeopsætning.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg en indstilling i feltet Stregkodetype.
    * Hvis du bruger USMF, kan du vælge "Kode 39".  
6. Angiv et tal i feltet Størrelse.
7. Angiv et tal i feltet Maksimumlængde.
8. Klik på Gem.
9. Luk siden.
10. Gå til Parametre til lager- og lokationsstyring.
11. Indtast eller vælg en værdi i feltet Stregkodeopsætning.
    * Vælg den stregkodeopsætning, som du oprettede før, men vær opmærksom på, at stregkodeformatet skal svare til formatet for det entydige id for den posttype, der bruges i processen. For eksempel bør stregkodeformatet til plukruter være samme format som til plukrutereferencen, der typisk er en nummerserie.  
12. Klik på Gem.
13. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]