---
title: Integrere lærredsapps fra Power Apps
description: Dette emne beskriver, hvordan du kan integrere lærredapps fra Microsoft Power Apps i klienten for at øge produktets funktioner.
author: jasongre
ms.date: 11/03/2020
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
ms.openlocfilehash: 7b20d24f79bd84f516e005b9d4a0ecdf6ef848fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752884"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Integrere lærredsapps fra Power Apps

[!include [banner](../includes/banner.md)]

Microsoft Power Apps er en tjeneste, der giver udviklere og ikke-tekniske brugere mulighed for at oprette brugerdefinerede forretningsapps til mobilenheder, tablets og internettet uden at skrive kode. Finance and Operations-apps understøtter integration med Power Apps. Lærredapps, som du, din organisation eller det bredere økosystem udvikler, kan integreres i Finance and Operations-apps for at øge produktets funktionalitet. Du kan f.eks. opbygge en lærredapp fra Power Apps, der supplerer en Finance and Operations-app med oplysninger, der er hentet fra et andet system.

Hvis du vil vide mere om Power Apps, kan du se den korte video [Sådan integreres Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Tilføjelse af en integreret lærredapp fra Power Apps til en side

### <a name="overview"></a>Overblik

Før du integrerer en lærredapp fra Power Apps i klienten, skal du finde eller oprette en app, der har den ønskede grafik eller funktionalitet. Dette emne omfatter ikke en detaljeret beskrivelse af processen til oprettelse af apps. Hvis du ikke vant til at bruge Power Apps, kan du se [dokumentationen til Power Apps](https://docs.microsoft.com/powerapps/).

Du kan få adgang til en specifik lærredapp på en side på to måder, når du er klar til at integrere appen. Du kan vælge, hvilken fremgangsmåde der passer bedre til dit scenarie. Det første fremgangsmåde bruger knappen **Power Apps**, der er føjet til standardhandlingsruden. De apps, du tilføjer ved hjælp af denne fremgangsmåde, vises som elementer på menuknappen for **Power Apps**. Når du vælger et af disse elementer, vises en siderude, der indeholder den integrerede app. Du kan også integrere en app direkte på en side, som en ny fane, et oversigtspanel eller blad eller som et nyt afsnit i et arbejdsområde.

Når du konfigurerer din integrerede lærredapp, kan du vælge et enkelt felt, du vil sende som kontekst til appen. Dette trin gør, at appen kan reagere på basis af de data, du aktuelt får vist.

> [!NOTE]
> Du kan i øjeblikket ikke bruge denne metode til at integrere udformede apps.  

### <a name="details"></a>Detaljer

Følgende procedure viser, hvordan du integrerer en lærredapp fra Power Apps i webklienten.

1. Gå til siden, hvor du vil integrere lærredappen. Denne side er den samme side, der indeholder de data, der skal sendes til appen som input.
2. Åbn ruden **Tilføj en app fra Power Apps**:

    - Klik på **Indstillinger**, og vælg derefter **Tilpas denne side**. Under menuen **Indsæt** skal du vælge **Power Apps**. Endelig skal du vælge det område, hvor du vil tilføje appen. Hvis du vil integrere appen under menuknappen Power Apps, skal du vælge handlingsruden. Hvis du vil integrere appen direkte på siden, skal du vælge den eller det relevante fane, oversigtspanel, blad eller afsnit (hvis du er på et arbejdsområde).
    - Hvis appen skal åbnes ved hjælp af menuknappen Power Apps, kan du også klikke på menuknappen **Power Apps** i standardhandlingsruden og derefter vælge **Tilføj en app**.

3. Konfigurere den integrerede app:

    - Feltet **Navn** angiver den tekst, der vises for knappen eller fanen, der indeholder den integrerede app. Ofte ønsker du blot at gentage navnet på appen i dette felt.
    - Feltet **App-id** angiver Globally Unique Identifier (GUID) for den lærredapp, du vil integrere. For at hente denne værdi skal du finde appen på [make.powerapps.com](https://make.powerapps.com) og derefter kigge i feltet **App-id** under **Detaljer**.
    - Som **Inputkontekst for appen** kan du eventuelt vælge det felt, der indeholder de data, du vil overføre til appen som input. Se afsnittet senere i dette emne med titlen [Opbygning af en app, der udnytter data afsendt fra Finance and Operations-apps](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) for at få oplysninger om, hvordan appen kan få adgang til data, der er sendt fra Finance and Operations-apps.
    - Vælg den **Programstørrelse**, der svarer til den type app, du vil integrere. Vælg **Tynd** til apps, der er bygget til mobilenheder, og **Bred** til apps, der er bygget til tablets. Dette sikrer, at der allokeres en tilstrækkelig mængde plads til den integrerede app.
    - Oversigtspanelet **Juridiske enheder** giver mulighed for at vælge, hvilke juridiske enheder appen er tilgængelig for. Standarden er at gøre appen tilgængelig for alle juridiske enheder. Denne indstilling er kun tilgængelig, når funktionen [Gemte visninger](saved-views.md) er deaktiveret. 

4. Når du har bekræftet, at konfigurationen er korrekt, skal du klikke på **Indsæt** for at integrere Power App på siden. Du bliver bedt om at opdatere browseren for at få vist den integrerede app.

## <a name="sharing-an-embedded-app"></a>Deling af en integreret app

Når du har integreret en lærredapp på en side og bekræftet, at den fungerer korrekt med alle typer datakontekst, der er overført fra pågældende side, ønsker du muligvis at dele appen med andre brugere i systemet. Du kan dele en integreret lærredapp ved at følge disse trin.

1. [Del lærredappen](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) med de relevante brugere, så de kan få adgang til appen i Power Apps. 

2. Sørg for, at de målrettede brugere har de relevante tilpasninger, så den integrerede app vises, når brugerne får vist siden. Du kan bruge en af følgende fremgangsmåder:

    - Anbefalet: Brug funktionen [Gemte visninger](saved-views.md) til at oprette og publicere en visning, der indeholder den integrerede app. Denne fremgangsmåde sikrer, at alle brugere, der har sikkerhedsroller, som er målrettet af den publicerede visning, kan se appen i Finance and Operations-apps. 
    - Hvis du ikke har aktiveret funktionen Gemte visninger, kan du få systemadministratoren til at sende en tilpasning, der omfatter den integrerede app, til alle brugere eller et undersæt af brugere. Du kan også eksportere din sides tilpasninger og sende dem til én eller flere brugere. Hver af disse brugere kan derefter importere tilpasningerne. Tilpasningsværktøjslinjen har handlinger, der giver dig mulighed for at eksportere og importere tilpasninger. 
    
> [!NOTE]
> Hvis lærredappen er delt med eksterne brugere, kan disse brugere ikke bruge den integrerede app i Finance and Operations-apps. De kan dog få adgang til appen direkte i Power Apps. Eksterne brugere omfatter gæster og brugere, der ikke tilhører Microsoft 365 Azure Directory, hvor Finance and Operations-appen er installeret.

Se [Tilpasse brugeroplevelsen](personalize-user-experience.md) for at få yderligere oplysninger om tilpasningsmuligheder i produktet, og hvordan de bruges.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Oprette en lærredapp, der bruger data, som er sendt fra Finance and Operations-apps

Når du opretter en lærredapp, der skal integreres i en Finance and Operations-app, er det en vigtig del af processen at bruge inputdataene fra den pågældende Finance and Operations-app. Fra Power Apps-udviklingsoplevelsen kan der opnås adgang til inputdata, der er overført fra en Finance and Operations-app, ved hjælp af variablen **Param ("EntityId")**.

For eksempel kan du i funktionen OnStart i appen indstille de indgående data fra Finance and Operations-apps til en variabel som denne:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Få vist en lærredapp

For at få vist en integreret lærredapp på en side i Finance and Operations-apps skal du blot gå til en side, der har en integreret app. Husk, at du har adgang til apps ved hjælp af **Power Apps**-knappen i standardhandlingsruden. De kan også vises direkte på siden som en ny fane, et oversigtspanel eller blad eller som et nyt afsnit i et arbejdsområde. Når brugerne første gang forsøger at indlæse en app på en side, bliver de bedt om at logge på. Dette trin sikrer, at brugerne har de relevante rettigheder til at bruge appen.

## <a name="editing-an-embedded-app"></a>Redigere en integreret app

Når en app er integreret på en side, har du muligvis behov for at foretage nogle ændringer af konfigurationen af appen. Det kan f.eks. være, du vil ændre den etiket, der er knyttet til den integrerede app, eller der er blevet oprettet en ny version af appen, og du skal opdatere App-id'et til at pege på den seneste.

Følg disse trin for at redigere konfigurationen af en integreret app:

1. Gå til ruden **Rediger appen**.

    - Hvis den integrerede app åbnes via menuknappen Power Apps, skal du højreklikke på menuknappen Power Apps og vælge **Personaliser**. Vælg den app, du vil konfigurere, i rullemenuen **Vælg en app**.
    - Hvis den integrerede app vises direkte på siden, skal du vælge **Indstillinger** og derefter vælge **Tilpas denne side**. Brug værktøjet **Vælg**, og klik på den integrerede app.

2. Foretag de nødvendige ændringer af appkonfigurationen, og klik derefter på **Gem**.

## <a name="removing-an-app"></a>Fjerne en app

Når en app er integreret på en side, er der to måder til at fjerne den, hvis det er nødvendigt:

- Gå til ruden **Rediger en app** ved at følge vejledningen fra afsnittet [Redigere en integreret app](#editing-an-embedded-app) tidligere i dette emne. Bekræft, at ruden vises oplysninger for den integrerede app, du vil fjerne, og klik derefter på knappen **Slet**.
- Eftersom den integrerede app er gemt som tilpasningsdata, vil fjernelse af din sides tilpasning også fjerne eventuelle integrerede apps på den pågældende side. Bemærk, at rydning af sidens tilpasning er permanent og ikke kan fortrydes. Hvis du vil fjerne dine tilpasninger på en side, skal du vælge **Indstillinger** og derefter klikke på **Tilpas denne side** og til sidst på knappen **Ryd**. Når du har opdateret din browser, fjernes alle de tidligere tilpasninger for denne side. Se [Tilpas brugeroplevelsen](personalize-user-experience.md) for at få flere oplysninger om, hvordan sider bruger tilpasninger.

## <a name="appendix"></a>Appendiks

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