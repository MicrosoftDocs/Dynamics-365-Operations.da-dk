---
title: Udvidelsesmuligheder i Attract
description: I dette emne beskrives, hvordan du kan udvide Microsoft Dynamics 365 Talent - Attract ved hjælp af Microsoft Power Platform.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ddc6593431585ed79cc15f7ede5daf856f11b959
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527236"
---
# <a name="extensibility-in-attract"></a>Udvidelsesmuligheder i Attract

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Talent er bygget oven på Common Data Service og kan udvides på forskellige måder ved hjælp af Microsoft Power Platform og de funktioner, som Common Data Service tilbyder. Derfor kan du konfigurere og tilpasse systemet ved hjælp af Microsoft Power Apps og Microsoft Power Automate. Du kan også få yderligere analyser om personer ved hjælp af Microsoft Power BI. Desuden gør nye, brugerdefinerede aktiviteter, f.eks. Power Apps og webindholdsaktiviteter (iframe), ansættelsesprocessen mere fleksibel end nogensinde før. Ved hjælp af disse aktiviteter kan du skræddersy ansættelsesprocessen til dine forretningsbehov og -processer og kan sikre dig, at både ansættelsesteam og kandidater får en problemfri tilpasset brugeroplevelse.

## <a name="extending-option-sets-in-attract"></a>Udvide grupperede indstillinger i Attract

