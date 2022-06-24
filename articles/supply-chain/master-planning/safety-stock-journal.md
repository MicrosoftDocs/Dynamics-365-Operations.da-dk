---
title: Bruge sikkerhedslagerkladde for at opdatere minimumdisponering af varer
description: Denne artikel beskriver, hvordan sikkerhedslagerkladder bruges til at opdatere sikkerhedslagerantal for varer ved at beregne forslag til minimumdisponering baseret på historiske transaktioner.
author: t-benebo
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 385144738b83fcf6873eae5204b4784d6ecd5b80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851762"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Bruge sikkerhedslagerkladde for at opdatere minimumdisponering af varer

[!include [banner](../../includes/banner.md)]

Et sikkerhedslager er et ekstra antal af en vare, der opbevares på lageret, for at reducere risikoen for, at varen udgår fra lageret. Sikkerhedslageret bruges som buffer i tilfælde af indgående salgsordrer, hvor leverandøren ikke er i stand til at opfylde kundens ønskede afsendelsesdato.

Denne artikel beskriver, hvordan du kan bruge sikkerhedslagerkladden til at beregne minimumdækningsforslaget baseret på historiske transaktioner og derefter opdatere varedisponeringen med forslagene.

## <a name="overview-of-minimum-coverage-usage"></a>Oversigt over brug af minimumdisponering

Sikkerhedslager konfigureres på siden **Varedisponering** for hver vare. Forskellige typer genopfyldning repræsenteres af forskellige disponeringskoder. (Du kan finde flere oplysninger i [Sikkerhedslageropfyldning for varer](safety-stock-replenishment.md)). Alle disponeringskoder bruger dog den værdi, der er angivet i feltet **Minimum** på siden **Varedisponering** for hver vare. Der er to overordnede metoder til brug af feltet **Minimum**:

- **Minimumantal til min./maks. formål** – Denne tilgang bruger minimumantallet sammen med min./maks. logik. Den gælder, når feltet **Disponeringskode** er angivet til *Min./Maks.* for den relevante vare eller disponeringsgruppe. Antallet **Minimum** repræsenterer den gennemsnitlige daglige brug ganget med varens gennemløbstid.
- **Minimumantal til lagerplansformål** – I denne tilgang bruges minimumantallet til at repræsentere en lagerplan i kombination med behovsprognoser. Den gælder, når feltet **Disponeringskode** er angivet til *Periode* eller *Krav* for den relevante vare eller disponeringsgruppe. Antallet **Minimum** repræsenterer en lagerplan, der afspejler det ønskede kundeserviceniveau som et led i reducering af udgået fra lager, delforsendelser og leveringstider. Minimumantallet afspejler en procentdel af prognosenøjagtigheden for en bestemt vare. Den repræsenterer ikke en ønsket lagerposition.

Værdien **Minimum** kan angives på tre måder:

- Manuelt på siden **Varedisponering**
- Efter Data Management Framework (*Varedisponering* som dataenheder)
- Efter sikkerhedslagerberegningen, der udføres af sikkerhedslagerkladder

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Beregne minimumdisponering baseret på historisk forbrug

Sikkerhedslagerkladder bruges til at beregne et foreslået minimumsantal baseret på en varens historiske anvendelse, enten til min./maks. eller til lagerplanformål. Historisk forbrug repræsenterer alle afgangstransaktioner i en bestemt periode. Disse afgangstransaktioner omfatter salgsordretransaktioner og lagerreguleringer. I beregningerne identificeres også den virkning, som det foreslåede minimumsantal har på lagerværdien, og ændringen i lagerværdien sammenlignet med det aktuelle minimumsantal.

Hver sikkerhedslagerkladdelinje repræsenterer en vare og dens disponeringsdimensioner. Disse kladdelinjer oprettes og vises på siden **Sikkerhedslagerkladdelinjer** (**Varedisponering \> Varedisponering \> Kør \> Sikkerhedslagerberegning**). Forretningsprocessen til brug af sikkerhedslagerkladder til beregning af de foreslåede minimumsantal beskrives senere i denne artikel.

I planlægningen bruges en sikkerhedslagerkladde til at beregne foreslåede minimumantal for udvalgte varer baseret på historisk forbrug i udvalgte perioder. De foreslåede minimumværdier kan tilsidesættes manuelt, hvis det er nødvendigt, og du kan gennemgå de potentielle virkninger af det foreslåede minimum for lagerværdi. Når kladden bogføres, opdateres de tilknyttede minimumsantal i varedisponering automatisk.

### <a name="create-a-new-safety-stock-journal-name"></a>Opret et nyt sikkerhedslagerkladdenavn

Du skal oprette mindst ét sikkerhedslagerkladdenavn, før du kan oprette denne kladdetype. Du kan typisk bruge flere kladdenavne til at adskille beregningerne af sikkerhedslager.

