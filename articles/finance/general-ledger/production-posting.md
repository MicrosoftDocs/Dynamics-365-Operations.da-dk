---
title: Produktionsordrebogføring
description: Dette emne indeholder oplysninger om forskellige typer af produktionsordrebogføring.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: cd1b6c49e59f9480fd831ad5ff143033ca09792c
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/24/2022
ms.locfileid: "8802996"
---
# <a name="production-postings"></a>Produktionsbogføringer

Dette mene indeholder oplysninger om forskellige typer af bogføring i produktionsordreprocessen.


## <a name="material-consumption"></a>Materialeforbrug

Materialer registreres som forbrugt under produktionen, når produktionspluklistekladden bogføres. Denne proces opretter transaktioner, der fratrækker den disponible lagerbeholdning. I **Produktionsparametrene** kan du angive, om værdien af råvarer, der er igangværende (kaldet IGVF), skal bogføres i finans.

Værdien af råvarer, der er i gang (IGVF), bogføres på **Forkalkuleret omkostning til forbrugte materialer**- og **Forkalkuleret omkostning til forbrugte materialer, IGVF**-konti. Pluklisteprocessen for produktionsordren er en fysisk opdatering af de lagertransaktioner, der er relateret til produktionsordren. Når en produktionsordre registreres som afsluttet, tilbageføres de fysiske transaktioner, og de tilhørende lagertransaktioner opdateres økonomisk. Når slutkladden bogføres, anvendes bogføringstyperne **Omkostning til forbrugte materialer** og **Omkostning til forbrugte materialer, IGVF**.

Fanen **Produktion** på siden **Lagerposteringsprofiler** bruges til at styre, hvordan produktionsordrer bogføres i finansmodulet. Dette bruges, når feltet **Finansbogføring** indstilles til enten **Vare og ressource** eller **Vare og kategori** på siden **Produktionsstyringsparametre**. 

Hvis en pluklistekladde skal bogføres i finansmodulet for en produktionsordre, skal følgende betingelser være opfyldt:

-   På siden **Produktionsstyringsparametre** skal afkrydsningsfeltet **Bogfør plukliste i finans** være markeret. Denne indstilling kan tilsidesættes for et bestemt websted på siden **Produktionsstyringsparametre pr. sted**.
-   På siden **Varemodelgrupper** skal afkrydsningsfeltet **Bogfør fysisk lager** være markeret for den vare, der er valgt på indkøbsordrelinjen.
-   På siden **Lagerposteringsprofil** skal der være angivet hovedkonti for følgende posteringstyper:
    -   **Forkalkuleret omkostning til forbrugte materialer**
    -   **Forkalkuleret omkostning til forbrugte materialer, IGVF**

## <a name="time-consumption"></a>Tidsforbrug

Den tid, medarbejdere bruger på produktionsjob registreres i **rutekortkladden** eller **jobkortkladden**. Når disse kladder bogføres, behandles finanskontering på en dedikeret konto for ressourcer, der er igangværende (IGVF). Denne bogføring repræsenterer værdien af den tid, der bruges på produktionsordren. Når produktionsordren er registreret som afsluttet, udlignes IGVA-konti.

Du kan bogføre tidsforbrug på tre måder afhængigt af den indstilling, der er valgt i feltet **Finansbogføring** på siden **Produktionsstyringsparametre**.

## <a name="reporting-finished-goods-and-error-quantities"></a>Rapportering af færdigvarer og mængden af fejl

Når en produktionsordre er **Færdigmeldt**, opdateres mængden af færdigvarer, der er fuldført, i lageret gennem **Færdigmeld**-kladden. Hvis du bruger IGVF-regnskabsførelse, bogføres en finanskladde for at reducere IGVF-kontiene og øge lageret af færdige varer. Kladden bruger de standardomkostninger, der er defineret for produktet. Hvis indstillingen **Brug forkalkuleret kostpris** er valgt på siden **Produktionsstyringsparametre**, bruges den forkalkulerede kostpris fra produktionsordren.

