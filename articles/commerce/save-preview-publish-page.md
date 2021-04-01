---
title: Gemme, få vist og udgive en side
description: Dette emne beskriver, hvordan du gemmer, ser forhåndsvisning af og udgiver en side i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 68fec8c2ddc05c71394045351cef880361f2e306
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254811"
---
# <a name="save-preview-and-publish-a-page"></a>Gemme, se prøveversion og udgive en side

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du gemmer, ser forhåndsvisning af og udgiver en side i Microsoft Dynamics 365 Commerce.

## <a name="save-a-page"></a>Gemme en side

Hvis du vil gemme en side, skal du selv have den tjekket ud til dig selv og åbnet den i sideeditoren. Vælg **Rediger** på kommandolinjen for at tjekke siden ud. Du bør gemme den straks efter, at du har redigeret den, for at sikre, at ændringerne bevares.

Når du gemmer en side, er ændringerne kun synlige for dig. Gemmehandlingen er primært beregnet til at gemme ændringer, mens siden endnu ikke er klar til at blive tjekket ind. Når du er færdig med at redigere siden, anbefales du at tjekke den ind, så ændringerne bliver synlige for andre. På dette tidspunkt kan siden også være tjekket ud af andre brugere, der skal redigere den.

## <a name="preview-a-page"></a>Se forhåndsvisning af en side

Oprettelsesværktøjet indeholder to slags funktioner til forhåndsvisning: den visuelle sidegenerator, som er en "what you see is what you get"-eksempelrude (WYSIWYG), og et separat eksempelvindue.

Mens du bruger sideeditoren, er der en "what you see is what you get"-forhåndsvisning (WYSIWYG) i den midterste rude. Denne forhåndsvisning opdateres automatisk, hver gang du gemmer siden. Du kan også opdatere den manuelt ved at vælge **Opdater** på kommandolinjen. I forhåndsvisningen gengives siden, som webstedets brugere kan se den, men hjælpefunktioner vises oven på den.

Når du er færdig med at redigere siden, kan det være en god ide at se forhåndsvisningen for at se, hvad kunderne kan se. Hvis du vil se forhåndsvisningen, skal du vælge **Forhåndsvisning** på kommandolinjen. Forhåndsvisningen åbnes i et separat browservindue. Siden i vinduet med forhåndsvisning gengives på samme måde, som webstedets bruger kan se den. Du kan ændre størrelsen på vinduet for at sikre, at dynamiske moduler gengives korrekt i alle visninger.

> [!NOTE]
> Der kræves godkendelse og korrekte tilladelser for at se en forhåndsvisning af indhold, der ikke er udgivet. Hvis du derfor deler URL-adressen til forhåndsvisningen med en anden, skal den pågældende person have de relevante rettigheder for at få adgang til indholdet.

## <a name="publish-a-page"></a>Udgive en side

Når siden er færdig, er næste trin at udgive den, så eksterne brugere kan få vist indholdet. Før du kan udgive en side, skal du tjekke den ind ved at vælge **Afslut redigering** på kommandolinjen.

Du kan udgive og annullere udgivelsen af sider fra enten sidefremviseren eller sideeditoren. Sideeditoren viser en liste over sider og tillader massehandlinger. Sideeditoren kan kun bruges til at udgive eller annullere udgivelsen af en enkelt side, der er åben i den.

Hvis du vil udgive en eller flere sider fra sidefremviseren, skal du vælge siderne, kontrollere, at de er tjekket ind, og derefter vælge **Publicer** på kommandolinjen. Siderne udgives, og du modtager en besked om handlingen i oprettelsesværktøjet.

Hvis du vil udgive en enkelt side fra sideeditoren, er proceduren den samme. Mens siden er åben i sideeditoren, skal du kontrollere, at den er tjekket ind, og derefter vælge **Publicer** på kommandolinjen. Siden udgives, og du modtager en besked om handlingen.

Når du udgiver en side, udgives kun sidens indhold. Du og andre brugere kan først gå til siden og se den, når der er knyttet en URL-adresse til den. URL-adressen skal udgives separat.

> [!IMPORTANT]
> Før du kan udgive en side, skal alle de billeder eller fragmenter, som siden refererer til, allerede være publiceret.

## <a name="save-preview-and-publish-a-home-page"></a>Gemme, se forhåndsvisning af og udgive en startside

Hvis du vil gemme, se forhåndsvisning af og udgive en startside, skal du følge disse trin.

1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **Sider** i navigationsruden til venstre.
1. Find og vælg startsiden for at åbne den i sideeditoren.
1. Vælg **Rediger**.
1. Rediger siden efter behov.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Brug feltet **Bemærkninger** til at skrive en note om de ændringer, du har foretaget, og vælg derefter **OK**.
1. Vælg **Eksempel** for at få vist din side. Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.
1. Vælg **Publicer**.

## <a name="publish-a-url"></a>Publicere en URL-adresse

Følg disse trin for at publicere en URL-adresse.

1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **URL-adresser** i navigationsruden til venstre.
1. Find og vælg den URL-adresse, der skal publiceres.
1. Vælg **Publicer** på kommandolinjen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Forbedre en produktside](enrich-product-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)

[Bekræfte tilgængelighed af sideindhold](verify-accessibility.md)

[Oprette dynamiske e-handelssider baseret på URL-parametre](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]