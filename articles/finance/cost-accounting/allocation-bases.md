---
title: Fordelingsgrundlag
description: Dette emne indeholder oplysninger om fordelingsgrundlag. Fordelingsgrundlag er centrale komponenter i omkostningsregnskabet og bruges oftest til at fordele faste omkostninger.
author: AndersGirke
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMAllocationBaseDetail, CAMFormulaAllocationBaseDetail, CAMAllocationBasePreview, CAMAllocationBase, CAMCostAllocationRule, CAMPredefinedMemberAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 223174
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 15155a987094da6047dea9245f543b5ed38e3680
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814050"
---
# <a name="allocation-bases"></a>Fordelingsgrundlag 

[!include [banner](../includes/banner.md)]

Et fordelingsgrundlag er det grundlag, som omkostningsregnskabet fordeler faste omkostninger på. Et fordelingsgrundlag kan være et antal, som f.eks. maskintimer, der bruges, kilowatttimer (kWh), der forbruges eller areal, der er optaget. Fordelingsgrundlag bruges oftest til at tildele faste omkostninger til lager, der er produceret. F.eks. fordeler en IT-afdeling sine udgifter i overensstemmelse med antallet af computere, som hver afdeling bruger.

Der findes tre typer fordelingsgrundlag i omkostningsregnskab:

- Foruddefinerede fordelingsbaser for dimensionsmedlem
- Fordelingsbaser for hierarkier
- Fordelingsbaser for formler

## <a name="predefined-dimension-member-allocation-bases"></a>Foruddefinerede fordelingsbaser for dimensionsmedlem

De foruddefinerede fordelingsgrundlag for dimensionsmedlemmer oprettes automatisk, når der oprettes et dimensionsmedlem af en af følgende typer:

- Statistiske dimensionsmedlemmer
- Dimensionsmedlemmer for omkostningselement

> [!NOTE]
> De foruddefinerede fordelingsgrundlag for dimensionsmedlemmer, der er baseret på et dimensionsmedlem for omkostningselement overvejer kun værdierne fra udbyderen af datakilden, f.eks. finans eller budget.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>Eksempel 1: Bruge et dimensionsmedlem for omkostningselement som fordelingsgrundlag
Dette eksempel viser, hvordan du opretter en regel for omkostningsfordeling for at fordele omkostningselement 10002 (medarbejderforsikring) til den saldo, der er registreret på omkostningselement 10001 (lønninger). Fordelingsreglen defineres baseret på forholdet mellem hver afdelings lønninger og de samlede lønninger. (Kræver gennemsyn!)

Kontoplanen defineres på følgende måde i de relevante finanskonti.

| Kontoplan | Hovedkonto | Beskrivelse        | Hovedkontotype |
|------------------|--------------|--------------------|-------------------|
| Delt           | 10001        | Lønninger           | Udgift           |
| Delt           | 10002        | Medarbejderforsikring | Udgift           |

Definer en omkostningselementdimension, og konfigurer dataconnectoren. Når dataene er importeret, oprettes følgende poster i omkostningsregnskabet.

**Dimensionsmedlemmer for omkostningselement**

| Navn på dimension for omkostningselement | Omkostningselement |  Beskrivelse       | Type    |
|-----------------------------|--------------|--------------------|---------|
| Omkostningselementer               | 10001        | Lønninger           | Primær |
| Omkostningselementer               | 10002        | Medarbejderforsikring | Primær |

**Foruddefinerede fordelingsgrundlag for dimensionsmedlem** 

| Navn  | Beskrivelse        | Dimension for omkostningselement |
|-------|--------------------|------------------------|
| 10001 | Lønninger           | Omkostningselementer          |
| 10002 | Medarbejderforsikring | Omkostningselementer          |

Følgende poster er blevet bogført i finansmodulet:

- De poster, der viser Lønninger-hovedkontoen, stammer fra lønsystemet og bogføres i bærere.
- Udgifterne for medarbejderforsikring bogføres manuelt til en standardbærer.

| Regnskabsdato | Bærer |  Beskrivelse        | Hovedkonto |  Beskrivelse       | Beløb i regnskabsvaluta |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 01-03-2017      | CC001       | HR                  | 10001        | Lønninger           | 2.000,00                      |
| 01-03-2017      | CC002       | FI                  | 10001        | Lønninger           | 5.000,00                      |
| 01-03-2017      | CC003       | LO                  | 10001        | Lønninger           | 3.000,00                      |
| 01-03-2017      | CC099       | Standardbærer | 10002        | Medarbejderforsikring | 1.000,00                      |

