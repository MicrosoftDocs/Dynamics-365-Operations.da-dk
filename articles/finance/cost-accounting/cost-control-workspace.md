---
title: Arbejdsområde for omkostningsstyring
description: Dette emne indeholder oplysninger om arbejdsområdet Omkostningsstyring. Dette arbejdsområde er et centralt punkt, hvor ledere, der er ansvarlige for styring af et omkostningsobjekt eller en række omkostningsobjekter inden for en dimension eller på tværs af dimensioner, har adgang til rapporter.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace, CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: db587f5526e0541fc81964d510000a42a671a9bd65224e7167b9d869475c3601
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763184"
---
# <a name="cost-control-workspace"></a>Arbejdsområde for omkostningsstyring 

[!include [banner](../includes/banner.md)]

Arbejdsområdet **Omkostningsstyring** er et centralt punkt, hvor ledere, der er ansvarlige for styring af et omkostningsobjekt eller en række omkostningsobjekter inden for en dimension eller på tværs af dimensioner (for eksempel bærere and produktgrupper), har adgang til rapporter. Rapporterne i arbejdsområdet administreres fuldstændigt af omkostninger lagerbogholdere, så layoutet og de data, der bruges til rapportering, kan være ensartet på tværs af hele organisationen.

## <a name="cost-control-workspace-configuration"></a>Konfiguration af arbejdsområde for omkostningsstyring

Lagerbogholdere kan definere så mange rapportkonfigurationer, de har brug for til den ønskede datakomposition eller layoutet. En rapportkonfiguration en består af seks sektioner, der hver især bidrager til at vælge kompositionen af måldata eller layoutet.

Når du vil konfigurere et arbejdsområde for omkostningsstyring, skal du klikke på **Omkostningsregnskab** \> **Opsætning** \> **Konfiguration af arbejdsområde for omkostningsstyring**.

### <a name="general"></a>Almindelig

I oversigtspanelet **Generelt** kan du oprette et entydigt rapportlayout. Navnet på rapporten er en entydig identifikator, som brugerne kan genkende i arbejdsområdet **Omkostningsstyring**. Du kan også angive, om rapporten skal deles eller kun gælde internt for bogholdere.

| Felt       | Beskrivelse |
|-------------|-------------|
| Navn        | Angiv et entydigt navn til layoutet. |
| Beskrivelse | Angiv en mere detaljeret beskrivelse. |
| Publiceret   | Hvis du indstiller dette felt til **Ja**, kan en bruger, der er tildelt en af følgende roller, få vist rapporten i arbejdsområdet **Omkostningsstyring**:<ul><li>Vedligehold regnskabschef for omkostning</li><li>Lagerbogholder</li><li>Lagerregnskabsassistent</li><li>Controller til omkostningsobjekt</li></ul>Hvis du indstiller dette felt til **Nej**, er det kun brugere, der er tildelt en af følgende roller, der kan få vist rapporten i arbejdsområdet **Omkostningsstyring**:<ul><li>Vedligehold regnskabschef for omkostning</li><li>Lagerbogholder</li><li>Lagerregnskabsassistent</li></ul> |

### <a name="data-filtering"></a>Filtrering af data

I oversigtspanelet **Filtrering af data** skal du definere datagrundlaget for rapporten. Brugerne af denne rapport får vist værdier i rapporten, når kildedataene er blevet behandlet.

| Felt                                                             | Beskrivelse |
|-------------------------------------------------------------------|-------------|
| Finanspost for omkostningsregnskab                                            | Den **Finanspost for omkostningsregnskab**, som rapporten er baseret på. Den værdi, der er afledt af feltet **Omkostningskontrolenhed**. |
| Omkostningskontrolenhed                                                 | Den værdi, du vælger, bestemmer den finanspostering for omkostningsregnskabet og de omkostningsobjekter, som rapporten skal baseres på. |
| Statistisk dimensionshierarki, Dimensionshierarki for omkostningselement | Et konfigurationspost for **Omkostningsstyring**-arbejdsområdet kan rapportere enten ikke-pengemæssige værdier eller pengeværdier, men ikke i det samme layout. Vælg en værdi i feltet **Dimensionshierarki for omkostningselement** for at rapportere pengemæssige værdier. Vælg en værdi i feltet **Statistisk dimensionshierarki** for at rapportere ikke-pengemæssige værdier. Den dimensionshierarkipost, som du vælger, bestemmer strukturen i rapporterings- og aggregeringsniveauerne.<blockquote>[!NOTE]<br>For at få vist ikke-pengemæssige og pengemæssige værdier ved siden af hinanden kan du eksportere data til Microsoft Excel til Microsoft Power BI-indholdspakken.</blockquote> |
| Dimensionshierarki for omkostningsobjekt                                   | Vælg dimensionshierarkiet for den omkostningsobjektdimension, der passer til formålet med den rapportering, som du definerer. |
| Oprindelig budgetversion                                           | Vælg det budgetversions-id, der fungerer som det oprindelige budget i forbindelse med denne rapport. |
| Revideret budgetversion                                            | Vælg det budgetversions-id, der fungerer som det reviderede budget i forbindelse med denne rapport. |

