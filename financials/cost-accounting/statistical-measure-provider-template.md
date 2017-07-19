---
title: "Skabeloner for statistiske dimensionsmedlemmer og providere af statistiske målinger"
description: "Dette emne indeholder oplysninger om skabeloner for statistiske dimensionsmedlemmer og providere af statistiske målinger. Statistiske dimensionsmedlemmer kan bruges som fordelingsbasis i politikker som f.eks. omkostningsdistribution og omkostningsfordeling. De kan også bruges til at rapportere forbrug af ikke-pengemæssige omkostninger."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 180863b5c3b8fe7870ab58f3849e52583f5880c1
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Skabeloner for statistiske dimensionsmedlemmer og providere af statistiske målinger

[!include[banner](../includes/banner.md)]

En statistisk dimension og dens medlemmer bruges til registrering og kontrol af ikke-pengemæssige poster i omkostningsregnskab. Statistiske dimensionsmedlemmer kan bruges til to formål:

- Som fordelingsbasis i politikker, f.eks. omkostningstildeling eller omkostningsdistribution
- Til rapportering af ikke-pengemæssigt forbrug

## <a name="statistical-dimension"></a>Statistisk dimension

En statistisk dimension har et entydigt navn og en række entydige dimensionsmedlemmer. Den statistiske dimension er tildelt et finanspost-id for omkostningsregnskab. Denne relation knytter alle tilsvarende statistiske dimensionsmedlemmer til finansposten for omkostningsregnskab. Derfor oprettes alle statistiske poster i konteksten af finansposten for omkostningsregnskab.

> [!NOTE]
> Den statistiske dimension kan tildeles mere end én finanspost for omkostningsregnskab.

Her er et eksempel på en statistisk dimension.

| Navn                        | Dataconnector for dimensionsmedlemmer |
|-----------------------------|--------------------------------------|
| Delte statistiske elementer | Importerede dimensionsmedlemmer           |

Her er et eksempel på en statistisk dimension, der er tildelt til en finanskonto i omkostningsregnskab.

| Navn                  | Regnskabsvaluta | Valutakurstype | Regnskabskalender | Dimension for omkostningselement | Statistisk dimension       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Ledelsesregnskab | USD                 | Konstant valuta  | Regnskabsperiode   | Delte omkostningselementer   | Delte statistiske elementer |

## <a name="statistical-dimension-members"></a>Statistiske dimensionsmedlemmer

Et statistisk dimensionsmedlem udgør en enhed, som du vil registrere ikke-pengemæssige målinger til. Disse målinger kan bruges som en fordelingsbasis eller blot til ikke-pengemæssige værdier i rapporter.

Statistiske dimensionsmedlemmer kan oprettes manuelt. De kan også importeres fra en fil ved hjælp af Datastyring-værktøjet til import/eksport.

Et statistisk dimensionsmedlem bliver automatisk en foruddefineret fordelingsbasis. Den kan bruges som fordelingsbasis i politikker eller som input i andre typer fordelingsbaser.

Her er nogle eksempler på typiske statistiske dimensionsmedlemmer.

| Navn på statistisk dimension  | Statistiske elementer | Betegnelse             | Enhed |
|-----------------------------|----------------------|-------------------------|------|
| Delte statistiske elementer | Fuldtidsansat                  | Fuldtidsmedarbejdere     | Styk  |
| Delte statistiske elementer | Elektricitet          | Forbrug af elektricitet | kWh  |
| Delte statistiske elementer | Pakke-CC              | Emballagebærer   | Timer |

## <a name="statistical-measure-provider-template"></a>Skabelon til provider af statistiske målinger

Statistiske målinger kan stamme fra mange forskellige kilder. Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, er en fremragende kilde til at udtrække statistiske målinger fra. Du kan bruge en provider-skabelon for statistisk målinger til nemt at konfigurere de statistiske målinger, som du vil udtrække.

Definitionen af en provider-skabelon til statistiske målinger er generisk og kan genbruges i flere statistiske dimensionsmedlemmer.

> [!NOTE]
> Alle tabeller, der indeholder økonomiske dimensioner, kan bruges som kilder til statistiske målinger.

**Eksempel: Antal medarbejdere pr. bærer**

Antallet af medarbejdere pr. bærer er en statistisk måling, der kan bruges til forskellige formål, der giver ledelsesmæssig indsigt:

