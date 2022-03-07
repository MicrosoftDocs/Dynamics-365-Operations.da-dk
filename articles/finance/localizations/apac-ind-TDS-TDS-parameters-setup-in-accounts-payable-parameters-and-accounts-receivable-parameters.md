---
title: Angive parametre for kildeskat i Kreditor og Debitor
description: Dette emne beskriver, hvordan du angiver parametre i Kreditor og Debitor, som understøtter fradrag af kildeskat (TDS – Tax Deducted at Source).
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
ms.openlocfilehash: ccf1557d3c95829421b26d5f84750e3d4236c9e0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358212"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Angive parametre for kildeskat i Kreditor og Debitor

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du angiver parametre i Kreditor og Debitor, som understøtter fradrag af kildeskat (TDS – Tax Deducted at Source).

1. Gå til **Skat \> Opsætning \> Parametre \> Debitorparametre**.
2. Vælg **Opdater ordrelinjer** under fanen **Opdateringer** for at åbne dialogboksen **Opdater ordrelinjer**.
3. I feltet **Opdatering af kildeskattegruppe** i sektionen **Kildeskattegruppe** skal du angive den metode, du vil bruge til at opdatere kildeskattegruppen på linjeniveau. Denne indstilling bruges, når kildeskattegruppen opdateres i et ordrehoved. Der findes følgende indstillinger:

    - **Aldrig** – Kildeskattegruppen opdateres ikke på ordrelinjerne, når den opdateres i ordrehovedet.
    - **Altid** – Kildeskattegruppen opdateres automatisk på ordrelinjerne, når den opdateres i ordrehovedet.
    - **Spørg** – Brugerne modtager en meddelelse, hvor de bliver spurgt, om de vil opdatere kildeskattegruppen på ordrelinjerne.
4. Vælg **OK**.

    [![Dialogboksen Opdater ordrelinjer.](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Gå til **Skat \> Opsætning \> Parametre \> Kreditorparametre**.
6. Under fanen **Generelt** skal du i oversigtspanelet **Opdeling baseret på leveringsoplysninger** skal du angive indstillingen **Produktkvittering** til **Ja** for at bogføre og opdele en produktkvittering, der har forskellige leveringsadresser og skattekontonumre (TAN – Tax Account Number). Hvis denne indstilling er angivet til **Nej**, kan du ikke bogføre et indkøbs følgeseddel, som har forskellige leveringsadresser og skattekontonumre.
7. Angiv indstillingen **Faktura** til **Ja** for at bogføre og opdele en indkøbsfaktura, der har forskellige leveringsadresser og skattekontonumre.

    [![Oversigtspanelet Opdeling baseret på leveringsoplysninger.](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Luk siden.
