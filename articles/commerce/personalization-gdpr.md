---
title: Framelde personlige anbefalinger
description: I dette emne forklares det, hvordan du kan lade kunderne framelde sig personlige anbefalinger i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e88980ef6ad585826762c8be35304aecbcc02ab
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154289"
---
# <a name="opt-out-of-personalized-recommendations"></a>Framelde personlige anbefalinger

[!include [banner](includes/banner.md)]

I dette emne forklares det, hvordan du kan lade kunderne framelde sig personlige anbefalinger i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Under oprettelsen af en konto konfigureres nye kunder automatisk til at modtage personlige anbefalinger. Dynamics 365 Commerce tilbyder dog forskellige måder for detailhandlere at lade brugerne framelde sig modtagelsen af disse anbefalinger og begrænse behandlingen af deres personlige data. Godkendte brugere, der fravælger personligt tilpassede anbefalinger, vil straks ophøre med at få vist personligt tilpassede lister. Desuden fjernes alle personlige data, der er indsamlet til personlig tilpasning, fra modellerne for tilpassede anbefalinger.

Der er flere oplysninger om personligt tilpassede produktanbefalinger, under [Aktivere personlige anbefalinger](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Forskellige måder for detailhandlere at implementere framelding på

Detailhandlere kan implementere framelding på tre måder.

### <a name="opting-out-on-behalf-of-users"></a>Framelding på vegne af brugere

I Kontostyring i Commerce-administrationen kan detailhandlere vælge framelding på brugernes vegne.

1. Søg efter **Alle kunder** fra startsiden i administrationen.
1. Søg efter og vælg en kunde, og vælg derefter oversigtspanelet **Detail**.

    ![Oversigtspanelet Detail](./media/Disablepersonalizationpart1.png)

1. Under **Beskyttelse af personlige oplysninger** skal du angive indstillingen **Deaktiver tilpasning** til **Ja**.

    ![Indstillinger for beskyttelse af personlige oplysninger](./media/Disablepersonalizationpart2.png)

1. Vælg **Gem**, og luk siden.

### <a name="module-based-opt-out-experience"></a>Modulbaseret framelding

Detailhandlere kan give godkendte brugere mulighed for selv at fravælge de personlige anbefalinger. Hvis du vil levere denne framelding, skal du tilføje brugerframeldingsmodulet på debitorkontoprofilsider.

### <a name="custom-extensions"></a>Brugerdefinerede udvidelser

Detailhandlere kan oprette deres egne udvidelser for at administrere brugernes mulighed for framelding. Yderligere oplysninger finder du under [Kalde Retail Server-API'er](e-commerce-extensibility/call-retail-server-apis.md) og [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Få en digital kopi af personligt tilpassede anbefalingers data på vegne af en godkendt bruger

Kunder vil måske gerne have en digital kopi af deres personlige data, og de kan også se en eksporteret visning af deres anbefalingsresultater. Hvis en kunde anmoder om disse oplysninger, skal forhandleren oprette en tilpasset udvidelse, der kalder Application Programming Interface (API) til Retail-Server programmet og forespørger på de fulde resultater ud fra **Udvalgt til dig**-listen på basis af kundens kunde-id. Resultatet kan derefter eksporteres i formatet med kommaseparerede værdier (CSV) og deles med kunden.

Følgende eksempel viser, hvordan en forhandler kan udføre denne opgave.

1. Detailhandleren opretter en brugerdefineret udvidelse for at trække personlige anbefalingsdata ud på brugerens vegne. Oplysninger om, hvordan du opretter moduler, kloner eksisterende moduler, kalder Retail Server-API'er og kalder datahandlinger, finder du under [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).
2. Den brugerdefinerede udvidelse kalder **get-recommendations**-kernedatahandlingen og overfører de nødvendige oplysninger til den ud fra kravene på listen. Hvis der er tale om **Udvalgt til dig**-listen, skal udvidelsen overføre det korrekte listenavn og kunde-id til datahandlingen.

    En måde at oprette den brugerdefinerede udvidelse på er at klone det eksisterende produktsamlingsmodul, der bruges til at returnere anbefalede resultater. Hvis du kloner dette eksisterende modul, kan en forhandler ændre den eksisterende kode og tilføje en ny knap, der eksporterer anbefalingsresultaterne til en CSV-fil. Der er flere oplysninger under [Klone et startpakke-modul](e-commerce-extensibility/clone-starter-module.md) og [Produktsamlingsmoduler](product-collection-module-overview.md).

    En komplet visning af Retail Server-API-biblioteket finder du under [Kunde- og forbruger-API'er for Retail Server](dev-itpro/retail-server-customer-consumer-api.md).

3. Når den brugerdefinerede udvidelse er oprettet, kan forhandleren eksportere en CSV-fil med alle anbefalingsresultater på baggrund af det entydige kunde-id for den godkendte bruger.
4. Detailhandleren kan dele den eksporterede CSV-fil, der indeholder den fulde personlige liste over anbefalede produkter, med den godkendte bruger.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivere ADLS i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)
