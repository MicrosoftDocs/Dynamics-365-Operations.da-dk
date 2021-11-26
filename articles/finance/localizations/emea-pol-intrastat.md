---
title: Polsk Intrastat
description: Dette emne indeholder oplysninger om Intrastat-rapportering i Polen.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfender
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: 9564892f768adb8f48208fe10b31c7c6392a4567
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779901"
---
# <a name="polish-intrastat"></a>Polsk Intrastat

[!include[banner](../includes/banner.md)]

Siden **Intrastat** bruges til at generere og rapportere oplysninger om handel mellem EU-lande. Den polske Intrastat-opgørelse indeholder oplysninger om varehandel til indberetning.

Følgende felter medtages i den polske Intrastat-opgørelse. Alle felterne er medtaget ved modtagelser og afsendelser med undtagelse af **RodzajTransportu** (transportmåden) og **KrajPochodzenia** (oprindelsesland eller -område), som ikke er medtaget på afsendelser, og **IdKontrahenta** (kundens udenlandske momsnummer), som ikke er medtaget på modtagelser.

| Feltnavn | Beskrivelse |
|-------------------------|-------------------------|
| Deklaracja Data | Den dato, hvor dokumentet blev oprettet. |
| Miesiac | Referencemåneden i erklæringen. |
| Rok | Referenceåret i erklæringen. |
| Numer | Opgørelsesnummeret i referenceperioden. |
| Wersja | Versionsnummeret i erklæringen. |
| NrWlasny | Erklæringens identifikator. Denne værdi oprettes automatisk. |
| Typ | Rapportens retning.</br><li>Ved modtagelser udskrives "P".</li><li>Ved afsendelser udskrives "W".</li> |
| Rodzaj | Typen af erklæring. Værdien angiver, om rapporten er den oprindelige erklæring eller en rettelseserklæring. |
| UC | Den enhedskode, som Intrastat-erklæringen sendes til. Værdien angives i feltet **SE-nummer** i sektionen **Moms** under fanen **Agent** på siden **Udenrigshandelsparametre**. |
| Nazwa | Navnet på firmaet. |
| Miejscowosc, UlicaNumer, KodPocztowy | Det fulde adresse på den juridiske enhed. |
| Nip | Det polske momsidentifikationsnummer (moms-id [VAT]). |
| Regon | Det polske statistiske id-nummer (virksomhedsnummer). |
| LacznaWartoscFaktur | Summen af fakturaværdier. |
| LacznaWartoscStatystyczna | Summen af statistiske værdier. |
| LacznaLiczbaPozycji | Det samlede antal varer. |
| PozId | Det fortløbende nummer på en given vare. |
| OpisTowaru | Varens handelsnavn. |
| KrajPochodzeniaWysylki | ISO-koden (International Organization for Standardization) for modpartens land eller område. |
| WarunkiDostawy | Intrastat-koden for leveringsbetingelserne. |
| RodzajTransakcji | Den kode, der angiver posteringens art. Polske virksomheder bruger tocifrede transaktionskoder. |
| KodTowarowy | Den ottecifrede varekode i henhold til den kombinerede nomenklatur. |
| RodzajTransportu | Intrastat-koden for transportmåden. |
| KrajPochodzenia | ISO-koden for det land eller område, hvor varerne blev produceret eller fremstillet. |
| MasaNetto | Nettovægten i hele kilogram. |
| IloscUzupelniajacaJm | Antallet i den supplerende måleenhed i hele tal. |
| WartoscFaktury | Fakturaværdien af alle posteringer, der er dækket af én vare. |
| WartoscStatystyczna | Den statistiske værdi. |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, Email | For- og efternavn, telefonnummer, faxnummer og mailadresse på den person, der indsender opgørelsen. |
| IdKontrahenta | Debitorens udenlandske momsnummer i et EU-medlemsland. |


## <a name="set-up-intrastat"></a>Konfigurere Intrastat

Fra det globale lager kan du importere den seneste version af følgende elektroniske rapporteringskonfigurationer (ER):

   - Intrastat-modul
   - Intrastat-rapport
   - Intrastat (PL)

