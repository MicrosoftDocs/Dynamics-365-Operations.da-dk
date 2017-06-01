---
title: Oprette et kontinuitetsprogram for et callcenter
description: I denne artikel beskrives det, hvordan du kan konfigurere et kontinuitetsprogram for et call center.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c0a9eec6bdf67deca885b30082b958869e64aae2
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Oprette et kontinuitetsprogram for et callcenter

[!include[banner](includes/banner.md)]


I denne artikel beskrives det, hvordan du kan konfigurere et kontinuitetsprogram for et call center.

I et kontinuitetsprogram, som er også kendt som et tilbagevendende ordreprogram, modtagerne kunderne regelmæssigt produktleverancer i henhold til en foruddefineret tidsplan. Hver leverance kan indeholde et andet produkt, f.eks. månedens bog i en bogklub, eller det samme produkt kan sendes flere gange. Hvis du vil konfigurere et kontinuitetsprogram, skal du udføre følgende opgaver.

1.  Angiv kontinuitetsparametrene på siden **Call center-parametre**.
2.  Opret et kontinuitetsprogram, som angiver oplysninger som f.eks. betalingsplan, tidspunktet for leverancerne og om fakturering skal ske på forhånd. Du skal også tilføje en liste over produkter, der indgår i kontinuitetsprogrammet. Hvert produkt modtager et hændelses-id-nummer, der tildeles fortløbende, startende med 1. Hændelsen id'erne bestemmer den rækkefølge, produkter sendes i.
    -   Hvis kunder modtager et andet produkt i hver leverance, sendes produkterne i sekventiel rækkefølge baseret på deres hændelses-id'er, begyndende med den aktuelle hændelse.
    -   Hvis kunder modtager det samme produkt i hver leverance, indeholder listen kun ét produkt, der har et hændelses-id. Den samme hændelse forekommer flere gange. Du kan angive, hvor mange gange hver hændelse gentages.

3.  Opret et overordnet produkt, der repræsenterer det kontinuitetsprogram, du oprettede i opgave 2. Hvis du føjer produktet til en salgsordre, åbnes siden **Kontinuitet**. Du kan derefter bruge denne side til at oprette den faktiske kontinuitetsrækkefølge. Det overordnede produkt angiver ikke de enkelte produkter, som kunden modtager i hver leverance.

Når du har oprettet et kontinuitetsprogram som beskrevet ovenfor , kan du oprette en kontinuitetsordre for en debitor. Du er muligvis nødt til at udføre følgende disse ekstra vedligeholdelsesopgaver.

-   **Opdater kontinuitetens aktuelle hændelsesperiode** – Opret et batchjob, der fortæller systemet, hvad den aktuelle hændelsesperiode er.
-   **Opret underordnede kontinuitetsordrer** – Opret underordnede ordrer fra den overordnede kontinuitetsordre.
-   **Behandl kontinuitetsbetalinger** – Behandl fakturering og meddelelser om betalinger, der er knyttet til kontinuitetssalgsordrer.
-   **Udvid om nødvendigt kontinuitetslinjer** – Udvid det antal gange, en kontinuitetshændelse kan gentages. Gentagelsen af forsendelser kan derefter går ud over den grænse, der er angivet i feltet **Grænse for gentagelse af kontinuitet** i call center-parametrene.
-   **Udfør om nødvendigt en kontinuitetsopdatering** – Synkroniser ændringer mellem kontinuitetsprogrammet og de overordnede kontinuitetssalgsordrer.
-   **Luk overordnede kontinuitetslinjer og ordrer** – Luk kontinuitetsordrer.





