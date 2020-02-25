---
title: Forudsætninger for konfiguration af kanal
description: Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002283"
---
# <a name="channel-setup-prerequisites"></a>Forudsætninger for konfiguration af kanal


[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Før en Dynamics 365 Commerce-kanal kan oprettes, skal der udføres flere nødvendige opgaver. Følgende lister med nødvendige opgaver er organiseret efter kanaltype.

> [!NOTE]
> Der skrives stadig en dokumentation, og links opdateres, efterhånden som der udgives nyt indhold.

## <a name="initialization"></a>Initialisering

- [Initialisere oprindelsesdata](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globale forudsætninger kræves til alle kanaltyper

- [Definere og konfigurere strukturen for den juridiske enhed](channels-legal-entities.md) 
- [Konfigurere dit organisationshierarki](channels-org-hierarchies.md)
- [Konfigurer et lagersted](channels-setup-warehouse.md)
- [Konfigurere moms](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [Konfigurere en mailbeskedprofil](email-notification-profiles.md)
- [Oprette nummerserier](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Oprette en standardkunde og -adressekartotek](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Forudsætninger for detailkanal

- [Infokoder og infokodegrupper](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Oprette en profil for detailfunktionalitet](retail-functionality-profile.md)
- [Oprette et medarbejderadressekartotek](new-address-book.md)
- [Konfigurere et skærmlayout](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Oprette en hardwarestation](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Forudsætninger for callcenter-kanal

- Call center-parametre
- Call center-refusionsmetoder
- Lejetyper
- Betalingstjenester
- Koder for ordrehold

## <a name="online-channel-prerequisites"></a>Forudsætninger for onlinekanal

- [Oprette en onlinefunktionalitetsprofil](online-functionality-profile.md)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Konfigurer organisationshierarkier](channels-org-hierarchies.md)

[Oprette juridiske enheder](channels-legal-entities.md)

[Konfigurer en detailkanal](channel-setup-retail.md)
    
[Konfigurere en onlinekanal](channel-setup-online.md)
