---
title: Framelde webaktivitetshændelser
description: Dette emne forklarer, hvordan du kan give besøgende på dit websted mulighed for at framelde indsamlingen af webaktivitetshændelser i Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791551"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Fravælge samling af webaktivitetshændelse
[!include [banner](includes/banner.md)]

I dette emne forklares det, hvordan du kan lade kunderne framelde indsamling af webaktivitetshændelser i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce lad webstedsadministratorer analysere webaktiviteten for brugere af deres e-handelswebsteder. På denne måde kan de bedre forstå, hvordan deres websteder bruges, og de kan optimere webstederne, så det er muligt at sikre en forbedret brugeroplevelse og opfylde forretningsmålsætningerne.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Forskellige måder for administratorer at implementere fravalg på

Administratorer kan implementere framelding på tre måder.

### <a name="opt-out-on-behalf-of-users"></a>Framelding på vegne af brugere

I Kontostyring i Commerce Headquarters (HQ) kan administratorer vælge framelding på brugernes vegne.

1. Gå til HQ-klienten, og søg efter og vælg en kunde på siden **Alle kunder**.
1. Gå til siden Kundeoplysninger, og indstil indstillingen **Spor ikke webaktivitet** til **Ja** i sektionen **Beskyttelse af personlige oplysninger** i oversigtspanelet **Detail**.

    ![Indstillinger for beskyttelse af personlige oplysninger](media/Disablepersonalizationpart2.png)

1. Vælg **Gem**, og luk derefter siden.

### <a name="module-based-opt-out-experience"></a>Modulbaseret framelding

Administratorer kan lade godkendte brugere selv framelde sig indsamlingen af webaktivitetshændelser. Hvis du vil levere denne framelding, skal du tilføje brugerframeldingsmodulet på debitorkontoprofilsider.

### <a name="custom-extensions"></a>Brugerdefinerede udvidelser

Administratorer kan oprette deres egne udvidelser for at administrere brugernes mulighed for framelding. Yderligere oplysninger finder du under [Kalde Retail Server-API'er](e-commerce-extensibility/call-retail-server-apis.md) og [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
