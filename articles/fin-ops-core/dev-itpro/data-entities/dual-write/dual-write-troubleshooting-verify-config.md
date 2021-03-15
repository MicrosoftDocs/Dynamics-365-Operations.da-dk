---
title: Kontrollere konfiguration af dobbeltskrivning i Finance and Operations-apps og Dataverse
description: I dette emne forklares det, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finance and Operations-apps og i Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 361d6555b60e02832c337b6f416b2b3627b6d365
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129301"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Kontrollere konfiguration af dobbeltskrivning i Finance and Operations-apps og Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse. Der redegøres specifikt for, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finance and Operations-apps og i Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kontrollere, at dobbeltskrivning er konfigureret i en Finance and Operations-app

Hvis du vil finde ud af, om de fejl, du ser, når du forsøger at gemme rækker til opdatering, kommer fra dobbeltskrivning, skal du først kontrollere, at dobbeltskrivning er konfigureret.

+ Hvis du har administratorrettigheder i Finance and Operations-appen, skal du gå til **Arbejdsområder \> Datastyring** og vælge feltet **Dobbeltskrivning**. Hvis detaljerne for de sammenkædede miljøer og listen over tabeltilknytninger, der kører, vises, er dobbeltskrivning konfigureret.

    ![Kontrollere Finance and Operations-appforbindelsen, når du har administratorrettigheder](media/verify_fin_ops_1.png)

+ Hvis du ikke har administratorrettigheder, modtager du fejlmeddelelsen *Der kan ikke skrives data til enheden \<entity name\>*. I eksemplet i følgende illustration kan du ikke oprette en kunderække i Finance and Operations-appen, fordi dobbeltskrivning er konfigureret, men referencedataene for debitorgruppen og betalingsbetingelser findes ikke i Dataverse.

    ![Kontrollere Finance and Operations-appforbindelsen, når du ikke har administratorrettigheder](media/verify_fin_ops_2.png)

Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Finance and Operations-apps, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollere, at dobbeltskrivning er konfigureret i Dataverse

Når du opretter data, og du ser kolonnen **Firma** på siderne i Dataverse, er dobbeltskrivning konfigureret.

![Kontrollere Dataverse-forbindelsen](media/verify_cds.png)

Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Dataverse, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

Du kan finde oplysninger om, hvordan du kan få vist detaljer om fejl, hvis der opstår fejl, mens du opretter data i Dataverse, under [Aktivere og få vist sporingsloggen for plug-ins i Dataverse for at få vist detaljer om fejl](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]