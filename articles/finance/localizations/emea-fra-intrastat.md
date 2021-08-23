---
title: Fransk Intrastat
description: Dette emne indeholder oplysninger om Intrastat-opgørelse i Frankrig.
author: andosip
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: d38169d73caf93a0f81e832293916c9e54855a1848fe6ab409a670a4bf707b7c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713130"
---
# <a name="french-intrastat"></a>Fransk Intrastat

[!include[banner](../includes/banner.md)]

Virksomheder i Frankrig, som er registreret for moms, og som handler med andre EU-lande, skal indberette udvekslingen af varer og tjenester til og fra Frankrig. Declaration d'exchanges de Biens (Opgørelse af varehandel) eller DEB er en kombination af EU-listesystemet og Intrastat-rapporten. Du skal indsende denne rapport hver måned for alt varesalg inden for fællesskabet.

Du kan generere DEB-rapporten i et af to elektroniske tekstfilformater: SAISUNIC 330 eller INTRACOM.

Følgende tabel viser de felter, der er medtaget i den franske Intrastat-opgørelse i SAISUNIC 330-format.

| **Felt**                   | **Rapportniveau**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (forenklet)** | **1 (fuldt)** |
| Referenceperiode         | X                  | X            |
| Opgørelsesnummer       | X                  | X            |
| Linjenummer                 | X                  | X            |
| ISO-landekode (FR)       | X                  | X            |
| Supplerende kode          | X                  | X            |
| Siren-nummer                | X                  | X            |
| Debitors momskode        | X                  | X            |
| Retningskode              | X                  | X            |
| Transaktionstype            | X                  | X            |
| Forpligtelsesniveau            | X                  | X            |
| Varekode              |                    | X            |
| National NGP-kode                |                    | X            |
| Land/område (afdeling)         |                    | X            |
| Posteringskategori       |                    | X            |
| Oprindelsesland      |                    | X            |
| Oprindelsesland – Import |                    | X            |
| Endelig destination – Eksport |                    | X            |
| Fakturaværdi               | X                  | X            |
| Statistisk værdi           |                    | X            |
| Nettovægt                  |                    | X            |
| Supplerende enheder            |                    | X            |
| Transportkode              |                    | X            |

Følgende tabel viser de felter, der er medtaget i den franske Intrastat-opgørelse i INTRACOM-format.

| **Felt**                   | **Rapportniveau**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (forenklet)** | **1 (fuldt)** |
| Kode                        | X                  | X            |
| Opgørelsesnummer       | X                  | X            |
| Linjenummer              | X                  | X            |
| Siren                       | X                  | X            |
| Land/område (afdeling)         |                    | X            |
| Transportkode              |                    | X            |
| Oprindelsesland           |                    | X            |
| Posteringskategori       |                    | X            |
| Fakturaværdi               | X                  | X            |
| Leveringsmåder           |                    | X            |
| Transaktionstype            | X                  | X            |
| Forpligtelsesniveau            | X                  | X            |
| Varekode              |                    | X            |
| National NGP-kode                |                    | X            |
| Nettovægt                  |                    | X            |
| Statistisk værdi           |                    | X            |
| Supplerende enheder            |                    | X            |
| Oprindelsesland – Import |                    | X            |
| Endelig destination – Eksport |                    | X            |
| Debitors momskode        | X                  | X            |
| Supplerende kode          | X                  | X            |
| Referenceperiode         | X                  | X            |

### <a name="set-up-intrastat"></a>Konfigurere Intrastat

1.  I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) i det delte aktivbibliotek kan du hente de seneste versioner af følgende ER-konfigurationer (ER – Electronic Reporting) til Intrastat-opgørelsen:

-   Intrastat-modul

-   Intrastat-rapport

-   Intrastat INTRACOM (FR)

-   Intrastat SAISUNIC (FR)

