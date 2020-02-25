---
title: Integrer Power Apps
description: Dette emne beskriver, hvordan du kan integrere Power Apps i klienten for at øge produktets funktioner.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 9585d5a399ebf45b0ad7640f3c4e48d8afc46cd8
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017722"
---
# <a name="embed-microsoft-power-apps"></a>Integrer Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Finance and Operations understøtter integration med Microsoft Power Apps, en tjeneste til udviklere og ikke-tekniske brugere til opbygning af brugerdefinerede forretningsapps til mobilenheder, tablets og internettet uden at skrive kode. Power Apps, der er udviklet af dig, din organisation eller det bredere økosystem, kan derefter integreres i Finance and Operations-apps for at øge produktets funktionalitet. Du kan f.eks. opbygge en app fra Power Apps, der supplerer en Finance and Operations-app med oplysninger, der er hentet fra et andet system.

Hvis du vil vide mere om Power Apps, kan du se den korte video [Sådan integreres Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Tilføjelse af en integreret app fra Power Apps til en side

### <a name="overview"></a>Oversigt

Før du integrerer en app fra Power Apps i klienten, skal du først finde eller oprette en app med den ønskede grafik og/eller funktionalitet. Vi beskriver ikke i detaljer processen til oprettelse af apps her. Emnet [Introduktion til Power Apps](https://docs.microsoft.com/powerapps/getting-started) er et godt udgangspunkt, hvis du ikke kender Power Apps.

Når du er klar til at integrere en bestemt app, kan du vælge mellem en af to måder til at få adgang til appen på en side, afhængig af hvilken måde der passer bedst til dit scenarie. Den første måde er via knappen Power Apps, der er føjet til standardhandlingsruden. Apps, der er tilføjet ved hjælp af denne mekanisme, vises som menupunkter i menuknappen Power Apps. Når den vælges, åbner hver af disse menupunkter en siderude, der indeholder den integrerede app. Du kan også vælge at integrere en app direkte på en side, som en ny fane, et oversigtspanel, blad eller som et nyt afsnit i et arbejdsområde.

Når du konfigurerer din integrerede app, kan du vælge et enkelt felt, du vil sende som kontekst til appen. Dette giver mulighed for, at appen kan reagere på basis af de data, du aktuelt får vist.

### <a name="details"></a>Oplysninger

Følgende instruktioner viser, hvordan du integrerer en app fra Power Apps i webklienten.

1. Gå til siden, hvor du vil integrere appen. Dette er den samme side, der indeholder de data, der skal sendes til appen som input.
2. Åbn ruden **Tilføj en app fra Power Apps**:

    - Klik på **Indstillinger**, og vælg derefter **Tilpas denne side**. Under menuen **Indsæt** skal du vælge **Power Apps**. Endelig skal du vælge det område, hvor du vil tilføje appen. Hvis du vil integrere appen under menuknappen Power Apps, skal du vælge handlingsruden. Hvis du vil integrere appen direkte på siden, skal du vælge den eller det relevante fane, oversigtspanel, blad eller afsnit (hvis du er på et arbejdsområde).
    - Hvis appen skal åbnes ved hjælp af menuknappen Power Apps, kan du også klikke på menuknappen **Power Apps** i standardhandlingsruden og derefter vælge **Tilføj en app**.

3. Konfigurere den integrerede app:

    - Feltet **Navn** angiver den tekst, der vises for knappen eller fanen, der indeholder den integrerede app. Ofte ønsker du blot at gentage navnet på appen i dette felt.
    - **App-ID** er GUID'et for den app, du vil integrere. For at hente denne værdi skal du finde appen på [web.powerapps.com](https://web.powerapps.com) og derefter finde feltet **App-id** feltet under **Detaljer**.
    - Som **Inputkontekst for appen** kan du eventuelt vælge det felt, der indeholder de data, du vil overføre til appen som input. Se afsnittet senere i dette emne med titlen [Opbygning af apps, der udnytter data fra Finance and Operations-apps](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) for at få oplysninger om, hvordan appen kan få adgang til data, der er sendt fra Finance and Operations-apps.
    - Vælg den **Programstørrelse**, der svarer til den type app, du vil integrere. Vælg **Tynd** til apps, der er bygget til mobilenheder, og **Bred** til apps, der er bygget til tablets. Dette sikrer, at der allokeres en tilstrækkelig mængde plads til den integrerede app.
    - Oversigtspanelet **Juridiske enheder** giver mulighed for at vælge, hvilke juridiske enheder appen er tilgængelig for. Standarden er at gøre appen tilgængelig for alle juridiske enheder. Denne indstilling er kun tilgængelig, når funktionen [Gemte visninger](saved-views.md) er deaktiveret. 

4. Når du har bekræftet, at konfigurationen er korrekt, skal du klikke på **Indsæt** for at integrere Power App på siden. Du bliver bedt om at opdatere browseren for at få vist den integrerede app.

## <a name="sharing-an-embedded-app"></a>Deling af en integreret app

Når du har integreret en app på en side og bekræftet, at den fungerer korrekt med alle typer datakontekst, der blev overført fra siden, ønsker du muligvis at dele denne integrerede dette med andre brugere i systemet. Dette kan gøres på to forskellige måder ved hjælp af funktionerne til brugertilpasning af produktet:

- Det anbefalede scenarie er via systemadministratoren, der kan overføre en tilpasning til alle brugere eller en undergruppe af brugere.
- Du kan også eksportere dine sidetilpasninger og sende dem til en eller flere brugere og få hver af disse brugere til at importere disse ændringer. Tilpasningsværktøjslinjen har handlinger, der giver dig mulighed for at eksportere og importere tilpasninger.

Se [Tilpasse brugeroplevelsen](personalize-user-experience.md) for at få yderligere oplysninger om tilpasningsmuligheder i produktet, og hvordan de bruges.

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Opbygge en app, der anvender data, som er sendt fra Finance and Operations-apps

En vigtig del af oprettelsen af en app fra Power Apps, der vil blive integreret i en Finance and Operations-app, anvender inputdataene fra det pågældende program. Fra Power Apps-udviklingsoplevelsen kan der opnås adgang til inputdata, der er overført fra en Finance and Operations-app, ved hjælp af variablen Param ("EntityId").

For eksempel kan du i funktionen OnStart i appen indstille de indgående data fra Finance and Operations-apps til en variabel som denne:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Visning af en app

For at få vist en integreret app på en side i Finance and Operations-apps skal du gå til en side med en integreret app. Husk, at apps kan åbnes via knappen Power Apps i standardhandlingsruden, eller at den kan vises direkte på siden som en ny fane, et oversigtspanel, et blad eller som en ny sektion i et arbejdsområde. Når en bruger første gang forsøger at indlæse en app på en side, bliver vedkommende bedt om at logge på for at sikre, at brugeren har de nødvendige tilladelser til at bruge appen.

## <a name="editing-an-embedded-app"></a>Redigere en integreret app

Når en app er integreret på en side, har du muligvis behov for at foretage nogle ændringer af konfigurationen af appen. Det kan f.eks. være, du vil ændre den etiket, der er knyttet til den integrerede app, eller der er blevet oprettet en ny version af appen, og du skal opdatere App-id'et til at pege på den seneste.

Følg disse trin for at redigere konfigurationen af en integreret app:

1. Gå til ruden **Rediger appen**.

    - Hvis den integrerede app åbnes via menuknappen Power Apps, skal du højreklikke på menuknappen Power Apps og vælge **Personaliser**. Vælg den app, du vil konfigurere, i rullemenuen **Vælg en app**.
    - Hvis den integrerede app vises direkte på siden, skal du vælge **Indstillinger** og derefter vælge **Tilpas denne side**. Brug værktøjet **Vælg**, og klik på den integrerede app.

2. Foretag de nødvendige ændringer af appkonfigurationen, og klik derefter på **Gem**.

## <a name="removing-an-app"></a>Fjerne en app

Når en app er integreret på en side, er der to måder til at fjerne den, hvis det er nødvendigt:

- Gå til ruden **Rediger en app** ved at følge vejledningen fra afsnittet [Redigere en integreret app](#editing-an-embedded-power-app) tidligere i dette emne. Bekræft, at ruden vises oplysninger for den integrerede app, du vil fjerne, og klik derefter på knappen **Slet**.
- Eftersom den integrerede app er gemt som tilpasningsdata, vil fjernelse af din sides tilpasning også fjerne eventuelle integrerede apps på den pågældende side. Bemærk, at rydning af sidens tilpasning er permanent og ikke kan fortrydes. Hvis du vil fjerne dine tilpasninger på en side, skal du vælge **Indstillinger** og derefter klikke på **Tilpas denne side** og til sidst på knappen **Ryd**. Når du har opdateret din browser, fjernes alle de tidligere tilpasninger for denne side. Se [Tilpas brugeroplevelsen](personalize-user-experience.md) for at få flere oplysninger om, hvordan sider bruger tilpasninger.

## <a name="appendix"></a>Appendiks

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Udviklerkontrol med hvor en app kan integreres

Som standard kan brugere integrere apps på enhver side, enten under menuknappen Power Apps eller direkte på siden som en fane, et oversigtspanel, et blad eller som en ny sektion i et arbejdsområde. Hvis det er nødvendigt, kan udviklerne imidlertid også konfigurere denne funktion til kun at tillade integrering af apps på visse sider ved at implementere følgende metoder:

- **isPowerAppPersonalizationEnabled**– Hvis denne metode returnerer falsk for en bestemt side, vises menuknappen Power Apps ikke, og brugerne kan derfor ikke integrere apps et vilkårligt sted på denne side, herunder som en fane.
- **isPowerAppTabPersonalizationEnabled** – Hvis denne metode returnerer falsk for en bestemt side, kan brugerne ikke integrere apps direkte på siden som en fane, et oversigtspanel eller en panoramasektion. Brugere vil stadig kunne integrere apps via menuknappen Power Apps, hvis integrering er tilladt på siden.

I følgende eksempel vises en ny klasse med de to metoder, der skal bruges til at konfigurere, hvor apps kan integreres.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
