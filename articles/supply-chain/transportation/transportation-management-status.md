---
title: Statusser for transportstyring
description: I dette emne forklares, hvordan du kan oprette en transportstatus og knytte den pågældende status til en fragtmands status.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425091"
---
# <a name="transportation-management-statuses"></a>Statusser for transportstyring

[!include [banner](../includes/banner.md)]

Konfigurer masterkoder for transportstatusser for at fortolke koder, der er leveret af dine fragtmænd. På denne måde kan du integrere med fragtmænd for at angive status. Den transportstatus, som du angiver for en transportmasterstatuskode, kan hjælpe dig med at spore statussen for en last, forsendelse eller container. Den specifikke transportstatus for en last, forsendelse eller container kan kun opdateres via dataintegration og ikke manuelt via brugergrænsefladen.

## <a name="create-a-transportation-status"></a>Oprette en transportstatus

Følg disse trin for at oprette en transportstatus:

1. Gå til **Transportstyring \> Opsætning \> Master for transportstatus**.
1. Vælg **Ny** for at oprette en transportstatusmaster.
1. Angiv en entydig kode for transportstatussen i feltet **Master for transportstatus**.
1. Vælg enten *Fragtmand* eller *Hub* som transporttype i feltet **Transporttype**.
1. Angiv et navn og en transportstatus.
1. Luk siden.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Knytte en transportstatus til en fragtmands status

Hvis du vil knytte en transportstatus til en fragtmands status, skal du følge disse trin:

1. Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Transportstatus for fragtmand**.
1. Vælg **Ny** for at knytte en kode fra en fragtmand til en transportstatusmasterkode.
1. Vælg det entydige id for fragtmanden og fragttjenesten.
1. Vælg den transportstatuskode, du vil knytte til den valgte fragtmands kode.
1. Angiv den eksterne kode, der bruges af fragtmanden.
1. Luk siden.