### <a name="assign-calculation-records"></a>Tildel beregningsposter

Beregningen af faste omkostninger udfører flere beregningstrin på kildedataene, f.eks. klassificering af omkostningsfunktionalitet, omkostningsfordeling og omkostningstildeling. Beregning af flere faste omkostninger kan udføres for samme regnskabsperiode, i tilfælde af manglende kildedata eller regler, der skal opdateres. Alle beregninger af faste omkostninger gemmes med et entydigt id. Bogholderen kan vælge et specifikt id for beregning af faste omkostninger. Brugerne af rapporten, f.eks. ledere, kan se resultatet af beregningen af faste omkostninger i arbejdsområdet **Omkostningsstyring**.

| Felt                  | Beskrivelse |
|------------------------|-------------|
| Regnskabskalenderperiode | Vælg den regnskabskalenderperiode, du vil tildele et id for beregning af faste omkostninger til.<blockquote>[!NOTE]<br>De regnskabsperioder, der er angivet i feltet, stammer fra den regnskabskalender, der er knyttet til finansposteringer for omkostningsregnskab.</blockquote> |
| Aktuel version         | Vælg den relevante id for beregning af faste omkostninger. |
| Budgetversion         | Vælg den relevante id for beregning af faste omkostninger. |
| Revideret budgetversion | Vælg den relevante id for beregning af faste omkostninger. |

### <a name="fiscal-periods-per-column"></a>Regnskabsperioder pr. kolonne

I oversigtspanelet **Regnskabsperioder pr. kolonne** vælger bogholderen, hvilke regnskabsperiode der skal vises i rapportens layout.

Værdierne i de markerede kolonner skal ganges med de valgte værdier i oversigtspanelet **Regnskabsperioder pr. kolonne**.

| Felt                | Beskrivelse |
|----------------------|-------------|
| Aktuel periode       | Saldoen for den aktuelle regnskabsperiode vises.<blockquote>[!NOTE]<br>Som standard afhænger den aktuelle periode af sessionsdatoen. I arbejdsområdet **Omkostningsstyring** kan du vælge en bestemt regnskabsperiode. Den valgte værdi repræsenterer derefter den aktuelle periode.</blockquote> |
| Forrige periode      | Saldoen for den forrige regnskabsperiode vises. Følgende formel bruges:<br>Aktuel regnskabsperiode – 1<blockquote>[!NOTE]<br>Som standard afledes den forrige periode af sessionsdatoen. I arbejdsområdet **Omkostningsstyring** kan du vælge en bestemt regnskabsperiode som den aktuelle periode. **Forrige periode** genberegnes derefter i overensstemmelse hermed.</blockquote> |
| År til dato         | År til dato vises. Følgende formel bruges:<br>YearToDate (aktuel regnskabsperiode)<blockquote>[!NOTE]<br>Som standard afhænger den aktuelle periode af sessionsdatoen. I arbejdsområdet **Omkostningsstyring** kan du vælge en bestemt regnskabsperiode. Den valgte værdi repræsenterer derefter den aktuelle periode, og **År til dato**-værdien opdateres tilsvarende.</blockquote> |
| Gennemsnit år til dato | Gennemsnit for år til dato vises. Følgende formel bruges:<br>(YearToDate [aktuel regnskabsperiode]) ÷ (Antal [aktuel regnskabsperiode])<p><strong>Eksempel</strong></p><ul><li>**Statistisk dimensionsmedlem:** Fuldtidsmedarbejdere</li><li>**Dags dato:** 21-3-2017</li><li>**Periode:** Regnskabsperiode 1, regnskabsperiode 2, regnskabsperiode 3</li><li>**Størrelsesorden:** 10, 10, 12</li></ul>I dette tilfælde er **Gennemsnit år til dato** = (10 + 10 + 12) ÷ 3 = 10,67<p>Værdien i **Gennemsnit år til dato** kan beregnes for omkostningselements dimensionsmedlemmer og statistiske dimensionsmedlemmer.</p><blockquote>[!NOTE]<br>Som standard afhænger den aktuelle periode af sessionsdatoen. I arbejdsområdet **Omkostningsstyring** kan du vælge en bestemt regnskabsperiode. Den valgte værdi repræsenterer derefter den aktuelle periode, og **År til dato** og **Gennemsnit år til dato**-værdierne opdateres tilsvarende.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Kolonner, der skal vises for omkostninger

