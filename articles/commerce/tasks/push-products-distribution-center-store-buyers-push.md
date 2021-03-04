---
title: " Skubbe produkter fra distributionscenter til butik ved hjælp af centraliseret indkøb"
description: Denne procedure gennemgår trin til oprettelse og behandling af et centraliseret indkøb med henblik på distribution af produkter fra én lokation til en eller mange butikker.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dad74855ab9a9c225a5cd64a8c27663aedcd21e4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411114"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a> Skubbe produkter fra distributionscenter til butik ved hjælp af centraliseret indkøb

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår trin til oprettelse og behandling af et centraliseret indkøb med henblik på distribution af produkter fra én lokation til en eller mange butikker. Brugeren kan definere flere konfigurationer og få systemet til at foreslå, hvordan produkter skal distribueres, eller manuelt angive, hvor produkterne skal distribueres til, og hvor meget der bliver distribueret til de enkelte butikker. Denne procedure omfatter ikke opsætning af data, der kan bruges i centraliseret indkøb som f.eks. genopfyldningsregler, organisationshierarkier og vægten af butikken. Denne procedure bruger demofirmaet USRT.

1. Gå til Bestilling efter ordre.
2. Klik på Ny.
3. Skriv en værdi i feltet Beskrivelse.
4. Indtast eller vælg en værdi i feltet Lokation.
5. Angiv eller vælg et lagersted, der har produkter med disponible antal, i feltet Lagersted.
6. Klik på Tilføj.
7. Markér den valgte række på listen.
8. Indtast eller vælg et produkt i feltet Varenummer.
9. Klik på Tilføj.
10. Markér den valgte række på listen.
11. Indtast eller vælg et variant-produkt i feltet Varenummer.
    * Når du angiver et variantprodukt, oprettes der linjer for hver variant.  
12. Markér en række på listen.
13. Skriv i feltet Udskudt antal, hvor mange af det valgte produkt, du vil fordele.
14. I feltet Tillægsantal til overførsel skal du angive antallet af produkter, der har tilgængeligt antal til fordeling.
15. Angiv "Lokationsvægt" i feltet Distribution.
    * Du kan vælge andre typer for at bruge andre regler for fordelingen.  
16. Vælg en værdi i feltet Opfyldningshierarki.
17. Vælg Ja i feltet Respektér udvalg.
18. Klik på Beregn antal, og gennemgå de antal, der er føjet til rækkerne i sektionen Lagersted.
19. Klik på Opret ordre.
20. Klik på Ja.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]