Når kildedataene for finansposter er behandlet, oprettes følgende poster i omkostningsregnskabet.

**Omkostningsposter**

| Omkostningsobjekt |  Beskrivelse        | Omkostningselement  |  Beskrivelse       | Funktionalitet af omkostning   |Beløb|Regnskabsdato|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | HR                  | 10001         | Lønninger           | Ikke-klassificerede    |2.000,00|  01-03-2017    |
| CC002       | FI                  | 10001         | Lønninger           | Ikke-klassificerede    |5.000,00|     01-03-2017         |
| CC003       | LO                  | 10001         | Lønninger           | Ikke-klassificerede    |3.000,00|      01-03-2017        |
| CC099       | Standardbærer | 10002         | Medarbejderforsikring | Ikke-klassificerede    |1.000,00|      01-03-2017       |

I dette forenklede eksempel er der oprettet en regel for omkostningsfordeling for at fordele omkostningselement 10002 (medarbejderforsikring) i forhold til den saldo, der er registreret på omkostningselement 10001 (lønninger).

**Regel for omkostningsfordeling**

| Dimensionshierarkinode for omkostningsobjekt | Dimensionshierarkinode for omkostningselement | Funktionalitet af omkostning | Tildelingsgrundlag |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Ikke-klassificerede  | 10001           |

**Udfør beregning af fast omkostning**

Når omkostningselementet 10001 (lønninger) anvendes som fordelingsbasis, er resultatet af beregningen af faste omkostninger følgende.

| Omkostningsobjekt | Beskrivelse | Størrelsesorden |   Fordelingsfaktor         | Beløb |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | HR          | 2.000     | (2.000 ÷ 10.000) × 1.000,00 | 200,00 |
| CC002       | FI          | 5.000     | (5.000 ÷ 10.000) × 1.000,00 | 500,00 |
| CC003       | LO          | 3.000     | (3.000 ÷ 10.000) × 1.000,00 | 300,00 |

**Kladde**

| Kladden | Kladdetype                          | Regnskabskalenderperiode | År | Termin   | Version                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Beregningskladde for omkostningsfordeling | Regnskabsår                 | 2017 | 1. Periode | Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1 |

**Kladdeposteringer for omkostningsobjektsaldo**

| Regnskabsdato | Omkostningsobjekt | Beskrivelse         | Omkostningselement | Beskrivelse        | Funktionalitet af omkostning |  Beløb  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 01-31-2017      | CC099       | Standardbærer | 10002        | Medarbejderforsikring | Ikke-klassificerede  | 1.000,00 |

**Omkostningsposter**

| Omkostningsobjekt |  Beskrivelse        | Omkostningselement |    Beskrivelse     | Funktionalitet af omkostning | Beløb    | Regnskabsdato |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Standardbærer | 10002        | Medarbejderforsikring | Ikke-klassificerede  | -1.000,00 | 01-31-2017      |
| CC001       | HR                  | 10002        | Medarbejderforsikring | Ikke-klassificerede  | 200,00    | 01-31-2017      |
| CC002       | FI                  | 10002        | Medarbejderforsikring | Ikke-klassificerede  | 500,00    | 01-31-2017      |
| CC099       | LO                  | 10002        | Medarbejderforsikring | Ikke-klassificerede  | 300,00    | 01-31-2017      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>Eksempel 2: Bruge et statistisk dimensionsmedlem som fordelingsgrundlag

Statistiske dimensionsmedlemmer kan bruges som fordelingsgrundlag til at definere politikker eller ikke-pengemæssigt forbrug i en rapport af omkostningsobjekter. Du kan manuelt oprette statistiske dimensionsmedlemmer eller importere dem fra en fil ved hjælp af værktøjet til import/eksport i Datastyring.

**Statistiske dimensionsmedlemmer**

| Navn på statistisk dimension | Statistisk element | Beskrivelse               | Enhed |
|----------------------------|---------------------|---------------------------|------|
| Statistiske elementer       | Fuldtidsansat                 | Fuldtidsmedarbejdere       | Styk   |
| Statistiske elementer       | Elektricitet         | Forbrug af elektricitet   | kWh  |

