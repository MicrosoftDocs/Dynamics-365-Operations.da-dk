---
title: Integrere tredjepartsapps
description: Denne artikel beskriver, hvordan du kan integrere tredjepartsapps for at forbedre produktets funktioner.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef5ed6c3c99d62010643940f3e2f158963ff0dc2
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123712"
---
# <a name="embed-third-party-apps"></a>Integrere tredjepartsapps

[!include [banner](../includes/banner.md)]

Mange kunder bruger en række programmer til at køre deres virksomhed. Nogle af disse applikationer er webapps fra en tredjepart, som fungerer sammen med programmer til finans og drift. For at give en mere problemfri brugeroplevelse kan du bruge funktionen **Fuld side-apps** til at integrere disse tredjepartsapps direkte i dine programmer til finans og drift (forudsat at disse tredjepartsapps tillader, at de bliver integreret). På denne måde kan brugere få adgang til de websteder og apps, de kræver, uden at skulle skifte faner eller vinduer.

Før du kan integrere tredjepartsapps i produktet, skal du aktivere funktionen **Fuld side-apps** i Funktionsstyring. Du kan derefter bruge en af følgende metoder til at integrere en tredjepartsapp eller et websted. Disse metoder svarer til de metoder, der bruges til at integrere lærredapps fra Microsoft Power Apps i programmer til finans og drift.

- Integrer appen eller webstedet på en eksisterende side som en ny fane (pivot-fane, oversigtspanel, blad eller arbejdsområdesektionen).
- Opret en ny fuld side-oplevelse for appen eller webstedet fra dashboardet.

## <a name="embed-a-website-on-an-existing-page"></a>Integrere et websted på en eksisterende side

Brug denne procedure, hvis du vil supplere en eksisterende side i systemet med en integreret app.

1. Åbn den side, hvor du vil integrere lærredappen.
2. Åbn ruden **Tilføj en app**:

    1. Vælg **Indstillinger** og derefter **Tilpas** for at åbne værktøjslinjen **Tilpasning**.
    2. Vælg **Flere \> Tilføj en app**.

3. Vælg det område på siden, hvor du vil tilføje appen. Dette område skal være en *fanebeholder* for en pivot-fane, et oversigtspanel, et blad eller en arbejdsområdesektion.
4. Vælg **Websted**.
5. Konfigurere den integrerede app:

    - **Navn** – Angiv den tekst, der skal vises under fanen, som indeholder den integrerede app. Ofte vil du have, at denne tekst skal være navnet på appen.
    - **URL** – Angiv appens placering.

    > [!IMPORTANT]
    > - Af sikkerhedsmæssige grunde skal URL-adressen bruge HTTPS (Hypertext Transfer Protocol Secure).
    > - Appen eller webstedet skal være konfigureret til at kunne blive integreret.

