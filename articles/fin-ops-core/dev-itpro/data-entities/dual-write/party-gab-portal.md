---
title: Brug af Power Portal sammen med datamodellen for part
description: I dette emne beskrives ændringerne af Power Portal-webrollerne på grund af datamodellen for part i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 3b03603038d05305c63fc2890a196670ae343e53
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358611"
---
# <a name="using-power-portal-with-the-party-data-model"></a>Brug af Power Portal sammen med datamodellen for part

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Dobbeltskrivningsprogrammets orkestreringsløsning version 2.0.999.0 og senere inkluderer datamodelændringer til part- og globalt adressekartotek for tabellerne Konto og Kontakt. Ændringerne giver mulighed for mange til mange-relationer, der understøtter avancerede forretningsscenarier. Disse ændringer understøttes ikke af portalwebroller, herunder kundeportalen, der medfølger som standard, eller som fandtes i dit miljø, før du installerede dobbeltskrivning. Hvis webrollerne skal fungere som forventet, skal du oprette nye webroller ved hjælp af den nye datamodel. 

Kort sagt er den måde, som tabellerne fungerer sammen på, ændret, men tabeltilladelserne i kundeportalen er ikke ændret. Dette emne forklarer, hvordan du opretter nye webroller, der kan arbejde med den nye avancerede datamodel.

Dette diagram viser tabelrelationen **uden** datamodellen for parten og det globale adressekartotek:

   ![uden partmodel.](media/without-party-model.PNG)

Dette diagram viser tabelrelationen **med** datamodellen for parten og det globale adressekartotek:

   ![med partmodel.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Oprette en ny tabeltilladelse

Benyt følgende fremgangsmåde for at oprette disse nye tabeltilladelser:

1. Log på [Power Apps](https://make.powerapps.com), og gå til dine apps.
2. Vælg din portalstyringsapp.
3. Vælg **Sikkerhed > Tabelrettigheder** i sidepanelet.

    Du skal oprette tre nye tilladelser:

    + Kontakt til part-forbindelse
    + Part til konto-forbindelse
    + Konto til ordre-forbindelse

4. Opret og gem en ny tilladelse for forbindelsen Kontakt til part ved at angive følgende parametre:

    + **Navn**: Part til konto-forbindelse (eller dit valg)
    + **Tabelnavn**: msdyn_contactforparty
    + **Websted**: Kundeportal
    + **Område**: Kontakt
    + **Rettigheder**: Vælg alle
    + **Webroller**: Godkendte brugere, kunderepræsentant (eller dit valg)

5. Opret og gem en ny tilladelse for forbindelsen Part til konto ved at angive følgende parametre:

    + **Navn**: Part til konto-forbindelse (eller dit valg)
    + **Tabelnavn**: konto
    + **Websted**: Kundeportal
    + **Område**: Overordnet
    + **Rettigheder**: Vælg alle
    + **Overordnet tabeltilladelse**: Kontakt til part-forbindelse

6. Opret og gem en ny tilladelse for forbindelsen Konto til ordre ved at angive følgende parametre:

    + **Navn**: Konto til ordre-forbindelse (eller dit valg)
    + **Tabelnavn**: salgsordre
    + **Websted**: Kundeportal
    + **Område**: Overordnet
    + **Rettigheder**: Vælg alle
    + **Overordnet tabeltilladelse**: Part til konto-forbindelse

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