Når et statistisk dimensionsmedlem er gemt, oprettes der en tilsvarende post i det foruddefinerede fordelingsgrundlag for dimensionsmedlem.

**Foruddefinerede fordelingsgrundlag for dimensionsmedlem**

| Navn        | Beskrivelse             | Dimension for statistisk element |
|-------------|-------------------------|-------------------------------|
| Fuldtidsansat         | Fuldtidsmedarbejdere     | Statistiske elementer          |
| Elektricitet | Forbrug af elektricitet | Statistiske elementer          |

Statistiske målinger kan komme fra forskellige kilder:

- Elforbrug kan måles af målere, der er installeret i forskellige områder af virksomheden.
- Tabeller indeholder statistiske målinger. F.eks. indeholder HcmEmployment-tabellen en liste over alle medarbejdere og de bærere, de arbejder for.

| Navn       | Bærer |  Beskrivelse  | Medarbejdertype |
|------------|-------------|----|-------------|
| Medarbejder A | CC001       | HR | Medarbejder    |
| Medarbejder B | CC002       | FI | Medarbejder    |
| Medarbejder C | CC002       | FI | Medarbejder    |
| Medarbejder D | CC003       | LO | Medarbejder    |
| Medarbejder F | CC003       | LO | Medarbejder    |

> [!NOTE]
> Alle de tabeller, der indeholder økonomiske dimensioner, kan bruges som kilder for statistiske målinger.

Omkostningsregnskabet understøtter en række statistiske målinger ved hjælp af følgende dataforbindelser:

- Værktøj til import/eksport i Datastyring
- Statistiske målinger

Når du vil udtrække statistiske målinger fra systemet, kræver det en skabelon til provider af statistisk målinger. Du kan finde flere oplysninger under Skabelon til providere af statistiske målinger. (Tilføjer et hyperlink, når dette emne er skrevet).

**Skabeloner til providere af statistiske målinger**

| Navn  | Funktion | Kildetabel  | Sumfelt      | Datofelt     |
|-------|----------|---------------|----------------|----------------|
| Fuldtidsansatte | Antal    | HcmEmployment | Ikke tilgængelig | Ikke tilgængelig |

Når kildedataene for statistiske målinger er behandlet, oprettes følgende poster i omkostningsregnskabet.

**Statistiske poster**

| Omkostningsobjekt | Beskrivelse      | Regnskabsdato | Statistisk dimensionsmedlem | Beskrivelse         | Størrelsesorden |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR               | 01-31-2017      | Fuldtidsansatte                        | Fuldtidsmedarbejdere | 1,00      |
| CC002       | FI               | 01-31-2017      | Fuldtidsansatte                        | Fuldtidsmedarbejdere | 2.00      |
| CC003       | LO               | 01-31-2017      | Fuldtidsansatte                        | Fuldtidsmedarbejdere | 2.00      |

Her er et eksempel på en regel til fordeling af omkostninger, hvis den foruddefinerede fordelingsbasis for dimensionsmedlem for Fuldtidsansatte er tildelt som fordelingsgrundlag i den.

| Omkostningsobjekt | Beskrivelse  | Størrelsesorden | Fordelingsfaktor |
|-------------|------|-----------|-------------------|
| CC001       | Human Resources   | 1,00      | (1/5) × beløb    |
| CC002       | FI   | 2.00      | (2/5) × beløb    |
| CC003       | LO   | 2.00      | (2/5) × beløb    |

Du kan bruge dataobjektet Importerede statistiske målinger til at importere statistiske målinger til omkostningsregnskabet. Du kan også bruge værktøjet til import/eksport i Datastyring. I Excel registreres forbruget af elektricitet på følgende måde.

| Regnskabsdato | Dimensionsmedlem | Størrelsesorden | Kildeidentifikator |
|-----------------|------------------|-----------|-------------------|
| 01-31-2017      | CC001            | 2,450.00  | Elektricitet       |
| 31-01-2017      | CC002            | 4,100.00  | Elektricitet       |
| 01-31-2017      | CC003            | 15.000,00 | Elektricitet       |

Når kildedataene for statistiske målinger er behandlet, oprettes følgende poster i omkostningsregnskabet.

**Statistiske poster**

