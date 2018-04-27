---
title: Konfigurere bedragerimeddelelser
description: "Dette emne forklarer, hvordan du opretter regler for at advare kundeservicemedarbejdere om potentielt falske oplysninger ved behandling af ordrer. Du kan definere bestemte koder, der skal bruges for automatisk eller manuelt at sætte mistænkelige ordrer på hold."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Konfigurere advarsler om svindel

[!INCLUDE [banner](includes/banner.md)]

I dette emne forklares, hvordan du definerer kriterier og regler for placering af potentielt falsk salgsordrer på hold til fornyet gennemgang. Funktionen til gennemsyn af svindel bruges til at bestemme gyldigheden af oplysningerne i en salgsordre. Hvis oplysningerne i salgsordren viser sig at være tvivlsomme baseret på en organisations svindelkriterier og -regler, kan ordren sættes på hold for fornyet gennemgang af en administrator.

> [!NOTE]
> Denne funktion kan kun bruges i forbindelse med behandling af salgsordrer i Retail-callcenterkanalen. 

Når callcenterkanalen defineres, skal **Aktivér ordrefuldførelse** angives til **Ja**. Når ordrefærdiggørelse er aktiveret, kan brugere få vist en opsummering på ordren og klikke på **Send** for at færdiggøre ordren. Brugere får også mulighed for manuelt at placere salgsordren på hold til gennemsyn for snyd. Salgsordrer, der indtastes af en callcenter-bruger, behandles via regler og kriterier for kontrol for svindel under processen Send.

Der findes to typer svindelkriterier, som systemet skal referere til for at kontrollere, om ordren skal holdes til gennemsyn for svindel:

-   **Statiske regler** bruger en bestemt værdi, f.eks. et telefonnummer, der er blevet sortlistet eller en mailadresse, der er markeret som værende kendt for at være brugt til tidligere falske transaktioner. På siden **Statiske svindeldata** kan svindeloplysninger tilføjes manuelt eller via dataimport med resultater, der er knyttet til oplysninger og svindlen. Hvis svindelkontrol er aktiveret, sammenlignes hver salgsordre, der er indtastes, med de statiske data. Hvis dataene findes i enten kundens fakturerings- eller leveringsadresse, eller hvis dataene findes i leveringsadressen på salgslinjen, opsummeres resultaterne af alle entydige sammenfald.  
-   **Dynamiske regler** består af variabler og betingelser, der er defineret for disse variabler. Med dynamiske regler kan andre kriterier, der ikke er defineret i de statiske regler, kontrolleres. Mere komplekse "OG/ELLER"-sætninger kan bruges til at overveje flere betingelser for at afgøre, om der er et positivt match i forhold til regelkriterierne og den salgsordre, der sendes. Hvis en bruger f.eks. ønsker at tilbageholde alle ordrer fra kunder, der er knyttet til en bestemt kundegruppeværdi, og som har bestilt et bestemt produkt, til gennemsyn af svindel, vil betingelserne for at validere debitor og validere produkter være defineret på siden **Regler** med en "OG"-betingelse. Ordren falder kun i tilbagehold for svindel, hvis begge betingelser er opfyldt, og hvis den scoreværdi, der er tildelt til reglen, bringer ordrens totale svindelscore over den minimumssvindelscore, som er defineret i callcenter-parametre.

En callcenter-bruger kan også manuelt placere en ordre i køen for svindeltilbageholdelse. Hvis brugeren, der angiver rækkefølgen, mener, at kunden, som afgiver ordren, kan være mistænkelig og ønsker, at en anden gennemser gyldigheden af ordren, før den behandles, kan brugeren, der indtaster ordren, vælge indstillingen **Manuelt svindelhold** på rullemenuen **På hold** på siden **Salgsordreoversigt** (der vises, når ordrefunktionen **Fuldført** kaldes). Brugeren vil blive bedt om at indtaste en bemærkning for at yderligere at forklare, hvorfor de mener, at ordren kan være falsk, så validatoren har mere kontekst.

Alle ordrer, der holdes via manuel svindelhold eller systematisk beregning af svindelscore, vises på siden **Ordrer på hold** side, hvor ordren kan gennemses og derefter enten annulleres eller frigives til behandling.

> [!NOTE]
> Brug af flere regler eller overdrevent komplekse regler resulterer i dårlig systemydeevne, når salgsordrer sendes. Svindelpåmindelsesfunktionen er ikke optimeret til at håndtere en stor mængde statiske svindeldataværdier og mange aktive regler. Det er vigtigt at huske, at hver regel evalueres i funktionen Send i indtastning af callcenter-salgsordrer. Reglerne skal evalueres mod salgsordrehovedet og alle ordrelinjer. Jo flere regler og jo mere avancerede regelsætninger der er, desto længere tager behandlingen. Hvis du har et stort antal linjeelementer på din ordre, og et stort antal aktive regler og statiske dataværdier, kan denne systematisk proces til at gennemse og validere alle data og beregning af svindelscore have en betydelig påvirkning på ydeevnen.  Organisationer, der bruger denne funktion skal altid teste og bekræfte, at behandlingstiden ved ordreafgivelse er acceptabelt, før der anvendes ændringer af regler eller statiske svindelkriterier i produktionsmiljøet.

