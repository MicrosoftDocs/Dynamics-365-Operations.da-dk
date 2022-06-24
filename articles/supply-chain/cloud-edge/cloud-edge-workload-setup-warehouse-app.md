---
title: Konfigurere mobilappen Warehouse Management til sky- og edge-skaleringsenheder
description: Denne artikel forklarer, hvordan du kan konfigurere dine Warehouse Management-mobilapps for lagersteder, der serviceres af en sky- eller edge-skalaenhed.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865232"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Konfigurere mobilappen Warehouse Management til sky- og edge-skaleringsenheder

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan konfigurere dine Warehouse Management-mobilapps, så de kan bruges i lagersteder, der serviceres af en sky- eller edge-skalaenhed.

## <a name="prerequisites"></a>Forudsætninger

Før du begynder at konfigurere dine mobilenheder til at oprette forbindelse til en sky- eller edge-skalaenhed, skal du bekræfte, at de kan oprette forbindelse til virksomhedshubben. Du kan finde vejledning under [Installere og tilslutte mobilappen Warehouse Management](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Yderligere opsætning, når du kører mobilappen Warehouse Management ud fra en skalaenhed

Som en del af [implementeringsprocessen for arbejdsbyrder til lagerstedsskalaenheder](cloud-edge-landing-page.md#scale-unit-manager-portal) synkroniseres de fleste af de data, der kræves for at forbinde dine enheder med mobilappen Warehouse Management, automatisk fra virksomhedshubben til skalaenheden. Du skal dog angive dataene på siden med **Azure Active Directory-programmer** (**Systemadministration \> Konfiguration \> Azure Active Directory-programmer**) på installationen af skaleringsenhed. Derudover skal du muligvis opdatere standardværdien af **Firma** for bruger-id'et eller oprette en ny bruger. Brugere, der er tilknyttet et firma, som ikke findes i implementering af en skalaenhed, kan ikke logge på, når en mobilappen Warehouse Management er tilknyttet denne skalaenhed.

> [!NOTE]
> Da dataene på siden **Azure Active Directory-programmer** ikke er synkroniseret, skal du vedligeholde disse data manuelt, hvis du vil flytte lagerstedsbelastningen til en anden skalaenhed.

Husk på, at som en del af forbindelsesopsætningen af hver enkelt Warehouse Management-mobilapp skal den angivne Azure Active Directory-ressources URL-adresse være for skalaenheden i stedet for virksomhedshubben.
