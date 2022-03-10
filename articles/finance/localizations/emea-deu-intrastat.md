---
title: Tysk Intrastat
description: Dette emne indeholder oplysninger om Intrastat-opgørelse i Tyskland.
author: anasyash
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 50c412fdfd7118843d285cbb70e8e44847c9d4a5
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2021
ms.locfileid: "7487919"
---
# <a name="german-intrastat"></a>Tysk Intrastat

[!include [banner](../includes/banner.md)]

Siden **Intrastat** bruges til at generere og rapportere oplysninger om handel mellem EU-lande. Den tyske Intrastat-opgørelse indeholder oplysninger om varehandel til indberetning. Rapporten formateres i overensstemmelse med de retningslinjer, der er angivet af de tyske myndigheder, som er vist på siden [6.2 Filerklæringer i INSTAT/XML-format](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html).

Følgende tabel viser de felter, der findes i den tyske Intrastat-opgørelse.

| Felter | Udførsel | Indførsel |
|-------------------------|-------------------------|-------------------------|
| Referenceperiode | X | X |
| Retningskode | X | X |
| Intrastat-opgørelsesvaluta</br>**Bemærk:** Denne valuta er <em>regnskabsvalutaen</em>. | X | X |
| Varekode | X | X |
| Varenavn | X | X |
| Kode for supplerende enhed | X | X |
| Medlemsstat for konsignation/destination | X | X |
| Nettomasse | X | X |
| Antal i supplerende enheder | X | X |
| Oprindelsesland |  | X |
| Fakturabeløb | X |  |
| Statistisk værdi | X | X |
| Arten af transaktioner | X | X |
| Transportmåde | X | X |
| Lande-/områdekode</br>**Note:**</br><ul></br><li>Hvis oprindelseslandet eller -området er Tyskland, og fakturaen er til udførsler, vises en Intrastat-kode for oprindelseslandet.</li></br><li>Hvis oprindelseslandet eller -området ikke er Tyskland, og fakturaen er til udførsler, vises kode **99**.</li></br><li>Hvis fakturaen er til indførsler, vises en Intrastat-kode for staten.</li></br></ul> | X | X |
| Havnekode for havn/lufthavn/indland | X | X |
| Leveringsbetingelse | X | X |


## <a name="set-up-intrastat"></a>Konfigurere Intrastat

1. Konfigurer firmaets koder.

    1. Gå til **Organisationsadministration** > **Organisationer** > **Juridiske enheder**.
    2. Angiv Id for udvekslingsaftale i feltet **DVR** i afsnittet **Identifikation** i oversigtspanelet **Udenrigshandel og logistik**. Dette id medtages i rapporten.
    3. I feltet **Eksport med momsfritagelsesnummer** skal du angive firmaets momsnummer til eksport.
    4. I feltet **Import med momsfritagelsesnummer** skal du angive firmaets momsnummer til import.
    5. Angiv den Intrastat-kode, der er tildelt den juridiske enhed, i feltet **Intrastat-kode**.
    6. I oversigtspanelet **Momsregistrering** skal du i feltet **Momsregistreringsnummer** angive din virksomheds momsregistreringsnummer.

    > [!NOTE]
    > Hvis du genererer en Intrastat-rapport til associerede selskaber, skal du angive dit moderselskabs momsregistreringsnummer i feltet **Momsregistreringsnummer**.

2. I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) i det delte aktivbibliotek kan du hente de seneste versioner af følgende ER-konfigurationer (ER – Electronic Reporting) til Intrastat-opgørelsen.

    - Intrastat-modul
    - Intrastat-rapport
    - INSTAT XML
    - INSTAT XML (DE)

