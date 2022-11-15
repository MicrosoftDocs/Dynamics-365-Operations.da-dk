---
title: Kendte problemer med Dynamics 365 Human Resources-infrastrukturfletning
description: Denne artikel viser de problemer, der kan opstå under fletningen af Microsoft Dynamics 365 Human Resources-infrastruktur.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752684"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Kendte problemer med Dynamics 365 Human Resources-infrastrukturfletning

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Delte Dataverse-miljøer

Dobbeltskrivningsstrukturen understøtter ikke sammenkædning af to økonomi- og driftsappmiljøer med det samme Dataverse-miljø. Hvis du har et Dataverse-miljø, der deles med begge følgende elementer, skal du enten duplikere Dataverse-miljøet eller opdele det:

- Et program til finans og drift
- Et aktuelt Human Resources-miljø

## <a name="environment-type-requirements"></a>Krav til miljøtype

Følgende miljøtyper er obligatoriske, før du kan udføre overførslen:

- Hvis du ikke har nogen enkeltstående sandkassemiljøer, skal du oprette ét for at validere overførslen.
- Hvis du har flere enkeltstående produktionsmiljøer, kan et af dem overføres. Kontakt Microsoft Support for markere de andre miljøer som sandkasser.

## <a name="teams-integration"></a>Teams-integration

Den eksisterende Human Resources-app i Teams er i øjeblikket ved at blive flyttet til en Microsoft Power Platform-løsning. Yderligere oplysninger finder du i [Human Resources-appen i Teams](hr-admin-teams-leave-app.md).