- En statistisk rapporteringsmåling pr. bærer
- En fordelingsbasis til forskellige former for udgifter
- Interne omkostningssatser efter bærer:

    - Omkostning pr. medarbejder
    - Indtægt pr. medarbejder.

HcmEmployment-tabellen indeholder en liste over alle medarbejdere i forekomsten. Denne tabel er en global tabel. Derfor er posterne ikke relateret til et bestemt dataområde-id.

Her er et eksempel på medarbejdere i HcmEmployment-tabellen.

| Navn       | Bærer | Betegnelse   | Medarbejdertype |
|------------|-------------|----|-------------|
| Medarbejder 1 | CC001       | Personale | Medarbejder    |
| Medarbejder 2 | CC002       | FI | Medarbejder    |
| Medarbejder 3 | CC002       | FI | Medarbejder    |
| Medarbejder 4 | CC003       | LO | Medarbejder    |
| Medarbejder 5 | CC003       | LO | Medarbejder    |
| Medarbejder 6 | CC002       | FI | Kontrahent  |

Når du opretter en post i en **skabelon til provider af statistiske målinger**, skal du beslutte, hvilken funktion du skal bruge:

- **Antal** – En optælling af poster pr. omkostningsobjekt overføres.
- **Sum** – En sum af poster pr. omkostningsobjekt overføres. (Feltet **Sum** og feltet **Dato** er obligatorisk).

## <a name="using-the-count-function"></a>Brug af funktionen Antal

F.eks. kan en skabelon til provider af statistiske målinger konfigureres på følgende måde.

| Navn  | Funktion | Kildetabel  | Sumfelt      | Datofelt     |
|-------|----------|---------------|----------------|----------------|
| Fuldtidsansatte  | Antal    | HcmEmployment | Ikke tilgængelig | Ikke tilgængelig |

Du kan også tilføje en eller flere afgrænsninger for at indsnævre målingerne fra kildetabellen.

I dette eksempel, hvis du kun vil have en optælling af alle medarbejdere på fuld tid (fuldtidsansatte), kan du tilføje en afgrænsning i feltet **Arbejdertype**. I feltet **Kriterier** skal du vælge **Medarbejder** for at begrænse outputtet på følgende måde.

**Afgrænsninger**

| Kildetabel  | Felt       | Afgrænsning |
|---------------|-------------|----------|
| HcmEmployment | Medarbejdertype | Medarbejder |

Før du kan få statistiske målinger i omkostningsregnskabet, skal du oprette relationen mellem skabelonen til provider af statistisk måling og det statistiske dimensionsmedlem. Denne relation oprettes pr. finanspost for omkostningsregnskab og version. Relationen består af en dataconnector og en dataprovider. Du kan have flere dataconnectorer og dataprovidere pr. statistiske dimensionsmedlem.

> [!NOTE]
> I dette eksempel skal du oprette en relation for den **faktiske version**.

Gå til **Finanspost for omkostningsregnskab** \> **Faktisk version** \> **Administrer** \> **Statistiske målinger** for at oprette relationen. I dette scenarie skal du vælge **Dynamics 365 for Finance and Operations, Enterprise edition – Statistiske målinger** som dataconnector for at udtrække data fra Finance and Operations.

**Datakilde**

| Navn        | Dataconnector                                                                     | Statistisk dimensionsmedlem |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| Fuldtidsansatte D365FO | Dynamics 365 for Finance and Operations, Enterprise edition – Statistiske målinger | Fuldtidsansatte                         |

**Konfiguration af dataprovider**

| Navn på statistisk skabelon |
|---------------------------|
| Fuldtidsansatte                      |

Når kildedataene for statistiske målinger er behandlet, oprettes følgende statistiske poster i omkostningsregnskabet.

**Kladde**

| Kladden | Kladdetype                       | Regnskabskalenderperiode | År   |  Termin  |  Version | Dataconnector-kildeposter|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Overførselskladde for statistisk post | Regnskabsår                 | 2017   | 1. Periode | CA-finans-USMF | Fuldtidsansatte                   |

**Overførselskladdeposteringer for statistisk post**

| Regnskabsdato | Størrelsesorden | Statistisk element |   Betegnelse       | Bærer |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31-01-2017      | 1,00      | Fuldtidsansatte                | Fuldtidsmedarbejdere | CC001       |
| 31-01-2017      | 2.00      | Fuldtidsansatte                | Fuldtidsmedarbejdere | CC002       |
| 31-01-2017      | 2.00      | Fuldtidsansatte                | Fuldtidsmedarbejdere | CC003       |

