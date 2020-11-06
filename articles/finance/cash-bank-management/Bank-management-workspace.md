---
title: Arbejdsområde for bankstyring
description: Dette emne indeholder oplysninger om arbejdsområdet Bankstyring. Dette arbejdsområde viser oplysninger, der er relateret til et firmas bankkonti og indeholder en oversigtsvisning og en analyseside. Oversigtsvisningen indeholder oversigtsfelter, bankkontooplysninger, et saldodiagram og relaterede oplysninger. Analysesiden bruger funktionerne i Microsoft Power BI til at vise grafik, der vedrører bankkontosaldi.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4b7d2da346880278f684a796f2d649e7da52b647
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097180"
---
# <a name="bank-management-workspace"></a>Arbejdsområde for bankstyring

[!include [banner](../includes/banner.md)]

Arbejdsområdet **Bankstyring** viser oplysninger, der er relateret til firmaets bankkonti. Arbejdsområdet indeholder en **Oversigt** -visning og siden **Analyser**. **Oversigt** -visningen indeholder oversigtsfelter, bankkontooplysninger, et saldodiagram og relaterede oplysninger. **Analyse** -siden bruger funktionerne i Microsoft Power BI til at vise grafik, der vedrører bankkontosaldi.

## <a name="summary-view"></a>Oversigtsvisning

### <a name="summary"></a>Resume

Felterne i afsnittet **Oversigt** giver et overblik over dine bankkonti og giver hurtig adgang til de sider, du oftest skal bruge. Bankafstemningsoplysningerne gælder kun for den avancerede bankkontoafstemningsfunktion. Der findes kun oplysninger for de bankkonti, hvor indstillingen **Avanceret bankafstemning** er sat til **Ja** på siden **Bankkonto**. Fra afsnittet **Oversigt** kan du importere elektroniske bankfiler for bankkonti på tværs af alle juridiske enheder.

### <a name="bank-accounts"></a>Bankkonti

De enkelte bankkonti i den juridiske enhed er repræsenteret af et kort i afsnittet **Bankkonti**. Den aktuelle saldo er vist, og du kan finde frem til de posteringer, der udgør saldobeløbet i denne oversigt. Med beløbet i **Mellemposteringer** kan du også finde frem til de posteringer, der udgør oversigtsbeløbet. Mellemposteringer er de ventende posteringer, der er bogført ved hjælp af mellemposteringsfunktioner, men endnu ikke er afstemt. Beløbet i **Afventende saldo** er den aktuelle saldo minus de mellemposterede eller ventende transaktioner.

Kortet viser også, hvornår bankkontoen sidst blev afstemt. Disse oplysninger vises kun, hvis Avanceret bankafstemning er aktiveret for bankkontoen.

### <a name="balance"></a>Restværdi

**Saldo** -diagrammet viser enten historiske saldooplysninger for den bankkonto, der er valgt i afsnittet **Bankkonti** , eller en oversigt over historiske saldooplysninger for alle bankkonti i den juridiske enhed. Disse oplysninger er tilgængelige for forskellige perioder: den aktuelle uge, den aktuelle måned, indeværende år, de sidste fem år og alle perioder (den fulde historik for bankkontoen). 

Hvis du får vist **Saldo** -diagrammet for en enkelt bankkonto, vises historiske saldi i bankkontoens valuta. Hvis du får vist diagrammet for alle bankkonti i den juridisk enhed, vises historiske saldi i regnskabsvalutaen.

Oplysninger om, hvornår dataene sidst blev opdateret, vises øverst i diagrammet. Du kan opdatere dataene efter behov.

### <a name="related-information"></a>Relaterede oplysninger

Fra afsnittet **Relaterede oplysninger** kan du åbne siden **Finanskladde** for at foretage bankoverførsler. Du kan også hurtigt åbne siderne **Bankposteringer** og **Mellemposteringer**.

## <a name="analytics-view"></a>Visningen Analyser

Siden **Analyser** giver vigtige oplysninger om bankkonti i det aktuelle firma. Siden indeholder følgende visualiseringer:

-   Den samlede banksaldo i systemvalutaen
-   Saldo pr. juridisk enhed
-   Dagens faktisk vs. budgetteret saldo i bankkontoens valuta
-   Saldo pr. bankkonto
-   Saldo pr. valuta

Du kan få vist bankanalyser på tværs af alle regnskaber fra arbejdsområdet **Oversigt over kontanter - alle firmaer**. Du kan finde flere oplysninger i [Power BI-indhold for oversigt over kontanter](Cash-Overview-Power-BI-content.md).
