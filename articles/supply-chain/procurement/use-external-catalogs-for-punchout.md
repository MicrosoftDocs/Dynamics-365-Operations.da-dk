---
title: "Bruge eksterne kataloger til PunchOut e-indkøb"
description: Dette emne forklarer, hvordan du kan bruge eksterne kataloger til at oprette og sende rekvisitioner.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 01955aefb27bd18809b35fd025c9dd1b8eb70520
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a>Bruge eksterne kataloger til PunchOut e-indkøb
Ved hjælp af eksterne kataloger til PunchOut-e-indkøb skal du ikke vedligeholde oplysninger om dine kreditorers produkter i dine egne masterdata. I stedet konverteres indkøbsvognen på en leverandørs websted til rekvisitionslinjer, der har de korrekte produktoplysninger. 

Du skal undgå at vedligeholde beskrivelserne af og priserne for dine leverandørers produkter i dine egne produktmasterdata. Brug i stedet eksterne kataloger til PunchOut e-indkøb. Derefter, når medarbejdere opretter indkøbsrekvisitioner, kan de "stemple ud" til en leverandørs eksterne katalogwebsted (med andre ord forlader de dit system og går til leverandørens websted). De produkter, der føjes til indkøbsvognen på leverandørens websted, kan derefter konverteres til rekvisitionslinjer. Derfor kan du få de korrekte produktoplysninger: produkt-id, navn, pris og så videre.

Hvis du vil bruge eksterne kataloger, skal en medarbejder oprette en rekvisition på siden **Mine indkøbsrekvisitioner**.

Den medarbejder, der opretter en rekvisition, kaldes klargøreren af rekvisitionen. Som klargører kan du udføre følgende opgaver.

Brug linjen **Eksterne kataloger** til at åbne en side, der indeholder alle eksterne kataloger, der er tilgængelige for den angivne anmoder, juridiske indkøbsenhed og modtagerdriftsenhed.

Alt efter dine rettigheder kan du ændre anmoderen, den juridiske indkøbsenhed og modtagerdriftsenheden. En ændring i disse værdier kan ændre listen over eksterne kataloger, der er tilgængelige for en anmoder. Eksterne kataloger, der er tilgængelige, afhænger af de aktuelle aktive indkøbspolitikker for den juridiske indkøbsenhed eller modtagerdriftsenheden. Disse politikker kan tillade eller forhindre adgang til bestemte indkøbskategorier. Listen over eksterne kataloger, der er knyttet til disse indkøbskategorier, kan derfor påvirkes.

Du kan finde flere oplysninger om politikker i [Indkøbspolitikker](../procurement/purchase-policies.md).

- For at finde eksterne kataloger til bestemte indkøbskategorier kan du indtaste tekst i søgefeltet til kataloger.
- Hvis du vil tilføje produkter fra en leverandørs eksterne katalog på leverandørens websted, skal du klikke på det eksterne katalog. Tilføj derefter produkter i indkøbsvognen, og gå til kassen. Linjerne for indkøbsvognen overføres til Microsoft Dynamics 365.

Hvis der er flere muligheder for indkøbskategorier, kan du vælge den korrekte indkøbskategori, før du tilføjer linjerne i rekvisitionen.
Når du har føjet linjer til en rekvisition, kan du tilføje flere linjer uden at bruge eksterne kataloger. Alternativt kan du fortsætte med at bruge eksterne kataloger til at tilføje linjer.

Når indkøbsrekvisitionen er klar, kan du bruge handlingen **Arbejdsgang** > **Send** til at sende den til godkendelse.
