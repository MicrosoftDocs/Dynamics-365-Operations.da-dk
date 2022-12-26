---
title: Forhåndsversion af Dynamics 365 Commerce 10.0.30 (November 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Commerce 10.0.30.
author: josaw1
ms.date: 12/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: a449c7eff21c059555f9659ea932705858d26275
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831741"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Forhåndsversion af Dynamics 365 Commerce 10.0.30 (November 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Commerce forhåndsversion 10.0.30. Denne version har et build-nummer på 10.0.1362 og er tilgængelig i følgende plan:

- **Udgivelse af forhåndsversion:** September 2022
- **Generel tilgængelighed af version (selv-opdatering):** oktober 2022
- **Generel tilgængelighed af version (auto-opdatering):** november 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---------|------------------|----------------|--------------| 
| Kundesupport   | Chat på et e-handelswebsted ved hjælp af en Power Virtual Agents-robot. | Denne funktion vil give brugere af e-handelswebstedet mulighed for at bruge en Power Virtual Agents-chatrobot til supportanmodninger. | Aktiveres af administratorer/beslutningstagere for slutbrugere |
| Indsigt  |  Stream POS-driftsindsigtshændelser til din Application Insights-konto. | [Få adgang til logfiler i Application Insights](../dev-itpro/operational-insights.md#enable-diagnostic-events-in-application-insights)   |  Tilmelding af it-medarbejder/udvikler   |
|  Betalinger  | Understøttelse af PayPal-ordrer efter 29 dages godkendelsesperiode. | Den maksimale godkendelsesperiode for PayPal er 29 dage, hvorefter der skal genereres et nyt godkendelses- og ordre-id. Som alternativ tilbyder PayPal en mulighed, hvor en ordre kan referere til en PayPal-ordre som en generel ordre, der tillader flere godkendelser og registrerer mod samme ordre-id i stedet for at generere et nyt godkendelses- og ordre-id efter 29 dage). | Når PayPal payment connector konfigureres i Commerce headquarters, er feltet **OrderIntent** tilføjet, og det kan have to værdier:<p><p>- **Authorize** – Denne konfiguration er standarden (hvis feltet ikke udfyldes, fungerer **Authorize** som standard). Konfigurering af **OrderIntent** til **Authorize** korrelerer til PayPal **processing_instruction** værdien **NO_INSTRUCTION**. Ordren godkendes med PayPal, og godkendelsen kan ikke ændres, når denne værdi bruges.<p>- **Save** – Når værdien **OrderIntent** er angivet til **Save**, korreleres til PayPal **processing_instruction** værdien **ORDER_SAVED_EXPLICITLY**. Ordrereferencer gemmes i PayPal-tjenesten, når denne værdi bruges.  |
| POS-logon  | [Aktivere funktioner for diagnose under selvbetjening af POS-logon](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Denne funktion indeholder diagnosefunktioner, der kan bruges til selvbetjening i POS (POS) og Commerce headquarters, for at hjælpe butiksmedarbejdere og ledere med hurtigt at identificere og rette rodårsagerne til POS-logonproblemer.<p><p>- De fejlmeddelelser, der vises på skærmen til POS-logon, er forbedret, så de giver konkrete rodårsagsoplysninger, der kan hjælpe butiksmedarbejdere, der bruger POS, med at forstå, hvad der gik galt, så de kan udføre de nødvendige handlinger for at løse problemet.<p>- Der findes en funktion til **Testlogon** på siden **Arbejdere** i Commerce headquarters, så butikschefer, der konfigurerer POS-enheder, kan simulere POS-logon. Hvis der opstår fejl ved logon, giver denne funktion handlingsvejledninger til fejlfinding, så ledere kan kontrollere relevante konfigurationer, løse problemer og validere rettelserne.  | Til som standard |


## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Dynamics 365 Finance 10.0.30 indeholder platformsopdateringer. Du kan få mere vide i [Platformsopdateringer til version 10.0.30 af programmer til finans og drift](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af version 10.0.30, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 2

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 2](/dynamics365-release-plan/2022wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-features"></a>Fjernede og udfasede funktioner

Artiklen om [fjernede eller udfasede funktioner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beskriver funktioner, der er blevet fjernet eller udfaset for Commerce.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
