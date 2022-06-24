---
title: Konfigurere et eksperiment
description: Denne artikel beskriver, hvordan du konfigurerer et eksperiment i en tredjepartstjeneste.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946160"
---
# <a name="set-up-an-experiment"></a>Konfigurere et eksperiment

Når du [definerer en hypotese og bestemmer, hvilke succesmålepunkter du vil bruge](experimentation-identify.md), skal du konfigurere dit eksperiment i tredjepartstjenesten. I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce. Yderligere trin behandles i separate artikler.

[ ![Eksperimenteringens brugerrejse - konfiguration.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Konfigurere dit eksperiment i tredjepartstjenesten
Nu skulle du have valgt en tredjepartstjeneste til at køre og overvåge dit eksperiment, så du kan konfigurere eksperimenteren-connectoren. Disse forudsætninger er angivet i [Eksperimenteren i Dynamics 365 Commerce](experimentation-overview.md).

Følg de trin, der er nødvendige for at oprette dit eksperiment i tredjepartstjenesten. Hvis connectoren er konfigureret korrekt, vil den fuldstændige liste over de eksperimenter, du konfigurerer i tredjepartstjenesten, blive synlig i Commerce-webstedsgeneratoren inden for 5 minutter.

## <a name="set-up-your-success-metrics"></a>Konfigurere succesmålepunkter
Alle eksperimenter skal bruge målepunkter til måling af variationernes effekt og for at validere hypotesen. Benyt følgende fremgangsmåde for at aktivere beregning af målepunkter i tredjepartstjenesten ved hjælp af hændelser med live telemetri fra Dynamics 365 Commerce.

Benyt følgende fremgangsmåde for at konfigurere dine succesværdier for moduler, der ikke er i boksen.

1. I Commerce-webstedsgeneratoren skal du vælge **Sider** i venstre navigationsrude og derefter vælge den side, du vil indsamle målepunkter for. 
1. Gå til sektionen **Hændelses-id'er, der skal spores** i egenskabsruden til højre for den side eller det modul, du vil spore.
1. Vælg **Vis**. Der vises en liste over alle kllik-hændelses-id'er. Kopiér den hændelse, du vil spore, og indsæt hændelsesnøglen på den angivne placering i tredjepartstjenesten. Hvis du skal bruge mere end én hændelse, skal du kopiere nøglerne én ad gangen. 
1. I forbindelse med sidevisninger kan SHA-256 den nummerlisteværdi for sidenavnet i Site builder, du har føjet til `.PageView`. Hændelses-id'et for `Homepage.PageView` kunne f.eks. være `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Udfør andre trin for at spore de påkrævede målepunkter i tredjepartstjenesten.

Ved brugerdefinerede modulklik skal du benytte følgende fremgangsmåde for at instrumentet til klikhændelser:

1. Forbered et **TelemetryContent**-objekt for modulet ved hjælp af funktionen nedenfor. Denne funktion bruger sidenavnet, modulnavnet og standard telemetryobjektet SDK som input.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Følgende er et eksempel: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Opret de nyttelastdata, der indeholder oplysninger om, hvad der skal registreres. For knapper og andre statiske kontroller kan du inkludere **etext**, f.eks. "Shop nu" eller "Søg". Og for komponenter med klik, f.eks. klik på et produktkort, kan du sende den **recid**, som er post-id'et for produktet eller produkt-id'et.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Som eksempel på statiske kontroller skal tekststrengen for knappen bestås som vist herunder:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Som et eksempel på produktklik skal produkt RecordID bestås som vist nedenfor:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Ringer til funktionen **OnClick** for at registrere hændelsen.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Følgende er et eksempel:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Forrige trin
[Identificere en hypotese og fastslå målepunkter for et eksperiment](experimentation-identify.md) 


## <a name="next-step"></a>Næste trin
[Tilslutte og redigere et eksperiment](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
