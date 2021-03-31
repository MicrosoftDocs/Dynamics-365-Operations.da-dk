---
title: Vedligeholdelsesarbejdere og arbejdergrupper
description: I dette emne forklares vedligeholdelsesarbejdere og arbejdergrupper i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00ada9e43ae08e1757de618bd2d63dc147beeca0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226827"
---
# <a name="maintenance-workers-and-worker-groups"></a>Vedligeholdelsesarbejdere og arbejdergrupper

[!include [banner](../../includes/banner.md)]

 

I dette emne forklares vedligeholdelsesarbejdere og arbejdergrupper i Styring af aktiver. I Styring af aktiver kan du knytte vedligeholdelsesarbejdere til arbejdssteder. (Du finder flere oplysninger om arbejdssteder under [Opret arbejdssteder](../functional-locations/create-functional-locations.md).) Denne funktion kan være nyttig, hvis du eksempelvis planlægger et vedligeholdelsesjob på en maskine, der er placeret i arbejdssted 01, og du vil allokere vedligeholdelsesarbejdere fra samme sted til at udføre jobbet.

Du kan også oprette vedligeholdelsesarbejdergrupper og knytte vedligeholdelsesarbejdere til dem. Denne funktion er nyttig, når du laver enkel arbejdsordreplanlægning, og du vil planlægge en gruppe vedligeholdelsesarbejdere på en arbejdsordre. Du kan bruge vedligeholdelsesarbejdere og vedligeholdelsesarbejdergrupper til at oprette foretrukne vedligeholdelsesarbejdere og ansvarlige vedligeholdelsesarbejdere. 


## <a name="create-workers"></a>Opret medarbejdere

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdere** \> **Arbejdere**.
2. Vælg **Ny** for at føje en arbejder til listen.
3. I feltet **Arbejder** skal du vælge arbejderen.
4. Angiv indstillingen **Aktiv** til **Ja** for at planlægge arbejderen på arbejdsordrer.

    I oversigtspanelet **Generelt** udfyldes felterne **Ressource** og **Beskrivelse** automatisk, hvis der er valgt en ressource for arbejderen. Feltet **Kalender** udfyldes også automatisk, forudsat at du har oprettet arbejderen som en ressource og har allokeret en kalender til den pågældende ressource på siden **Ressourcer** (**Organisationsadministration** \> **Ressourcer** \> **Ressourcer**).

5. I oversigtspanelet **Grupper** skal du vælge **Tilføj** og derefter vælge en vedligeholdelsesarbejdergruppe for arbejderen. En arbejder kan knyttes til mere end én gruppe.
6. I standardopsætningen er en arbejders tilknytning til en gruppe gældende fra den dato, hvor du tilføjer gruppen, og den udløber aldrig. Denne dato vises i feltet **Gyldig**. Hvis du vil se feltet **Gyldig**, skal du vælge **Se** \> **Alle**. Hvis arbejderens tilknytning til en gruppe bør begrænses til en bestemt periode, skal du bruge felterne **Gyldig** og **Udløb** til at definere perioden.
7. I oversigtspanelet **Arbejdssteder** skal du vælge **Tilføj** og derefter vælge et arbejdssted for vedligeholdelsesarbejderen. Angiv også, hvilket sted der er arbejderens primære arbejdssted.

    > [!NOTE]
    > Når du føjer arbejdssteder til en arbejder, vises alle aktive aktiver, der er relateret til disse arbejdssteder, på forskellige menupunkter såsom **Mine aktive aktiver** og **Mine aktive arbejdssteder**. De fremgår også af de opslag i aktiver, der vises, når du opretter et nyt aktiv, en vedligeholdelsesanmodning eller en arbejdsordre.

    Felterne i oversigtspanelet **Detaljer** viser antallet af vedligeholdelsesarbejdergrupper og de arbejdssteder, som den valgte vedligeholdelsesarbejder er relateret til.

## <a name="create-worker-groups"></a>Opret arbejdergrupper

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdere** \> **Vedligeholdelsesarbejdergrupper**.
2. Vælg **Ny** for at føje en arbejdergruppe til listen.
3. I feltet **Vedligeholdelsesarbejdergruppe** skal du indtaste et ID for gruppen.
4. Indtast et navn i feltet **Navn**.
5. I oversigtspanelet **Arbejdere** skal du vælge **Tilføj** og derefter vælge en vedligeholdelsesarbejder for arbejdergruppen. Yderligere oplysninger om felterne **Gyldig** og **Udløb** finder du i trin 6 i den forrige procedure.
6. Hvis en ressourcegruppe skal relateres til den valgte vedligeholdelsesarbejdergruppe, skal du vælge **Kopiér fra ressourcegruppe**. Vælg den ressourcegruppe, du vil kopiere kalenderindstillinger fra, i feltet **Gruppe**. I feltet **Arbejdergruppe** skal du derefter vælge den arbejdergruppe, som ressourcegruppens kalenderindstillinger skal kopieres til. Dette trin er kun relevant, hvis du ønsker, at vedligeholdelsesarbejderne skal bruge den kalender, der er relateret til en ressource (arbejdscenter) under planlægningen af arbejdsordren.

    Feltet i oversigtspanelet **Detaljer** viser antallet af vedligeholdelsesarbejdere, som er blevet konfigureret for den valgte vedligeholdelsesarbejder.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]