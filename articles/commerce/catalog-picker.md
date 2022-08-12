---
title: Modul til katalogvælger
description: Denne artikel indeholder oplysninger om katalogplukkere og beskriver, hvordan du kan føje dem til Microsoft Dynamics 365 Commerce B2B-e-handelswebsteder (Business-To-Business).
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136939"
---
# <a name="catalog-picker-module"></a>Modul til katalogvælger

[!include [banner](includes/banner.md)]

Denne artikel indeholder oplysninger om katalogplukkere og beskriver, hvordan du kan føje dem til Microsoft Dynamics 365 Commerce B2B-e-handelswebsteder (Business-To-Business).

Et katalogplukkermodul er en speciel container, der bruges til at få vist alle de produktkataloger, der er tilgængelige for B2B-webstedsbrugere til indkøb. Flere kataloger understøttes i øjeblikket kun for B2B-websteder.

Følgende illustration viser et eksempel på et katalogplukkermodul.

![Eksempel på et katalogplukkermodul, der indeholder tre produktkataloger.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Føje et katalogplukkermodul til en side

Hvis du vil tilføje et katalogplukkermodul til websiden i Commerce-webstedsgenerator, skal du følge disse trin.

### <a name="create-a-catalog-picker-page"></a>Oprette en side til katalogplukker

Opret første en side til katalogplukker.

1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Opret en ny side** skal du angive **Katalogplukker** under **Sidenavn**.
1. Under **Side-URL** skal du angive en URL for siden og vælge **Næste**.

    ![Dialogboksen Opret ny side.](./media/Create-catalog-picker-page.png)

1. Vælg **Generelt indhold** under **Vælg en skabelon**, og vælg derefter **Næste**.
1. Vælg **Fleksibelt layout** under **Vælg layout**, og vælg derefter **Næste**.
1. Gennemse sidekonfigurationen under **Gennemse og afslut**. Hvis du skal redigere sideoplysningerne, skal du vælge **Tilbage**. Hvis sideoplysningerne er korrekte, skal du vælge **Opret side**.
1. Under **Katalogvælger** skal du vælge **Hoved**, vælge ellipsen (**...**) og derefter **Tilføj modul**.

    ![Tilføjelse af et modul til Hoved under Katalogplukker.](./media/Author-web-page-catalog-picker-1.png)

1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. Vælg **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Katalogvælger** og derefter **OK**.
1. Vælg **Kataloger** i ruden Egenskaber for **katalogplukker** under **Overskrift**, og angiv derefter en overskrift til katalogplukkesiden.
1. Vælg **overskriftsniveauet**, vælg et overskriftsniveau, og vælg **OK**.
1. Angiv tekst, der skal vises øverst på siden til katalogplukker, under **RTF**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

### <a name="add-a-link-on-your-account-page"></a>Tilføje et link på kontosiden

Derefter skal du føje en reference til siden til katalogplukkeren på siden **Min konto**.

1. Gå til **sider**, søg efter og vælg webstedets **Min kontoside**, og vælg derefter **Rediger**.
1. Under **Hoved** skal du vælge **generisk kontofelt**. 
1. Vælg **Tilføj handlingslink** under **Links** i ruden **Generiske kontoegenskaber**, og vælg derefter **Handlingslink**.
1. Angiv linktekst for linket til katalogplukkesiden under **Link tekst** i dialogboksen **Handlingslink**.
1. Vælg **Tilføj et link** under **Linkdestination**.
1. Vælg **Brugerdefineret side** i dialogboksen **Tilføj et link**, og vælg derefter **Næste**.
1. Under **Navn** skal du vælge siden til katalogplukkeren, vælge **Anvend** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

I følgende illustration vises et eksempel på en kontoside med en reference til katalogsiden.

![Min kontoside med link til katalog.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Tilføje et link fra hovedet

Endelig skal du føje et link fra webstedshovedet til dine kataloger.

1. Gå til **Fragmenter**, søg efter og vælg webstedets hovedfragment, og vælg derefter **Rediger**.
1. Vælg **Sidehoved**-pladsen. 
1. Vælg **Tilføj handlingslink** under **Mine kontolinks** i ruden **Hoved**, og vælg derefter **Handlingslink**.
1. Angiv linktekst for linket til katalogplukkesiden under **Link tekst** i dialogboksen **Handlingslink**.
1. Vælg **Tilføj et link** under **Linkdestination**.
1. Vælg **Brugerdefineret side** i dialogboksen **Tilføj et link**, og vælg derefter **Næste**.
1. Under **Navn** skal du vælge siden til katalogplukkeren, vælge **Anvend** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke sidehovedfragmentet ind, og vælg derefter **Publicer** for at publicere det.

I følgende illustration vises et eksempel på et sidehoved til e-commerce-websted med link til B2B-kataloget.

![Sidehoved til e-commerce-websted med rullelistelink til katalog.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Yderligere ressourcer 

[Oprette handelskataloger til B2B-websteder](catalogs-b2b-sites.md)

[Udvidet virkning af Commerce-kataloger til B2B-tilpasninger](catalogs-b2b-sites-dev.md)

[Handelskataloger for B2B Ofte stillede spørgsmål](catalogs-b2b-sites-FAQ.md)

[Kontostyringssider og -moduler](account-management.md)

[Sidehovedmodul](author-header-module.md)
