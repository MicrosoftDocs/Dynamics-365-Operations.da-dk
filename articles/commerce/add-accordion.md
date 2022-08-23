---
title: Harmonikamodul
description: Denne artikel dækker harmonikamoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: ec895476770f297825d6c88d0b0a5fef43a5c6ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279150"
---
# <a name="accordion-module"></a>Harmonikamodul

[!include [banner](includes/banner.md)]

Denne artikel dækker harmonikamoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Harmonikamoduler er containerlignende moduler, der bruges til at organisere oplysningerne eller modulerne på en side ved hjælp af en skuffeagtig funktion, der kan skjules. Et harmonikamodul kan bruges på alle sider.

Inde i hvert harmonikamodul kan et eller flere harmonikaelementmoduler tilføjes. Hvert enkelt harmonikaelementmodul repræsenterer en skuffe, der kan skjules. Inde i hvert harmonikaelementmodul kan et eller flere moduler tilføjes. Der er ingen begrænsninger for de typer moduler, der kan føjes til et harmonikaelementmodul.

Følgende billede viser et eksempel på et harmonikamodul, der bruges til at organisere oplysninger på en butiks side med ofte stillede spørgsmål (FAQ).

![Eksempel på et harmonikamodul.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Harmonikamodulegenskaber

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift | Tekst | Denne egenskab specificerer en valgfri tekstoverskrift i harmonikamodulet. |
| Udvid alle | **Sand** eller **Falsk** | Hvis værdien er angivet til **Sand**, er funktionen Udvid/skjul slået til, så alle elementerne i harmonikamodulet kan udvides og skjules. |
| Interaktionstypografi | **Uafhængig** eller **Udvid kun et element** | Denne egenskab definerer interaktionstypografien for harmonikaelementerne. Hvis værdien er angivet som **Uafhængig**, kan hver enkelt element udvides eller skjules uafhængigt. Hvis værdien er angivet til **Udvid kun et element**, kan kun et element udvides ad gangen. Efterhånden som elementerne udvides, skjules tidligere udvidede elementer. |

## <a name="accordion-item-module-properties"></a>Egenskaber for harmonikaelementmoduler

| Egenskabsbetegnelse | Værdier | Beskrivende tekst |
|----------------|--------|-------------|
| Stilling | Tekst | Denne egenskab specificerer titelteksten for harmonikaelementmodulet. Når du vælger titelområde, kan brugerne udvide eller skjule sektionen. |
| Udvid som standard | **Sand** eller **Falsk** | Hvis værdien er angivet til **Sand**, udvides harmonikaelementet som standard, når siden indlæses. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Føje et harmonikamodul til en FAQ-side

Hvis du vil føje et harmonikamodul til en FAQ-side og angive dets egenskaber i webstedsgeneratoren, skal du følge disse trin.

1. Gå til **Sider**, og brug Fabrikam-marketingskabelonen (eller en skabelon uden begrænsninger) til at oprette en ny side, der hedder **Gem ofte stillede spørgsmål**.
1. På pladsen **Hoved** på **Standardsiden** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Harmonika** og derefter **OK**.
1. Vælg **Overskrift** ud for blyantsymbolet i egenskabsruden for harmonikamodulet.
1. I dialogboksen **Overskrift** under **Overskriftstekst** skal du angive **Ofte stillede spørgsmål**. Vælg derefter **OK**.
1. I egenskabsruden for harmonikamodulet skal du vælge afkrydsningsfeltet **Vis udvid alle** og derefter skal du i feltet **Interaktionstype** vælge **Uafhængig**.
1. På pladsen **Harmonika** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Harmonikaelement** og derefter **OK**.
1. l egenskabsruden for harmonikaelementmodulet under **Titel** skal du angive titelteksten (f.eks. **Hvordan fungerer returneringer?**).
1. På pladsen **Harmonikaelement** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Tekstblok** og derefter **OK**.
1. I egenskabsruden i tekstblokmodulet skal du angive et tekstafsnit (f.eks.: **Returneringer skal behandles via callcentret. Kontakt 1-800-FABRIKAM for returneringer. Produkterne har 30 dages returret. Returneringer skal indledes inden for denne tidsramme.**).
1. På pladsen **Harmonika** tilføjes nogle flere harmonikaelementmoduler. Tilføj et tekstblokmodul med indhold i hvert harmonikaelementmodul.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. På siden vises et harmonikamodul med det indhold, du har tilføjet.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Container-modul](add-container-module.md)

[Fanemodul](add-tab.md)

[Tekstblokmodul](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
