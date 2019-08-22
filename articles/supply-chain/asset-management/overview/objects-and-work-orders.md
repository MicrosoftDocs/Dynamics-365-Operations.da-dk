---
title: Aktiver og arbejdsordrer
description: I dette emne beskrives aktiver og arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783148"
---
# <a name="assets-and-work-orders"></a>Aktiver og arbejdsordrer

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I dette emne beskrives aktiver og arbejdsordrer i Styring af aktiver. Aktiver og arbejdsordrer er de centrale dele af Styring af aktiver. Et *Aktiv* er en maskine eller en maskindel, der kræver kontinuerlig vedligeholdelse og service. Aktiver kan oprettes i en hierarkisk struktur, og de kan relateres til arbejdssteder. Vedligeholdelsesjob kan planlægges på alle niveauer i aktivstrukturen.

Der oprettes forskellige data, såsom produktoplysninger og aktivspecifikation samt påkrævede vedligeholdelsesplaner, for hvert aktiv. I følgende illustration vises en oversigt over aktivdata og tilknytningen af aktiver til jobtyper. Rød tekst bruges til eksempler, der viser nedarvning og afhængigheder.

![Figur 1](media/05-overview-image.png)

Hver arbejdsordre har en arbejdsordretype, såsom forebyggende vedligeholdelse, korrigerende vedligeholdelse eller inspektion. Arbejdsordren indeholder et eller flere arbejdsordrejob. Alle arbejdsordrejob definerer et job, der skal udføres på et aktiv og en relateret jobtype. Eksempler på relaterede jobtyper omfatter 10.000 km, 50.000 km, 1 års eftersyn og sikkerhedsinspektion. En arbejdsordre kan relateres til flere aktiver.

I følgende illustration vises en oversigt over nøgledataene i en arbejdsordre.

![Figur 2](media/06-overview-image.png)

En arbejdsordre kan relateres til en anden arbejdsordre, og jobtyper kan indeholde efterfølgende job, der opretter en arbejdsordre. Generelt er der ingen afhængigheder mellem arbejdsordrer. Derfor kan arbejdsordrene ændre deres livscyklustilstand og planlægges uafhængigt af hinanden.

Arbejdsordrer kan oprettes på forskellige måder, der er relateret til korrigerende, forebyggende eller proaktiv vedligeholdelse. Du kan også oprette arbejdsordre manuelt. I følgende illustration vises en oversigt over processen for automatisk eller manuel oprettelse af arbejdsordrer.

![Figur 3](media/07-overview-image.png)

Adskillige trin skal fuldføres, når du vil planlægge og køre et vedligholdelsesjob på en arbejdsordre. I følgende illustration vises en oversigt over processen for en arbejdsordre.

![Figur 4](media/08-overview-image.png)

> [!NOTE]
> Når du generelt arbejder i Microsoft Dynamics 365 for Finance and Operations og modulet **Styring af aktiver**, skal du vælge **Ny** for at oprette en ny post, **Rediger** for at opdatere en eksisterende post og **Gem** for at gemme nye eller redigerede data.