1. Gå til **Varedisponering \> Konfiguration \> Sikkerhedslagerkladdenavne**.
1. Gå til handlingsruden, og vælg **Ny**.
1. På den nye linje skal du angive følgende felter:

    - **Navn** – Angiv et kort navn til kladden.
    - **Beskrivelse** – Angiv en kort beskrivelse af kladden.
    - **Privat for brugergruppe** – Hvis du vil begrænse målgruppen for det aktuelle kladdenavn, skal du vælge en brugergruppe.
    - **Slet linjer efter bogføring** – Markér dette afkrydsningsfelt for som standard at rydde op i kladdelinjerne, når du bogfører dem. Ryd det, hvis du vil beholde alle bogførte linjer.

    Feltet **Kladdetype** er skrivebeskyttet og er forudindstillet til *Sikkerhedslager*.

1. Luk siden.

### <a name="create-a-safety-stock-journal-and-lines"></a>Oprette en sikkerhedslagerkladde og linjer

Dette trin opretter en kladde og føjer automatisk linjer til den. Hver linje identificerer en vare, dens disponeringsdimensioner og flere beregnede antal fra brugshistorikken. De beregnede antal omfatter gennemsnitsudstedelser pr. varegennemløbstid, gennemsnitligt antal udstedelser pr. måned og den månedlige standardafvigelse.

#### <a name="automatically-generate-journal-lines"></a>Oprette kladdelinjer automatisk

Kladdelinjer kan kun genereres automatisk, hvis der ikke findes linjer for den kladde, der vises i øjeblikket.

Benyt følgende fremgangsmåde for at generere kladdelinjer automatisk.

1. Gå til **Varedisponering \> Varedisponering \> Kør \> Beregning af sikkerhedslager**.
1. Gå til handlingsruden, og vælg **Ny**. Der oprettes en ny sikkerhedslagerkladde.
1. I oversigtspanelet **Journalhoveddetaljer** skal du angive følgende felter:

    - **Navn** – Vælg navnet på sikkerhedslagerkladden, som linjen skal føjes til.
    - **Beskrivelse** – Standardværdien er beskrivelsen af det valgte kladdenavn. Du kan dog redigere værdien efter behov.
    - **Slet linjer efter bogføring** – Markér dette afkrydsningsfelt for at rydde op i kladdelinjerne, når du bogfører dem. Ryd det, hvis du vil beholde alle bogførte linjer. Indstillingen nedarves fra det valgte kladdenavn.

    Feltet **Kladde** er skrivebeskyttet og viser id-nummeret på den kladde, du er ved at oprette og føje linjer til.

1. Vælg **Opret linjer** på værktøjslinjen i oversigtspanelet **Kladdelinjer**.
1. I dialogboksen **Opret kladdelinjer til foreslåede minimumslagerniveauer** skal du angive følgende felter:

    - **Fra dato** – Vælg startdatoen i den periode, som udstedelserne skal medtages i beregningen for.
    - **Til dato** – Vælg slutdatoen i den periode, som udstedelserne skal medtages i beregningen for. Der skal være mindst to måneder mellem start- og slutdatoen.
    - **Beregn standardafvigelse** – Angiv denne indstilling til *Ja* for at beregne standardafvigelsen. Du skal angive denne indstilling til *Ja* for at bruge indstillingen **Brug serviceniveau**, når du beregner forslaget (som beskrevet senere i denne artikel).

1. I oversigtspanelet **Poster, som skal medtages** kan du konfigurere filtre og begrænsninger for at definere, hvilke elementer der skal medtages. (Du kan f.eks. filtrere efter **Disponeringsgruppeværdi**). Vælg **Filter** for at åbne en standarddialogboks til forespørgselseditoren, hvor du kan definere udvælgelseskriterier, sorteringskriterier og join-forbindelser. Felterne fungerer på samme måde som for andre typer af forespørgsler i Microsoft Dynamics 365 Supply Chain Management.
1. På oversigtspanelet **Kør i baggrunden** skal du vælge, om jobbet skal køres i batchtilstand, og/eller konfigurere en tilbagevendende tidsplan. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK**. Linjer oprettes for de dimensioner, der har lagerposteringer.

#### <a name="manually-add-or-remove-journal-lines"></a>Tilføje eller fjerne kladdelinjer manuelt

Du kan manuelt tilføje og/eller fjerne kladdelinjer når som helst (enten efter eller i stedet for automatisk genererede linjer). Brug følgende knapper på værktøjslinjen i oversigtspanelet **Kladdelinjer**:

- **Ny** – Tilføj en ny linje. Angiv derefter en værdi i hver kolonne for at definere det produkt, der skal beregnes og anvendes nye minimumsværdier for. Da foreslåede minimumberegninger ikke er tilgængelige for manuelt tilføjede linjer, vises der ikke nye værdier for **Beregnet minimumantal** af dem. Du skal derfor angive værdierne af **Nyt minimumantal** manuelt. Du kan dog stadig se den potentielle virkning af værdien **Nyt minimumantal** på lagerværdien og den potentielle ændring i lageret sammenlignet med det aktuelt angivne minimum.
- **Slet** – Slet den valgte linje.
- **Slet kladdelinjer** – Slet alle linjer i kladden.

### <a name="calculate-a-proposal"></a>Beregne et forslag