I oversigtspanelet **Kolonner, der skal vises for omkostninger** angiver bogholderen, hvilke kolonner rapportlayoutet skal indeholde. Der findes tre kategorier: fast omkostning, variabel omkostning og ikke-klassificeret omkostning.

| Felt                 | Beskrivelse |
|-----------------------|-------------|
| Fast omkostning            | Denne kolonnetype viser de faste omkostninger baseret på det valgte id for beregning af faste omkostninger.<blockquote>[!NOTE]<br>Denne kolonnetype viser kun en saldo, når der er valgt et id for beregning af faste omkostninger for regnskabsperioden.</blockquote> |
| Variabel omkostning         | Denne kolonnetype viser de variable omkostninger baseret på det valgte id for beregning af faste omkostninger.<blockquote>[!NOTE]<br>Denne kolonnetype viser kun en saldo, når der er valgt et id for beregning af faste omkostninger for regnskabsperioden.</blockquote> |
| Fast + variabel omkostning | Denne kolonnetype viser de faste omkostninger og variable omkostninger baseret på det valgte id for beregning af faste omkostninger.<blockquote>[!NOTE]<br>Denne kolonnetype viser kun en saldo, når der er valgt et id for beregning af faste omkostninger for regnskabsperioden.</blockquote> |
| Totalomkostning            | Denne kolonne viser de samlede omkostninger (ikke-klassificerede omkostninger, faste omkostninger og variable omkostninger).<blockquote>[!NOTE]<br>Kolonnetypen viser den til enhver tid gældende saldo.</blockquote> |
| Ikke-klassificeret omkostning     | Denne kolonnetype viser de ikke-klassificerede omkostninger.<blockquote>[!NOTE]<br>Denne kolonne kan bruges til at validere, om alle omkostninger er blevet klassificeret korrekt ved beregningen af faste omkostninger, eller om reglerne for omkostningsfunktionalitet skal justeres.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Kolonner, der skal vises for budgetterede omkostninger

I oversigtspanelet **Kolonner, der skal vises for budgetterede omkostninger** angiver bogholderen, hvilke kolonner der skal vises for de valgte budgetversioner. Individuelle valg kan foretages for det originale og det reviderede budget.

> [!NOTE]
> Eftersom følgende felter fungerer på samme måde for det oprindelige budget og det reviderede budget, forklares de kun én gang.

| Felt                     | Beskrivelse |
|---------------------------|-------------|
| Budget                    | Budgetsaldi vises pr. de markerede kolonner.<blockquote>[!NOTE]<br>Saldiene baseres på de budgetversioner, der er valgt i oversigtspanelet **Filtrering af data**.</blockquote> |
| Budgetafvigelse           | Beregn og vis forskellen mellem de budgetterede og de faktiske værdier. Følgende formel bruges:<br>Budgetsaldo – faktisk saldo |
| Budgetafvigelse i %      | Beregn og vis forskellen mellem de budgetterede og de faktiske værdier i procent. Følgende formel bruges:<br>(Budgetsaldo – faktisk saldo) ÷ budgetsaldo |
| Grænse for afvigelsesperiode | Angiv en grænse for afvigelsen i pengebeløb for den aktuelle periode. Hvis grænsen overskrides, markeres linjen med rødt i arbejdsområdet **Omkostningsstyring**.<blockquote>[!NOTE]<br>Dette felt gælder kun for de omkostningselementer, der repræsenterer udgifter.</blockquote> |
| Grænse for afvigelsesår   | Angiv en grænse for afvigelsen i pengebeløb for det aktuelle år. Hvis grænsen overskrides, markeres linjen med rødt i arbejdsområdet **Omkostningsstyring**. |
| Grænse for afvigelse i %      | Angiv en grænse for afvigelsen i procent. Hvis grænsen overskrides, markeres linjen med rødt i arbejdsområdet **Omkostningsstyring**.<blockquote>[!NOTE]<br>Den samme grænseprocent gælder for den aktuelle periode og det aktuelle år.</blockquote> |

