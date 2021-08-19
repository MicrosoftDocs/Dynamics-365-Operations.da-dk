---
title: Rabatstyringsaftaler
description: Dette emne beskriver, hvordan du opretter rabatstyringsaftaler. Aftaler bruges til at styre forskellige metoder og grundlag for beregning af rabatter og royalties. De omfatter regler for inkludering og udelukkelser.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 5b8a1beae80ad63f26cd1b532d1d6026a5b38a8701c9c1d0aadfee5da8965477
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716486"
---
# <a name="rebate-management-deals"></a>Rabatstyringsaftaler

[!include [banner](../includes/banner.md)]

Rabatstyringsaftaler bruges til at styre forskellige metoder og grundlag for beregning af rabatter og royalties. De omfatter regler for inkludering og udelukkelser. Der er tre typer rabatstyringsaftaler: debitorrabatter, debitorroyalties og kreditorrabatter. Alle tre typer bruger samme indstillinger. I dette emne påpeges forskelle, hvor de findes.

## <a name="create-a-deal"></a>Oprette en aftale

1. Gå til **Rabatstyring \> Rabatstyringsaftaler \> Alle rabatstyringsaftaler**. På listesiden **Alle rabatstyringsaftaler** kan du oprette og arbejde med aftaler af alle tre typer.

    Du kan også følge et af disse trin. I hvert tilfælde indeholder den listeside, der vises, alle de samme indstillinger som listesiden **Alle rabatstyringstilbud**, men den er filtreret, så den kun viser aftaler af én type.

    - Gå til **Rabatstyring \> Rabatstyringsaftaler \> Debitorrabataftaler** for kun at oprette debitorrabataftaler.
    - Gå til **Rabatstyring \> Rabatstyringsaftaler \> Debitorroyaltyaftaler** for kun at oprette debitorroyaltyaftaler.
    - Gå til **Rabatstyring \> Rabatstyringsaftaler \> Kreditorrabataftaler** for kun at oprette kreditorrabataftaler.

1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende felter i dialogboksen **Opret ny aftale**:

    - **Rabatstyringsaftale** – Hvis du har [konfigureret en nummerserie](rebate-management-parameters.md) til rabataftaler, angives dette felt automatisk til et entydigt systemgenereret id. Du skal ellers indtaste et entydigt id.
    - **Beskrivelse** – Indtast en beskrivelse af aftalen.
    - **Modul** – Vælg den type partner, som aftalen gælder for (*Kunde* eller *Leverandør*). Afhængigt af hvilken side du startede fra, kan dette felt angives automatisk ud fra den valgte aftaletype. Dette felt er skrivebeskyttet her.
    - **Type** – Vælg aftaletypen (*Rabat* eller *Royalty*). Afhængigt af hvilken side du startede fra, kan dette felt angives automatisk ud fra den valgte aftaletype. Dette felt er skrivebeskyttet her.
    - **Afstem efter** – Vælg, hvordan aftalen skal beregnes og afstemmes:

        - *Aftale* – Der skal behandles en enkelt rabat for alle rabatter og fradrag i aftalen.
        - *Linje* – Rabatter skal behandles for hver linje i en aftale.

    - **Posteringsprofil** – Vælg den [posteringsprofil](rebate-management-posting.md), der skal bruges til transaktioner, hvor aftalen er gældende. Dette felt er kun tilgængeligt, når feltet **Afstem efter** er angivet til *Aftale*. Hvis den er angivet til *Linje*, skal du tildele profilen senere for hver linje, du føjer til aftalen.
    - **Posteringsprofil for garanti** – Vælg den [posteringsprofil](rebate-management-posting.md), der skal bruges til garantitransaktioner. Posteringsprofiler er kun påkrævede i forbindelse med garantitransaktioner, hvis garantien gælder for en royalty. Ellers vises der en fejl, når der bogføres garantier, selvom en posteringsprofil ikke er obligatorisk, hvis der ikke er angivet en posteringsprofil. Dette felt er kun tilgængeligt, når feltet **Type** er angivet til *Royalty*. 
    - **Rabatoutput** – Vælg, hvordan rabatten eller royaltyen skal betales:

        - *Økonomisk* – Opret en fritekstkreditnota eller kreditordebetnota, så du kan betale eller modtage penge senere. Bemærk, at der **kan** bruges hensættelser til rabatter, når denne indstilling er valgt. Denne indstilling er kun tilgængelig, når feltet **Type** er angivet til *Royalty*.
        - *Vare* – Opret en salgsordre for varer i overensstemmelse med aftaleopsætningen. På denne salgsordre tildeles en pris på 0 (nul) til hver vare. Bemærk, at der **ikke kan** bruges hensættelser til rabatter, når denne indstilling er valgt.

    - **Rabatvaluta** – Vælg den valuta, der skal bruges, når rabatten, fradraget eller royaltyen betales.
    - **Dokumentnoter** – Skriv noter om aftalen efter behov.
    - **Akkumuleret garanti** – Du kan kun angive denne indstilling til *Ja*, hvis feltet **Type** er angivet til *Royalty*. Denne indstilling har indflydelse på beregningen af garanterede fradragsbetalinger. Her er et eksempel:

        - Garantien for aftalen er at sælge til en værdi, der vil medføre en betaling på 10.000 kr. pr. kvartal.
        - Den organisation, der sælger varerne, sælger til en værdi, der medfører en fradragsbetaling på 12.000 kr. i kvartal 1. Resultatet er en udbetalt royalty på 12.000 kr. minus garantien på 10.000 kr.
        - Hvis indstillingen for **Akkumuleret garanti** er angivet til *Ja*, gælder de 2.000 kr. ekstra royalties, der blev betalt i kvartal 1, for kvartal 2. Kunden er derfor garanteret 8.000 kr. (10.000 kr. garantien minus 2.000 kr. ekstra betaling).
        - I kvartal 2 registrerer du salg, der udløser en royalty på 5.000 kr.
        - Systemet identificerer en 3.000 kr. betaling (8.000 kr. garanti minus 5.000 kr. af betalte royalties).
        - Hvis indstillingen **Akkumuleret garanti** er angivet til *Nej*, vil det fulde beløb på 10.000 kr. være garanteret hvert kvartal. Denne garanti svarer til en foreslået betaling af 5.000 kr. i kvartal 2 (10.000 kr. i garanti minus 5.000 kr. betalte royalties).

