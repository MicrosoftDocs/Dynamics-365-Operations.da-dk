---
title: Tilføj en side med politik om beskyttelse af personlige oplysninger
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer en side med politik om beskyttelse af personlige oplysninger i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001317"
---
# <a name="add-a-privacy-policy-page"></a>Tilføj en side med politik om beskyttelse af personlige oplysninger


[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du tilføjer en side med politik om beskyttelse af personlige oplysninger i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Overholdelse af privatlivets fred omfatter organisatoriske foranstaltninger, der informerer webstedets brugere om, hvordan deres data indsamles og håndteres. Brugerne kan derefter beslutte, hvordan de ønsker, at deres personlige data skal håndteres, og kan foretage de nødvendige handlinger.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Gennemse Microsofts erklæring om beskyttelse af personlige oplysninger i Dynamics 365 Commerce

Hvis du vil gennemse Microsofts erklæring om beskyttelse af personlige oplysninger, mens du er logget på oprettelsesværktøjerne i Dynamics 365 Commerce, skal du vælge knappen **Hjælp** (**?**) i øverste højre hjørne og derefter vælge **Beskyttelse af personlige oplysninger og cookies**. Der åbnes en ny fane, som har et link til [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).

## <a name="build-a-privacy-policy-page-for-your-site"></a>Opret en side med politik for beskyttelse af personlige oplysninger for dit websted

I Dynamics 365 Commerce er der flere måder at give brugere af dit websted adgang til din privatlivspolitik på. Dette afsnit viser, hvordan du opretter en side med politik om beskyttelse af personlige oplysninger og derefter refererer til siden ved hjælp af et sidefodsfragment.

Følgende vejledning er et eksempel, der viser, hvordan man opbygger en generisk side med politik om beskyttelse af personlige oplysninger for et Commerce-websted. Du er ansvarlig for at designe og implementere en side, som indeholder en politik om beskyttelse af personlige oplysninger, og som bedst muligt opfylder lovkravene til din virksomhed.

For at komme i gang skal du i oprettelsesværktøjerne gå til det websted, som du vil oprette en side med politik om beskyttelse af personlige oplysninger for.

### <a name="create-a-template"></a>Opret en skabelon

> [!NOTE]
> Hvis der allerede er oprettet en skabelon, som kan bruges til siden med politik for beskyttelse af personlige oplysninger, skal du springe frem til afsnittet [Opret en side med politik om beskyttelse af personlige oplysninger](#build-a-privacy-policy-page).

Følg disse trin for at oprette en skabelon.

1. Gå til **Skabeloner \> Ny skabelon**.
1. Angiv skabelonens navn, og vælg derefter **OK**.
1. Tilføj eventuelle påkrævede moduler til de påkrævede sidepladser i skabelonen. Hold musen over de røde udråbstegn for vejledning.

    For eksempel kræver pladsen **HTML-hoved** muligvis et **Eksternt Standard Script**-modul.

1. På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.
1. I modulet **Standardside** skal du på pladsen **Primær** tilføje et **Indholdsrig blokmodul**.
1. I **Indholdsrigt blokmodul** skal du tilføje et **Indholdsrigt blokelement**-modul.
1. Check skabelonen ind, og publicer den.

### <a name="build-a-privacy-policy-page"></a>Opret en side med politik om beskyttelse af personlige oplysninger

Følg disse trin for at oprette en side med politik om beskyttelse af personlige oplysninger.

1. Gå til **Sider \> Ny side**.
1. Vælg skabelonen for privatlivspolitiksiden.
1. Angiv et sidenavn og URL-adresse, og vælg derefter **OK**. 
1. På pladsen **Primær** på siden skal du tilføje et **Indholdsrigt blokmodul**.
1. I **Indholdsrigt blokmodul** skal du tilføje et **Indholdsrigt blokelement**-modul.
1. I egenskabsruden for **Indholdsrigt blokmodul** skal du vælge **Tilføj datakilde** og derefter vælge **RTF-indhold**.
1. I RTF-editoren skal du angive indholdet til siden med politik om beskyttelse af personlige oplysninger. Udvid RTF-editoren til fuldskærmstilstand efter behov.
1. Når du er færdig med at indtaste indholdet, skal du vælge **Forhåndsvisning** for at få vist siden i webbrowseren.
1. Gør eventuelle resterende tilføjelser til sidens og modulets egenskaber færdig.
1. Check siden med politik om beskyttelse af personlige oplysninger ind, og publicer den.

Følg disse trin for at publicere URL-adressen til siden med politik om beskyttelse af personlige oplysninger.

1. Gå til **URL**, og vælg URL-adressen for siden med politik om beskyttelse af personlige oplysninger.
1. Publicer den valgte URL-adresse.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Opret et link til siden med politik om beskyttelse af personlige oplysninger i en sidefod

Du kan tilføje et link til siden med politik om beskyttelse af personlige oplysninger til et fragment. På denne måde kan du dele linket og opdatere det på tværs af flere webstedssider ved at referere til fragmentet. I dette eksempel vises, hvordan du føjer et link til siden med politik om beskyttelse af personlige oplysninger til et sidefodsfragment.

Følg disse trin for at føje et link til sidefodsfragment.

1. Gå til **Sidefragmenter \> Nyt sidefragment**.
1. Vælg modulet **Sidefod**, og angiv derefter et navn i feltet **Sidefragmentsnavn**.
1. På pladsen **Sidefodskategori** skal du tilføje modulet **Sidefodselement**.
1. Vælg **Linktekst** i egenskabsruden til højre.
1. I dialogboksen **Linktekst** skal du angive linkteksten og linkmålet på siden med politik om beskyttelse af personlige oplysninger og derefter klikke på **OK**.

    Hvis du vil have URL-adressen tilføjet til siden med politik om beskyttelse af personlige oplysninger, skal du gå til **Sider** og derefter til siden med politik om beskyttelse af personlige oplysninger og kopierer URL-adressen fra egenskabsruden.

1. Gem fragmentet, check det ind, og publicer det.
1. Se et eksempel på fragmentet, og test linket til siden med politik om beskyttelse af personlige oplysninger.

Der kan nu refereres til fragmentet i skabelonen for andre webstedssider. Når der refereres til dette fragment i modulet **Sidefod** i en skabelon, vises linkreferencen på alle sider, der er oprettet ved hjælp af denne skabelon.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over overholdelse](compliance-overview.md)

[Funktioner og egenskaber til øget tilgængelighed](accessibility.md)

[Cookie-overholdelse](cookie-compliance.md)