## <a name="cost-control-workspace"></a>Arbejdsområde for omkostningsstyring

Arbejdsområdet **Omkostningsstyring** er designet som en webrapport. Derfor kan alle ledere, der er ansvarlige for et omkostningsobjekt, få adgang som beskrevet i [Angive adgangsrettigheder for controllere til omkostningsobjekt](access-rights-cost-object-controller.md).

Listen over rapporter, der er tilgængelige for brugere, som f.eks. ledere, styres af indstillingen **Udgivet** på siden **Konfigurationer af arbejdsområde for omkostningsstyring**.

![En rapport, som brugere kan se i arbejdsområdet Omkostningsstyring.](./media/report-cost-control.png)

En leder kan vælge den regnskabskalenderperiode, der skal vises. Sessionsdatoen bruges til at angive den aktuelle periode, der skal bruges som standard.

Værdierne i regnskabskalenderperioden bestemmes af rapportens navn og den regnskabskalender, der er valgt for de finansposteringer for omkostningsregnskab, der er knyttet til rapportens navn på siden **Konfigurationer af arbejdsområde for omkostningsstyring**.

Brugere kan vælge det aggregeringsniveau, saldi skal vises i, i dimensionshierarkiet for omkostningsobjektet. Når du aktiverer sikkerhed på adgangsniveau, kan du styre rettighederne, så brugere kun kan vælge de hierarkiniveauer, de har fået adgang til. Derfor kan de kun se de samlede saldi, som de har fået adgang til.

### <a name="add-or-remove-columns"></a>Tilføj eller fjern kolonner

Brugerne kan tilpasse kolonnerne i en rapport, så de passer til deres behov.

### <a name="view-details"></a>Vis detaljer

Brugerne kan dykke ned i detaljerne bag de saldi, der vises i arbejdsområdet. Hvis brugerne vælger en dimensionshierarkinode for et omkostningselement og derefter klikke på **Vis detaljer**, viser dialogboksen **Detaljer om omkostningselement** detaljerede oplysninger for noden.

Et gitter viser det enkelte omkostningselement, der er knyttet til omkostningselementets dimensionshierarkinode, og de tilhørende værdier. De kolonner, der vises i gitteret, stemmer overens med indstillingerne for arbejdsområdet.

To diagrammer viser en oversigt over faktisk vs. budget og budgetafvigelse pr. periode.

![Diagrammer, som viser en oversigt over faktisk vs. budget og budgetafvigelse pr. periode.](./media/cost-element-details-operations.png)

Brugerne kan klikke på **Omkostningsposter** for at dykke ned i postens oplysninger som nødvendigt.

![Omkostningsposter.](./media/cost-entries.png)

Leje er f.eks. en udgift, som fordeles til bærere. En bruger, der ønsker at forstå den lejeomkostning, som bæreren skal dække, kan undersøge, hvordan lejen er blevet beregnet.

Hvis brugerne klikker på **Fordelingsgrundlag** på siden **Omkostningsposter**, vises en dialogboks. Brugerne kan derefter tildele fordelingsgrundlaget til reglen og få vist de tilsvarende statistiske mål, der er registreret for perioden.

I følgende eksempel er fordelingsgrundlaget af typen **Fordelingsbasis for formel**, og formlen vises. De faktorer, der definerer formlen, vises. Desuden viser et gitter den beregning, der udføres pr. omkostningsobjekt.

![Beregninger pr. omkostningsobjekt.](./media/cost-entries-allocation-base.png)

Yderligere ressourcer 

[Angive adgangsrettigheder for controllere til omkostningsobjekt](access-rights-cost-object-controller.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]