---
title: Prioritetsbaseret planlægning
description: Denne artikel indeholder en beskrivelse af den prioritetsbaserede planlægningsfunktion i Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 4997ba123f105f683daaa6b29fe8c5ee72cb47cb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873805"
---
# <a name="priority-based-planning"></a>Prioritetsbaseret planlægning

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en beskrivelse af den prioritetsbaserede planlægningsfunktion i Microsoft Dynamics 365 Supply Chain Management. Denne funktion giver understøttelse af efterspørgselsbaseret planlægning, som er et trin i DDMRP (Demand Driven Material Requirements Planning). Ved hjælp af prioritetsbaseret planlægning kan Planlægningsoptimering generere ordreforslag, der er baseret på planlægningsprioriteter i stedet for behovsdatoer.

Med prioritetsbaseret planlægning kan du prioritere genopfyldningsordrer for at sikre, at hasteefterspørgsel prioriteres højere end knap så vigtig efterspørgsel. En lagergenopfyldningsordre prioriteres f.eks. højere end en standardgenopfyldningsordre. Systemet kan automatisk opdele større ordrer i mindre separate ordrer, hvor ordrelinjer grupperes efter prioritet. Derefter kan alle ordrer med høj prioritet behandles først.

Du kan få et hurtigt overblik over denne funktion i følgende video: [Understøttelse af planlægningsoptimering til prioritetsstyret planlægning i Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Aktivere prioritetsbaseret planlægning i systemet

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Varedisponering*
- **Funktionsnavn:** *Prioritetsstyret MRP-understøttelse af planlægningsoptimering*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Hvor og hvordan planlægningsprioriteter tildeles

*Planlægningsprioritet*-oplysninger om udbud og efterspørgsel er rygraden for prioritetsbaseret planlægning. Planlægningsprioritet definerer vigtigheden af en efterspørgsels- eller udbudslinje. Planlægningsoptimering bruger det, når feltet **Dækningskode** er angivet til *Prioritet*.

Planlægningsprioriteten er normalt et tal mellem 0 (nul) og 100, hvor 0 repræsenterer den største vigtighed. Den vises og angives i feltet **Planlægningsprioritet**. Dette felt findes på følgende sider: **Behovsprognoselinjer**, **Salgsordredetaljer**, **Indkøbsordredetaljer**, **Flytteordredetaljer** og **Oplysninger om ordreforslag**.

Når feltet **Dækningskode** for den relevante vare eller disponeringsgruppe er angivet til *Prioritet*, afstemmer Planlægningsoptimering udbud med efterspørgsel ved hjælp af en efterspørgselsbaseret tilgang, når planlægningsprioriteten beregnes, og for hvert frigivet produkt tages der højde for de værdier, der er angivet for felterne **Minimum**, **Genbestillingspunkt** og **Maksimum** på **Varedisponering**-siden.

> [!NOTE]
> Værdien *Prioritet* er kun tilgængelig for feltet **Dækningskode**, når Planlægningsoptimering er aktiveret.

De relaterede *planlægningsprioritetsmodeller* styrer planlægningsprioriteten og opdeler ordreforslag efter prioritetsområde. Du kan også angive prioritetsværdier for standardplanlægning for hver udbuds- eller efterspørgselstype og definere prioritetsberegningsmetoden.

## <a name="types-of-priority-calculation-methods"></a>Typer af prioritetsberegningsmetoder

Hver model for planlægningsprioritet har indstillingen **Prioritetsberegningsmetode**, der styrer, hvordan behovsplanlægning anvender prioritet på ordreforslag. De tilgængelige værdier er *Procent af maks. lagerantal* og *Prioritetsintervaller*. *Prioritetsintervaller* repræsenterer en mere avanceret version af metoden *Procent af maks. lagerantal*.

### <a name="percent-of-maximum-inventory-quantity"></a>Procent af maks. lagerantal

I beregningsmetoden *Procent af maks. lagerantal* finder beregningen af leveringsprioritet den aktuelle *disponible lagerbeholdning* (nettoflow) som en procentdel af **Maks. lagerantal**, der er angivet for en vare. Derefter oprettes et enkelt ordreforslag pr. vare og leverandør (medmindre maksimumordreantallet bruges til at gennemtvinge en opdeling). Ordrens planlægningsprioritet beregnes som en procentdel af maksimum.

Følgende formel bruges:

*Procentdel af maksimum* = (*Nettoflowposition* × 100) ÷ *Maksimumlagerantalsværdi fra varedisponering*

I denne formel beregnes *Nettoflowposition* på følgende måde:

*Nettoflowposition* = *Beholdning* + *I bestilling* – *Kvalificeret efterspørgsel*

- *I bestilling* er den forventede levering.
- *Kvalificeret efterspørgsel* repræsenterer de nettobehov, der har behovsdatoen inden for planlægningens tidsramme.

Under varedisponeringskørslen oprettes nye ordreforslag, når nettoflowpositionen er mindre end antallet for en vares genbestillingspunkt. Ordreforslagsantallet er forskellen mellem værdien af **Maks. lagerantal**, der angives på vareniveau, og nettoflowpositionen. Ordreforslagsprioriteten beregnes som en *nettoflowposition* i procent af værdien for **Maks. lagerantal**.

> [!NOTE]
> Den beregnede prioritet kan ikke være negativ, heller ikke selvom efterspørgslen overstiger det samlede udbud. Hvis efterspørgslen overstiger det samlede udbud, angives den beregnede prioritet til 0 (nul).

### <a name="priority-ranges"></a>Prioritetsintervaller

Beregningsmetoden *Prioritetsintervaller* er mere avanceret end metoden *Procent af maks. lagerantal* og konfigureres på niveauet for planlægningsprioritetsmodellen. Der kan oprettes flere nye planlagte forsyningsordrer til opfyldelse af behovet pr. vare. Prioriteterne af den planlagte forsyning følger de værdier, der er defineret i gitteret **Intervaller for planlægningsprioritet** på siden **Planlægningsprioritetsmodeller**.

Følgende ekstra regler gælder, når feltet **Prioritetsberegningsmetode** er angivet til *Prioritetsintervaller*:

- Hvis indstillingen **Overvej efterspørgselsprioritet** for den planlagte prioritetsmodel er angivet til *Ja*, vil den prioritet, der angives på hver efterspørgselslinje, begrænse prioritetsintervallets bucket. Prioriteten af et nyt ordreforslag til levering vil ikke være lavere end behovets prioritet. Den øverste værdi af intervallet betragtes som en grænseværdi, som behovets prioritetsværdi sammenlignes med. Hvis behovets prioritet er præcist i midten mellem de øvre tærskelværdier i to intervaller, vælges det interval, der har den højeste prioritet (dvs. den laveste prioritetsværdi).
- Hvis feltet **Planlagt oprettelse af ordre** for den planlagte prioritetsmodel er angivet til *Enkelt levering med vigtigste prioritet*, oprettes der kun én forsyning til at fylde hele vejen op til maksimum. Prioriteten angives til prioriteten for det første interval, der udløser en forsyning.
- Hvis der ikke findes nogen disponible lagerbeholdninger, ingen forsyning og ingen efterspørgsel, bruges linjen i gitteret **Planlægningsprioritetsinterval**, hvor feltet **Fra antal** er angivet til *Nul*.
- Hvis der findes et behov, men ingen disponible lagerbeholdninger eller forventet forsyning, bruges linjen i gitteret **Planlægningsprioritetsinterval**, hvor feltet **Fra antal** er angivet til *Nul eller derunder*.
- Når det interval, som behovet er en del af, evalueres, vil indstillingen af **Overvej efterspørgselsprioritet** stadig have effekt.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Forskelle mellem traditionelle tidslinjeberegninger og prioritetsbaseret planlægning

Prioritetsbaseret planlægning er forskellig fra de traditionelle tidslinjeberegninger på følgende måder:

- Alle de almindelige processorer før planlægning er stadig gældende. Disse forudgående processorer omfatter udligning af godkendte ordreforslag i forhold til salgsbehov, tilknytning af indkøbsrekvisition og reservationslogik. Det er kun den efterspørgsel, som disse forudgående processorer ikke kan opfylde, der bliver behandlet.
- Under udligning tages der højde for al forsyning uanset prioriteten. Denne forsyning omfatter lagerbeholdning, frigivet forsyning og den ikke-udlignede del af godkendte ordreforslag.
- Ingen "negative dage"-efterspørgsel kan udlignes mod forsyning i løbet af hele disponeringstiden.
- Når forsyning udlignes i forhold til efterspørgslen, bruges den forsyning, der har den højeste prioritet (dvs. den laveste prioritetsværdi), først. Beholdningsforsyning anses for at have prioritetsværdien 0 (nul). Den vil derfor blive forbrugt som den første kilde.
- Der oprettes nye planlagte forsyningslinjer i overensstemmelse med de almindelige regler for minimumordrestørrelse, maksimumordrestørrelse, antals multiplum osv.

## <a name="planning-priority-models"></a>Planlægningsprioritetsmodeller

*Planlægningsprioritetsmodeller* tildeles disponeringsgrupper og styrer planlægningsprioriteten for ordreforslag. De definerer den logik, der bestemmer, hvordan værdien af planlægningsprioritet beregnes for hvert ordreforslag, og hvordan prioriteten tildeles ordreforslag, leveringslinjer og efterspørgselslinjer.

Hvis du vil arbejde med planlægningsprioritetsmodellerne, skal du gå **Varedisponering \> Konfiguration \> Planlægningsprioritetsmodeller**. Som det tidligere er blevet beskrevet, er en af en models vigtigste indstillinger værdien af **Prioritetsberegningsmetode**. Denne indstilling styrer den beregningsmetode, der bruges, når varedisponering tildeler ordreforslag en prioritetsværdi.

> [!NOTE]
> Planlægningsprioritetsmodeller gælder for hele organisationen på tværs af alle juridiske enheder.

### <a name="coverage-group"></a>Dækningsgruppe

Opret en ny dækningsgruppe, som du vil bruge til prioritetsbaseret planlægning, som beskrevet i [Definere dækningsregler for varer](../tasks/define-coverage-rules-items.md). Når du har oprettet dækningsgruppen, skal du angive følgende yderligere felter:

- **Dækningskode** – Vælg *Prioritet*, hvis dækningsgruppen skal bruge prioritetsbaseret planlægning.
- **Planlægningsprioritetsmodel** – Vælg en prioritetsmodel for planlægning i hele organisationen.

### <a name="item-coverage"></a>Varedisponering

Konfigurer indstillinger for varedisponering som beskrevet i [Disponeringsindstillinger](../coverage-settings.md). Den værdi af **Dækningskode**, der er valgt for dækningsgruppen, kopieres som standard til indstillingerne for varedisponering. Du kan dog tilsidesætte standardværdien efter behov. I nogle tilfælde er feltet **Dækningskode** for en varedisponeringspost angivet til *Planlægning*, men der er ikke defineret nogen planlægningsprioritetsmodel for den relaterede dækningsgruppe. I disse tilfælde anvendes enhver model, hvor feltet **Prioritetsberegningsmetode** er angivet til *Procent af maks. lagerantal*, og feltet **Planlagt oprettelse af ordre** er angivet til *Enkelt levering med vigtigste prioritet*, som standard.

Indstil feltet **Dækningskode** til *Prioritet* for at gøre feltet **Genbestillingspunkt** i indstillingerne for varedisponering tilgængelige. I dette felt skal du angive det antal i genbestillingspunktet, der skal bruges, mens systemet afgør, hvornår der skal anbringes ordreforslag med **Dækningskode**-værdien *Prioritet*.

Antallet for genbestillingspunktet beregnes ofte som behovet under gennemløbstiden plus en minimumværdi (sikkerhedslager). Det skal være en værdi mellem **Minimum**- og **Maksimum**-værdierne.

Du kan f.eks. indstille felterne på følgende måde:

- **Minimum:** *10*
- **Genbestillingspunkt:** *45*
- **Maksimum:** *60*

I dette eksempel er antallet for genbestillingspunkt baseret på en gennemløbstid på syv dage og et gennemsnitligt dagligt forbrug på 5. Behovet i gennemløbstiden er derfor 35. Minimumværdien 10 (sikkerhedslager) tilføjes derefter for at få et genbestillingspunkt på 45. Når denne opsætning anvendes, foreslås levering, når den forventede beholdning er under 45. Ordreprioriteten baseres på opsætningen af planlægningsprioritet.

### <a name="manage-planning-priority-models"></a>Håndtere modeller til planlægningsprioritet

Til arbejde med planlægningsprioritetsmodellerne. skal du følge disse trin.

1. Gå til **Varedisponering \> Konfiguration \> Planlægningsprioritetsmodeller**.
1. Vælg enten en eksisterende model i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny model.
1. Angiv følgende felter i postens hoved:

    - **Navn** – Angiv et navn på modellen. Navnet skal være entydigt på tværs af alle juridiske enheder i din organisation.
    - **Beskrivelse** – Indtast en beskrivelse af modellen.
    - **Prioritetsberegningsmetode** – Vælg en af følgende værdier:

        - *Prioritetsintervaller* – Når du vælger denne værdi, bliver gitteret **Planlægningsprioritetsintervaller** tilgængeligt. Her skal du oprette flere prioritetsintervaller for at definere værdien for planlægningsprioritet.
        - *Procent af maks. lagerantal* – Beregn planlægningsprioritetsværdien som en procentdel baseret på det forventede lagerniveau over det maksimale lagerantal.

    - **Planlagt oprettelse af ordre**– Dette felt er tilgængeligt, når feltet **Prioritetsberegningsmetode** er angivet til *Prioritetsintervaller*. Vælg en af følgende værdier:

        - *Enkelt levering med vigtigste prioritet* – Opdel ikke ordreforslag baseret på prioritetsintervallet. Planlægningsprioriteten for et ordreforslag er baseret på det vigtigste prioritetsinterval (det vil sige den laveste værdi af planlægningsprioritet).
        - *Opdel i henhold til prioritetsområder* – Opdel behovet i flere ordreforslag på basis af prioritetsområder for planlægning. Planlægningsprioriteten for individuelle ordreforslag defineres af planlægningsprioriteten for det tilknyttede prioritetsinterval for planlægning.

    - **Overvej efterspørgselsprioritet** – Angiv denne indstilling til *Ja* for at begrænse prioriteten af et nyt ordreforslag, der oprettes til levering. (Prioriteten vil ikke være lavere end den relaterede efterspørgsels prioritet). Hvis du angiver denne indstilling til *Nej*, tages behovsordren ikke i betragtning, når forsyningsordren får sin prioritet beregnet.

1. Hvis du angiver feltet **Prioritetsberegningsmetode** til *Prioritetsintervaller*, kan du bruge knapperne **Tilføj** og **Fjern** på værktøjslinjen i oversigtspanelet **Intervaller for planlægningsprioritet** til at tilføje eller fjerne rækker med prioritetsintervaller efter behov. Hvis der findes flere rækker, og du indsætter en ny række, angives planlægningsprioriteten automatisk til gennemsnittet af den valgte række og rækken over den. På hver række skal du angive følgende felter:

    - **Planlægningsprioritet** – Angiv enhver værdi mellem 0,00 og 100,00. Denne værdi repræsenterer den planlægningsprioritet, der bruges for rækken. Den laveste prioritetsværdi repræsenterer den højeste prioritet. En standardværdi tildeles, men du kan ændre den efter behov. Samme værdi af **Planlægningsprioritet** kan ikke bruges til mere end ét planlægningsprioritetsinterval i samme planlægningsprioritetsmodel.
    - **Beskrivelse** – Angiv en beskrivelse af planlægningsprioritetsintervallet (f.eks. *Genbestillingspunkt til Maksimum*).
    - **Fra antal** – Den nedre grænse for planlægningsprioritetsintervallet. Denne værdi er skrivebeskyttet og er baseret på værdierne af **Til antal** og **Procentdel af til antal** for det forrige planlægningsprioritetsinterval.
    - **Til antal** – Vælg feltet fra varedisponering, som skal bruges til at definere intervallets øvre grænse. Følgende værdier understøttes og påvirker værdien af **Fra antal** i det næste interval:

        - *Nul* – Denne værdi repræsenterer et negativt til nul-interval (*Nul eller derunder* eller *Nul*). For rækker, hvor denne værdi er valgt, er feltet **Procent af til antal** skrivebeskyttet og er altid angivet til *100* procent.
        - *Minimum lagerantal* – Denne værdi repræsenterer **Minimum**-værdien for en vare på siden **Varedisponering**. For rækker, hvor denne værdi vælges, kan feltet **Procentdel af til antal** redigeres og bruges til at angive værdien af **Fra antal** i det næste interval (f.eks. til *80 % af minimumlagerantallet*).
        - *Genbestillingspunkt* – Denne værdi repræsenterer **Genbestillingspunkt**-værdien for en vare på siden **Varedisponering**. For rækker, hvor denne værdi vælges, kan feltet **Procentdel af til antal** redigeres og bruges til at angive værdien af **Fra antal** for det næste interval (f.eks. til *80 % af genbestillingspunkt*).
        - *Maks. lagerantal* – Denne værdi repræsenterer **Maksimum**-værdien for en vare på siden **Varedisponering**. For rækker, hvor denne værdi vælges, kan feltet **Procentdel af til antal** redigeres og bruges til at angive værdien **Fra antal** i det næste interval (f.eks. til *80 % af minimumlagerantallet*).
        - *Uendelig* – Denne værdi repræsenterer et ubegrænset øvre niveau i intervallet (*Uendelig eller derunder* til *Uendelig*). For rækker, hvor denne værdi er valgt, er feltet **Procent af til antal** skrivebeskyttet og er altid angivet til *100* procent.

    - **Procent af til antal** – Angiv en procentværdi, der skal bruges til at beregne den øvre grænse for planlægningsprioritetsintervallet baseret på den værdi, der er valgt i feltet **Til antal**. Hvis feltet **Til antal** f.eks. er angivet til *Minimumlagerantal*, og feltet **Procentdel af til antal** er angivet til *50*, vil den øvre grænse være 50 procent af minimumlagerantallet fra den relaterede varedisponering.

1. I oversigtspanelet **Standarder for planlægningsprioritet** kan du angive felterne efter behov for at definere standardplanlægningsprioriteter for hver type udbuds- eller efterspørgselslinje (salgsordre, indkøbsordre, flytteordre eller behovsprognose). Der kan kun angives positive værdier.

## <a name="view-and-maintain-planning-priority"></a>Se og vedligeholde planlægningsprioritet

Planlægningsprioriteten vises og angives i feltet **Planlægningsprioritet**. Du kan finde dette felt på de sider, der vises i følgende tabel. Prioriteten angives som et tal mellem 0 (nul) og 100, hvor 0 repræsenterer den største vigtighed.

| Side | Feltlokation | Værdikilde |
|---|---|---|
| Behovsprognoselinjer | <p>Fanen **Vare**</p><p>(Vælg en linje i den øverste sektion, og vælg derefter fanen **Vare**).</p> | Standardværdi eller værdi, der angives manuelt |
| Oplysninger om salgsordre | <p>Fanen **Levering** i oversigtspanelet **Linjedetaljer**</p><p>(Vælg en linje i oversigtspanelet **Salgsordrelinjer**, og vælg derefter fanen **Levering** i oversigtspanelet **Linjedetaljer**).</p> | Standardværdi, intern værdi eller værdi, der angives manuelt |
| Indkøbsordredetaljer | <p>Fanen **Levering** i oversigtspanelet **Linjedetaljer**</p><p>(Vælg en linje i oversigtspanelet **Indkøbsordrelinjer**, og vælg derefter fanen **Levering** i oversigtspanelet **Linjedetaljer**).</p> | Værdi, der angives ved autorisation fra ordreforslag, intern værdi eller værdi, der angives manuelt |
| Flytteordredetaljer | <p>Fanen **Levering** i oversigtspanelet **Linjedetaljer**</p><p>(Vælg en linje i oversigtspanelet **Flytteordrelinjer**, og vælg derefter fanen **Levering** i oversigtspanelet **Linjedetaljer**).</p> | Værdi, der angives ved autorisation fra ordreforslag, eller værdi, der angives manuelt |
| Oplysninger om ordreforslag | Oversigtspanelet **Generelt** | Værdi, der beregnes under varedisponering, eller værdi, som angives manuelt |

### <a name="intercompany-trade"></a>Intern handel

Værdien af **Planlægningsprioritet** på interne udbuds- og efterspørgselslinjer er delt mellem de tilknyttede enheder. Ændringer på begge sider afspejles på den sammenkædede ordrelinje.

Her er nogle eksempler:

- En bruger ændrer planlægningsprioriteten for en intern salgsordrelinje fra 20 til 30. Denne ændring afspejles på den tilknyttede interne indkøbsordrelinje.
- En bruger ændrer planlægningsprioriteten for en intern indkøbsordrelinje fra 40 til 50. Denne ændring afspejles på den tilknyttede interne salgsordrelinje.
