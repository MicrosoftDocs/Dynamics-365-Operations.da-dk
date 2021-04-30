---
title: Ofte stillede spørgsmål om udgivelse
description: Dette emne indeholder ofte stillede spørgsmål om, hvordan du udgiver et Dynamics 365 Human Resources-implementeringsprojekt.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b4b336953ef6bd74da009b3bb44fbcf2eab5a8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892317"
---
# <a name="go-live-faq"></a>Ofte stillede spørgsmål om udgivelse 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emne indeholder ofte stillede spørgsmål om, hvordan du udgiver et Dynamics 365 Human Resources-implementeringsprojekt. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Hvornår kan jeg konfigurere og anmode om mit produktionsmiljø? 

Et produktionsmiljø kan i de fleste tilfælde implementeres, når følgende kriterier er opfyldt:

- Alle tilpasninger er code-complete (kræver ikke tilføjelse af helt ny kildekode).
- Når test af brugeraccept (UAT) er fuldført.
- Kunden har godkendt løsningen.
- Ingen problemer blokerer for udgivelsen. 

Når kvalificerede kunder er på dette trin, kan Microsoft FastTrack-teamet samarbejde med projektteamet om at foretage en udgivelsesvurdering. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Hvad er forudsætningerne for at implementere et produktionsmiljø? 

Du kan se en liste over forudsætninger under  [Forberede til udgivelse](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Hvad er en udgivelsesvurdering?  

En udgivelsesvurdering er en del af  [Microsoft FastTrack-programmet](/dynamics365/fasttrack/). Under denne gennemgang vurderer en løsningsarkitekt, om et implementeringsprojekt er klar til cutover-overgangsfasen og udgivelse. Denne gennemgang er obligatorisk for ethvert implementeringsprojekt, før du kan anmode om udgivelse i et produktionsmiljø. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Vores sandkassemiljøer implementeres i det centrale USA's datacenter. Vi ønsker, at vores produktionsmiljøer skal implementeres i det vestlige USA's datacenter. Kan jeg vælge Det vestlige USA som datacenter i min produktionskonfiguration? 

LCS forhindrer ikke valg af et andet datacenter, når du implementerer et Human Resources-miljø, men det kan ikke anbefales at vælge et andet datacenter.  

Hvis du vil placere dit produktionsmiljø i Det vestlige USA's datacenter, skal du først geninstallere dine sandkassemiljøer i Det vestlige USA's datacenter, teste dem og derefter godkende. 

Oplysninger om, hvordan du vælger det korrekte datacenter, finder du under [Netværkskrav](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Hvilket adgangsniveau skal jeg bruge til Azure-ressourcerne i mine Human Resources-miljøer?  

Adgang til Human Resources-miljøer er begrænset. Du kan ikke få adgang til den virtuelle maskine (VM) eller Microsoft Internet Information Services (IIS). Du kan heller ikke få adgang til databasen via Microsoft SQL Server Management Studio. 

Selvom du ikke kan få adgang til dine Azure-ressourcer eller Dynamics 365 Human Resources-miljøer direkte, er der flere funktioner, du kan bruge til at få adgang til dine data:

- Du kan installere en Azure SQL-database i din egen Azure-lejer og bruge BYOD-funktionen (Bring Your Own Database) til at synkronisere data. Yderligere oplysninger finder du i afsnittet [Bruge din egen database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).

- Du kan bruge Dataverse-integration til at synkronisere udvalgte enheder i Dataverse-databasen. Yderligere oplysninger finder du i [Dataverse-tabeller](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Hvor ofte sikkerhedskopieres min produktionsdatabase? 

Databaser beskyttes gennem automatiske sikkerhedskopieringer med følgende frekvens:

| Backuptype | Frekvens |
| --- | --- |
| Fuld sikkerhedskopiering af database | Ugentligt |
| Differentieret sikkerhedskopiering af database | Hver 12-24. time |
| Sikkerhedskopiering af transaktionslog | Hvert 5. til 10. minut |

Microsoft opbevarer et tilstrækkeligt antal sikkerhedskopier, der giver mulighed for gendannelse til bestemt tidspunkt (PITR) inden for de seneste 14 dage. 

Du kan finde flere oplysninger i  [Få mere at vide om automatiske sikkerhedskopieringer af SQL Database](/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Kan jeg anmode om en kopi af sikkerhedskopien af min produktionsdatabase? 

Nej Du kan dog sende en serviceanmodning om en databaseopdatering for at kopiere dit produktionsmiljø til dit sandkassemiljø. Du kan installere en Azure SQL-database i din egen Azure-lejer og bruge BYOD-funktionen til at synkronisere data fra dit produktionsmiljø. Yderligere oplysninger finder du i afsnittet [Bruge din egen database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Hvordan flytter jeg mit sandkassemiljø til produktion med henblik på udgivelse? 

Da der ikke findes en kopieringsfunktion, som kan flytte miljøet fra en sandkasse til et produktionsmiljø, skal du bruge datapakker til at flytte data til produktionsmiljøet.  

Vi anbefaler, at du udarbejder en tydelig liste over enheder, der er konfigureret i sandkassen, under hele projektet. Test derefter cutover- og migreringsprocessen for eventuelle datapakker, der er nødvendige, før du kan iværksætte udgivelsen. Du skal manuelt flytte datapakker ind i produktionsmiljøet, når du er klar til udgivelse. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Hvad skal jeg gøre, hvis mit produktionsmiljø er nede? 

Hvis du vil rapportere en produktionsafbrydelse, skal du følge den proces, der er beskrevet under  [Rapportere en produktionsafbrydelse](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md). 

 ## <a name="see-also"></a>Se også

 [Forberede til udgivelse](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]