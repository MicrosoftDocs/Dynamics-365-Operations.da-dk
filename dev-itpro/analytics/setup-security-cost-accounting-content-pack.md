---
title: "Angive sikkerhed for omkostningsregnskab analyse strøm BI-indhold"
description: "Dette emne forklarer, hvordan du kan overføre sikkerhed på brugerniveau i omkostningsregnskabet på rækkeniveau sikkerhed i Microsoft Power BI. Denne funktionalitet hjælper med at sikre, at brugerne får vist kun strøm BI-data, som de får adgang til."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Angive sikkerhed for omkostningsregnskab analyse strøm BI-indhold

Dette emne forklarer, hvordan du kan overføre sikkerhed på brugerniveau i omkostningsregnskabet på rækkeniveau sikkerhed i Microsoft Power BI. Denne funktionalitet hjælper med at sikre, at brugerne får vist kun strøm BI-data, som de får adgang til.

<a name="overview"></a>Overblik
--------

Den **omkostningsregnskab analyse** Microsoft Power BI indhold bruges strøm BI rækkeniveau sikkerhed til at begrænse en brugers adgang. Sikkerhed er baseret på adgangsniveau organisationshierarki, der er angivet i parametrene for omkostningsregnskab. Yderligere oplysninger om den **omkostningsregnskab analyse** Power BI indhold, se [omkostningsregnskab analyse strøm BI indhold](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Konfiguration
Hvis du vil overføre strøm BI-niveau sikkerhed, skal ejeren af indholdet strøm BI følge disse trin. **Bemærk:** den bruger, der udgiver den **omkostningsregnskab analyse** Power BI indhold bliver automatisk ejer. Kun en ejer kan konfigurere sikkerhed i strømforsyning BI. Derudover indtil en ejer tilføjer andre brugere på PowerBI.com, ingen undtagen ejeren kan se nogen data i den **omkostningsregnskab analyse** Power BI-indhold.

1.  Udgive definitionsfilen til strøm BI.
2.  Logge på PowerBI.com.
3.  Find datasæt for den **omkostningsregnskab analyse** Power BI-indhold.
4.  Åbne sikkerhedssiden. 

    [![Åbne sikkerhedssiden](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  Den **omkostninger objekt controller** rolle er allerede oprettet. Føje andre medlemmer, der er en del af omkostningsregnskabet adgangsniveau organisationshierarki. 

    [![Tilføjelse af medlemmer](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Brugere, der føjes til den **omkostninger objekt controller** rolle ser kun de data, de har tilladelse til at se ifølge definitionen i organisationshierarkiet for omkostningsregnskab-adgangsniveau. **Bemærk:** på rækkeniveau sikkerhed gælder for fliser og rapporter i Microsoft Dynamics 365 for operationer, der er integreret fra Power BI.

## <a name="updating-security"></a>Opdatering af sikkerhed
Hvis der foretages opdateringer adgangsniveau sikkerhed i forbindelse med omkostningsregnskab, og du vil strøm BI at afspejle disse opdateringer, skal du opdatere enhed butikken for den **omkostningsregnskab analyse** Power BI-indhold. Når du har afsluttet opdateringen store enhed fra Dynamics 365 for operationer, skal du opdatere artefakter på PowerBI.com. Finde flere oplysninger om, hvordan du gør en enhed store opdatering [opdatering enhed butik](power-bi-integration-entity-store.md#update-entity-store). Ejeren af den **omkostningsregnskab analyse** Power BI indhold skal også gøre en enhed store opdatering, hvis nye brugere får adgang til det organisatoriske hierarki. Ejeren skal desuden føje nye brugere til den **omkostninger objekt controller** rolle på PowerBI.com, så gælder denne rækkeniveau sikkerheden for dem.

## <a name="disabling-security"></a>Deaktivering af sikkerhed
Vi antager, at din organisation ønsker at begrænse adgang til data. Hvis en eller anden grund sikkerhedsparametrene er deaktiveret, når du kører omkostningsregnskab, ejeren skal føje brugere til den **bogholder** rolle i BI strøm i stedet. Hvis du ændrer sikkerhed fra en stat, der er aktiveret til deaktiveret tilstand, er det en god ide at fjerne brugere fra den **omkostninger objekt controller** rolle. Og omvendt, hvis du genaktiverer sikkerhed. Brugere kan tilhøre begge roller. Fælles adgang er at forene begge roller. I tilfælde af den **omkostningsregnskab analyse** Power BI indhold, brugere, der har adgang til fælles har ubegrænset adgang til data. Hvis dit mål er at anvende begrænset adgang, brugerne skal tildeles kun til de **omkostninger objekt controller** rolle. Disse sikkerhedsopdateringer på rækkeniveau træder straks i kraft. Berørte brugere skal opdatere deres browsere.

## <a name="additional-resources"></a>Yderligere ressourcer
Hvis du vil vide mere om Power BI rækkeniveau sikkerhed, se [administrere sikkerhed på din model i Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


