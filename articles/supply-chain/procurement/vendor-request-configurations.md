---
title: Konfigurationer for kreditoranmodning
description: I dette emne beskrives de felter, der skal udfyldes i en ny kreditoranmodning.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 1d34a9974da41b7abb40bb2cf046a15432c249eb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570291"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]