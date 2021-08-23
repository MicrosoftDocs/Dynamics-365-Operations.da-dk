---
title: Fanemodul
description: Dette emne omhandler fanemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9062e584d159e0f1986c46140d535f06f5d2817af048f30e812f9049bd52d4f6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723281"
---
# <a name="tab-module"></a>Fanemodul

[!include [banner](includes/banner.md)]

Dette emne omhandler fanemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Fanemoduler er containeragtige moduler, som bruges til at organisere oplysningerne på en webstedsside på faner. De kan bruges på alle sider, hvor oplysninger skal vises under faner.

Inde i hvert fanemodul kan et eller flere faneelementmoduler tilføjes. De enkelte faneelementmoduler repræsenterer en enkelt fane. I hvert faneelementmodul kan et eller flere moduler tilføjes. Der er ingen begrænsninger for de typer moduler, der kan føjes til et faneelementmodul.

Det følgende billede viser et eksempel på et fanemodul på en webstedside. I dette eksempel er fanen **Levering** valgt.

![Eksempel på et fanemodul.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Fanemodulegenskaber

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift | Tekst | Denne egenskab specificerer en valgfri tekstoverskrift i fanemodulet. |
| Aktiv fane-indeks | Tal | Denne egenskab specificerer den fane, der skal være aktiv som standard, når en side indlæses. Hvis der ikke angives en værdi, er det første faneelement som standard aktivt. |

## <a name="tab-item-module-properties"></a>Faneelementmodulegenskaber

| Egenskabsbetegnelse | Værdier | Beskrivende tekst |
|---------------|--------|-------------|
| Stilling | Tekst | Denne egenskab specificerer titelteksten for faneelementmodulet. |

## <a name="add-a-tab-module-to-a-page"></a>Føje et fanemodul til en side

Hvis du vil føje et fanemodul til en side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Brug Fabrikam-marketingskabelonen (eller en skabelon uden begrænsninger) til at oprette en ny side, der hedder **Gem side med politikker**.
1. På pladsen **Hoved** på **Standardsiden** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Fane** og derefter **OK**.
1. Vælg **Overskrift** ud for blyantsymbolet i egenskabsruden for fanemodulet.
1. I dialogboksen **Overskrift** under **Overskrifttekst** skal du angive en overskrifttekst (f.eks. **Politikker**). Vælg derefter **OK**.
1. På pladsen **Fane** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Faneelement** og derefter **OK**.
1. l egenskabsruden for faneelementmodulet under **Titel** skal du angive titelteksten (f.eks. **Levering**).
1. På pladsen **Faneelement** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Tekstblok** og derefter **OK**.
1. I egenskabsruden for tekstblokmodulet under **RTF-tekst** skal du angive et tekstafsnit.
1. På pladsen **Fane** skal du tilføje flere faneelementmoduler, der har titler. Tilføj et tekstblokmodul med indhold i hvert faneelementmodul.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. På siden vises et fanemodul, der indeholder faneelementmoduler med det indhold, du har tilføjet.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Container-modul](add-container-module.md)

[Harmonikamodul](add-accordion.md)

[Tekstblokmodul](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]