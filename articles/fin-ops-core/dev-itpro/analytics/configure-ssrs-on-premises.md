---
title: Konfigurere SQL Server Reporting Services for lokal installationer
description: Denne artikel indeholder oplysninger om konfiguration af SQL Server Reporting Services (SSRS) for en lokal installation.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: ae1e78a268d6c61cc4ab6afd9e3f6d6b1bd1561a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876915"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>Konfigurere SQL Server Reporting Services for lokal installationer

[!include [banner](../includes/banner.md)]

Brug trinnene i denne artikel til at konfigurere SQL Server Reporting Services (SSRS) til din Microsoft Dynamics 365 Finance + Operations (on-premises)-installation.

1. Åbn programmet Konfigurationsstyring til Reporting Services.
2. Lad standard **Servernavn** stå, som bør være navnet på den aktuelle computer, og **Rapportserverforekomst**, **MSSQLSERVER**.
3. Klik på **Tilknyt**.

    [![Reporting Services-konfigurationsforbindelse.](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Klik på fanen **Tjenestekonto**, og kontroller, at indstillingerne svarer til følgende illustration.

    [![Fanen Tjenestekonto.](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Klik på fanen **URL-adresse til webtjeneste**, og kontroller, at indstillingerne svarer til følgende illustration.

    [![Fanen URL-nøgle til webtjeneste.](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Klik på fanen **Database**, og kontroller, at den **Databasenavn** og **Indstillinger for legitimationsoplysninger** svarer til følgende grafik.

    > [!NOTE]
    > Du skal oprette en ny database. Det gør du ved at klikke på **Skift database** og derefter kontrollere, at det nye databasenavn er: **DynamicsAxReportServer**.

    [![fanen database.](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Klik på fanen **URL-adresse til webportal**, og kontroller, at indstillingerne svarer til følgende illustration.

    > [!NOTE]
    > Du skal klikke på **Anvend** for at oprette og konfigurere portalen korrekt.

    [![fanen URL-adresse til webportal.](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Når portalen er konfigureret, svarer fanen **Webportal** til følgende illustration.

    [![fanen webportal.](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Klik på URL-adressen til rapporter for at se SQL Server Reporting Services-webportalen.
9. Når du er på portalen, kan du oprette en ny mappe med navnet **Dynamics**.

    [![dynamics-mappe.](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. I **Konfigurationsstyring til Reporting Services** skal du klikke på fanen **Mailindstillinger** og kontrollere, at indstillingerne svarer til følgende illustration.

    [![fanen mailindstillinger.](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Klik på fanen **Udførelseskonto**, og kontroller, at indstillingerne svarer til følgende illustration.

    [![fanen udførelseskonto.](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Du skal ikke ændre standardindstillingerne under fanen **Krypteringsnøgler**.

    [![fanen krypteringsnøgler.](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Klik på fanen **Abonnementsindstillinger**, og kontroller, at indstillingerne svarer til følgende illustration.

    [![fanen abonnementsindstillinger.](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Du skal ikke ændre standardindstillingerne under fanen **Udvidet installation**.

    [![fanen udvidet installation.](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Du skal ikke ændre standardindstillingerne under fanen **Power BI-integration**.

    [![fanen power bi-integration.](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Klik på **Afslut** for at lukke **Konfigurationsstyring til Reporting Services**.

    [![konfigurationsstyring til reporting services.](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
