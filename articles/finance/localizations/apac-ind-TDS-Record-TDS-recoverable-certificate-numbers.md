---
title: Registrere certifikatnumre for skatterefundering
description: Denne artikel forklarer, hvordan du bruger siden Refusionscertifikater for at registrere certifikatnumrene og datoer på certifikater for kildeskat (TDS – Tax Deducted at Source), der er modtaget for en specifik kreditor-, debitor- og finanskonti.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 513412e292167795fad9d80b68e6e5e14dbd13c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853250"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Registrere certifikatnumre for skatterefundering

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du bruger siden **Refusionscertifikater** for at registrere certifikatnumrene og datoer på certifikater for kildeskat (TDS – Tax Deducted at Source), der er modtaget for en specifik kreditor-, debitor- og finanskonti. Hvis du vil opdatere skattecertifikatnumre og -datoer, der er registreret for skattetransaktioner på denne side, skal du bruge siden **Opdater certifikat** (**Finans \> Periodisk \> A-skat \> Opdater certifikat**). Når du er færdig med at opdatere skattecertifikatnumre, skal du lukke dem.

Følg disse trin for at registrere numre og -datoer for skattecertifikater.

1. Gå til **Skat \> Indirekte skat \> A-skat \> Refusionscertifikater**.

    [![Siden Refusionscertifikater.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Vælg **Kildeskat** i feltet **Skattetype** på siden **Refusionscertifikater**.
3. Vælg **Ny** for at oprette en post.
4. Angiv skattecertifikatnummeret i feltet **Certifikatnummer**.
5. Vælg den kontotype, som skattecertifikatet modtages for, i feltet **Kontotype**: **Kreditor**, **Debitor** eller **Finans**.
6. Vælg kreditor-, debitor- eller finanskontonummeret i feltet **Konto** afhængigt af den valgte kontotype. Feltet **Navn** viser navnet på kreditor-, debitor- eller finanskontoen.
7. Angiv beløbet for skattecertifikatet i feltet **Certifikatbeløb**.
8. Angiv certifikatdatoen for certifikatnummeret i feltet **Dato**.
9. Vælg **Forespørgsler** for at åbne siden **Certifikattransaktioner**, hvor du kan få vist de skattetransaktioner, som skattecertifikatnummeret og -datoen opdateres for. Disse oplysninger kan opdateres på siden **Opdater certifikat** (**Skat \> Angivelser \> A-skat \> Opdater certifikat**).

    På siden **Opdater certifikat** vises følgende oplysninger for hver skattetransaktion:

    - **Dato** – Bogføringsdatoen for skattetransaktionen.
    - **Bilag** – Bilagsnummeret på skattetransaktionen.
    - **Kilde** – Det modul, som skattetransaktionen blev oprettet i.
    - **Konto** – Det kreditor-, debitor- eller finanskontonummer, som skattetransaktionen er oprettet for.
    - **Navn** – Navnet på den kreditor-, debitor- eller finanskonton, som skattetransaktionen er oprettet for.
    - **Beløb** – Det fakturabeløb, som kildeskat blev beregnet for.
    - **Skattebeløb** – Det kildeskattebeløb, der er beregnet for transaktionen.
    - **Certifikatdato** – Den skattecertifikatdato, der blev opdateret for skattetransaktionen.
    - **Certifikatnummer** – Det skattecertifikatnummer, der blev opdateret for skattetransaktionen.

10. På siden **Refusionscertifikater** skal du markere afkrydsningsfeltet **Lukket** for at lukke skattecertifikatnummeret, når du er færdig med at opdatere det for skattetransaktioner på siden **Opdater certifikat**.

    Hvis du vil markere afkrydsningsfeltet **Lukket** for alle poster på siden, skal du markere **Markér alle**.

    > [!NOTE]
    > Skattecertifikatnumre, som afkrydsningsfeltet **Lukket** er markeret for, er ikke tilgængelige på siden **Opdater certifikat**.
