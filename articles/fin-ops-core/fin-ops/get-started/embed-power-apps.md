---
title: Integrere lærredapps fra Power Apps
description: Dette emne beskriver, hvordan du kan integrere lærredapps fra Microsoft Power Apps i klienten for at øge produktets funktioner.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 32bf477bb42657b06f22f7677dcb580b38f0a55c
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488048"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Integrere lærredapps fra Power Apps

[!include [banner](../includes/banner.md)]

Microsoft Power Apps er en tjeneste, der giver udviklere og ikke-tekniske brugere mulighed for at oprette brugerdefinerede forretningsapps til mobilenheder, tablets og internettet uden at skrive kode. Finance and Operations-apps understøtter integration med Power Apps. Lærredapps, som du, din organisation eller det bredere økosystem udvikler, kan integreres i Finance and Operations-apps for at øge produktets funktionalitet. Du kan f.eks. opbygge en lærredapp fra Power Apps, der supplerer en Finance and Operations-app med oplysninger, der er hentet fra et andet system.

Hvis du vil vide mere om integration af lærredapps, kan du se den korte video [Sådan integreres lærredapps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Tilføjelse af en integreret lærredapp fra Power Apps til en side

Før du integrerer en lærredapp fra Power Apps i klienten, skal du finde eller oprette en app, der har den ønskede grafik eller funktionalitet. Dette emne omfatter ikke en detaljeret beskrivelse af processen til oprettelse af apps. Hvis du ikke vant til at bruge Power Apps, kan du se [dokumentationen til Power Apps](/powerapps/).

Du kan integrere en lærredapp i en Finance and Operations-app på tre måder. Du kan bruge den fremgangsmåde, der passer bedst til dit scenarie. 

- Integrer lærredappen i **Power Apps**-knappen i standardhandlingsruden på en side. Apps, som du tilføjer på denne måde, vises som elementer på **Power Apps**-menuknappen, og appsene åbnes i sideruder. 
- Integrer lærredappen direkte på en eksisterende side som en ny fane (pivot-fane, oversigtspanel, blad eller arbejdsområdesektionen).
- Opret en ny fuld side-oplevelse for lærredappen eller webstedet fra dashboardet.

Når du konfigurerer din integrerede lærredapp, kan du vælge et enkelt felt, du vil sende som kontekst til appen. Dette trin gør, at appen kan reagere på basis af de data, du aktuelt får vist.

> [!NOTE]
> Du kan ikke bruge denne metode til at integrere modelbaserede apps.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Integration af en lærredapp på en eksisterende side

Følgende procedure viser, hvordan du integrerer en lærredapp på en eksisterende side fra Power Apps.

1. Gå til siden, hvor du vil integrere lærredappen. Denne side vil indeholde de data, der skal sendes til appen som input.
2. Åbn ruden **Tilføj en app fra Power Apps**:

    - Hvis appen bliver integreret direkte på siden, skal du vælge **Indstillinger** \> **Tilpas denne side** \> **Mere** og derefter følge et af disse trin:

        - Hvis funktionen **Fuld side-apps** er aktiveret, skal du vælge **Tilføj en side** og derefter vælge det område, hvor du vil tilføje appen. Hvis du vil integrere appen i **Power Apps**-menuknappen, skal du vælge handlingsruden. Hvis du vil integrere appen direkte på siden, skal du vælge den relevante fane, oversigtspanel, blad eller sektion (hvis du er på et arbejdsområde). Vælg derefter **Power Apps** i ruden **Tilføj en app**.
        - Hvis funktionen **Fuld side-apps** er deaktiveret, skal du vælge **Tilføj en app fra Power Apps** og derefter vælge det område, hvor du vil tilføje appen. Hvis du vil integrere appen i **Power Apps**-menuknappen, skal du vælge handlingsruden. Hvis du vil integrere appen direkte på siden, skal du vælge den relevante fane, oversigtspanel, blad eller sektion (hvis du er på et arbejdsområde).

    - Hvis appen skal åbnes ved hjælp af **Power Apps**-menuknappen , kan du vælge **Power Apps**-menuknappen i standardhandlingsruden og derefter vælge **Tilføj en app**.

3. Konfigurer den integrerede app. Du kan finde flere oplysninger i afsnittet [Konfiguration af en lærredapp](#configuring-a-canvas-app) senere i dette emne.
4. Når du bekræfter, at konfigurationen er korrekt, skal du vælge **Indsæt**.

    - Hvis funktionen **Gemte visninger** er deaktiveret, bliver du bedt om at opdatere browseren for at se den integrerede app.
    - Hvis funktionen **Gemte visninger** er aktiveret, skal du gemme visningen for at bevare ændringen.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Integration af en lærredapp som en fuld side-oplevelse fra dashboardet

Du kan også integrere en lærredapp fra dashboardet, hvis appen ikke er tilknyttet en eksisterende side, eller hvis du blot vil vise appen som en fuld side-oplevelse i Finance and Operations-appen.

> [!NOTE]
> Hvis du vil gøre denne egenskab tilgængelig, skal du aktivere funktionen **Fuld side-apps** i Funktionsstyring. 

1. Åbn dashboardet.
2. Vælg og hold (eller højreklik) på siden, vælg **Tilpas**, og vælg derefter **Tilføj en side**.
3. I ruden **Tilføj en side** skal du vælge **Power Apps**.
4. Konfigurer den integrerede app. Du kan finde flere oplysninger i afsnittet [Konfiguration af en lærredapp](#configuring-a-canvas-app) senere i dette emne.
5. Vælg **Gem** for at føje appen til dashboardet som et nyt felt.
6. Vælg det nye felt på dashboardet, og bekræft, at lærredappen vises som forventet.

### <a name="configuring-a-canvas-app"></a>Konfiguration af en lærredapp

Når du integrerer en lærredapp, skal du angive følgende parametre:

- **Navn** – Angiv den tekst, der skal vises for knappen eller fanen, som vil indeholde den integrerede app. Ofte ønsker du at gentage navnet på appen i dette felt.
- **App-id** – Angiv Globally Unique Identifier (GUID) for den lærredapp, du vil integrere. For at hente denne værdi skal du finde appen på [make.powerapps.com](https://make.powerapps.com) og derefter kigge i feltet **App-id** under **Detaljer**.
- **Inputkontekst for appen** – Du kan eventuelt vælge det felt, der indeholder de data, du vil overføre til appen som input. Du finde finde oplysninger om, hvordan appen kan få adgang til data, der sendes fra Finance and Operations, i afsnittet [Opbygning af en app, der udnytter data sendt fra Finance and Operations-apps](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) senere i dette emne.

    Fra version 10.0.19 overføres den aktuelle juridiske enhed også til lærredappen som kontekst via URL-parameteren **cmp**. Denne funktionsmåde påvirker ikke mållærredappen, før den pågældende app bruger oplysningerne.

- **Programstørrelse** – Vælg den type app, du vil integrere. Vælg **Tynd** til apps, der er bygget til mobilenheder, eller **Bred** til apps, der er bygget til tablets. Denne parameter sikrer, at der allokeres tilstrækkelig plads til den integrerede app.
- **Juridiske enheder** – Du kan vælge de juridiske enheder, som appen skal være tilgængelig for. Som standard er appen tilgængelig for alle juridiske enheder. Denne indstilling er kun tilgængelig, når du integrerer direkte på en eksisterende side, og funktionen **[Gemte visninger](saved-views.md)** er deaktiveret.

## <a name="sharing-an-embedded-app"></a>Deling af en integreret app

Når du har integreret en lærredapp på en side og bekræftet, at den fungerer korrekt, ønsker du muligvis at dele appen med andre brugere i systemet. Du kan dele en integreret lærredapp ved at følge disse trin.

1. [Del lærredappen i Power Apps](/powerapps/maker/canvas-apps/share-app) med de relevante brugere, så de kan få adgang til appen direkte i Power Apps.
2. Del de tilpasninger, der er knyttet til den integrerede app, med de ønskede brugere. Du kan bruge en af følgende fremgangsmåder:

    - **Publicer visningen (anbefales):** Hvis funktionen **[Gemte visninger](saved-views.md)** er aktiveret, er den anbefalede og foretrukne fremgangsmåde at oprette en visning, der omfatter den integrerede lærredapp, og derefter publicere visningen til de ønskede brugere. Denne fremgangsmåde sikrer, at alle brugere, der har sikkerhedsroller, som er omfattet af den publicerede visning, kan se lærredappen på siden.

        Du kan også publicere en lærredapp, der er integreret som en fuld side-oplevelse fra dashboardet. Vælg og hold (eller højreklik på) det felt på dashboardet, som er knyttet til appen, vælg **Tilpas**, og vælg derefter **Publicer side**. Visningen svarer til *Publicering af visninger*, og du kan vælge de sikkerhedsroller, der skal udgives til. I opdatering 10.0.21 eller senere, hvis funktionen **Forbedret understøttelse af juridiske enheder for gemte visninger** er slået til, kan du også publicere appen til de ønskede juridiske enheder.

    - Hvis funktionen **Gemte visninger** er deaktiveret, kan systemadministratoren angive en tilpasning, der omfatter lærredappen, for det relevante sæt af brugere via siden **Tilpasning**. Du kan også eksportere sidens tilpasninger og derefter sende dem til en eller flere brugere. Hver af disse brugere kan derefter importere tilpasningen. Tilpasningsværktøjslinjen indeholder knapper til eksport og import af tilpasninger.

> [!NOTE]
> Hvis lærredappen er delt med eksterne brugere, kan disse brugere ikke bruge den integrerede app i Finance and Operations-apps. De kan dog få adgang til appen direkte i Power Apps. Eksterne brugere omfatter gæster og brugere, der ikke tilhører Microsoft 365 Azure Directory, hvor Finance and Operations-appen er installeret.

Se [Tilpasse brugeroplevelsen](personalize-user-experience.md) for at få yderligere oplysninger om tilpasningsmuligheder i produktet, og hvordan de bruges.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Oprette en lærredapp, der bruger data, som er sendt fra Finance and Operations-apps

Når du opretter en lærredapp, der skal integreres i en Finance and Operations-app, er det en vigtig del af processen at bruge inputdataene fra den pågældende Finance and Operations-app. Fra Power Apps-udviklingsoplevelsen kan der opnås adgang til inputdata, der er overført fra en Finance and Operations-app, ved hjælp af variablen **Param ("EntityId")**. Fra version 10.0.19 overføres den aktuelle juridiske enhed også som lærredappen via variablen **Param("cmp")**. 

For eksempel kan du i funktionen OnStart i appen indstille de indgående data fra Finance and Operations-apps til en variabel som denne:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Få vist en lærredapp

For at få vist en integreret lærredapp på en side i Finance and Operations-apps skal du blot gå til en side, der har en integreret app. Husk, at du har adgang til apps ved hjælp af **Power Apps**-knappen i standardhandlingsruden. De kan også vises direkte på siden som en ny fane, et oversigtspanel eller blad eller som et nyt afsnit i et arbejdsområde. Når brugerne første gang forsøger at indlæse en app på en side, bliver de bedt om at logge på. Dette trin sikrer, at brugerne har de relevante rettigheder til at bruge appen.

## <a name="editing-an-embedded-app"></a>Redigere en integreret app

Når en app er integreret på en side, har du muligvis behov for at foretage nogle ændringer af konfigurationen af appen. Det kan f.eks. være, du vil ændre den etiket, der er knyttet til den integrerede app, eller der er blevet oprettet en ny version af appen, og du skal opdatere App-id'et til at pege på den seneste.

Følg disse trin for at redigere konfigurationen af en integreret app:

1. Gå til ruden **Rediger appen**.

    - Hvis den integrerede app åbnes via Power Apps-menuknappen , skal du vælge og holde (eller højreklikke på) Power Apps-menuknappen og vælge **Tilpas**. Vælg den app, du vil konfigurere, i rullemenuen **Vælg en app**.
    - Hvis den integrerede app vises direkte på siden, skal du vælge **Indstillinger** og derefter vælge **Tilpas denne side**. Brug værktøjet **Vælg**, og klik på den integrerede app.
    - Hvis den integrerede app er tilføjet fra dashboardet, skal du åbne dashboardet, vælge og holde (eller højreklikke på) det felt, der er tilknyttet lærredappen, vælge **Tilpas** og derefter vælge **Rediger side**.

2. Foretag de nødvendige ændringer af appkonfigurationen, og klik derefter på **Gem**.

## <a name="removing-an-app"></a>Fjerne en app

Når en app er integreret på en side, er der nogle få metoder til at fjerne den, hvis det er nødvendigt:

- Gå til ruden **Rediger en app** ved at følge vejledningen fra afsnittet [Redigere en integreret app](#editing-an-embedded-app) tidligere i dette emne. Bekræft, at ruden vises oplysninger for den integrerede app, du vil fjerne, og klik derefter på knappen **Slet**.
- Hvis den integrerede app er tilføjet fra dashboardet, skal du åbne dashboardet, vælge og holde (eller højreklikke på) det felt, der er tilknyttet lærredappen, vælge **Tilpas** og derefter vælge **Fjern side**. 
- Eftersom den integrerede app er gemt som tilpasningsdata, vil fjernelse af din sides tilpasning også fjerne eventuelle integrerede apps på den pågældende side. Bemærk, at rydning af sidens tilpasning er permanent og ikke kan fortrydes. Hvis du vil fjerne dine tilpasninger på en side, skal du vælge **Indstillinger** og derefter klikke på **Tilpas denne side** og til sidst på knappen **Ryd**. Når du har opdateret din browser, fjernes alle de tidligere tilpasninger for denne side. Se [Tilpas brugeroplevelsen](personalize-user-experience.md) for at få flere oplysninger om, hvordan sider bruger tilpasninger.

## <a name="appendix"></a>Appendiks

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Udvikler] Modellering af en lærredapp i en formular

Mens dette emne fokuserer på integration af lærredapps gennem tilpasning, har udviklere også mulighed for at føje en lærredapp til en formular ved hjælp af Visual Studio-udviklingsløsningen. Det kan du gøre ved blot at føje en PowerAppsHostControl til formularen. De metadataegenskaber, der er tilgængelige i kontrolelementet, indeholder de samme egenskaber som tilpasningsfunktionen.

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Udvikler] Angiver, hvor en app kan integreres

Som standard kan brugere integrere apps på enhver side, enten under menuknappen Power Apps eller direkte på siden som en fane, et oversigtspanel, et blad eller som en ny sektion i et arbejdsområde. Hvis det er nødvendigt, kan udviklerne imidlertid også konfigurere denne funktion til kun at tillade integrering af apps på visse sider ved at implementere følgende metoder:

- **isPowerAppPersonalizationEnabled**– Hvis denne metode returnerer falsk for en bestemt side, vises menuknappen Power Apps ikke, og brugerne kan derfor ikke integrere apps et vilkårligt sted på denne side, herunder som en fane.
- **isPowerAppTabPersonalizationEnabled** – Hvis denne metode returnerer falsk for en bestemt side, kan brugerne ikke integrere apps direkte på siden som en fane, et oversigtspanel eller en panoramasektion. Brugere vil stadig kunne integrere apps via menuknappen Power Apps, hvis integrering er tilladt på siden.

I følgende eksempel vises en ny klasse med de to metoder, der skal bruges til at konfigurere, hvor apps kan integreres.

```powerapps
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

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