Du kan finde flere oplysninger under [Downloade ER-konfigurationer fra det globale lager i konfigurationstjeneste](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Konfigurere et moms-id og et virksomhedsnummer til din virksomhed

### <a name="create-registration-types-for-company-codes"></a>Oprette registreringstyper for firmakoder

Du skal oprette to registreringstyper for firmakoder: en til moms-id (NIP-kode) og en til firmanummeret (Regon-kode).

1. Gå til **Virksomhedsadministration** > **Globalt adressekartotek** > **Registreringstyper** > **Registreringstyper**.
2. Vælg **Ny** i handlingsruden for at oprette en registreringstype til moms-id.
3. Angiv et navn til den nye registreringtype i feltet **Navn** i dialogboksen **Angiv oplysninger om registreringstype**. Indtast for eksempel **NIP**.
4. Vælg **POL** i feltet **Land/område**.
5. Vælg **Opret**.
6. Vælg **Ny** i handlingsruden for at oprette en registreringstype til virksomhedsnummeret.
7. Angiv et navn til den nye registreringtype i feltet **Navn** i dialogboksen **Angiv oplysninger om registreringstype**. Indtast for eksempel **Regon**.
8. Vælg **POL** i feltet **Land/område**.
9. Vælg **Opret**.

### <a name="match-the-registration-types-with-registration-categories"></a>Matche registreringstyper med registreringskategorier

1. Gå til **Virksomhedsadministration** > **Globalt adressekartotek** > **Registreringstyper** > **Registreringskategorier**.
2. Vælg **Ny** i handlingsruden for at oprette et link mellem hver registreringstype, du har oprettet, og en registreringskategori.

    - Vælg registreringskategorien **Moms-id** for registreringstypen Moms-id (NIP-kode).
    - Vælg registreringskategorien **Virksomheds-id (COID)** for registreringstypen virksomhedsnummer (Regon-kode).

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Konfigurere et moms-id og et virksomhedsnummer til din virksomhed

1. Gå til **Organisationsadministration** > **Organisationer** > **Juridiske enheder**.
2. Vælg dit firma i gitteret.
3. Vælg **Registrerings-id'er** i handlingsruden.
4. Vælg **Tilføj** i oversigtspanelet **Registrerings-id**.
5. I feltet **Registreringstype** skal du vælge en af de registreringstyper, du har oprettet tidligere.
6. Angiv dit firmas moms-id (NIP-kode) eller virksomhedsnummer (Regon-kode), afhængigt af den registreringstype, du valgte i det foregående trin.
7. Gentag trin 4 til 6 for den anden registreringstype, du oprettede tidligere.

## <a name="set-up-a-company-address"></a>Konfigurere en firmaadresse

1. Gå til **Organisationsadministration** > **Organisationer** > **Juridiske enheder**.
2. Vælg dit firma i gitteret.
3. Vælg **Rediger** under fanen **Adresser**.
4. Vælg dit firmas postnummer i feltet **Postnummer** i dialogboksen **Rediger adresse**.
5. I feltet **Gade** skal du angive din adresse.
6. Vælg din by i feltet **By**.

## <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre

1. Gå til **Moms** > **Opsætning** > **Parametre for udenrigshandel**.
2. Under fanen **Intrastat** skal du i feltet **Tilknytning af filformat** vælge **Intrastat (PL)** i oversigtspanelet **Elektronisk rapportering**.
3. Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.
4. Vælg **Intrastat** i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
5. I feltet **Transaktionskode** skal du vælge transaktionskoden for egenskabsoverførsler. Denne kode bruges til transaktioner, der opretter faktiske eller planlagte overførsler af egenskab mod kompensation (økonomisk eller på anden vis). Du kan også bruge den til rettelser. Firmaer i Polen bruger tocifrede transaktionskoder.
6. I feltet **Kreditnota** skal du vælge transaktionskoden for returnering af varer.
7. Under fanen **Lande-/områdeegenskaber** indeholder feltet **Land/område** alle de lande eller områder, som dit firma handler med. For hvert land/område, der indgår i EU, skal du vælge **EU** i feltet **Lande-/områdetype**, så landet/området vises i Intrastat-rapporten. Vælg **Indland** for Polen i feltet **Lande-/områdetype**.
8. Angiv **420000** i feltet **SE-nummer** i sektionen **Moms** under fanen **Agent** i oversigtspanelet **Agent** for at angive den enhedskode, som Intrastat-opgørelsen er adresseret til.
9. Under fanen **Kontakt** skal du angive navn, telefonnummer, faxnummer og mailadresse på den person, der indsender opgørelsen.
10. Under fanen **Nummerserier** skal du i feltet **Nummerseriekode** til **XML-filnummer**-referencen angive en ikke-fortløbende nummerserie, der maksimalt indeholder ni tegn. Dette felt bruges til automatisk at generere en værdi til feltet **Opgørelsesidentifikator** i Intrastat-rapporten.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Angive produktparametre for Intrastat-opgørelsen

1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
2. Vælg et produkt i gitteret.
3. Vælg den relevante varekode i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**. Navnet på varen udskrives i feltet **Beskrivelse af varer** i Intrastat-rapporten.
4. Vælg produktets oprindelsesland eller -område i feltet **Land/område** i afsnittet **Oprindelse**.
5. Angiv produktets vægt i kilo i feltet **Nettovægt** i oversigtspanelet **Styr lager**.

## <a name="set-up-compression-of-intrastat"></a>Opsætning af komprimering af Intrastat

-   Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Komprimering for Intrastat**, og vælg de felter, der skal sammenlignes, når Intrastat-oplysninger opsummeres. Vælg følgende felter til polsk Intrastat:

    - Varekode
    - Transaktionsart
    - Oprindelsesland/område
    - Transporter
    - Leveringsbetingelse
    - Afsenderland/-område
    - Land/område
    - Rettelse
    - SE-nummer
    - Vej
    - Faktura

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Angive transportmetode og leveringsbetingelser

1.  Konfigurer transportkoder.

    1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Transportmetode**.
    2. Gå til handlingsruden, og vælg **Ny**.
    3. I feltet **Transport** skal du angive en entydig kode. Polske virksomheder bruger etcifrede transportkoder.

2.  Konfigurer Intrastat-koder for leveringsmåde.

    1. Gå til **Indkøb og forsyning** > **Opsætning** > **Distribution** > **Leveringsbetingelser**.
    2. Vælg leveringsbetingelserne i gitteret.
    3. Angiv den entydige kode i feltet **Intrastat-kode** i oversigtspanelet **Generelt**.

## <a name="intrastat-transfer"></a>Intrastat-overførsel

På siden **Intrastat** i handlingsruden kan du vælge **Overfør** for automatisk at overføre oplysninger om samhandel med andre steder fra salgsordrer, fritekstfakturaer, indkøbsordrer, kreditorfakturaer, produktkvittering for kreditorer, projektfakturaer og overførselsordrer. Det er kun dokumenter, hvor et EU-land er destinationsland eller -område eller konsignation, der overføres.

Du kan også angive posteringer manuelt ved at vælge **Ny** i handlingsruden.

### <a name="generate-an-intrastat-report"></a>Generere en Intrastat-rapport

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Output** &gt; **Rapport** i handlingsruden.
3. I dialogboksen **Intrastat-rapport** skal du angive følgende felter.

    | Felt | Beskrivelse |
    |-------------------------|-------------------------|
    | Fra-dato | Vælg startdatoen for rapporten. |
    | Generer fil | Angiv denne indstilling til **Ja** for at generere en .xml-fil til Intrastat-rapporten. |
    | Filnavn | Angiv navnet på .xml-filen. |
    | Generér rapport | Angiv denne indstilling til **Ja** for at generere en .xlsx-fil til Intrastat-rapporten. |
    | Rapportfilnavn | Angiv navnet på .xlsx-filen. |
    | Vej | Vælg **Modtagelser** for en rapport om modtagelser inden for fællesskabet.</br>Vælg **Afsendelser** for en rapport om afsendelser inden for fællesskabet. |
    | Erklæringens identifikator | Dokument-id'et genereres automatisk og kan opdateres. |
    | Opgørelsestype | Vælg **Opgørelse** for en oprindelig opgørelse.</br>Vælg **Opgørelsesrettelse – erstatning** for en rettelsesopgørelse, der skal erstatte en eksisterende, tidligere indsendt original- eller rettelsesopgørelse fuldt ud. |
    | By for dokumentoprettelse | Angiv den værdi, der skal udskrives i feltet **Miejscowosc** i Intrastat-opgørelsen. |
    | Dato for dokumentoprettelse | Angiv den værdi, der skal udskrives i feltet **Deklaracja Data** i Intrastat-opgørelsen. |
    | Dokumentnummer | Angiv den værdi, der skal udskrives i feltet **Numer** i Intrastat-opgørelsen. |
    | Dokumentversion | Angiv den værdi, der skal udskrives i feltet **Wersja** i Intrastat-opgørelsen. |

4. Vælg **OK**, og gennemse de genererede rapporter.

## <a name="example"></a>Eksempel

Dette eksempel viser, hvordan du bogfører indførsler og udførsler til Intrastat med den juridiske enhed **DEMF**.

### <a name="preliminary-setup"></a>Foreløbig opsætning

Importér den seneste version af følgende ER-konfigurationer:

   - Intrastat-modul
   - Intrastat-rapport
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Konfigurere en firmaadresse

1. Gå til **Organisationsadministration** > **Globalt adressekartotek** > **Adresser** > **Adresseopsætning**.
2. Vælg **Ny** under fanen **By**.
3. Vælg **POL** i feltet **Land/område**.
4. Angiv **Warszawa** i feltet **By**.
5. Vælg **Ny** under fanen **Postnummer**.
6. Vælg **POL** i feltet **Land/område**.
7. Vælg **Warszawa** i feltet **By**.
8. Angiv **00-844** i **Postnummer**-feltet.
9. Gå til **Organisationsadministration** > **Organisation** > **Juridiske enheder**, og vælg den juridiske **DEMF**-enhed.
10. Vælg **Rediger** i oversigtspanelet **Adresser**.
11. Vælg **POL** i feltet **Land/område**.
12. Vælg **31-111** i **Postnummer**-feltet.
13. I feltet **Gade** skal du angive **Statystyczna 22/1**.
14. Vælg **Warszawa** i feltet **By**.
15. Vælg **OK**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Konfigurere et moms-id og en virksomhedsnummerkode til din virksomhed

### <a name="create-registration-types-for-company-codes"></a>Oprette registreringstyper for firmakoder

1. Gå til **Virksomhedsadministration** > **Globalt adressekartotek** > **Registreringstyper** > **Registreringstyper**.
2. Vælg **Ny** i handlingsruden for at oprette en registreringstype til moms-id (NIP-kode).
3. Angiv **NIP** i feltet **Navn** i dialogboksen **Angiv oplysninger om registreringstype**.
4. Vælg **POL** i feltet **Land/område**.
5. Vælg **Opret**.
6. Vælg **Ny** i handlingsruden for at oprette en registreringstype til virksomhedsnummeret (Regon-kode).
7. Angiv **Regon** i feltet **Navn** i dialogboksen **Angiv oplysninger om registreringstype**.
8. Vælg **POL** i feltet **Land/område**.
9. Vælg **Opret**.

### <a name="match-the-registration-types-with-registration-categories"></a>Matche registreringstyper med registreringskategorier

1. Gå til **Virksomhedsadministration** > **Globalt adressekartotek** > **Registreringstyper** > **Registreringskategorier**.
2. Vælg **Ny** i handlingsruden for at oprette et link mellem hver registreringstype, du har oprettet, og en registreringskategori.

    - Vælg registreringskategorien **Moms-id** for registreringstypen **NIP**.
    - Vælg registreringskategorien **Virksomheds-id (COID)** for registreringstypen **Regon**.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Konfigurere et moms-id og et virksomhedsnummer til din virksomhed

1. Gå til **Organisationsadministration** > **Organisationer** > **Juridiske enheder**.
2. Vælg **DEMF** i gitteret.
3. Vælg **Registrerings-id'er** i handlingsruden.
4. Vælg **Tilføj** i oversigtspanelet **Registrerings-id**.
5. Vælg **NIP** i feltet **Registreringstype**.
6. Angiv **1234567890** i feltet **Registreringsnummer**.
7. Vælg **Tilføj**.
8. Vælg **Regon** i feltet **Registreringstype**.
9. Angiv **12345678901234** i feltet **Registreringsnummer**.

### <a name="set-up-a-number-sequence-code"></a>Konfigurere en nummerseriekode

1. Gå til **Organisationsadministration** > **Nummerserier** > **Nummerserier**.
2. Vælg **Nummerserie** i gruppen **Ny** under fanen **Nummerserie** i handlingsruden.
3. Angiv **XML\_fil** i feltet **Nummerseriekode** i oversigtspanelet **Identifikation**.
4. Vælg **Firma** i feltet **Område** i oversigtspanelet **Intervalparametre**.
5. Vælg **DEMF** i feltet **Firma**.
6. I feltet **Længde** for **Alfanumerisk** segment i oversigtspanelet **Segmenter** skal du angive **4**.
7. I sektionen **Opsætning** i oversigtspanelet **Generelt** skal du angive indstillingen **Fortløbende** til **Nej**.
8. Angiv **9999** i sektionen **Nummertildeling** i feltet **Største**.

### <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre

1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Udenrigshandelsparametre**.
2. Vælg **11** i feltet **Transaktionskode** i oversigtspanelet **Generelt** under fanen **Intrastat**.
3. Vælg **Intrastat (PL)** i feltet **Tilknytning af filformat** i oversigtspanelet **Elektronisk rapportering**.
4. Vælg **Intrastat-rapport** i feltet **Rapportformattilknytning**.
5. Sørg for, at **Intrastat** er valgt i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
6. Vælg **Ny** under fanen **Egenskaber for land/område**.
7. Vælg **POL** i feltet **Land/område for part**. Vælg derefter **Indland** i feltet **Lande-/områdetype**.
8. Vælg **DEU** i feltet **Land/område for part**. Vælg derefter **EU** i feltet **Lande-/områdetype**.
9. Angiv **420000** i feltet **Momsfritagelsesnummer** i sektionen **Moms** i oversigtspanelet **Agent** under fanen **Agent**.
10. Angiv **Manish Chopra** i feltet **Navn** under fanen **Kontakt**.
11. Angiv **425-555-5068** i feltet **Telefon**.
12. Angiv **425-555-5049** i feltet **Faxnummer**.
13. Angiv **manishc@contoso.com** i feltet **Mail**.
14. I feltet **Nummerseriekode** til **xml-filnummer**-referencen under fanen **Nummerserier** skal du vælge **XML\_fil**.

### <a name="set-up-product-information"></a>Angive produktoplysninger

1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne** **produkter**.
2. Vælg **D0001** i gitteret.
3. Vælg **100 200 30** i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
4. Angiv **2** i feltet **Nettovægt** i sektionen **Vægtmålinger** i oversigtspanelet **Styr lager**.
5. Vælg **Gem** i handlingsruden.
6. Vælg **D0003** i gitteret.
7. Vælg **100 200 30** i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
8. Vælg **DEU** i feltet **Land/område** i sektionen **Oprindelse**.
9. Angiv **5** i feltet **Nettovægt** i sektionen **Vægtmålinger** i oversigtspanelet **Styr lager**.
10. Vælg **Gem** i handlingsruden.

### <a name="change-the-site-address"></a>Ændre adressen for webstedet

1. Gå til **Lagerstedsstyring** > **Konfiguration** > **Lagersted** > **Steder**.
2. Vælg **1** i gitteret.
3. Vælg **Rediger** i oversigtspanelet **Adresser**.
4. Vælg **POL** i feltet **Land/område** i dialogboksen **Rediger adresse**.
5. Vælg **OK**.

### <a name="set-up-a-transport-method"></a>Konfigurere en transportmetode

1. Opret en transportmetode.

    1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Transportmetode**.
    2. Gå til handlingsruden, og vælg **Ny**.
    3. Angiv **3** i feltet **Transport**.
    4. Indtast **Vejtransport** i feltet **Beskrivelse**.

2. Tildel den nye transportmåde en leveringsmåde. På denne måde kan du angive de standardværdier, der bruges til transportmåden, når den tilsvarende leveringsmåde er valgt.

    1. Gå til **Indkøb og forsyning** > **Opsætning** > **Distribution** > **Leveringsmåder**.
    2. Vælg **10** i gitteret.
    3. Vælg **3** i feltet **Transport** i oversigtspanelet **Udenrigshandel**.

3. Vælg standardleveringsmåden for en kunde.

    1. Gå til **Debitor** > **Kunder** > **Alle kunder**.
    2. Vælg **DE-016** i gitteret.
    3. Vælg **10** i feltet **Leveringsmåde** i oversigtspanelet **Faktura og levering**.

4. Vælg standardleveringsmåden for en leverandør.

    1. Gå til **Kreditor** > **Kreditorer** > **Alle kreditorer**.
    2. Vælg **DE-001** i gitteret.
    3. Vælg **10** i feltet **Leveringsmåde** i oversigtspanelet **Faktura og levering**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Konfigurere koder for leveringsbetingelser

1. Konfigurer en Intrastat-kode for leveringsbetingelserne.

    1. Gå til **Indkøb og forsyning** > **Opsætning** > **Distribution** > **Leveringsbetingelser**.
    2. Vælg **CIF** i gitteret.
    3. Angiv **CIF** i feltet **Intrastat-kode** i oversigtspanelet **Generelt**.

2. Vælg standardleveringsbetingelserne for en kunde.

    1. Gå til **Debitor** > **Kunder** > **Alle kunder**.
    2. Vælg **DE-016** i gitteret.
    3. Vælg **CIF** i feltet **Leveringsbetingelser** i oversigtspanelet **Faktura og levering**.

3. Vælg standardleveringsbetingelserne for en leverandør.

    1. Gå til **Kreditor** > **Kreditorer** > **Alle kreditorer**.
    2. Vælg **DE-001** i gitteret.
    3. Vælg **CIF** i feltet **Leveringsbetingelser** i oversigtspanelet **Faktura og levering**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>Verificere en EU-kundes kode for momsfritagelsesnummer

1. Gå til **Debitor** > **Kunder** > **Alle kunder**.
2. Vælg **DE-016** i gitteret.
3. Verificer, at feltet **Momsfritagelsesnummer** er angivet til **DE9012** i sektionen **Moms** i oversigtspanelet **Faktura og levering**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Oprette en salgsordre for en EU-kunde

1. Gå til **Debitor** > **Ordrer** > **Alle salgsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. I dialogboksen **Opret salgsordre** skal du i sektionen **Debitor** i feltet **Debitorkonto** i oversigtspanelet **Debitor** vælge **DE-016**.
4. Vælg **1** i feltet **Websted** i sektionen **Lagringsdimensioner** i oversigtspanelet **Generelt**.
5. Vælg **11** i feltet **Lagersted**.
6. Under fanen **Adresse** skal du kontrollere, at feltet **Adresse** er angivet til **Teichgasse 12, Kiel, 24103, DEU**, fordi kunden er fra Tyskland.
7. Vælg **OK**.
8. Under fanen **Overskrift** i oversigtspanelet **Levering** skal du kontrollere, at feltet **Leveringsbetingelser** er angivet til **CIF**, og at feltet **Leveringsmåde** er angivet til **10**.
9. Vælg **D0001** i feltet **Varenummer** i oversigtspanelet **Salgsordrelinjer** under fanen **Linjer**. Angiv derefter **8** i feltet **Antal**.
10. I oversigtspanelet **Linjedetaljer** under fanen **Udenrigshandel** skal du kontrollere, at feltet **Transaktionskode** er angivet til **11**, feltet **Vare** er angivet til **100 200 30**, og feltet **Oprindelsesland/-område** er angivet til **POL**.
11. Vælg **Gem** i handlingsruden.
12. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
13. I dialogboksen **Bogføringsfaktura** i oversigtspanelet **Parametre** i sektionen **Parameter** i feltet **Antal** skal du vælge **Alle**.
14. Vælg **10/18/2021** (18. oktober 2021) i feltet **Salgsdato** i oversigtspanelet **Opsætning**.
15. Vælg **OK** for at bogføre fakturaen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Overføre transaktionen til Intrastat-kladden og gennemse resultatet

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Overfør** i handlingsruden.
3. Angiv indstillingen **Debitorfaktura** til **Ja** i sekionen **Parametre** i dialogboksen **Intrastat (Overførsel)**.
4. Vælg **Filter**.
5. Vælg den første linje i dialogboksen **Intrastat-filter** under fanen **Interval**, og kontrollér, at feltet **Felt** er angivet til **Dato**.
6. Vælg dags dato i feltet **Kriterier**.
7. Vælg **OK** for at lukke dialogboksen **Intrastat-filter**.
8. Vælg **OK** for at lukke dialogboksen **Intrastat (Overførsel)** og gennemgå resultatet. Linjen repræsenterer den salgsordre, du har oprettet tidligere.

    ![Linje, der repræsenterer salgsordren på siden Intrastat](media/intrastat_pl_1.png)

9. Vælg transaktionslinjen, og vælg derefter fanen **Generelt** for at få vist flere detaljer.

    ![Salgsordredetaljer under fanen Generelt på Intrastat-siden](media/intrastat_pl_2.png)

10. Vælg **Output** > **Rapport** i handlingsruden.
11. Vælg den første dag i indeværende måned i feltet **Fra dato** i sektionen **Dato** i oversigtspanelet **Parametre** i dialogboksen **Intrastat-rapport**.
12. Angiv indstillingen **Generer** **fil** til **Ja** i sektionen **Eksportindstillinger**. Angiv derefter det krævede navn i feltet **Filnavn**.
13. Angiv indstillingen **Generer rapport** til **Ja**. Angiv derefter det krævede navn i feltet **Rapportfilnavn**.
14. Vælg **Udførsel** i feltet **Retning**.
15. Kontrollér, at feltet **Opgørelsestype** er angivet til **Opgørelse** i afsnittet **Filformattilknytning**.
16. Angiv **Krakow** i feltet **By for dokumentoprettelse**.
17. Vælg **10/19/2021** (19. oktober 2021) i feltet **Dato for dokumentoprettelse**.
18. Angiv **11** i feltet **Dokumentnummer**.
19. Angiv **22** i feltet **Dokumentversion**.
20. Vælg **OK**, og gennemse den rapport i XML-format, der er oprettet. Følgende tabel viser værdierne i eksempelrapporten.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Feltnavn</strong></p>
    </td>
    <td>
    <p><strong>Beskrivelse af felt</strong></p>
    </td>
    <td>
    <p><strong>Værdi</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Oplysninger om dokumentet</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Den dato, hvor dokumentet blev oprettet.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Den by, hvor dokumentet blev oprettet.</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Det samlede antal varer.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Den totale statistiske værdi.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Den totale fakturaværdi.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Enhedskoden.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Typen af erklæring.</p>
    </td>
    <td>
    <p>N</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Dokumentversionen.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Dokumentnummeret.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Referencemåneden.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Referenceåret.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>Rapportens retning.</p>
    </td>
    <td>
    <p>O</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>Erklæringens identifikator.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Oplysninger om firmaet</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>Den by, hvor firmaet har adresse.</p>
    </td>
    <td>
    <p>Warszawa</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>Firmaets Regon-kode.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Firmaets NIP-kode.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Firmaets postnummer.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Den gade, hvor firmaet har adresse.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Navnet på firmaet.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Tyskland</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Oplysninger om varen</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Den statistiske værdi.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Fakturaværdien.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Nettomassen.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>Kundens momsnummer.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Varekoden.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Transaktionskoden.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Leveringsmådens betingelser.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Koden for afsendelses- eller destinationsland eller -område.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>En beskrivelse af varerne.</p>
    </td>
    <td>
    <p>Hardware</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Varenummeret.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Kontaktpersonoplysninger</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-mail</p>
    </td>
    <td>
    <p>Afsenderens mailadresse.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Afsenderens faxnummer.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Afsenderens telefonnummer.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Afsenderens navn.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Gennemse den rapport i Excel-format, der er genereret.

    ![Intrastat-rapport for afsendelser](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Kreditor** > **Indkøbsordrer** > **Alle indkøbsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Gå til dialogboksen **Opret indkøbsordre**, og vælg **DE-001** i feltet **Kreditorkonto**.
4. Vælg **1** i feltet **Sted**.
5. Vælg **11** i feltet **Lagersted**.
6. Vælg **OK**.
7. Under fanen **Overskrift** i oversigtspanelet **Levering** skal du kontrollere, at feltet **Leveringsmåde** er angivet til **10**, og at feltet **Leveringsbetingelser** er angivet til **CIF**.
8. Vælg **D0003** i feltet **Varenummer** i oversigtspanelet **Indkøbsordrelinjer** under fanen **Linjer**. Angiv derefter **6** i feltet **Antal**.
9. I oversigtspanelet **Linjedetaljer** under fanen **Udenrigshandel** skal du kontrollere, at feltet **Transaktionskode** er angivet til **11**, feltet **Transport** er angivet til **3**, feltet **Vare** er angivet til **100 200 30**, og feltet **Oprindelsesland/-område** er angivet til **DEU**.
10. Vælg **Bekræft** i gruppen **Handlinger** under fanen **Indkøb** i handlingsruden.
11. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
12. Vælg **Standard fra** i handlingsruden og derefter **Bestilt antal** i feltet **Standardmængde for linjer**. Vælg derefter **OK**.
13. Angiv **00010** i feltet **Nummer** i sektionen **Fakturaidentifikation** i oversigtspanelet **Kreditorfakturahoved**.
14. Vælg daga dato i feltet **Fakturadato** i sektionen **Fakturadatoer**. Denne dato bruges til Intrastat-overførsel.
15. Vælg **10/18/2021** (18. oktober 2021) i feltet **Dato for dokumentmodtagelse**.
16. Vælg **Bogfør** i handlingsruden for at bogføre kladden.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Oprette en Intrastat-opgørelse for modtagelser

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Overfør** i handlingsruden.
3. Angiv indstillingen **Kreditorfaktura** til **Ja** i dialogboksen **Intrastat (Overførsel)**.
4. Vælg **OK** for at overføre transaktionerne, og gennemse derefter Intrastat-kladden.

    ![Linje, der repræsenterer indkøbsordren på siden Intrastat](media/intrastat_pl_4.png)

5. Gennemse oplysningerne under fanen **Generelt** for indkøbsordren.

    ![Detaljer om indkøbsordre under fanen Generelt på Intrastat-siden](media/intrastat_pl_5.png)

6. Vælg **Output** > **Rapport** i handlingsruden.
7. Vælg den første dag i indeværende måned i feltet **Fra dato** i sektionen **Dato** i oversigtspanelet **Parametre** i dialogboksen **Intrastat-rapport**.
8. Angiv indstillingen **Generer** **fil** til **Ja** i sektionen **Eksportindstillinger**. Angiv derefter det krævede navn i feltet **Filnavn**.
9. Angiv indstillingen **Generer rapport** til **Ja**. Angiv derefter det krævede navn i feltet **Rapportfilnavn**.
10. Vælg **Indførsel** i feltet **Retning**.
11. Kontrollér, at feltet **Opgørelsestype** er angivet til **Opgørelse** i afsnittet **Filformattilknytning**.
12. Angiv **Krakow** i feltet **By for dokumentoprettelse**.
13. Vælg **10/19/2021** (19. oktober 2021) i feltet **Dato for dokumentoprettelse**.
14. Angiv **11** i feltet **Dokumentnummer**.
15. Angiv **22** i feltet **Dokumentversion**.
16. Vælg **OK**, og gennemse den rapport i XML-format, der er oprettet. Følgende tabel viser værdierne i eksempelrapporten.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Feltnavn</strong></p>
    </td>
    <td>
    <p><strong>Beskrivelse af felt</strong></p>
    </td>
    <td>
    <p><strong>Værdi</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p style="text-align: center;"><strong>Oplysninger om dokumentet</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Den dato, hvor dokumentet blev oprettet.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Den by, hvor dokumentet blev oprettet.</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Det samlede antal varer.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Den totale statistiske værdi.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Den totale fakturaværdi.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Enhedskoden.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Typen af erklæring.</p>
    </td>
    <td>
    <p>N</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Dokumentversionen.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Dokumentnummeret.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Referencemåneden.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Referenceåret.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>Rapportens retning.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>Erklæringens identifikator.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p style="text-align: center;"><strong>Oplysninger om firmaet</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>Den by, hvor firmaet har adresse.</p>
    </td>
    <td>
    <p>Warszawa</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>Firmaets Regon-kode.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Firmaets NIP-kode.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Firmaets postnummer.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Den gade, hvor firmaet har adresse.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Navnet på firmaet.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Tyskland</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p style="text-align: center;"><strong>Oplysninger om varen</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Den statistiske værdi.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Fakturaværdien.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Nettomassen.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>Koden for oprindelseslandet eller -området.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Koden for transportmåden.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Varekoden.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Transaktionskoden.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Leveringsmådens betingelser.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Koden for afsendelses- eller destinationsland eller -område.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>En beskrivelse af varerne.</p>
    </td>
    <td>
    <p>Hardware</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Varenummeret.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p style="text-align: center;"><strong>Kontaktpersonoplysninger</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-mail</p>
    </td>
    <td>
    <p>Afsenderens mailadresse.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Afsenderens faxnummer.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Afsenderens telefonnummer.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Afsenderens navn.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Gennemse den rapport i Excel-format, der er genereret.

    ![Intrastat-rapport for modtagelser](media/intrastat_pl_6.png)
