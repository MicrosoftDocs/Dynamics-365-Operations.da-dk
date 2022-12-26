---
title: Fransk Intrastat
description: Denne artikel indeholder oplysninger om Intrastat-opgørelse i Frankrig.
author: anasyash
ms.date: 11/30/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 2076649c7fff9f47b9c1fda62a103168b19bb973
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831799"
---
# <a name="french-intrastat"></a>Fransk Intrastat

[!include[banner](../includes/banner.md)]

Virksomheder i Frankrig, som er registreret for moms, og som handler med andre EU-lande, skal indberette udvekslingen af varer og tjenester til og fra Frankrig. Declaration d'exchanges de Biens (Opgørelse af varehandel) eller DEB er en kombination af EU-listesystemet og Intrastat-rapporten. Du skal indsende denne rapport hver måned for alt varesalg inden for fællesskabet.

Du kan generere DEB-rapporten i et af to elektroniske tekstfilformater: SAISUNIC 330 eller INTRACOM.

Følgende tabel viser de felter, der er medtaget i den franske Intrastat-opgørelse i SAISUNIC 330-format. Tabellen angiver også rapportniveau for hvert felt. Et felt kan have følgende rapportniveauer:

- **4** – Momsopgørelse.
- **1** – Statistisk svar.
- **5** – Statistisk svar på forsendelses- og momsopgørelse samt samlet udfyldning.

| Felt                       | Rapportniveauer |
|-----------------------------|---------------|
| Referenceperiode         | 4, 1, 5       |
| Opgørelsesnummer       | 4, 1, 5       |
| Linjenummer                 | 4, 1, 5       |
| ISO-landekode (FR)       | 4, 1, 5       |
| Supplerende kode          | 4, 1, 5       |
| Siren-nummer                | 4, 1, 5       |
| Debitors momskode        | 4, 1, 5       |
| Retningskode              | 4, 1, 5       |
| Transaktionstype            | 4, 1, 5       |
| Forpligtelsesniveau            | 4, 1, 5       |
| Varekode              | 1, 5          |
| National NGP-kode                | 1, 5          |
| Land/område (afdeling)         | 1, 5          |
| Posteringskategori       | 1, 5          |
| Oprindelsesland      | 1, 5          |
| Oprindelsesland – Import | 1, 5          |
| Endelig destination – Eksport | 1, 5          |
| Fakturaværdi               | 4, 1, 5       |
| Statistisk værdi           | 1, 5          |
| Nettovægt                  | 1, 5          |
| Supplerende enheder            | 1, 5          |
| Transportkode              | 1, 5          |

Følgende tabel viser de felter, der er medtaget i den franske Intrastat-opgørelse i INTRACOM-format. Tabellen angiver også rapportniveau for hvert felt. Et felt kan have følgende rapportniveauer:

- **4** – Momsopgørelse.
- **1** – Statistisk svar.
- **5** – Statistisk svar på forsendelses- og momsopgørelse samt samlet udfyldning.

| Felt                       | Rapportniveauer |
|-----------------------------|---------------|
| Retningskode              | 4, 1, 5       |
| Opgørelsesnummer       | 4, 1, 5       |
| Linjenummer              | 4, 1, 5       |
| Siren                       | 4, 1, 5       |
| Land/område (afdeling)         | 1, 5          |
| Transportkode              | 1, 5          |
| Oprindelsesland           | 1, 5          |
| Posteringskategori       | 1, 5          |
| Fakturaværdi               | 4, 1, 5       |
| Leveringsmåder           | 1, 5          |
| Transaktionstype            | 4, 1, 5       |
| Forpligtelsesniveau            | 4, 1, 5       |
| Varekode              | 1, 5          |
| National NGP-kode                | 1, 5          |
| Nettovægt                  | 1, 5          |
| Statistisk værdi           | 1, 5          |
| Supplerende enheder            | 1, 5          |
| Oprindelsesland – Import | 1, 5          |
| Endelig destination – Eksport | 1, 5          |
| Debitors momskode        | 4, 1, 5       |
| Supplerende kode          | 4, 1, 5       |
| Referenceperiode         | 4, 1, 5       |

## <a name="set-up-intrastat"></a>Konfigurere Intrastat