En **Grupperet indstilling** (valgliste) er en type felt, der kan indgå i en enhed. Den definerer en gruppering af indstillinger. Når en grupperet indstilling vises i en formular, bruger den et kontrolelement på rullelisten.  I Attract er der flere felter, som er grupperede indstillinger.  Vi er ved at indføre mulighed for at udvide grupperede indstillinger, startende med felterne Årsag til afvisning, Medarbejdertype og Anciennitetstype.   Desuden kan du tilføje oversatte visningsetiketter for de indstillinger, du tilføjer. Du kan finde flere oplysninger under [Tilpasse etiketter for grupperede indstillinger](https://docs.microsoft.com/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Funktionen til jobopslag på LinkedIn kræver brug af **Medarbejdertype** og **Anciennitetstype** på siden **Jobdetaljer**. Standardværdierne i disse felter understøttes af LinkedIn og vises, når jobbet er opslået. Derfor, hvis du laver jobopslag på LinkedIn, og du ændrer de eksisterende værdier for disse felter med grupperede indstillinger, bliver jobbet opslået, men LinkedIn viser ikke de brugerdefinerede værdier i **Medarbejdertype** og **Anciennitetstype**.  

Nedenfor vises trinnene til opdatering af **Årsag til afvisning** med værdier, der er specifikke for din virksomhed.  

1. Hvis du vil udvide den angivne indstilling **Årsag til afvisning**, skal du gå til [Power Apps Administration-webstedet](https://admin.powerapps.com).
2. Du kan blive bedt om at logge på din konto. Angiv det bruger-id og den adgangskode, du bruger til at logge på Dynamics 365 og/eller Office 365, og klik derefter på **Næste**.
3. Under fanen **Miljøer** skal du vælge det miljø, som du vil administrere, og dobbeltklikke for at få adgang til fanen **Oplysninger**.
4. Under fanen **Oplysninger** skal du vælge **Dynamics 365 Administration**.
5. Vælg den forekomst, du vil redigere, og vælg **Åbn**.
6. Gå til **Indstillinger** og derefter **Tilpasninger**, og vælg **Tilpas systemet**.
7. Find den enhed, du vil udvide den grupperede indstilling for, ved at vælge **Enheder** og udvide gruppen. I dette eksempel er det enheden **Jobansøgning**.
8. Gå til det felt, du vil udvide den grupperede indstilling for, ved at vælge indstillingen **Felter**. I dette eksempel er det **msdyn_rejectionreason**. Dobbeltklik på feltet.
9. I feltet **Grupperet indstilling** skal du vælge **Rediger**.
10. Vælg ikonet **+**.
11. Angiv en **Etiket**.  (Det skal være en entydig værdi – ingen dubletter).
12. Vælg **Gem**.
13. Vælg **Udgiv** øverst på siden.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Drage fordel af Microsoft Power Platform 

Da alle dataene fra Attract findes i Common Data Service, kan du bruge værktøjer fra Microsoft Power Platform til at integrere dine særlige virksomhedsbehov i Attract.

### <a name="power-apps"></a>Power Apps

Du kan bruge Power Apps til nemt at bygge apps, der er tilknyttet dine Attract-data, og som bruger udtryk som dem, der findes i Microsoft Excel, til at tilføje logik. Apps, som du opretter ved hjælp af Power Apps, kan køre på internettet og på Apple iOS- og Google Android-enheder.

For eksempel kan du gøre det nemmere for rekrutteringsmedarbejdere at bruge universitetskarrieremesser ved at bygge en letvægtsapp, så de kan scanne cv'er og sende kandidater videre til en stilling i Attract. Du kan også oprette en app, der hjælper med at opfylde organisationens overholdelsesbehov. Du kan finde flere oplysninger om Power Apps, og hvordan det anvendes til at udvikle programmer, under [Integrere data i Common Data Service](https://docs.microsoft.com/powerapps).

### <a name="microsoft-power-automate"></a>Microsoft Power Automate 

Du kan bruge Microsoft Power Automate til at oprette automatiserede arbejdsgange, der kører oven på Attract-data. Du kan nemt forbinde hundredvis af populære apps og tjenester uden at skulle skrive kode. Ved at oprette processer, der kommunikerer med Attract-jobenheden, kandidatenheden og ansøgningsenheden i Common Data Service, kan du automatisere forskellige handlinger. F.eks., når en kandidat accepterer et tilbud, kan der sendes en besked til et onboardingteam, eller nyheder kan offentliggøres på Twitter. Du kan finde flere oplysninger om flows i [Microsoft Power Automate-dokumentationen](https://docs.microsoft.com/flow/).

### <a name="power-bi"></a>Power BI

Med Power BI kan du oprette og få vist brugerdefinerede rapporter og dashboards, der giver dig bedre indsigt i dine data i Attract. Du kan finde flere oplysninger om Power BI, og hvordan du opretter interaktive rapporter og dashboards, i [Power BI-dokumentationen](https://docs.microsoft.com/power-bi/).

### <a name="custom-activities"></a>Brugerdefinerede aktiviteter 

Du kan tilføje brugerdefinerede aktiviteter, f.eks. Power Apps-apps og webindholdsaktiviteter (iframe), på niveauet for jobprocesskabeloner, eller når du opretter et nyt job. Med disse aktiviteter kan du tilpasse ansættelsesprocessen og overføre forretningslogik, der gælder specifikt for din virksomhed, til Attract.

#### <a name="power-apps-activity"></a>Power Apps-aktivitet 

Med Power Apps-aktiviteten kan forfatteren til en job- eller jobprocesskabelon integrere en Power Apps-app i ansættelsesprocessen. Når du opretter og udgiver appen, kan du angive dens app-ID i konfigurationerne af aktiviteten. Ved hjælp af en Power Apps-app kan du læse og skrive data i Common Data Service. Du kan også tilknytte appen til en proces. Du har f.eks. en app, som rekrutteringsmedarbejdere bruger til at udfylde en formular, mens de fører telefonsamtaler. I denne situation kan du knytte appen til en proces, der evaluerer, om en ansøgeren kan rykkes yderligere frem i jobansøgningsprocessen. Denne type aktivitet kan kun ses af medlemmer af ansættelsesteamet. Du kan finde flere oplysninger om, hvordan du konfigurerer Power Apps-aktiviteten, i [Aktiviteter i ansættelsesprocesser](./activities-attract.md).

> [!NOTE]
> Power Apps-aktiviteten er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse.

#### <a name="web-content-iframe-activity"></a>Webindholdsaktivitet (iframe)

Med aktiviteten Webindhold (iframe) kan du integrere en brugerdefineret webløsning, som du har oprettet i ansættelsesprocessen eller p kandidatportalen. Du kan læse og skrive data direkte fra Common Data Service. Du kan også tilpasse løsningen, så den udløser processer eller udnytter Microsoft Azure-funktioner. Du kan finde flere oplysninger om, hvordan du konfigurerer webindholdsaktiviteten, i [Aktiviteter i ansættelsesprocesser](./activities-attract.md).

> [!NOTE]
> Aktiviteten Webindhold er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]