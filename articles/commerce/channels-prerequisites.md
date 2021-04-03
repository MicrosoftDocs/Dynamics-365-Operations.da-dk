---
title: Forudsætninger for konfiguration af kanal
description: Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477918"
---
# <a name="channel-setup-prerequisites"></a>Forudsætninger for konfiguration af kanal

[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanal i Microsoft Dynamics 365 Commerce.

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