3. Konfigurere udenrigshandelsparametre:

    1. Gå i Dynamics 365 Finance til **Moms** > **Opsætning** > **Parametre for udenrigshandel**.
    2. Under fanen **Intrastat** skal du i feltet **Tilknytning af filformat** vælge **Intrastat XML (DE)** i oversigtspanelet **Elektronisk rapportering**.
    3. Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.
    4. Vælg **Intrastat** i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
    5. I feltet **Transaktionskode** skal du vælge transaktionskoden for egenskabsoverførsler. Denne kode bruges til transaktioner, der opretter faktiske eller planlagte overførsler af egenskab mod kompensation (økonomisk eller anden). Du kan også bruge den til rettelser.
    6. I feltet **Kreditnota** skal du vælge transaktionskoden for returnering af varer.
    7. Vælg kontaktpersonen til Intrastat-rapporten i feltet **Arbejder**. Alternativt kan du angive eller vælge værdier i felterne **Navn**, **Telefon**, **Fax**, **Mail** og **Internetadresse** under fanen **Kontakt**. Disse felter medtages i rapporten.
    8. Vælg Intrastat-myndigheden i feltet **Myndighed**.
    9. Gå til **Moms** > **Indirekte moms** > **Salgsmoms** > **Momsmyndigheder**, og angiv følgende oplysninger for den Intrastat-myndighed, du valgte i det forrige trin:

       - Myndighedsidentifikation
       - Adressering
       - Kontaktpersonoplysninger

    10. Under fanen **Lande-/områdeegenskaber** indeholder feltet **Land/område** alle de lande eller områder, som dit firma handler med. For hvert land eller område skal du vælge **EU** i feltet **Lande-/områdetype**, så landet eller området vises i Intrastat-rapporten.

4. Konfigurere områdekoder.

    1. Gå til **Organisationsadministration** > **Globalt adressekartotek** > **Adresser** > **Adresseopsætning**.
    2. Vælg **DEU** i feltet **Land/område** under fanen **Delstat eller provins**, og vælg derefter **Anvend filter**.
    3. Vælg staten i gitteret. I feltet **Intrastat-kode** skal du angive den entydige Intrastat-kode.

5. Konfigurer oprindelsesadressen for et produkt.

    1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
    2. Vælg produktet i gitteret.
    3. Vælg **DEU** i feltet **Oprindelsesland** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.

6. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Komprimering for Intrastat**, og vælg de felter, der skal sammenlignes, når Intrastat-oplysninger opsummeres. Vælg følgende felter til for tysk Intrastat:

    - Varekode
    - Land/område
    - Rettelse
    - Vej
    - Leveringsbetingelse
    - Fakturaer
    - Oprindelsesland/-område
    - Havn
    - Afsenderland/-område
    - Afsenders stat
    - Statistisk procedure
    - Transaktionsart
    - Transporter
    - SE-nummer

### <a name="intrastat-transfer"></a>Intrastat-overførsel

På siden **Intrastat** i handlingsruden kan du vælge **Overfør** for automatisk at overføre oplysninger om samhandel med andre steder fra salgsordrer, fritekstfakturaer, indkøbsordrer, kreditorfakturaer, produktkvittering for kreditorer **,** projektfakturaer og flytteordrer. Det er kun dokumenter, hvor et EU-land er destinationsland eller -område (til afsendelser) eller forsendelse (til modtagelser), der overføres.

Du kan også angive posteringer manuelt ved at vælge **Ny** i handlingsruden.

### <a name="generate-an-intrastat-report"></a>Generere en Intrastat-rapport

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Output** > **Rapport** i handlingsruden.
3. I dialogboksen **Intrastat-rapport** skal du angive følgende felter.

    | Felt | Betegnelse |
    |-------------------------|-------------------------|
    | Fra-dato | Vælg startdatoen for rapporten. |
    | Til-dato | Vælg slutdatoen for rapporten. |
    | Generer fil | Angiv denne indstilling til **Ja** for at generere en .xml-fil. |
    | Filnavn | Lad feltet være tomt. Filnavnet genereres automatisk og består af værdien af XML-koden **&lt;envelopeIdl&gt;** plus filtypenavnet **.xml**.</br>Værdien **&lt;envelopeId&gt;** er en sammentrækning af følgende elementer i denne rækkefølge:</br><ol type="1"></br><li>Værdien af koden **&lt;interchangeAgreementId&gt;**</li></br><li>En bindestreg (-)</li></br><li>Værdien af koden **&lt;referencePeriod in YYYYMM&gt;**</li></br><li>En bindestreg (-)</li></br><li>Værdien af koden **&lt;Envelope/DateTime/date in YYYYMMDD&gt;**</li></br><li>En bindestreg (-)</li></br><li>Værdien af koden **&lt;Envelope/DateTime/time in hhmm&gt;**</li></br></ol> |
    | Vej | <ul></br><li>Vælg **Indførsel** for at indberette om indførsler inden for fællesskabet.</li></br><li>Vælg **Udførsel** for at indberette udførsler inden for fællesskabet.</li></br><li>Vælg **Begge** for at indberette både indførsler og udførsler inden.</li></br></ul> |
    | SE-nummer | Angiv det registreringsnummer, der skal bruges til at generere afsenderens identifikationskode, hvis nummeret afviger fra den juridiske enheds momsregistreringsnummer. |


