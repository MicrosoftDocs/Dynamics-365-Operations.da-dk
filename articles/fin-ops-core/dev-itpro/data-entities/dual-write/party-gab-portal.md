---
title: Brug af Microsoft Power Apps-portaler sammen med datamodellen for part
description: I dette emne beskrives ændringerne af webrollerne for Microsoft Power Apps-portaler på grund af datamodellen for part i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 8242a74b8b2251a8489b772f5c4746b113fe2987
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060914"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Brug af Microsoft Power Apps-portaler sammen med datamodellen for part

[!INCLUDE[banner](../../includes/banner.md)]



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