| Omkostningsobjekt |    | Regnskabsdato | Statistisk dimensionsmedlem |    Beskrivelse          | Størrelsesorden |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Human Resources | 31-01-2017      | Elektricitet                  | Forbrug af elektricitet | 2,450.00  |
| CC002       | FI | 31-01-2017      | Elektricitet                  | Forbrug af elektricitet | 4,100.00  |
| CC003       | LO | 01-31-2017      | Elektricitet                  | Forbrug af elektricitet | 15.000,00 |

Her er et eksempel på en regel til fordeling af omkostninger, hvis den foruddefinerede fordelingsbasis for dimensionsmedlem for Elektricitet er tildelt som fordelingsgrundlag i den.

| Omkostningsobjekt | Beskrivelse  | Størrelsesorden | Fordelingsfaktor          |
|-------------|------|-----------|----------------------------|
| CC001       | HR   | 2,450.00  | (2.450 ÷ 21.550) × beløb  |
| CC002       | FI   | 4,100.00  | (4.100 ÷ 21.550) × beløb  |
| CC003       | LO   | 15.000,00 | (15.000 ÷ 21.550) × beløb |

## <a name="hierarchy-allocation-bases"></a>Fordelingsbaser for hierarkier

Bogholdere kan manuelt oprette hierarkiets fordelingsgrundlag ved at anvende en dimensionshierarkinode for et omkostningsobjekt på et eksisterende fordelingsgrundlag. På denne måde kan du begrænse omfanget af det oprindelige foruddefinerede fordelingsgrundlag for dimensionsmedlem. Et foruddefineret fordelingsgrundlag for dimensionsmedlem kan bruges til at oprette flere fordelingsbaser for hierarkier. Områder kan vedligeholdes i det dimensionshierarki for omkostningsobjekt, der er tilknyttet fordelingsbaser for hierarkiet.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Eksempel: Fordelingsbaser for hierarki, der er baseret på fuldtidsmedarbejdere i organisationen
Her er et eksempel på et dimensionshierarki for omkostningsobjekt, der kan oprettes for at beskrive en forenklet organisation.

| Hierarkinavn | Nodeniveau 0 | Nodeniveau 1 | Nodeniveau 2 | Dimensionsmedlemmer |
|----------------|--------------|--------------|--------------|-------------------|
| Organisation   | Administrerende direktør          | Regnskabsdirektør          | FICO         | CC001             |
| Organisation   | Administrerende direktør          | Regnskabsdirektør          | HR           | CC002             |
| Organisation   | Administrerende direktør          | Informationschef          | LO           | CC003             |

Det oprindelige foruddefinerede fordelingsgrundlag for dimensionsmedlemmer for Fuldtidsansatte, som blev oprettet i det forrige afsnit, indeholder følgende poster.

**Statistiske poster**

| Omkostningsobjekt | Beskrivelse  | Regnskabsdato | Statistisk dimensionsmedlem | Beskrivelse | Størrelsesorden |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR   | 01-31-2017      | Fuldtidsansatte                        | Fuldtidsmedarbejdere | 1,00      |
| CC002       | FI   | 01-31-2017      | Fuldtidsansatte                        | Fuldtidsmedarbejdere | 2.00      |
| CC003       | LO   | 01-31-2017      | Fuldtidsansatte                        | Fuldtidsmedarbejdere | 2.00      |

En omkostning skal fordeles mellem bærere, der rapporterer til organisationens regnskabsdirektør. Det er almindeligt anerkendt, at det korrekte fordelingsforhold er antallet af fuldtidsansatte (fuldtidsmedarbejdere) pr. bærer.

**Fordelingsbaser for hierarkier**

| Navn                  | Tildelingsgrundlag | Dimensionshierarki for omkostningsobjekt | Dimensionshierarkinode for omkostningsobjekt |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| Antal fuldtidsansatte under Regnskabsdirektør | Fuldtidsansatte           | Organisation                    | Regnskabsdirektør                                  |

Med en eksempelfunktion kan du validere fordelingsbasis for det hierarki, der er oprettet, baseret på statistiske poster i systemet.

**Oplysninger om fordelingsbasis**

| Omkostningsobjekt | Beskrivelse  |  Størrelsesorden |
|-------------|------|------------|
| CC001       | HR   | 1,00       |
| CC002       | FI   | 2.00       |

