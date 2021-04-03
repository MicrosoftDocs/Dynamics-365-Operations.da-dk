---
title: Juster resultater for AI-ML-baserede produktanbefalinger
description: I dette emne beskrives, hvordan du kan skræddersy resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9e370faed7feb0640959a9fcc4b608f18f9ffc1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263940"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>Juster resultater for AI-ML-baserede produktanbefalinger


[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du justerer resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed. 

Når du har aktiveret produktanbefalinger, træder standardindstillingerne i kraft. Disse parametre kan bruges ved mange behov og til mange formål. Det er bedst at planlægge at bruge tid på at evaluere, om resultaterne opfylder produkternes markedsbevægelse. Vi foreslår, at du evaluerer resultaterne i nogle dage, før du ændrer parametre efter behov og tester igen. 

## <a name="understanding-recommendation-list-parameters"></a>Om parametre for anbefalingslister

Før du ændrer parametrene, skal du sætte dig ind i, hvordan de påvirker resultaterne nedenfor.

### <a name="trending-product-list"></a>Liste over mest populære produkter

Listen over de mest populære produkter har to parametre, der kan ændres:

![Eksempel på standardparametre for liste over mest populære produkter](./media/exampletrendingparameters.png)

1. **Medtag nye produkter fra de seneste X dage** - Produkter, der er blevet tilføjet inden for det angivne antal dage, før den aktuelle dato kan bruges til at vælge produktkandidater. Standardværdien på billedet antyder, at produkter så gamle som 180 dage, kan bruges på listen med populære produkter.
1. **Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne. Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over populære produkter. 

### <a name="best-selling-product-list"></a>Liste over mest solgte produkter

Afhængigt af din virksomhed kan listen over mest solgte produkter give et andet resultat end de mest populære produkter, selvom de begge bruger transaktionsdata til at rangordne produkter. Da Bedst sælgende ikke har nogen skæring baseret på dato for udvælgelse, kan Bedst sælgende stadig fremhæve meget populære produkter af ældre dato, der muligvis er blevet slettet fra popularitetslisten. 

Listen over de mest solgte produkter har én parameter, der kan ændres:

![Eksempel på standardparameter for liste over bedst sælgende](./media/examplebestsellingparameters.PNG)

1. **Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne. Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over bedst sælgende produkter. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Tilføje eller fjerne produkter manuelt fra anbefalingslister

### <a name="for-new-trending-or-best-selling-lists"></a>For listerne Ny, Mest populære eller Mest solgte

1.  Gå til **Retail og Commerce** > **Produktanbefalinger** > **Anbefalingsparametre**.
1.  Vælg **Anbefalingslister** på listen over delte parametre.
1.  Vælg listen, du vil tilføje eller fjerne produkter fra.
1.  Hvis du vil føje produkter til tabellen, skal du vælge **Tilføj linje**. 
1.  Søg efter et produkts **Navn** eller **Produktnummer** i produktkolonnen.

    ![Eksempel på søgning efter et produkt på listen Nyt produkt](./media/examplenewlistconfiguration1.png)

1.  I kolonnen Linjetype skal du vælge en af to indstillinger:
    -   **Medtag** – tvinger et produkt op forrest på listen
    -   **Udeluk** – fjerner et produkt, så det ikke bliver vist på listen
    
    ![Eksempel på, hvordan et produkt medtages eller udelukkes fra listen Nyt produkt](./media/examplenewlistconfiguration2.png)

1.  Hvis du ændrer **Visningsrækkefølge**, ændres den rækkefølge, som de produkter, der er markeret **medtag**, vises i på listen.
    - Hvis to produkter har samme værdi for **visningsrækkefølge**, kan den endelige rækkefølge af disse to resultater afvige fra administrationens.
1.  Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge **Fjern**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>For listerne "Andre synes også godt om" eller "Ofte købt sammen"

I forbindelse med listerne "Ofte købt sammen" eller "Andre synes også godt om" bruges maskinel indlæring til at analysere forbrugeres indkøbsmønstre for at anbefale relaterede produkter, der ofte købes sammen, som et produkt med entydig oprindelse. 
 
Et *oprindelsesprodukt* er det produkt, du vil generere resultater for. I forbindelse med manuel justering af anbefalingslister tilføjer eller fjerner du resultater for dette produkt. 

Udfør følgende trin for manuelt at tilføje eller fjerne resultater for et oprindelsesprodukt:
1.  Vælg **Oprindelsesprodukt**. 
1.  Søg i kolonnen **Produkt** efter et produkt ud fra **Navn** eller **Produktnummer**.
![Eksempel på søgning efter et produkt på listen Ofte købt sammen](./media/exampleFBTlistconfiguration1.png)
1. I kolonnen **Linjetype** skal du vælge en af to indstillinger:
    - **Medtag** – tvinger et produkt op forrest på listen
    - **Udeluk** – fjerner et produkt, så det ikke bliver vist på listen     
![Eksempel på at medtage eller udelukke et produkt fra listen Ofte købte sammen](./media/exampleFBTlistconfiguration2.png)
1.  Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge Fjern.


## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]