**Statistiske poster**

| Omkostningsobjekt |    | Regnskabsdato | Statistisk dimensionsmedlem |  Betegnelse        | Størrelsesorden |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personale | 31-01-2017      | Fuldtidsansatte                         | Fuldtidsmedarbejdere | 1,00      |
| CC002       | FI | 31-01-2017      | Fuldtidsansatte                         | Fuldtidsmedarbejdere | 2.00      |
| CC003       | LO | 31-01-2017      | Fuldtidsansatte                         | Fuldtidsmedarbejdere | 2.00      |

Hvis de fuldtidsansattes foruddefinerede fordelingsbasis for dimensionsmedlemmer tildeles som en fordelingsbasis i en regel til fordeling af omkostninger, fordeles omkostningerne ved hjælp af følgende fordelingsfaktor.

| Omkostningsobjekt | Betegnelse    | Størrelsesorden | Fordelingsfaktor |
|-------------|----|-----------|-------------------|
| CC001       | Personale | 1,00      | (1/5) × beløb    |
| CC002       | FI | 2.00      | (2/5) × beløb    |
| CC003       | LO | 2.00      | (2/5) × beløb    |

## <a name="using-the-sum-function"></a>Brug af funktionen Sum

En produktionsbærer, CC010 (Emballage), er ansvarlig for emballering af produkterne, før de sendes til kunderne. Den direkte arbejdsomkostning føjes til produkter via styklister og rute. De indirekte omkostninger til driften af bæreren skal også fordeles på de fremstillede produkter. Den bedste statistiske måling for en sådan fordeling er ofte antallet af registrerede produktionstimer pr. produkt i den pågældende periode.

Tabellen ProdRouteTrans indeholder alle posteringer for produktionsarbejde pr. juridisk enhed i DataAreadID.

Her er et eksempel på tabellen ProdRouteTrans.

| Reference        | Tal | Handling | Type | Tidspunkt  | Fysisk dato | Produktgruppe (økonomisk dimension) | Juridisk enhed |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Produktionsordre | P0001  | Emballage | Tidspunkt | 8,00  | 01-01-2017    | Appelsinjuice B2B                    | USMF         |
| Produktionsordre | P0001  | Emballage | Tidspunkt | 8,00  | 02-01-2017    | Appelsinjuice B2B                    | USMF         |
| Produktionsordre | P0002  | Emballage | Tidspunkt | 4,00  | 03-01-2017    | Appelsinjuice Forbruger               | USMF         |
| Produktionsordre | P0003  | Emballage | Tidspunkt | 4,00  | 03-01-2017    | Appelsinjuice Forbruger               | USMF         |
| Produktionsordre | P0004  | Rekonst.  | Tidspunkt | 10,00 | 03-01-2017    | Appelsinjuice Forbruger               | USMF         |

Når du opretter en post i en **skabelon til provider af statistiske målinger**, skal du beslutte, hvilken funktion du skal bruge:

- **Antal** – En optælling af poster pr. omkostningsobjekt overføres.
- **Sum** – En sum af poster pr. omkostningsobjekt overføres. (Feltet **Sum** og feltet **Dato** er obligatorisk).

Skabelonen til provider af statistiske målinger kan konfigureres på følgende måde.

| Navn    | Funktion | Kildetabel   | Sumfelt | Datofelt    |
|---------|----------|----------------|-----------|---------------|
| Pakke-CC | Sum      | ProdRouteTrans | Timer     | Fysisk dato |

Du kan også tilføje afgrænsninger for at indsnævre målingerne fra kildetabellen.

I dette eksempel, hvis du kun vil have summen af de timer, der er relateret til CC010-emballagebæreren, kan du tilføje en afgrænsning i feltet **Handling**. I feltet **Kriterier** skal du vælge **Emballage** for at begrænse outputtet på følgende måde.

**Afgrænsninger**

| Kildetabel   | Felt     | Afgrænsning  |
|----------------|-----------|-----------|
| ProdRouteTrans | Handling | Emballage |

