---
title: Bekræfte dobbeltskrivningskonfiguration i programmer til finans og drift og Dataverse
description: Denne artikel forklarer, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i programmer til finans og drift og i Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289384"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Bekræfte dobbeltskrivningskonfiguration i programmer til finans og drift og Dataverse

[!include [banner](../../includes/banner.md)]





Denne artikel indeholder fejlfindingsoplysninger for dobbeltskrivning mellem programmer til finans og drift og Dataverse. Der redegøres specifikt for, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i programmer til finans og drift og i Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Bekræfte, at dobbeltskrivning er konfigureret i programmet til finans og drift

Hvis du vil finde ud af, om de fejl, du ser, når du forsøger at gemme rækker til opdatering, kommer fra dobbeltskrivning, skal du først kontrollere, at dobbeltskrivning er konfigureret.

+ Hvis du har administratorrettigheder i programmet til finans og drift, skal du gå til **Arbejdsområder \> Datastyring** og vælge feltet **Dobbeltskrivning**. Hvis detaljerne for de sammenkædede miljøer og listen over tabeltilknytninger, der kører, vises, er dobbeltskrivning konfigureret.

    ![Kontrollere forbindelsen til programmer til finans og drift, når du har administratorrettigheder.](media/verify_fin_ops_1.png)

+ Hvis du ikke har administratorrettigheder, modtager du fejlmeddelelsen *Der kan ikke skrives data til enheden \<entity name\>*. I eksemplet i følgende illustration kan du ikke oprette en kunderække i programmer til finans og drift, fordi dobbeltskrivning er konfigureret, men referencedataene for debitorgruppen og betalingsbetingelser findes ikke i Dataverse.

    ![Kontrollere forbindelsen til programmer til finans og drift, når du ikke har administratorrettigheder.](media/verify_fin_ops_2.png)

Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i programmer til finans og drift, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollere, at dobbeltskrivning er konfigureret i Dataverse

Når du opretter data, og du ser kolonnen **Firma** på siderne i Dataverse, er dobbeltskrivning konfigureret.

![Kontrollere Dataverse-forbindelsen.](media/verify_cds.png)

Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Dataverse, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

Du kan finde oplysninger om, hvordan du kan få vist detaljer om fejl, hvis der opstår fejl, mens du opretter data i Dataverse, under [Aktivere og få vist sporingsloggen for plug-ins i Dataverse for at få vist detaljer om fejl](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
