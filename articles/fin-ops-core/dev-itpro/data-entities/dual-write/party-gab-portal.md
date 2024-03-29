---
title: Bruge Microsoft Power Apps-portaler sammen med datamodellen for part
description: Denne artikel beskriver ændringerne af webrollerne for Microsoft Power Apps-portaler på grund af datamodellen for part i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 8d7a6ae48834ddd5f06f73bfe3129e44d14d86b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288980"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Brug af Microsoft Power Apps-portaler sammen med datamodellen for part

[!INCLUDE[banner](../../includes/banner.md)]



Dobbeltskrivningsprogrammets orkestreringsløsning version 2.0.999.0 og senere inkluderer datamodelændringer til part- og globalt adressekartotek for tabellerne Konto og Kontakt. Ændringerne giver mulighed for mange til mange-relationer, der understøtter avancerede forretningsscenarier. Disse ændringer understøttes ikke af portalwebroller, herunder kundeportalen, der medfølger som standard, eller som fandtes i dit miljø, før du installerede dobbeltskrivning. Hvis webrollerne skal fungere som forventet, skal du oprette nye webroller ved hjælp af den nye datamodel. 

Kort sagt er den måde, som tabellerne fungerer sammen på, ændret, men tabeltilladelserne i kundeportalen er ikke ændret. Denne artikel forklarer, hvordan du opretter nye webroller, der kan arbejde med den nye avancerede datamodel.

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

    + Forbindelse mellem tabellen **Kontakt** og **Part**
    + Forbindelse mellem tabellen **Part** og **Konto**
    + Forbindelse mellem tabellen **Konto** og **Ordre**

4. Opret og gem en ny tilladelse for forbindelsen Kontakt til part ved at angive følgende parametre:

    + **Navn**: Forbindelse mellem tabellen **Part** og **Konto** (eller dit valg)
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