## <a name="example"></a>Eksempel

Dette eksempel viser, hvordan du bogfører indførsler og udførsler til Intrastat. Det bruger den juridiske enhed **DEMF**.

1. I [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)skal du i det delte aktivbibliotek hente de seneste versioner af følgende ER-konfigurationer til Intrastat-opgørelsesformat:

    - Intrastat-modul
    - Intrastat-rapport
    - Intrastat-XML
    - Intrastat-XML (DE)

2. Opret transaktionskoder.

    1. Gå til **Moms** > **Konfiguration** > **Udenrigshandel** > **Transaktionskoder**.
    2. Gå til handlingsruden, og vælg **Ny**.
    3. Angiv **21** i feltet **Transaktionskode**.
    4. I feltet **Navn** skal du angive **Returnering af varer**.
    5. Vælg **Gem** i handlingsruden.

3. Konfigurer myndighedens identifikationsnummer.

    1. Gå til **Moms** > **Indirekte skatter** > **Moms** > **Momsmyndigheder**.
    2. Vælg **TA** på listen.
    3. Indtast **123** i feltet **Myndighedens id**.

4. Konfigurere områdekoder.

    1. Gå til **Organisationsadministration** > **Globalt adressekartotek** > **Adresser** > **Adresseopsætning**.
    2. Vælg **DEU** i feltet **Land/område** under fanen **Delstat eller provins**, og vælg derefter **Anvend filter**.
    3. I gitteret skal du vælge **BE** og derefter angive **11** i feltet **Intrastat-kode**.
    4. Vælg **Gem** i handlingsruden.

5. Konfigurere udenrigshandelsparametre.

    1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Udenrigshandelsparametre**.
    2. Vælg **11** i feltet **Transaktionskode** i oversigtspanelet **Generelt** under fanen **Intrastat**.
    3. Vælg **21** i feltet **Kreditnota**.
    4. Vælg **TA** i feltet **Myndighed**.
    5. Vælg **INSTAT XML (DE)** i feltet **Tilknytning af filformat** i oversigtspanelet **Elektronisk rapportering**.
    6. Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.
    7. Sørg for, at **Intrastat** er valgt i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
    8. Vælg **Ny** under fanen **Egenskaber for land/område**.
    9. Vælg **FRA** i feltet **Land/område for part**.
    10. Vælg **EU** i feltet **Lande-/områdetype**.

6. Tildel et produkt en varekode, og angiv produktets oprindelse. Felterne **Varekode**, **Oprindelsesland/-område** og **Oprindelsesstat** angives derefter automatisk på salgsordrer og indkøbsordrer, når du vælger produktet.

    1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
    2. Vælg **D0001** i gitteret.
    3. Vælg **920 20 34** i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
    4. Vælg **DEU** i feltet **Land/område** i sektionen **Oprindelse**.
    5. Angiv **12** i feltet **Nettovægt** i sektionen **Vægtmålinger** i oversigtspanelet **Styr lager**.
    6. Vælg **Gem** i handlingsruden.

7. Knyt transport til en leveringsmåde. Transportkoden angives derefter automatisk på ordrer, når du vælger leveringsmåden.

    1. Gå til **Indkøb og forsyning** > **Opsætning** > **Distribution** > **Leveringsmåder**.
    2. Vælg **10** på listen .
    3. Vælg **01** i feltet **Transport** i oversigtspanelet **Udenrigshandel**.

