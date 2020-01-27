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
ms.openlocfilehash: 8b5e64cb9ba916f9cbd628703394318b4044867b
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870235"
---
# <a name="embed-microsoft-power-apps"></a>Integrer Microsoft Power Apps

[!include [banner](../includes/banner.md)]

I Platform update 14 understøtter integration med Microsoft Power Apps, en tjeneste til udviklere og ikke-tekniske brugere til opbygning af brugerdefinerede forretningsapps til mobilenheder, tablets og internettet uden at skrive kode. Power Apps, der er udviklet af dig, din organisation eller det bredere økosystem, kan derefter integreres i Finance and Operations-appen for at øge produktets funktionalitet. Du kan f.eks. opbygge en Power App, der supplerer Finance and Operations-apps med oplysninger, der er hentet fra et andet system.

Hvis du vil vide mere om Power Apps, kan du se den korte video [Sådan integreres Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-power-app-to-a-page"></a>Tilføjelse af en integreret Power App til en side

### <a name="overview"></a>Overblik

Før du integrerer en Power App i klienten, skal du først finde eller oprette en Power App med den ønskede grafik og/eller funktionalitet. Vi beskriver ikke i detaljer processen til oprettelse af en Power App her. Emnet [Introduktion til Power Apps](https://docs.microsoft.com/powerapps/getting-started) er et godt udgangspunkt, hvis du ikke kender Power Apps.

Når du er klar til at integrere en bestemt Power App, kan du vælge mellem en af to måder til at få adgang til Power App'en på en side, afhængig af hvilken måde der passer bedst til dit scenarie. Den første måde er via knappen Power Apps, der er føjet til standardhandlingsruden. Power Apps, der er tilføjet ved hjælp af denne mekanisme, vises som menupunkter i menuknappen Power Apps. Når den vælges, åbner hver af disse menupunkter en siderude, der indeholder den integrerede Power App. Du kan også vælge at få vist en Power App direkte på en side, som en ny fane, et oversigtspanel, blad eller som et nyt afsnit i et arbejdsområde.

Når du konfigurerer din integrerede Power App, kan du vælge et enkelt felt, du vil sende som input til Power App'en. Dette giver mulighed for, at Power App'en kan reagere på basis af de data, du aktuelt får vist.

### <a name="details"></a>Oplysninger

Følgende instruktioner viser, hvordan du integrerer en Power App i webklienten.

1. Gå til siden, hvor du vil integrere Power App'en. Dette er den samme side, der indeholder de data, der skal sendes til Power App'en som input.
2. Åbn ruden **Indsæt en Power App**:

    - Klik på **Indstillinger**, og vælg derefter **Tilpas denne formular**. Under menuen **Indsæt** skal du vælge **Power App**. Endelig skal du vælge det område, hvor du vil tilføje Power App'en. Hvis du vil integrere Power App'en under menuknappen Power Apps, skal du vælge handlingsruden. Hvis du vil integrere Power App'en direkte på siden, skal du vælge den eller det relevante fane, oversigtspanel, blad eller afsnit (hvis du er på et arbejdsområde).
    - Hvis Power App skal åbnes ved hjælp af menuknappen Power Apps, kan du også klikke på menuknappen **Power Apps** i standardhandlingsruden og derefter vælge **Indsæt en Power App**.

3. Konfigurere den integrerede Power App:

    - Feltet **Navn** angiver den tekst, der vises for knappen eller fanen, der indeholder den integrerede Power App. Ofte ønsker du blot at gentage navnet på Power App'en i dette felt.
    - **App-ID** er GUID'et for den Power App, du vil integrere. For at hente denne værdi skal du finde Power App'en på [web.powerapps.com](https://web.powerapps.com) og derefter finde feltet **App-id** feltet under **Detaljer**.
    - Som **Inputdata for Power App** kan du eventuelt vælge det felt, der indeholder de data, du vil overføre til Power App som input. Se afsnittet senere i dette emne med titlen [Oprette en Power App, der anvender data fra Finance and Operations-apps](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) for at få flere oplysninger om, hvordan Power App får adgang til de data, der er sendt fra Finance and Operations-apps.
    - Vælg den **Programstørrelse**, der svarer til den type Power App, du vil integrere. Vælg **Tynd** for Power Apps, der er bygget til mobilenheder, og **Bred** for Power Apps, der er bygget til tablets. Dette sikrer, at der allokeres en tilstrækkelig mængde plads til den integrerede Power App.
    - Oversigtspanelet **Juridiske enheder** giver mulighed for at vælge, hvilke juridiske enheder Power App'en er tilgængelig for. Standarden er at vise Power App'en i alle juridiske enheder.

4. Når du har bekræftet, at konfigurationen er korrekt, skal du klikke på **Indsæt** for at integrere Power App på siden. Du bliver bedt om at opdatere browseren for at få vist den integrerede Power App.

## <a name="sharing-an-embedded-power-app"></a>Deling af en integreret Power App

Når du har integreret en Power App på en side og bekræftet, at den fungerer korrekt med alle typer datakontekst, der blev overført fra siden, ønsker du muligvis at dele denne integrerede Power App med andre brugere i systemet. Dette kan gøres på to forskellige måder ved hjælp af funktionerne til brugertilpasning af produktet:

- Det anbefalede scenarie er via systemadministratoren, der kan overføre en tilpasning til alle brugere eller en undergruppe af brugere.
- Du kan også eksportere dine sidetilpasninger og sende dem til en eller flere brugere og få hver af disse brugere til at importere disse ændringer. Indstillingen Administrer på værktøjslinjen for personlige indstillinger giver dig mulighed for at eksportere og importere tilpasninger.

Se [Tilpasse brugeroplevelsen](personalize-user-experience.md) for at få yderligere oplysninger om tilpasningsmuligheder i produktet, og hvordan de bruges.

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Oprettelse af en Power App, der udnytter data, der sendes fra Finance and Operations-apps

En vigtig del ved at opbygge en Power App, som kan integreres med Finance and Operations-apps, er at udnytte de indgående data fra Finance and Operations-apps. I Power App'en er der adgang til data ved hjælp af variablen Param("EntityId").

F.eks. kan du i funktionen OnStart i Power App'en indstille de indgående data fra Finance and Operations-apps til en variabel som denne:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Visning af en integreret Power App

For at få vist en integreret Power App på en side i Finance and Operations-apps skal du gå til en side med en integreret Power App. Tilbagekald, at Power Apps kan åbnes via knappen Power Apps i standardhandlingsruden, eller at den kan vises direkte på siden som en ny fane, et oversigtspanel, et blad eller som en ny sektion i et arbejdsområde. Når en bruger første gang forsøger at indlæse en Power App på en side, bliver vedkommende bedt om at logge på Power Apps for at sikre, at brugeren har de nødvendige tilladelser til at bruge Power App'en.

## <a name="editing-an-embedded-power-app"></a>Redigere en integreret Power App

Når en Power App er integreret på en side, har du muligvis behov for at foretage nogle ændringer af konfigurationen af den pågældende Power App. Du vil f.eks. ændre den etiket, der er knyttet til den integrerede Power App, eller der er blevet oprettet en ny version af en Power App, og du skal opdatere App-id'et til at pege på den seneste Power App.

Følg disse trin for at redigere konfigurationen af en integreret Power App:

1. Gå til ruden **Rediger en Power App**.

    - Hvis den integrerede Power App åbnes via menuknappen Power Apps, skal du højreklikke på menuknappen Power Apps og vælge **Personaliser**. Vælg den Power App, du vil konfigurere, i rullemenuen **Vælg Power App**.
    - Hvis den integrerede Power App vises direkte på siden, skal du vælge **Indstillinger** og derefter vælge **Personaliser denne formular**. Brug værktøjet **Vælg**. og klik på den integrerede Power App.

2. Foretag de nødvendige ændringer af Power Apps-konfigurationen, og klik derefter på **Gem**.

## <a name="removing-an-embedded-power-app"></a>Fjerne en integreret Power App

Når en Power App er integreret på en side, er der to måder til at fjerne den, hvis det er nødvendigt:

- Gå til ruden **Rediger en Power App** ved at følge vejledningen fra afsnittet [Redigere en integreret Power App](#editing-an-embedded-power-app) tidligere i dette emne. Bekræft, at ruden vises oplysninger for den integrerede Power App, du vil fjerne, og klik derefter på knappen **Slet**.
- Fordi en integreret Power App er gemt som tilpasningsdata, vil fjernelse af din sides tilpasning også fjerne eventuelle integrerede Power Apps på den pågældende side. Bemærk, at rydning af sidens tilpasning er permanent og ikke kan fortrydes. Hvis du vil fjerne dine tilpasninger på en side, skal du vælge **Indstillinger** og derefter klikke på **Tilpas denne formular**. Under menuen **Administrer** skal du vælge knappen **Ryd**. Når du har opdateret din browser, fjernes alle de tidligere tilpasninger for denne side. Se [Tilpas brugeroplevelsen](personalize-user-experience.md) for at få flere oplysninger om, hvordan sider bruger tilpasninger.

## <a name="appendix"></a>Appendiks

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Udviklerkontrol med hvor en Power App kan integreres

Som standard kan brugere integrere Power Apps på enhver side, enten under menuknappen Power Apps eller direkte på siden som en fane, et oversigtspanel, et blad eller som en ny sektion i et arbejdsområde. Hvis det er nødvendigt, kan udviklerne imidlertid også konfigurere denne funktion til kun at tillade integrering af Power Apps på visse sider ved at implementere følgende metoder:

- **isPowerAppPersonalizationEnabled** – Hvis denne metode returnerer falsk for en bestemt side, vises menuknappen Power Apps ikke, og brugerne kan derfor ikke integrere Power Apps et vilkårligt sted på denne side, herunder som en fane.
- **isPowerAppTabPersonalizationEnabled** – Hvis denne metode returnerer falsk for en bestemt side, kan brugerne ikke integrere Power Apps direkte på siden som en fane, et oversigtspanel eller en panoramasektion. Brugere vil stadig kunne integrere Power Apps via menuknappen Power Apps, hvis integrering er tilladt på siden.

I følgende eksempel vises en ny klasse med de to metoder, der skal bruges til at konfigurere, hvor Power Apps kan integreres.

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
