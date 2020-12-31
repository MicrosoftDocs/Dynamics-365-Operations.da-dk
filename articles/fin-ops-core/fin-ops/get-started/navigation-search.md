---
title: Navigationssøgning
description: I dette emne forklares, hvordan du kan bruge søgefunktionen til at navigere til sider.
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b68182ff7da07f350e2eacaf569089e0fdf44a8d
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4695055"
---
# <a name="navigation-search"></a>Navigationssøgning

[!include [banner](../includes/banner.md)]

I dette emne forklares, hvordan du kan bruge søgefunktionen til at navigere til sider.

Programmet indeholder en række områder og sider, der kan hjælpe dig med at udføre forskellige opgaver. Du kan hurtigt finde de sider, som du skal bruge til at udføre opgaverne, med brug af funktionen til navigationssøgning.

Hvis du vil bruge denne funktion, skal du klikke på ikonet **Søg** for at få vist feltet **Søg**. Du kan derefter skrive et eller flere ord i feltet. Systemet søger øjeblikkeligt efter relevante sider i programmet, der svarer til de ord, du har angivet. Du kan for eksempel skrive "kreditorfaktura" som input, så viser systemet resultaterne, der stemmer overens med indtastningen.

> [!NOTE]
> Feltet **Søg** bruges til at finde og navigere til sider. Det hjælper ikke dig med at finde bestemte data eller handlinger.

[![søgefelt](media/navigation-search.png "Søgefelt")

## <a name="quickly-navigate-to-a-particular-page"></a>Hurtigt navigere til en bestemt side

Funktionen til navigationssøgning fungerer også som en enestående mulighed for at navigere hurtigt til en bestemt side. Hvis du for eksempel er kreditormedarbejder og ofte bruger siden **Betalingskladde**, kan du skrive "betalingskladde" i feltet **Søg**. Da inputtet er et nøjagtigt match for sidetitlen, vises siden øverst i søgeresultaterne, og du kan hurtigt navigere til den.

Listen over søgeresultater viser sidens titel og navigationsstien. Placeringen af siden vises i programmet. Det hjælper dig også med at skelne mellem to eller flere lignende sider i resultaterne.

Når du søger efter en side, sammenholdes dit input mod sidens titel samt dens navigationssti. Hvis du for eksempel angiver "debitor" i feltet **Søg**, vises resultaterne for de sider, der er tilgængelige for dig i området Debitor – selvom sidetitlerne ikke indeholder ordet "debitor".

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Navigere hurtigt til en side baseret på formularens tekniske navn

Funktionen til navigationssøgning indeholder også en meget efterspurgt funktion for Superbrugere: muligheden for hurtigt at navigere til en side baseret på formens tekniske navn. Mange brugere er så fortrolig med systemet, at nøjagtigt ved, hvilke formularnavne de arbejder med. Hvis du er en af disse brugere, kan du angive **form:** efterfulgt af navnet på den form, du søger efter. Hvis du for eksempel angiver **form: kreditorfaktura**, viser søgeresultaterne alle sider, hvor formens navn starter med **kreditorfaktura**.

## <a name="administration-and-security"></a>Administration og sikkerhed

Fra et forvaltnings- og sikkerhedsmæssigt perspektiv viser funktionen til navigationssøgning kun to resultattyper:

- Sider, der er aktiveret i den aktuelle konfiguration (via konfigurationsnøgler).
- Sider, som brugeren har adgang til baseret på brugerens rolle.

Listen over søgeresultater er begrænset til 10 elementer. Hvis du ikke kan finde det, du søger, i resultaterne, skal du prøve at afgrænse eller opdatere inputtet.

## <a name="development"></a>Udvikling

Fra et udviklingsperspektiv er funktionen til navigationssøgning meget nem at udnytte, fordi der praktisk talt ikke er nogen forsinkelse mellem implementering af menupunkter og deres evne til at blive vist i søgeresultater. Så længe menupunkterne er tilknyttet fra navigationsruden eller dashboardet, bliver det automatisk muligt at søge i dem.