8. Opret en salgsordre med en EU-kunde.

    1. Gå til **Debitor** > **Ordrer** > **Alle salgsordrer**.
    2. Gå til handlingsruden, og vælg **Ny**.
    3. I dialogboksen **Opret salgsordre** skal du i sektionen **Debitor** i feltet **Debitorkonto** i oversigtspanelet **Debitor** vælge **DE-012**.
    4. Vælg **1** i feltet **Websted** i sektionen **Lagringsdimensioner** i oversigtspanelet **Generelt**.
    5. Vælg **11** i feltet **Lagersted**.
    6. Vælg **OK**.
    7. Vælg **53** i feltet **Havn** i oversigtspanelet **Udenrigshandel** under fanen **Overskrift**.
    8. Vælg **31710** i feltet **Statistisk procedure**.
    9.  Vælg **D0001** i feltet **Varenummer** under fanen **Linjer** i oversigtspanelet **Salgsordrelinjer**. Angiv derefter **10** i feltet **Antal**.
    10. I oversigtspanelet **Linjedetaljer** skal du under fanen **Udenrigshandel** kontrollere, at felterne **Transaktionskode**, **Transport**, **Vare** og **Oprindelsesland/-område** er angivet automatisk.
    11. Vælg **Gem** i handlingsruden.
    12. Vælg **Faktura** i sektionen **Generér** under fanen **Faktura** i handlingsruden.
    13. I dialogboksen **Bogføringsfaktura** i oversigtspanelet **Parametre** i sektionen **Parameter** i feltet **Antal** skal du vælge **Alle**.
    14. Vælg **OK** for at bogføre fakturaen.

9.  Overfør transaktionen til Intrastat-kladden, og gennemse resultatet.

    1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
    2. Vælg **Overfør** i handlingsruden.
    3. Angiv indstillingen **Debitorfaktura** til **Ja** i sekionen **Parametre** i dialogboksen **Intrastat (Overførsel)**.
    4. Vælg **Filter**.
    5. Vælg den første linje i dialogboksen **Intrastat-filter** under fanen **Interval**, og kontrollér, at feltet **Felt** er angivet til **Dato**.
    6. Vælg dags dato i feltet **Kriterier**.
    7. Vælg **OK** for at lukke dialogboksen **Intrastat-filter**.
    8. Vælg **OK** for at lukke dialogboksen **Intrastat (Overførsel)** og gennemgå resultatet. Linjen repræsenterer den salgsordre, du har oprettet tidligere.

        ![Linje, der repræsenterer salgsordren på siden Intrastat](media/intrastat_deu_1.png)

10. Vælg transaktionslinjen, og vælg derefter fanen **Generelt** for at få vist flere detaljer.

    ![Salgsordredetaljer under fanen Generelt på Intrastat-siden](media/intrastat_deu_2.png)

11. Opret en kreditnota på baggrund af en salgsordre.

    1. Gå til **Debitor** > **Ordrer** > **Alle salgsordrer**.
    2. Gå til handlingsruden, og vælg **Ny**.
    3. I dialogboksen **Opret salgsordre** skal du i sektionen **Debitor** i feltet **Debitorkonto** i oversigtspanelet **Debitor** vælge **DE-012**.
    4. Vælg **1** i feltet **Websted** i sektionen **Lagringsdimensioner** i oversigtspanelet **Generelt**.
    5. Vælg **11** i feltet **Lagersted**.
    6. Vælg **53** i feltet **Havn** i oversigtspanelet **Udenrigshandel** under fanen **Overskrift**.
    7. Vælg **31710** i feltet **Statistisk procedure**.
    8. Vælg **D0001** i feltet **Varenummer** under fanen **Linjer** i oversigtspanelet **Salgsordrelinjer**. Angiv derefter **-2** i feltet **Antal**.
    9. Vælg **21** i feltet **Transaktionskode** i oversigtspanelet **Linjedetaljer** under fanen **Udenrigshandel**.
    10. Kontrollér, at felterne **Transport**, **Vare** og **Oprindelsesland/-område** er indstillet automatisk.
    11. Vælg **Gem** i handlingsruden.
    12. Vælg **Faktura** i sektionen **Generér** under fanen **Faktura** i handlingsruden.
    13. I dialogboksen **Bogføringsfaktura** i oversigtspanelet **Parametre** i sektionen **Parameter** i feltet **Antal** skal du vælge **Alle**.
    14. Vælg **OK** for at bogføre fakturaen.

