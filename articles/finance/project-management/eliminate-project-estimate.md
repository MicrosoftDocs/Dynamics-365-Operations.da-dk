---
title: Eliminere et projektestimat
description: Dette emne indeholder oplysninger om eliminering af et projektestimat, efter at det er færdigt.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410202"
---
# <a name="eliminate-a-project-estimate"></a>Eliminere et projektestimat

[!include [banner](../includes/banner.md)]

Projektestimater giver den økonomiske visning for arbejde, der er forkalkuleret og planlagt for et projekt. For at arbejde med estimater for et projekt, skal projektet knyttes til et forkalkuleret projekt. Et forkalkuleret projekt er altid baseret på et eksisterende projekt, men flere projekter kan referere til et enkelt forkalkuleret projekt. Der kan kun knyttes fastpris- og investeringsprojekter til forkalkulerede projekter, og de pågældende projekter skal tilhøre samme projektgruppe som det forkalkulerede projekt.

Hvis du vil eliminere et forkalkuleret projekt, skal dette være færdigt. I følgende fremgangsmåde beskrives det, hvordan du eliminerer et estimat.

1. Gå til **Projektstyring og regnskab** > **Alle projekter**, og åbn projektet. 
2. På fanen **Administrer** skal du vælge **Estimater** og på siden **Estimat** skal du vælge **Eliminer**.
3. På siden **Eliminer estimat** på fanen **Generelt** skal du væge følgende indstillinger:

   - **Periodekode**: Vælg den periodekode, som skal vælge de forkalkulerede projekter. 
   - **Estimatdato**: Vælg estimatdatoen for eliminering.
   - **Eliminer med IGVA-advarsler**: Aktivér denne indstilling for at give besked, når et estimat, der er tilknyttet et igangværende arbejde (IGVA), elimineres. Hvis denne indstilling ikke er aktiveret, kan elimineringen ikke fortsætte, hvis der findes posteringer, som ikke er estimerede. 
   > [!NOTE]
   > Denne indstilling er kun tilgængelig, hvis eliminering anvendes på et forkalkuleret projekt. Den er ikke tilgængelig, hvis du anvender periodiske posteringer. Denne indstilling fungerer sammen med indstillingerne på fanen **Estimat** på siden **Projektparametre** i feltgruppen **Tillad eliminering, når der findes ikke-forkalkulerede posteringer**.
   - **Indstil stadie til Færdig**: Aktivér denne indstilling for at angive det forkalkulerede projeks stadie til **Færdig,** når du har kørt elimineringen.
   - **Udskriv estimatliste**: Vælg de oplysninger, som skal medtages, når estimatlisten udskrives.
   - **Vis infolog**: Aktivér denne indstilling for at få vist infologgen.
   - **Bogføringsdato**: Vælg estimatets finansbogføringsdato.

4.  Vælg **OK**.
5. Når elimineringsprocessen er færdig, vises det eliminerede forkalkulerede projekt med en negativ værdi. 

Hvis du ikke har tænkt dig at eliminere et estimat, kan du vælge det eliminerede estimat og vælge **Tilbagefør eliminering**.   
