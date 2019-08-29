---
title: Typer af vedligeholdelsesanmodninger
description: Dette emne beskriver, hvordan du konfigurerer typer af vedligeholdelsesanmodninger i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790477"
---
# <a name="maintenance-request-types"></a>Typer af vedligeholdelsesanmodninger

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Vedligeholdelsesanmodningstyper bruges til at kategorisere vedligeholdelsesanmodninger. Du kan for eksempel have vedligeholdelsesanmodningstyper, der er relateret til forebyggende vedligeholdelse og korrigerende vedligeholdelse. Eller du kan have en særlig vedligeholdelsesanmodningstype, der bruges til at administrere reparationer af aktiver (depotreparation).

En vedligeholdelsesanmodningstype definerer tilknytningen til en vedligeholdelsesanmodnings livscyklustilstandsgruppe (vedligeholdelseslivscyklusmodel). Livscyklusmodeller for vedligeholdelsesanmodninger definerer de livscyklustilstande, der kan angives for en vedligeholdelsesanmodning. (Eksempler på livscyklustilstande for vedligeholdelsesanmodninger omfatter **Oprettet**, **Aktive** og **Afsluttede**.)

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsesanmodninger** \> **Vedligeholdelsesanmodningstyper**.
2. Vælg **Ny** for at oprette en vedligeholdelsesanmodningstype.
3. I feltet **Vedligeholdelsesanmodningstype** skal du angive et ID for vedligeholdelsesanmodningstypen.
4. Indtast et navn i feltet **Navn**.
5. I oversigtspanelet **Generelt** skal du i feltet **Vedligeholdelsesanmodningens livscyklusmodel** vælge en livscyklusmodel for vedligeholdelsesanmodningen.
6. I feltet **Arbejdsordretype** skal du vælge en arbejdsordretype. Når en vedligeholdelsesanmodning konverteres til en arbejdsordre, får arbejdsordren automatisk den arbejdsordretype, der er relateret til vedligeholdelsesanmodningstypen.

I følgende illustration vises et eksempel på listesiden **Vedligeholdelsesanmodningstype**.

![Figur 1](media/07-setup-for-requests.png)