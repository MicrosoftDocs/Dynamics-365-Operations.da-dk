---
title: Konfigurere stregkoder
description: I denne artikel beskrives det, hvordan stregkoder bruges i Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52801e0d09b1d7da50719966700ca45275d702f7
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057272"
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
4. Opret stregkoder til produkter.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere stregkodemasker](set-up-bar-code-masks.md)
