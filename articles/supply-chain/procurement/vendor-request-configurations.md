---
title: Konfigurationer for kreditoranmodning
description: I dette emne beskrives de felter, der skal udfyldes i en ny kreditoranmodning.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: e9b22a6f846607e8afc5d4f01c685f1364b1c01d
ms.contentlocale: da-dk
ms.lasthandoff: 02/08/2018

---

# <a name="vendor-request-configurations"></a>Konfigurationer for kreditoranmodning
[!include [banner](../includes/banner.md)]

For at fuldføre en kreditoranmodning skal en kontaktperson for kreditoren fuldføre registreringsguiden for den mulige kreditor.

I formularen **Konfigurationer for kreditoranmodning** kan du oprette profiler, der angiver nødvendige og synlige felter i registreringsguiden for den mulige kreditor.

Registreringsguiden begynder med at bede den mulige kreditorbruger, hvilket land/område kreditoren gør forretninger i. Disse oplysninger bestemmer, hvilken konfiguration der er gældende. Hvis der ikke er defineret nogen bestemt konfiguration for et land/område, bruges en standardkonfiguration.

### <a name="set-up-a-vendor-request-configuration"></a>Konfigurere en kreditoranmodning

Som standard findes der en kreditorkonfiguration i formularen Konfigurationer for kreditoranmodning.

Det er ikke muligt at vælge lande/områder til standardkonfigurationen, så afsnittet **Lande/områder** kan ikke ændres.

1. Klik på **Indkøb og forsyning** > **Konfiguration** > **Kreditorer**, og klik derefter på **Konfigurationer for kreditoranmodning**.
2. Klik på fanen **Felter** for at angive status for de angivne felter.
3. Skjult (ikke-synlig)
4. Vist (synlig, men ikke obligatorisk)
5. Påkrævet (synlig og obligatorisk)
6. Klik på fanen **Indhold** for at angive, om tekst skal vises i guiden, og om der skal være en bekræftelse af, at den mulige kreditorbruger skal acceptere dette, før han eller hun går videre til næste trin i guiden. Der anmodes om bekræftelsen for de vilkår og betingelser, som brugeren skal acceptere for at fortsætte.

Du kan også angive en bekræftelsesmeddelelse, der bliver vist, når guiden er færdig, og du kan føje et eller flere spørgeskemaer.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Oprette en kreditorkonfiguration for et bestemt land/område
1.  Klik på **Indkøb og forsyning** > **Konfiguration** > **Kreditorer**, og klik derefter på **Konfigurationer for kreditoranmodning**.
2.  Klik på **Ny** for at oprette en ny konfiguration, og angiv et navn til konfigurationen.
3.  Klik på **Gem**.
4.  Åbn fanen **Lande/områder** for at vælge det land/område, som konfigurationen skal bruges til.
5.  Fuldfør konfigurationen ved at følge retningslinjerne for standardkonfigurationen.


