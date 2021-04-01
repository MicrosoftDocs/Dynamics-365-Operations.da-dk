---
title: Oversigt over produktionsordres livscyklus
description: Når der oprettes en produktionsordre, oprettes en anmodning om at starte produktionen af en vare. Produktionsordren indeholder oplysninger om, hvad der skal produceres, det antal, der skal produceres, og den planlagte slutdato. Den indeholder også oplysninger om, hvilke materialer der skal bruges, og hvilken proces der skal følges for at producere varen.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68758f4ddf39b4b8f7f0758f9e59e17c3411723a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246303"
---
# <a name="production-order-lifecycle-overview"></a>Oversigt over produktionsordres livscyklus

[!include [banner](../includes/banner.md)]

Når der oprettes en produktionsordre, oprettes en anmodning om at starte produktionen af en vare. Produktionsordren indeholder oplysninger om, hvad der skal produceres, det antal, der skal produceres, og den planlagte slutdato. Den indeholder også oplysninger om, hvilke materialer der skal bruges, og hvilken proces der skal følges for at producere varen.

En produktionsordre gennemgår trin i produktionslevetiden. Når en ordre oprettes, får den statusangivelsen **Oprettet**. Når en ordre er afsluttet, får den statusangivelsen **Afsluttet**. En parameterindstilling i hver fase gør det muligt for en bruger at konfigurere de enkelte trin. Indstillingen kan konfigureres til en enkelt bruger eller til alle brugere.

Produktionsstyklisten og produktionsruten er de vigtigste enheder i produktionsordren. De kopieres til produktionsordren baseret på den valgte vare og mængde, der skal produceres. Før produktionsordren startes, kan produktionsstyklisten og ruten redigeres.

En produktionsordre kan oprettes i følgende situationer:

-   Oprettes af varedisponeringsudførelse baseret på materialebehov.
-   Oprettes direkte fra en salgsordrelinje, eller når en produktionsordre på højere niveau oprettes og forkalkuleres (sporet forsyning).
-   Oprettes manuelt.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]