1. Vælg **OK** for at oprette aftalen og lukke dialogboksen.

Med denne procedure oprettes overskriftsniveauet for den nye aftale. Derefter skal du føje linjer til aftalen.

## <a name="add-lines-to-a-deal"></a>Føje linjer til en aftale

Når du har oprettet en aftale som beskrevet i forrige afsnit, kan du åbne den fra listesiden. Du kan derefter tilføje linjer for at identificere kunder eller leverandører, varer, tidsrammer, en basis og beregningsmetoder for aftalen. En aftale kan have en eller flere linjer. Hvis der er flere linjer i en aftale, er de normalt af samme type, eller der er tilknyttet de samme parametre. Indtil du føjer linjer til en aftale, sker der faktisk ikke noget ved aftalen.

1. Åbn den relevante listeside med rabataftaler som beskrevet i forrige afsnit.
1. Find og åbn den aftale, du vil arbejde med.
1. Vælg en af følgende knapper i oversigtspanelet **Rabatstyring** for at føje en aftalelinje til gitteret:

    - **Tilføj linje** – Tilføj en ny tom aftalelinje.
    - **Kopiér linje** – Hvis en eksisterende aftalelinje ligner den aftalelinje, du vil tilføje, kan du vælge denne knap for at tilføje en kopi af den. Den nye aftalelinje indeholder alle indstillinger fra de relaterede oplysninger om rabatstyring. Du kan derefter redigere indstillingerne. Du vil f.eks. typisk opdatere varerelationen og rabatprocenten.

1. På den nye aftalelinje skal du angive følgende felter:

    - **Rabatstyringsnummer** – Hvis du har [konfigureret en nummerserie](rebate-management-parameters.md) til rabataftalenumre, angives dette felt automatisk til et entydigt systemgenereret id. Du skal ellers indtaste et entydigt id.
    - **Type** – Den type aftale, som linjen gælder for (*Rabat* eller *Royalty*). Værdien kopieres fra overskriftet og kan ikke ændres.
    - **Beskrivelse** – Indtast en beskrivelse af aftalelinjen.
    - **Firma** – Vælg det firma (juridisk enhed), som aftalelinjen gælder for. Under behandlingen kan brugere kun behandle aftalelinjer, der er tildelt det firma, som de aktuelt bruger. Listesiden **Debitorrabataftaler** indeholder en visning for flere virksomheder baseret på brugerens sikkerhedsadgang. Du kan dog kun redigere og behandle rabatter for det firma, du aktuelt bruger.
    - **Kontokode** – Vælg området for de debitorer eller kreditorer, som aftalelinjen gælder for:

        - *Tabel* – Aftalelinjen gælder for en bestemt debitor eller kreditor.
        - *Gruppe* – Aftalelinjen gælder for en gruppe af debitorer eller kreditorer. Du kan finde flere oplysninger om, hvordan du konfigurerer grupper, i [Rabatstyringsgrupper](rebate-management-groups.md).
        - *Alle* – Aftalelinjen gælder for alle debitorer eller kreditorer.

    - **Kontorelation** – Hvis du har valgt *Tabel* i feltet **Kontokode**, skal du vælge den kreditor eller debitor, som aftalen gælder for. Hvis du har valgt *Gruppe*, skal du vælge debitor- eller kreditorgruppen. Hvis du vælger *Alle*, er dette felt ikke tilgængeligt.
    - **Varekode** – Vælg området for de varer, som aftalelinjen gælder for:

        - *Tabel* – Aftalelinjen gælder for en bestemt vare.
        - *Gruppe* – Aftalelinjen gælder for en gruppe af varer. Du kan finde flere oplysninger om, hvordan du konfigurerer grupper, i [Rabatstyringsgrupper](rebate-management-groups.md).
        - *Alle* – Aftalelinjen anvendes til alle varer.

    - **Varerelation** – Hvis du har valgt *Tabel* i feltet **Varekode**, skal du vælge den vare, som aftalelinjen gælder for. Hvis du har valgt *Gruppe*, skal du vælge varegruppen. Hvis du vælger *Alle*, er dette felt ikke tilgængeligt.
    - **Enhedstype** – Vælg den enhedstype, der gælder for aftalelinjen (*Lagerenhed* eller *Fastvægtenhed*). Bemærk, at dette felt kan være tomt for ældre poster. I dette tilfælde antages *Lagerenhed*-værdien.
    - **(Lagerstyringsparametre)** – I de resterende felter på aftalelinjen skal du angive værdier for de lagerstyringsparametre, der skal bruges til at definere de varer, der er medtaget i aftalen (f.eks. varestørrelse, farve, stil, lokation og lagersted). Hvis du vil tilføje eller fjerne dimensionerne, skal du vælge **Vis dimensioner** i handlingsruden.

