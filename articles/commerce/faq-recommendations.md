---
title: Ofte stillede spørgsmål om produktanbefalinger
description: Dette emne indeholder oplysninger om processer og værktøjer, du kan bruge til at foretage fejlfinding af problemer, der vedrører produktanbefalinger eller resultaterne af dem.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cf3df2267671b50c20b28dbdb1c6a21696bf2515
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410970"
---
# <a name="product-recommendations-faq"></a>Ofte stillede spørgsmål om produktanbefalinger


[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om processer og værktøjer, du kan bruge til at foretage fejlfinding af problemer, der vedrører [produktanbefalinger](product-recommendations.md) eller resultaterne af dem.

## <a name="best-practices"></a>Bedste fremgangsmåder
Det er meget vigtigt at udnytte begrebet produktmastere og -varianter. Grupperingen af varianter i en overordnet produktmaster udnyttes af listealgoritmerne og tjenesten til at oprette bedre modeller. Desuden kan tjenesten kun levere én forekomst af et produkt i stedet for at sætte alle tæt forbundne varianter på en liste. Når alle nært relaterede varianter placeres på en liste, kan der forekomme forkerte eller identiske resultater.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Hvorfor mangler der produkter i mine anbefalingslister?

Hvis der mangler en vare på en produktanbefalingsliste, kan der typisk være problemer med produktkonfigurationen. Der kan f.eks. være en forkert produktstartdato eller -slutdato, en dimension kan være fejlkonfigureret, eller produktet er muligvis ikke i det korrekte kanalsortiment osv.

Hvis der mangler en vare på en anbefalingsliste, der er baseret på kunstig intelligens-maskinel indlæring (AI-ML), er varen muligvis ikke i overensstemmelse med kriterierne for anbefalingslisten, eller der er muligvis ikke nok indkøbstransaktioner på anbefalingslister til at vise den.

Det anbefales, at du kontrollerer disse trin:
1. **Sørg for, at produktanbefalingerne er aktiveret i hovedkontoret.** Du kan finde oplysninger om, hvordan du aktiverer denne tjeneste, under [Aktiver produktanbefaler](enable-product-recommendations.md).
1. **Sørg for, at nøgleproduktegenskaberne er angivet.** Produktsortimenter skal f.eks. være indstillet til **Medtag**.
1. **For nyligt udvalgte produkter kan det tage op til tre timer, før produktet begynder at blive vist på den nye liste.**
1. **Hvis et produkt stadig ikke vises i Mest populære, Bedst sælgende, Andre synes også godt om eller Ofte købt sammen, vil produktet muligvis ikke have nok transaktioner.** I dette tilfælde kan du enten vente på, at der foretages flere transaktioner, opdatere standardparametrene for anbefalingslisten eller bruge manuel indgriben til at redigere resultaterne af produktlisten. Du kan finde flere oplysninger om anbefalingsparametre under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).
1. **Kontroller, at produktet opfylder anbefalingskriterierne for listen.** Du kan finde flere oplysninger om produktanbefalingsparametre under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Hvordan kan jeg forhindre, at der returneres dårlige anbefalingsresultater?

Anbefalingslister kræver en stor mængder transaktioner for at opnå resultater. Det er derfor vigtigt, at brugerne leverer fuldstændige historiske transaktionsdata.

Desuden har produkter, der ikke har nogen transaktioner eller få transaktioner, typisk ikke resultater af typen **Andre synes også godt om** eller **Ofte købt sammen**, og de vises ikke i **Mest populære** eller **Bedst sælgende**-anbefalingslister. Denne situation kan ofte forekomme for meget nye produkter eller for gamle produkter, der har et lille antal indkøb. Nye populære varer kan nemt overvinde dette problem.

Det anbefales, at du følger disse trin:
1. **Kontroller, at produktet opfylder anbefalingskriterierne for denne liste.** Du kan finde flere oplysninger om produktanbefalingsparametre under Redigere resultater for AI-ML-baserede produktanbefalinger.
1. **Hvis produktet er nyt, bør du overveje at redigere en anbefalingsliste, indtil produktet har flere transaktioner.** Du kan finde flere oplysninger om, hvordan du redigerer anbefalingslistens resultater under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).


- **Kontroller, at produktet opfylder anbefalingskriterierne for denne liste.** Du kan finde flere oplysninger om produktanbefalingsparametre under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).
- **Hvis produktet er nyt, bør du overveje at redigere en anbefalingsliste, indtil produktet har flere transaktioner**. Du kan finde flere oplysninger om, hvordan du redigerer anbefalingslistens resultater under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Kan jeg fjerne et produkt, men stadig se det i butikken?

Du kan justere lister, der genereres algoritmisk, hvis der opstår et forretningsmæssigt behov. Men hvis et produkt fjernes fra en anbefalingsliste, vil produktet stadig være synligt i butikken. Du kan finde flere oplysninger om, hvordan du redigerer produktanbefalingsresultater under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).

Hvis du vil forhindre, at en vare er synlig i butikken, skal du ændre værdien for **Varesortimenter**, til **Udelad**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Hvordan føjer jeg en liste til en e-handelsside?

Du kan finde flere oplysninger om, hvordan du føjer produktanbefalingssider til e-handelswebsteder, under [Tilføje lister med produktanbefalinger på sider](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Hvordan aktiverer jeg anbefalinger i POS?

Når du har aktiveret produktanbefalinger, skal du tilføje anbefalingspanelet på kontrolelementets POS-skærm. Du kan få flere oplysninger i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]