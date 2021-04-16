---
title: Dato- og omkostningsstyring
description: I dette emne beskrives omkostnings- og datostyring i Styring af aktiver.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d6f0a155b38b1d732d17bd2f964677862ff363e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808658"
---
# <a name="cost-and-date-control"></a>Dato- og omkostningsstyring

[!include [banner](../../includes/banner.md)]

 

I Styring af aktiver kan du beregne omkostninger for at få et overblik over de faktiske omkostninger i forhold til budgetterede omkostninger på aktiver, arbejdssteder og arbejdsordrer. De faktiske omkostninger er baseret på bogførte transaktioner. 

Du kan også foretage en datoberegning, hvis du vil sammenligne planlagte start- og slutdatoer med faktiske start- og slutdatoer på arbejdsordrer.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Omkostningsstyring for aktiver, arbejdssteder og arbejdsordrer

De beregninger, der foretages for aktiver, arbejdssteder og arbejdsordrer, er næsten identiske. Den eneste forskel er, at for aktiver og arbejdssteder kan du også medtage underaktiver og underordnede arbejdssteder i beregningen. Datoen er den transaktionsdato, da registreringen blev foretaget.

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Omkostningsstyring for aktiv** eller **Omkostningsstyring for arbejdssted** eller **Styring af aktiver** > **Forespørgsler** > **Arbejdsordrer** > **Omkostningsstyring for arbejdsordre**.

2. Vælg et tidsinterval, der skal beregnes, i **Omkostningsstyring for aktiv** / **Omkostningsstyring for arbejdssted** / **Omkostningsstyring for arbejdsordre**.

3. Hvis det er nødvendigt, skal du vælge en økonomisk dimensionsopsætning, der skal medtages i beregningen.

4. Vælg "Ja" på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater med en omkostning på nul.

5. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede omkostningsstyringslinjerne skal være i forbindelse med arbejdssteder. 

    Hvis du f.eks. indsætter tallet "1" i feltet, og du har et arbejdsstedshierarki med flere niveauer, vises alle omkostningsstyringslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. 
    
    Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle omkostningsstyringslinjer på alle de arbejdsstedsniveauer, de er relateret til.

6. Vælg "Ja" på knappen **Vis åben bindende omkostning**, hvis du vil medtage denne kolonne i beregningen.

7. Vælg "Ja" i til/fra-knappen **Medtag underaktiver** for at få vist omkostninger, der er relateret til underaktiver som separate linjer.

8. Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver / arbejdssteder / arbejdsordrer i oversigtspanelet **Poster, der skal indgå**.

9. Klik på **OK** for at starte beregningen.

    I figuren herunder vises et eksempel på dialogboksen **Omkostningsstyring for aktiv**.

    ![Dialogboksen Omkostningsstyring for aktiv](media/01-controlling-and-reporting.png)

10. Klik på **Sammenlæg pr.**-knapperne på siden **Omkostningsstyring for aktiv** for at få vist det nødvendige detaljeringsniveau i beregningen. De valgte **Sammenlæg pr.**-knapper er fremhævet. Klik på en knap for at aktivere eller deaktivere den.

## <a name="example"></a>Eksempel

I skærmbilledet herunder vises et eksempel på beregningsresultater i **Omkostningsstyring for aktiv**.

- I feltet **Oprindeligt budget** vises budgetomkostninger fra arbejdsordrebudgettet. 
- Feltet **Bindende omkostning** viser det samlede udgiftsbeløb, som en juridisk enhed har bundet sig til at betale. 
- Feltet **Åben bindende omkostning** viser forpligtelser til at betale for varer, timer og tjenester, du har bestilt eller modtaget, men endnu ikke betalt for. 
- Når alle forbrugsregistreringer er bogført, vises de tilknyttede omkostninger i feltet **Faktiske omkostninger**.

![Eksempel på beregningsresultater i Omkostningsstyring for aktiv](media/02-controlling-and-reporting.png)

Du kan også foretage en omkostningsberegning ved at vælge flere aktiver i **Alle aktiver** eller **Aktive aktiver**. Derefter skal du klikke på knappen **Omkostningsstyring** under fanen **Generelt**. I dialogboksen **Omkostningsstyring for aktiv** indsættes de valgte aktiver automatisk i feltet **Aktiv** i oversigtspanelet **Poster, der skal indgå**. Klik på **OK**, så der vises en omkostningsberegning for de valgte aktiver. Den samme procedure kan udføres for arbejdssteder i **Alle arbejdssteder** eller **Aktive arbejdssteder** og for arbejdsordrer i **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.


## <a name="work-order-date-control"></a>Datokontrol af arbejdsordre

Brug denne side til at få en oversigt over forventede start- og slutdatoer sammenlignet med faktiske start- og slutdatoer på arbejdsordrer.

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Arbejdsordrer** > **Datostyring af arbejdsordre**.

2. Klik på **Beregn**.

3. I feltet **Arbejdssted** skal du vælge et arbejdssted.

4. Indsæt det interval, du vil foretage beregningen for, i felterne **Fra-dato** og **Til-dato**. Alle de arbejdsordrer, der har forventet startdato i intervallet, vil blive medtaget.

5. Klik på **OK**.

6. Klik på **Sammenlæg pr.**-knapper for at få vist det nødvendige detaljeringsniveau i beregningen. De valgte **Sammenlæg pr.**-knapper er fremhævet. Klik på en knap for at aktivere eller deaktivere den.

## <a name="example"></a>Eksempel

I skærmbilledet herunder vises et eksempel på beregningsresultater i **Datostyring af arbejdsordre**.

- Feltet **Gns. startforsinkelse** viser forskellen i dage mellem den planlagte startdato for en arbejdsordre sammenlignet med den faktiske startdato. Hvis den faktiske startdato f.eks. er to dage før den planlagte startdato, vises "-2" i dette felt.  
- Feltet **Gns. slutforsinkelse** viser forskellen i dage mellem den planlagte slutdato for en arbejdsordre sammenlignet med den faktiske slutdato. Hvis den faktiske slutdato f.eks. er tre dage efter den planlagte slutdato, vises "3" i dette felt.  
- Felterne **Forekomster** viser antallet af gange, som afvigelser forekommer vedrørende planlagt og faktisk startdato samt planlagt og faktisk slutdato for arbejdsordren.

![Eksempel på beregningsresultater i Datostyring af arbejdsordre](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]