Før du kan få statistiske målinger i omkostningsregnskabet, skal du oprette relationen mellem skabelonen til provider af statistisk måling og det statistiske dimensionsmedlem. Denne relation oprettes pr. finanspost for omkostningsregnskab og version. Relationen består af en dataconnector og en dataprovider. Du kan have flere dataconnectorer og dataprovidere pr. statistiske dimensionsmedlem.

> [!NOTE]
> I dette eksempel skal du oprette en relation for den **faktiske version**.

Gå til **Finanspost for omkostningsregnskab** \> **Faktisk version** \> **Administrer** \> **Statistiske målinger** for at oprette relationen. I dette scenarie skal du vælge **Dynamics 365 for Finance and Operations, Enterprise edition – Statistiske målinger** som dataconnector for at udtrække data fra Finance and Operations.

**Datakilde**

| Navn           | Dataconnector                                                                     | Statistisk dimensionsmedlem |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Pakke CC D365FO | Dynamics 365 for Finance and Operations, Enterprise edition – Statistiske målinger | Pakke-CC                      |

Systemet registrerer, at ProdRouteTrans er en tabel, hvor hver post tilhører en særskilt juridisk enhed. Derfor vil du blive bedt om at vælge den juridiske enhed, som posteringer skal importeres fra.

**Konfiguration af dataprovider**

| Navn på statistisk skabelon | Juridisk enhed |
|---------------------------|--------------|
| Pakke-CC                   | USMF         |

Når kildedataene for statistiske målinger er behandlet, oprettes følgende statistiske poster i omkostningsregnskabet.

**Kladde**

| Kladden | Kladdetype                     | Regnskabskalenderperiode | År   | Termin | Version   |   Dataconnector-kildeposter  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Overførselskladde for statistisk post | Regnskabsår               | 2017    | 1. Periode  | CA-finans-USMF | Pakke-CC |

**Overførselskladdeposteringer for statistisk post**

| Regnskabsdato | Størrelsesorden | Statistisk element |  Betegnelse          | Produktgruppe         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31-01-2017      | 16,00     | Pakke-CC             | Emballagebærer | Appelsinjuice B2B      |
| 31-01-2017      | 8,00      | Pakke-CC             | Emballagebærer | Appelsinjuice Forbruger |

**Statistiske poster**

| Omkostningsobjekt           | Regnskabsdato | Statistisk dimensionsmedlem |    Betegnelse        | Størrelsesorden |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Appelsinjuice B2B      | 31-01-2017      | Pakke-CC                      | Emballagebærer | 16,00     |
| Appelsinjuice Forbruger | 31-01-2017      | Pakke-CC                      | Emballagebærer | 8,00      |

Hvis den foruddefinerede Pakke-CC-fordelingsbasis for dimensionsmedlemmer tildeles som en fordelingsbasis i en regel til fordeling af omkostninger, fordeles omkostningerne ved hjælp af følgende fordelingsfaktor.

| Omkostningsobjekt           | Størrelsesorden | Fordelingsfaktor  |
|-----------------------|-----------|--------------------|
| Appelsinjuice B2B      | 16,00     | (16 ÷ 24) × beløb |
| Appelsinjuice Forbruger | 8,00      | (8 ÷ 24) × beløb  |

## <a name="imported-statistical-measures"></a>Importerede statistiske målinger

Du kan importere statistiske målinger til omkostningsregnskab ved hjælp af værktøjet import/eksport i Datastyring.

Den dataenhed, der bruges til importen, hedder Importerede statistiske målinger.

> [!NOTE]
> Denne dataenhed er designet, så maksimalt fem entydige dimensionsværdier tillades pr. post.

Forbruget af elektricitet registreres i Microsoft Excel ved hjælp af det foruddefinerede format for dataenheden. Her er et eksempel.

| Regnskabsdato | Navn 1 på dimensionsmedlem | Navn 2 på dimensionsmedlem | Navn 5 på dimensionsmedlem | Størrelsesorden  | Kildeidentifikator |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31-01-2017      | CC001                  |                        |                        | 2,450.00   | Elektricitet       |
| 31-01-2017      | CC002                  |                        |                        | 4,100.00   | Elektricitet       |
| 31-01-2017      | CC003                  |                        |                        | 15.000,00  | Elektricitet       |

Når du har importeret dataene via datastyring, gemmes dataene i en midlertidig tabel i omkostningsregnskabet. De importerede data kan derfor bruges på flere finansposter for omkostningsregnskab. En genindlæsning af data er ikke påkrævet.

