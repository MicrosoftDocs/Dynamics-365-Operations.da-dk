---
title: Bekræfte dobbeltskrivningskonfiguration i programmer til finans og drift og Dataverse
description: Denne artikel forklarer, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finans- og driftsapps og i Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7131e6c2c4ca4d9c6bb84ad74bf425faf28bd92c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884453"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Bekræfte dobbeltskrivningskonfiguration i programmer til finans og drift og Dataverse

[!include [banner](../../includes/banner.md)]





Denne artikel indeholder fejlfindingsoplysninger for dobbeltskrivning mellem Finans- og driftsapps og Dataverse. Der redegøres specifikt for, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finans- og driftsapps og i Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Bekræfte, at dobbeltskrivning er konfigureret i Finans- og driftsapps

Hvis du vil finde ud af, om de fejl, du ser, når du forsøger at gemme rækker til opdatering, kommer fra dobbeltskrivning, skal du først kontrollere, at dobbeltskrivning er konfigureret.

+ Hvis du har administratorrettigheder i Finans- og driftsapps, skal du gå til **Arbejdsområder \> Datastyring** og vælge feltet **Dobbeltskrivning**. Hvis detaljerne for de sammenkædede miljøer og listen over tabeltilknytninger, der kører, vises, er dobbeltskrivning konfigureret.

    ![Kontrollere forbindelsen til Finans- og driftsapps, når du har administratorrettigheder.](media/verify_fin_ops_1.png)

+ Hvis du ikke har administratorrettigheder, modtager du fejlmeddelelsen *Der kan ikke skrives data til enheden \<entity name\>*. I eksemplet i følgende illustration kan du ikke oprette en kunderække i Finans- og driftsapps, fordi dobbeltskrivning er konfigureret, men referencedataene for debitorgruppen og betalingsbetingelser findes ikke i Dataverse.

    ![Kontrollere forbindelsen til Finans- og driftsapps, når du ikke har administratorrettigheder.](media/verify_fin_ops_2.png)

Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Finans- og driftsapps, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollere, at dobbeltskrivning er konfigureret i Dataverse

Når du opretter data, og du ser kolonnen **Firma** på siderne i Dataverse, er dobbeltskrivning konfigureret.

![Kontrollere Dataverse-forbindelsen.](media/verify_cds.png)

Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Dataverse, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

Du kan finde oplysninger om, hvordan du kan få vist detaljer om fejl, hvis der opstår fejl, mens du opretter data i Dataverse, under [Aktivere og få vist sporingsloggen for plug-ins i Dataverse for at få vist detaljer om fejl](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]