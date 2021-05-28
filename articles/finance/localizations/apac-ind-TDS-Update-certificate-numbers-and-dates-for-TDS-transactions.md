---
title: Opdatere certifikatnumre og -datoer for TDS-posteringer
description: Dette emne forklarer, hvordan du opdaterer de numre og datoer på refusionscertifikater, der er registreret for kreditor-, debitor- og finanskonti for afgifter fratrukket ved kilden (TDS).
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023114"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Opdatere certifikatnumre og -datoer for TDS-posteringer

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du opdaterer de numre og datoer på refusionscertifikater, der er registreret for kreditor-, debitor- og finanskonti for afgifter fratrukket ved kilden (TDS). Du kan få vist certifikaterne for TDS-transaktioner på siden **Refusionscertifikater**. Du kan opdatere certifikaterne ved hjælp af siden **Opdater certifikater**.

Følg disse trin for at opdatere certifikatnumre og -datoer for TDS-posteringer.

1. Gå til **Moms \> Opgørelser \> A-skat \> Opdater certifikat**.

    [![Siden Opdater certifikat](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Vælg **TDS** i feltet **Skattetype** i sektionen **Vælg** på siden **Opdater certifikat**.
3. Vælg debitors eller kreditors TDS-certifikatnummer i feltet **Certifikatnummer**.

    > [!NOTE]
    > I feltet **Certifikatnummer** vises kun TDS-certifikatnumre, som ikke er markeret i afkrydsningsfeltet **Lukket** på siden **Refusionscertifikater**.

    I feltet **Certifikatdato** vises certifikatdatoen. Feltet **Kontotype** viser den kontotype, som TDS-certifikatnummeret er modtaget for, og feltet **Navn** viser navnet på kontoen.

5. Vælg start- og slutdatoerne for den periode, TDS-transaktionerne skal vises for, i felterne **Fra-dato** og **Til-dato**.
6. Vælg **Vis data** for at få vist de TDS-transaktioner, der blev bogført i den valgte periode.

    Under fanen **Oversigt** viser gitteret i den øverste rude følgende oplysninger om hver TDS-transaktion, der er bogført for kreditoren eller debitoren i den valgte periode:

    - **Bilag** – Bilagsnummeret på skattetransaktionen.
    - **Dato** – Datoen for TDS-transaktionen.
    - **Beløb** – Det fakturabeløb, som kildeskat blev beregnet for.
    - **Skattebeløb** – Det kildeskattebeløb, der er beregnet for transaktionen.

7. Hvis du vil flytte specifikke TDS-posteringer fra det øverste gitter til det nederste gitter, skal du vælge posteringerne og derefter vælge **Medtag**. Alternativt kan du vælge **Medtag alle** for at flytte alle TDS-posteringer fra det øverste gitter til det nederste gitter.

    Hvis du vil flytte specifikke TDS-posteringer eller alle TDS-transaktioner fra det nederste gitter til det øverste gitter, skal du bruge knappen **Udelad** eller knappen **Udelad alle**.

8. Vælg **Opdater** for at opdatere felterne **Certifikatnummer** og **Certifikatdato** for TDS-posteringer i nederste gitter.
10. Gå til **Moms \> Indirekte skatter \> A-skat \> Refusionscertifikat**, og vælg **Forespørgsel** for at få vist de opdaterede posteringslinjer, der har de nye certifikatnumre, på siden **Certifikatposteringer**.

    [![Siden Certifikatposteringer](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