Værdien af råvarer, der er i gang (IGVF), bogføres på **Forkalkuleret produktionsomkostning**- og **Forkalkuleret produktionsomkostning, IGVF**-konti. Processen **Færdigmeld** for produktionsordren er en fysisk opdatering af de lagertransaktioner, der er relateret til produktionsordren. Når en produktionsordre er afsluttet, tilbageføres de fysiske transaktioner, og de tilhørende lagertransaktioner opdateres økonomisk. Når slutkladden bogføres, anvendes bogføringstyperne **Produktionsomkostning** og **Produktionsomkostning, IGVF**.

Fanen **Produktion** på siden **Lagerposteringsprofiler** bruges til at styre, hvordan produktionsordrer bogføres i finansmodulet. Dette bruges, når feltet **Finansbogføring** indstilles til enten **Vare og ressource** eller **Vare og kategori** på siden **Produktionsstyringsparametre**. Oversigtspanelet **Finansvarer** på siden **Produktionsgrupper** kan også bruges til at styre bogføring for produktionsordrer, når feltet er angivet til **Produktionsgrupper**.

Hvis en **Færdigmeld**-kladde skal bogføres i finansmodulet for en produktionsordre, skal følgende betingelser være opfyldt:
-   På siden **Produktionsstyringsparametre** skal afkrydsningsfeltet **Bogfør færdigmeldinger i finans** være markeret. Denne indstilling kan tilsidesættes for et bestemt websted på siden **Produktionsstyringsparametre pr. sted**.
-   På siden **Varemodelgrupper** skal afkrydsningsfeltet **Bogfør fysisk lager** være markeret for den vare, der er valgt på indkøbsordrelinjen.
-   På siden **Lagerposteringsprofil** skal der være angivet hovedkonti for følgende posteringstyper:
    -   **Forkalkuleret produktionsomkostning**
    -   **Forkalkuleret produktionsomkostning, IGVF**

## <a name="ending-the-production-order"></a>Afslutte produktionsordrer

Inden en produktionsordre afsluttes, beregnes de faktiske omkostninger for den mængde, der er produceret. Alle estimerede omkostninger til materialer, løn og indirekte omkostninger tilbageføres og erstattes med faktiske omkostninger. Den overordnede omkostning for færdigvaren debiteres på kontoen **Produktionsomkostning** og krediteres på kontoen **Produktionsomkostning, IGVF**. De materialer, der er forbrugt i løbet af produktionsordren, krediteres **Omkostning til forbrugte materialer** og debiteres på kontoen **Omkostning til forbrugte materialer, IGVF**.

Hvis du markerer afkrydsningsfeltet **Slutkørsel**, når du udfører omkostningsberegningen, ændres produktionsordrens status til **Afsluttet**. Denne status forhindrer, at ekstra omkostninger ved en fejltagelse bogføres på en færdigmeldt produktionsordre. Du kan angive, at værdien for mængder med fejl, der er færdigmeldt, skal tildeles de gode mængder, der er færdigmeldt. Du kan også angive, at værdien for antal fejl skal bogføres på en dedikeret spildkonto. 

Følg disse trin for at angive en specifik spildkonto:
1.  Gå til **Produktionsstyring** > **Konfiguration** > **Produktionsstyringsparametre**.
2.  Vælg fanen **Standardopdatering**.
3.  Vælg **Spildkonto** i feltet **Spildmetode**.
4.  Vælg den hovedkonto i feltet **Spildkonto**, hvor spild for antal fejl skal bogføres, når produktionsordren afsluttes. Vælg f.eks. en udgiftskonto som 510380: Produktionsspild.

Hvis en slutkladde skal bogføres i finansmodulet for en produktionsordre, skal følgende betingelser være opfyldt:
-   På siden **Lagerposteringsprofil** eller **Produktionsgrupper** skal der være angivet hovedkonti for følgende posteringstyper:
    -   **Omkostning til forbrugte materialer**
    -   **Omkostning til forbrugte materialer, IGVF**
    -   **Produktionsomkostning**
    -   **Produktionsomkostning, IGVF**
