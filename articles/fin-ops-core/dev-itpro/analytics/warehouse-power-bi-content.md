---
title: Power BI-indhold til Lagerstedperformance
description: Denne artikel beskriver, hvad der er omfattet af Power BI-indhold til lagerstedsperformance.
author: Mirzaab
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d43cef4970cdf180d0db39086220def56b08f280
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851916"
---
# <a name="warehouse-performance-power-bi-content"></a>Power BI-indhold til Lagerstedperformance

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvad der er omfattet af Microsoft Power BI-indhold til **Lagerstedsperformance**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der bruges til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indhold til **Lagerstedperformance** er oprettet, så lagerstedschefer og driftsledere kan overvåge indgående og udgående nøgletal og nøgletal for lager. Det bruger styring af lagersted, produktdata og andre transaktionsdata fra dit system og giver både en samlet oversigt over lagerstedperformance og en opdeling for kreditorer, produktgrupper og produkter og websted og lagersteder.

Lagerchefer kan bruge Power BI-indhold til **Lagerstedsperformance** til at måle følgende tre områder:

- **Indgående performance**: Måler, hvor godt en leverandør fungerer i forhold til kundekrav (med andre ord måles leveringsperformance) og måler læg på lager-performance, så du kan identificere problemer, der involverer arbejdere eller varer i en periode. Det er vigtigt, at du ved, om leverandører leverer til tiden, tidligt eller for sent, så du kan bestemme, hvordan leverandørers performance påvirker den overordnede læg-på-lager-performance. En leverandør, der leverer uden for de datoer, der er aftalt, kan give ekstra belastning for lageret på grund af uventet arbejde og kan øge den gennemsnitlige tid til at lægge på lager.
- **Leveringsperformance**: Måler, om lageret leverer alle varer og til tiden til kunder (med andre ord måle udgående leveringsperformance), så du kan identificere eventuelle problemer, der vedrører produkter, lokationer eller lagersteder eller dedikerede kunder. Hvis du bliver opmærksom på, at du leverer for sent til bestemte områder eller byer, skal du muligvis fokusere mere på transport eller kontoadministration.
- **Lagernøjagtighed på lokation**: Lagernøjagtighed er vigtig intern business intelligence (BI) for et lagersted. Det er meget vigtigt, at du bestemmer, hvor præcise dine optællinger er generelt. Men det er også vigtigt at fastlægge, hvor nøjagtig din opbevaring af varer er på de rette steder, og at du fremhæver data vedr. uoverensstemmelser, så du kan finde bedre placeringer til varer eller starte en samlet optælling af bestemte varer. (I øjeblikket leveres den nye varebaserede funktionalitet til optælling som et hotfix). Hvis du bruger dette Power BI-indhold til at bestemme korrektheden af dataene for den disponible lagerbeholdning pr. lokation, kan du også identificere tyveri i dine butikker. Du kan også bestemme, om der er disponible mængder på andre lokaliteter, der afviger fra ERP-dataene (enterprise resource planning). Disse lokaliteter kan være for store, eller de kan være umulige at tælle. Det kan også være, at den fysiske placering er uhensigtsmæssig, så det er svært at holde en enkelt type vare synkroniseret med disponible data.

