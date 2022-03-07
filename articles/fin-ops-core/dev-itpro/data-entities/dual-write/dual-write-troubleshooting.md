---
title: Generel fejlfinding
description: Dette emne indeholder generelle fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: bcedb9f6e8fb15210512ed6a376d4329759593e4
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781168"
---
# <a name="general-troubleshooting"></a>Generel fejlfinding

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emne indeholder generelle fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivere og åbne plug-in-sporingslogge i Dataverse for at få vist oplysninger om fejl

**Følgende rolle er påkrævet for at kunne aktivere sporingsloggen og få vist fejl:** systemadministrator

Udfør følgende trin for at aktivere sporingsloggen.

1. Log på Customer Engagement-appen, åbn siden **Indstillinger**, og vælg derefter **Administration** under **System**.
2. På siden **Administration** skal du vælge **Systemindstillinger**.
3. Under fanen **Tilpasning** i kolonnen **Plug-in og brugerdefineret sporing af arbejdsgangsaktivitet** skal du vælge **Alle** for at aktivere sporingslogfilen for plug-in'en. Hvis du kun vil logføre sporingslogge, når der opstår undtagelser, kan du vælge **Undtagelse** i stedet.


Udfør følgende trin for at få vist sporingsloggen.

1. Log på Customer Engagement-appen, åbn siden **Indstillinger**, og vælg derefter **Plug-in-sporingslogfil** under **Tilpasning**.
2. Find sporingslogfilerne, hvor kolonnen **Typenavn** er indstillet til **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Dobbeltklik på et element for at få vist hele loggen, og gennemse derefter **Message Block**-teksten i oversigtspanelet **Udførelse**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktivere fejlfindingstilstand for at foretage fejlfinding af problemer med direkte synkronisering i Finance and Operations-apps

**Påkrævet rolle for at få vist fejl** : Systemadministrator

Dobbeltskrivningsfejl, der stammer fra Dataverse, kan forekomme i Finance and Operations-appen. Hvis du vil aktivere detaljeret logføring for fejlene, skal du følge disse trin.

1. For alle projektkonfigurationer i Finance and Operations-appen er flaget **IsDebugMode** angivet i tabellen **DualWriteProjectConfiguration**.
2. Åbn **DualWriteProjectConfiguration** ved hjælp af tilføjelsesprogrammet til Excel. Hvis du vil bruge tilføjelsesprogrammet, skal du aktivere designtilstand i Finance and Operations Excel-tilføjelsesprogrammet og føje **DualWriteProjectConfiguration** til arket. Du kan finde flere oplysninger i [Få vist og opdatere enhedsdata med Excel](../../office-integration/use-excel-add-in.md).
3. Angiv **IsDebugMode** til **Ja** på projektet.
4. Kør det scenario, der genererer fejl.
5. De detaljerede logfiler lagres i tabellen **DualWriteErrorLog**.
6. Hvis du vil slå data op i en tabels browser, skal du bruge følgende link: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, hvor du erstatter `999` efter behov.
7. Opdater igen efter [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), som er tilgængelig for platformopdateringer 37 og senere. Hvis du har denne rettelse installeret, vil fejlfindingstilstanden registrere flere logfiler.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Kontrollere synkroniseringsfejl på den virtuelle maskine for Finance and Operations-appen

**Påkrævet rolle for at få vist fejl:** Systemadministrator

1. Log på Microsoft Dynamics LifeCycle Services (LCS).
2. Åbn det LCS-projekt, du har valgt til at udføre dobbeltskrivningstesten for.
3. Vælg titlen **Skybaserede miljøer**.
4. Brug Fjernskrivebord til at logge på den virtuelle maskine (VM) for Finance and Operations-appen. Brug den lokale konto, der vises i LCS.
5. Åbn Logbog.
6. Vælg **Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationel**.
7. Gennemse listen over seneste fejl.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Fjerne sammenkædning og sammenkæde med et andet Dataverse-miljø fra en Finance and Operations-app

**Påkrævet rolle for at fjerne miljøtilknytningen:** Systemadministrator for enten Finance and Operations-app eller Dataverse.

1. Log på Finance and Operations-appen.
2. Gå til **Arbejdsområder \> Datastyring**, og vælg feltet **Dobbeltskrivning**.
3. Vælg alle kørende tilknytninger, og vælg derefter **Stop**.
4. Vælg **Ophæv sammenkædning af miljø**.
5. Vælg **Ja** for at bekræfte operationen.

Nu kan du sammenkæde et nyt miljø.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Kan ikke se linjeoplysningsformularen for salgsordren 

Når du opretter en salgsordre i Dynamics 365 Sales, kan klik på **+ Tilføj produkter** omdirigere dig til ordrelinjeformen i Dynamics 365 Project Operations. Du kan ikke få vist formularen for salgsordrelinjens **Oplysninger** på denne måde. Indstillingen for **Oplysninger** vises ikke på rullelisten under **Ny ordrelinje**. Dette sker, fordi Project Operations er installeret i dit miljø.

Hvis du vil aktivere formularindstillingen **Oplysninger** igen, skal du følge disse trin:

1. Naviger til tabellen **Ordrelinje**.
2. Find formularen **Oplysninger** under formularernoden.
3. Vælg formularen **Oplysninger**, og klik på **Aktivér sikkerhedsroller**.
4. Ret sikkerhedsindstillingen til **Vis for alle**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Sådan aktiveres og gemmes netværksspor, så der kan tilknyttes sporing til supportbilletter

Supportteamet skal muligvis gennemse netværksspor for at udføre fejlfinding af visse problemer. Hvis du vil oprette et netværksspor, skal du følge disse trin:

### <a name="chrome"></a>Chrome

1. Tryk på **F12** under den åbne fane, eller vælg **Udviklingsværktøjer** for at åbne udviklingsværktøjerne.
2. Åbn fanen **Netværk**, og skriv **integ** i filtertekstfeltet.
3. Kør scenariet, og vær opmærksom på de anmodninger, der logføres.
4. Højreklik på indtastningerne, og vælg **Gem alle som en HAR med indhold**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Tryk på **F12** under den åbne fane, eller vælg **Udviklingsværktøjer** for at åbne udviklingsværktøjerne.
2. Åbn fanen **Netværk**.
3. Kør scenariet.
4. Vælg **Gem** for at eksportere resultaterne som HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
