---
title: Bygge brugerdefinerede svarsider for 4xx/5xx statuskodefejl
description: I dette emne beskrives, hvordan du bygger tilpassede svarsider for 4xx- og 5xx-statuskodefejl ved hjælp af oprettelsesværktøjerne i Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799635"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Bygge brugerdefinerede svarsider for 4xx/5xx statuskodefejl

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du bygger tilpassede svarsider for 4xx- og 5xx-statuskodefejl ved hjælp af oprettelsesværktøjerne i Microsoft Dynamics 365 Commerce.

Hvis en anmodning ikke lykkes, udsteder serveren fejlsvar med HTTP-statuskode. Statuskoden 404 registreres og returneres, hvis der ikke bliver fundet en side, og statuskoden 500 registreres og returneres, hvis der opstår en serverfejl. I Dynamics 365 Commerce kan programbrugere opbygge brugerdefinerede fejlsvarsider med statuskode, der vises for brugere af disse statuskodefejlsvar.

## <a name="build-a-status-code-error-response-page"></a>Oprette en svarside for statuskodefejl

Udfør følgende trin for at begynde at opbygge en svarside for statuskodefejl.

1. Log på Dynamics 365 Commerce i din foretrukne webbrowser. 
1. Vælg det websted, du vil bygge en svarside for 4xx/5xx statuskodefejl for.

### <a name="build-the-template"></a>Opbygge skabelonen

Udfør følgende trin for at begynde at opbygge skabelonen for svarsiden for statuskodefejl.

1. Gå til **Skabeloner**.
1. Vælg **Ny** for at oprette en sideskabelon.
1. Angiv et navn til den nye skabelon under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.
1. Opret skabelonen på basis af den struktur, som du ønsker, at svarsiden for statuskodefejlen skal have.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den. 

### <a name="build-the-status-code-error-response-page"></a>Oprette svarsiden for statuskodefejl

Udfør følgende trin for at opbygge svarsiden for statuskodefejl.

1. Gå til **Sider**.
1. Vælg **Ny** for at oprette en side.
1. Vælg en skabelon i dialogboksen **Vælg en skabelon**, og angiv derefter navnet på svarsiden for statuskodefejl under **Sidenavn**. Lad feltet **Sidens URL-adresse** stå tomt.
1. Opbyg siden.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

> [!NOTE]
> Du kan oprette separate svarsider for statuskodefejl 4xx og 5xx. Du kan også bruge den samme generelle svarside for statuskodefejl til begge fejlkategorier.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Konfigurere en omdirigering for svarside for statuskodefejl

Udfør følgende trin for at konfigurere en omdirigering for svarsiden for statuskodefejl.

1. Gå til **URL-adresser \> Ny \> Nyt alias**, og vælg den svarside for statuskodefejl, du har opbygget tidligere.
1. I feltet **Alias** skal du enten angive **standard-4xx** eller **standard-5xx**, afhængigt af svarsiden for statuskodefejl, som du vil konfigurere en omdirigering for. Disse aliasser skal publiceres. Ellers vil omdirigeringen ikke fungere.
1. Vælg **OK** for at oprette tilknytningen.

> [!NOTE]
> Hvis du bruger en enkelt svarside for statuskodefejl til begge fejlkategorier, skal du gentage denne procedure for at sammenkæde et alias for den anden fejlkategori med den samme side.

## <a name="additional-resources"></a>Yderligere ressourcer

[Arbejde med skabeloner](work-with-templates.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Oprette en side-URL](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