-   Hovedkontiene skal angives på siden **Omkostningskategorier**, **Ressourcer** eller **Ressourcegrupper** for følgende typer:
    -   **Produktionsomkostninger, der er overtaget**
    -   **Omkostning til forbrugt produktion, IGVF**

## <a name="indirect-costs-for-production-orders"></a>Indirekte omkostninger for produktionsordrer

Når du behandler transaktioner for en produktionsordre, kan du konfigurere indirekte omkostninger til at registrere faste omkostninger eller yderligere gebyrer i finansmodulet. Fysiske transaktioner for indirekte omkostninger registreres på lageret, når du bogfører en pluklistekladde eller en færdigmeldingskladde. Økonomiske transaktioner for indirekte omkostninger registreres på lageret, når du bogfører slutkladden.

Du kan genkende indirekte omkostninger på dit tidsforbrug i forbindelse med **Rutekort**-kladder eller **jobkort**-kladder. Disse transaktioner tilbageføres og bogføres på finanskonti, når du afslutter produktionsordren. Du kan finde flere oplysninger i [Kostprisark](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Styre finanskonteringsniveauet

På siden **Produktionsstyringsparametre** kan du bruge feltet **Finanskontering** til at angive niveauet for finanskontering for produktionsprocesser. 

Følgende felter er tilgængelige:

### <a name="item-and-resource"></a>Vare og ressource

Når du vælger indstillingen **Vare og ressource** i feltet **Finansbogføring**, kommer bogføringskontiene fra ressourcen eller ressourcegruppen, der er i brug i ruten. Konti til den specifikke ressource er den første bogføringsindstilling. Hvis der ikke er angivet en konto, bruges de konti, der er angivet for ressourcegruppen. Hver operationslinje i en rute kan have angivet én ressource som **Efterkalkuleret ressource**. Denne ressource bruges til at bestemme, hvilken konto der skal bruges. Denne indstilling bruges normalt, når en organisation tildeler driftsomkostninger til ressourcerne. Omkostningerne er ofte højere for ressourcerne og bruges til at træffe valg om produktion eller køb. Dette er den mest detaljerede bogføringskonfiguration og giver adgang til den mest detaljerede styring af bogføringerne og meget detaljerede analyser af produktionsprocessen.

### <a name="item-and-category"></a>Vare og art

Når du vælger indstillingen **Vare og art** i feltet **Finansbogføring**, kommer bogføringskontiene fra siden **Omkostningsart**, der er relateret til hver linje i ruten. Hver operationslinje i ruten kan have tre omkostningsarter: **Opstillingstid**, **Kørselstid** og **Antal**. Denne indstilling bruges normalt, når organisationens hovedfokus er på proceseffektivitet og varighed af aktiviteter. Denne indstilling er en mere opsummeret bogføringsmåde, og den gør det stadig muligt at gruppere omkostninger i arter.

### <a name="production-group"></a>Produktionsgruppe

Når du vælger indstillingen **Produktionsgrupper** i feltet **Finansbogføring**, kommer bogføringskontiene fra siden **Produktionsgrupper**. **Produktionsgrupper** bruges typisk, når mere end én produktionslinje kører lignende produkter eller har lignende udstyr. Du kan bruge denne indstilling til at sammenligne omkostningerne mellem to forskellige produktionsgrupper.  
  
> [!NOTE]
> Hvis standardmetoden til beregning af omkostningen for færdigvaren er brugt, afspejles dette også i den endelige postering. Hvis der er en difference mellem de faktiske omkostninger og de omkostninger, der er beregnet ved hjælp af standardmetoden, bogføres differencer på kontoen, der viser avance og tab.

### <a name="route-groups-and-ledger-posting"></a>Rutegrupper og finansbogføring

Der er angivet en **Rutegruppe** for hver operationslinje i en rute. Felterne **Opstillingstid**, **Kørselstid** og **Antal** i **Rutegruppen** i gruppen **For- og efterkalkulation** bruges til at styre, om tiden skal bruges til efterkalkulation, når der bogføres et **Jobkort** eller en **Rutekortkladde** i produktionsordren. Hvis indstillingerne er deaktiveret, oprettes der ikke et bilag i finansmodulet for tidsforbruget.

Hvis et **Rutekort** eller en **Jobkortkladde** skal bogføres i finansmodulet for en produktionsordre, skal følgende betingelser være opfyldt:

-   Feltet **Opstillingstid**, **Kørselstid** eller **Antal** skal markeres i gruppen **For- og efterkalkulation** på siden **Rutegruppe**.
-   På enten siden **Omkostningsart**, **Rute**, **Rutegruppe** eller **Produktionsgrupper** skal der være angivet hovedkonti for følgende bogføringstyper:
    -   Anslåede produktionsomkostninger, der er overtaget
    -   Forkalkuleret omkostning til forbrugt produktion, IGVF

I følgende diagram vises forholdet mellem rutegruppen og beregningen af de samlede omkostninger for hver operation (rutelinje) i en given rute. Hver rutelinje har én rutegruppe. Rutegruppen styrer parametre for opstillingstid, kørselstid og antal. Fanen **Omkostningsart** indeholder tre indstillinger for **Opsætning**, **Kørsel** og **Antal**, der er aktiveret på baggrund af indstillingen for rutegrupper. Oversigtspanelet **Tidsmålinger** indeholder tre felter, der er baseret på rutegruppen.

Den formel, der bruges, er baseret på, om indstillingen er aktiveret i rutegruppen. Omkostningen fra den valgte omkostningsart ganges med det antal, der blev angivet på tidsmålingerne for at beregne de samlede omkostninger.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Forholdet mellem rutegrupper og de samlede beregnede omkostninger.":::
Forholdet mellem rutegrupper og de samlede beregnede omkostninger. Hver rutelinje har én rutegruppe. Rutegruppen styrer parametre for opstillingstid, kørselstid og antal. Fanen Omkostningsart indeholder tre indstillinger for Opsætning, Kørsel og Antal, der er aktiveret på baggrund af indstillingen for rutegrupper. Oversigtspanelet Tidsmålinger indeholder tre felter, der er aktiveret og baseret på rutegruppen. Den formel, der bruges, er baseret på, om indstillingen er aktiveret i rutegruppen. Omkostningen fra den valgte omkostningsart ganges med det antal, der er angivet på tidsmålingerne for at beregne de samlede omkostninger.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfiguration af posteringsprofil

I følgende tabel vises eksempler på standardbogføringstyper med eksempler på hovedkonti og beskrivelser. 

 - I kolonnen **Debet/Kredit** angives, om transaktionen typisk er debet eller kredit eller i visse tilfælde kan bogføres som det ene eller det andet. 
 - I kolonnen **Clearingkonto** angives, om bogføringstypen er en clearingkonto. Det beløb, der bogføres på denne konto, tilbageføres automatisk, når en senere transaktion bogføres. 
 - I **P/F**-kolonnen angives **P** til fysisk bogføring og **F** til økonomisk bogføring. 
 - Kolonnen **Følg** angiver, om hovedkontoen for en bestemt bogføringstype typisk er den samme som en anden bogføringstype. Værdien i kolonnen angiver den bogføringstype, der typisk anvendes.

> [!NOTE]
> Disse hovedkonti og hovedkontonavne er kun forslag. Det anbefales, at du arbejder sammen med bogholderen for at finde den bedste konfiguration til virksomhedens behov.


| Bogføringstype  | Eksempel på hovedkonto | Eksempel på hovedkontonavn| Kontotype | Debet/Kredit? | Clearingkonto | Fysisk eller økonomisk | Følg | Beskrivende tekst |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Forkalkuleret omkostning til forbrugte materialer      | 140100               | Materialelager        | Aktiv        | Kredit         | Y                | P                     | Omkostning til forbrugte materialer                | Denne konto bruges, når du bogfører en pluklistekladde for en produktionsordre. Dennes modkonto er Forkalkuleret omkostning til forbrugte materialer, IGVF. Beløbet på denne konto tilbageføres automatisk, når produktionsordren afsluttes. Denne konto repræsenterer lagerkontoen i balancen.       |
| Forkalkuleret omkostning til forbrugte materialer, IGVF | 150150               | IGVF for produktion – materialer | Aktiv        | Debet          | Y                | P                     | Forkalkuleret produktionsomkostning, IGVF          | Denne konto bruges, når du bogfører en pluklistekladde for en produktionsordre. Dennes modkonto er Forkalkuleret omkostning til forbrugte materialer. Beløbet på denne konto tilbageføres automatisk, når en produktionsordre afsluttes. Denne konto repræsenterer IGVF i balancen.                  |
| Forkalkuleret produktionsomkostning               | 140200               | Færdigvarelager   | Aktiv        | Debet          | Y                | P                     | Produktionsomkostning                         | Denne konto bruges, når du bogfører en færdigmeldingskladde for en produktionsordre. Dennes modkonto er Forkalkuleret produktionsomkostning, IGVF. Beløbet på denne konto tilbageføres automatisk, når produktionsordren afsluttes. Denne konto repræsenterer lagerkontoen i balancen. |
| Forkalkuleret produktionsomkostning, IGVF          | 150150               | IGVF for produktion – materialer | Aktiv        | Kredit         | Y                | P                     | Produktionsomkostning, IGVF                    | Denne konto bruges, når du bogfører en færdigmeldingskladde for en produktionsordre. Dennes modkonto er Forkalkuleret produktionsomkostning. Beløbet på denne konto tilbageføres automatisk, når en produktionsordre afsluttes. Denne konto repræsenterer IGVF i balancen.                     |
| Omkostning til forbrugte materialer                | 140100               | Materialelager        | Aktiv        | Kredit         | N                 | F                     | Forkalkuleret omkostning til forbrugte materialer      | Denne konto bruges til at genkende de materialer, der forbruges i produktionsordren under slutprocessen. Dennes modkonto er Omkostning til forbrugte materialer, IGVF.                                                                                                    |
| Omkostning til forbrugte materialer, IGVF           | 150150               | IGVF for produktion – materialer | Aktiv        | Debet          | N                 | F                     | Forkalkuleret omkostning til forbrugte materialer, IGVF | Denne konto bruges til at genkende de materialer i IGVF, der forbruges i produktionsordren under slutprocessen. Dennes modkonto er Omkostning til forbrugte materialer.                                                |
| Produktionsomkostning                         | 140200               | Færdigvarelager   | Aktiv        | Debet          | N                 | F                     | Forkalkuleret produktionsomkostning               | Denne konto bruges til at genkende omkostningerne for den færdigvare, der produceres af en produktionsordre, når du afslutter produktionsordren. Dennes modkonto er Produktionsomkostning, IGVF.                                                                  |
| Produktionsomkostning, IGVF                    | 150150               | IGVF for produktion – materialer | Aktiv        | Kredit         | N                 | F                     | Forkalkuleret produktionsomkostning, IGVF          | Denne konto bruges til at genkende omkostningerne for den færdigvare i IGVF, der produceres af en produktionsordre, når du afslutter produktionsordren. Dennes modkonto er Produktionsomkostning.                                     |

> [!NOTE]
> Kontoen **Tilgang af lean service-IGVF** og **Clearing af lean service-IGVF** bruges med efterkalkuleret varetræk for lean produktion. Du kan finde flere oplysninger i [Efterkalkuleret varetræk](/supply-chain/cost-management/backflush-costing.md).

