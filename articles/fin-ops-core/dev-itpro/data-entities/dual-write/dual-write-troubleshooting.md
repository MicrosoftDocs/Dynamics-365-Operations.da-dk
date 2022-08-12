---
title: Generel fejlfinding
description: Denne artikel indeholder generelle fejlfindingsoplysninger for dobbeltskrivning mellem programmer til finans og drift og Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f263e331d23ce0ddf60a4abc2467513aa342445
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112358"
---
# <a name="general-troubleshooting"></a>Generel fejlfinding

[!include [banner](../../includes/banner.md)]



Denne artikel indeholder generelle fejlfindingsoplysninger for dobbeltskrivning mellem programmer til finans og drift og Dataverse.

> [!IMPORTANT]
> Nogle af de problemer, som denne artikel vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivere og åbne plug-in-sporingslogge i Dataverse for at få vist oplysninger om fejl

Sporingslogge kan være nyttige, når du foretager fejlfinding af problemer med dynamiske synkroniseringer af dobbeltskrivning mellem Finance & Operations og Dataverse. Logfilerne kan give specifikke oplysninger til de teams, der leverer teknisk support til Dynamics 365. I denne artikel beskrives det, hvordan sporingslogfiler aktiveres, og hvordan de kan vises. Sporingslogfiler administreres på siden Dynamics 365-indstillinger og kræver rettigheder på administratorniveau for at kunne ændre og se dem. 

**Følgende rolle er påkrævet for at kunne aktivere sporingsloggen og få vist fejl:** systemadministrator

### <a name="turn-on-the-trace-log"></a>Aktivere sporingsloggen
Udfør følgende trin for at aktivere sporingsloggen.

1.  Log på Dynamics 365, og vælg **Indstillinger** på den øverste navigationslinje. Klik på **Administration** på siden Systemer.
2.  På siden Administration skal du klikke på **Systemindstillinger**.
3.  Vælg fanen **Tilpasning** og plug-in, og i sektionen for sporing af brugerdefineret arbejdsflow skal du ændre rullelisten til **Alle**. Dette sporer alle aktiviteter og leverer et omfattende sæt data til de teams, der skal gennemgå potentielle problemer.

> [!NOTE]
> Når du indstiller rullelisten til **Undtagelse**, leveres der kun sporingsoplysninger, når der opstår undtagelser (fejl).

Når sporingslogfilerne i plug-in er aktiveret, fortsætter de med at blive indsamlet, indtil de er slået fra manuelt, ved at vende tilbage til dette sted og vælge **Fra**.

### <a name="view-the-trace-log"></a>Se sporingsloggen
Udfør følgende trin for at få vist sporingsloggen.

1. Vælg **Indstillinger** på den øverste navigationslinje på siden Dynamics 365-indstillinger. 
2. Vælg **Plug-in-sporingslogfil** i sektionen **Tilpasninger** på siden.
3. Du kan finde poster på listen over sporingslogfiler baseret på typenavn og/eller meddelelsesnavn.
4. Åbn den ønskede post for at få vist hele loggen. Meddelelsesblokken i sektionen Udførelse har tilgængelige oplysninger til denne plug-in. Hvis det er tilgængeligt, vil der også være undtagelsesoplysninger. 

Du kan kopiere indholdet af sporingslogfilerne og indsætte dem i et andet program, f.eks. Notesblok eller andre værktøjer, for at få vist logfiler eller tekstfiler, så det er nemmere at se alt indholdet. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktivere fejlfindingstilstand for at foretage fejlfinding af problemer med direkte synkronisering i programmer til finans og drift

**Påkrævet rolle for at få vist fejl** : Systemadministrator

Dobbeltskrivningsfejl, der stammer fra Dataverse, kan forekomme i programmer til finans og drift. Hvis du vil aktivere detaljeret logføring for fejlene, skal du følge disse trin.

1. For alle projektkonfigurationer i programmer til finans og drift er flaget **IsDebugMode** angivet i tabellen **DualWriteProjectConfiguration**.
2. Åbn **DualWriteProjectConfiguration** ved hjælp af tilføjelsesprogrammet til Excel. Hvis du vil bruge tilføjelsesprogrammet, skal du aktivere designtilstand i Excel-tilføjelsesprogrammet finans og drift og føje **DualWriteProjectConfiguration** til arket. Du kan finde flere oplysninger i [Få vist og opdatere enhedsdata med Excel](../../office-integration/use-excel-add-in.md).
3. Angiv **IsDebugMode** til **Ja** på projektet.
4. Kør det scenario, der genererer fejl.
5. De detaljerede logfiler lagres i tabellen **DualWriteErrorLog**.
6. Hvis du vil slå data op i en tabels browser, skal du bruge følgende link: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, hvor du erstatter `999` efter behov.
7. Opdater igen efter [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), som er tilgængelig for platformopdateringer 37 og senere. Hvis du har denne rettelse installeret, vil fejlfindingstilstanden registrere flere logfiler.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Kontrollere synkroniseringsfejl på den virtuelle maskine for programmer til finans og drift

**Påkrævet rolle for at få vist fejl:** Systemadministrator

1. Log på Microsoft Dynamics LifeCycle Services (LCS).
2. Åbn det LCS-projekt, du har valgt til at udføre dobbeltskrivningstesten for.
3. Vælg titlen **Skybaserede miljøer**.
4. Brug Fjernskrivebord til at logge på den virtuelle maskine (VM) for programmer til finans og drift. Brug den lokale konto, der vises i LCS.
5. Åbn Logbog.
6. Vælg **Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationel**.
7. Gennemse listen over seneste fejl.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Landingsside for brugergrænseflade til dobbeltskrivning er blank
Når du åbner siden til dobbeltskrivning i Microsoft Edge eller Google Chrome-browseren, indlæses startsiden ikke, og du får vist en tom side eller en fejl som f.eks. "Noget gik galt".
I Devtools vises en fejl i konsollogfilerne:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Kunne ikke læse egenskaben 'sessionStorage' fra 'Vindue': Adgang er afvist for dette dokument. ved t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) ved ny t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) ved Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) ved jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) ved Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) ved Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) ved Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) ved vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) ved hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

