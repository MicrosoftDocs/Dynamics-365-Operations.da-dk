---
title: Optimere BYOD-planlagte batchjob
description: I dette emne forklares det, hvordan du kan optimere ydeevnen, når du bruger funktionen Bring din egen database (BYOD) sammen med Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 4b9cf4b4181b64ef4daf397edd852fb2f881424e
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111854"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>Optimere BYOD-planlagte batchjob

I dette emne forklares det, hvordan du kan optimere ydeevnen, når du bruger funktionen Bring din egen database (BYOD). Yderligere oplysninger om BYOD finder du i afsnittet [Bruge din egen database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json).

## <a name="performance-considerations-for-data-export"></a>Overvejelser om ydeevne for dataeksport

Når enheder er publiceret til destinationsdatabasen, kan du bruge eksportfunktionen i arbejdsområdet **Dataadministration** til at flytte data. Med eksportfunktionen kan du definere et job til dataflytning, der indeholder en eller flere enheder. Du kan finde flere oplysninger om dataeksport i [Oversigt over dataimport og eksportjob](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json).

Du kan bruge siden **Eksportér** til at eksportere data til forskellige destinationsdataformater, f.eks. en CSV-fil (kommaseparerede værdier). Denne side understøtter også SQL-databaser som en anden destination.

Du kan oprette et dataprojekt med flere enheder og bruge et batchjob til at planlægge dette dataprojekt til kørsel. Hvis du vælger indstillingen **Eksportér i batch**, kan du planlægge, at dataeksportjobbet skal køres med jævne mellemrum.

Du skal være omhyggelig, når du føjer flere enheder til et eksportprojekt, for at bevare den overordnede pålidelighed i BYOD-eksporten. Når du bestemmer antallet af enheder, der skal føjes til det samme projekt, skal du overveje følgende parametre:

- Kompleksiteten af enhederne
- Den forventede datamængde pr. enhed
- Den samlede tid, der skal bruges til at udføre eksporten på jobniveau

Hvis du vil opnå den bedste ydeevne, skal du undgå at tilføje hundredvis af enheder i et enkelt projekt. Det anbefales, at du opretter flere job, der hver især indeholder færre enheder.

## <a name="scheduling-byod-batch-jobs"></a>Planlægning af BYOD-batchjob

For at reducere påvirkningen hos brugere af Microsoft Dynamics 365 Human Resources, skal du køre BYOD-batchjob om natten eller efter arbejdstid. Sørg for at kontrollere tidszonen for tilbagevendende batchjob. Nogle batchjob bruger muligvis Pacific Standard Time (PST).

Som en hjælp til at undgå problemer med ydeevnen skal du overveje følgende faktorer, når du konfigurerer planlægningsfrekvensen for BYOD-batchjob:

- Den tid, det tager at udføre hvert batchjob
- Forretningsbehovet for dataene i BYOD

Angiv frekvensen for hvert batchjob til en værdi, der sikrer, at jobbet kan fuldføres korrekt før den næste planlagte kørselstid. Undgå at køre flere job parallelt, da denne fremgangsmåde kan have en negativ indvirkning på ydeevnen for Human Resources.

Hvis du vil opnå den bedste ydelse, skal du altid bruge indstillingen **Eksportér i batch** på siden **Eksportér** til at planlægge BYOD. Undgå at planlægge tilbagevendende eksport ved **Administrer \> Administrer tilbagevendende datajobs**.

## <a name="incremental-export"></a>Trinvis eksport

Når du tilføjer en enhed til dataeksport, kan du enten foretage en trinvis push (eksport) eller en fuld push. En fuld push sletter alle eksisterende poster fra en enhed i BYOD-databasen. Derefter indsættes det aktuelle sæt poster fra Human Resources-enheden.

Hvis du vil udføre en trinvis push, skal du aktivere registrering af ændringer for de enkelte enheder på siden **Enheder**. Du kan finde flere oplysninger under [Aktivere ændringssporing for enheder](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).

Hvis du vælger trinvis push, er den første push altid en fuld push. SQL registrerer ændringer fra denne første fulde push. Når der indsættes en ny post, eller når en post opdateres eller slettes, afspejles ændringen i destinationsenheden.

## <a name="time-outs"></a>Timeout

Følgende er standardtimeout for BYOD-eksporter:

- Ti minutter for afkortende handlinger
- En time for masseindsættelser

Når mængden er høj, er disse timeoutindstillinger muligvis ikke tilstrækkelige. Hvis du vil opdatere dem, skal du gå til **Dataadministration \> Rammeparametre \> Brug din egen database**. Disse timeout er firmaspecifikke og skal angives separat for hvert firma.

## <a name="known-limitations"></a>Kendte begrænsninger

BYOD-funktionen har følgende begrænsninger:

- Der må ikke være aktive låse i databasen under synkronisering. Aktive låse kan forårsage langsomme skrivninger eller endda manglende eksport af data til din Azure SQL-database.
- Du kan ikke eksportere sammensatte enheder til din egen-database. I øjeblikket understøttes sammensatte enheder ikke. Du skal eksportere de enkelte enheder, der udgør den sammensatte enhed. Du kan dog eksportere begge enheder i det samme dataprojekt.
- Enheder, der ikke har entydige nøgler, kan ikke eksporteres ved hjælp af trinvis push. Du kan komme ud for denne begrænsning, især når du forsøger at eksportere poster gradvist fra nogle få enheder, der er færdiggjort. Da disse enheder er designet til at muliggøre import af data, har de ikke en entydig nøgle.

## <a name="troubleshooting"></a>Fejlfinding

### <a name="incremental-push-doesnt-work-correctly"></a>Trinvis push fungerer ikke korrekt

**Problem:** Når der foretages en fuld push for en enhed, kan du se et stort sæt poster i BYOD, når du bruger en **select**-sætning. Men når du foretager en trinvis push, får du kun vist nogle få poster i BYOD. Det ser ud til, at den trinvise push slettede alle poster og kun tilføjede de ændrede poster i BYOD.

**Løsning:** SQL-ændringssporingstabellerne er muligvis ikke i den forventede tilstand. I tilfælde af denne type anbefales det, at du slår sporing af ændringer fra for enheden og derefter aktiverer den igen. Du kan finde flere oplysninger under [Aktivere ændringssporing for enheder](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).

## <a name="see-also"></a>Se også

[Oversigt over datastyring](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages?toc=/dynamics365/human-resources/toc.json)<br>
[Brug din egen database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json)<br>
[Oversigt over dataimport- og -eksportjob](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json)<br>
[Aktivere ændringssporing for enheder](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]