## <a name="accessing-the-power-bi-content-pack"></a>Adgang til Power BI-indholdspakken
Power BI-indholdet **Lagerstedperformance** vises på siden **Lagerstedperformance** (**Lokationsstyring** \> **Forespørgsler og rapporter** \> **Performanceanalyse for lagersted** \> **Lagerstedperformance**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indholdet
Power BI-indholdet til **Lagerstedsperformance** omfatter en rapport. Denne rapport består af en række målinger, som er visualiseret som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne i Power BI-indholdet til **Lagerstedsperformance**.

| Rapportside                 | Diagrammer                                   | Betegnelse |
|-----------------------------|------------------------------------------|-------------|
| Indgående performance         | Lagt på lager i alt                          | Antallet af linjer med læg-på-lager-arbejde, der behandles i en given tidsperiode. |
| Indgående performance         | Gennemsnitlig læg på lager-tid                    | Den gennemsnitlige tid i timer for alle læg-på-lager-linjer i indkøbsordre, der behandles fra registreringen af varerne, indtil sidst læg på lager-handling. |
| Indgående performance         | Modtaget tidligt                           | Antallet af indkøbsordrelinjer, der er modtaget tidligt. |
| Indgående performance         | Modtaget til tiden                         | Antallet af indkøbsordrelinjer, der er modtaget til tiden. |
| Indgående performance         | Modtaget sent                            | Antallet af indkøbsordrelinjer, der er modtaget for sent. |
| Indgående performance         | Til tiden fra leverandør                        | En visning af procentdelen af indkøbsordrelinjer, der er modtaget fra en leverandør eller leverandørgruppe, tidligt, til tiden og for sent. |
| Indgående performance         | Lagt på lager, fra område til lagerbeholdning (timer) | Den gennemsnitlige tid for område til lagerbeholdning i timer over tid. |
| Indgående performance         | Lagt på lager i gennemsnit pr. arbejder               | Den gennemsnitlige tid i timer, som læg-på-lager-behandling af indkøbsordrelinjer har taget en arbejder. |
| Indgående performance         | Lagt på lager i gennemsnit pr. leverandør          | Den gennemsnitlige læg-på-lager-tid i timer pr. leverandør eller leverandørgruppe. |
| Indgående performance         | Lagt på lager i gennemsnit pr. produkt         | Den gennemsnitlige læg-på-lager-tid i timer pr. vare eller varegruppe. |
| Lagernøjagtighed på lokation | Samlet antal                              | Antallet af optællingsarbejdslinjer, der behandles i en given periode. |
| Lagernøjagtighed på lokation | Afvigelseshyppighed                         | Den samlede afvigelseshyppighed som en procentdel af alle linjer, der tælles for en given periode. |
| Lagernøjagtighed på lokation | Antal uden afvigelse                | Det antal linjer, der behandles uden afvigelser, ud af det samlede antal af optællingsarbejdslinjer, der behandles. |
| Lagernøjagtighed på lokation | Varer optalt over tid                  | De procentdel af varer, der optælles med og uden afvigelse over tid. |
| Lagernøjagtighed på lokation | Afvigelse i vareantal større end % | En tabelvisning af optællingslinjer med afvigelser, der overskrider den angivne procentdel. Tabellen indeholder oplysninger om lokationer, varer, gennemsnitlig afvigelse, samlet antal optællingsarbejdslinjer, der er optalt, antal optællingslinjer med afvigelser for lokationen, gennemsnitligt optalt antal, forventet samlet antal, der skal optælles, og det faktiske vareantal, der er optalt. |
| Lagernøjagtighed på lokation | Vareantal pr. arbejder                     | Arbejderes optællingsperformance. Performance udtrykkes som en procentdel af optællingsarbejdslinjer, der har og ikke har afvigelser. |
| Lagernøjagtighed på lokation | Vareantal pr. sted/lagersted           | Optællingsperformance efter antallet af behandlede optællingsarbejdslinjer pr. sted eller lagersted, der ikke har uoverensstemmelser. |
| Lagernøjagtighed på lokation | Afvigelseshyppighed pr. produkt              | Afvigelseshyppighed for optællingsperformance. Satsen udtrykkes som en procentdel af behandlede optællingsarbejdslinjer pr. vare eller varegruppe. |
| Leveringsperformance        | Linjer, der er leveret                            | Det samlede antal forsendelseslinjer, der er leveret i en given periode. |
| Leveringsperformance        | For tidlig                                    | Procentdelen af leverancelinjer, der leveres tidligt. |
| Leveringsperformance        | Til tiden                                  | Procentdelen af leverancelinjer, der leveres til tiden. |
| Leveringsperformance        | For sent                                     | Procentdelen af leverancelinjer, der leveres for sent. |
| Leveringsperformance        | Forsendelser over tid                      | Den procentdel af forsendelseslinjer, der er leveret til tiden, tidligt eller for sent i en given periode. En tendenslinje viser tendensen for linjer, der er sendt til tiden. |
| Leveringsperformance        | Sendt for sent efter by                     | En kortvisualisering af byer og områder, der påvirkes af forsinkede forsendelser. |
| Leveringsperformance        | Afsendt efter biprodukt                       | Den procentdel, der er leveret tidligt, til tiden eller for sent efter vare eller varegruppe. |
| Leveringsperformance        | Afsendt efter kunder                      | Den procentdel, der er leveret tidligt, til tiden eller for sent efter kunde eller kundegruppe. |
| Leveringsperformance        | Afsendt pr. websted/lagersted              | Den procentdel, der er leveret tidligt, til tiden eller for sent pr. sted eller lagersted. |

## <a name="understanding-the-data-model-and-calculations"></a>Om datamodellen og beregninger
Følgende data bruges til at udfylde rapportsiderne i Power BI-indholdet til **Lagerstedperformance**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Power BI-integration med Enhedslager](power-bi-integration-entity-store.md).

