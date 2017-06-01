---
title: Konfigurer stregkoder
description: I dette emne beskrives det, hvordan du bruger stregkoder i Microsoft Dynamics 365 for Operations- Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f182f719d2e20673db9b576d9831e060c351a550
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-bar-codes"></a>Konfigurer stregkoder

[!include[banner](includes/banner.md)]


I dette emne beskrives det, hvordan du bruger stregkoder i Microsoft Dynamics 365 for Operations- Retail.

Du kan bruge stregkoder til at købe og sælge produkter, spore produktvarianter og konfigurere kunder og medarbejdere. Du kan også bruge stregkoder til at udstede og påtegne kuponer, gavekort og kreditnotaer. Du kan konfigurere detailprodukter, så de indeholder standardstregkoder eller brugerdefinerede, interne stregkoder. Produkter kan have mere end en stregkode. Et produkt kan f.eks. eventuelt have flere stregkoder, hvis det stammer fra forskellige producenter, eller hvis det har varianter, der er baseret på størrelse, typografi eller farve. Stregkoder kan omfatte produktets vægt eller pris. Stregkodemasker er skabeloner, der bruges til at oprette stregkoder. **Bemærk:** Når du tildeler en entydig stregkode til hver variantkombination, kan du scanne stregkoden i kasseapparatet og lade programmet afgøre, hvilken variant af produktet der sælges. Du kan også indsamle og få vist statistik over salg efter variant. Hver størrelses-, farve- og typografigruppe kan tildeles et entydigt nummer, der identificerer gruppen i stregkoden. Dynamics 365 for Operations bruger stregkodemasken til automatisk at generere stregkoder til alle variantkombinationer. Denne funktionalitet kan være praktisk, hvis der er mange størrelser, farver og typografier, da antallet af kombinationer øges betydeligt, efterhånden som hver variantkode tilføjes. Hvis denne funktionalitet ikke bruges, skal stregkoder tildeles manuelt til hver enkelt kombination, der repræsenterer en produktvariant. Du kan oprette stregkoder manuelt eller automatisk. Udfør følgende opgaver i den rækkefølge, hvori de er angivet, for at oprette stregkoder.

1.  [Opsætning af stregkodemasketegn](set-up-bar-code-masks.md).
2.  [Opsætning af stregkodemasker](set-up-bar-code-masks.md).
3.  Konfigurer stregkodeopsætninger.
4.  Opret stregkoder til produkter.


<a name="see-also"></a>Se også
--------

[Opsætning af stregkodemasker](set-up-bar-code-masks.md)




