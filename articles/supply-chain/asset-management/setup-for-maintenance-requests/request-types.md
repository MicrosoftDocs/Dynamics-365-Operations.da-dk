---
title: Typer af vedligeholdelsesanmodninger
description: Dette emne beskriver, hvordan du konfigurerer typer af vedligeholdelsesanmodninger i Styring af aktiver.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 125a4efda6fe8e9e65e2a0c166355235727e6cfa
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356434"
---
# <a name="maintenance-request-types"></a>Typer af vedligeholdelsesanmodninger

[!include [banner](../../includes/banner.md)]

 

Vedligeholdelsesanmodningstyper bruges til at kategorisere vedligeholdelsesanmodninger. Du kan for eksempel have vedligeholdelsesanmodningstyper, der er relateret til forebyggende vedligeholdelse og korrigerende vedligeholdelse. Eller du kan have en særlig vedligeholdelsesanmodningstype, der bruges til at administrere reparationer af aktiver (depotreparation).

En vedligeholdelsesanmodningstype definerer tilknytningen til en vedligeholdelsesanmodnings livscyklustilstandsgruppe (vedligeholdelseslivscyklusmodel). Livscyklusmodeller for vedligeholdelsesanmodninger definerer de livscyklustilstande, der kan angives for en vedligeholdelsesanmodning. (Eksempler på livscyklustilstande for vedligeholdelsesanmodninger omfatter **Oprettet**, **Aktive** og **Afsluttede**.)

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsesanmodninger** \> **Vedligeholdelsesanmodningstyper**.
2. Vælg **Ny** for at oprette en vedligeholdelsesanmodningstype.
3. I feltet **Vedligeholdelsesanmodningstype** skal du angive et ID for vedligeholdelsesanmodningstypen.
4. Indtast et navn i feltet **Navn**.
5. I oversigtspanelet **Generelt** skal du i feltet **Vedligeholdelsesanmodningens livscyklusmodel** vælge en livscyklusmodel for vedligeholdelsesanmodningen.
6. I feltet **Arbejdsordretype** skal du vælge en arbejdsordretype. Når en vedligeholdelsesanmodning konverteres til en arbejdsordre, får arbejdsordren automatisk den arbejdsordretype, der er relateret til vedligeholdelsesanmodningstypen.

I følgende illustration vises et eksempel på listesiden **Vedligeholdelsesanmodningstype**.

![Siden Vedligeholdelsesanmodningstyper.](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]