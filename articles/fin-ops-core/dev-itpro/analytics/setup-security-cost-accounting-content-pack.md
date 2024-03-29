---
title: Konfigurere sikkerhed for Power BI-indhold til analyse af omkostningsregnskab
description: Denne artikel forklarer, hvordan du kan overføre sikkerheden på adgangsniveau i omkostningsregnskabet til sikkerhed på rækkeniveau i Microsoft Power BI.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.openlocfilehash: 9f019bec9c28602e31b43a8b3ab820f4a3a31ee8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267926"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Konfigurere sikkerhed for Power BI-indhold til analyse af omkostningsregnskab

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan overføre sikkerheden på adgangsniveau i omkostningsregnskabet til sikkerhed på rækkeniveau i Microsoft Power BI. Denne funktionalitet hjælper med til at sikre, at brugerne kun får vist de Power BI-data, de er tildelt adgang til.

## <a name="overview"></a>Overblik

Til **omkostningsregnskabsanalysen** af Microsoft Power BI-indhold bruges sikkerhed på Power BI-rækkeniveau til at begrænse en brugers adgang. Sikkerheden er baseret på det organisationshierarki for adgangsniveau, der er angivet i parametrene for omkostningsregnskab. Du kan finde yderligere oplysninger om **omkostningsregnskabsanalysen** af Power BI-indhold i [Omkostningsregnskabsanalyse af Power BI-indhold](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Konfiguration
Hvis du vil overføre sikkerhed på adgangsniveau til Power BI, skal ejeren af Power BI-indholdet følge disse trin.

> [!NOTE]
> Den bruger, der udgiver **Omkostningsregnskabsanalyse** af Power BI-indhold, bliver automatisk ejer. Kun en ejer kan konfigurere sikkerhed i Power BI. Indtil en ejer tilføjer andre brugere på PowerBI.com, kan ingen undtagen ejeren desuden se nogen data i **omkostningsregnskabsanalysen** af Power BI-indhold.

1. Udgiv definitionsfilen til Power BI.
2. Log på PowerBI.com.
3. Find datasættet til **omkostningsregnskabsanalysen** af Power BI-indhold.
4. Åbn sikkerhedssiden.

    ![Åbning af sikkerhedssiden.](./media/CA-picture-1.png)

5. Rollen **Controller til omkostningsobjekt** er allerede oprettet. Tilføj andre medlemmer, der er en del af organisationshierarkiet for adgangsniveau for omkostningsregnskabet.

    ![Tilføjelse af medlemmer.](./media/CA-picture-2.png)

Brugere, der føjes til rollen **Controller til omkostningsobjekt** ser kun de data, de har tilladelse til at se ifølge definitionen i organisationshierarkiet for adgangsniveau for omkostningsregnskabet.

> [!NOTE]
> Sikkerheden på rækkeniveau gælder for felter og rapporter, der er integreret fra Power BI.

## <a name="updating-security"></a>Opdatering af sikkerhed
Hvis der foretages opdateringer af sikkerheden på adgangsniveau i omkostningsregnskab, og du ønsker, at Power BI skal afspejle disse opdateringer, skal du opdatere enhedslageret for **omkostningsregnskabsanalysen** af Power BI-indhold. Når du har afsluttet opdateringen af enhedslageret, skal du opdatere artefakterne på PowerBI.com. Du kan finde flere oplysninger om, hvordan du foretager en opdatering af enhedslager, i [Power BI-integration med enhedslager](power-bi-integration-entity-store.md#update-entity-store). Ejeren af **omkostningsregnskabsanalysen** af Power BI-indhold skal også foretage en opdatering af enhedslager, hvis nye brugere får adgang til det organisatoriske hierarki. Ejeren skal desuden føje nye brugere til rollen **Controller til omkostningsobjekt** på PowerBI.com, så sikkerhed på rækkeniveau gælder for dem.

## <a name="disabling-security"></a>Deaktivering af sikkerhed
Vi antager, at din organisation ønsker at begrænse adgang til data. Hvis sikkerhedsparametrene af en eller anden grund er deaktiveret, når du kører omkostningsregnskab, skal ejeren i stedet føje brugere til rollen **Bogholder** i Power BI. Hvis du ændrer sikkerhed fra en aktiveret tilstand til en deaktiveret tilstand, er det en god ide at fjerne brugere fra rollen **Controller til omkostningsobjekt**. Og omvendt, hvis du genaktiverer sikkerhed. Brugere kan tilhøre begge roller. Fælles adgang er foreningsmængden af begge roller. Når det gælder **omkostningsregnskabsanalysen** af Power BI- indhold, har brugerne med fælles adgang ubegrænset adgang til data. Hvis dit mål er at anvende begrænset adgang, skal brugerne kun tildeles rollen **Controller til omkostningsobjekt**. Disse opdateringer af sikkerhed på rækkeniveau træder straks i kraft. Berørte brugere skal opdatere deres browsere.

## <a name="additional-resources"></a>Yderligere ressourcer
Du kan få mere at vide om sikkerhed på rækkeniveau i Power BI i [Administrer sikkerhed på din model i Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
