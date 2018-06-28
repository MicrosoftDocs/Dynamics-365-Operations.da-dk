---
title: Integrere PowerApps
description: "Dette emne beskriver, hvordan du kan integrere PowerApps i Finance and Operations-klienten for at øge produktets funktioner."
author: jasongre
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 07224faabcf2b183d4c8da0ba4588c33ec140d03
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="embed-powerapps"></a>Integrere PowerApps

[!include [banner](../includes/banner.md)]

I platformsopdatering 14 understøtter Microsoft Dynamics 365 for Finance and Operations integration med Microsoft PowerApps, en tjeneste til udviklere og ikke-tekniske brugere til opbygning af brugerdefinerede forretningsapps til mobilenheder, tablets og internettet uden at skrive kode. PowerApps, der er udviklet af dig, din organisation eller det bredere økosystem, kan derefter integreres i Finance and Operations-klienten for at øge produktets funktioner. Du kan f.eks. opbygge en PowerApp, der supplerer Finance and Operations med oplysninger, der er hentet fra et andet system. 

Hvis du vil vide mere om PowerApps, kan du se den korte video [Sådan integreres PowerApps i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Tilføjelse af en integreret PowerApp til en side
### <a name="overview"></a>Overblik
Før du integrerer en PowerApp i Finance and Operations-klienten, skal du først finde eller oprette en PowerApp med den ønskede grafik og/eller funktionalitet. Vi beskriver ikke i detaljer processen til oprettelse af en PowerApp her. Emnet [Introduktion til PowerApps](https://docs.microsoft.com/en-us/powerapps/getting-started) er et godt udgangspunkt, hvis du ikke kender PowerApps.

Når du er klar til at integrere en bestemt PowerApp, kan du vælge mellem en af to måder til at få adgang til PowerApp'en på en side, afhængig af hvilken måde der passer bedst til dit scenarie. Den første måde er via knappen PowerApps, der er føjet til standardhandlingsruden. PowerApps, der er tilføjet ved hjælp af denne mekanisme, vises som menupunkter i menuknappen PowerApps. Når den vælges, åbner hver af disse menupunkter en siderude, der indeholder den integrerede PowerApp. Du kan også vælge at få vist en PowerApp direkte på en side, som en ny fane, et oversigtspanel, blad eller som et nyt afsnit i et arbejdsområde. 

Når du konfigurerer din integrerede PowerApp i Finance and Operations, kan du vælge et enkelt felt, du vil sende som input til PowerApp'en. Dette giver mulighed for, at PowerApp'en kan reagere på basis af de data, du aktuelt får vist i Finance and Operations.  

### <a name="details"></a>Oplysninger
Følgende instruktioner viser, hvordan du integrerer en PowerApp i Finance and Operations-webklienten.  

1. Gå til siden, hvor du vil integrere PowerApp'en. Dette er den samme side, der indeholder de data, der skal sendes til PowerApp'en som input.  
2. Åbn ruden **Indsæt en PowerApp**:
   - Klik på **Indstillinger**, og vælg derefter **Tilpas denne formular**. Under menuen **Indsæt** skal du vælge **PowerApp**. Endelig skal du vælge det område, hvor du vil tilføje PowerApp'en. Hvis du vil integrere PowerApp'en under menuknappen PowerApps, skal du vælge handlingsruden. Hvis du vil integrere PowerApp'en direkte på siden, skal du vælge den eller det relevante fane, oversigtspanel, blad eller afsnit (hvis du er på et arbejdsområde).   
   - Hvis PowerApp skal åbnes ved hjælp af menuknappen PowerApps, kan du også klikke på menuknappen **PowerApps** i standardhandlingsruden, og derefter vælge **Indsæt en PowerApp**.  
3. Konfigurere den integrerede PowerApp:
   - Feltet **Navn** angiver den tekst, der vises for knappen eller fanen, der indeholder den integrerede PowerApp. Ofte ønsker du blot at gentage navnet på PowerApp'en i dette felt.  
   - **App-id** er GUID'et for den PowerApp, du vil integrere. For at hente denne værdi skal du finde PowerApp'en på [web.powerapps.com](https://web.powerapps.com) og derefter finde feltet **App-id** feltet under **Detaljer**.  
   - Som **Inputdata for PowerApp** kan du eventuelt vælge det felt, der indeholder de data, du vil overføre til PowerApp som input. Se afsnittet senere i dette emne, der hedder [Oprette en PowerApp, der anvender data fra Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations), for at få flere oplysninger om, hvordan PowerApp får adgang til de data, der er sendt fra Finance and Operations.  
   - Vælg den **programstørrelse**, der svarer til den type PowerApp, du vil integrere. Vælg **Tynd** til PowerApps, der er bygget til mobilenheder, og **Bred** til PowerApps, der er bygget til tablets. Dette sikrer, at der allokeres en tilstrækkelig mængde plads til den integrerede PowerApp.
   - Oversigtspanelet **Juridiske enheder** giver mulighed for at vælge, hvilke juridiske enheder PowerApp'en er tilgængelig for. Standarden er at vise PowerApp'en i alle juridiske enheder.  
4. Når du har bekræftet, at konfigurationen er korrekt, skal du klikke på **Indsæt** for at integrere PowerApp på siden. Du bliver bedt om at opdatere browseren for at få vist den integrerede PowerApp. 

## <a name="sharing-an-embedded-powerapp"></a>Deling af en integreret PowerApp
Når du har integreret en PowerApp på en side og bekræftet, at den fungerer korrekt med alle typer datakontekst, der blev overført fra siden, ønsker du muligvis at dele denne integrerede PowerApp med andre brugere i systemet. Dette kan gøres på to forskellige måder ved hjælp af funktionerne til brugertilpasning af produktet:

- Det anbefalede scenarie er via systemadministratoren, der kan overføre en tilpasning til alle brugere eller en undergruppe af brugere. 

- Du kan også eksportere dine sidetilpasninger og sende dem til en eller flere brugere og få hver af disse brugere til at importere disse ændringer. Indstillingen Administrer på værktøjslinjen for personlige indstillinger giver dig mulighed for at eksportere og importere tilpasninger.

Se [Tilpasse brugeroplevelsen](personalize-user-experience.md) for at få yderligere oplysninger om tilpasningsmuligheder i produktet, og hvordan de bruges.

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Oprettelse af en PowerApp, der udnytter data, der sendes fra Finance and Operations
En vigtig del ved at opbygge en PowerApp, som kan integreres med Finance and Operations, er at udnytte de indgående data fra Finance and Operations. I PowerApp'en er der adgang til data ved hjælp af variablen Param("EntityId").  

F.eks. kan du i funktionen OnStart i PowerApp'en angive de indgående data fra Finance and Operations til en variabel som denne:

If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, "")); 

## <a name="viewing-an-embedded-powerapp"></a>Visning af en integreret PowerApp
For at få vist en integreret PowerApp på en side i Finance and Operations, skal du gå til en side med en integreret PowerApp. Tilbagekald, at PowerApps kan åbnes via knappen PowerApps i standardhandlingsruden , eller at den kan vises direkte på siden som en ny fane, et oversigtspanel, et blad eller som en ny sektion i et arbejdsområde. Når en bruger første gang forsøger at indlæse en PowerApp på en side, bliver vedkommende bedt om at logge på PowerApps for at sikre, at brugeren har de nødvendige tilladelser til at bruge PowerApp'en.   

## <a name="editing-an-embedded-powerapp"></a>Redigere en integreret PowerApp
Når en PowerApp er integreret på en side, har du muligvis behov for at foretage nogle ændringer af konfigurationen af den pågældende PowerApp. Du vil f.eks. ændre den etiket, der er knyttet til den integrerede PowerApp, eller der er blevet oprettet en ny version af en PowerApp, og du skal opdatere App-id'et til at pege på den seneste PowerApp. 

Følg disse trin for at redigere konfigurationen af en integreret PowerApp:
1. Gå til ruden **Rediger en PowerApp**. 
   - Hvis den integrerede PowerApp åbnes via menuknappen PowerApps, skal du højreklikke på menuknappen PowerApps og vælge **Personaliser**. Vælg den PowerApp, du vil konfigurere, i rullemenuen **Vælg PowerApp**.  
   - Hvis den integrerede PowerApp vises direkte på siden, skal du vælge **Indstillinger** og derefter vælge **Personaliser denne formular**. Brug værktøjet **Vælg**. og klik på den integrerede PowerApp.  
2. Foretag de nødvendige ændringer af PowerApps-konfigurationen, og klik derefter på **Gem**.  

## <a name="removing-an-embedded-powerapp"></a>Fjerne en integreret PowerApp
Når en PowerApp er integreret på en side, er der to måder til at fjerne den, hvis det er nødvendigt: 

- Gå til ruden **Rediger en PowerApp** ved at følge vejledningen fra afsnittet [Redigere en integreret PowerApp](#editing-an-embedded-powerapp) tidligere i dette emne. Bekræft, at ruden vises oplysninger for den integrerede PowerApp, du vil fjerne, og klik derefter på knappen **Slet**. 

- Fordi en integreret PowerApp er gemt som tilpasningsdata, vil fjernelse af din sides tilpasning også fjerne eventuelle integrerede PowerApps på den pågældende side. Bemærk, at rydning af sidens tilpasning er permanent og ikke kan fortrydes. Hvis du vil fjerne dine tilpasninger på en side, skal du vælge **Indstillinger** og derefter klikke på **Tilpas denne formular**. Under menuen **Administrer** skal du vælge knappen **Ryd**. Når du har opdateret din browser, fjernes alle de tidligere tilpasninger for denne side. Se [Tilpasse brugeroplevelsen](personalize-user-experience.md) for at få flere oplysninger om, hvordan sider bruger tilpasninger.  

## <a name="appendix"></a>Appendiks 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Udviklerkontrol med hvor en PowerApp kan integreres
Som standard kan brugere integrere PowerApps på enhver side, enten under menuknappen PowerApps eller direkte på siden som en fane, et oversigtspanel, et blad eller som en ny sektion i et arbejdsområde. Hvis det er nødvendigt, kan udviklerne imidlertid også konfigurere denne funktion til kun at tillade integrering af PowerApps på visse sider ved at implementere følgende metoder: 

- **isPowerAppPersonalizationEnabled** – Hvis denne metode returnerer falsk for en bestemt side, så vises menuknappen PowerApps vises ikke, og brugerne vil ikke kunne integrere PowerApps i et vilkårligt sted på denne side, herunder som en fane. 

- **isPowerAppTabPersonalizationEnabled** - Hvis denne metode returnerer falsk for en bestemt side, kan brugere ikke integrere PowerApps direkte på siden som en fane, et oversigtspanel eller en panoramasektion. Brugere vil stadig kunne integrere PowerApps via menuknappen PowerApps, hvis integrering er tilladt på siden.  

I følgende eksempel vises en ny klasse med de to metoder, der skal bruges til at konfigurere, hvor PowerApps kan integreres.  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}


