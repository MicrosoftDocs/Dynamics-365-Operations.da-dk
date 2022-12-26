---
title: Konfigurere Operational Insights
description: I denne artikel beskrives, hvordan du kan konfigurere og bruge administrere driftsindsigtsfunktionen i Microsoft Dynamics 365 Commerce.
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832118"
---
# <a name="set-up-operational-insights"></a>Konfigurere Operational Insights

[!include [banner](../includes/banner.md)]

I denne artikel beskrives, hvordan du kan konfigurere og bruge administrere driftsindsigtsfunktionen i Microsoft Dynamics 365 Commerce.

Operational Insights er en Dynamics 365 Commerce-funktion, der er udviklet til at give kunderne et bedre overblik over deres service og virksomhedsfunktionalitet ved at sende telemetri direkte til en Application Insights-konto, der ejes af kunden.

Ved at aktivere Operational Insights for dine miljøer i Commerce Headquarters kan du indsamle en liste over hændelser fra både CSU-enheder (Commerce Scale Unit) og pos-enheder. Disse hændelser kan hjælpe dig med at få en bedre forståelse af, hvordan systemerne klarer sig, og de giver dig mulighed for at overvåge de vigtigste tekniske og forretningsmæssige værdier.

Selvom du ikke vil indsamle telemetri hele tiden, kan du med fordel aktivere eller deaktivere samling for bestemte miljøer. På denne måde kan telemetry hjælpe dig med at foretage fejlfinding eller fejlfinding under udvikling eller i produktion.

## <a name="access-logs-in-application-insights"></a>Få adgang til logfiler i Application Insights

Hvis du vil have adgang til diagnosticeringshændelseslogfiler for komponenterne Commerce CSU og POS via Application Insights, skal du gennemføre procedurerne i dette afsnit.

### <a name="minimum-version-requirements-for-csu"></a>Minimumversionskrav til CSU

CSU har følgende minimumversionskrav:

- 10.0.23 (Retail Server-version 9.33.22062.15 og senere)
- 10.0.24 (Retail Server-version 9.34.22062.14 og senere)
- 10.0.25 (Retail Server-version 9.35.22062.13 og senere)
- 10.0.26 og senere (alle versioner)

### <a name="enable-diagnostic-events-in-application-insights"></a>Aktiver diagnosticeringshændelser i Application Insights

> [!IMPORTANT]
> Hvis du tidligere har brugt en eksempelversion af Operational Insights, skal du bruge følgende procedure for at aktivere Operational Insights. På denne måde sikrer du, at der kan fortsættes pålidelige og sikre adgang til hændelser.

Hvis du vil aktivere diagnosticeringshændelser for handelskomponenter, skal du have en Application Insights-konto. Du kan bruge en eksisterende konto eller [oprette en ny konto](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource). Af hensyn til beskyttelse af personlige oplysninger anbefales det, at du bruger separate Application Insights-konti til produktions-, sandboks- og udviklingsmiljøer. Når du har oprettet en konto, skal du aktivere funktionen **Operational Insights** i headquarters.

Benyt følgende fremgangsmåde for at aktivere diagnosticeringshændelser Application Insights.

1. I headquarters skal du åbne arbejdsområdet **Funktionesstyring** og aktivere funktionen **Operational Insights**.
1. Gå til **Systemadministration \> Opsætning \> Operational Insights**.
1. Angiv indstillingen **Handelskanalhændelser** til **Ja** under fanen **Konfigurer**.
1. Angiv værdier **for LCS-miljø-id** og **Miljøtilstand** i **Miljøer** for alle miljøer, hvor du planlægger at bruge Application Insights Du kan finde de enkelte miljøers miljø-id på siden **Miljødetaljer** for det pågældende miljø i Microsoft Dynamics Lifecycle Services. Dette trin er påkrævet for at hjælpe med at forhindre, at diagnosticeringshændelser ved en fejl sendes til et forkert miljø, når der udføres databasekopieringshandlinger.
1. I fanen **Application Insights-registrering** skal du angive Application Insights **Instrumenteringsnøgle**-værdien og tilhørende **Miljøtilstand**-værdi for det miljø, du planlægger at bruger til Application Insights-kontoen.
1. Når du har fuldført den foregående konfiguration, skal du køre **CDX-jobbet 1110**. Du kan vente, indtil jobbet køres af sig selv, eller du kan køre det manuelt.
1. I Lifecycle Services skal du gå til **Miljødetaljer \> Handel \> Administrer**, vælge en CSU-forekomst og derefter vælge **Genstart**. Gentag dette trin for hver CSU.
1. Gentag de foregående trin for hvert miljø, hvor du planlægger at bruge Application Insights.

> [!NOTE]
> - Telemetrihændelser i Operational Insights kan ændres. Det anbefales, at du bruger Operational Insights-hændelser til foreløbig analyse og fejlfinding alene, ikke til at definere dashboards eller påmindelser. Hvis du bruger hændelser uden for selvbetjeningsfejlfinding, anbefales det, at du validerer og opdaterer dine forespørgsler efter hver version af CSU/POS.
> - Pr. handelsversion 10.0.29 giver procedurerne i dette afsnit også mulighed for at installere POS Operational Insights-hændelser på din Application Insights-konto. Du kan finde flere oplysninger [i Operational Insights for POS – Hændelser og forespørgsler](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf).

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>Bruge DLLHost.exe.config-filen til at styre POS Operational Insights-hændelser

Bruge DLLHost.exe.config-filen til at styre POS Operational Insights-hændelser ved at følge disse trin.

1. Åbn i tekst-editoren filen **DLLHost.exe.config** i **C:\\Program files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker**.
1. I afsnittet **diagnosticsSection** skal du fjerne det XML-element på det xml-element, der har klassenavnet **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger**.
1. Gem filen.

### <a name="disable-diagnostic-events-in-application-insights"></a>Deaktiver diagnosticeringshændelser i Application Insights

> [!IMPORTANT]
> Hvis du vil deaktivere diagnosticeringshændelser og ikke længere sende dem til Application Insights, skal du gennemføre følgende procedure. Du kan deaktivere denne visningsfunktion i Funktionsstyring.

Benyt følgende fremgangsmåde for at deaktivere diagnosticeringshændelser i Application Insights.

1. I headquarters skal du gå til **Systemadministration \> Operational Insights**.
1. Angiv indstillingen **Handelskanalhændelser** til **Nej** under fanen **Konfigurer**.
1. Når du har fuldført den foregående konfiguration, skal du køre **CDX-jobbet 1110**. Du kan vente, indtil jobbet køres af sig selv, eller du kan køre jobbet manuelt.
1. I Lifecycle Services skal du gå til **Miljødetaljer \> Handel \> Administrer**, vælge en CSU-forekomst og derefter vælge **Genstart**. Gentag dette trin for hver CSU.
1. Gentag de foregående trin for hvert miljø, hvor du planlægger at deaktivere Application Insights.

Hvis du vil deaktivere diagnosticeringshændelser for et enkelt miljø, skal du slette instrumenteringsnøglen på fanen **Application Insights-registrering** under fanen i registreringsdatabasen på siden **Operational Insights**. Udfør derefter trin 3 og 4 i den foregående procedure.

> [!NOTE]
> I handelsversion 10.0.29 og derefter deaktiverer trinnene i dette afsnit også streaming af POS Operational Insights-hændelser på din Application Insights-konto. 
