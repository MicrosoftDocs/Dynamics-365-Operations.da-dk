---
title: "Arbejdsområde til omkostningsstyring på mobilenheder i Microsoft Dynamics 365 for Operations-app"
description: "Med arbejdsområdet til omkostningsstyring på mobilenheder kan ledere af bærere se bærerydeevnen når som helst og hvor som helst."
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

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Arbejdsområde til omkostningsstyring på mobilenheder i Microsoft Dynamics 365 for Operations-app

Med arbejdsområdet til omkostningsstyring på mobilenheder kan ledere af bærere se bærerydeevnen når som helst og hvor som helst. 

<a name="prerequisites"></a>Forudsætninger
-------------

| Forudsætning                                                         | Betegnelse                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Læs om Microsoft Dynamics 365 for Operations-mobilplatformen | [Dynamics 365 for Operations-mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Sørg for, at du bruger et miljø, der har Microsoft Dynamics 365 for Operations version 1611 og opdatering 3 til Microsoft Dynamics for Operations platformen (november 2016). |
| Hotfix KB 3215650                                                    | Installer hotfixet, hvis du vil aktivere de arbejdsområder, der findes i Microsoft Dynamics 365 for Operations.                                                                       |
| Mobileenhed, hvor Dynamics 365 for Operations-appen er installeret | Hent og installer Dynamics 365 for Operations-appen fra din mobilapp-butik.                                                                                                      |

## <a name="introduction"></a>Introduktion
Arbejdsområdet til omkostningsstyring på mobilenheder giver et øjeblikkeligt overblik over den aktuelle ydeevne af bærere ved at sammenligne faktiske omkostninger med de budgetterede omkostninger. Du kan gå ned på detailniveau og se status for individuelle kostelementer.

### <a name="example"></a>Eksempel

En medarbejder modtager en invitation til en international konference. Organisationen skal dække alle rejseudgifter. Medarbejderen spørger sin chef, om han må deltage i konferencen. Chefen åbnes hurtigt arbejdsområde til omkostningsstyring på sin mobiltelefon for at se, om han har budget til, at medarbejderen kan deltage i konferencen.

### <a name="data-security"></a>Datasikkerhed

Dataene i arbejdsområdet til omkostningsstyring er sikret med brugerlegitimationsoplysninger. En bærerleder kan kun se data for egen bærer. Sikkerheden på adgangsniveau administreres i modulet Omkostningsregnskab. Bogholdere definerer konfiguration af arbejdsområdet til omkostningsstyring i modulet Omkostningsregnskab. Når arbejdsområdet er publiceret på Microsoft Dynamics 365 for Operations-appen, er det tilgængeligt i Dynamics 365 for Operations-mobilappen. Dette sikrer, at alle bærerledere i organisationen får vist data i samme format.

### <a name="actions-views-and-links"></a>Handlinger, visninger og links

Arbejdsområdet til omkostningsstyring på mobilenheder til Dynamics 365 for Operations-appen indeholder følgende handlinger, visninger og links:

-   Handlinger 
    -   Vælg **Konfigurationer** for at vælge et layout.
    -   Vælg **Omkostningsobjekter** for at plukke de bærere, som du vil filtrere data. **Bemærk!** Listen vises i henhold til den adgang, der er givet i modulet Omkostningsregnskab.

<!-- -->

-   Baseret på, hvad der er valgt **Handlinger**, og hvad er konfigureret i modulet Omkostningsregnskab, kan du se følgende oplysninger i kortene. Bemærk, at beløbet vises i samme format: Faktisk, Budget, Afvigelse og Afvigelse i %. 
    -   Faktisk vs. budget (aktuel periode)
    -   Faktisk vs. revideret budget (aktuel periode)
    -   Faktisk vs. budget (forrige periode)
    -   Faktisk vs. revideret budget (forrige periode)
    -   Faktisk vs. budget (år til dato)
    -   Faktisk vs. revideret budget (år til dato)

<!-- -->

-   Links
    -   Detaljer for aktuel periode.
    -   Detaljer for forrige periode.
    -   Detaljer for år til dato.

Når du vælger et link, vises et kort pr. omkostningselement. Beløbet i feltet Kort vises i følgende format: faktisk, budget, budgetafvigelse, budgetafvigelse i %, revideret budget, revideret budgetafvigelse og revideret budgetafvigelse i %.  [![cost-controlling](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Introduktion
Følg disse trin for at komme i gang med at bruge din mobilenheds arbejdsområde til omkostningsstyring.

1.  I din mobilappbutik skal du hente og installere Microsoft Dynamics 365 for Operations-appen.
2.  Start appen på din enhed.
3.  Angiv URL-adressen til din Dynamics 365.
4.  Angiv det firma, du vil logge på. Du kan f.eks. skrive **USMF**.
5.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Microsoft Dynamics 365 for Operations-konto. Angiv dine legitimationsoplysninger. Når du har logget på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed.

For at få vist arbejdsområder på din mobilapp skal du først publicere de ønskede arbejdsområder til Dynamics 365 for Operations-appen.

1.  Start Dynamics 365 for Operations.
2.  Gå til **Systemadministration** &gt; **Opsætning** &gt; **systemparametre**.
3.  Vælg **Administrer mobilapp**.
4.  Vælg arbejdsområdet **Omkostningsstyring** for at publicere til mobilplatformen.
5.  Vælg **Publicer arbejdsområde**.
6.  Opdater din enhed for at se de publicerede arbejdsområder.

## <a name="view-the-performance-of-your-cost-center"></a>Få vist ydeevnen for din bærer
1.  På din mobilenhed skal du vælge arbejdsområdet **Omkostningsstyring**.
2.  Vælg **Styring af omkostningsobjekt**.
3.  Klik på **Handlinger**.
4.  Klik på **Vælg variant** for at vælge et omkostningsstyringslayout.
5.  Klik på **Udført**.
6.  Klik på **Handlinger**.
7.  Klik på **Vælg omkostningsobjekt** for at vælge de bærere, som du har fået adgang til.
8.  Klik på **Udført**.
9.  Se den samlede ydeevne for din bærer.
10. Klik på **Detaljer for aktuel periode**.
11. Se ydeevnen for individuelle omkostningselementer.
12. Du kan også søge efter bestemte omkostningselementer.