Her er et eksempel på en regel til fordeling af omkostninger, hvis fordelingsbasis i Antal fuldtidsansatte under Regnskabsdirektør er tildelt som fordelingsgrundlag i den.

| Omkostningsobjekt | Beskrivelse  | Størrelsesorden | Fordelingsfaktor |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1,00      | (1/3) × beløb    |
| CC002       | FI   | 2.00      | (2/3) × beløb    |

## <a name="formula-allocation-bases"></a>Fordelingsbaser for formler

Med fordelingsbaser for formler kan du definere særlige formler for at opnå den korrekte fordelingsbasis. Du kan manuelt oprette fordelingsbaser for formler.

Når du opretter en fordelingsbase for en formel, kan du vælge, hvilken statistisk dimension og dimension for omkostningselement der skal være grundlag for formlen. Alle fordelingsbaser, som kommer fra de tidligere valgte dimensioner, kan bruges i en fordelingsbasis for formlen.

> [!NOTE]
> Tidligere definerede fordelingsbaser for formler kan bruges til at definere en ny fordelingsbasis for formlen.

I Fordelingsbasisfaktor for formel opretter du et alias og tilknytter det til enten en fordelingsbasis eller en konstant. Aliaserne bruges derefter til at definere formlen.

Du kan bruge følgende operatorer til at definere formlen.

| Symboler | Tekst           |
|---------|----------------|
| ( )     | Parenteser    |
| \<      | Mindre end   |
| \>      | Større end    |
| +       | Tilføjelse       |
| –       | Subtraktion    |
| \*      | Multiplikation |

Traditionelle **IF**-sætninger understøttes ikke. Du kan dog oprette sætninger og kontrollere, om de er sande.

| Sætning | Validering | Resultat |
|-----------|------------|--------|
| a \> b    | Sand       | 1      |
| a \> b    | Falsk      | 0      |

### <a name="example-1-a-simple-formula"></a>Eksempel 1: En simpel formel

Elektricitetsregninger består ofte af to dele:

- Et fast gebyr for at være forbundet med gitteret
- En omkostning, der er knyttet til forbruget pr. kWh

Den foruddefinerede fordelingsbasis for dimensionsmedlem for Elektricitet er allerede defineret og indeholder disse værdier.

**Statistiske poster**

| Omkostningsobjekt | Navn | Regnskabsdato | Statistisk dimensionsmedlem | Beskrivelse             | Størrelsesorden |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Human Resources   | 31-01-2017      | Elektricitet                  | Forbrug af elektricitet | 2,450.00  |
| CC002       | FI   | 31-01-2017      | Elektricitet                  | Forbrug af elektricitet | 4,100.00  |
| CC003       | LO   | 01-31-2017      | Elektricitet                  | Forbrug af elektricitet | 15.000,00 |

Hvis det faste gebyr nu skal fordeles jævnt over omkostningsobjekter, der forbruger elektricitet, har du to muligheder for fordeling af omkostningerne:

- Oprette en ny foruddefineret fordelingsbasis, elektricitet, der er fastsat, og derefter anvende en statistisk måling på 1,00 for hvert omkostningsobjekt, der har forbrugt elektricitet.
- Oprette en fordelingsbasis for formlen, elektricitet, der er fastsat, som udnytter den foruddefinerede fordelingsbasis for Elektricitet, der allerede er defineret i systemet. Fordelen ved denne mulighed er, at data kun skal indlæses i omkostningsregnskabet for ét statistisk dimensionsmedlem for Elektricitet.

**Fordelingsbasis for formel** 

| Navn              | Dimension for omkostningselement | Statistisk dimension | Formel |
|-------------------|------------------------|-----------------------|---------|
| Elektricitet, der er fastsat |                        | Statistiske elementer  |         |

Før feltet **Formel** kan udfyldes, skal du angive det alias, der skal bruges i formlen.

**Fordelingsbasisfaktorer for formel**

| Alias | Konstant | Tildelingsgrundlag |
|-------|----------|-----------------|
| a     |          | Elektricitet     |
| b     | 0,01     |                 |

Bemærk, at 0 (nul) ikke understøttes som en konstant.

**Fordelingsbasis for formel**

| Navn              | Dimension for omkostningselement | Statistisk dimension | Formel |
|-------------------|------------------------|-----------------------|---------|
| Elektricitet, der er fastsat |                        | Statistiske elementer  | a \> b  |

