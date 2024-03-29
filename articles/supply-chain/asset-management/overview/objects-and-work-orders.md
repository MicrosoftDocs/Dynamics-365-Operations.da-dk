---
title: Aktiver og arbejdsordrer
description: Denne artikel beskriver aktiver og arbejdsordrer i Styring af aktiver.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df2d0fcc5162900ad2ad67f2629d14015f694bd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869685"
---
# <a name="assets-and-work-orders"></a>Aktiver og arbejdsordrer

[!include [banner](../../includes/banner.md)]

 

Denne artikel beskriver aktiver og arbejdsordrer i Styring af aktiver. Aktiver og arbejdsordrer er de centrale dele af Styring af aktiver. Et *Aktiv* er en maskine eller en maskindel, der kræver kontinuerlig vedligeholdelse og service. Aktiver kan oprettes i en hierarkisk struktur, og de kan relateres til arbejdssteder. Vedligeholdelsesjob kan planlægges på alle niveauer i aktivstrukturen.

Der oprettes forskellige data, såsom produktoplysninger og aktivspecifikation samt påkrævede vedligeholdelsesplaner, for hvert aktiv. I følgende illustration vises en oversigt over aktivdata og tilknytningen af aktiver til jobtyper. Rød tekst bruges til eksempler, der viser nedarvning og afhængigheder.

![Diagram, der viser aktivdata vedrørende jobtyper.](media/05-overview-image.png)

Hver arbejdsordre har en arbejdsordretype, såsom forebyggende vedligeholdelse, korrigerende vedligeholdelse eller inspektion. Arbejdsordren indeholder et eller flere arbejdsordrejob. Alle arbejdsordrejob definerer et job, der skal udføres på et aktiv og en relateret jobtype. Eksempler på relaterede jobtyper omfatter 10.000 km, 50.000 km, 1 års eftersyn og sikkerhedsinspektion. En arbejdsordre kan relateres til flere aktiver.

I følgende illustration vises en oversigt over nøgledataene i en arbejdsordre.

![Diagram, der viser nøgledata i en arbejdsordre.](media/06-overview-image.png)

En arbejdsordre kan relateres til en anden arbejdsordre, og jobtyper kan indeholde efterfølgende job, der opretter en arbejdsordre. Generelt er der ingen afhængigheder mellem arbejdsordrer. Derfor kan arbejdsordrene ændre deres livscyklustilstand og planlægges uafhængigt af hinanden.

Arbejdsordrer kan oprettes på forskellige måder, der er relateret til korrigerende, forebyggende eller proaktiv vedligeholdelse. Du kan også oprette arbejdsordre manuelt. I følgende illustration vises en oversigt over processen for automatisk eller manuel oprettelse af arbejdsordrer.

![Diagram, der viser automatisk eller manuel oprettelse af arbejdsordrer.](media/07-overview-image.png)

Adskillige trin skal fuldføres, når du vil planlægge og køre et vedligholdelsesjob på en arbejdsordre. I følgende illustration vises en oversigt over processen for en arbejdsordre.

![Diagram, der viser oversigt over behandling af en arbejdsordre.](media/08-overview-image.png)

> [!NOTE]
> Når du generelt arbejder i Dynamics 365 Supply Chain Management og modulet **Styring af aktiver**, skal du vælge **Ny** for at oprette en ny post, **Rediger** for at opdatere en eksisterende post og **Gem** for at gemme nye eller redigerede data.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]