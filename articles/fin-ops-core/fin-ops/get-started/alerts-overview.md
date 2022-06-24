---
title: Oversigt over påmindelser (indeholder video)
description: Denne artikel indeholder generelle oplysninger om påmindelser. Du kan bruge påmindelser til at holde dig orienteret om de hændelser, du vil holde styr på i løbet af arbejdsdagen.
author: RichdiMSFT
ms.date: 09/04/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 4b63ac8a09efb9ab449b651d030bd14a24d5cc36
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850058"
---
# <a name="alerts-overview"></a>Oversigt over påmindelser

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Om påmindelser
Påmindelser udgør et beskedsystem for kritiske hændelser i systemet. Du kan bruge påmindelser til at holde dig orienteret om de hændelser, du vil holde styr på i løbet af arbejdsdagen. Du kan nemt oprette dit eget sæt påmindelsesregler, så du bliver påmindet om forfaldne leveringer, slettede ordrer, ændrede priser eller andre hændelser, du skal reagere på.

I ressourceplanlægning (ERP) er der flere typiske scenarier, hvor påmindelsesfunktionen kan bruges. Her er nogle eksempler.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Scenarie 1: Opret en påmindelsesregel for nye salgsordrer

1. Åbn siden **Alle salgsordrer**.
2. I handlingsruden under fanen **Indstillinger** i gruppen **Del** skal du vælge **Opret en brugerdefineret påmindelse**.
3. I dialogboksen **Opret påmindelsesregel** under oversigtspanelet **Vis påmindelse, når** i feltet **Hændelse** skal du vælge **Posten er oprettet**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Scenarie 2: Opret en påmindelsesregel for udskydning af en leveringsdato

1. Åbn siden **Alle indkøbsordrer**.
2. Vælg en indkøbsordre-id for at få adgang til oplysningerne i indkøbsordren.
3. Udvid oversigtspanelet **Indkøbsordrehoved**.
4. I handlingsruden under fanen **Indstillinger** i gruppen **Del** skal du vælge **Opret en brugerdefineret påmindelse**.
5. I dialogboksen **Opret påmindelsesregel** under oversigtspanelet **Vis påmindelse, når** i feltet **Felt** skal du vælge **Leveringsdato**.
6. I feltet **Hændelse** skal du vælge **er udsat**.
    
Når du lukker dialogboksen **Opret påmindelsesregel**, vises reglen på siden **Administrer regler for påmindelser**. Du kan bruge siden **Administrer regler for påmindelser** til at opdatere de eksisterende påmindelsesregler. Du kan f.eks. ændre hændelsesudløsere, opdatere hændelsesmeddelelser og opdatere udløbsdatoer. Hvis du vil åbne siden **Administrer regler for påmindelser**, skal du bruge knappen **Påmind mig** under fanen **Indstillinger** i handlingsruden.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Hvad sker der, når der oprettes en påmindelse?

Når du opretter påmindelsesregler, kan du knytte en foruddefineret hændelse til et bestemt felt. For eksempel, når den dato, der er angivet i feltet bliver nået, eller når indholdet af feltet ændres. Du kan også knytte en hændelse til poster på en bestemt side. For eksempel, når en post oprettes, eller når en post slettes.

Når den valgte hændelse indtræffer for feltet eller en post på siden, får du tilsendt en påmindelse. Du opretter f.eks. en regel, hvor du knytter feltet **Leveringsdato** til en bestemt indkøbsordrelinje med hændelsen **forfald for så længe siden, som angivet her**. Du kan angive tidsintervallet til fem dage. I dette eksempel sendes en påmindelse fem dage efter leveringsdatoen for den pågældende indkøbsordrelinje.

Du kan desuden forfine påmindelsesregler ved at angive betingelser. Du kan for eksempel blive påmindet om nye indkøbsordrer, der oprettes for bestemt kreditorkonti.

## <a name="preparing-for-an-alert"></a>Forberede til en påmindelse

Før du opretter en påmindelsesregel, skal du beslutte, hvornår og i hvilke situationer du vil modtage påmindelser. Når du ved, hvilke hændelser du vil have besked om, skal du finde den side, hvor de data vises, der udløser den pågældende hændelse. Hændelsen kan være en dato, der bliver nået, eller en bestemt ændring, der opstår. Derfor skal du finde den side, hvor datoen er angivet, eller hvor det felt, der ændres, eller posten, der oprettes, bliver vist. Når du har disse oplysninger, kan du oprette påmindelsesreglen.

## <a name="components-of-an-alert-rule"></a>Komponenter i en påmindelsesregel

En påmindelsesregel har fem komponenter

- **Hændelse** – Den hændelse, der udløser en påmindelsesregel, kan være en dato eller en bestemt ændring, der opstår. Du kan definere hændelser i oversigtspanelet **Send e-mail-påmindelser, når jobstatus ændres** i dialogboksen **Opret påmindelsesregel**.
- **Betingelse** – I oversigtspanelet **Påmind mig i** i dialogboksen **Opret påmindelsesregel** kan du vælge omfanget af betingelsen for at styre, hvornår du bliver påmindet om hændelser. Du kan anvende reglen enten kun på den aktuelle post eller på alle de poster, der er synlige på siden. Hvis reglen gælder på tværs af juridiske enheder, kan du angive indstillingen **Globalt** til **Ja**.
- **Reglens udløb** – I oversigtspanelet **Påmind mig indtil** i dialogboksen **Opret påmindelsesregel** kan du angive, hvor længe påmindelsesreglen skal være aktiv.
- **Indhold** – I oversigtspanelet **Vis påmindelse med** i dialogboksen **Opret påmindelsesregel** kan du angive den emnetekst og meddelelsestekst, der skal bruges i advarselsmeddelelserne.
- **Bruger** – I oversigtspanelet **Hvem skal påmindes** i dialogboksen **Opret påmindelsesregel** kan du angive, hvilken bruger der skal modtage påmindelserne. Dit bruger-ID er som standard markeret.

    > [!NOTE]
    > Denne indstilling er begrænset til administratorer i organisationen.

## <a name="videos"></a>Videoer

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>Sådan bruges påmindelser til at overvåge filtrerede data

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

Videoen [Sådan bruges påmindelser til at overvåge filtrerede data](https://youtu.be/ZYKMcv6kl9s) (vises ovenfor) er inkluderet på [Finans- og driftsafspilningslisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), som er tilgængelig på YouTube.

### <a name="alert-rule-options"></a>Indstillinger for påmindelsesregel

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

Videoen [Indstillinger for påmindelsesregel](https://youtu.be/cpzimwOjicM) (vist ovenfor) er inkluderet på [Finans- og driftsafspilningslisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), som er tilgængelig på YouTube.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]