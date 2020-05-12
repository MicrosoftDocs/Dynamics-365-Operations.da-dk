---
title: Foretage fejlfinding af problemer i forbindelse med opgraderinger af Finance and Operations-apps
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til opgraderinger af Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 53df00de82b101aa02160d865a9c3bbebcfcae15
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275458"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Foretage fejlfinding af problemer i forbindelse med opgraderinger af Finance and Operations-apps

[!include [banner](../../includes/banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til opgraderinger af Finance and Operations-apps.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="database-synchronization-errors"></a>Fejl ved databasesynkronisering

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist en fejlmeddelelse, der ligner følgende eksempel, når du forsøger at bruge **DualWriteProjectConfiguration**-enheden til at opdatere en Finance and Operations-app til Platform Update 30.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
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

## <a name="missing-entity-fields-issue-on-maps"></a>Problemer med manglende enhedsfelter i tilknytninger

**Påkrævet rolle for at rette fejlen:** Systemadministrator

På siden **Dobbeltskrivning** kan du få vist en fejlmeddelelse, der ligner følgende eksempel:

*Manglende kildefelt \<feltnavn\> i skemaet.*

![Eksempel på fejlmeddelelsen om manglende kildefelt](media/error_missing_field.png)

Hvis du vil løse problemet, skal du først følge disse trin for at sikre, at felterne findes i enheden.

1. Log på den virtuelle maskine for Finance and Operations-appen.
2. Gå til **Arbejdsområder \> Datastyring**, vælg feltet **Rammeparametre**, og vælg derefter **Enhedsindstillinger** under fanen **Opdater liste over enheder** for at opdatere enhederne.
3. Gå til **Arbejdsområder \> Datastyring**, vælg fanen **Dataenheder**, og kontroller, at enheden er angivet. Hvis enheden ikke vises, skal du logge på den virtuelle maskine for Finance and Operations-appen og kontrollere, at enheden er tilgængelig.
4. Åbn siden **Enhedstilknytning** fra siden **Dobbeltskrivning** i Finance and Operations-appen.
5. Vælg **Opdater liste over enheder**, så felterne i enhedstilknytninger automatisk udfyldes.

Hvis problemet stadig ikke er løst, skal du følge disse trin.

> [!IMPORTANT]
> Disse trin fører dig gennem processen til sletning af en enhed og derefter tilføjelse af den igen. Hvis du vil undgå problemer, skal du sørge for at følge trinene nøjagtigt.

1. Gå i Finance and Operations-appen til **Arbejdsområder \> Datastyring**, og marker feltet **Dataenheder**.
2. Find den enhed, der mangler attributten. Klik på **Rediger måltilknytning** på værktøjslinjen.
3. Klik på **Generér tilknytning** i ruden **Knyt midlertidig placering til mål**.
4. Åbn siden **Enhedstilknytning** fra siden **Dobbeltskrivning** i Finance and Operations-appen.
5. Hvis attributten ikke udfyldes automatisk på tilknytningen, skal du tilføje den manuelt ved at klikke på knappen **Tilføj attribut** og derefter klikke på **Gem**. 
6. Vælg tilknytningen, og klik på **Kør**.