---
title: Oprette en leasinggruppe
description: I dette emne forklares, hvordan du konfigurerer leasinggrupper. Der kræves leasinggrupper for at oprette nye leasingaftaler.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 88a49e4db868078fd05875df33ca5727363aaa18
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881222"
---
# <a name="create-a-lease-group"></a>Oprette en leasinggruppe

[!include [banner](../includes/banner.md)]

I dette emne forklares, hvordan du konfigurerer leasinggrupper. Der kræves leasinggrupper for at oprette nye leasingaftaler. Leasingkartoteker knyttes til hver leasinggruppe. Leasingkartoteker bestemmer, hvilke standardprofiler der skal oprettes for hver leasingaftale. Du kan knytte bestemte konti til en leasinggruppe på siden **Leasingbogføringsparametre**.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Oprette en leasingprofil og tilføje en leasinggruppe

1. Gå til **Aktivleasing \> Konfiguration \> Leasinggrupper**.
2. Vælg **Ny** i handlingsruden for at tilføje en leasinggruppe. Der føjes en linje til gitteret.
3. Angiv en værdi i feltet **Leasinggruppe**.
4. Indtast en værdi i feltet **Beskrivelse**.

De oplysninger, du netop har angivet, føjes til feltet **Leasinggruppe** på siden **Tilføj leasingaftale**.

## <a name="associate-a-book-with-a-lease-group"></a>Knytte et kartotek til en leasinggruppe

Når du har oprettet leasinggrupper, kan du knytte kartoteker til hver gruppe. Når du opretter en leasingaftale og tildeler den til en leasinggruppe, opretter systemet et sæt planer for hvert enkelt kartotek, der er knyttet til leasinggruppen.

> [!NOTE]
> Kartoteker skal konfigureres, før de kan tildeles en leasinggruppe.

1. Gå til **Aktivleasing \> Konfiguration \> Leasinggruppe**.
2. Vælg en leasinggruppe, og vælg derefter **Kartoteker**.
3. Vælg **Ny**, og vælg derefter feltet **Kartotekstype**, der skal knyttes til leasinggruppen. Du kan tildele flere kartoteker til en leasinggruppe, hvis en leasingaftalen skal redegøres for på forskellige måder.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