6. Vælg **Gem** for at integrere appen på siden. Appen tilføjes som den sidste fane eller sektion i gruppen.
7. Bekræft, at appen vises som forventet. Hvis appen ikke er gengivet, skal du se afsnittet [Fejlfinding](#troubleshooting) senere i denne artikel.
8. Åbn visningsvælgeren, og vælg enten **Gem** (hvis appen skal knyttes til den aktuelle visning) eller **Gem som** (for at gemme appen for en anden visning).

    Hvis siden ikke har en visningsvælger (f.eks. hvis siden er en dialogboks eller et arbejdsområde), kan du springe dette trin over.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Integrere et websted som en fuld side-oplevelse fra dashboardet

Brug denne procedure, hvis den app, du vil integrere, ikke er tilknyttet en eksisterende side, eller hvis du blot vil have en fuld side-oplevelse for appen i programmet til finans og drift.

1. Åbn dashboardet.
2. Vælg og hold (eller højreklik på) dashboardet, vælg **Tilpas**, og vælg derefter **Tilføj en side**.
3. I ruden **Tilføj en side** skal du vælge **Websted**.
4. Konfigurere den integrerede app:

    - **Navn** – Angiv den tekst, der skal vises på det felt, som tilføjes for den integrerede app på dashboardet. Ofte vil du have, at denne tekst skal være navnet på appen.
    - **URL** – Angiv appens placering.

    > [!IMPORTANT]
    > - Af sikkerhedsmæssige grunde skal URL-adressen bruge HTTPS.
    > - Appen eller webstedet skal være konfigureret til at kunne blive integreret.

5. Vælg **Gem** for at føje appen til dashboardet som et nyt felt.
6. Vælg det nye felt på dashboardet, og bekræft, at appen vises som forventet. Hvis appen ikke bliver gengivet, skal du se afsnittet [Fejlfinding](#troubleshooting) senere i denne artikel.

## <a name="sharing-embedded-apps"></a>Deling af integrerede apps

Når du har integreret en app ved hjælp af en af de metoder, der er beskrevet i de forrige afsnit, kan du dele visningen med andre brugere i systemet. Hvis du vil dele en integreret app, skal du benytte en af følgende metoder:

- **Publicer visningen (Anbefalet):** Hvis den integrerede app er gemt i en visning, er den anbefalede og foretrukne metode at dele den ved at publicere visningen til brugere med de relevante sikkerhedsroller i de tilsigtede juridiske enheder. I så fald er det kun de ønskede brugere, der kan se den integrerede app på den pågældende side. Du kan finde flere oplysninger om, hvordan du publicerer en visning i [Publicering af visninger](saved-views.md#publishing-views).

    Du kan også publicere en app, der er integreret som en fuld side-oplevelse fra dashboardet. Vælg og hold (eller højreklik på) det felt på dashboardet, som er knyttet til appen, vælg **Tilpas**, og vælg derefter **Publicer side**. Visningen svarer til *Publicering af visninger*, og du kan vælge de sikkerhedsroller, der skal udgives til. I opdatering 10.0.21 eller senere, hvis funktionen **Forbedret understøttelse af juridiske enheder for gemte visninger** er slået til, kan du også publicere appen til de ønskede juridiske enheder.

- **Kopier tilpasningen:** For sider, der ikke understøtter visninger (f.eks. dialogbokse eller arbejdsområder) eller for fuld side-appoplevelsen, kan du kopiere tilpasningen til de relevante brugere. Yderligere oplysninger finder du i [Deling af tilpasninger](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Visning af integrerede apps

For at få vist en integreret app på en side i programmer til finans og drift skal du åbne den side, der har den integrerede app. Husk, at på nogle sider kan du åbne integrerede apps ved hjælp af **Power Apps**-knappen i standardhandlingsruden. Muligvis kan de også blive vist direkte på siden som en ny fane, et oversigtspanel, et blad eller som en ny sektion i et arbejdsområde.

## <a name="editing-or-removing-embedded-apps"></a>Redigering eller fjernelse af integrerede apps

Når en app er blevet integreret på en side, skal du muligvis redigere konfigurationen af den (f.eks. ved at ændre sektionsetiketten eller URL-adressen). Du kan også være nødt til at fjerne den fra siden. Brug en af følgende procedurer til at redigere konfigurationen af en integreret app eller fjerne den helt.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Apps, der er integreret på eksisterende sider

1. Åbn den side, hvor appen er integreret.
2. Vælg **Indstillinger** og derefter **Tilpas** for at åbne værktøjslinjen **Tilpasning**.
3. Vælg værktøjet **Vælg**, og vælg derefter den integrerede app.
4. Hvis du vil redigere appen, skal du foretage de nødvendige ændringer af konfigurationen og derefter vælge **Gem**.

    Du kan også vælge **Slet** for at fjerne appen.

5. Gem visningen eller publicer den igen. Bemærk, at hvis du forlader siden uden eksplicit at gemme visningen, bevares ingen af de handlinger, du har udført i ruden **Rediger websted**.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Apps, der er integreret fra dashboardet

1. Åbn dashboardet.
2. Vælg og hold (eller højreklik på) det felt, der er knyttet til den integrerede app, og vælg derefter **Tilpas**.
3. Hvis du vil redigere appen, skal du vælge **Rediger side**. I ruden **Rediger websted** kan du foretage de nødvendige ændringer af appens konfiguration og derefter vælge **Gem**.

    Du kan også vælge **Fjern side** for at fjerne appen.

## <a name="appendix"></a>Appendiks

### <a name="troubleshooting"></a>Fejlfinding

Hvis et websted ikke er gengivet korrekt, efter det er blevet integreret i en Finans og drift-app, eller hvis du modtager en fejlmeddelelse, der angiver, at URL-adressen blev afvist at få en forbindelse, er webstedet sandsynligvis konfigureret til at forhindre, at det bliver integreret i en iframe. Benyt denne fremgangsmåde for at finde ud af, om webstedet kan integreres.

1. Åbn udviklerværktøjerne for den browser, du bruger.
2. Find og vælg svaret fra den integrerede websted under fanen **Netværk**.
3. Søg efter **x-frame-indstillinger** under **Svarhoveder** under fanen **Sidehoveder**. Hvis der findes **x-frame-indstillinger** i svarhovederne, og de har værdien **DENY** eller **SAMEORIGIN**, kan webstedet ikke integreres i øjeblikket. Du skal arbejde sammen med ejeren af appen, hvis den skal kunne integreres sikkert.

### <a name="developer-modeling-a-website-on-a-form"></a>[Udvikler] Modellering af et websted i en formular

Selvom denne artikel fokuserer på integrationen af tredjepartsapps eller websteder via tilpasning, kan udviklere også integrere dem i en formular ved hjælp af Visual Studio-udviklingsløsningen. Tilføj et kontrolelement af typen **WebstedHostControl** til formularen. De metadataegenskaber, der er tilgængelige for kontrolelementet, indeholder de samme egenskaber som tilpasningsfunktionen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

