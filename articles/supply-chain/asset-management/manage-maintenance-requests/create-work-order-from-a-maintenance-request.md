---
title: Oprette arbejdsordrer ud fra vedligeholdelsesanmodninger
description: Denne artikel forklarer, hvordan du opretter en arbejdsordre ud fra en vedligeholdelsesanmodning i Styring af aktiver.
author: johanhoffmann
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb54ec3466086afbd87a023a40e346a6a3464c98
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017168"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Oprette arbejdsordrer ud fra vedligeholdelsesanmodninger

[!include [banner](../../includes/banner.md)]

 


Når du har oprettet vedligeholdelsesanmodninger, kan du nemt konvertere dem til arbejdsordrer. Denne artikel beskriver den hurtigste metode til at arbejde med vedligeholdelsesanmodninger på, opdatere flere vedligeholdelsesanmodninger på samme tid og derefter oprette en arbejdsordre for flere vedligeholdelsesanmodninger på samme tid. På siden **Aktive vedligeholdelsesanmodninger** og **Vedligeholdelsesanmodninger for mine arbejdssteder** kan du også arbejde med én vedligeholdelsesanmodning ad gangen og konvertere én vedligeholdelsesanmodning til en arbejdsordre.

> [!NOTE]
> Enhver vedligeholdelsesanmodning kan kun relateres til én arbejdsordre. Flere vedligeholdelsesanmodninger kan dog inkluderes i én arbejdsordre, selvom vedligeholdelsesanmodningerne har forskellige aktiver.

1. Vælg **Styring af aktiver** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger**.
2. Før du kan oprette en arbejdsordre ud fra vedligeholdelsesanmodninger, skal du som minimum vælge en vedligeholdelsesjobtype for vedligeholdelsesanmodningerne og også en variant og handel for vedligeholdelsesjobtypen, hvis disse oplysninger er relevante. I gittervisningen kan du nemt opdatere oplysninger for en vedligeholdelsesanmodning.
3. Når du er klar til at oprette en arbejdsordre, skal du vælge de vedligeholdelsesanmodninger, der skal medtages i den.

    - Hvis du vælger flere vedligeholdelsesanmodninger, der skal konverteres til en arbejdsordre, skal både feltet **Aktiv** og feltet **Vedligeholdelsesjobtype** angives, før du opretter arbejdsordren.
    - Hvis du vælger én vedligeholdelsesanmodning, der skal konverteres til en arbejdsordre, er det kun feltet **Aktiv**, der skal angives, før du opretter arbejdsordren. Men når du opretter arbejdsordren, kan du vælge en vedligeholdelsesjobtype (og en relateret variant og handel for vedligeholdelsesjobtypen, hvis disse oplysninger er relevante) i dialogboksen **Opret arbejdsordre**.

4. Vælg **Arbejdsordre**.
5. Angiv felterne i dialogboksen **Opret arbejdsordre**, og vælg derefter **OK**.

    En meddelelseslinje kan give dig besked om, at der er oprettet en ny arbejdsordre.

    Når du opretter en arbejdsordre, der er baseret på en vedligeholdelsesanmodning, og det aktiv, der er relateret til vedligeholdelsesanmodningen, er inkluderet i en garantiaftale, giver en meddelelseslinje dig desuden besked om garantiaftalen.

6. Vælg **Styring af aktiver** \> **Arbejdsordrer** \> **Alle arbejdsordrer**, og åbn derefter den nye arbejdsordre.

    ![Åbne ny arbejdsordre.](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]