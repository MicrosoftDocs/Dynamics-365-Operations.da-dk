---
title: Udvidelsesmuligheder i Attract
description: "I dette emne beskrives, hvordan du kan udvide programmet Microsoft Dynamics 365 for Talent - Attract ved hjælp af Microsoft Power Platform."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 0af60a0aea0f7a5de793631445aaebb37dbb0d74
ms.contentlocale: da-dk
ms.lasthandoff: 10/22/2018

---

# <a name="extensibility-in-attract"></a>Udvidelsesmuligheder i Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent er bygget oven på Common Data Service (CDS) for Apps-platformen og kan udvides på forskellige måder ved hjælp af Microsoft Power Platform og de funktioner, som Common Data Service for Apps. Derfor kan du konfigurere og tilpasse systemet ved hjælp af Microsoft PowerApps og Microsoft Flow. Du kan også få yderligere analyser om personer ved hjælp af Microsoft Power BI. Desuden gør nye, brugerdefinerede aktiviteter, f.eks. PowerApps og webindholdsaktiviteter (iframe), ansættelsesprocessen mere fleksibel end nogensinde før. Ved hjælp af disse aktiviteter kan du skræddersy ansættelsesprocessen til dine forretningsbehov og -processer og kan sikre dig, at både ansættelsesteam og kandidater får en problemfri tilpasset brugeroplevelse.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Udnytte Microsoft Power Platform 

Da alle dataene fra Attract findes i Common Data Service for Apps, kan du bruge værktøjer fra Microsoft Power Platform til at integrere dine særlige forretningsbehov i Attract.

### <a name="powerapps"></a>PowerApps

Du kan bruge PowerApps til nemt at bygge apps, der er tilknyttet dine Attract-data, og som bruger udtryk som dem, der findes i Microsoft Excel, til at tilføje logik. Apps, som du opretter ved hjælp af PowerApps, kan køre på internettet og på Apple iOS- og Google Android-enheder.

For eksempel kan du gøre det nemmere for rekrutteringsmedarbejdere at bruge universitetskarrieremesser ved at bygge en letvægtsapp, så de kan scanne cv'er og sende kandidater videre til en stilling i Attract. Du kan også oprette en app, der hjælper med at opfylde organisationens overholdelsesbehov. Du kan finde flere oplysninger om PowerApps, og hvordan det bruges til at opbygge programmer, i [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Du kan bruge Microsoft Flow til at oprette automatiserede arbejdsgange, der kører oven på Attract-data. Du kan nemt forbinde hundredvis af populære apps og tjenester uden at skulle skrive kode. Ved at oprette processer, der kommunikerer med Attract-job, kandidat og programenheder i Common Data Service for Apps, kan du automatisere forskellige handlinger. F.eks., når en kandidat accepterer et tilbud, kan der sendes en besked til et onboardingteam, eller nyheder kan offentliggøres på Twitter. Du kan finde flere oplysninger om processer i [dokumentationen til Microsoft Flow](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Med Power BI kan du oprette og få vist brugerdefinerede rapporter og dashboards, der giver dig bedre indsigt i dine data i Attract. Du kan finde flere oplysninger om Power BI, og hvordan du opretter interaktive rapporter og dashboards, i [Power BI-dokumentationen](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Brugerdefinerede aktiviteter 

Du kan tilføje brugerdefinerede aktiviteter, f.eks. PowerApps-apps og webindholdsaktiviteter (iframe), på jobprocesskabelonniveau, eller når du opretter et nyt job. Med disse aktiviteter kan du tilpasse ansættelsesprocessen og overføre forretningslogik, der gælder specifikt for din virksomhed, til Attract.

#### <a name="powerapps-activity"></a>Aktiviteten PowerApps 

Med aktiviteten PowerApps kan forfatteren til en job- eller jobprocesskabelon få mulighed for at integrere en PowerApps-app i ansættelsesprocessen. Når du opretter og udgiver appen, kan du angive dens app-ID i konfigurationerne af aktiviteten. Ved hjælp af en PowerApps-app kan du læse og skrive data i Common Data Service for Apps. Du kan også tilknytte appen til en proces. Du har f.eks. en app, som rekrutteringsmedarbejdere bruger til at udfylde en formular, mens de fører telefonsamtaler. I denne situation kan du knytte appen til en proces, der evaluerer, om en ansøgeren kan rykkes yderligere frem i jobansøgningsprocessen. Denne type aktivitet kan kun ses af medlemmer af ansættelsesteamet. Du kan finde flere oplysninger om, hvordan du konfigurerer PowerApps-aktiviteten, i [Aktiviteter i Attract](./activities-attract.md).

> [!NOTE]
> Aktiviteten PowerApps er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse.

#### <a name="web-content-iframe-activity"></a>Webindholdsaktivitet (iframe)

Med aktiviteten Webindhold (iframe) kan du integrere en brugerdefineret webløsning, som du har oprettet i ansættelsesprocessen eller p kandidatportalen. Du kan læse og skrive data direkte fra Common Data Service for Apps. Du kan også tilpasse løsningen, så den udløser processer eller udnytter Microsoft Azure-funktioner. Du kan finde flere oplysninger om, hvordan du konfigurerer webindholdsaktiviteten, i [Aktiviteter i Attract](./activities-attract.md).

> [!NOTE]
> Aktiviteten Webindhold er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse.

