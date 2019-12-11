---
title: Administrere resultater for AI-ML-baserede produktanbefalinger
description: I dette emne beskrives, hvordan du kan skræddersy resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770064"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a>Administrere resultater for AI-ML-baserede produktanbefalinger

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan skræddersy resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed. 

Når du har aktiveret produktanbefalinger, træder standardindstillingerne i kraft. Disse parametre kan bruges ved mange behov og til mange formål. Det er bedst at planlægge at bruge tid på at evaluere, om resultaterne opfylder produkternes markedsbevægelse. Vi foreslår, at du evaluerer resultaterne i nogle dage, før du ændrer parametre efter behov og tester igen. 

## <a name="understanding-recommendation-list-parameters"></a>Om parametre for anbefalingslister

Før du ændrer parametrene, skal du sætte dig ind i, hvordan de påvirker resultaterne nedenfor.

### <a name="trending-product-list"></a>Liste over populære produkter

Listen med **Mest populære** for produkter har to parametre, der kan ændres: ![Eksempel på standardparametre for tendensliste](./media/exampletrendingparameters.png)
1. **Medtag nye produkter fra de seneste X dage** - Produkter, der er blevet tilføjet inden for det angivne antal dage, før den aktuelle dato kan bruges til at vælge produktkandidater. Standardværdien på billedet antyder, at produkter så gamle som 180 dage, kan bruges på listen med populære produkter.
1. **Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne. Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over populære produkter. 

### <a name="best-selling-product-list"></a>Liste over bedst sælgende produkter

Afhængigt af virksomheden kan Bedst sælgende give et andet resultat end Tendens, selvom de begge bruger transaktionsdata til at rangordne produkter. Da Bedst sælgende ikke har nogen skæring baseret på dato for udvælgelse, kan Bedst sælgende stadig fremhæve meget populære produkter af ældre dato, der muligvis er blevet slettet fra popularitetslisten. 

Produktlisten **Bedst sælgende** har én parameter, der kan ændres:

![Eksempel på standardparameter for liste over bedst sælgende](./media/examplebestsellingparameters.PNG)
1. **Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne. Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over bedst sælgende produkter. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Tilføje eller fjerne produkter manuelt fra anbefalingslister

### <a name="for-new-trending-or-best-selling"></a>For Ny, Mest populære eller Bedst sælgende

1.  Gå til **Detail** > **Produktanbefalinger** > **Anbefalingsparametre**.
1.  Vælg **Anbefalingslister** på listen over delte detailparametre.
1.  Vælg listen, du vil tilføje eller fjerne produkter fra.
1.  Hvis du vil føje produkter til tabellen, skal du vælge **Tilføj linje**. 
1.  Søg i kolonnen Produkt efter et produkt ud fra **Navn** eller **Produktnummer**.
![Eksempel på søgning efter et produkt på listen Ny produkt](./media/examplenewlistconfiguration1.png)
1.  I kolonnen Linjetype skal du vælge en af to indstillinger:
    -   **Medtag** – tvinger et produkt op forrest på listen
    -   **Udeluk** – fjerner et produkt, så det ikke bliver vist på listen ![Eksempel på at medtage eller udelukke et produkt fra listen Ny produkt](./media/examplenewlistconfiguration2.png)
1.  Hvis du ændrer **Visningsrækkefølge**, ændres den rækkefølge, som de produkter, der er markeret **medtag**, vises i på listen.
    - Hvis to produkter har samme værdi for **visningsrækkefølge**, kan den endelige rækkefølge af disse to resultater afvige fra administrationens.
1.  Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge **Fjern**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>For listerne Andre synes også godt om eller Ofte er købt sammen

I forbindelse med listerne **Ofte købt sammen** eller **Andre synes også godt om** bruges maskinel indlæring til at analysere forbrugeres indkøbsmønstre for at anbefale relaterede produkter, der ofte købes sammen, som et produkt med entydig oprindelse. 
 
Et **oprindelsesprodukt** er det produkt, du vil generere resultater for. I forbindelse med manuel justering af anbefalingslister tilføjer eller fjerner du resultater for dette produkt. 

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

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Tilføje lister med produktanbefalinger på sider](add-reco-list-to-page.md)
