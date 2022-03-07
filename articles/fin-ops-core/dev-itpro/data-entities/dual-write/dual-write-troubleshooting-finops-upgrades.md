---
title: Fejlfinde fejl fra opgraderinger af Finans og drift-apps
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til opgraderinger af Finans- og driftsapps.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c7c036ef44b0470c9b3f8087e7b5b1e16dde1b34
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062819"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Fejlfinde fejl fra opgraderinger af Finans og drift-apps

[!include [banner](../../includes/banner.md)]





Dette emne indeholder fejlfindingsoplysninger for dobbeltskrivning mellem Finans- og driftsapps og Dataverse. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til opgraderinger af Finans- og driftsapps.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="database-synchronization-errors"></a>Fejl ved databasesynkronisering

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist en fejlmeddelelse, der ligner følgende eksempel, når du forsøger at bruge tabellen **DualWriteProjectConfiguration** til at opdatere Finans- og driftsapps til Platform Update 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Følg disse trin for at løse dette problem.

1. Log på den virtuelle maskine (VM) for Finans- og driftsapps.
2. Åbn Visual Studio som administrator, og åbn applikationsobjekttræet (AOT).
3. Søg efter **DualWriteProjectConfiguration**.
4. I applikationsobjekttræet skal du højreklikke på **DualWriteProjectConfiguration** og vælge **Føj til nyt projekt**. Vælg **OK** for at oprette det nye projekt, der bruger standardindstillinger.
5. Højreklik på **Projektegenskaber** i Solution Explorer, og indstil **Synkroniser database i Build** til **True**.
6. Byg projektet, og bekræft, at buildet fungerer korrekt.
7. Vælg **Synkroniser database** i menuen **Dynamics 365**.
8. Vælg **Synkroniser** for at foretage en komplet databasesynkronisering.
9. Når hele database synkroniseringen er udført korrekt, skal du køre databasesynkroniseringstrinnet igen i Microsoft Dynamics Lifecycle Services (LCS) og bruge de manuelle opgraderingsscripts, så du kan fortsætte med opdateringen.

## <a name="missing-table-columns-issue-on-maps"></a>Problem med manglende tabelkolonner i tilknytning

**Påkrævet rolle for at rette fejlen:** Systemadministrator

På siden **Dobbeltskrivning** kan du få vist en fejlmeddelelse, der ligner følgende eksempel:

*Manglende kildefelt \<field name\> i skemaet.*

![Eksempel på fejlmeddelelsen om manglende kildekolonne.](media/error_missing_field.png)

Hvis du vil løse problemet, skal du først følge disse trin for at sikre, at kolonnerne findes i tabellen.

1. Log på VM for Finans- og driftsapps.
2. Gå til **Arbejdsområder \> Datastyring**, vælg feltet **Rammeparametre**, og vælg derefter **Opdater tabelliste** under fanen **Tabelindstillinger** for at opdatere tabellerne.
3. Gå til **Arbejdsområder \> Datastyring**, vælg fanen **Datatabeller**, og kontrollér, at tabellen er vist. Hvis tabellen ikke vises, skal du logge på den VM for Finans- og driftsappen og kontrollere, at tabellen er tilgængelig.
4. Åbn siden **Tabeltilknytning** fra siden **Dobbeltskrivning** i Finans- og driftsappen.
5. Vælg **Opdater tabelliste**, så kolonnerne i tabeltilknytninger automatisk udfyldes.

Hvis problemet stadig ikke er løst, skal du følge disse trin.

> [!IMPORTANT]
> Disse trin fører dig gennem processen til sletning af en tabel og derefter tilføjelse af den igen. Hvis du vil undgå problemer, skal du sørge for at følge trinene nøjagtigt.

1. Gå i Finans- og driftsappen til **Arbejdsområder \> Datastyring**, og vælg feltet **Datatabeller**.
2. Find den tabel, der mangler attributten. Klik på **Rediger måltilknytning** på værktøjslinjen.
3. Klik på **Generér tilknytning** i ruden **Knyt midlertidig placering til mål**.
4. Åbn siden **Tabeltilknytning** fra siden **Dobbeltskrivning** i Finans- og driftsappen.
5. Hvis attributten ikke udfyldes automatisk på tilknytningen, skal du tilføje den manuelt ved at klikke på knappen **Tilføj attribut** og derefter klikke på **Gem**. 
6. Vælg tilknytningen, og klik på **Kør**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]