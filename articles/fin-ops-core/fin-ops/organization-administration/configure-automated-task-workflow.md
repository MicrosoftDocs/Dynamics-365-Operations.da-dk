---
title: Konfigurere automatiserede opgaver i en arbejdsgang
description: Denne artikel forklarer, hvordan du konfigurerer egenskaberne for en automatiseret opgave.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b482338c436ea9226d31f74c823ee1dc141b24cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891747"
---
# <a name="configure-automated-tasks-in-a-workflow"></a>Konfigurere automatiserede opgaver i en arbejdsgang

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikel forklarer, hvordan du konfigurerer egenskaberne for en automatiseret opgave.

Hvis du vil konfigurere en automatiseret opgave i arbejdsgangseditoren, skal du højreklikke på opgaven og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**. Brug derefter følgende procedurer for at konfigurere egenskaberne for den automatiserede opgave.

## <a name="name-the-task"></a>Navngive opgaven

Udfør følgende trin for at angive et navn på den automatiserede opgave.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. Angiv et entydigt navn til opgaven i feltet **Navn**.

## <a name="specify-when-notifications-are-sent"></a>Angive, hvornår beskeder sendes

Du kan sende beskeder til personer, når en automatiseret opgave er afviklet eller annulleret. Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem de sendes til.

1. Klik på **Beskeder** i ruden til venstre.
2. Markér afkrydsningsfeltet ud for de hændelser, der skal sendes beskeder i forbindelse med.

    - **Udførelse** – der sendes beskeder, når opgaven er afviklet.
    - **Annulleret** – der sendes beskeder, når opgaven er annulleret.

3. Vælg rækken for den hændelse, du har valgt i trin 2.
4. Indtast teksten til beskeden i tekstfeltet på fanen **Beskedtekst**.
5. Hvis du vil personalisere beskeden, kan du indsætte pladsholdere. Pladsholderne erstattes med de relevante data, når beskeden vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.

    1. I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.
    2. Klik på **Indsæt pladsholder**.
    3. Vælg den pladsholder, du vil indsætte, på den viste liste.
    4. Klik på **Indsæt**.

6. Følg disse trin for at tilføje oversættelser af beskeden:

    1. Klik på **Oversættelser**.
    2. Klik på **Tilføj** på den viste side.
    3. På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4. Indtast teksten i feltet **Oversat tekst**.
    5. Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 5.
    6. Klik på **Luk**.

7. På fanen **Modtager** skal du angive, hvem beskederne skal sendes til. Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 8.

    <table>
    <thead>
    <tr>
    <th>Indstilling</th>
    <th>Modtagere af besked</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deltager</td>
    <td>Brugere, som er tildelt til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</li>
    <li>Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbejdsgangsbruger</td>
    <td>Brugere, som deltager i den aktuelle arbejdsgang</td>
    <td>
    <ul>
    <li>Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruger</td>
    <td>Specifikke brugere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere. Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Gentag trin 3 til 7 for hvert af de hændelser, du har valgt i trin 2.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]