Du kan finde flere oplysninger i [Downloade elektroniske rapporteringskonfigurationer fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  I Dynamics 365 Finance skal du gå til **Moms** &gt; **Opsætning** &gt; **Udenrigshandel** &gt; **Parametre for udenrigshandel** og følge disse trin:

    1.  Under fanen **Intrastat** i oversigtspanelet **Elektronisk rapportering** i feltet **Tilknytning af filformat** skal du vælge **Intrastat INTRACOM (FR)** eller **Intrastat SAISUNIC (FR)**.

    2.  Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.

    3.  Vælg **Intrastat** i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.

    4.  Vælg den kode, der bruges til vareoverførsler, i feltet **Transaktionskode** i oversigtspanelet **Generelt**.

    5.  Vælg den kode, der skal bruges til returnering af varer, i feltet **Kreditnota**.

    6.  Angiv detaljeringsniveauet for eksportrapporten i feltet **Forpligtelsesniveau for eksport**. Det niveau, du vælger, påvirker de linjer, der vises i rapporten. Du kan finde yderligere oplysninger i tabellerne i begyndelsen af dette emne.

3.  Gå til **Organisations administration** &gt; **Organisationer** &gt; **Juridiske enheder**, vælg din virksomhed, og følg derefter disse trin:

    1.  Angiv NAF-koden i feltet **NAF-kode** i oversigtspanelet **Registreringsnumre**. Du kan finde flere oplysninger under [FR-00003 NAF-koder og Siret-numre](tasks/fr-00003-naf-codes-siret-numbers.md).

    2.  I oversigtspanelet **Udenrigshandel og logistik** skal du i sektionen **Intrastat** angive felterne til **Eksport med momsfritagelsesnummer** og **Import med momsfritagelsesnummer**.

    3.  I oversigtspanelet **Momsregistrering** skal du i feltet **Momsregistreringsnummer** angive din virksomheds momsregistreringsnummer.

4.  Hvis du vil angive NAF-koder og momsfritagelsesnumre for debitorer, skal du gå til **Debitorer** &gt; **Debitorer** &gt; **Alle debitorer** og følge disse trin:

    1.  Vælg en kunde.

    2.  Angiv debitorens momsfritagelsesnummer i feltet **Momsfritagelsesnummer** i sektionen **Salgsmoms** i oversigtspanelet **Faktura og levering**.

    3.  Angiv virksomhedens Siret-nummer i feltet **Fransk Siret** i oversigtspanelet **Salgsdemografi**.

    4.  Angiv virksomhedens NAF-kode i feltet **NAF-kode**.

    5.  Gentag disse trin for andre debitorer.

5.  Hvis du vil angive NAF-koder og momsfritagelsesnumre for kreditorer, skal du gå til **Kreditorer** &gt; **Kreditorer** &gt; **Alle kreditorer** og følge disse trin:

    1.  Vælg en kreditor.

    2.  Angiv kreditorens momsfritagelsesnummer i feltet **Momsfritagelsesnummer** i sektionen **Salgsmoms** i oversigtspanelet **Faktura og levering**.

    3.  Angiv virksomhedens Siret-nummer i feltet **Fransk Siret** i oversigtspanelet **Købsdemografi**.

    4.  Angiv virksomhedens NAF-kode i feltet **NAF-kode**.

    5.  Gentag disse trin for andre kreditorer.

6.  Gå til **Moms** &gt; **Opsætning** &gt; **Udenrigshandel** &gt; **Komprimering for Intrastat**, og vælg de felter, der skal sammenlignes, når Intrastat-oplysninger opsummeres. Ved fransk Intrastat skal du vælge **Statistisk procedure**, **Oprindelsesland**, **Oprindelsesland/-område**, **Leveringsbetingelser**, **Transport**, **Rettelse**, **Land/område**, **Land for oprindelse/destination**, **Retning**, **Land/område for afsender**, **Afsenderstat**, **Stat**, **Transaktionskode** og **Vare**.

7.  Gå til **Warehouse Management** &gt; **Opsætning** &gt; **Lagersted** &gt; **Lagersteder**, vælg et lagersted, og følg derefter disse trin:

    1.  Vælg **Tilføj** eller **Rediger** i oversigtspanelet **Adresser**.

    2.  Vælg byen for lagerstedet i dialogboksen **By**. Byens stat bruges som land eller område for din DEB-rapport.

### <a name="ngp-codes"></a>NGP-koder

I DEB-rapporten består produktkodningen af følgende elementer:

1.  KN8-koden med otte cifre, der repræsenterer tariffen og statistik nomenklatur for EU.

2.  Hvis det er relevant, er den nationale NGP-varekode (Nomenclature Générale des Produits) på ét ciffer.

I 2021 gælder NGP kun for tre typer produkter:

-   Nogle produkter fra køer, får og geder

-   Militært udstyr

-   Franske vine

Du skal konfigurere NGP-koderne og knytte dem til relaterede produkter. Feltet **NGP** angives derefter automatisk på siden **Intrastat-kladde**.

#### <a name="set-up-an-ngp-code"></a>Konfigurere en NGP-kode

1.  Gå til **Moms** &gt; **Opsætning** &gt; **Udenrigshandel** &gt; **NGP-koder**.

2.  Vælg **Ny** i handlingsruden for at oprette en NGP-kode.

3.  Angiv en kode på ét ciffer i feltet **NGP**.

4.  Angiv en beskrivelse for koden i feltet **Beskrivelse**.

#### <a name="assign-an-ngp-code-to-a-product"></a>Tildele en NGP-kode til et produkt

1.  Gå til **Administration af produktoplysninger** &gt; **Produkter** &gt; **Frigivne produkter**.

2.  Vælg et produkt i gitteret.

3.  Vælg den relevante NGP-kode i feltet **NGP** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.

## <a name="intrastat-journal"></a>Intrastat-kladde

Gå til **Moms** &gt; **Opgørelser** &gt; **Udenrigshandel** &gt; **Intrastat** for at administrere dine transaktioner, som er relevante for udenrigshandel med EU-lande. Du kan finde flere oplysninger under [Intrastat-oversigt](emea-intrastat.md).

Kolonnen **NGP** er specifik for Frankrig. Den viser NGP-koden for produktet. Hvis NGP-koden ikke gælder for et produkt, vises **0** (nul). Du kan justere NGP-koden. Vælg transaktionen, og vælg derefter den ønskede NGP-kode i feltet **NGP** under fanen **Generelt** i sektionen **Koder**.

### <a name="intrastat-transfer"></a>Intrastat-overførsel

På siden **Intrastat** i handlingsruden kan du vælge **Overfør** for automatisk at overføre oplysninger om samhandel med andre steder fra salgsordrer, fritekstfakturaer, indkøbsordrer, kreditorfakturaer, produktkvittering for kreditorer, projektfakturaer og overførselsordrer. Det er kun dokumenter, hvor et EU-land er destinationsland eller -område (til afsendelser) eller forsendelse (til modtagelser), der overføres.

Da DEB-rapporten er en kombination af EU-listesystemet og Intrastat-rapporten, omfatter den også *trekantstransaktioner*, hvor der foretages direkte levering fra ét EU-land (part A) til et andet EU-land (part C), og en fransk juridisk enhed (part B) ligger midt i trekantshandelen.

### <a name="generate-a-deb-intrastat-report"></a>Generere en DEP-rapport (Intrastat)

1.  Gå til **Moms** &gt; **Opgørelser** &gt; **Udenrigshandel** &gt; **Intrastat**.

2.  Vælg **Output** &gt; **Rapport** i handlingsruden.

3.  I dialogboksen **Intrastat-rapport** skal du angive følgende felter.

| Felt            | Betegnelse                                                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Fra-dato        | Vælg startdatoen for rapporten.                                                                                               |
| Til-dato          | Vælg slutdatoen for rapporten.                                                                                                 |
| Generer fil    | Angiv denne indstilling til **Ja** for at generere en .txt-fil.                                                                                 |
| Filnavn        | Angiv navnet på .txt-filen til Intrastat-rapporten.                                                                          |
| Generér rapport  | Angiv denne indstilling til **Ja** for at generere en .xml-fil.                                                                                |
| Rapportfilnavn | Angiv det krævede navn.                                                                                                            |
| Kun rettelser | Angiv denne indstilling til **Ja** for kun at rapportere korrektioner. Angiv det til **Nej** for at rapportere både normale transaktioner og korrektioner.         |
| Vej        | Vælg **Modtagelser** for en rapport om modtagelser inden for fællesskabet. Vælg **Afsendelser** for en rapport om afsendelser inden for fællesskabet. |

## <a name="example"></a>Eksempel

I følgende eksempel vises, hvordan du kan konfigurere og arbejde med NGP-koder. Det bruger den juridiske enhed **DEMF**.

1.  I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) i det delte aktivbibliotek kan du hente de seneste versioner af følgende ER-konfigurationer til Intrastat-opgørelsesformat:

