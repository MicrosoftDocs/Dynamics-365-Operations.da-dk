---
title: " Regler for kategoriprissætning til oprettelse af samhandelsaftaler"
description: Denne procedure viser, hvordan du opretter salgsprissamhandelsaftaler ved hjælp af en kategoriprissætningsregel.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35c85e6e3bbdc913e9cd7aefdf6b143f3f03496f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022008"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a> Regler for kategoriprissætning til oprettelse af samhandelsaftaler

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter salgsprissamhandelsaftaler ved hjælp af en kategoriprissætningsregel. Det demodatafirma, der bruges til at oprette denne opgave, er USRT. Denne opgave er tiltænkt rollen Commerce-produktchef.

1. Klik på Styring af prissætning og rabatter.
2. Klik på Ny.
3. Klik på Regel for kategoripriser.
4. Markér den valgte række på listen.
5. Vælg en indstilling i feltet Kontokode.
    * En kontokode af typen "Gruppe" bruges til at konfigurere salgsprissamhandelsaftaler, der er specifikke for kanaler, fordelskundeprogrammer, kataloger og tilhørsforhold.  
6. Indtast eller vælg en værdi i feltet Kontovalg.
7. Indtast eller vælg en værdi i feltet Kategori.
8. Angiv et tal i feltet Beløb/procent.
9. Indtast eller vælg en værdi i feltet Afrundingsversion.
10. Klik på Generér handelsaftaler.
11. Klik på Næste.
12. Indtast en dato i feltet Fra dato.
13. Indtast en dato i feltet Til dato.
14. Vælg Ja i feltet Find næste.
15. Klik på Næste.
16. Klik på Finish.
    * Dette opretter en samhandelskladde og åbnes den til korrektur.  
17. Find og vælg den ønskede post på listen.
    * Samhandelskladder, der oprettes ud fra Kategoriprissætningsregler, bogføres ikke. Du kan gennemse og redigere de priser, der genereres, før de bogføres.  
18. Klik på Rediger.
19. Indtast et tal i feltet Beløb i valuta.
20. Klik på Bogfør.
21. Klik på OK.
22. Luk siden.
23. Luk siden.
24. Klik på fanen Regler for kategoripriser.
    * Kanalbestemte Kategoriprissætningsregler bliver vist i denne liste.  