Med en eksempelfunktion kan du validere den fordelingsbasis for formlen, der er oprettet, baseret på statistiske poster i systemet.

**Oplysninger om fordelingsbasis**

| Omkostningsobjekt | Beskrivelse  | Formel           | Størrelsesorden |
|-------------|------|-------------------|-----------|
| CC001       | HR   | 2.450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1,00      |
| CC003       | LO   | 15.000,00 \> 0,01 | 1,00      |

Her er et eksempel på en regel til fordeling af omkostninger, hvis fordelingsbasis for formlen for Elektricitet er tildelt som fordelingsgrundlag i den.

**Fordelingsfaktor for størrelsesorden af omkostningsobjekt**

| Omkostningsobjekt | Navn | Størrelsesorden |  Fordelingsfaktor |
|-------------|------|-----------|--------------------|
| CC001       | HR   | 1,00      | (1/3) × beløb     |
| CC002       | FI   | 1,00      | (1/3) × beløb     |
| CC003       | LO   | 1,00      | (1/3) × beløb     |

### <a name="example-2-an-advanced-formula"></a>Eksempel 2: En særlig formel
I dette eksempel skal prisen på elektricitet ikke blot følge den faktiske elektricitet, der forbruges i kWh. Ledelsen ønsker at inkorporere et incitament til at sænke forbruget af elektricitet. 

| Regel              | Kurs | 
|-------------------|------|
| a < = 10000,00 kWh | 0.75 |
| a > 10000,00 kWh  | 1.15 |

Der oprettes en ny fordelingsbasis for formlen, Forbrug af elektricitet.

**Fordelingsbasis for formel**

| Navn              | Dimension for omkostningselement | Statistisk dimension | Formel |
|-------------------|------------------------|-----------------------|---------|
| Forbrug af elektricitet |                        | Statistiske elementer  |         |

Før feltet **Formel** kan udfyldes, skal du angive det alias, der skal bruges i formlen.

**Fordelingsbasisfaktorer for formel**

| Alias | Konstant  | Tildelingsgrundlag |
|-------|-----------|-----------------|
| a     |           | Elektricitet     |
| b     | 10.000,00 |                 |
| k     | 0.75      |                 |
| d     | 1.15      |                 |

**Fordelingsbasis for formel**

| Navn              | Dimension for omkostningselement | Statistisk dimension | Formel                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Elektricitet, der er fastsat |                        | Statistiske elementer  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Med en eksempelfunktion kan du validere den fordelingsbasis for formlen, der er oprettet, baseret på statistiske poster i systemet.

**Oplysninger om fordelingsbasis**

| Omkostningsobjekt |    | Formel                                                                                                                             | Størrelsesorden |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | HR | ((2.450,00 \> 10.000,00) × ((10.000,00 × 0,75) + (2.450,00 – 10.000,00) × 1,15)) + ((2.450,00 \<= 10.000,00) × 2.450,00 × 0,75)     | 1,837.50  |
| CC002       | FI | ((4.100,00 \> 10,000,00) × ((10.000,00 × 0,75) + (4.100,00 – 10.000,00) × 1,15)) + ((4.100,00 \<= 10.000,00) × 4.100,00 × 0,75)     | 3,075.00  |
| CC003       | LO | ((15.000,00 \> 10,000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) | 1,3250.00 |

Her kan du se nærmere på formlen for CC003 (LO):

((15.000,00 \> 10.000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) = 13.250,00

(1 × (7.500,00 + 5.000,00 × 1,15)) + (0 × 15.000,00 × 0,75)            

1 × 7.500,00 + 5.750,00 + 0 

Her er et eksempel på en regel til fordeling af omkostninger, hvis fordelingsbasis for formlen for Elektricitet, der er fastsat, er tildelt som fordelingsgrundlag i den.


| Omkostningsobjekt | Beskrivelse | Størrelsesorden |        Fordelingsfaktor         |
|-------------|-------------|-----------|----------------------------------|
|    CC001    |     HR      | 1,837.50  | (1.837,50 ÷ 18.162,50) × beløb  |
|    CC002    |     FI      | 3,075.00  | (3.075,00 ÷ 18.162,50) × beløb  |
|    CC003    |     LO      | 13,250.00 | (13.250,00 ÷ 18.162,50) × beløb |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]