-   Intrastat-modul

-   Intrastat-rapport

-   Intrastat INTRACOM (FR)

2.  I Finance skal du oprette en transaktionskode:

    1.  Gå til **Moms** &gt; **Opsætning** &gt; **Udenrigshandel** &gt; **Transaktionskoder**.

    2.  Gå til handlingsruden, og vælg **Ny**.

    3.  Angiv **11** i feltet **Transaktionskode**.

    4.  Angiv **Køb eller Salg** i feltet **Navn**.

    5.  Vælg **Gem** i handlingsruden.

3.  Konfigurer et produkthierarki:

    1.  Gå til **Administration af produktoplysninger** &gt; **Opsætning** &gt; **Kategorier og attributter** &gt; **Kategorihierarkier**.

    2.  Vælg **Intrastat** i gitteret. Vælg **Rediger** i gruppen **Vedligehold** under fanen **Kategorihierarki** i handlingsruden.

    3.  Vælg **Ny kategorinode** i handlingsruden.

    4.  Angiv **Autres Libournais** i feltet **Navn**.

    5.  Angiv **2204 21 42** i feltet **Kode**.

    6.  Vælg **Gem** i handlingsruden.

4.  Gå til **Moms** &gt; **Opsætning** &gt; **Udenrigshandel** &gt; **Parametre for udenrigshandel** og følge disse trin:

    1.  Vælg **11** i feltet **Transaktionskode** i oversigtspanelet **Generelt** under fanen **Intrastat**.

    2.  Vælg **Intrastat INTRACOM (FR)** i feltet **Tilknytning af filformat** i oversigtspanelet **Elektronisk rapportering**.

    3.  Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.

    4.  Vælg **Intrastat** i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.

