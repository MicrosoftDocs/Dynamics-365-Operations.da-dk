---
title: Arbejdsområde for kreditorbetalinger
description: Denne artikel indeholder oplysninger om arbejdsområdet Kreditorbetalinger. Arbejdsområdet Kreditorbetalinger viser oplysninger, der vedrører behandling af kreditorbetalinger.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6463e25fdcbc77dacc286460f3acd30ccc3d6e86
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847025"
---
# <a name="vendor-payments-workspace"></a>Arbejdsområde for kreditorbetalinger

[!include [banner](../includes/banner.md)]

Arbejdsområdet **Kreditorbetalinger** viser oplysninger, der vedrører behandling af kreditorbetalinger. Arbejdsområdet indeholder en **Mit arbejde**-visning og siden **Analyser**. Visningen **Mit arbejde** viser oversigtsfelter, gitre til kreditorpostering og relaterede kreditoroplysninger. Siden **Analyser** bruger funktionerne i Microsoft Power BI til at vise grafik, der vedrører kreditorbetalinger.

## <a name="setup-needed-to-view-power-bi-content"></a>Opsætning, der kræves for at se Power BI-indhold

Følgende konfiguration skal være fuldført for de data, der skal vises i visuelle elementer for **Kreditorbetalinger** Power BI.
1. Gå til **Systemadministration > Konfiguration > systemparametre** for at angive **Systemvaluta** og **Systemvalutakurs**.
2. Gå til **Finans > Kalendere > Regnskabskalendere** for at validere regnskabskalenderdatoer, der er tildelt den aktive tidsperiode.
3. Gå til **Finans > Opsætning > Finans** for at angive **Regnskabsvaluta** og **Valutakurstype**. 
4. Definer valutakurser mellem transaktionsvalutaer og regnskabsvaluta, regnskabsvaluta og systemvaluta. Det gør du ved at gå til **Finans > Valutaer > Valutakurser**.
5. Gå til **Systemadministration > Konfiguration > Enhedslager** for at opdatere den samlede måling af **VendPaymentBIMeasureV2**.

## <a name="my-work-view"></a>Visningen Mit arbejde

### <a name="summary-tiles"></a>Oversigt over felter

Felterne i sektionen **Oversigt** giver et overblik over status for dine betalingsoplysninger. Du kan se betalingskladder, der endnu ikke er bogført, forfaldne fakturaer, alle kreditorer og kreditorer, der er på hold. Fra sektionen **Oversigt** kan du oprette en ny kørsel af betaling.

Oplysningerne i sektionen **Oversigt** er for det firma, du er logget på.

### <a name="vendor-transactions-grids"></a>Gitre for kreditorposteringer

Sektionen **Kreditorposteringer** indeholder gitre, der viser de fakturaer, der er forfaldne, og betalinger, der ikke er udlignet. I **Forfaldne fakturaer**-gitteret kan du se udligningshistorikken for den valgte faktura. I **Betalinger ikke udlignet**-gitteret kan du se udligningshistorikken for den valgte faktura og udligne en faktura.

Centrale medarbejdere kan bruge et filter, der vises øverst på hvert gitter, til at vælge et firma. Gitteret filtreres derefter, så det kun viser de firmaer, der er defineret i det organisationshierarki til centraliserede betalinger, som den centrale medarbejder har rettigheder til at få vist.

Under fanen **Find transaktioner** i sektionen **Kreditorposteringer** kan du søge efter en kreditorpostering.

### <a name="related-information"></a>Relaterede oplysninger

Du kan få vist rapporten **Aldersfordelte kreditorer** og rapporten **Betalingsoversigt pr. dato** ved hjælp af links i sektionen **Relaterede oplysninger** i arbejdsområdet.

## <a name="analytics-page"></a>Siden Analyser

Siden **Analyser** indeholder vigtige metrikker f.eks. kreditorfakturaer, der er forfaldne, og kreditorfakturaer, der forfalder i fremtiden. Denne side indeholder ni rapportsider. En side indeholder en oversigt, og de andre otte sider indeholder oplysninger om kreditorbetalinger.

