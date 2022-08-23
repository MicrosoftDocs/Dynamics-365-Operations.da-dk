---
title: Oprette dynamiske e-handelssider baseret på URL-parametre
description: Denne artikel beskriver, hvordan du kan konfigurere en Microsoft Dynamics 365 Commerce-e-handelsside, der kan have dynamisk indhold baseret på URL-parametre.
author: bicyclingfool
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: 718bc099347f2924b299ccd4562d9d7055c43187
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282870"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Oprette dynamiske e-handelssider baseret på URL-parametre

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du kan konfigurere en Microsoft Dynamics 365 Commerce-e-handelsside, der kan have dynamisk indhold baseret på URL-parametre.

En e-handelsside kan konfigureres til at have forskelligt indhold baseret på et segment i URL-stien. Derfor kaldes siden for en dynamisk side. Segmentet bruges som parameter til at hente sideindholdet. Hvis der f.eks. oprettes en side i webstedsgeneratoren med navnet **blog\_fremviser**, bliver den tilknyttet URL-adressen `https://fabrikam.com/blog`. Denne side kan derefter bruges til at vise forskelligt indhold baseret på det sidste segment i URL-stien. Det sidste segment i URL-adressen er f.eks. `https://fabrikam.com/blog/article-1` **artikel-1**.

Du kan også tilsidesætte et parameteriseret URL-segment med en side i webstedsgeneratoren. Hvis der f.eks. oprettes en side i webstedsgeneratoren med navnet **blog\_oversigt**, kan den tilknyttes URL-adressen `https://fabrikam.com/blog/about-this-blog`. Når der anmodes om URL-adressen `https://fabrikam.com/blog` med segmentet `/about-this-blog` i slutningen, returneres sideindholdet af **blog\_oversigt** i stedet for det `/about-this-blog`-segment, der fortolkes som en parameter, der skal bruges af siden `https://fabrikam.com/blog`. 

Når du vælger navne for de parametre, der skal overføres til den dynamiske side, kan navnet på den dynamiske side, som det vises i URL-adressen (`/blog` i eksemplet ovenfor) ikke bruges som et parameternavn eller en understreng af et parameternavn. 

> [!NOTE]
> Funktionerne til modtagelse, hentning og visning af dynamisk sideindhold implementeres ved hjælp af et brugerdefineret modul. Du kan finde flere oplysninger i [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Konfigurere en dynamisk e-handelsside

Hvis du vil konfigurere en dynamisk e-handelsside, skal du oprette den dynamiske side, oprette den grundlæggende URL-adresse og konfigurere ruten til den dynamiske side.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Opret den side, der kan vise dynamisk indhold

Hvis du vil oprette en side, der kan vise dynamisk indhold, skal du følge trinnene i [Tilføj en ny webstedsside](add-new-page.md). Den side, du opretter, kræver implementering af et modul, der bruger det sidste segment i URL-stien til at hente indhold fra en ekstern datakilde. Yderligere oplysninger om brugerdefineret moduludvikling finder du i [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Oprette basis-URL-adressen til den dynamiske side

Hvis du vil oprette basis-URL-adressen til den dynamiske side i Commerce-webstedsgenerator, skal du følge disse trin.

1. Gå til **URL**-adresser, og vælg **Ny \> Ny URL**-adresse.
1. I dialogboksen **Opret ny URL-adresse** vælges **Intern side**. Angiv den **URL-sti**, der skal fungere som rod for den dynamiske side (i dette eksempel **/blog**). Vælg derefter **Næste**.
1. I dialogboksen **Vælg en side** vælges den side, der blev oprettet som dynamisk side, og vælg derefter **Gem**.
1. Vælg **Publicer**.

### <a name="configure-the-route-to-the-dynamic-page"></a>Konfigurere ruten til den dynamiske side

Hvis du vil konfigurere ruten til den dynamiske side i Commerce-webstedsgenerator, skal du følge disse trin.

1. Gå til **Webstedsindstillinger \> Udvidelser**.
1. Under **Parameteriserede URL-stier** skal du vælge **Tilføj** og derefter angive den URL-sti, du angav, da du oprettede URL-adressen (i dette eksempel, **/blog**).
1. Vælg **Gem og udgiv**.

Når ruten er konfigureret, returnerer alle anmodninger til den parameteriserede URL-sti den side, der er knyttet til URL-adressen. Hvis en anmodning indeholder et yderligere segment, returneres den tilknyttede side, og sideindholdet hentes ved hjælp af segmentet som parameter. F.eks. vil `https://fabrikam.com/blog/article-1` returnere siden `https://fabrikam.com/blog`, der viser indholdet, som er hentet ved hjælp af parameteren **/article-1**.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Tilsidesætte en parameteriseret URL-adresse med en brugerdefineret side

Hvis du vil tilsidesætte en parameteriseret URL-adresse med en brugerdefineret side i Commerce-webstedsgenerator, skal du følge disse trin.

1. Gå til **URL**-adresser, og vælg **Ny \> Ny URL**-adresse.
1. I dialogboksen **Opret ny URL-adresse** vælges **Intern side**. Under **URL-stien** skal du angive den sti, der indeholder det segment, der skal tilsidesættes (i dette eksempel **/blog/about-this-blog**). Vælg derefter **Næste**.
1. I dialogboksen **Vælg en side** vælges den brugerdefinerede side, og derefter vælges **Gem**.
1. Vælg **Publicer**.
1. Hvis den brugerdefinerede side endnu ikke er publiceret, skal du gå til **Sider**, vælge den brugerdefinerede side og derefter vælge **Udgiv**.

Når den brugerdefinerede side er publiceret, vises den i stedet for den dynamiske side, der har parameteriseret indhold.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Gemme, se prøveversion og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)

[Bekræfte tilgængelighed af sideindhold](verify-accessibility.md)

[Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
