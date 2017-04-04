---
title: "Oversigt over indkøbsordrer"
description: "Denne artikel indeholder generelle oplysninger om indkøbsordrer (IO&quot;er) og links til andre artikler, der er relateret til de forskellige stadier, som en indkøbsordre gennemgår."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: aed1a411aaefeebb96c2b922afc2e3e7f82cdbb7
ms.lasthandoff: 03/31/2017


---

# <a name="purchase-order-overview"></a>Oversigt over indkøbsordrer

Denne artikel indeholder generelle oplysninger om indkøbsordrer (IO'er) og links til andre artikler, der er relateret til de forskellige stadier, som en indkøbsordre gennemgår.

En købsordre (IO) er et dokument, der repræsenterer en aftale med en leverandør om at købe varer eller tjenesteydelser. Dokumentet hjælper også med at holde styr på de produktkvitteringer, der foretages på ordren, og senere bogføring af kreditorfakturaer, som leverandøren fakturerer på ordren.  

Siden **Indkøbsordrer** indeholder en oversigt over de ordrer, der er tilgængelige, og kan du redigere disse ordrer. Når du åbner en indkøbsordre, kan du vælge visningen **Hoved**, der indeholder oplysninger, der kun angives én gang for hver indkøbsordre, som f.eks. kreditor. Du kan også vælge visningen **Linjer**, hvor du kan redigere ordrelinjer. Du vil typisk skifte mellem disse to visninger, som du redigerer POs. Tillæg ikke står direkte på den **indkøbsordrer,**, men de er tilgængelige via menuer i ordrehovedet og på linjerne.  

Der er mange rapporter, hvor du kan se oplysninger om IO'er, produktkvitteringer og kreditorfakturaer. Disse rapporter findes i modulerne **Indkøb og forsyning** og **Kreditor**.  

I arbejdsområderne **Klargøring af indkøbsordrer** og **Indkøbsordre, modtagelse og opfølgning** kan du få vist en liste over IO'er i de forskellige statusser, som de er kommet til. De indeholder også en oversigt over de handlinger, der skal træffes. Arbejdsområdet **Klargøring af indkøbsordrer** er fokuseret på IO-oprettelse og -gennemsyn, behandling af ordren via godkendelse og bekræftelse med leverandøren. Den **købe ordretilgang og opfølgning** arbejdsområde er fokuseret på behandling af modtagelsen af varer eller tjenester mod POs. Det indeholder lister, der giver indsigt i tilgange, der er forfaldne, eller der vil snart være forfalden til levering af leverandøren. Disse arbejdsområder bruges ikke til at udføre de tilhørende tilgangsaktiviteter, der udføres på lagerstedet. Disse aktiviteter udføres ved hjælp af siderne i modulerne **Lagerstyring** og **Lokationsstyring**. Behandling af kreditorfakturaer skal udføres ved hjælp af arbejdsområdet **Kreditorfakturapostering**, og betalinger skal ske ved hjælp af arbejdsområdet **Kreditorbetalinger**.  

Følgende artikler indeholder en oversigt over de forskellige faser, som en IO gennemgår:

-   [Oprettelse af indkøbsordre](purchase-order-creation.md)
-   [Godkendelse og bekræftelse af indkøbsordre](purchase-order-approval-confirmation.md)
-   [Produktkvittering sammenlignet med indkøbsordrer](product-receipt-against-purchase-orders.md)
-   [Oversigt over kreditorfakturaer](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)

## <a name="types-of-purchase-orders"></a>Indkøbsordretyper
Der findes tre typer POs. Når du opretter en Indkøbsordre, skal du angive typen. Du kan oprette en standardordretype for nye ordrer på siden **Indkøbs- og forsyningsparametre**.

| IO-type        | Beskrivelse                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Journal        | Brug denne type til at oprette et udkast til en ordre. Denne type har ingen indflydelse på lagermængder og genererer ingen lagertransaktioner. IO-kladdelinjerne medtages ikke i behovsplanlægningen.                                                                                                       |
| Indkøbsordre | Brug denne type til at oprette IO'er, når ordrer bekræftes med en leverandør, og efterhånden som ordrerne behandles via modtagelse og fakturering, før betalingen foretages til kreditoren. Denne type IO er den mest almindelige.                                                                          |
| Returordre | Brug denne type, når du returnerer varer til leverandøren. Denne ordretype kræver, at du angiver det RMA-nummer (Return Material Authorization), som leverandøren giver dig. Du kan angive RMA-nummeret under fanen **Generelt** i indkøbsordren. Ordrelinjerne skal have negative antal. |

## <a name="purchase-order-statuses"></a>Statusser for indkøbsordre
IO'er inkluderer flere statusfelter, der angiver status for ordren. Disse felter kan ses i ordrevisningen **Hoved**, og nogle af dem kan også ses i gitteroversigten over alle ordrer. Feltet **Status** vises status for antal i ordren. Følgende værdier er tilgængelige:

-   **Åben ordre** – Ordrer er blevet oprettet, og mængder er bestilt.
-   **Modtaget** – Nogle af mængderne er modtaget, men de er ikke faktureret endnu.
-   **Faktureret** – Den fulde mængde i ordren er blevet faktureret. **Bemærk:** Hvis en ordre er blevet *delvist* faktureret, skal hverken **Modtaget** status eller **Faktureret** status anvendes. Derfor har ordren stadig status som **Åben ordre**.
-   **Annulleret** – En ordre blev bekræftet, men senere annulleret. Denne status angiver derfor, at der er ikke længere nogen åbne antal i bestilling.

I feltet **Dokumentstatus** kan du hurtigt gennemse ordrens status med hensyn til dokumenter, der er blevet behandlet. Det viser status for det seneste dokument, der er fuldført på ordren. Følgende værdier er tilgængelige:

-   **Ingen** – Ingen dokumenter er blevet behandlet for ordren endnu.
-   **Købsforespørgsel** – En købsforespørgsel er blevet genereret, og ordren afventer tilbagemelding fra leverandøren.
-   **Indkøbsordre** – Bekræftelsen er blevet behandlet for ordren.
-   **Produktkvittering** – Produktkvittering er blevet behandlet for ordren.
-   **Faktura** – Der er registreret en faktura sammen med ordren.

Feltet **Godkendelsesstatus** bruges, når en IO gennemgår en gennemsynsproces eller arbejdsgang. Følgende værdier er tilgængelige:

-   **Udkast**, **Til gennemsyn** og **Afvist** – Disse statusser bruges kun, når der bruges en godkendelsesarbejdsgang for indkøbsordren.
-   **Godkendt** – Denne status tildeles til ordrer, der har godkendelse af fuldført arbejdsgang. Ordrer, der oprettes uden brug af en arbejdsgang for godkendelse, får straks status **Godkendt**.
-   **Til eksternt gennemsyn** – Denne status bruges i situationer, hvor en købsforespørgsel sendes til kreditoren, så kreditoren kan bekræfte vilkårene i indkøbsordren. Denne status bruges også i den proces, der iværksættes af handlingen **Anmodning om bekræftelse**. For denne proces bliver kreditoren bedt om at bekræfte vilkår for indkøbsordren ved at oprette forbindelse til dit system og registrere, om ordren bekræftes eller afvises.
-   **Bekræftet** – Denne status tildeles, når ordren er blevet bekræftet. Denne status er typisk den sidste godkendelsesstatus, der tildeles til en ordre.


<a name="see-also"></a>Se også
--------

[Purchase order creation](purchase-order-creation.md)

[Godkendelse og bekræftelse af indkøbsordre](purchase-order-approval-confirmation.md)

[Produktkvittering sammenlignet med indkøbsordrer](product-receipt-against-purchase-orders.md)

[Oversigt over kreditorfakturaer](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)


