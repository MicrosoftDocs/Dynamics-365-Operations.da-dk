---
title: Kontrollere, at dobbeltskrivning er konfigureret i Finance and Operations-apps og Common Data Service
description: I dette emne forklares det, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finance and Operations-apps og i Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172639"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Kontrollere, at dobbeltskrivning er konfigureret i Finance and Operations-apps og Common Data Service

[!include [banner](../../includes/banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service. Der redegøres specifikt for, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finance and Operations-apps og i Common Data Service.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kontrollere, at dobbeltskrivning er konfigureret i en Finance and Operations-app

Hvis du vil finde ud af, om de fejl, du ser, når du forsøger at gemme poster til opdatering, kommer fra dobbeltskrivning, skal du først kontrollere, at dobbeltskrivning er konfigureret.

+ Hvis du har administratorrettigheder i Finance and Operations-appen, skal du gå til **Arbejdsområder \> Datastyring** og vælge feltet **Dobbeltskrivning**. Hvis detaljerne for de sammenkædede miljøer og listen over enhedstilknytninger, der kører, vises, er dobbeltskrivning konfigureret.

    ![Kontrollere Finance and Operations-appforbindelsen, når du har administratorrettigheder](media/verify_fin_ops_1.png)

+ Hvis du ikke har administratorrettigheder, modtager du fejlmeddelelsen *Der kan ikke skrives data til enheden \<enhedsnavn\>*. I eksemplet i følgende illustration kan du ikke oprette en kundepost i Finance and Operations-appen, fordi dobbeltskrivning er konfigureret, men referencedataene for debitorgruppen og betalingsbetingelser findes ikke i Common Data Service.

    ![Kontrollere Finance and Operations-appforbindelsen, når du ikke har administratorrettigheder](media/verify_fin_ops_2.png)

Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Finance and Operations-apps, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Kontrollere, at dobbeltskrivning er konfigureret i Common Data Service

Når du opretter data, og du ser feltet **Firma** på siderne i Common Data Service, er dobbeltskrivning konfigureret.

![Kontrollere Common Data Service-forbindelsen](media/verify_cds.png)

Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Common Data Service, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

Du kan finde oplysninger om, hvordan du kan få vist detaljer om fejl, hvis der opstår fejl, mens du opretter data i Common Data Service, under [Aktivere og få vist sporingsloggen for plug-ins i Common Data Service for at få vist detaljer om fejl](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
