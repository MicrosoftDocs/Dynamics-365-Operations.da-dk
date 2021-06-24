---
title: Forberede at vedligeholde standardomkostninger for producerede varer
description: I dette emne beskrives trinnene til forberedelse af vedligeholdelse af omkostninger for producerede varer.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a82b0a205ac6b7a86b9aca0771303469c6666c1
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187740"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Forberede at vedligeholde standardomkostninger for producerede varer

[!include [banner](../includes/banner.md)]

I dette emne beskrives trinnene til forberedelse af vedligeholdelse af omkostninger for producerede varer. Trinnene for producerede varer varierer en smule fra trinnene for købte varer.

Regler, der er knyttet til producerede varer, kan påvirke omkostningsberegningerne for de overordnede producerede varer. Benyt følgende fremgangsmåde, hvis du vil forberede vedligeholdelse af omkostninger for producerede varer.

1. Knyt en varemodelgruppe til den producerede vare. 

   Varemodelgruppen identificerer, at der skal bruges standardomkostninger.

2. Knyt en varegruppe til den producerede vare. 

   Varegruppen indeholder finanskonti, der gælder for den producerede vare. Finanskontiene for en produceret vare, der har en lagermodel af typen standardomkostninger, omfatter flere produktionsafvigelser, en ændring for omkostningsafvigelse og værdiregulering af lageromkostninger.

3. Knyt måleenheder for lageret til varen. 

   Varens omkostninger er altid udtrykt i varens måleenhed for lageret.

4. Du skal ikke knytte en kostprisgruppe til den producerede vare, medmindre varen skal behandles som en købt vare.

5. Knyt en styklisteberegningsgruppe til den producerede vare. 

   Varens styklisteberegningsgruppe definerer advarselssituationer, der gælder. På denne måde, kan advarselsmeddelelser, når der udføres en styklisteberegning, oprettes om mulige kilder til beregningsfejl. En advarsel kan f.eks. identificere, hvornår der ikke findes en aktiv stykliste eller rute. Styklisteberegningsgruppen indeholder en regel om stop af udfoldning, der angiver, hvornår en produceret vare skal behandles som en købt vare.

6. Hvis den producerede vare har konstante omkostninger, kan du knyt et standardordreantal til den. 

   Standardordreantallet er en regnskabsmæssig lotstørrelse til amortisering af konstante omkostninger. Eksempler på konstante omkostninger omfatter opsætningstider i ruteoperationer og et konstant komponentantal på styklisten.

7. Definer styklisten for den producerede vare. 

   Der kan defineres en eller flere styklisteversioner for den producerede vare. Kontroller, at de versioner, du ønsker, er markeret som godkendt og aktive, og at de har de ønskede ikrafttrædelsesdatoer. Styklisteversionen kan gælde for hele firmaet eller være lokationsspecifik.

8. Definer ruten for den producerede vare. 

   Der kan defineres en eller flere ruter for den producerede vare. Kontroller, at de versioner, du ønsker, er markeret som godkendt og aktive, og at de har de ønskede ikrafttrædelsesdatoer. Ruten skal være lokationsspecifik.

Hvis du vil bruge ruteoplysninger i forbindelse med efterkalkulation, er der brug for flere trin i forberedelsen. Omkostningskategorier, der er knyttet til ruteoperationer, skal f.eks. være korrekte og fuldførte.

## <a name="related-topics"></a>Relaterede emner

[Amortisere konstante omkostninger for en produceret vare](amortize-constant-costs-manufactured-item.md)

[Konfigurere produkter, som kan være produceret eller indkøbt](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]