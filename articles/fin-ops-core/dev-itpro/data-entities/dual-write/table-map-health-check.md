---
title: Fejlkoder for sundhedskontrol af tabeltilknytningen
description: Dette emne indeholder en beskrivelse af fejlkoder for sundhedskontrol af tilknytningen.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061272"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Fejlkoder for sundhedskontrol af tabeltilknytningen

[!include [banner](../../includes/banner.md)]



Dette emne indeholder en beskrivelse af fejlkoder for sundhedskontrol af tilknytningen.

## <a name="error-100"></a>Fejl 100

Fejlmeddelelsen er "Der anbefales som minimum Finans- og driftsplatform version PU 43 for at køre Finans- og driftsanbefalinger".

Funktionen kræver platformopdateringer til version 10.0.19 eller nyere af Finans- og driftsapps.

## <a name="error-400"></a>Fejl 400

Fejlmeddelelsen er "Ingen registreringsdata for forretningshændelser blev fundet for enheden \{Finans og drift-UniqueEntityName\}, hvilket betyder, at tilknytningen enten ikke kører, eller alle felttilknytningerne er envejs."

## <a name="error-500"></a>Fejl 500

Fejlmeddelelsen er "Der blev ikke fundet nogen projektkonfigurationer for projektet \{projektnavn\}. Det kan enten skyldes, at projektet ikke er aktiveret, eller at alle felttilknytninger er envejs fra kundeengagement til Finans og drift."

Kontrollér tilknytningerne for tabeloversigten. Hvis de er envejs fra kundeengagementsapps til Finans- og driftsapps, genereres der ingen trafik til live-synkronisering fra Finans- og driftsapps til Dataverse.

## <a name="error-900"></a>Fejl 900

Fejlmeddelelsen er "Udyldigt kildefilter \{sourceFilter\}-format for enheden \{Finans og drift-UniqueEntityName\}."

Det kildefilter, der er angivet i tabeltilknytningen for Finans- og driftsapps, er ikke korrekt syntaks. Se [Fejlfinde problemer med aktiv synkronisering](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps) for at validere filterkriterierne.

## <a name="error-1000"></a>Fejl 1000

Fejlmeddelelsen er "Den enhedsforespørgsel \{Finans og drift-UniqueEntityName\}, der bruges til live-synkronisering af dobbeltskrivning, er \{Finans og drift-EntityFilterQueryString\}. Poster, der opfylder forespørgselskriterierne, anvendes til live-synkronisering."

Den enhedsforespørgsel, der blev returneret, er den understøttende SQL-forespørgsel for enheden. Kontrollér, om der er indre joinforbindelser eller filtre i forespørgslen, som bestemmer, hvilke forretningsdata der anvendes til live-synkronisering. Indre joinforbindelser og filtre er obligatoriske betingelser, der skal være opfyldt for hver post, som vælges med henblik på live-synkronisering af dobbeltskrivning.

## <a name="error-1300"></a>Fejl 1300

Fejlmeddelelsen er "Virtuelle felter \{s.EntityFieldName\} for enheden \{Finans og drift EntityMetadata.EntityProperties.LogicalEntityName\} spores muligvis ikke med henblik på dobbeltskrivning."

Virtuelle felter fra Finans- og driftstabeller kan ikke spores. Live-synkronisering kan synkronisere dataene, men kan ikke registrere de ændringer, der er foretaget i kolonnerne.

## <a name="error-1500"></a>Fejl 1500

Fejlmeddelelsen er "Der skal være knyttet mindst ét felt til et ikke-opslagsfelt for kundeengagement for at gøre det muligt at spore datakilden \{datasource.DataSourceName\}."

Datakilden fra enheden har ingen felter, der er knyttet til dobbeltskrivning. Ændringer i den underliggende tabel spores ikke for dobbeltskrivning.

## <a name="error-1600"></a>Fejl 1600

Fejlmeddelelsen er "Datakilde: \{datasource.DataSourceName\} for enheden \{Finans og drift EntityMetadata.EntityProperties.LogicalEntityName\} har et område. Kun poster, der opfylder områdebetingelsen, anvendes som udgående."

Enheder i Finans- og driftsapps kan have datakilder, hvor filterområder er aktiveret. Disse områder definerer de poster, der anvendes som en del af live-synkronisering. Hvis nogle af posterne springes over fra Finans- og driftsapps til Dataverse, skal du kontrollere, om posterne opfylder områdekriterierne på enheden. Det kan du ganske enkelt gøre ved at køre en SQL-forespørgsel, der ligner følgende eksempel.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Fejl 1700

Fejlmeddelelsen er "Tabel: \{datasourceTable.Key.subscribedTableName\} for enheden \{datasourceTable.Key.entityName\} spores for enheden \{origTableToEntityMaps.EntityName\}. De samme tabeller, der spores for flere enheder, kan have indflydelse på systemets ydeevne for transaktioner med live-synkronisering."

Hvis den samme tabel spores af flere enheder, vil en eventuel ændring i tabellen udløse evaluering af dobbeltskrivning for de tilknyttede enheder. Selvom filtersætningerne kun sender de gyldige poster, kan evalueringen forårsage et ydeevneproblem, hvis der er forespørgsler, som kører længe, eller forespørgselsplaner, der ikke er optimeret. Dette problem kan muligvis ikke undgås ud fra et forretningsmæssigt perspektiv. Men hvis der er mange tabeller med skæringspunkter på tværs af flere enheder, skal du overveje at forenkle enheden eller kontrollere, om enhedsforespørgsler er optimeret.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
