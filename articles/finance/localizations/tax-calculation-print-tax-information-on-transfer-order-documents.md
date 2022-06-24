---
title: Udskrive momsoplysninger på flytteordredokumenter
description: Denne artikel forklarer, hvordan de momsoplysninger, der bestemmes af tjenesten til momsberegning, kan udskrives på flytteordredokumenter.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: ca7a610162c539a0ecd74cf9e663f08ea80a7e44
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855196"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Udskrive momsoplysninger på flytteordredokumenter

[!include [banner](../../includes/banner.md)]

Denne artikel forklarer, hvordan du udskriver momsoplysninger i flytteordredokumenter. Du kan udskrive pro-forma-fakturadokumentet for en flytteordre for lageroverførsler, der opfattes som fællesskabsforsyninger og -anskaffelser inden for EU i henhold til EU's momsregler. 

Følgende momsrelevante data føjes til flytteordredokumenterne:

- Navnene på og afsendelses- og leveringsadresserne for lageroverførslen
- Momsidentifikationsnumrene for leverandøren og modtageren
- Enhedsprisen og det momspligtige beløb for de leverede varer
- Momskode, momssats, momsbeløb og momsdirektiver

Hvis du vil konfigurere disse data, skal du udføre følgende hovedtrin.

1. [Aktivere og konfigurere momsfunktionen for flytteordrer](tasks/Tax-feature-support-for-transfer-order.md).
2. [Oprette og konfigurere flere momsregistreringsnumre for en juridisk enhed](emea-multiple-vat-registration-numbers.md).
3. Konfigurere fritagelseskode, beskrivelse, momsdirektiver og udskriftskode i momskoder. I dette eksempel er der oprettet tre momskoder, som synkroniseres i Microsoft Dynamics 365 Finance: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.

    1. I Finance skal du gå til **Moms** \> **Konfiguration** \> **Moms** \> **Momsfritagelseskoder**.
    2. Vælg **Rediger**, og angiv en beskrivelse af fritagelseskoden **EC**. Skriv for eksempel **Momsfri EC-leveringer med momsregistreringsnummer**.
    3. Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momskoder**.
    4. Vælg momskoden **BE-RC-21**, og vælg derefter **Momsdirektiver**.
    5. Vælg **Ny**.
    6. I feltet **Sprog** skal du vælge **EN-US**. I feltet **Tekst** skal du derefter skrive **Dokument, der fastsætter vareoverførslen i henhold til 138. 2. c) i EU-momsdirektiv 2006/112/EC**.
    7. Luk siden.
    8. Vælg **Momssats** i feltet **Udskriv** i oversigtspanelet **Generelt**.
    8. Vælg momskoden **NL-Exempt**, og vælg derefter **Momssats** i feltet **Udskriv** i oversigtspanelet **Generelt**.

    > [!NOTE] 
    > Beskrivelsen af momskode, momssats og momsfritagelse udskrives ikke på flytteordredokumenter, hvis der ikke er en beskrivelse af fritagelseskoden eller momsdirektiver for momskoden.

## <a name="print-the-transfer-order---shipment-document"></a>Udskrive flytteordren – forsendelsesdokument

Når en overførsel er afsendt, skal du benytte følgende fremgangsmåde for at udskrive flytteordren – forsendelsesdokument.

1. Gå til **Lagerstyring** \> **Forespørgsler og rapporter** \> **Flytteordrer** \> **Forsendelse**.
2. Aktivér **Momsoplysninger** i gruppen **Udskriv** under fanen **Parametre**.
3. Under fanen **Poster, der skal indgå** skal du vælge **Filter**, vælge flytteordrenummeret og derefter vælge **OK**.
4. Vælg **OK** for at udskrive flytteordren – forsendelsesdokument.

## <a name="print-the-transfer-order---receipt-document"></a>Udskrive flytteordren – modtagelsesdokument

Når en overførsel er modtaget, skal du benytte følgende fremgangsmåde for at udskrive flytteordren – modtagelsesdokument.

1. Gå til **Lagerstyring** \> **Forespørgsler og rapporter** \> **Flytteordrer** \> **Modtag**.
2. Aktivér **Momsoplysninger** i gruppen **Udskriv** under fanen **Parametre**.
3. Under fanen **Poster, der skal indgå** skal du vælge **Filter**, vælge flytteordrenummeret og derefter vælge **OK**.
4. Vælg **OK** for at udskrive flytteordren – modtagelsesdokument.

## <a name="print-the-transfer-overview-document"></a>Udskrive dokumentet med overførselsoversigten

Benyt følgende fremgangsmåde for at udskrive dokumentet med overførselsoversigten.

> [!NOTE]
> Momsoplysninger er kun tilgængelige, når flytteordren er afsendt eller modtaget.

1. Gå til **Lagerstyring** \> **Forespørgsler og rapporter** \> **Flytteordrer** \> **Overførselsoversigt**.
2. Aktivér **Momsoplysninger** i gruppen **Udskriv** under fanen **Parametre**.
3. Under fanen **Poster, der skal indgå** skal du vælge **Filter**, vælge flytteordrenummeret og derefter vælge **OK**.
4. Vælg **OK** for at udskrive dokumentet med overførselsoversigten.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