- I [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index) i det delte aktivbibliotek kan du hente de seneste versioner af følgende ER-konfigurationer (ER – Electronic Reporting) til Intrastat-opgørelsen.

    - Intrastat-modul
    - Intrastat-rapport
    - Intrastat INTRACOM (FR)
    - Intrastat SAISUNIC (FR)

    Du kan finde flere oplysninger i [Downloade elektroniske rapporteringskonfigurationer fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="set-up-vat-ids"></a>Opsætning af moms-id'er

#### <a name="set-up-vat-codes-for-your-company"></a>Angiv momskoder for firmaet

1. Gå til **Moms** \> **Opsætning** \> **Salgsmoms** \> **SE-numre**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Vælg **FRA** i feltet **Land/område**.
4. I feltet **SE-nummer** skal du angive firmaets momsnummer.
5. Gå til **Organisationsadministration** \> **Organisationer** \> **Juridiske enheder** og vælg din virksomhed.
6. I oversigtspanelet **Udenrigshandel og logistik** skal du i sektionen **Intrastat** angive felterne til **Eksport med momsfritagelsesnummer** og **Import med momsfritagelsesnummer** for den kode, du oprettede i trin 4.
7. I oversigtspanelet **Momsregistrering** skal du i feltet **Momsregistreringsnummer** angive din virksomheds momsregistreringsnummer.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Konfigurer moms-id for samhandelspartnere

##### <a name="create-a-registration-type-for-the-company-code"></a>Oprette en registreringstyper for firmakoden

Du skal oprette moms-id-registreringstyper for alle de lande eller områder, som firmaet handler med.

1. Gå til **Organisationsadministration** \> **Globalt adressekartotek** \> **Registreringstyper** \> **Registreringstyper**.
2. Vælg **Ny** i handlingsruden for at oprette en registreringstype til moms-id.
3. Angiv et navn til den nye registreringtype i feltet **Navn** i dialogboksen **Angiv oplysninger om registreringstype**. Indtast for eksempel **MOMS-id**.
4. Vælg land eller område for handelspartneren i feltet **Land/område**.
5. Vælg **Opret**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Match registreringstype med registreringskategori

1. Gå til **Organisationsadministration** \> **Globalt adressekartotek** \> **Registreringstyper** \> **Registreringskategorier**.
2. Vælg **Ny** i handlingsruden for at oprette et link mellem en registreringstype og en registreringskategori.
3. Vælg registreringskategorien **Moms-id** for registreringstypen Moms-id.
4. Gentag trin 2 og 3 for de andre registreringstyper, du har oprettet for de lande eller områder, som firmaet gør forretning med.

##### <a name="set-up-the-vat-number-of-a-trading-partner"></a>Oprette momsnummeret på en samhandelspartner

1. Gå til **Debitor** \> **Kunder** \> **Alle kunder**.
2. Vælg en kunde i gitteret.
3. Gå til handlingsruden, og vælg **Registrerings-id'er** i gruppen **Registrering** under fanen **Kunde**.
4. Vælg **Tilføj** i oversigtspanelet **Registrerings-id** for at oprette et registrerings-id.
5. I feltet **Registreringstype** skal du vælge den registreringstype, du har oprettet for firmakoden.
6. Angiv momsnummeret i feltet **Registreringsnummer**.
7. Vælg **Gem** i handlingsruden, og luk siden.

Du kan finde flere oplysninger under [Registrerings-id'er](emea-registration-ids.md).

### <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre

1. Gå til **Moms** \> **Konfiguration** \> **Udenrigshandel** \> **Udenrigshandelsparametre**.
2. Under fanen **Intrastat** i oversigtspanelet **Elektronisk rapportering** i feltet **Tilknytning af filformat** skal du vælge **Intrastat INTRACOM (FR)** eller **Intrastat SAISUNIC (FR)**.
3. Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.
4. Vælg **Intrastat** i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
5. Vælg den kode, der bruges til vareoverførsler, i feltet **Transaktionskode** i oversigtspanelet **Generelt**.
6. Vælg den kode, der skal bruges til returnering af varer, i feltet **Kreditnota**.
7. Vælg navnet på kontakten i feltet **Arbejder**.
8. Tilføj oplysninger om kontaktpersonen under fanen **Kontakt**:

    - Angiv kontaktpersonens telefonnummer i feltet **Telefon**.
    - Angiv kontaktpersonens faxnummer i feltet **Fax**.

9. Under fanen **Lande-/områdeegenskaber** indeholder feltet **Land/område** alle de lande eller områder, som dit firma handler med. For hvert land/område, der indgår i EU, skal du vælge **EU** i feltet **Lande-/områdetype**, så landet/området vises i Intrastat-rapporten. Vælg **Indland** for Frankrig i feltet **Lande-/områdetype**.

### <a name="set-up-compression-of-intrastat"></a>Opsætning af komprimering af Intrastat

- Gå til **Moms** \> **Opsætning** \> **Udenrigshandel** \> **Komprimering for Intrastat**, og vælg de felter, der skal sammenlignes, når Intrastat-oplysninger opsummeres. Vælg følgende felter til for fransk Intrastat:
 
    - Statistisk procedure
    - Oprindelsesland/område
    - Transporter
    - Rettelse
    - Land/område
    - Oprindelsesområde/destination
    - Vej
    - Afsenderland/-område
    - Transaktionsart
    - Varekode

### <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Angive produktparametre for Intrastat-opgørelsen

1. Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.
2. Vælg et produkt i gitteret.
3. Vælg den relevante varekode i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**. Navnet på varen udskrives i feltet **Beskrivelse af varer** i Intrastat-rapporten.
4. Vælg produktets oprindelsesland eller -område i feltet **Land/område** i afsnittet **Oprindelse**.
5. Angiv produktets vægt i kilo i feltet **Nettovægt** i oversigtspanelet **Styr lager**.

### <a name="ngp-codes"></a>NGP-koder

I DEB-rapporten består produktkodningen af følgende elementer:

- KN8-koden med otte cifre, der repræsenterer tariffen og statistik nomenklatur for EU.
- Hvis det er relevant, er den nationale NGP-varekode (Nomenclature Générale des Produits) på ét ciffer.

I 2022 gælder NGP kun for tre typer produkter:

- Nogle produkter fra køer, får og geder
- Militært udstyr
- Franske vine

Du skal konfigurere NGP-koderne og knytte dem til relaterede produkter. Feltet **NGP** angives derefter automatisk på siden **Intrastat-kladde**.

#### <a name="set-up-an-ngp-code"></a>Konfigurere en NGP-kode

1. Gå til **Moms** \> **Opsætning** \> **Udenrigshandel** \> **NGP-koder**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv en kode på ét ciffer i feltet **NGP**.
4. Angiv en beskrivelse for koden i feltet **Beskrivelse**.

#### <a name="assign-an-ngp-code-to-a-product"></a>Tildele en NGP-kode til et produkt

1. Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.
2. Vælg et produkt i gitteret.
3. Vælg den relevante NGP-kode i feltet **NGP** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.

### <a name="set-up-warehouse-parameters-for-the-intrastat-declaration"></a>Angive lagerstedsparametre for Intrastat-opgørelsen

1. Gå til **Warehouse Management** \> **Konfiguration** \> **Lagersted** \> **Lagersteder**.
2. Vælg et lagersted, og vælg derefter **Tilføj** eller **Rediger** i oversigtspanelet **Adresser**.
3. Vælg byen for lagerstedet i dialogboksen **By**. Byens stat eller provins bruges som land eller område for din DEB-rapport.

### <a name="set-up-the-transport-method"></a>Konfigurere transportmetoden

1. Gå til **Moms** \> **Opsætning** \> **Udenrigshandel** \> **Transportmetode**.
2. Gå til handlingsruden, og vælg **Ny**.
3. I feltet **Transport** skal du angive en entydig kode. Franske virksomheder bruger etcifrede transportkoder.

### <a name="intrastat-journal"></a>Intrastat-kladde

Gå til **Moms** \> **Opgørelser** \> **Udenrigshandel** \> **Intrastat** for at administrere dine transaktioner, som er relevante for udenrigshandel med EU-lande. Du kan finde flere oplysninger under [Intrastat-oversigt](emea-intrastat.md).

Kolonnen **NGP** er specifik for Frankrig og viser NGP-koden for produktet. Hvis NGP-koden ikke gælder for et produkt, vises **0** (nul). Vælg transaktionen for at justere NGP-koden, og vælg derefter den ønskede NGP-kode i feltet **NGP** under fanen **Generelt** i sektionen **Koder**.

#### <a name="intrastat-transfer"></a>Intrastat-overførsel

På siden **Intrastat** i handlingsruden kan du vælge **Overfør** for automatisk at overføre oplysninger om samhandel med andre steder fra salgsordrer, fritekstfakturaer, indkøbsordrer, kreditorfakturaer, produktkvittering for kreditorer, projektfakturaer og overførselsordrer. Det er kun dokumenter, hvor et EU-land er destinationsland eller -område (til afsendelser) eller forsendelse (til modtagelser), der overføres.

Da DEB-rapporten er en kombination af EU-listesystemet og Intrastat-rapporten, omfatter den også *trekantstransaktioner*, hvor der foretages direkte levering fra ét EU-land (part A) til et andet EU-land (part C), og en fransk juridisk enhed (part B) ligger midt i trekantshandelen.

#### <a name="generate-a-deb-intrastat-report"></a>Generere en DEP-rapport (Intrastat)

1. Gå til **Moms** \> **Opgørelser** \> **Udenrigshandel** \> **Intrastat**.
2. Vælg **Output** \> **Rapport** i handlingsruden.
3. I dialogboksen **Intrastat-rapport** skal du angive følgende felter.

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

4. Vælg **OK** for at lukke dialogboksen **Intrastat-rapport**.
5. I dialogboksen **Parametre for elektronisk rapport** i oversigtspanelet **Parametre** i feltet **Rapportniveau** skal du vælge rapportniveau. Rapportniveauet kan være **1 - statistisk svar**, **4 - momsopgørelse** eller **5 - statistisk svar på forsendelses- og momsopgørelse**.

## <a name="example"></a>Eksempel:

Følgende eksempel viser, hvordan du konfigurerer fransk Intrastat og opretter DEB-rapporten. Det bruger den juridiske enhed **DEMF**.

### <a name="preliminary-setup"></a>Foreløbig opsætning

1. I [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index) i det delte aktivbibliotek kan du hente de seneste versioner af følgende ER-konfigurationer til Intrastat-opgørelsesformat:

    - Intrastat-modul
    - Intrastat-rapport
    - Intrastat INTRACOM (FR)

2. Konfigurer et produkthierarki:

    1. Gå til **Administration af produktoplysninger** \> **Opsætning** \> **Kategorier og attributter** \> **Kategorihierarkier**.
    2. Vælg **Intrastat** i gitteret.
    3. Vælg **Rediger** i gruppen **Vedligehold** under fanen **Kategorihierarki** i handlingsruden.
    4. Vælg **Ny kategorinode** i handlingsruden.
    5. Angiv **Autres Libournais** i feltet **Navn**.
    6. Angiv **2204 21 42** i feltet **Kode**.
    7. Vælg **Gem** i handlingsruden.

### <a name="set-up-vat-ids"></a>Opsætning af moms-id'er

#### <a name="set-up-vat-codes-for-your-company"></a>Angiv momskoder for firmaet

1. Gå til **Moms** \> **Opsætning** \> **Salgsmoms** \> **SE-numre**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Vælg **FRA** i feltet **Land/område**.
4. Angiv **MS123456** i feltet **SE-nummer**.
5. Gå til **Organisationsadministration** \> **Organisationer** \> **Juridiske enheder**, og vælg **DEMF**.
6. I oversigtspanelet **Udenrigshandel og logistik** skal du i sektionen **Intrastat** angive felterne til **Eksport med momsfritagelsesnummer** og **Import med momsfritagelsesnummer** for den kode, du oprettede i trin 4.
7. Angiv **123456789** i oversigtspanelet **Momsregistrering** i feltet **SE-nummer**.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Konfigurer moms-id for samhandelspartnere

##### <a name="create-a-registration-type-for-the-company-code"></a>Oprette en registreringstyper for firmakoden

1. Gå til **Organisationsadministration** \> **Globalt adressekartotek** \> **Registreringstyper** \> **Registreringstyper**.
2. Vælg **Ny** i handlingsruden for at oprette en registreringstype til moms-id.
3. Angiv **Moms-id** i feltet **Navn** i dialogboksen **Angiv oplysninger om registreringstype**.
4. Vælg **DEU** i feltet **Land/område**.
5. Vælg **Opret**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Match registreringstype med registreringskategori

1. Gå til **Organisationsadministration** \> **Globalt adressekartotek** \> **Registreringstyper** \> **Registreringskategorier**.
2. Vælg **Ny** i handlingsruden for at oprette et link mellem en registreringstype og en registreringskategori.
3. Vælg **Moms-id**-registreringskategorien for **DEU**-landet i **Moms-id**-registreringstype.

##### <a name="set-up-the-customers-vat-registration-number"></a>Konfigurere kundens moms-nummer

1. Gå til **Debitor** \> **Kunder** \> **Alle kunder**.
2. Vælg **DE-016** i gitteret.
3. Gå til handlingsruden, og vælg **Registrerings-id'er** i gruppen **Registrering** under fanen **Kunde**.
4. Vælg **Tilføj** i oversigtspanelet **Registrerings-id** for at oprette et registrerings-id.
5. Vælg **Moms-id** i feltet **Registreringstype**.
6. Angiv **DE9012** i feltet **Registreringsnummer**.
7. Vælg **Gem** i handlingsruden, og luk siden.
8. Vælg **DE9012** i feltet **SE-nummer** i sektionen **Salgsmoms** i oversigtspanelet **Faktura og levering**.

### <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre

1. Gå til **Moms** \> **Konfiguration** \> **Udenrigshandel** \> **Udenrigshandelsparametre**.
2. Vælg **11** i feltet **Transaktionskode** i oversigtspanelet **Generelt** under fanen **Intrastat**.
3. Vælg **Intrastat INTRACOM (FR)** i feltet **Tilknytning af filformat** i oversigtspanelet **Elektronisk rapportering**.
4. Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.
5. Vælg **Intrastat** i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
6. Vælg en post i feltet **Arbejder**.
7. Angiv kontaktpersonens telefonnummer i feltet **Telefon** på fanen **Kontakt**
8. Angiv kontaktpersonens faxnummer i feltet **Fax**.

### <a name="create-ngp-code"></a>Oprette en NGP-kode

1. Gå til **Moms** \> **Opsætning** \> **Udenrigshandel** \> **NGP-koder**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv **8** i feltet **NGP**.
4. Angiv **NGP 8** i feltet **Beskrivelsesnavn**.
5. Vælg **Gem** i handlingsruden.

### <a name="set-up-product-information"></a>Angive produktoplysninger

1. Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.
2. Vælg **D0001** i gitteret.
3. Vælg **8** i feltet **NGP** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
4. Vælg **2204 21 42** i feltet **Vare**.
5. Vælg **FRA** i feltet **Land/område** i sektionen **Oprindelse**.
6. Angiv **2** i feltet **Nettovægt** i sektionen **Vægtmålinger** i oversigtspanelet **Styr lager**.
7. Vælg **Gem** i handlingsruden, og luk siden.
8. Vælg **D0003** i gitteret.
9. Vælg **100 200 30** i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
10. Vælg **DEU** i feltet **Land/område** i sektionen **Oprindelse**.
11. Angiv **5** i feltet **Nettovægt** i sektionen **Vægtmålinger** i oversigtspanelet **Styr lager**.
12. Vælg **Gem** i handlingsruden.

### <a name="set-up-regime-codes"></a>Konfigurere Regime-koder

1. Gå til **Moms** \> **Opsætning** \> **Udenrigshandel** \> **Statistisk procedure**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Vælg **21** i feltet **Statistisk procedure**.
4. Angiv **Regime-kode 21** i feltet **Tekst 1**.

### <a name="change-the-site-address"></a>Ændre adressen for webstedet

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Lagersted** \> **Sted**.
2. Vælg **1** i gitteret.
3. Vælg **Rediger** i oversigtspanelet **Adresser**.
4. Vælg **FRA** i feltet **Land/område** i dialogboksen **Rediger adresse**.
5. Vælg **OK**.
6. Gå til **Warehouse Management** \> **Opsætning** \> **Lagersted** \> **Lagersteder** og vælg et lagersted.
7. Vælg **Tilføj** i oversigtspanelet **Adresser**.
8. Vælg **FRA** i feltet **Land/område** i dialogboksen **Ny adresse**.
9. Vælg **Bordeaux** i feltet **By**.
10. Vælg **OK** for at lukke dialogboksen.

### <a name="set-up-a-transport-method"></a>Konfigurere en transportmetode

1. Gå til **Moms** \> **Opsætning** \> **Udenrigshandel** \> **Transportmetode**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv **3** i feltet **Transport**.
4. Indtast **Vejtransport** i feltet **Beskrivelse**.

### <a name="assign-a-transport-mode-to-a-mode-of-delivery"></a>Knyt en transporttilstand til en leveringsmåde

1. Gå til **Indkøb og forsyning** \> **Opsætning** \> **Distribution** \> **Leveringsmåder**.
2. Vælg **50** i gitteret.
3. Vælg **3** i feltet **Transport** i oversigtspanelet **Udenrigshandel**.

### <a name="create-a-sales-order-with-an-eu-customer-that-includes-the-new-product"></a>Opret en salgsordre med en EU-kunde, der omfatter det nye produkt

1. Gå til **Debitor** \> **Ordrer** \> **Alle salgsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. I dialogboksen **Opret salgsordre** i sektionen **Kunde** i feltet **Kundekonto** skal du vælge **DE-016**.
4. I feltet **Leveringsadresse** i afsnittet **Adresse** skal du vælge plustegnet (**+**) for at oprette en adresse.
5. Angiv **Tyskland** i feltet **Navn på beskrivelse** i dialogboksen **Ny adresse**.
6. Vælg **DEU** i feltet **Land/område**.
7. Vælg **OK**.
8. Vælg **OK** for at åbne dialogboksen **Opret salgsordre**.
9. Vælg **0001** i feltet **Varenummer** i oversigtspanelet **Salgsordrelinjer**.
10. Vælg **21** i feltet **Statistisk procedure** i oversigtspanelet **Linjedetaljer** under fanen **Udenrigshandel**.
11. Vælg **AL** i feltet **Oprindelsesstat**.
12. Vælg **Gem** i handlingsruden.
13. Kontroller, at der er valgt **50** i feltet **Leveringsmåde** på oversigtpanelet **Levering** på fanen **Overskrift**.
14. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
15. I dialogboksen **Bogføringsfaktura** i oversigtspanelet **Parametre** i sektionen **Parameter** i feltet **Antal** skal du vælge **Alle**. Vælg derefter **OK** for at bogføre fakturaen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Overføre transaktionen til Intrastat-kladden og gennemse resultatet

1. Gå til **Moms** \> **Opgørelser** \> **Udenrigshandel** \> **Intrastat**.
2. Vælg **Overfør** i handlingsruden.
3. Angiv indstillingen **Debitorfaktura** til **Ja** i sekionen **Parametre** i dialogboksen **Intrastat (Overførsel)**. Vælg derefter **OK**.
4. Sortér transaktioner efter feltet **Dato**. Den øverste postering er resultatposteringen.

    ![Linje, der repræsenterer salgsordren på siden Intrastat.](media/intrastat_fr_1.png)

5. Vælg transaktionslinjen, og vælg derefter fanen **Generelt** for at få vist flere detaljer.

    ![Salgsordredetaljer under fanen Generelt på Intrastat-siden.](media/intrastat_fr_2.png)

6. Vælg **Output** \> **Rapport** i handlingsruden.
7. Vælg måneden for den salgsordre, du har oprettet, i sektionen **Dato** i oversigtspanelet **Parametre** i dialogboksen **Intrastat-rapport**.
8. Angiv indstillingen **Generer fil** til **Ja** i sektionen **Eksportindstillinger**.
9. Angiv det krævede navn i feltet **Filnavn**.
10. Vælg **OK** for at lukke dialogboksen **Intrastat-rapport**.
11. I dialogboksen **Parametre for elektronisk rapport** i oversigtspanelet **Parametre** i feltet **Rapportniveau** skal du vælge **5 -statistisk svar på forsendelses- og momsopgørelse** og gennemse rapporten.

    ![Intrastat Intracom-rapport for afsendelser.](media/intrastat_fr_3.png)

12. Gennemse den oprettede Excel-rapport.

    ![Intrastat-rapport for afsendelser.](media/intrastat_fr_4.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
