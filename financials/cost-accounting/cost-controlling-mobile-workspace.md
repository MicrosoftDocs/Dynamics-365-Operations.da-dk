---
title: "Omkostning styrende mobile arbejdsområde for Microsoft Dynamics 365 for operationer app"
description: "Med omkostningerne kan styring af mobile arbejdsområde, omkostninger center ledere se center omkostningspræstationer når som helst og hvor som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Omkostning styrende mobile arbejdsområde for Microsoft Dynamics 365 for operationer app

Med omkostningerne kan styring af mobile arbejdsområde, omkostninger center ledere se center omkostningspræstationer når som helst og hvor som helst. 

<a name="prerequisites"></a>Forudsætninger
-------------

| Forudsætning                                                         | Betegnelse                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Læs om Microsoft Dynamics-365 for operationer mobilplatform | [Dynamics 365 for operationer mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 til operationer                                          | Sørg for, at du bruger et miljø, hvor Microsoft Dynamics 365 for operationer version 1611 opdager og Microsoft Dynamics for operationer platform update 3 (November 2016). |
| Hotfix KB 3215650                                                    | Installere hotfixet, hvis du vil aktivere de arbejdsområder, der findes i Microsoft Dynamics 365 for operationer.                                                                       |
| Mobile enhed, der har den Dynamics 365 for operationer app installeret | Hent den Dynamics 365 for operationer app fra din mobile app butik.                                                                                                      |

## <a name="introduction"></a>Introduktion
De omkostninger, der styrer mobile arbejdsområde giver et øjeblikkeligt overblik over den aktuelle ydeevne af bærere ved at sammenligne faktiske omkostninger med de budgetterede omkostninger. Du kan finde frem til status for individuelle kostelementer.

### <a name="example"></a>Eksempel

En medarbejder modtager en invitation til en international konference. Organisationen har til dækning af rejseudgifter. Medarbejderen spørger hans Manager, hvis han kan deltage i konferencen. Manager åbnes hurtigt omkostningerne styring af mobile arbejdsområde på sin mobiltelefon til at se, om han har budget for medarbejderen til at deltage i konferencen.

### <a name="data-security"></a>Datasikkerhed

Dataene i de omkostninger, der styrer arbejdsområde er sikret med brugerlegitimationsoplysninger. En omkostning center manager er kun tilladt at se data for eget bærer. Sikkerheden på access er administreret i modulet Omkostningsregnskab. Omkostninger revisorer definere omkostningen styre konfiguration af mobile arbejdsområde i modulet Omkostningsregnskab. Når arbejdsområdet er udgivet på Microsoft Dynamics 365 for operationer app, er tilgængelige i Dynamics-365 for operationer mobile app. Dette sikrer, at alle omkostninger center ledere i organisationen se data i samme format.

### <a name="actions-views-and-links"></a>Handlinger, visninger og links

De omkostninger, der styrer mobile arbejdsområde for Dynamics 365 for operationer app giver følgende handlinger, visninger og links:

-   Handlinger 
    -   Vælg **konfigurationer** til at vælge et layout.
    -   Vælg **omkostningsobjekter** til at plukke omkostningssteder, som du vil filtrere data. **Bemærk:** listen vises i henhold til den adgang, der er givet i modulet Omkostningsregnskab.

<!-- -->

-   Baseret på, hvad der er valgt **handlinger** og hvad er konfigureret i modulet Omkostningsregnskab, kan du se følgende oplysninger i kortene. Bemærk, at beløbet vises i samme format: faktisk, Budget, afvigelsen og afvigelsen %. 
    -   Faktisk vs. Budget (aktuelle periode)
    -   Faktisk vs. budget for opdateret (aktuelle periode)
    -   Faktisk vs. Budget (forrige periode)
    -   Faktisk vs. budget for opdateret (forrige periode)
    -   Faktisk vs. Budget (år til dato)
    -   Faktisk vs. budget for opdateret (år til dato)

<!-- -->

-   Links
    -   Detaljer for den aktuelle periode.
    -   Detaljer for forrige periode.
    -   Detaljer for år til dato.

Når du vælger et af links, vises et kort pr. omkostningselement. Beløbet i feltet kort vises i følgende format: faktisk, Budget, Budget afvigelse, Afvigelsespct Budget, opdateret budget, opdateret budget afvigelse og opdateret budget afvigelse i %.  [![styring af omkostninger](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Introduktion
Følg disse trin for at komme i gang ved hjælp af omkostningen kontrol mobil-app'en på din mobilenhed.

1.  Din mobile app store, Hent og Installer Microsoft Dynamics-365 for operationer app.
2.  Du kan starte programmet på din enhed.
3.  Angiv URL-adressen for din Dynamics 365.
4.  Angiv firma til at logge på. F.eks. **USMF**.
5.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Microsoft Dynamics-365 for operationer konto. Angiv dine legitimationsoplysninger. Når du logger på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed.

For at få vist arbejdsområder på din mobile app, skal du først udgive de ønskede arbejdsområder til Dynamics-365 for operationer app.

1.  Start Dynamics 365 for operationer.
2.  Gå til **systemadministration**&gt;**Setup**&gt;**systemparametre**.
3.  Vælg **Manage mobile app**.
4.  Vælg arbejdsområdet ** omkostninger styre ** til at udgive til mobil platform.
5.  Vælg **udgive arbejdsområde**.
6.  Opdater din enhed for at se de udgivne arbejdsområder.

## <a name="view-the-performance-of-your-cost-center"></a>Få vist ydeevnen for dit bærer
1.  På din mobilenhed, skal du vælge den **omkostninger, styring af** arbejdsområde.
2.  Vælg **omkostninger, styring af objektet**.
3.  Klik på **handlinger**.
4.  Klik på **Select configuration** til at vælge en omkostning, styre layout.
5.  Click **Done**.
6.  Klik på **handlinger**.
7.  Klik på **Vælg omkostningsobjekt** til at vælge de omkostningssteder, som du har fået adgang.
8.  Click **Done**.
9.  Få vist den generelle ydeevne af din bærer.
10. Klik på **detaljer for den aktuelle periode**.
11. Få vist ydeevnen for individuelle kostelementer.
12. Du kan også søge efter bestemte omkostningselementer.