Følgende samlede nøglemålinger bruges som grundlag for indholdet.

| Rapportside                 | Diagrammer                                   | Tabeller                                | Beskrivelse af beregninger |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Indgående performance         | Lagt på lager i alt                          | WHSWorkLine                           | Antallet af arbejdslinjer, hvor arbejdstypen er **læg på lager**. |
| Indgående performance         | Gennemsnitlig læg på lager-tid                    | WHSWorkLine                           | Summen af maks. tid for arbejdslinjer divideret med antallet af maks. tid for arbejdslinjer, hvor maks. tid for arbejdslinjer er den maksimale forskel mellem oprettelsesdatoen og afslutningsdatoen for arbejdet. |
| Indgående performance         | Modtaget tidligt                           | WHSWorkLine                           | Antallet af arbejdslinjer, hvor arbejdets oprettelsesdato ligger før den leveringsdato, der bruges. Hvis dato for bekræftelse af leveringen ikke er angivet, kan du bruge standardleveringsdatoen. |
| Indgående performance         | Modtaget til tiden                         | WHSWorkLine                           | Antallet af arbejdslinjer, hvor arbejdets oprettelsesdato er lig med den leveringsdato, der bruges. Hvis dato for bekræftelse af leveringen ikke er angivet, kan du bruge standardleveringsdatoen. |
| Indgående performance         | Modtaget sent                            | WHSWorkLine                           | Antallet af arbejdslinjer, hvor arbejdets oprettelsesdato ligger efter den leveringsdato, der bruges. Hvis dato for bekræftelse af leveringen ikke er angivet, kan du bruge standardleveringsdatoen. |
| Indgående performance         | Til tiden fra leverandør                        | WHSWorkLine                           | Modtaget tidligt, modtaget til tiden og modtaget for sent (se beskrivelserne tidligere i denne tabel). |
| Indgående performance         | Lagt på lager, fra område til lagerbeholdning (timer)   | WHSWorkLine                           | Gennemsnitlig tid for lagt på lager (se beskrivelsen tidligere i denne tabel). |
| Indgående performance         | Lagt på lager i gennemsnit pr. arbejder               | WHSWorkLine                           | Gennemsnitlig tid for lagt på lager (se beskrivelsen tidligere i denne tabel). |
| Indgående performance         | Lagt på lager i gennemsnit pr. leverandør          | WHSWorkLine                           | Gennemsnitlig tid for lagt på lager (se beskrivelsen tidligere i denne tabel). |
| Indgående performance         | Lagt på lager i gennemsnit pr. produkt         | WHSWorkLine                           | Gennemsnitlig tid for lagt på lager (se beskrivelsen tidligere i denne tabel). |
| Lagernøjagtighed på lokation | Samlet antal                              | WHSWorkLineCycleCount                 | Cyklusoptællinger, hvor det absolutte afvigelsesantal er lig med eller større end 0 (nul). |
| Lagernøjagtighed på lokation | Afvigelseshyppighed                         | WHSWorkLineCycleCount                 | Cyklusoptællinger, der har afvigelser, divideret med det samlede antal. En cyklusoptælling anses for at have afvigelser, hvis det absolutte afvigelsesantal er større end 0 (nul). |
| Lagernøjagtighed på lokation | Antal uden afvigelse                | WHSWorkLineCycleCount                 | Cyklusoptællinger, hvor det absolutte afvigelsesantal er større end 0 (nul). |
| Lagernøjagtighed på lokation | Antal med afvigelse                   | WHSWorkLineCycleCount                 | Cyklusoptællinger, hvor det absolutte afvigelsesantal er lig med 0 (nul). |
| Lagernøjagtighed på lokation | Varer optalt over tid                  | WHSWorkLineCycleCount                 | Antal uden afvigelse og Antal med afvigelse (se beskrivelserne tidligere i denne tabel). |
| Lagernøjagtighed på lokation | Afvigelse i vareantal større end % | WHSWorkLineCycleCount                 | Den gennemsnitlige afvigelse er antallet af absolutte afvigelser divideret med det forventede antal, hvor antallet af absolutte afvigelser er større end 0 (nul). Det gennemsnitlige antal afvigelse er det gennemsnitlige antal af absolutte afvigelser, hvor antallet af absolutte afvigelser er større end 0 (nul). Antal med afvigelse, samlet antal, forventet antal og optalt antal, hvor hele antallet er grupperet efter vare og lokation (se beskrivelserne tidligere i denne tabel). |
| Lagernøjagtighed på lokation | Vareantal pr. arbejder                     | WHSWorkLineCycleCount                 | Antal uden afvigelse og Antal med afvigelse (se beskrivelserne tidligere i denne tabel). |
| Lagernøjagtighed på lokation | Vareantal pr. sted/lagersted           | WHSWorkLineCycleCount                 | Antal uden afvigelse og Antal med afvigelse (se beskrivelserne tidligere i denne tabel). |
| Lagernøjagtighed på lokation | Afvigelseshyppighed pr. produkt              | WHSWorkLineCycleCount                 | Afvigelseshyppighed (se beskrivelsen tidligere i denne tabel). |
| Leveringsperformance        | Linjer, der er leveret                            | SalesLine               | Antallet af salgslinjer, hvor salgslinjer er afsendt. |
| Leveringsperformance        | For tidlig                                    | CustPackingSlipOnTimeStatus           | Salgslinjer, hvor status for afsendelsesdato er **1 (tidlig)**. Tidlig betyder, at afsendelsesdatoen for følgesedlen er tidligere end den bekræftede afsendelsesdato på salgslinjen. Hvis den bekræftede afsendelsesdato ikke er angivet, bruges den ønskede afsendelsesdato. |
| Leveringsperformance        | Til tiden                                  | CustPackingSlipOnTimeStatus           | Salgslinjer, hvor status for afsendelsesdato er **2 (til tiden)**. Til tiden betyder, at afsendelsesdatoen for følgesedlen er lig med den bekræftede afsendelsesdato på salgslinjen. Hvis den bekræftede afsendelsesdato ikke er angivet, bruges den ønskede afsendelsesdato. |
| Leveringsperformance        | For sent                                     | CustPackingSlipOnTimeStatus           | Salgslinjer, hvor status for afsendelsesdato er **3 (for sent)**. For sent betyder, at afsendelsesdatoen for følgesedlen er senere end den bekræftede afsendelsesdato på salgslinjen. Hvis den bekræftede afsendelsesdato ikke er angivet, bruges den ønskede afsendelsesdato. |
| Leveringsperformance        | Forsendelser over tid                      | SalesLine CustPackingSlipOnTimeStatus | Ordrer, der er fuldt leveret, hvor hele antallet for salgslinjen er afsendt, plus tidlig, til tiden og for sent (se beskrivelserne tidligere i denne tabel). |
| Leveringsperformance        | Sendt for sent efter by                     | CustPackingSlipOnTimeStatus           | For sent (se beskrivelserne tidligere i denne tabel). |
| Leveringsperformance        | Afsendt efter biprodukt                       | CustPackingSlipOnTimeStatus           | Tidligt, til tiden og for sent (se beskrivelserne tidligere i denne tabel). |
| Leveringsperformance        | Afsendt efter kunder                      | CustPackingSlipOnTimeStatus           | Tidligt, til tiden og for sent (se beskrivelserne tidligere i denne tabel). |
| Leveringsperformance        | Afsendt pr. websted/lagersted              | CustPackingSlipOnTimeStatus           | Tidligt, til tiden og for sent (se beskrivelserne tidligere i denne tabel). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]