12. Overfør transaktionen til Intrastat-kladden, og gennemse resultatet.

    1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
    2. Vælg **Overfør** i handlingsruden.
    3. Angiv indstillingen **Debitorfaktura** til **Ja** i sekionen **Parametre** i dialogboksen **Intrastat (Overførsel)**.
    4. Vælg **OK** for at lukke dialogboksen **Intrastat (Overførsel)** og gennemgå resultatet. Der er tilføjet en ny linje, hvor feltet **Retning** er indstillet til **Indførsel**.            
        Denne linje repræsenterer den fysiske returnering af varer.

        ![Linje for fysisk returnering af varer på Intrastat-siden](media/intrastat_deu_3.png)

13. Vælg transaktionslinjen, og vælg derefter fanen **Generelt** for at få vist flere detaljer.

    ![Detaljer om den fysiske returnering af varer under fanen Generelt på Intrastat-siden](media/intrastat_deu_4.png)

14. Opret en rettelse på baggrund af en salgsordre:

    1. Gå til **Debitor** > **Ordrer** > **Alle salgsordrer**.
    2. Gå til handlingsruden, og vælg **Ny**.
    3. I dialogboksen **Opret salgsordre** skal du i sektionen **Debitor** i feltet **Debitorkonto** i oversigtspanelet **Debitor** vælge **DE-012**.
    4. Vælg **1** i feltet **Websted** i sektionen **Lagringsdimensioner** i oversigtspanelet **Generelt**.
    5. Vælg **11** i feltet **Lagersted**.
    6. Vælg **53** i feltet **Havn** i oversigtspanelet **Udenrigshandel** under fanen **Overskrift**.
    7. Vælg **31710** i feltet **Statistisk procedure**.
    8. Vælg **D0001** i feltet **Varenummer** under fanen **Linjer** i oversigtspanelet **Salgsordrelinjer**. Angiv derefter **-3** i feltet **Antal**.
    9. Vælg **11** i feltet **Transaktionskode** i oversigtspanelet **Linjedetaljer** under fanen **Udenrigshandel**.
    10. Kontrollér, at felterne **Transport**, **Vare** og **Oprindelsesland/-område** er indstillet automatisk.
    11. Vælg **Gem** i handlingsruden.
    12. Sørg for, at feltet **Transaktionskode** er angivet til 11.
    13. Vælg **Faktura** i sektionen **Generér** under fanen **Faktura** i handlingsruden.
    14. I dialogboksen **Bogføringsfaktura** i oversigtspanelet **Parametre** i sektionen **Parameter** i feltet **Antal** skal du vælge **Alle**.
    15. Vælg **OK** for at bogføre fakturaen.

15. Overfør transaktionen til Intrastat-kladden, og gennemse resultatet:

    1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
    2. Vælg **Overfør** i handlingsruden.
    3. Angiv indstillingen **Debitorfaktura** til **Ja** i sekionen **Parametre** i dialogboksen **Intrastat (Overførsel)**.
    4. Vælg **OK** for at lukke dialogboksen **Intrastat (Overførsel)** og gennemgå resultatet. Der er tilføjet en ny linje, hvor kolonnen **Rettelse** nu er markeret.

        ![Linje for rettelsen på Intrastat-siden](media/intrastat_deu_5.png)

16. Vælg transaktionslinjen, og vælg derefter fanen **Generelt** for at få vist flere detaljer.

    ![Detaljer om rettelse under fanen Generelt på Intrastat-siden](media/intrastat_deu_6.png)

17. Vælg **Output** > **Rapport** i handlingsruden.
18. Vælg måneden for den salgsordre, du har oprettet, i sektionen **Dato** i oversigtspanelet **Parametre** i dialogboksen **Intrastat-rapport**.
19. Angiv indstillingen **Generer** **fil** til **Ja** i sektionen **Eksportindstillinger**.
20. Angiv det krævede navn i feltet **Filnavn**.
21. Vælg **OK**, og gennemse den rapport, der er oprettet. Følgende tabel viser værdierne i eksempelrapporten.

    | **Navn**                  | **Salgsfaktura**  |   **Rettelse**   | **Kreditnota** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | N                  | T                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | Speaker            | Speaker            | Speaker         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