1. Vælg **Gem** i handlingsruden.
1. Hvis du yderligere vil begrænse det sæt varer, som en aftalelinje gælder for, skal du vælge linjen og derefter vælge **Filter** i oversigtspanelet **Rabatstyring** for at åbne en standarddialogboks til **Forespørgsel**.
1. For hver rabatlinje, du tilføjer, skal du konfigurere beregningsdetaljer og andre detaljer i oversigtspanelet **Rabatstyringsdetaljer** som beskrevet i næste afsnit.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Føje oplysninger om rabatstyring til en aftalelinje

For hver linje i aftalen skal du konfigurere detaljer i oversigtspanelet **Rabatstyringsdetaljer**. Vælg aftalelinjen i oversigtspanelet **Rabatstyring**. Angiv derefter værdier for den pågældende aftalelinje ved hjælp af de forskellige faner i oversigtspanelet **Rabatstyringsdetaljer**. I følgende underafsnit beskrives, hvordan du kan bruge de enkelte faner.

### <a name="settings-on-the-general-tab"></a>Indstillinger under fanen Generelt

Fanen **Generelt** i oversigtspanelet **Rabatstyringsdetaljer** giver dig mulighed for at konfigurere beregningsmetoden og grundlaget for den valgte aftalelinje. Denne opsætning styrer, om der kræves et minimumkøb, de posteringsprofiler, der er knyttet til aftalelinjen, og detaljerne i beregningen. I følgende tabel forklares de felter, der er tilgængelige.

