---
title: Foretage fejlfinding af problemer under den første synkronisering
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.
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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172708"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Foretage fejlfinding af problemer under den første synkronisering

[!include [banner](../../includes/banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering. 

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Kontrollere, om der er fejl i første synkronisering i en Finance and Operations-app

Når du har aktiveret tilknytningsskabelonerne, skal status for tilknytningerne være **Kører**. Hvis status er **Kører ikke**, er der opstået fejl under den første synkronisering. Hvis du vil have vist fejlene, skal du vælge fanen **Oplysninger om første synkronisering** på siden **Dobbeltskrivning**.

![Fanen Oplysninger om første synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Du kan ikke fuldføre den første synkronisering: 400 ugyldig anmodning

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist følgende fejlmeddelelse, når du forsøger at køre tilknytningen og den første synkronisering:

*Fjernserveren returnerede en fejl: (400) ugyldig anmodning. AX-eksport registrerede en fejl*

Her er et eksempel på den fulde fejlmeddelelse.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Hvis denne fejl opstår konsekvent, og du ikke kan fuldføre den første synkronisering, skal du følge disse trin for at løse problemet.

1. Log på den virtuelle maskine (VM) for Finance and Operations-appen.
2. Åbn Microsoft Management Console. 
3. I ruden **Services** skal du sikre dig, at Microsoft Dynamics 365 Dataimport/eksportstruktur-tjenesten kører. Genstart, hvis den er stoppet, fordi den første synkronisering kræver det.

## <a name="initial-synchronization-error-403-forbidden"></a>Fejl under første synkronisering: 403 forbudt

Du kan få vist følgende fejlmeddelelse under første synkronisering:

*(\[Forbudt\], Fjernserveren returnerede en fejl: (403) forbudt.), AX-eksport registrerede en fejl*

Følg disse trin for at løse dette problem.

1. Log på Finance and Operations-appen.
2. Slet **DtAppID**-klienten på siden **Azure Active Directory-programmer**, og tilføj den derefter igen.

![Liste over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a>Selvreferencefejl under første synkronisering

Du kan få vist en fejlmeddelelse, der minder om følgende, hvis nogen af dine tilknytninger har selvreferencer:

*I forbindelse med Kreditor V2 vises følgende fejlmeddelelse: Post-id: ny post, ErrorMessage: Det var ikke muligt at fortolke GUID'et for feltet: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Opslagsværdien blev ikke fundet: CN-001. Prøv følgende URL-adresse(r) for at se, om referencedataene findes: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Denne type fejl opstår ved første synkronisering af tilknytninger, der har selvreferencer. I det foregående eksempel refererer feltet fakturakonto til kreditorenheden.

Hvis du vil løse problemet, skal du muligvis køre tilknytningen to gange, før den første synkronisering lykkes.

