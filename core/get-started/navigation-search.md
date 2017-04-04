---
title: "Navigationssøgning"
description: "Denne artikel beskriver, hvordan du kan bruge søgefunktionen til at navigere til siderne i Microsoft Dynamics 365 for operationer."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>Navigationssøgning

Denne artikel beskriver, hvordan du kan bruge søgefunktionen til at navigere til siderne i Microsoft Dynamics 365 for operationer.

Dynamics 365 for operationer giver funktionalitet for en lang række brancher og lodrette. Programmet indeholder en række områder og sider kan hjælpe dig med at udføre forskellige opgaver. Du kan hurtigt finde de sider, du skal udføre opgaverne, skal du bruge søgefunktionen navigation. Hvis du vil bruge denne funktion, skal du klikke på ikonet **Søg** for at få vist feltet **Søg**. Du kan derefter skrive et eller flere ord i feltet. Systemet søger øjeblikkeligt efter relevante sider i programmet, der svarer til de ord, du har angivet. Du kan for eksempel skrive "kreditorfaktura" som input, så viser systemet resultaterne, der stemmer overens med indtastningen. **Bemærk!** Feltet **Søg** bruges til at finde og navigere til sider. Det hjælper ikke dig med at finde bestemte data eller handlinger. 

[![søgefeltet i](./media/search-box.png)](./media/search-box.png) navigation søgefunktionen fungerer også som en enestående mulighed at navigere hurtigt til en bestemt side. For eksempel, hvis du er en kreditor medarbejder der ofte bruger den **betalingskladde** side, kan du angive "betalingskladde" i søgefeltet. Fordi inputtet er et nøjagtigt match for sidetitel, siden vises øverst i søgeresultaterne, og du kan hurtigt navigere til den. 

[![søgning-til-betaling-kladde](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Listen over søgeresultater vises sidetitel samt navigationssti. Dette hjælper med at gøre dig opmærksom på placeringen af siden i programmet. Det hjælper dig også med at skelne mellem to eller flere lignende sider i resultaterne. Når du søger efter en side, sammenholdes dit input mod sidens titel samt dens navigationssti. For eksempel, hvis du angiver "indgående" i den ** ** søgefeltet, vises resultaterne for de sider, der er tilgængelige i området Debitor – selvom sidetitlerne ikke indeholder ordet "indgående". 

[![Søg-for-the-word-debitor](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Navigationen Søg funktioner kun overflader fra et forvaltnings- og sikkerhedsmæssigt perspektiv:

-   Sider, der er aktiveret i den aktuelle konfiguration (via konfigurationsnøgler).
-   Sider, som brugeren har adgang til baseret på brugerens rolle

Listen over søgeresultater er begrænset til 10 elementer. Hvis du ikke kan finde det, du søger, i resultaterne, skal du prøve at afgrænse eller opdatere inputtet. Fra et udviklingsperspektiv er funktionen til navigationssøgning meget nem at udnytte, da der praktisk talt ikke er nogen forsinkelse mellem implementering af menupunkter og deres evne til at blive vist i søgeresultater. Så længe menupunkterne er tilknyttet fra navigationsruden eller dashboardet, bliver det automatisk muligt at søge i dem. Funktionen til navigationssøgning indeholder også en meget efterspurgt funktion for Superbrugere: muligheden for hurtigt at navigere til en side baseret på formens tekniske navn. Mange brugere er så fortrolig med systemet, at nøjagtigt ved, hvilke formularnavne de arbejder med. Hvis du er en af disse brugere, kan du angive **form:** efterfulgt af navnet på den form, du søger efter. Hvis du for eksempel angiver **form: kreditorfaktura**, viser søgeresultaterne alle sider, hvor formens navn starter med **kreditorfaktura**. 

[![Søg efter-formular vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)