Du kan importere dataene ved at gå til **Importerede data** \> **Dataenhed** \> **Importerede statistiske målinger**.

| Kildeidentifikator | Regnskabsdato | Størrelsesorden  | Navn 1 på dimensionsmedlem | Navn 2 på dimensionsmedlem | Navn 5 på dimensionsmedlem |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektricitet       | 31-01-2017      | 2,450.00   | CC001                  |                        |                        |
| Elektricitet       | 31-01-2017      | 4,100.00   | CC002                  |                        |                        |
| Elektricitet       | 31-01-2017      | 15.000,00  | CC003                  |                        |                        |

Før du kan få statistiske målinger i omkostningsregnskabet, skal du oprette relationen mellem kildeidentifikatoren og det statistiske dimensionsmedlem. Denne relation oprettes pr. finanspost for omkostningsregnskab og version. Relationen består af en dataconnector og en dataprovider. Du kan have flere dataconnectorer og dataprovidere pr. statistiske dimensionsmedlem.

> [!NOTE]
> I dette eksempel skal du oprette en relation for den **faktiske version**.

Gå til **Finanspost for omkostningsregnskab** \> **Faktisk version** \> **Administrer** \> **Statistiske målinger** for at oprette relationen. I dette scenarie skal du vælge **Importerede statistiske målinger** som dataconnector, fordi dataene er importeret fra et tredjepartssystem til omkostningsregnskabet via Microsoft Excel.

**Datakilde**

| Navn        | Dataconnector                | Statistisk dimensionsmedlem |
|-------------|-------------------------------|------------------------------|
| Elektricitet | Importerede statistiske målinger | Elektricitet                  |

**Konfiguration af dataprovider**

| Importér kildeidentifikator | Funktion | Dimension 1   | Dimension 2 | Dimension 5 |
|--------------------------|----------|--------------|------------|------------|
| Elektricitet              | Sum      | Bærere |            |            |

> [!NOTE]
> Når du definerer konfigurationen af dataprovider, skal du angive, hvilke omkostningsobjektdimensioner der skal sammenholdes med de importerede transaktioner. Når kildedataene for statistiske målinger er behandlet, oprettes følgende statistiske poster i omkostningsregnskabet.

**Kladde**

| Kladden | Kladdetype                       | Regnskabskalenderperiode | År  | Perid  |Version      |Dataconnector-kildeposter |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Overførselskladde for statistisk post | Regnskabsår                 | 2017  | 1. Periode | CA-finans-USMF | Elektricitet |

**Overførselskladdeposteringer for statistisk post**

| Regnskabsdato | Størrelsesorden  | Omkostningselement |   Betegnelse           | Bærer |
|-----------------|------------|--------------|-------------------------|-------------|
| 31-01-2017      | 2,450.00   | Elektricitet  | Forbrug af elektricitet | CC001       |
| 31-01-2017      | 4,100.00   | Elektricitet  | Forbrug af elektricitet | CC002       |
| 31-01-2017      | 15.000,00  | Elektricitet  | Forbrug af elektricitet | CC003       |

**Statistiske poster**

| Omkostningsobjekt |    | Regnskabsdato | Statistisk dimensionsmedlem |      Betegnelse                   | Størrelsesorden  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | Personale | 31-01-2017      | Elektricitet                  | Forbrug af elektricitet | 2,450.00   |
| CC002       | FI | 31-01-2017      | Elektricitet                  | Forbrug af elektricitet | 4,100.00   |
| CC003       | LO | 31-01-2017      | Elektricitet                  | Forbrug af elektricitet | 15.000,00  |

Hvis elektricitetens foruddefinerede fordelingsbasis for dimensionsmedlemmer tildeles som en fordelingsbasis i en regel til fordeling af omkostninger, fordeles omkostningerne ved hjælp af følgende fordelingsfaktor.

| Omkostningsobjekt |    | Størrelsesorden | Fordelingsfaktor          |
|-------------|----|-----------|----------------------------|
| CC001       | Personale | 2,450.00  | (2.450 ÷ 21.550) × beløb  |
| CC002       | FI | 4,100.00  | (4.100 ÷ 21.550) × beløb  |
| CC003       | LO | 15.000,00 | (15.000 ÷ 21.550) × beløb |

## <a name="see-also"></a>Se også

[Fordelingsgrundlag](allocation-bases.md)