Dette trin beregner et foreslået minimum for hver kladdelinje og linjens potentielle indflydelse på lagerværdien. (Det foreslåede minimum vises som **Beregnet minimumantal**-værdi). Du kan udføre beregningen flere gange, som du vil. Beregningen opdaterer den værdi af **Beregnet minimumantal**, der vises for alle kladdelinjer.

De beregninger, der vises, påvirker ikke de faktiske minimumantalsværdier for hvert produkt, før du har valgt **Bogfør** i handlingsruden. På det tidspunkt anvendes værdierne af **Nyt minimumantal** for hvert produkt.

1. Gå til **Varedisponering \> Varedisponering \> Kør \> Beregning af sikkerhedslager**.
1. Åbn den kladde, der skal beregnes et forslag for. Du kan også oprette en ny kladde som beskrevet tidligere i denne artikel.
1. Vælg **Opret forslag** på værktøjslinjen i oversigtspanelet **Kladdelinjer**. (Du behøver ikke vælge linjer).
1. I dialogboksen **Beregn forslag for minimumslagerniveau** skal du angive følgende felter:

    - **Brug gns.afgang under gennemløbstiden** – Vælg denne indstilling for at generere **Beregnet minimumantal**-værdier baseret på den gennemsnitlige afgang i den angivne periode. Angiv derefter en værdi i feltet **Multiplikationsfaktor** for at justere resultatet efter behov. Du kan f.eks. angive *1,0* for at bruge det nøjagtige beregnede gennemsnit eller *1,1* for at tilføje en ekstra buffer på 10 procent.
    - **Brug serviceniveau** – Vælg denne indstilling for at beregne et foreslået minimum baseret på det ønskede serviceniveau. Vælg derefter det foretrukne serviceniveau i feltet **Serviceniveau**.
    - **Leveringstidmargen** – Angiv en værdi for at udvide den normale leveringstid (f.eks. for at give tid til administration).
    - **Brug det beregnede minimumantal som det nye minimumantal** – Angiv denne indstilling til *Ja*, hvis du automatisk vil kopiere værdier fra kolonnen **Beregnet minimumantal** til kolonnen **Nyt minimumantal** for alle linjer, når beregningen er fuldført. Hvis du angiver denne indstilling til *Nej*, kopieres værdien af **Aktuel minimummængde** til kolonnen **Ny minimummængde** for alle linjer. Derefter skal du redigere værdierne for **Ny minimummængde** manuelt efter behov.

1. På oversigtspanelet **Kør i baggrunden** skal du vælge, om jobbet skal køres i batchtilstand, og/eller konfigurere en tilbagevendende tidsplan. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK**. Resultaterne af beregningen vises i kolonnen **Beregnet minimumantal** i oversigtspanelet **Kladdelinjer**. I øjeblikket er værdierne kun foreslåede værdier, som endnu ikke er anvendt på dine produkter.

### <a name="update-minimum-quantity"></a>Opdater minimummængde

Du kan markere en hvilken som helst linje i en sikkerhedslagerkladde og manuelt tilsidesætte værdien i feltet **Ny minimummængde**.

1. Gå til **Varedisponering \> Varedisponering \> Kør \> Beregning af sikkerhedslager**.
1. Åbn kladden, der skal redigeres. Du kan også oprette en ny kladde som beskrevet tidligere.
1. Find den linje, der skal reguleres, i oversigtspanelet **Kladdelinjer**, og rediger derefter værdien i kolonnen **Ny minimummængde**. Du kan f.eks. angive værdien af **Ny minimummængde**, så den svarer til værdien af **Beregnet minimumantal**. Hvis værdien af **Beregnet minimumantal** er *0* (nul), kan du angive den ønskede fremtidige værdi.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Bogfør det nye minimumantal, og valider resultatet

Følg disse trin for at bogføre det nye minimumantal og validere resultatet.

1. Gå til **Varedisponering \> Varedisponering \> Kør \> Beregning af sikkerhedslager**.
1. Åbn den kladde, der skal bogføres nye minimumantal for. Du kan også oprette en ny kladde som beskrevet tidligere.
1. Vælg **Bogfør** i handlingsruden.
1. I dialogboksen **Bogfør kladde** skal du angive feltet **Overfør alle bogføringsfejl til en ny kladde** efter behov. Vælg derefter **OK** for at bogføre kladden.
1. Hvis du har ændret værdien af **Ny minimummængde** for en linje i oversigtspanelet **Kladdelinjer**, kan du bekræfte ændringen ved at følge disse trin:

    1. Vælg linket i kolonnen **Varenummer** for den linje, du har redigeret.
    1. I dialogboksen **Produktoplysninger** skal du vælge linket i feltet **Varenummer** for at åbne den relaterede frigivne produktpost.
    1. Vælg **Varedisponering** i gruppen **Disponering** under fanen **Planlæg** i handlingsruden.
    1. Bemærk, at **Minimum**-værdien for den lokation og det lagersted, du har justeret ved hjælp af den bogførte sikkerhedslagerkladde, nu er opdateret, så den svarer til din redigering.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Opfyldning af sikkerhedslager for varer](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
