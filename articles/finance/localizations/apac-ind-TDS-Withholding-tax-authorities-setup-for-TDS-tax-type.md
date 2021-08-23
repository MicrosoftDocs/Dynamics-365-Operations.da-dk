---
title: Konfigurere A-skat-myndigheder for TDS-skattetypen
description: Dette emne forklarer, hvordan du opretter TDS-skattemyndigheder for afgifter trukket ved kilden.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: aff7c932a1395393935819dee1f342d2abdc75169bb68c6c6776edc1c5b2a3bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758819"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a>Konfigurere A-skat-myndigheder for TDS-skattetypen

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du opretter TDS-skattemyndigheder for afgifter trukket ved kilden.

1. Gå til **Moms \> Indirekte skatter \> A-skattemyndigheder**.

    [![Siden A-skattemyndigheder.](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)

2. Vælg **TDS** i feltet **Skattetype** for at konfigurere skattemyndigheder for TDS-skattetypen.
3. Vælg **Ny** i handlingsruden for at oprette en linje.
4. Angiv et navn for TDS-myndigheden i feltet **A-skattemyndighed**.
5. Indtast en beskrivelse i feltet **Beskrivelse**.
6. Vælg kreditorkontoen for TDS-skattemyndigheden i feltet **Kreditorkonto** under fanen **Generelt**.

    > [!NOTE]
    > Du skal definere navnet på den bank, hvor penge, som skyldes til TDS-myndighedskreditoren, skal indbetales. Bankens navn defineres på siden **Bankkonti** (**Kreditor \> Alle kreditorer \> Kreditor \> Konfigurerer \> Bankkonti**).

7. Luk siden.
