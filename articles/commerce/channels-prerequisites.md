---
title: Forudsætninger for konfiguration af kanal
description: Denne artikel indeholder en oversigt over forudsætninger for konfiguration af kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 98ca2dc4691534853467c1680890199d08bc4e79
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282289"
---
# <a name="channel-setup-prerequisites"></a>Forudsætninger for konfiguration af kanal

[!include [banner](includes/banner.md)]

Denne artikel indeholder en oversigt over forudsætninger for konfiguration af kanal i Microsoft Dynamics 365 Commerce.

Før en Dynamics 365 Commerce-kanal kan oprettes, skal der udføres flere nødvendige opgaver. Følgende lister med nødvendige opgaver er organiseret efter kanaltype.

> [!NOTE]
> Der skrives stadig en dokumentation, og links opdateres, efterhånden som der udgives nyt indhold.

## <a name="initialization"></a>Initialisering

- [Initialisere oprindelsesdata](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globale forudsætninger kræves til alle kanaltyper

- [Definere og konfigurere strukturen for den juridiske enhed](channels-legal-entities.md) 
- [Konfigurere dit organisationshierarki](channels-org-hierarchies.md)
- [Konfigurer et lagersted](channels-setup-warehouse.md)
- [Konfigurere moms](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Konfigurere en mailbeskedprofil](email-notification-profiles.md)
- [Oprette nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Oprette en standardkunde og -adressekartotek](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Forudsætninger for detailkanal

- [Infokoder og infokodegrupper](info-codes-retail.md)
- [Oprette en profil for detailfunktionalitet](retail-functionality-profile.md)
- [Oprette et medarbejderadressekartotek](new-address-book.md)
- [Konfigurere et skærmlayout](pos-screen-layouts.md)
- [Oprette en hardwarestation](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Forudsætninger for callcenter-kanal

- Call center-parametre
- [Callcenter-ordre og refusionsbetalingsmetoder](work-with-payments.md)
- [Callcenterets leveringsmåder og -gebyrer](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Forudsætninger for onlinekanal

- [Oprette en onlinefunktionalitetsprofil](online-functionality-profile.md)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Konfigurer organisationshierarkier](channels-org-hierarchies.md)

[Oprette juridiske enheder](channels-legal-entities.md)

[Konfigurer en detailkanal](channel-setup-retail.md)
    
[Konfigurere en onlinekanal](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
