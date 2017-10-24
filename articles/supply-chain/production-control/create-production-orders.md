---
title: Opret produktionsordrer
description: "Når der oprettes en produktionsordre, oprettes en anmodning om at starte produktionen af en vare. Produktionsordren indeholder oplysninger om, hvad der skal produceres, det antal, der skal produceres, og den planlagte slutdato. Den indeholder også oplysninger om, hvilke materialer der skal bruges, og hvilken proces der skal følges for at producere varen."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58213d4d6e8c29ab6605eb7aa5c6cb9ca6ba4a10
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="create-production-orders"></a>Opret produktionsordrer

[!include[banner](../includes/banner.md)]


Når der oprettes en produktionsordre, oprettes en anmodning om at starte produktionen af en vare. Produktionsordren indeholder oplysninger om, hvad der skal produceres, det antal, der skal produceres, og den planlagte slutdato. Den indeholder også oplysninger om, hvilke materialer der skal bruges, og hvilken proces der skal følges for at producere varen.

En produktionsordre gennemgår trin i produktionslevetiden. Når en ordre oprettes, får den statusangivelsen **Oprettet**. Når en ordre er afsluttet, får den statusangivelsen **Afsluttet**. En parameterindstilling i hver fase gør det muligt for en bruger at konfigurere de enkelte trin. Indstillingen kan konfigureres til en enkelt bruger eller til alle brugere.

Produktionsstyklisten og produktionsruten er de vigtigste enheder i produktionsordren. De kopieres til produktionsordren baseret på den valgte vare og mængde, der skal produceres. Før produktionsordren startes, kan produktionsstyklisten og ruten redigeres.

En produktionsordre kan oprettes i følgende situationer:

-   Oprettes af varedisponeringsudførelse baseret på materialebehov.
-   Oprettes direkte fra en salgsordrelinje, eller når en produktionsordre på højere niveau oprettes og forkalkuleres (sporet forsyning).
-   Oprettes manuelt.