| Felt | Betegnelse |
|---|---|
| Beregningsmåde | Vælg den metode, der skal bruges, når den valgte aftalelinje kombineres med andre aftalelinjer (*Trinvis*, *Akkumuleret*, *Glidende* eller *Total*). Værdien i dette felt kan påvirke udfaldet af rabatberegningerne markant. Du kan finde en detaljeret beskrivelse af de enkelte metoder og eksempler, der viser, hvordan det påvirker rabatberegningen, i afsnittet [Beregningsmetoder for aftalelinjer](#calc-methods) senere i dette emne. |
| Basis | Vælg, om rabatten anvendes baseret på antal (dvs. det samlede antal enheder, der er købt eller solgt) eller værdi (dvs. den samlede pris for varer, der er købt eller solgt). |
| Transaktionstype | <p>Vælg det punkt i processen, hvor beregningen skal finde sted:</p><ul><li>*Ordre* – Brug det bestilte antal eller den bestilte værdi som udgangspunkt for beregningen.</li><li>*Leveret* – Brug det leverede antal eller den leverede værdi som udgangspunkt for beregningen.</li><li>*Faktura* – Brug det fakturerede antal eller den fakturerede værdi som udgangspunkt for beregningen.</li></ul> |
| Enhed | Hvis du valgte *Antal* i feltet **Basis**, skal du vælge den enhed, som antallet skal angives i. |
| Minimumsbeløb | Angiv det minimumbeløb, der skal betales pr. periode. Du kan angive en negativ værdi for at tillade negative rabatbeløb, hvis kreditnotaerne overstiger salget for perioden. |
| Fradragsprincip for rabat | Vælg det [rabatfradragsprincip](rebate-reduction-principle.md), som gælder for aftalelinjen. |
| Variantnummer | Hvis aftalelinjen gælder for en vare med varianter, skal du vælge den variant, som aftalelinjen gælder for. |
| Kreditorrabatgrundlag | <p>Dette felt vises kun for kreditorrabatter (dvs. aftaler, hvor feltet **Modul** er angivet til *Kreditor*). Vælg grundlaget for kreditorrabatten:</p><ul><li>*Indkøbsordre* – Den rabat, kreditoren modtager, er baseret på antallet eller værdien på indkøbsordren.</li><li>*Salgsordre* – Kreditoren får først rabat, når varerne er solgt. Rabatten er baseret på antallet eller værdien på salgsordren.</li></ul> |
| Prisbasis | <p>Dette felt vises kun for kreditorrabatter (aftaler, hvor feltet **Modul** er angivet til *Kreditor*). Hvis du har valgt *Salgsordre* i feltet **Kreditorrabatgrundlag**, skal du vælge det relevante prisgrundlag:</p><ul><li><p>*FIFO* – Den periodiske opgave **Beregn FIFO-købspris** skal køres for at beregne rabatten. (Hvis du vil køre opgaven, skal du gå til **Rabatstyring \> Periodiske opgaver \> Beregn FIFO-købspris**). Der bruges en FIFO-regel (First In, First Out) til beregning af værdien af den lagerbeholdning, der sælges. Denne værdi bruges derefter til at beregne kreditorrabatter. Her er et eksempel:</p><ul><li>**Solgt lagerbeholdning:** 1.000 enheder a 3,00 kr hver = 3.000 kr</li><li>**Aktuel indkøbspris baseret på FIFO:** 2,00 kr</li><li>**Fungerende beregning:** *Solgte enheder* × *Aktuel indkøbspris* = 1.000 × 2,00 kr = 2.000 kr</li></ul></li><li><p>*Sidste indkøbspris* – Værdien fra den sidste indkøbstransaktion bruges til at beregne kreditorrabatter. Her er et eksempel:</p><ul><li>**Solgt lagerbeholdning:** 1.000 enheder a 3,00 kr hver = 3.000 kr</li><li>**Sidste købspris:** 2,00 kr</li><li>**Fungerende beregning:** *Solgte enheder* × *Sidste indkøbspris* = 1.000 × 2,00 kr = 2.000 kr</li></ul></li><li><p>*Gennemsnitskøbspris* – Den vægtede gennemsnitsværdi af de seneste *X* måneder bruges til at beregne kreditorrabatter. Hvis du vælger denne indstilling, skal du angive antallet af måneder i feltet **Antal måneder** (som kun er tilgængeligt, når feltet **Prisgrundlag** er angivet til *Gennemsnitlig indkøbspris*). Her er et eksempel:</p><ul><li>**Solgt lagerbeholdning:** 1.000 enheder a 3,00 kr hver = 3.000 kr</li><li>**Gennemsnitlig indkøbspris:** 2,00 kr</li><li>**Fungerende beregning:** *Solgte enheder* × *Gennemsnitlig indkøbspris* = 1.000 × 2,00 kr = 2.000 kr</li></ul></li><li><p>*Salgspris* – Salgsprisen bruges til at beregne kreditorrabatter. Her er et eksempel:</p><ul><li>**Solgt lagerbeholdning:** 1.000 enheder a 3,00 kr hver = 3.000 kr</li><li>**Gennemsnitlig indkøbspris:** 2,00 kr</li><li>**Fungerende beregning:** *Solgte enheder* × *Salgspris* = 1.000 × 3,00 kr = 3.000 kr</li></ul></li></ul> |
| Antal måneder | Dette felt vises kun for kreditorrabatter (aftaler, hvor feltet **Modul** er angivet til *Kreditor*). Hvis du har valgt *Gennemsnitskøbspris* i feltet **Prisgrundlag**, skal du angive det antal måneder, der skal bruges. |
| Posteringsprofil | Vælg den [posteringsprofil](rebate-management-posting.md), der gælder for den valgte aftalelinje. Denne profil bruges kun, når feltet **Afstem efter** i aftalehovedet er angivet til *Linje*. Hvis feltet **Afstem efter** er angivet til *Aftale*, bruges den posteringsprofil, der er angivet i aftalehovedet, altid. Hvis ingen posteringsprofil er angivet på aftalelinjen, bruges den posteringsprofil, der er angivet i aftalehovedet. |
| Posteringsprofil for garanti | Dette felt fungerer på samme måde som feltet **Posteringsprofil**, men gælder kun for royalties. |
| Betalingstype | Betalingstypen for den posteringsprofil, der er valgt for aftalen. |
| Moms inkluderet | Vælg, om transaktionen er inklusive moms. Moms inkluderet er kun relevant, når feltet **Grundlag** er angivet til *Værdi*. Fakturabeløbet bruges som beløbet inklusive moms. Hvis rabatberegningen er baseret på en procent, ganges rabatprocenten med beløbet inklusive moms. Bemærk, at momsværdien bruges fra aftalelinjen i beregningen. |
| Medtag kreditnotaer | <p>Angiv denne indstilling til *Ja* for at medtage kreditnotaer i rabatberegningen.</p><p>Hvis du angiver denne indstilling til *Ja*, varierer virkningen, afhængigt af værdien i feltet **Transaktionstype**:</p><ul><li>Hvis feltet **Transaktionstype** er angivet til *Faktura*, vil beregningsfaktoren være på kreditnotaer. Denne konfiguration er den normale konfiguration.</li><li>Hvis feltet **Transaktionstype** er angivet til *Ordre*, vil beregningsfaktoren være i både salgsordrer, der har negative værdier, og åbne returordrer.</li></ul> |
| Rabatbeløb | Angiv denne indstilling til *Ja* for at basere beregningen på varens rabatbeløb eller varerne i tilfælde, hvor der gives rabat på aftalelinjer. |
| Kun betalte fakturaer | Angiv denne indstilling til *Ja*, hvis beregningen kun skal tage højde for fuldt betalte fakturaer. (Det vil sige, at rabatter ikke beregnes for delvist betalte fakturaer). Denne indstilling er kun tilgængelig, når feltet **Transaktionstype** er angivet til *Faktura*. |
| Inkluder fritekst | Angiv denne indstilling til *Ja* for at medtage fritekstfakturaer i rabatberegningen. Fritekstfakturaer kan kun inkluderes for aftalelinjer, hvor feltet **Varekode** er angivet til *Alle*. |
| Inkluder udligningsrabat | Angiv denne indstilling til *Ja* for at reducere rabatten med den første udligningsrabat. Det forudsættes, at organisationen vil tage den første udligningsrabat. Angiv denne indstilling til *Nej*, hvis du vil aktivere udligningsrabatten til brug senere. |
| Dokumentnoter | Angiv noter, der skal bruges som posteringstekst på rabatposteringskladdelinjer. |

### <a name="settings-on-the-dates-tab"></a>Indstillinger under fanen Datoer

Indstillingerne under fanen **Datoer** i oversigtspanelet **Rabatstyringsdetaljer** definerer hyppigheden og tidspunktet for de beregninger, der er angivet under fanen **Generelt**. De bestemmer, hvordan beregninger foretages på behandlingstidspunktet.

Under denne fane kan du angive det datointerval, som den valgte aftalelinje gælder for, og beregningsfrekvensen. Du kan også angive, om garantien skal bogføres og hvornår.

Brug knapperne på værktøjslinjen til at føje datolinjer til gitteret eller fjerne dem. Hvis der findes flere datolinjer, må de gyldige datointervaller ikke overlappe. Ellers modtager du en fejlmeddelelse, når du forsøger at gemme aftalen.

I følgende tabel forklares de felter, der er tilgængelige for hver datolinje.

| Felt | Betegnelse |
|---|---|
| Fra-dato | Angiv den første dato, som datolinjen gælder for. Hvis der er angivet "fra"- og "til"-datoer i aftalehovedet, bruges de som standardværdier for alle nye datolinjer. |
| Til-dato | Angiv den sidste dato, som datolinjen gælder for. Hvis der er angivet "fra"- og "til"-datoer i aftalehovedet, bruges de som standardværdier for alle nye datolinjer. |
| Pr. | Angiv, hvor ofte aftalelinjen skal beregnes. Angiv et heltal her, og vælg derefter en enhed i feltet **Akkumuler efter**. Hvis du f.eks. vil beregne hver anden uge, skal du angive feltet **Pr.** til *2* og feltet **Akkumuler efter** til *Uger*. |
| Akkumuler efter | Vælg den enhed, der gælder for indstillingen **Pr**. Vælg *Levetid* for at beregne over hele levetiden af aftalelinjen. Vælg *Tilpasset periode* for at vælge en periode, der er defineret i Finans. I så fald skal du også angive feltet **Periodetype**. |
| Periodetype | Dette felt er kun tilgængeligt, når feltet **Akkumuler efter** er angivet til *Tilpasset periode*. De værdier, der kan vælges, kommer fra de periodetyper, der er defineret i finansmodulet. |
| Første ugedag | Angiv, hvordan ugerne identificeres for perioden. Dette felt er kun tilgængeligt, når feltet **Akkumuler efter** er angivet til *Uger*. |
| Krav pr. | Angiv, hvor ofte der kan gøres krav på rabat for aftalelinjen. Angiv et heltal her, og vælg derefter en enhed i feltet **Krav pr**. |
| Krav efter | Vælg den enhed, der gælder for indstillingen **Krav pr**. Vælg *Levetid* for at tillade krav én gang i løbet af hele aftalelinjens levetid. Vælg *Tilpasset periode* for at vælge en periode, der er defineret i Finans. I så fald skal du også angive feltet **Kravsperiodetype**. |
| Kravsperiodetype | Dette felt er kun tilgængeligt, når feltet **Krav efter** er angivet til *Tilpasset periode*. De værdier, der kan vælges, kommer fra de periodetyper, der er defineret i finansmodulet. |
| Behandling ved bogføring | Markér dette afkrydsningsfelt, hvis kravlinjen skal behandles på bogføringstidspunktet. Denne indstilling er kun tilgængelig for aftalelinjer, hvor feltet **Transaktionstype** under fanen **Generelt** er angivet til *Leveret* eller *Faktura*. I forbindelse med hensættelser bogføres hensættelsen, når leveringsnotaen eller fakturaen oprettes. |
| Garanti pr. | Dette felt gælder kun for royaltyaftaler. Angiv, hvor ofte royaltygarantien skal beregnes i løbet af den periode, der er defineret af indstillingen **Akkumuler efter**. Angiv et heltal her, og vælg derefter en betalingstid i feltet **Garantibetalt**. |
| Garantibetalt | <p>Dette felt gælder kun for royaltyaftaler. Det bruges sammen med feltet **Garanti pr.** til at definere frekvensen af garantiberegningen. Vælg en af følgende værdier:</p><ul><li><p>*Periodens start* – Garantien betales ved starten af den aftaleperiode, der er defineret for datolinjen. Den fulde garanti behandles først. Det er kun værdien af royalties, der overstiger garantibeløbet, der bogføres som royalty. Her er et eksempel:</p><ul><li>**Garantiminimum:** 10.000 kr over to måneder.</li><li>**Måned 1:** 10.000 kr bogført som en garanti og 0 kr bogført som royalties.</li><li>**Måned 2:** 2.000 kr bogført som royalties og 0 kr bogført som garantier.</li><li>**Fungerende beregning:** *Resterende garanti* – *Bogførte royalties* = 0 kr - 2.000 kr = -2.000 kr.</li></ul><p>Da der kræves 2.000 kr royaltybetaling, oprettes der en kladde til 2.000 kr.</p><p>**Bemærk:** Garantien skal beregnes og bogføres sammen med fradragshensættelsen for den første periode.</p></li><li><p>*Slutning af periode* – Garantien betales først ved afslutningen af fradragsaftalen, som defineret på datolinjen. Her er et eksempel:</p><ul><li>**Garantiminimum:** 10.000 kr over to måneder.</li><li>**Måned 1:** 5.000 kr bogført som royalty, og der blev oprettet en kladde.</li><li>**Måned 2:** 7.000 kr bogført som royalty, og der blev oprettet en kladde.</li><li>**Fungerende beregning:** Da royalties overstiger garantibeløbet, bogføres 0 kr på garantien.</li></ul><p>**Bemærk:** Garantien skal kun beregnes og bogføres sammen med fradrags- og rabattransaktionen for den sidste periode.</p></li></ul> |
| Garantiminimum | Dette felt gælder kun for royaltyaftaler. Angiv minimumbeløbet til garantien for en royalty i den valuta, der er defineret i aftalehovedet. |

### <a name="settings-on-the-lines-tab"></a>Indstillinger under fanen Linjer

Fanen **Linjer** i oversigtspanelet **Rabatstyringsdetaljer** giver dig mulighed for at definere beregningslinjer for den valgte aftalelinje. Hver beregningslinje opretter en antals- eller værditærskel og et tilhørende kompensationsbeløb eller varer. Feltet **Basis** under fanen **Generelt** angiver, om hver beregningslinje er baseret på et antal eller en værdi.

Brug knapperne på værktøjslinjen til at føje beregningslinjer til gitteret eller fjerne dem. Der kan være et vilkårligt antal beregningslinjer. Hvis der findes flere beregningslinjer, må antallet eller værdiintervaller i "til" og "fra" ikke overlappe.

I følgende tabel forklares de felter, der er tilgængelige for hver beregningslinje.

| Felt | Betegnelse |
|---|---|
| Fra antal/værdi | Angiv minimumantal eller -værdi, som beregningslinjen gælder for. |
| Til antal/værdi | Angiv maksimumantal eller -værdi, som beregningslinjen gælder for. |
| Rabatstyringsmetode | <p>Dette felt er kun tilgængeligt for aftaler, hvor feltet **Rabatoutput** i hovedet er angivet til *Økonomisk*. Vælg den metode, du vil bruge til at beregne rabatten.</p><ul><li>*Fast* – Der bruges et fast prisbeløb for linjen.</li><li>*Procent* – Der bruges en procent af salgsbeløbet.</li><li>*Sats* – Der bruges et fast prisbeløb pr. ordre.</li></ul><p>**Vigtigt:** Det anbefales på det kraftigste, at du bruger samme metode til hver beregningslinje under fanen **Linjer**. Hvis der kræves en ny metode, skal du oprette en ny aftalelinje. Husk, at du kan bruge knappen **Kopiér linje** i oversigtspanelet **Rabatstyring** til at oprette en ny aftalelinje ud fra en eksisterende aftalelinje.</p><p>**Bemærk:** Hvis feltet **Rabatoutput** er angivet til *Vare*, angives dette felt altid som *Fast*. Yderligere oplysninger om, hvordan varerne angives, finder du i den tekst, der følger efter denne tabel. |
| Rabatstyringsbeløb | Dette felt er kun tilgængeligt for aftaler, hvor **Rabatoutput** i hovedet er angivet til *Økonomisk*. Angiv det beløb, der skal bruges til beregning af rabatten, baseret på den metode, du har valgt i feltet **Rabatstyringsmetode**. |

Som nævnt i den foregående tabel, skal du for aftaler, hvor feltet **Rabatoutput** i hovedet angives til *Vare*, angive de varer, der skal leveres for hver beregningslinje, under fanen **Linjer**. Benyt følgende fremgangsmåde for at angive varerne.

1. Opret den ønskede beregningslinje under fanen **Linjer**, hvis den ikke findes, og vælg den.
1. Hvis aftalen ikke er gemt, siden du oprettede beregningslinjen, skal du vælge **Gem** i handlingsruden.
1. Vælg **Varer** under fanen **Linjer**.
1. På siden **Varer** kan du bruge knapperne i handlingsruden til at føje varer til gitteret eller fjerne dem efter behov. På hver række skal du angive følgende felter:

    - **Varenummer** – Vælg den vare, der skal leveres.
    - **(Andre dimensioner)** – Hvis du skal bruge flere dimensioner til at definere varen (f.eks. varekonfiguration, størrelse, farve, typografi, lokation eller lagersted), skal du angive dem. Hvis du vil tilføje eller fjerne tilgængelige dimensioner, skal du vælge **Vis dimensioner** i handlingsruden.
    - **Antal** – Angiv det antal, der vil blive leveret, når grænsen for den valgte beregningslinje er nået.
    - **Enhed** – Vælg den enhed, som værdien **Antal** er angivet i.
    - **Multiplum** – Dette felt bruges sammen med feltet **Antal**. På en varelinje angiver du f.eks. feltet **Antal** til *2* og feltet **Multiplum** til *100*. Hvis du derefter har et samlet salgsordreantal på 150, er to af varerne gratis (to pr. 100).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Indstillinger under fanen Lagerdimensioner

Fanen **Lagerdimensioner** i oversigtspanelet **Rabatstyringsdetaljer** viser alle de tilgængelige dimensionsværdier for det produkt, der er angivet for den valgte aftalelinje. Den indeholder dimensioner, der ikke vises i oversigtspanelet **Rabatstyring**. Du kan kun redigere værdier for de dimensioner, der gælder for det valgte produkt.

Du kan føje flere dimensioner til gitteret i oversigtspanelet **Rabatstyring** ved at vælge **Vis dimensioner** i handlingsruden.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Beregningsmetoder for aftalelinjer

Hver gang du konfigurerer oplysninger for en af dine aftalelinjer som beskrevet i forrige afsnit, skal du vælge beregningsmetoden for den pågældende linje. I dette afsnit forklares de enkelte beregningsmetoder, og der vises eksempler på, hvordan den enkelte metode beregner den samlede rabat for ordre- og aftalelinjer. I disse eksempler er ordrerne og aftalelinjerne identiske. Det er kun beregningsmetoderne, der er forskellige.

### <a name="stepped-calculation-method"></a>Trinvis beregningsmetode

Den trinvise beregningsmetode beregner på trinvis basis, hvor hver enkelt aftalelinje bidrager trinvist til rabatten, indtil salgsantallet eller -værdien er nået. Trinnene kan baseres på enten antallet eller værdien af de solgte varer, afhængigt af indstillingen i feltet **Basis** under fanen **Generelt** i oversigtspanelet **Rabatstyringsdetaljer**.

Der konfigureres f.eks. en aftalelinje, så feltet **Beregningsmetode** indstilles til *Trinvis*, og **Basis**-feltet er angivet til *Værdi*. Den indeholder beregningslinjer med følgende rabatter:

- **Linje A:** 10 procent op til 1.000 kr
- **Linje B:** 25 procent op til 2.500 kr

Hvis værdien af de købte eller solgte varer er 2.000 kr, beregnes rabatten på 350 kr på følgende måde:

- **Rabat (A):** *Grænseværdi (A)* × *Procent (A)* = 1.000 kr × 10 procent = 100 kr
- **Rabat (B):** (*Solgt værdi* – *Grænseværdi (A)*) × *Procent (B)* = (2.000 kr – 1.000 kr) × 25 procent = 250 kr
- **Samlet rabat:** *Rabat (A)* + *Rabat (B)* = 100 kr + 250 kr = 350 kr

Hvis feltet **Basis** er angivet til *Antal* i stedet for *Værdi*, fungerer den trinvise beregningsmetode på samme måde. Det første trin bruges for det identificerede antal, indtil det andet trin nås. Det andet trin bruges derefter for hele antallet over det første trin, indtil det tredje trin nås. Derefter fortsætter denne proces gennem alle efterfølgende trin.

### <a name="cumulative-calculation-method"></a>Akkumuleret beregningsmetode

Der bruges kun én beregningsmetode til beregning af rabatten ved den akkumulerede beregningsmetode. Hvis der er flere tilgængelige beregningslinjer for aftalelinjen, bruges beregningslinjen med højeste værdi eller højeste antal for hele antallet eller værdien. Ligesom de andre beregningsmetoder bruger den akkumulerede metode indstillingen i feltet **Basis** under fanen **Generelt** i oversigtspanelet **Rabatstyringsdetaljer** til at bestemme, om salgsantallet eller salgsværdien bruges til at beregne rabatterne.

Der konfigureres f.eks. en aftalelinje, så feltet **Beregningsmetode** indstilles til *Akkumuleret*, og **Basis**-feltet er angivet til *Værdi*. Den indeholder beregningslinjer med følgende rabatter:

- **Linje A:** 10 procent op til 1.000 kr
- **Linje B:** 25 procent op til 2.500 kr

Hvis værdien af de købte eller solgte varer er 2.000 kr, beregnes rabatten kun ud fra linje B. Resultatrabatten på 500 kr beregnes på følgende måde:

- **Samlet rabat:** *Værdi solgt* × *Rabat (B)* = 2.000 kr × 25 procent = 500 kr

### <a name="rolling-calculation-method"></a>Glidende beregningsmetode

Den glidende beregningsmetode beregner alle mulige beregningslinjer for aftalen. Hvis der er flere beregningslinjer, og flere af dem nås, bruges alle de beregningslinjer, der nås, men de øvre tærskler gælder for hver procent. Ligesom de andre beregningsmetoder bruger den glidende metode indstillingen i feltet **Basis** under fanen **Generelt** i oversigtspanelet **Rabatstyringsdetaljer** til at bestemme, om salgsantallet eller salgsværdien bruges til at beregne rabatterne.

Der konfigureres f.eks. en aftalelinje, så feltet **Beregningsmetode** indstilles til *Glidende*, og **Basis**-feltet er angivet til *Værdi*. Den indeholder beregningslinjer med følgende rabatter:

- **Linje A:** 10 procent op til 1.000 kr
- **Linje B:** 25 procent op til 2.500 kr

Hvis værdien af de købte eller solgte varer er 2.000 kr, beregnes rabatten på 600 kr på følgende måde:

- **Rabat (A):** *Grænseværdi (A)* × *Procent (A)* = 1.000 kr × 10 procent = 100 kr
- **Rabat (B):** *Solgt værdi* × *Procent (B)* = 2.000 kr × 25 procent = 500 kr
- **Samlet rabat:** *Rabat (A)* + *Rabat (B)* = 100 kr + 500 kr = 600 kr

### <a name="total-calculation-method"></a>Samlet beregningsmåde

Den samlede beregningsmetode bruger alle beregningslinjerne til at beregne rabatten. Den anvender det samlede antal til beregning af rabatten for hver beregningslinje, der nås, og hver beregningslinje anvender sin procent på det fulde beløb. Ligesom de andre beregningsmetoder bruger den samlede metode indstillingen i feltet **Basis** under fanen **Generelt** i oversigtspanelet **Rabatstyringsdetaljer** til at bestemme, om salgsantallet eller salgsværdien bruges til at beregne rabatterne.

Der konfigureres f.eks. en aftalelinje, så feltet **Beregningsmetode** indstilles til *Samlet*, og **Basis**-feltet er angivet til *Værdi*. Den indeholder beregningslinjer med følgende rabatter:

- **Linje A:** 10 procent op til 1.000 kr
- **Linje B:** 25 procent op til 2.500 kr

Hvis værdien af de købte eller solgte varer er 2.000 kr, beregnes rabatten på 700 kr på følgende måde:

- **Rabat (A):** *Solgt værdi* × *Procent (A)* = 2.000 kr × 10 procent = 200 kr
- **Rabat (B):** *Solgt værdi* × *Procent (B)* = 2.000 kr × 25 procent = 500 kr
- **Samlet rabat:** *Rabat (A)* + *Rabat (B)* = 200 kr + 500 kr = 700 kr