5.  Konfigurer en NGP-kode:

    1.  Gå til **Moms** &gt; **Opsætning** &gt; **Udenrigshandel** &gt; **NGP-koder**.

    2.  Gå til handlingsruden, og vælg **Ny**.

    3.  Angiv **8** i feltet **NGP**.

    4.  Angiv **NGP 8** i feltet **Beskrivelsesnavn**.

    5.  Vælg **Gem** i handlingsruden.

6.  Tildel NGP-koden til et produkt:

    1.  Gå til **Administration af produktoplysninger** &gt; **Produkter** &gt; **Frigivne produkter**.

    2.  Vælg **0001** i gitteret.

    3.  Vælg **8** i feltet **NGP** i oversigtspanelet **Udenrigshandel**.

    4.  Vælg **2204 21 42** i feltet **Vare**.

    5.  Vælg **Gem** i handlingsruden.

7.  Opret en salgsordre, der omfatter det nye produkt:

    1.  Gå til **Debitor** &gt; **Ordrer** &gt; **Alle salgsordrer**.

    2.  Gå til handlingsruden, og vælg **Ny**.

    3.  I dialogboksen **Opret** **salgsordre** i sektionen **Debitor** i feltet **Debitorkonto** skal du vælge **100001**.

    4.  I feltet **Leveringsadresse** i afsnittet **Adresse** skal du vælge plustegnet (**+**) for at oprette en adresse.

    5.  Angiv **Tyskland** i feltet **Navn på beskrivelse** i dialogboksen **Ny adresse**.

    6.  Vælg **DEU** i feltet **Land/område**.

    7.  Vælg **OK**.

    8.  Vælg **OK** for at åbne dialogboksen **Opret salgsordre**.

    9.  Vælg **0001** i feltet **Varenummer** i oversigtspanelet **Salgsordrelinjer**.

    10. Vælg **Gem** i handlingsruden.

    11. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.

    12. I dialogboksen **Bogføringsfaktura** i oversigtspanelet **Parametre** i sektionen **Parameter** i feltet **Antal** skal du vælge **Alle**. Vælg derefter **OK** for at bogføre fakturaen.

8.  Opret DEB-rapporten:

    1.  Gå til **Moms** &gt; **Opgørelser** &gt; **Udenrigshandel** &gt; **Intrastat**:

    2.  I handlingsruden. Vælg **Overfør**.

    3.  Angiv indstillingen **Debitorfaktura** til **Ja** i sekionen **Parametre** i dialogboksen **Intrastat (Overførsel)**. Vælg derefter **OK**.

    4.  Sortér transaktioner efter feltet **Dato**. Den øverste postering er resultatposteringen. Feltet **NGP** angives automatisk.

    5.  Vælg **Output** &gt; **Rapport** i handlingsruden.

    6.  Vælg måneden for den salgsordre, du har oprettet, i sektionen **Dato** i oversigtspanelet **Parametre** i dialogboksen **Intrastat-rapport**.

    7.  Angiv indstillingen **Generer fil** til **Ja** i sektionen **Eksportindstillinger**.

    8.  Angiv det krævede navn i feltet **Filnavn**.

    9.  Vælg **OK**, og gennemse rapporten.

