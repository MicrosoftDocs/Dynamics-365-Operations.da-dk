---
title: Svensk Intrastat
description: Dette emne indeholder oplysninger om Intrastat-rapportering i Sverige.
author: anasyash
ms.date: 8/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 1031b93950e44fe3b1b6254bf1503b4c09d6fd10
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727392"
---
# <a name="swedish-intrastat"></a>Svensk Intrastat

[!include[banner](../includes/banner.md)]

Siden **Intrastat** bruges til at generere og rapportere oplysninger om handel mellem EU-lande. Den svenske Intrastat-opgørelse indeholder oplysninger om varehandel til indberetning.

Følgende felter medtages i den svenske Intrastat-opgørelse:

   - ISO-kode for partnerland
   - Transaktionsart
   - Varekode
   - Supplerende enhed
   - Tykkelse
   - Fakturabeløb

## <a name="set-up-intrastat"></a>Konfigurere Intrastat

Importer den seneste version af følgende ER-konfigurationer (Elektronisk rapportering):

   - Intrastat-modul
   - Intrastat-rapport
   - Intrastat (SE)

Du kan finde flere oplysninger under [Downloade ER-konfigurationer fra det globale lager i konfigurationstjeneste](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre

1. I Microsoft Dynamics 365 Finance skal du gå til **Moms** > **Konfiguration** > **Parametre for udenrigshandel**.
2. Under fanen **Intrastat** skal du i feltet **Tilknytning af filformat** vælge **Intrastat (SE)** i oversigtspanelet **Elektronisk rapportering**.
3. Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.
4. Vælg **Intrastat** i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
5. I feltet **Transaktionskode** skal du vælge transaktionskoden for egenskabsoverførsler. Denne kode bruges til transaktioner, der opretter faktiske eller planlagte overførsler af egenskab mod kompensation (økonomisk eller på anden vis). Du kan også bruge den til rettelser. Virksomheder i Sverige bruger etcifrede transaktionskoder.
6. I feltet **Kreditnota** skal du vælge transaktionskoden for returnering af varer.
7. Under fanen **Lande-/områdeegenskaber** indeholder feltet **Land/område** alle de lande eller områder, som dit firma handler med. For hvert land/område, der indgår i EU, skal du vælge **EU** i feltet **Lande-/områdetype**, så landet/området vises i Intrastat-rapporten.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>Angive produktparametre for Intrastat-opgørelsen

1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
2. Vælg et produkt i gitteret.
3. Vælg den relevante varekode i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
4. Angiv produktets vægt i kilo i feltet **Nettovægt** i oversigtspanelet **Styr lager**.
5. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Komprimering for Intrastat**, og vælg de felter, der skal sammenlignes, når Intrastat-oplysninger opsummeres. Vælg følgende felter til for svensk Intrastat:

    - Varekode
    - Transaktionsart
    - Vej
    - Land/område
    - Rettelse
    - Fakturaer

## <a name="intrastat-transfer"></a>Intrastat-overførsel

På siden **Intrastat** i handlingsruden kan du vælge **Overfør** for automatisk at overføre oplysninger om samhandel med andre steder fra salgsordrer, fritekstfakturaer, indkøbsordrer, kreditorfakturaer, produktkvittering for kreditorer, projektfakturaer og overførselsordrer. Det er kun dokumenter, hvor et EU-land er destinationsland eller -område (til afsendelser) eller forsendelse (til modtagelser), der overføres.

Du kan også angive posteringer manuelt ved at vælge **Ny** i handlingsruden.

### <a name="generate-an-intrastat-report"></a>Generere en Intrastat-rapport

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Output** > **Rapport** i handlingsruden.
3. I dialogboksen **Intrastat-rapport** skal du angive følgende felter.

    | Felt            | Betegnelse                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Fra-dato        | Vælg startdatoen for rapporten.                                                                                               |
    | Til-dato          | Vælg slutdatoen for rapporten.                                                                                                 |
    | Generer fil    | Angiv denne indstilling til **Ja** for at generere en .txt-fil til Intrastat-rapporten.                                                       |
    | Filnavn        | Angiv navnet på .txt-filen.                                                                                                    |
    | Generér rapport  | Angiv denne indstilling til **Ja** for at generere en .xlsx-fil til Intrastat-rapporten.                                                     |
    | Rapportfilnavn | Angiv navnet på .xlsx-filen.                                                                                                   |
    | Vej        | Vælg **Modtagelser** for en rapport om modtagelser inden for fællesskabet. Vælg **Afsendelser** for en rapport om afsendelser inden for fællesskabet. |

4. Vælg **OK**, og gennemse de genererede rapporter.

## <a name="example"></a>Eksempel

Dette eksempel viser, hvordan du bogfører indførsler og udførsler til Intrastat. Det bruger den juridiske enhed **DEMF**.

### <a name="preliminary-setup"></a>Foreløbig opsætning

1. Gå til **Organisationsadministration** > **Organisation** > **Juridiske enheder**, og vælg den juridiske **DEMF**-enhed.
2. Vælg **Rediger** i oversigtspanelet **Adresser**, og vælg derefter **SWE (Sverige)** i feltet **Land/område**.
3. Importér den seneste version af følgende ER-konfigurationer:

    - Intrastat-modul
    - Intrastat-rapport
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Oprette transaktionskoder

1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Transaktionskoder**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv **1** i feltet **Transaktionskode**.
4. Angiv **Normale transaktioner** i feltet **Navn**.
5. Vælg **Gem** i handlingsruden.

### <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre

1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Udenrigshandelsparametre**.
2. Vælg **1** i feltet **Transaktionskode** i oversigtspanelet **Generelt** under fanen **Intrastat**.
3. Vælg **Intrastat (SE)** i feltet **Tilknytning af filformat** i oversigtspanelet **Elektronisk rapportering**.
4. Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.
5. Sørg for, at **Intrastat** er valgt i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
6. Vælg **Ny** under fanen **Egenskaber for land/område**.
7. Vælg **SWE** i feltet **Land/område for part**.
8. Vælg **Indland** i feltet **Lande-/områdetype**.
9. Vælg **DEU** i feltet **Land/område for part**, og vælg derefter **EU** i feltet **Lande/områdetype**.

### <a name="set-up-product-information"></a>Angive produktoplysninger

1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
2. Vælg **D0001** i gitteret.
3. Vælg **100 200 30** i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
4. Angiv **5** i feltet **Nettovægt** i sektionen **Vægtmålinger** i oversigtspanelet **Styr lager**.
5. Vælg **Gem** i handlingsruden.

### <a name="change-the-site-address"></a>Ændre adressen for webstedet

1. Gå til **Lagerstedsstyring** > **Konfiguration** > **Lagersted** > **Steder**.
2. Vælg **1** i gitteret.
3. Vælg **Rediger** i oversigtspanelet **Adresser**.
4. Vælg **SWE** i feltet **Land/område** i dialogboksen **Rediger adresse**.
5. Vælg **OK**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Oprette en salgsordre for en EU-kunde

1. Gå til **Debitor** > **Ordrer** > **Alle salgsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. I dialogboksen **Opret salgsordre** skal du i sektionen **Debitor** i feltet **Debitorkonto** i oversigtspanelet **Debitor** vælge **DE-015**.
4. Vælg **1** i feltet **Websted** i sektionen **Lagringsdimensioner** i oversigtspanelet **Generelt**.
5. Vælg **11** i feltet **Lagersted**.
6. Vælg **OK**.
7. Vælg **D0001** i feltet **Varenummer** i oversigtspanelet **Salgsordrelinjer** under fanen **Linjer**. Angiv derefter **10** i feltet **Antal**.
8. I oversigtspanelet **Linjedetaljer** skal du under fanen **Udenrigshandel** kontrollere, at felterne **Transaktionskode** og **Vare** er angivet automatisk.
9. Vælg **Gem** i handlingsruden.
10. Vælg **Faktura** i sektionen **Generér** under fanen **Faktura** i handlingsruden.
11. I dialogboksen **Bogføringsfaktura** i oversigtspanelet **Parametre** i sektionen **Parameter** i feltet **Antal** skal du vælge **Alle**.
12. Vælg **OK** for at bogføre fakturaen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Overføre transaktionen til Intrastat-kladden og gennemse resultatet

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Overfør** i handlingsruden.
3. Angiv indstillingen **Debitorfaktura** til **Ja** i sekionen **Parametre** i dialogboksen **Intrastat (Overførsel)**.
4. Vælg **Filter**.
5. Vælg den første linje i dialogboksen **Intrastat-filter** under fanen **Interval**, og kontrollér, at feltet **Felt** er angivet til **Dato**.
6. Vælg dags dato i feltet **Kriterier**.
7. Vælg **OK** for at lukke dialogboksen **Intrastat-filter**.
8. Vælg **OK** for at lukke dialogboksen **Intrastat (Overførsel)** og gennemgå resultatet. Linjen repræsenterer den salgsordre, du har oprettet tidligere.

    ![Intrastat-kladdelinjer for salgsordre](media/swe_intrastat_journal_sales_order.png)

9. Vælg transaktionslinjen, og vælg derefter fanen **Generelt** for at få vist flere detaljer.

    ![Intrastat-kladdelinjeoplysninger for salgsordre](media/swe_intrastat_journal_sales_order_line_details.png)

10. Vælg **Output** > **Rapport** i handlingsruden.
11. Vælg måneden for den salgsordre, du har oprettet, i sektionen **Dato** i oversigtspanelet **Parametre** i dialogboksen **Intrastat-rapport**.
12. Angiv indstillingen **Generer** **fil** til **Ja** i sektionen **Eksportindstillinger**. Angiv derefter det krævede navn i feltet **Filnavn**.
13. Angiv indstillingen **Generer rapport** til **Ja**. Angiv derefter det krævede navn i feltet **Rapportfilnavn**.
14. Vælg **Udførsel** i feltet **Retning**.
15. Vælg **OK**, og gennemse den rapport i .txt-format, der er oprettet. Følgende tabel viser værdierne i eksempelrapporten.

    | ISO-kode for partnerland | Transaktionsart | Varekode | Supplerende enhed | Tykkelse | Fakturabeløb |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Gennemse den rapport i Excel-format, der er genereret.

    ![Intrastat-rapport](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Kreditor** > **Indkøbsordrer** > **Alle indkøbsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Gå til dialogboksen **Opret indkøbsordre**, og vælg **DE-001** i feltet **Kreditorkonto**.
4. Vælg **OK**.
5. På fanen **Hoved** i oversigtspanelet **Udenrigshandel** skal du kontrollere, at feltet **Transaktionskode** er angivet til **1**.
6. Vælg **D0001** i feltet **Varenummer** i oversigtspanelet **Indkøbsordrelinjer** under fanen **Linjer**. Angiv derefter **6** i feltet **Antal**.
7. Vælg **Bekræft** i gruppen **Handlinger** under fanen **Indkøb** i handlingsruden.
8. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
9. Vælg **Standard fra** i handlingsruden. Vælg **Bestilt antal** i feltet **Standardmængde for linjer**. Vælg derefter **OK**.
10. Angiv **0001** i feltet **Nummer** i sektionen **Fakturaidentifikation** i oversigtspanelet **Kreditorfakturahoved**.
11. Vælg **Bogfør** i handlingsruden for at bogføre kladden.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Oprette en Intrastat-opgørelse for modtagelser

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Overfør** i handlingsruden.
3. Angiv indstillingen **Kreditorfaktura** til **Ja** i dialogboksen **Intrastat (Overførsel)**.
4. Vælg **OK** for at overføre transaktionerne og gennemse Intrastat-kladden.

    ![Intrastat-kladde for indkøbsordre](media/swe_intrastat_journal_purchase_order.png)

5. Gennemse fanen **Generelt** for indkøbsordren.

    ![Intrastat-kladdelinjeoplysninger for indkøbsordre](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Vælg **Output** > **Rapport** i handlingsruden.
7. Vælg måneden for den salgsordre, du har oprettet, i sektionen **Dato** i oversigtspanelet **Parametre** i dialogboksen **Intrastat-rapport**.
8. Angiv indstillingen **Generer** **fil** til **Ja** i sektionen **Eksportindstillinger**. Angiv derefter det krævede navn i feltet **Filnavn**.
9. Angiv indstillingen **Generer rapport** til **Ja**. Angiv derefter det krævede navn i feltet **Rapportfilnavn**.
10. Vælg **Indførsel** i feltet **Retning**.
11. Vælg **OK**, og gennemse den rapport i .txt-format, der er oprettet. Følgende tabel viser værdierne i eksempelrapporten.

    | ISO-kode for partnerland | Transaktionsart | Varekode | Supplerende enhed | Tykkelse | Fakturabeløb |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Gennemse den rapport i Excel-format, der er genereret.

    ![Rapport for Intrastat-modtagelser](media/swe_intrastat_arrivals_report.png)
