---
title: Konfigurere stregkoder
description: I denne artikel beskrives det, hvordan stregkoder bruges i Dynamics 365 Commerce.
author: jblucher
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d2b6754dadd3bf6ad797ecf2831c486fc03f64fcc5e0bb570a7adc98ae42d106
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743953"
---
# <a name="set-up-bar-codes"></a>Konfigurere stregkoder

[!include [banner](includes/banner.md)]

I denne artikel beskrives det, hvordan stregkoder bruges i Dynamics 365 Commerce.

Du kan bruge stregkoder til at købe og sælge produkter, spore produktvarianter og konfigurere kunder og medarbejdere. Du kan også bruge stregkoder til at udstede og påtegne kuponer, gavekort og kreditnotaer. Du kan konfigurere produkter, så de indeholder standardstregkoder eller brugerdefinerede, interne stregkoder. Produkter kan have mere end en stregkode. Et produkt kan f.eks. eventuelt have flere stregkoder, hvis det stammer fra forskellige producenter, eller hvis det har varianter, der er baseret på størrelse, typografi eller farve. Stregkoder kan omfatte produktets vægt eller pris. Stregkodemasker er skabeloner, der bruges til at oprette stregkoder.

> [!NOTE]
> Når du tildeler en entydig stregkode til hver variantkombination, kan du scanne stregkoden i kasseapparatet og lade programmet afgøre, hvilken variant af produktet der sælges. Du kan også indsamle og få vist statistik over salg efter variant. Hver størrelses-, farve- og typografigruppe kan tildeles et entydigt nummer, der identificerer gruppen i stregkoden. Commerce bruger stregkodemasken til automatisk at generere stregkoder til alle variantkombinationer. Denne funktionalitet kan være praktisk, hvis der er mange størrelser, farver og typografier, da antallet af kombinationer øges betydeligt, efterhånden som hver variantkode tilføjes. Hvis denne funktionalitet ikke bruges, skal stregkoder tildeles manuelt til hver enkelt kombination, der repræsenterer en produktvariant.

Du kan oprette stregkoder manuelt eller automatisk. Udfør følgende opgaver i den rækkefølge, hvori de er angivet, for at oprette stregkoder.

1. [Opsætning af stregkodemasketegn](set-up-bar-code-masks.md).
2. [Opsætning af stregkodemasker](set-up-bar-code-masks.md).
3. Konfigurer stregkodeopsætninger.
4. [Oprette stregkoder til produkter](../supply-chain/pim/tasks/create-bar-code-product.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere stregkodemasker](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]