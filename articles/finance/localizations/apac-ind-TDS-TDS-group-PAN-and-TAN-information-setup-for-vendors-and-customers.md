---
title: Konfigurere kildeskattegruppe, permanent kontonummer og skattekontonummer for kreditorer og kunder
description: Dette emne beskriver, hvordan du angiver oplysninger om kildeskattegruppen (TDS – Tax Deducted at Source), det permanente kontonummer (PAN – Permanent Account Number) og skattekontonummeret (TAN – Tax Account Number) for kreditorer og kunder.
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
ms.openlocfilehash: b736838f1743a39d1f899f2679a31a2c0fe9a2b31e03b29d22af821314f329c9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745742"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Konfiguration af kildeskattegruppe, permanent kontonummer og skattekontonummer for kreditorer og kunder

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du angiver oplysninger om kildeskattegruppen (TDS – Tax Deducted at Source), det permanente kontonummer (PAN – Permanent Account Number) og skattekontonummeret (TAN – Tax Account Number) for kreditorer og kunder.

1. Gå til **Kreditor \> Kreditorer \> Alle kreditorer** eller **Debitor \> Kunder \> Alle kunder**.

    [![Siden Alle kreditorer.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Vælg **Ny** i handlingsruden for at oprette en kreditor eller debitor, og angiv de krævede oplysninger. Du kan også vælge en eksisterende kreditor eller debitor.
3. I sektionen **A-skat** i oversigtspanelet **Faktura og levering** skal du angive indstillingen **Beregn A-skat** til **Ja** for at beregne A-skat, kildeskat (TDS - Tax Deducted at Source) eller skat, der opkræves ved kilden (TCS – Tax Collected at Source) for kreditoren eller debitoren.
4. Kildeskat for en indkøbsfaktura beregnes på basis af den standardgruppe for kildeskat, der er defineret for kreditoren eller debitoren. I feltet **Kildeskattegruppe** skal du vælge kildeskattegruppen.

    > [!NOTE]
    > Når du vælger et kildeskattegruppe i feltet **Kildeskattegruppe**, bliver felterne **Gruppe for A-skat** og **Gruppe for skatteopkrævning ved kilde** utilgængelige.

5. Vælg statussen for det permanente kontonummer (PAN) for kreditoren eller debitoren i feltet **Status** i sektionen **PAN-oplysninger** i oversigtspanelet **Skatteoplysninger**:

    - **Ikke tilgængelig** – Kreditoren eller debitoren har ikke et PAN.
    - **Modtaget** – Kreditoren eller debitoren har et PAN.
    - **Ansøgt** – Kreditoren eller debitoren har ansøgt om et PAN.
    - **Ugyldig** – Kreditoren eller debitoren har et PAN, men det er ikke gyldigt.

6. Hvis du har valgt **Modtaget** i feltet **Status** for at angive, at kreditoren eller debitoren har et PAN, skal du angive dette PAN i feltet **Nummer**. Det permanente kontonummer (PAN) skal indeholde fem alfabetiske tegn, derefter fire numeriske tegn og derefter ét alfabetisk tegn. Her er et eksempel: **ABCDE1260A**.
7. Hvis du har valgt **Ansøgt** i feltet **Status** for at angive, at kreditoren eller debitoren har ansøgt om et PAN, skal du angive referencenummeret i feltet **Referencenummer**.
8. I feltet **Art af vurdering** skal du vælge den vurderingskategori, som kreditoren eller debitoren tilhører:

    - Firma
    - HUF
    - Autoriser
    - Individuelt
    - AOP
    - BOI
    - Lokal myndighed
    - Andre

    [![Oversigtspanelet Skatteoplysninger.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. I handlingsruden i gruppen **Registrering** under fanen **Kreditor** skal du vælge **Registrerings-id'er** for at åbne siden **Admistrer adresser**.
10. Vælg **Tilføj** eller **Rediger** på siden **Administrer adresser** i oversigtspanelet **Skatteoplysninger** for at åbne siden **Administrer skatteoplysninger**, hvor du kan opbevare skatteregistreringen.
11. I feltet **Skattekontonummer (TAN)** på siden **Administrer skatteoplysninger** i oversigtspanelet **A-skat** skal du skrive skattekontonummeret (TAN – Tax Account Number). Skattekontonummeret skal indeholde fire alfabetiske tegn, derefter fem numeriske tegn og derefter ét alfabetisk tegn. Her er et eksempel: **AFGH54821T**.
12. Luk siden.
