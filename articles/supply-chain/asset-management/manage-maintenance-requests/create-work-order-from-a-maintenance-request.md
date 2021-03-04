---
title: Oprette arbejdsordrer ud fra vedligeholdelsesanmodninger
description: Dette emne forklarer, hvordan du opretter en arbejdsordre ud fra en vedligeholdelsesanmodning i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424689"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Oprette arbejdsordrer ud fra vedligeholdelsesanmodninger

[!include [banner](../../includes/banner.md)]

 


Når du har oprettet vedligeholdelsesanmodninger, kan du nemt konvertere dem til arbejdsordrer. I dette emne beskrives den hurtigste metode til at arbejde med vedligeholdelsesanmodninger på, opdatere flere vedligeholdelsesanmodninger på samme tid og derefter oprette en arbejdsordre for flere vedligeholdelsesanmodninger på samme tid. På siden **Aktive vedligeholdelsesanmodninger** og **Vedligeholdelsesanmodninger for mine arbejdssteder** kan du også arbejde med én vedligeholdelsesanmodning ad gangen og konvertere én vedligeholdelsesanmodning til en arbejdsordre.

> [!NOTE]
> Enhver vedligeholdelsesanmodning kan kun relateres til én arbejdsordre. Flere vedligeholdelsesanmodninger kan dog inkluderes i én arbejdsordre, selvom vedligeholdelsesanmodningerne har forskellige aktiver.

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger**.
2. Før du kan oprette en arbejdsordre ud fra vedligeholdelsesanmodninger, skal du som minimum vælge en vedligeholdelsesjobtype for vedligeholdelsesanmodningerne og også en variant og handel for vedligeholdelsesjobtypen, hvis disse oplysninger er relevante. I gittervisningen kan du nemt opdatere oplysninger for en vedligeholdelsesanmodning.
3. Når du er klar til at oprette en arbejdsordre, skal du vælge de vedligeholdelsesanmodninger, der skal medtages i den.

    - Hvis du vælger flere vedligeholdelsesanmodninger, der skal konverteres til en arbejdsordre, skal både feltet **Aktiv** og feltet **Vedligeholdelsesjobtype** angives, før du opretter arbejdsordren.
    - Hvis du vælger én vedligeholdelsesanmodning, der skal konverteres til en arbejdsordre, er det kun feltet **Aktiv**, der skal angives, før du opretter arbejdsordren. Men når du opretter arbejdsordren, kan du vælge en vedligeholdelsesjobtype (og en relateret variant og handel for vedligeholdelsesjobtypen, hvis disse oplysninger er relevante) i dialogboksen **Opret arbejdsordre**.

4. Vælg **Arbejdsordre**.
5. Angiv felterne i dialogboksen **Opret arbejdsordre**, og vælg derefter **OK**.

    En meddelelseslinje kan give dig besked om, at der er oprettet en ny arbejdsordre.

    Når du opretter en arbejdsordre, der er baseret på en vedligeholdelsesanmodning, og det aktiv, der er relateret til vedligeholdelsesanmodningen, er inkluderet i en garantiaftale, giver en meddelelseslinje dig desuden besked om garantiaftalen.

6. Vælg **Styring af aktiver** \> **Almindeligt** \> **Arbejdsordrer** \> **Alle arbejdsordrer**, og åbn derefter den nye arbejdsordre.

    ![Åbne ny arbejdsordre](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]