---
title: Arbejde med forudindstillede layout
description: Dette emne beskriver, hvordan du kan arbejde med forudindstillede layout i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 57dc0de64ce7536cf70c1f277d5212c3b8dd7480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009587"
---
# <a name="work-with-preset-layouts"></a>Arbejde med forudindstillede layout


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du kan arbejde med forudindstillede layout i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Før du fuldfører procedurerne i dette emne, skal du sørge for at læse [Forudindstillede og brugerdefinerede layout](templates-layouts-overview.md#preset-and-custom-layouts). Du kan finde en generel oversigt under [Oversigt over skabeloner og layout](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Oprette et nyt forudindstillet layout

Der findes to metoder til oprettelse af et forudindstillet layout. Du kan gemme et eksisterende brugerdefineret layout som et nyt forudindstillet layout, eller du kan oprette et forudindstillet layout fra bunden.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Oprette et forudindstillet layout ud fra et eksisterende brugerdefineret layout

Du kan oprette et forudindstillet layout ud fra et eksisterende brugerdefineret layout ved at følge disse trin.

1. Åbn en eksisterende side, der ikke aktuelt bruger et foruddefineret layout, og som har en modulstruktur, du vil genbruge til andre sider på webstedet.
1. Vælg **Rediger** for at tjekke siden ud.
1. Vælg **Gem som nyt layout**. Dialogboksen **Gem som nyt layout** vises.
1. Indtast et navn og en beskrivelse til det forudindstillede layout. De værdier, du angiver, vises for andre forfattere, når de opretter nye sider ud fra dit layout eller skifter til det. Angiv derfor værdier, der vil være nyttige for sideforfattere.
1. Vælg **OK**.

Det forudindstillede layout er nu tilgængeligt, når du opretter nye sider eller vælger et andet layout for en side i samme skabelonhierarki.

> [!TIP]
> Hvis du hurtigt vil se, om en bestemt side i øjeblikket er bundet til et foruddefineret layout, skal du vælge siden i listevisningen af sider og undersøge metadata til layout i egenskabsruden til højre.

### <a name="create-a-new-preset-layout"></a>Oprette et nyt forudindstillet layout

Du kan oprette et forudindstillet layout fra bunden ved at følge disse trin.

1. Vælg **Layout** i navigationsruden til venstre.
1. Vælg **Nyt layout**. Dialogboksen **Nyt layout** vises.
1. Vælg den skabelon, der skal bruges til dit forudindstillede layout.
1. Indtast et navn og en beskrivelse til det forudindstillede layout. De værdier, du angiver, vises for andre forfattere, når de opretter nye sider ud fra dit layout eller skifter til det. Angiv derfor værdier, der vil være nyttige for sideforfattere.
1. Vælg **OK** for at oprette det nye forudindstillede layout og åbne layouteditoren.
1. Tilføj og konfigurer moduler ved hjælp af dispositionstræet til venstre og egenskabsruden til højre i layouteditoren. (Processen minder om processen for tilføjelse og konfiguration af moduler til en skabelon i skabeloneditoren). Placeringen af moduler og eventuelle låste standardindstillinger bliver den centraliserede modulkonfiguration for alle de sider, der bruger dette foruddefinerede layout.

## <a name="modify-a-preset-layout"></a>Redigere et forudindstillet layout

Benyt følgende fremgangsmåde for at redigere et forudindstillet layout.

1. Vælg **Layout** i navigationsruden til venstre.
1. Vælg det modul, der skal redigeres, i dispositionstræet til venstre i layouteditoren. Udfør derefter ethvert af følgende trin:

    - Hvis du vil flytte et modul op eller ned inden for det overordnede objekt, skal du vælge ellipseknappen (**...**) for modulet og vælge **Flyt op** eller **Flyt ned**.
    - Hvis du vil ændre standardindstillingerne i et modul, skal du bruge egenskabsruden til at angive standardværdier og derefter låse dem til alle downstream-sider.
    - Hvis du vil føje nye moduler eller fragmenter til containermoduler, skal du vælge ellipseknappen og derefter vælge **Tilføj modul** eller **Tilføj fragment**.
    - Hvis du vil fjerne et modul fra layoutet, skal du vælge ellipseknappen og derefter vælge **Slet**.

## <a name="change-a-preset-layout-theme"></a>Ændre et forudindstillet layouttema

En typisk praksis er at angive et standardtema for alle sider, der bruger et forudindstillet layout.

Hvis du vil angive eller ændre temaet for alle de underordnede sider, der bruger det forudindstillede layout, skal du følge disse trin.

1. Vælg sidecontainermodulet i dispositionstræet til venstre i layouteditoren. (Dette modul er typisk den anden node og hedder **Standardside**).
1. Vælg et tema i feltet **Tema** i egenskabsruden til højre.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Gemme, checke ind, se forhåndsvisning af og publicere et forudindstillet layout

Følg disse trin for at gemme og checke dit forudindstillede layout ind.

1. Vælg **Gem** øverst i layouteditoren. Gemte ændringer påvirker ikke downstream-sider, før de er checket ind.
1. Vælg **Afslut redigering**. Dine ændringer er nu synlige for downstream-arbejdsgange.

Hvis du vil se ændringerne på forhånd, skal du enten åbne en eksisterende side, der bruger det forudindstillede layout, eller oprette en ny side ud fra layoutet.

Når du har set ændringerne af det forudindstillede layout, skal du følge et af disse trin for at publicere layoutet til dit aktive websted:

* Gå til **Layout**, vælg layoutet, og vælg derefter **Publicer**.
* Vælg layoutnavnet for at åbne layouteditoren, og vælg derefter **Publicer**.
* Publicer en side, der refererer til det ikke-publicerede layout. Layoutet vil automatisk blive publiceret.

> [!WARNING]
> Der kan refereres til forudindstillede layout fra flere sider. Når du publicerer et forudindstillet layout, skal du være opmærksom på, at du kan påvirke layoutet af flere sider.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Arbejde med skabeloner](work-with-templates.md)