Brugergrænsefladen bruger browserens 'sessionslager' til at gemme nogle egenskabsværdier til indlæsning af startsiden. For at dette kan fungere skal der være tilladt tredjeparts cookies i webstedets browser. Fejlen opstår, når brugergrænsefladen ikke kan få adgang til sessionslageret. Der kan være to scenarier, hvor dette problem kan opstå:

1.  Du åbner brugergrænsefladen i inkognito-tilstand i Edge/Chrome og tredjeparts-cookies er blokeret i inkognito-tilstand.
2.  Du har blokeret tredjeparts-cookies helt i Edge/Chrome.

### <a name="mitigation"></a>Afhjælpning
Tredjeparts cookies skal være tilladt i browserindstillingerne.

### <a name="google-chrome-browser"></a>Google Chrome-browser
1. mulighed:
1.  Gå til indstillinger ved at indtaste chrome://settings/ på adresselinjen, og gå derefter til Sikkerhed og privatliv -> Cookies og andre websitedata.
2.  Vælg 'Tillad alle cookies'. Hvis du ikke ønsker at gøre dette, skal du vælge den anden mulighed.

2. mulighed:
1.  Gå til indstillinger ved at indtaste chrome://settings/ på adresselinjen, og gå derefter til Sikkerhed og privatliv -> Cookies og andre websitedata.
2.  Hvis der er valgt 'Bloker tredjeparts cookies i inkognito' eller 'Bloker tredjeparts cookies' er valgt, skal du gå til 'Websteder, der altid kan bruge cookies' og klikke på **Tilføj**. 
3.  Tilføj navnet på dit websted for Finance & Operations-apps - https://<din_FinOp_forekomst>.cloudax.dynamics.com. Sørg for at markere afkrydsningsfeltet "Alle cookies, kun på dette websted". 

### <a name="microsoft-edge-browser"></a>Microsoft Edge-browser
1.  Gå til Indstillinger - > Tilladelser for webstedet - > Cookies og webstedsdata.
2.  Deaktiver 'Bloker cookies fra tredjepart'.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Frakoble og tilknytte et andet Dataverse-miljø fra programmer til finans og drift

**Påkrævet rolle for at fjerne miljøtilknytningen**: Systemadministrator for enten programmer til finans og drift eller Dataverse.

1. Log på programmer til finans og drift.
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

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>Sådan sikrer du, at dataintegration bruger det nyeste finans og driftsskema

Du kan komme ud for dataproblemer i dataintegrationen, hvis det mest opdaterede skema ikke bruges. Følgende trin hjælper dig med at opdatere enhedslisten i programmer til finans og drift og enhederne i dataintegratoren.

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>Opdater enhedslisten i finans og drift-miljø
1.  Log på dit finans og driftsmiljø.
2.  Vælg **Datastyring**.
3.  I Datastyring skal du vælge **Rammeparametre**.
4.  Vælg **Enhedsindstillinger** på siden Parametre for **dataimport/eksportstruktur**, og vælg derefter **Listen Opdater enhed**. Det kan tage mere end 30 minutter at opdatere, afhængigt af antallet af involverede enheder.
5.  Naviger til **datastyring**, og vælg **dataenheder** for at validere, at de forventede enheder vises. Hvis de forventede enheder ikke findes på listen, skal du kontrollere, at enhederne vises i finans og drift-miljøet, og gendanne de manglende enheder efter behov.

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>Hvis problemet ikke kan løses af opdateringen, kan du slette enhederne og tilføje dem igen

> [!NOTE]
> Det kan være nødvendigt at standse alle behandlingsgrupper, der benytter enhederne, før de slettes.

1.  Vælg **Datastyring** i finans- og drift-miljøet, og vælg **dataenheder**.
2.  Søg efter enheder med problemer og tag notat af destinationsenheden, den midlertidige tabel, enhedsnavnet og andre indstillinger. Slet enheden eller enhederne fra listen.
3.  Vælg **Ny**, og tilføj enheden eller enhederne igen ved hjælp af dataene fra trin 2. 

#### <a name="refresh-entities-in-data-integrator"></a>Opdatere enheder i Dataintegrator
Log på Power Platform Administration, og vælg **dataintegration**. Åbn det projekt, hvor der opstår problemer, og vælg **Opdater enheder**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Sådan aktiveres og gemmes netværksspor, så der kan tilknyttes sporing til supportbilletter

Supportteamet skal muligvis gennemse netværksspor for at udføre fejlfinding af visse problemer. Hvis du vil oprette et netværksspor, skal du følge disse trin:

### <a name="google-chrome-browser"></a>Google Chrome-browser

1. Tryk på **F12** under den åbne fane, eller vælg **Udviklingsværktøjer** for at åbne udviklingsværktøjerne.
2. Åbn fanen **Netværk**, og skriv **integ** i filtertekstfeltet.
3. Kør scenariet, og vær opmærksom på de anmodninger, der logføres.
4. Højreklik på indtastningerne, og vælg **Gem alle som en HAR med indhold**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge-browser

1. Tryk på **F12** under den åbne fane, eller vælg **Udviklingsværktøjer** for at åbne udviklingsværktøjerne.
2. Åbn fanen **Netværk**.
3. Kør scenariet.
4. Vælg **Gem** for at eksportere resultaterne som HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

