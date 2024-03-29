---
title: Tilføje en ny webstedsside
description: Denne artikel indeholder en beskrivelse af, hvordan du tilføjer en ny side på et websted i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f6714463c9d5dc844b03f78f0f6ff60c5f270da3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270312"
---
# <a name="add-a-new-site-page"></a>Tilføje en ny webstedsside

[!include [banner](includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du tilføjer en ny side på et websted i Microsoft Dynamics 365 Commerce.

Når du har oprettet skabeloner og fragmenter til dit websted, er næste trin at starte med at oprette sider, der bruger dem. For at komme i gang skal du vælge en skabelon eller et layout, et sidenavn og en side-URL-adresse.

## <a name="template-or-layout"></a>Skabelon eller layout

Du kan enten bruge en skabelon eller et layout til din nye side. Du kan finde flere oplysninger under [Oversigt over skabeloner og layout](templates-layouts-overview.md).

## <a name="specify-the-page-name"></a>Angive sidenavnet

Sidenavnet skal være entydigt for dit websted og være sigende, så du nemt kan finde siden, og så andre personer ved, hvad formålet med siden er. Du kan omdøbe siden senere ved at redigere den og derefter vælge blyantssymbolet ud for sidenavnet i egenskabsruden.

## <a name="specify-the-page-url"></a>Angive sidens URL-adresse

Du kan vælge at angive en URL-adresse til den nye side. Når du opretter en side, kan du angive en streng, der bruges til at danne en komplet URL-adresse. Denne streng kaldes også en relativ URL-adresse eller en URL-slug. Der genereres derefter en komplet URL-adresse ud fra URL-sluggen, og den nye side tildeles til den. Du kan ændre URL-sluggen senere, før du publicerer siden. Du kan finde flere oplysninger i [Oprette en side-URL](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce frakobler URL-adresser og indhold. Med andre ord kan der oprettes en side, der ikke er knyttet til en URL-adresse, og der kan oprettes en URL-adresse, som ikke er knyttet til en side. Derfor kan der foretages indholdsswapping for en URL-adresse, uden at det kræver nedetid, og omdirigeringer er nemmere at administrere.

## <a name="add-a-new-page"></a>Tilføje en ny side

Hvis du vil føje en ny side til dit websted, skal du følge disse trin.

1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **Ny side**.
1. I dialogboksen **Ny side** skal du vælge en skabelon og derefter vælge **OK**.
1. I feltet **Sidenavn** skal du indtaste et sidenavn (f.eks. **Min nye side**).
1. I feltet **URL-adresse** skal du indtaste en streng (URL-slug) for at fuldføre URL-adressen (f.eks. **minnyeside**).
1. Vælg **OK**. Sideeditoren vises. Bemærk, at der automatisk føjes et sidehoved og en sidefod til siden baseret på den skabelon, du har valgt.
1. Vælg pladsen **Hoved** i sidedispositionen, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. Vælg **Container**, og vælg derefter **OK**.
1. Vælg **Flydende container**, vælg ellipseknappen, og vælg derefter **Tilføj modul**.
1. Vælg **Indholdsrig blok**, og vælg derefter **OK**.
1. Vælg **Indholdsrig blok**, vælg ellipseknappen, og vælg derefter **Tilføj modul**.
1. Vælg **Element for indholdsrig blok**, og vælg derefter **OK**.
1. I egenskabsruden til højre skal du vælge **Afsnit** og derefter angive **Min testtekst** i feltet.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Angiv **Tilføjet ny side** i feltet **Kommentarer**, og vælg derefter **OK**.
1. Vælg **Eksempel** for at få vist din side. Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.
1. Vælg **Publicer**.
1. Vælg **Fabrikam** (eller navnet på dit websted) i navigationsstien (brødkrummer).
1. Vælg **URL-adresser** i navigationsruden til venstre.
1. Find og vælg din URL-adresse (**minnyeside**) på listen.
1. Vælg **Publicer**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)

[Bekræfte tilgængelighed af sideindhold](verify-accessibility.md)

[Oprette dynamiske e-handelssider baseret på URL-parametre](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