Følgende tabel viser de visualiseringer, der er tilgængelig på hver rapportside.


|            Rapportside            |                                                                                                                                                                                Visualisering                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Oversigt over kreditorbetalinger      | <ul><li>Forfaldne fakturaer</li><li>Fakturaer, der forfalder i dag</li><li>Rabatter, der er overført til mistede rabatter</li><li>Fakturaer med forfaldsdato i fremtiden efter kasserabatdato</li><li>Fakturaer med forfaldsdato i fremtiden efter forfaldsdato</li><li>Fakturaer betalt sent til fakturaer, der er betalt til tiden</li><li>Tildeling af arbejdsgang for betaling</li><li>Kreditor til debitor-saldo</li><li>Åbne fakturaer med betaling på hold</li></ul> |
|         Forfaldne fakturaer         |                                                                                             <ul><li>Forfaldne fakturaer</li><li>Detaljer om forfaldne fakturaer</li><li>Åbne fakturaer i alt</li><li>Forfaldne fakturaer pr. kreditorgruppe</li><li>Forfaldne fakturaer pr. firma</li></ul>                                                                                              |
|        Fakturaer, der forfalder i dag         |                                                                                                         <ul><li>Fakturaer, der forfalder i dag</li><li>Detaljer om fakturaer, der forfalder i dag</li><li>Fakturaer, der forfalder i dag, pr. firma</li><li>Fakturaer, der forfalder i dag pr. kreditorgruppe</li></ul>                                                                                                          |
| Rabatter, der er overført til mistede rabatter |                                                                             <ul><li>Rabatter, der er overført til mistet rabat</li><li>Detaljer om rabatter, der er overført til mistet rabat</li><li>Rabatter, der er overført til mistet rabat, pr. firma</li><li>Rabatter, der er overført til mistet rabat, pr. kreditorgruppe</li></ul>                                                                              |
|      Fakturaer med forfald i fremtiden       |                                                 <ul><li>Fakturaer med forfald i fremtiden</li><li>Detaljer om fakturaer med forfald i fremtiden</li><li>Fakturaer med forfald i fremtiden pr. firma</li><li>Fakturaer med forfald i fremtiden pr. kreditorgruppe</li><li>Fakturaer med forfaldsdato i fremtiden efter kasserabatdato</li><li>Fakturaer med forfaldsdato i fremtiden efter forfaldsdato</li></ul>                                                  |
|        For sent betalte fakturaer         |                                                         <ul><li>Fakturaer, der er betalt efter forfaldsdato</li><li>Detaljer om fakturaer, der er betalt efter forfaldsdato</li><li>Fakturaer, der er betalt efter forfaldsdato, pr. firma</li><li>Fakturaer, der er betalt efter forfaldsdato, pr. kreditorgruppe</li><li>Fakturaer betalt for sent versus fakturaer betalt til tiden</li></ul>                                                          |
|         Arbejdsgang for betaling          |                                                                                <ul><li>Arbejdsgangsforekomster for kreditorbetaling</li><li>Arbejdsgangsforekomster for kreditorbetaling pr. godkender</li><li>Arbejdsgangsforekomster for kreditorbetaling pr. firma</li><li>Gennemsnitligt antal dage i arbejdsgang pr. godkender</li></ul>                                                                                |
|    Kreditor til debitor-saldo     |                                                                                                                   <ul><li>Kreditor til debitor-saldo</li><li>Kreditor til debitor-saldo pr. firma</li><li>Detaljer om kreditor til debitor-saldo</li></ul>                                                                                                                    |
|    Fakturaer med betaling på hold     |                                                                                         <ul><li>Fakturaer med betaling på hold</li><li>Detaljer om fakturaer med betaling på hold</li><li>Fakturaer med betaling på hold pr. firma</li><li>Fakturaer med betaling på hold pr. kreditorgruppe</li></ul>                                                                                          |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]