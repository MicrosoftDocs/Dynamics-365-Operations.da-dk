---
title: Bogføre modtagelser og afsendelser for Intrastat
description: Dette emne indeholder et eksempel, som viser, hvordan du bogfører modtagelser og afsendelser for Intrastat.
author: anasyash
ms.date: 8/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 4ab4402740d199043519773b18732bdde9a0fb2f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724777"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>Bogføre modtagelser og afsendelser for Intrastat

[!include [banner](../includes/banner.md)]

Dette emne indeholder et eksempel, som viser, hvordan du bogfører modtagelser og afsendelser for Intrastat. I eksemplet bruges den juridiske enhed **ITCO**.

## <a name="setup"></a>Konfiguration

1. Importer den seneste version af følgende ER-konfigurationer (Elektronisk rapportering):

    - Intrastat-modul
    - Intrastat-rapport
    - Intrastat (IT)

    Find flere oplysninger under [Downloade ER-konfigurationer fra det globale lager i konfigurationstjeneste](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. I Microsoft Dynamics 365 Finance skal du definere følgende nummerserier som fortløbende: **Gene\_397**, **Acco\_16403**, **Gene\_407** og **PUR\_EU**.

    1. Gå til **Organisationsadministration** > **Nummerserier** > **Nummerserier**.
    2. Vælg en af nummerseriekoderne i gitteret.
    3. Vælg **Rediger** i handlingsruden.
    4. I sektionen **Opsætning** i oversigtspanelet **Generelt** skal du angive indstillingen **Fortløbende** til **Ja**.
    5. Vælg **Gem** i handlingsruden.

3. Angiv en lagerstedsadresse.

    1. Gå til **Warehouse Management** &gt; **Konfiguration** &gt; **Lagersted** &gt; **Lagersteder**.
    2. Vælg lagerstedet **11** på listen.
    3. Vælg **Tilføj** i oversigtspanelet **Adresse**.
    4. Angiv **Hoved** i feltet **Navn** **eller** **beskrivelse** i dialogboksen **Ny** **adresse**.
    5. Vælg **ITA (Italien)** i feltet **Land/område**.
    6. Vælg **Aprilia** i feltet **By**.
    7. Vælg **OK**.

4. Konfigurer transaktionskoder.

    1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Transaktionskoder**.
    2. Vælg **Ny**, og konfigurer en transaktionskode for egenskabsoverførsler.

        - Angiv **1** i feltet **Transaktionskode**.
        - Skriv **Overførsel af egenskab** i feltet **Navn**.

    3. Vælg **Ny**, og konfigurer en transaktionskode for returneringer.

        - Angiv **2** i feltet **Transaktionskode**.
        - I feltet **Navn** skal du angive **Returnering af varer**.

5.  Konfigurere udenrigshandelsparametre.

    1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Udenrigshandelsparametre**.
    2. Vælg **1** i feltet **Transaktionskode** i oversigtspanelet **Generelt** under fanen **Intrastat**.
    3. Vælg **2** i feltet **Kreditnota**.
    4. I feltet **Salgsrapporteringsperiode** skal du vælge **Måned**.
    5. I feltet **Indkøbsrapporteringsperiode** skal du vælge **Måned**.
    6. Vælg **Intrastat (IT)** i feltet **Tilknytning af filformat** i oversigtspanelet **Elektronisk rapportering**.
    7. Vælg **Intrastat-rapport** i feltet **Tilknytning af rapporteringsformat**.
    8. Vælg **Intrastat** i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
    9. Angiv indstillingen **Udskriv og eksportér statistiske data** til **Ja** i oversigtspanelet **Statistisk værdi**.
    10. Kontrollér, at følgende linjer findes, under fanen **Egenskaber for land/område**.

        | **Part/land/område** | **Intrastat-kode** | **Valuta** | **Lande-/områdetype** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Indland                |
        | SMR                      | SM                 | EUR          | Speciel indenlandsk        |

    11. Vælg **Ny** på værktøjslinjen for at oprette følgende linje.

        | **Part/land/område** | **Intrastat-kode** | **Valuta** | **Lande-/områdetype** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | EU                      |

6. Konfigurer SE-numre.

    1. Gå til **Moms** > **Opsætning** > **Moms** > **SE-numre**.
    2. Vælg **Ny** i handlingsruden for at oprette følgende linjer.

        | **Land/område** | **SE-nummer** | **Firmanavn** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE-KREDITOR        |
        | DNK                | DK0987654321          | Debitor-ER      |

7. Angiv kreditorens adresse.

    1. Gå til **Kreditor** &gt; **Kreditorer** &gt; **Alle kreditorer**.
    2. Vælg **UE-kreditor** i gitteret.
    3. Vælg **Tilføj** i oversigtspanelet **Adresser**.
    4. Angiv **Tyskland** i feltet **Navn eller beskrivelse** i dialogboksen **Ny adresse**.
    5. Vælg **DEU** i feltet **Land/område**.
    6. Vælg **OK** for at oprette den nye adresse.
    7. Vælg **Alle** og derefter **1234567890** i feltet **Momsfritagelsesnummer** i sektionen **Moms** i oversigtspanelet **Faktura og levering**.
    8. Vælg **Gem** i handlingsruden.

8. Angiv kundeadresser.

    1. Gå til **Debitor** > **Kunder** > **Alle kunder**.
    2. Vælg **ITCO-000001** i gitteret.
    3. Vælg **Rediger** i oversigtspanelet **Adresser**.
    4. Angiv **San Marino** i feltet **Navn eller beskrivelse** i dialogboksen **Ny adresse**.
    5. Vælg **SMR** i feltet **Land/område**.
    6. Vælg **OK** for at oprette den nye adresse.
    7. Vælg **ITCO-000001** i feltet **Fakturakonto** i sektionen **Faktura** i oversigtspanelet **Faktura og levering**.
    8. I feltet **Nummerseriegruppe** skal du vælge **IT\_VENDOM**.
    9. Vælg **Gem** i handlingsruden, og luk siden.
    10. Vælg **ITCO-000002** i gitteret på siden **Alle kunder**.
    11. Vælg **Tilføj** i oversigtspanelet **Adresser**.
    12. Angiv **Danmark** i feltet **Navn eller beskrivelse** i dialogboksen **Ny adresse**.
    13. Vælg **DNK** i feltet **Land/område**.
    14. Vælg **OK** for at oprette den nye adresse.
    15. Vælg **DKK** i feltet **Valuta** i oversigtspanelet **Demografi for salg**.
    16. Vælg **IT\_PUREU** i feltet **Momsgruppe** i sektionen **Moms** i oversigtspanelet **Faktura og levering**.
    17. Vælg **Alle** og derefter **DK0987654321** i feltet **SE-nummer**.
    18. Vælg **Gem** i handlingsruden.

9. Konfigurer kategorihierarkiet.

    1. Gå til **Administration af produktoplysninger** > **Opsætning** > **Kategorier og attributter** > **Kategorihierarkier**.
    2. Vælg **Intrastat** i gitteret.
    3. Vælg **Ny kategorinode** i handlingsruden.
    4. I feltet **Navn** skal du angive **Tjeneste**.
    5. Angiv **123456** i feltet **Kode**.
    6. Vælg **Gem** i handlingsruden.

10. konfigurer produkter.

    1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
    2. Vælg **ITEM** i gitteret.
    3. Vælg **ITCO-000001** i feltet **Kreditor** i sektionen **Administration** i oversigtspanelet **Indkøb**.
    4. Vælg **\[100 200 30\] Højttaler** i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
    5. Vælg **DEU** i feltet **Land/område** i sektionen **Oprindelse**.
    6. I feltet **Område** skal du vælge **BE**.
    7. Angiv **5** i feltet **Nettovægt** i sektionen **Nettomålinger** i oversigtspanelet **Styr lager**.
    8. Vælg **Gem** i handlingsruden.
    9. Vælg **Servicevare** i gitteret på siden **Frigivne produkter**.
    10. Vælg **\[123456\] Tjeneste** i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
    11. Vælg **Gem** i handlingsruden.

11. Konfigurer transportmetoder.

    1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Transportmetode**.
    2. Vælg **Ny** i handlingsruden for at oprette følgende transportmetoder.

        | **Transporter** | **Beskrivelse** |
        |---------------|-----------------|
        | 1             | Vej            |
        | 2             | Luft             |

12. Konfigurer en leveringsmåde.

    1. Gå til **Indkøb og forsyning** > **Opsætning** > **Distribution** > **Leveringsmåder**.
    2. Gå til handlingsruden, og vælg **Ny**.
    3. Angiv **1** i feltet **Leveringsmåde**.
    4. Indtast **Lastvogn** i feltet **Beskrivelse**.
    5. Vælg **1 Vej** i feltet **Transport** i oversigtspanelet **Udenrigshandel**.
    6. Vælg **Gem** i handlingsruden.

13. Konfigurer leveringsbetingelser.

    1. Gå til **Kreditor** > **Opsætning** > **Leveringsbetingelser**.
    2. Vælg **CFR** på listen .
    3. Angiv **1** i feltet **Intrastat-kode** i oversigtspanelet **Generelt**.

## <a name="post-arrivals-for-intrastat"></a>Bogføre modtagelser for Intrastat

### <a name="purchase-goods-by-using-a-purchase-order"></a>Købe varer ved hjælp af en indkøbsordre

I denne del af eksemplet vises det, hvordan du kan bruge en indkøbsordre til at købe varer fra EU-lande.

1. Gå til **Kreditor** > **Indkøbsordrer** > **Alle indkøbsordrer**.
2.  Gå til handlingsruden, og vælg **Ny**.
3.  Gå til dialogboksen **Opret indkøbsordre**, og vælg **UE-kreditor** i feltet **Kreditorkonto**.
4.  Vælg **it** i feltet **Sprog** i oversigtspanelet **Administration**.
5.  Vælg **OK**.
6.  I visningen **Hoved** i oversigtspanelet **Udenrigshandel** skal du kontrollere, at feltet **Transaktionskode** er angivet til **1**.
7.  Kontrollér, at feltet **Land/område for oprindelse/destination** er angivet til **RM**.
8.  Vælg **1** i feltet **Leveringsmåde** i sektionen **Levering** i oversigtspanelet **Levering**.
9.  Vælg **CFR** i feltet **Leveringsbetingelser**.
10. Vælg **Vare** i feltet **Varenummer** i oversigtspanelet **Indkøbsordrelinjer** i visningen **Linjer**.
11. Vælg **1** i feltet **Sted**.
12. Vælg **11** i feltet **Lagersted**.
13. Angiv **10** i feltet **Antal**.
14. Indtast **100** i feltet **Enhedspris**.
15. Vælg **22%EU** i feltet **Varemomsgruppe** i sektionen **Moms** under fanen **Opsætning**.
16. Vælg **Bekræft** i gruppen **Handlinger** under fanen **Indkøb** i handlingsruden.
17. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
18. Vælg **Standard fra** i handlingsruden.
19. Vælg **Bestilt antal** i feltet **Standardmængde for linjer**, og vælg derefter **OK**.
20. Angiv **0001** i feltet **Nummer** i sektionen **Fakturaidentifikation** i oversigtspanelet **Kreditorfakturahoved**.
21. Vælg **7/9/2021** i feltet **Fakturadato** i sektionen **Fakturadatoer**.
22. Vælg **Bogfør** i handlingsruden for at bogføre kladden.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Købe tjenester ved hjælp af en kreditorfaktura

I denne del af eksemplet vises det, hvordan du kan bruge en kreditorfaktura til at købe tjenester fra EU-lande.

1. Gå til **Kreditor** > **Fakturaer** > **Fakturakladde**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Vælg **VEND\_EUINV** i feltet **Navn**.
4. Vælg **Linjer** i handlingsruden.
5. Angiv **7/9/2021** i feltet **Dato**.
6. Vælg **Kreditor** i feltet **Kontotype**.
7. Vælg **UE-kreditor** i feltet **Konto**.
8. Vælg **7/9/2021** i feltet **Fakturadato**.
9. Angiv **ITA-0004** i feltet **Faktura**.
10. Angiv **120000** i feltet **Kredit**.
11. Vælg **Finans** i feltet **Modkontotype**.
12. Vælg **110130** i feltet **Modkonto**.
13. Vælg **IT\_PUREU** i feltet **Momsgruppe**.
14. Vælg **22%EU** i feltet **Varemomsgruppe**.
15. Følg disse trin på fanen **Udenrigshandel**:

    1. Vælg **1** i feltet **Transaktionskode**.
    2. Vælg **2 Fly** i feltet **Transport**.
    3. Vælg **\[123456\] Tjeneste** i feltet **Vare**.
    4. Vælg **ITA** i feltet **Land/område**.
    5. Vælg **LAZ** i feltet **Område**.
    6. Vælg **LT** i feltet **Land/område for oprindelse/destination**.


16. Vælg **Bogfør** i handlingsruden.
17. Opret en Intrastat-opgørelse for modtagelser.

    1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
    2. Vælg **Overfør** i handlingsruden.
    3. Angiv indstillingen **Kreditorfaktura** til **Ja** i dialogboksen **Intrastat (Overførsel)**.
    4. Vælg **OK** for at overføre transaktionerne, og gennemse derefter Intrastat-kladden.

   ![Intrastat-kladdeside, fanen Oversigt.](media/ita_intrastat_journal_vendor_invoice.png)

18. Gennemse fanen **Generelt** for indkøbsordren.

    ![Intrastat-kladdelinjeoplysninger for indkøbsordre](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Gennemse fanen **Generelt** for kreditorfakturaen.

    ![Intrastat-kladdelinjeoplysninger for kreditorfaktura](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Generere Intrastat-rapport for modtagelser.

    1. Vælg **Output** > **Rapport** i handlingsruden.
    2. Vælg **7/1/2021** i feltet **Fra dato** i sektionen **Dato** i dialogboksen **Intrastat-rapport**.
    3. Vælg **7/31/2021** i feltet **Til dato**.
    4. Angiv indstillingerne **Generer fil** og **Generer rapport** til **Ja** i sektionen **Eksportindstillinger**.
    5. Angiv **Modtagelsesfil** i feltet **Filnavn**.
    6. Angiv **Modtagelsesrapport** i feltet **Rapportfilnavn**.
    7. Vælg **Indførsel** i feltet **Retning**.
    8. Angiv **123456** i feltet **Referencenummer**.
    9. Vælg **OK** for at generere Intrastat-rapporten og Intrastat-filen, og gennemse dem.

    Følgende illustration viser et eksempel på en Intrastat-rapport.

    ![Rapport for Intrastat-modtagelser.](media/ita_intrastat_arrivals_report.png)

    Følgende illustration viser et eksempel på en Intrastat-fil.

    ![Fil for Intrastat-modtagelser.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Bogføre afsendelser for Intrastat

### <a name="sell-goods-by-using-a-sales-order"></a>Sælge varer ved hjælp af en salgsordre

I denne del af eksemplet vises det, hvordan du kan bruge en salgsordre til at sælge varer til EU-lande.

1. Gå til **Debitor** > **Ordrer** > **Alle salgsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Gå til dialogboksen **Opret salgsordre**, og vælg **ITCO-000002** i feltet **Debitorkonto**.
4. Vælg **OK**.
5. Vælg **1 Lastvogn** i feltet **Leveringsmåde** i sektionen **Diverse leveringsoplysninger** i oversigtspanelet **Levering** i visingen **Hoved**.
6. Vælg **CFR** i feltet **Leveringsbetingelser**.
7. Vælg **ITEM** i feltet **Varenummer** i oversigtspanelet **Salgsordrelinjer** i visningen **Linjer**.
8. Angiv **50** i feltet **Antal**.
9. Vælg **1** i feltet **Sted**.
10. Vælg **11** i feltet **Lagersted**.
11. Indtast **250** i feltet **Enhedspris**.
12. Vælg **22%EU** i feltet **Varemomsgruppe** i sektionen **Moms** i oversigtspanelet **Linjedetaljer** under fanen **Opsætning**.
13. Vælg **Gem** i handlingsruden.
14. I handlingsruden under fanen **Faktura** i gruppen **Generer** skal du vælge **Faktura** for at oprette fakturaen for ordren.
15. I dialogboksen **Bogføringsfaktura** i oversigtspanelet **Parametre** i sektionen **Parameter** i feltet **Antal** skal du vælge **Alle**.
16. Vælg **7/9/2021** i feltet **Fakturadato** i oversigtspanelet **Opsætning**.
17. Vælg **OK**.
18. Gennemse linjerne i Intrastat-kladden.

    1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
    2. Vælg **Overfør** i handlingsruden.
    3. Angiv indstillingen **Debitorfaktura** til **Ja** i dialogboksen **Intrastat (Overførsel)**.
    4. Vælg **OK** for at overføre transaktionerne og gennemse Intrastat-kladden. Kreditnotaposteringen markeres som en rettelse og har et negativt fakturabeløb.

        ![Intrastat-kladdeside](media/ita_intrastat_journal_sales_order.png)

        ![Intrastat-kladdelinjeoplysninger for salgsordre](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Returnere varer ved hjælp af en kreditnota

I denne del af eksemplet vises det, hvordan du kan bruge en kreditnota til at returnere varer fra EU-lande.

1. Gå til **Debitor** > **Ordrer** > **Alle salgsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Gå til dialogboksen **Opret salgsordre**, og vælg **ITCO-000002** i feltet **Debitorkonto**.
4. Vælg **OK**.
5. Vælg **1 Lastvogn** i feltet **Leveringsmåde** i sektionen **Diverse leveringsoplysninger** i oversigtspanelet **Levering** i visingen **Hoved**.
6. Vælg **CFR** i feltet **Leveringsbetingelser**.
7. Vælg **2** i feltet **Transaktionskode** i oversigtspanelet **Udenrigshandel**.
8. Vælg **ITEM** i feltet **Varenummer** i oversigtspanelet **Salgsordrelinjer** under fanen **Linjer**.
9. Angiv **-10** i feltet **Antal**.
10. Vælg **1** i feltet **Sted**.
11. Vælg **11** i feltet **Lagersted**.
12. Indtast **250** i feltet **Enhedspris**.
13. Vælg **22%EU** i feltet **Varemomsgruppe** i sektionen **Moms** i oversigtspanelet **Linjedetaljer** under fanen **Opsætning**.
14. Vælg det parti, du oprettede tidligere, i feltet **Retur parti-id** i sektionen **Returordre**.
15. Vælg **Gem** i handlingsruden.
16. I handlingsruden under fanen **Faktura** i gruppen **Generer** skal du vælge **Faktura** for at oprette fakturaen for ordren.
17. Vælg **Alle** i feltet **Antal** i sektionen **Parameter** i oversigtspanelet **Parametre**.
18. Vælg **7/9/2021** i feltet **Fakturadato** i oversigtspanelet **Opsætning** i dialogboksen **Bogføring af faktura**.
19. Vælg **OK** for at bogføre fakturaen.
20. Gennemse linjerne i Intrastat-kladden.

    1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
    2. Vælg **Overfør** i handlingsruden.
    3. Angiv indstillingen **Debitorfaktura** til **Ja** i dialogboksen **Intrastat (Overførsel)**.
    4. Vælg **OK** for at overføre transaktionerne og gennemse Intrastat-kladden. Kreditnotaposteringen markeres som en rettelse og har et negativt fakturabeløb.

    ![Kreditnota for Intrastat-kladde](media/ita_intrastat_journal_credit_note.png)

    ![Intrastat-kladdelinjeoplysninger for kreditnota](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Sælge varer til San Marino ved hjælp af en salgsordre

I denne del af eksemplet vises det, hvordan du kan bruge en salgsordre til at købe varer fra San Marino.

1. Gå til **Debitor** > **Ordrer** > **Alle salgsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Gå til dialogboksen **Opret salgsordre**, og vælg **ITCO-000001** i feltet **Debitorkonto**.
4. Vælg **OK**.
5. Vælg **1** i feltet **Leveringsmåde** i sektionen **Diverse leveringsoplysninger** i oversigtspanelet **Levering** i visingen **Hoved**.
6. Vælg **CFR** i feltet **Leveringsbetingelser**.
7. Vælg **ITEM** i feltet **Varenummer** i oversigtspanelet **Salgsordrelinjer** under fanen **Linjer**.
8. Angiv **30** i feltet **Antal**.
9. Vælg **1** i feltet **Sted**.
10. Vælg **11** i feltet **Lagersted**.
11. Indtast **200** i feltet **Enhedspris**.
12. Vælg **Gem** i handlingsruden.
13. I handlingsruden under fanen **Faktura** i gruppen **Generer** skal du vælge **Faktura** for at oprette fakturaen for ordren.
14. Vælg **Alle** i feltet **Antal** i sektionen **Parameter** i oversigtspanelet **Parametre**.
15. Vælg **7/9/2021** i feltet **Fakturadato** i oversigtspanelet **Opsætning** i dialogboksen **Bogføring af faktura**.
16. Vælg **OK** for at bogføre fakturaen.
17. Gennemse linjerne i Intrastat-kladden.

    1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
    2. Vælg **Overfør** i handlingsruden.
    3. Angiv indstillingen **Debitorfaktura** til **Ja** i dialogboksen **Intrastat (Overførsel)**.
    4. Vælg **OK** for at overføre transaktionerne og gennemse Intrastat-kladden.

   ![Intrastat-kladde for San Marino](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![Intrastat-kladdelinjeoplysninger for San Marino](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Opret en Intrastat-opgørelse for afsendelser.

    1. Gå til **Moms** &gt; **Opgørelser** &gt; **Udenrigshandel** &gt; **Intrastat**.
    2. Vælg **Output** &gt; **Rapport** i handlingsruden.
    3. Vælg **7/1/2021** i feltet **Fra dato** i sektionen **Dato** i dialogboksen **Intrastat-rapport**.
    4. Vælg **7/31/2021** i feltet **Til dato**.
    5. Angiv indstillingerne **Generer fil** og **Generer rapport** til **Ja** i sektionen **Eksportindstillinger**.
    6. Angiv **Afsendelsesfil** i feltet **Filnavn**.
    7. Angiv **Afsendelsesrapport** i feltet **Rapportfilnavn**.
    8. Vælg **Udførsel** i feltet **Retning**.
    9. Angiv **98754** i feltet **Referencenummer**.
    10. Vælg **OK** for at generere Intrastat-rapporten og Intrastat-filen.

        Følgende illustration viser et eksempel på en udskrevet Intrastat-rapport.

        ![Intrastat-rapport](media/ita_intrastat_report_for_dispatches.png)

        Følgende illustration viser et eksempel på en udskrevet Intrastat-fil.

        ![Intrastat-fil for afsendelser](media/ita_intrastat_file_for_dispatches.png)
