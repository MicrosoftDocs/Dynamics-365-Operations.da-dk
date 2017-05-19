---
title: "Rækkedefinitioner i Designer til økonomirapporter"
description: "En rækkedefinition er en rapportkomponent, eller dokumentkomponent, der angiver indholdet af hver række i en økonomirapport. En rækkedefinition kan kombineres med kolonnedefinitioner, rapporteringstrædefinitioner og rapportdefinitioner, så de danner en komponentgruppe, der kan bruges af flere firmaer."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: aa9fcc4d0c122d2355362b75ca210af4c2ef4338
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="row-definitions-in-financial-report-designer"></a>Rækkedefinitioner i Designer til økonomirapporter

[!include[banner](../includes/banner.md)]


En rækkedefinition er en rapportkomponent, eller dokumentkomponent, der angiver indholdet af hver række i en økonomirapport. En rækkedefinition kan kombineres med kolonnedefinitioner, rapporteringstrædefinitioner og rapportdefinitioner, så de danner en komponentgruppe, der kan bruges af flere firmaer.

<a name="create-a-row-definition"></a>Opret en rækkedefinition.
-----------------------

1.  Klik på **Rækkedefinitioner** i navigationsruden i Report Designer.
2.  Klik på **Ny** i menuen **Filer**, og klik derefter på **Rækkedefinition**. Der er flere oplysninger om indholdet af hver celle under [Redigere rækkedefinitionsceller](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Åbn en rækkedefinition
1.  Klik på **Rækkedefinitioner** i navigationsruden i Report Designer.
2.  Dobbeltklik på navnet på den rækkedefinition, du vil åbne.
3.  For at få vist de komponenter, der hører til rækkedefinitionen, skal du højreklikke på rækkedefinitionen, og derefter vælge **Tilknytninger**.

## <a name="contents-of-a-row-definition"></a>Indholdet af en rækkedefinition
En rækkedefinition kan indeholde op til 20.000 rækker med økonomiske dimensioner og kan indeholde følgende oplysninger:

-   Beskrivende tekst i form af afsnitsoverskrifter, linjer og mellemrum, der har en forklarende funktion i rapporten, f.eks. **Kontanter** eller **Samlet omsætning**.
-   Links til økonomiske data, der kan indeholde dimensionsværdier i Microsoft Dynamics 365 for Operations **Bemærk!** Du kan oprette en rækkedefinition til at hente data fra systemet med de økonomiske dimensioner, hver gang der genereres en rapport.
-   Rækketotaler og formler, der er baseret på de tilknyttede økonomiske data

Hver række i en rækkedefinition indeholder normalt en af følgende typer oplysninger:

-   Henvisninger til systemet med økonomiske dimensioner
-   Totaler eller beregninger, der er baseret på dataene
-   Formattering

Der er to metoder til at angive oplysninger i en rækkedefinition:

-   Du kan indtaste rækkeoplysninger manuelt i en ny rækkedefinition. Yderligere oplysninger finder du under [Redigere rækkedefinitionsceller](modify-row-definition-cells-financial-reporting.md).
-   Du kan bruge rapportdesigneren til at trække oplysninger direkte fra de økonomiske dimensioner. Du kan finde flere oplysninger i afsnittet "Relaterede formler/rækker/enheder" i [Ændre rækkedefinitionsceller](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a>Tilføje dimensioner i en rækkedefinition
En dimension er et skæringspunkt for data og værdier. Du kan gruppere data og værdier i Report Designer. Du kan derefter klassificere og analysere posteringer i flere detaljer. Du kan bruge dialogboksen **Indsæt rækker fra dimensioner** til at føje flere rækker til en rækkedefinition på samme tid. Dialogboksen indeholder én kolonne for hver dimension. Følgende tabel beskriver de oplysninger, du kan angive for hver dimension.

| Indstilling                | Beskrivelse                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimension             | Det mønster, der identificerer den dimension, der skal føjes til rækkedefinitionen. Dette mønster indeholder et (&) eller et nummertegn (\#) for hver enkelt position i dimensionerne. Generelt skal du bruge alle plustegn for hovedkontodimensionen og alle nummertegn til andre dimensioner. |
| Start på dimensionsområde | Den første værdi for den dimension, der skal føjes til rækkedefinitionen.                                                                                                                                                                                                                 |
| Slut på dimensionsområde   | Den sidste værdi for den dimension, der skal føjes til rækkedefinitionen.                                                                                                                                                                                                                  |

Udfør følgende trin for at føje dimensioner til en rækkedefinition.

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  I menuen **Rediger** skal du klikke på **Indsæt rækker fra dimensioner**.
3.  I dialogboksen **Indsæt rækker fra dimensioner**i rækken **Dimensioner** skal du markere cellen for den dimension, der skal overføres til rækkedefinitionen, og derefter klikke på **Alle &&&**.
4.  For at begrænse rækkedefinitionen til et bestemt område af dimensionsværdier skal du angive startdimensionsværdien i cellen **Start på dimensionsområde**og derefter angive slutdimensionsværdien i cellen **Slut på dimensionsområde**. Hvis du vil medtage alle værdier for den valgte dimension, skal du lade disse celler være tomme. **Bemærk!** Jokertegn (\* eller ?) i dimensionsområder returnerer muligvis ikke alle de ønskede resultater, afhængigt af hvordan ERP-databasen indsamler data.
5.  I feltet **Startrækkekode** skal du angive rækkekoden for den første dimensionsværdi, der skal føjes til rækkedefinitionen.
6.  I feltet **Forøg hver række med** skal du angive afstanden mellem på hinanden følgende rækkekoder. Hvis den første rækkekode er 100, og den stigende værdi er 30, har de første nye rækker koderne 100, 130, 160, 190 og 220. Brug en forøgelsesværdi, der indeholder tilstrækkelig plads til at indsætte nye formater og formelrækker.
7.  Klik på **OK**. Der tilføjes én linje for hver af de valgte dimensionsværdier i rækkedefinitionen.

## <a name="adjust-rounding-in-a-row-definition"></a>Justere afrunding i en rækkedefinition
Hvis du har en balance, hvor beløbene er afrundede, stemmer totalerne muligvis ikke. Dette problem kan opstå, hvis du f.eks. bruger afrundingsindstillingen på en balancerapport og rapportdefinitionen angiver også afrunding. Du kan bruge indstillingen **Afrundingsdifference** i rækkedefinitionen for at afbalancere beløbene i balancer. Du kan slå afrunding fra eller ændre det under fanen **Indstillinger** i rapportdefinitionen. I følgende tabel vises, hvordan beløb afrundes. I denne tabel afviger totalerne for række 100 og 200, når afrunding er aktiveret.

| Rækkekode | Beløb uden afrunding | Beløb med afrunding til hele tusinder |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| I alt    | 7,300                    | 8                                       |

Hvis du vil justere afrunding i en balance, skal du følge disse trin.

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  I menuen **Rediger** skal du klikke på **Regulering af afrunding**.
3.  I dialogboksen **Regulering af afrunding** skal du angive følgende værdier:
    -   **Række til regulering af afrunding** – rækkekoden for den række, der skal reguleres for at afstemme balancen.
    -   **Række for samlede aktiver** – rækkekoden for den række i balancen, der indeholder de samlede aktiver.
    -   **Række for samlede passiver og egenkapital** – rækkekoden for den række i balancen, der indeholder de samlede passiver og egenkapital.
    -   **Reguleringsbeløbsgrænse** – et positivt heltal, der angiver grænsen for automatiske reguleringer. Dette beløb sammenlignes med den absolutte værdi af den faktiske afrundingsdifference.

    **Bemærk:**Disse rækkekoder skal være knyttet til de økonomiske data. Med andre ord skal rækken have en dimensionsværdi i cellen **Link til økonomiske dimensioner**. Henvis **ikke** en beskrivelsesrække (**DESC**), beregnet række (**CALC**) eller sammenlagt (**TOT**) række.

Beløbene i din balance er nu afstemt, hvis afrunding er slået til. **Bemærk:**Reguleringsgrænsen anvendes baseret på indstillingen **Afrundingspræcision**, der er angivet til rapportdefinitionen. Hvis du for eksempel vælger at afrunde rapporten til tusinder og angiver **2** i feltet **Reguleringsbeløbsgrænse**, vises en advarselsmeddelelse, når værdien i feltet **Række til regulering af afrunding** øges eller reduceres med mere end $2.000.

## <a name="format-row-and-column-text"></a>Formatere række og kolonnetekst
Du kan tilpasse udseendet af dine rapporter ved at ændre skrifttyper og formatere tekst. I følgende afsnit beskrives, hvordan du kan formatere udseendet af rækker og kolonner i rapporter.

### <a name="manage-font-styles"></a>Administrere typografier

Du kan oprette og ændre typografier for rapporten. Du kan derefter anvende disse typografier i dokumentet eller på en bestemt række eller kolonne i en rapport.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Oprette en typografi</td>
<td><ol>
<li>I menuen <strong>Formater</strong> i Report Designer skal du klikke på <strong>Typografier og formatering</strong>.</li>
<li>Klik på <strong>Ny</strong> i dialogboksen <strong>Typografier og formatering</strong> og derefter skrive et entydigt navn til den nye typografi.</li>
<li>Vælg skrifttype, og klik derefter på <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Ændre en typografi</td>
<td><ol>
<li>I menuen <strong>Formater</strong> i Report Designer skal du klikke på <strong>Typografier og formatering</strong>.</li>
<li>Vælg en typografi, der skal ændres, i dialogboksen <strong>Typografier og formatering</strong>, og klik derefter på <strong>Rediger</strong>.</li>
<li>Vælg skrifttype, og klik derefter på <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Anvende en typografi</td>
<td><ol>
<li>I Report Designer i en definition eller kolonnedefinition eller i sidehoveder og sidefødder skal du vælge en eller flere celler.</li>
<li>Vælg en typografi på listen <strong>Typografi</strong> på værktøjslinjen.</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Formatere rækketekst

Den formatering, der er angivet i rækkedefinitionen, tilsidesætter den formatering, der er angivet i kolonnedefinitionen og rapportdefinitionen. Du kan ændre tekstformatet ved hjælp af kontrolelementerne på formateringsværktøjslinjen. Disse kontrolelementer er standardkontrolelementer til Microsoft Windows.

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  Marker de celler, der skal formateres. Du kan markere flere celler ved at holde Ctrl-tasten nede, mens du markerer cellen.
3.  Klik på værktøjslinjeknappen for det format, du vil anvende. Hvis du for eksempel vil indrykke en række, skal du markere rækken og derefter klikke på **Forøg indrykning** ![Forøg indrykning](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Forøg indrykning") på værktøjslinjen.

### <a name="adjust-columns-while-you-design-reports"></a>Justere kolonner, mens du designer rapporter

For at gøre det lettere at få vist de kolonner, du arbejder på i rækkedefinitionen, kan du også justere bredden på en kolonne og skjule (minimere) eller vise kolonner i visningsruden. De ændringer, du foretager, påvirker kun visningen på skærmen af kolonnerne. De påvirker ikke kolonneformateringen i rapporter.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Ændre bredden på en kolonne i visningsruden

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  Vælg **Kolonnebredde** i menuen **Formater**.
3.  Angiv en værdi i dialogboksen **Kolonnebredde**, og klik derefter på **OK**. Du kan også trække i højre kant af cellen med kolonneoverskriften for at ændre kolonnens bredde.

### <a name="hide-columns-in-the-view-pane"></a>Skjule kolonner i visningsruden

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  Vælg den eller de kolonner, der skal minimeres.
3.  Højreklik, og klik derefter på **Skjul**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Få vist alle skjulte kolonner i visningsruden

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  Højreklik på den minimerede kolonne, der skal vises, og klik derefter på **Vis**.


<a name="see-also"></a>Se også
--------

[Økonomirapportering](financial-reporting-intro.md)




