---
title: Regnskab i den offentlige sektor i Frankrig
description: I denne artikel beskrives regnskaber for den franske offentlige sektor.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19621
ms.assetid: f6bfb9dd-c3a7-48d3-b31d-23e6f27c1323
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 751da12da1ffb8ff7e691f9fc17bb59185e94cb3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206068"
---
# <a name="public-sector-accounting-in-france"></a>Regnskab i den offentlige sektor i Frankrig

[!include [banner](../includes/banner.md)]

I denne artikel beskrives regnskaber for den franske offentlige sektor.

## <a name="prerequisites"></a>Forudsætninger

Funktioner til den offentlige sektor i Frankrig er tilgængelige, når følgende betingelser er opfyldt:

-   Konfigurationsnøglen **Offentlig sektor** og undernøglen **Franske myndighedskrav** vælges.
-   Indstillingen **Brug konteringsreglerne for den franske offentlige sektor** er valgt på siden **Budgetparametre**.
-   Standardkoden for land/område er Frankrig.

Yderligere konfigurationstrin for bestemte funktioner er omfattet af artiklen for hver funktion.

## <a name="french-public-sector-topics"></a>Emner for den franske offentlige sektor
-   [Mandat de paiement](emea-fra-mandats-de-paiement.md): Direktøren bruger mandat de paiement til at underrette og autorisere bogholderen til at betale et specifikt beløb til en anden enhed.
-   [Spærringer for kreditorfakturabetaling](emea-fra-vendor-invoice-payment-holds-public-sector.md): De almindelige processer, der vedrører betalingsspærringer af kreditorfakturaer, er suppleret for franske enheder i den offentlige sektor.
-   [Titres de recette](emea-fra-titres-de-recette-public-sector.md): Direktøren bruger titres de recette til at underrette og autorisere bogholderen til at opkræve et specifikt beløb fra en anden enhed.
-   [Forpligtelser](emea-fra-commitments-public-sector.md): Forpligtelser bruges til at reservere budgetterede beløb. Derved kan en organisation udtrykkeligt kan spore budgetreservationer til administration og rapportering i hele udgiftscyklussen.
-   [Indkøb og forsyning](emea-fra-procurement-sourcing-public-sector.md):
    -   De standardfunktioner, der vedrører købsaftaler, suppleres for franske enheder i den offentlige sektor. For eksempel kan du oprette trancher og partier, styre adgangen til afdelinger, administrere kreditorcertificeringer og konfigurere de største kontrahenter, medkontrahenter og underleverandører. Disse funktioner gør det nemmere at opfylde kravene i Code des Marchés Publics.
    -   For at opfylde offentlige lovgivningsmæssige krav i Frankrig skal du angive forbrugsgrænser for køb i de indkøbskategorier, som er defineret af Clé de Contrôle Marché. Med en **Forbrugsgrænser efter kategori**-politikregel, der bruges sammen med indkøbspolitikregler, kan du bruge attributter for ikrafttrædelsesdato, estimerede udgiftsbeløb og tærskelbeløb til at understøtte krævede indkøbspraksis. Politikreglen sikrer også en effektiv brug af offentlige midler.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]