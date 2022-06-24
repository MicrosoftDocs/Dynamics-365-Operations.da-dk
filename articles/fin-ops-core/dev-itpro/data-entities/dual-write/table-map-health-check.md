---
title: Fejlkoder for tabeltilknytningens sundhedskontrol
description: Denne artikel indeholder en beskrivelse af fejlkoder for sundhedskontrol af tilknytningen.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 3ae78077fc716311c38620b14665af3983a44c2d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884077"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Fejlkoder for tabeltilknytningens sundhedskontrol

[!include [banner](../../includes/banner.md)]



Denne artikel indeholder en beskrivelse af fejlkoder for sundhedskontrol af tilknytningen.

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

## <a name="error-1800"></a>Fejl 1800
Fejlmeddelelsen er" "Datakilde: {} for enheden CustCustomerV3Entity omfatter en intervalværdi. Indgående postkonfigurationer fra Dataverse til Finans og drift kan påvirkes af intervalværdier på enheden. Test postopdateringerne fra Dataverse til Finans og drift med poster, der ikke opfylder filtrerkriterierne, for at validere dine indstillinger."

Hvis der er angivet et interval for enheden i programmer til finans og drift, skal den indgående synkronisering fra Dataverse til programmer til finans og drift testes for opdateringsfunktionsmåden på poster, der ikke opfylder dette intervalkriterium. Enhver post, der ikke matcher intervallet, behandles som en indsættelseshandling af enheden. Hvis der er en eksisterende post i den underliggende tabel, mislykkes indsættelsen. Det anbefales, at du tester dette brugsmønster for alle scenarier, før du udruller til produktion.

## <a name="error-1900"></a>Fejl 1900
Fejlmeddelelsen er: "Enhed: har {} datakilder, som ikke spores for udgående dobbeltskrivning. Dette kan påvirke ydeevnen af live-synkroniseringsforespørgslen. Du skal redigere enheden i Finans og drift for at fjerne ubrugte datakilder og tabeller eller implementere getEntityRecordIdsImpactedByTableChange for at optimere kørselsforespørgslerne."

Hvis der er mange datakilder, der ikke bruges til sporing i den faktiske live synkronisering fra programmer til finans og drift, er der en mulighed for, at enhedsydeevnen påvirker live-synkronisering. Hvis du vil optimere de sporede tabeller, skal du bruge metoden getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Fejl 5000
Fejlmeddelelsen er, "Synkrone plugins er registreret for datastyringshændelser for enhedskonti. Dette kan have indflydelse på den første synkronisering og ydeevnen for live-synkroniseringsimport i Dataverse. For at opnå den bedste ydeevne skal du ændre plugins til asynkron behandling. Liste over registrerede plugins {}."

Synkrone plugins i en Dataverse-enhed kan påvirke ydeevnen for live synkronisering og indledende synkronisering, mens der føjes til transaktionsindlæsning. Den anbefalede fremgangsmåde er enten at deaktivere plugins eller gøre disse plugins asynkrone, hvis du har langsommere indlæsningstider i første synkronisering eller live synkronisering for en bestemt enhed.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
