---
title: Fravælge tilpassede anbefalinger
description: Denne artikel forklarer det, hvordan du kan lade kunderne framelde sig personlige anbefalinger i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 5d75f1ae4ec8fbccd00635d3c245a5ae7c1e1dff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283662"
---
# <a name="opt-out-of-personalized-recommendations"></a>Fravælge tilpassede anbefalinger

[!include [banner](includes/banner.md)]

Denne artikel forklarer det, hvordan du kan lade kunderne framelde sig personlige anbefalinger i Microsoft Dynamics 365 Commerce.

Under oprettelsen af en konto konfigureres nye kunder automatisk til at modtage personlige anbefalinger. Dynamics 365 Commerce tilbyder dog forskellige måder for detailhandlere at lade brugerne framelde sig modtagelsen af disse anbefalinger og begrænse behandlingen af deres personlige data. Godkendte brugere, der fravælger personligt tilpassede anbefalinger, vil straks ophøre med at få vist personligt tilpassede lister. Desuden fjernes alle personlige data, der er indsamlet til personlig tilpasning, fra modellerne for tilpassede anbefalinger.

Der er flere oplysninger om personligt tilpassede produktanbefalinger, under [Aktivere personlige anbefalinger](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Forskellige måder for detailhandlere at implementere framelding på

Detailhandlere kan implementere framelding på tre måder.

### <a name="opting-out-on-behalf-of-users"></a>Framelding på vegne af brugere

I Kontostyring i Commerce-administrationen kan detailhandlere vælge framelding på brugernes vegne.

1. Søg efter **Alle kunder** fra startsiden i administrationen.
1. Søg efter og vælg en kunde, og vælg derefter oversigtspanelet **Detail**.

    ![Oversigtspanelet Detail.](./media/Disablepersonalizationpart1.png)

1. Under **Beskyttelse af personlige oplysninger** skal du angive indstillingen **Deaktiver tilpasning** til **Ja**.

    ![Indstillinger for beskyttelse af personlige oplysninger.](./media/Disablepersonalizationpart2.png)

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

    En måde at oprette den brugerdefinerede udvidelse på er at klone det eksisterende produktsamlingsmodul, der bruges til at returnere anbefalede resultater. Hvis du kloner dette eksisterende modul, kan en forhandler ændre den eksisterende kode og tilføje en ny knap, der eksporterer anbefalingsresultaterne til en CSV-fil. Der er flere oplysninger under [Klone et modul i modulbiblioteket](e-commerce-extensibility/clone-starter-module.md) og [Produktsamlingsmoduler](product-collection-module-overview.md).

    En komplet visning af Retail Server-API-biblioteket finder du under [Kunde- og forbruger-API'er for Retail Server](dev-itpro/retail-server-customer-consumer-api.md).

3. Når den brugerdefinerede udvidelse er oprettet, kan forhandleren eksportere en CSV-fil med alle anbefalingsresultater på baggrund af det entydige kunde-id for den godkendte bruger.
4. Detailhandleren kan dele den eksporterede CSV-fil, der indeholder den fulde personlige liste over anbefalede produkter, med den godkendte bruger.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
