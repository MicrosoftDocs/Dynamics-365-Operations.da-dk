---
title: Foretage fejlfinding af problemer med opgraderinger af Finance and Operations-apps
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til opgraderinger af Finance and Operations-apps.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 5a68e17e3bce4efdd1a10f8f8319ff996690604572d57e9f8232f5ec45fa39e7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728157"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Foretage fejlfinding af problemer med opgraderinger af Finance and Operations-apps

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til opgraderinger af Finance and Operations-apps.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="database-synchronization-errors"></a>Fejl ved databasesynkronisering

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist en fejlmeddelelse, der ligner følgende eksempel, når du forsøger at bruge tabellen **DualWriteProjectConfiguration** til at opdatere en Finance and Operations-app til Platform Update 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Følg disse trin for at løse dette problem.

1. Log på den virtuelle maskine (VM) for Finance and Operations-appen.
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

1. Log på den virtuelle maskine for Finance and Operations-appen.
2. Gå til **Arbejdsområder \> Datastyring**, vælg feltet **Rammeparametre**, og vælg derefter **Opdater tabelliste** under fanen **Tabelindstillinger** for at opdatere tabellerne.
3. Gå til **Arbejdsområder \> Datastyring**, vælg fanen **Datatabeller**, og kontrollér, at tabellen er vist. Hvis tabellen ikke vises, skal du logge på den virtuelle maskine for Finance and Operations-appen og kontrollere, at tabellen er tilgængelig.
4. Åbn siden **Tabeltilknytning** fra siden **Dobbeltskrivning** i Finance and Operations-appen.
5. Vælg **Opdater tabelliste**, så kolonnerne i tabeltilknytninger automatisk udfyldes.

Hvis problemet stadig ikke er løst, skal du følge disse trin.

> [!IMPORTANT]
> Disse trin fører dig gennem processen til sletning af en tabel og derefter tilføjelse af den igen. Hvis du vil undgå problemer, skal du sørge for at følge trinene nøjagtigt.

1. Gå i Finance and Operations-appen til **Arbejdsområder \> Datastyring**, og markér feltet **Datatabeller**.
2. Find den tabel, der mangler attributten. Klik på **Rediger måltilknytning** på værktøjslinjen.
3. Klik på **Generér tilknytning** i ruden **Knyt midlertidig placering til mål**.
4. Åbn siden **Tabeltilknytning** fra siden **Dobbeltskrivning** i Finance and Operations-appen.
5. Hvis attributten ikke udfyldes automatisk på tilknytningen, skal du tilføje den manuelt ved at klikke på knappen **Tilføj attribut** og derefter klikke på **Gem**. 
6. Vælg tilknytningen, og klik på **Kør**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]