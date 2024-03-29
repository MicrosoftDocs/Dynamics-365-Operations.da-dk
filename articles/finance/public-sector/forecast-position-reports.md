---
title: Rapporter over budgetteret stilling for den offentlige sektor
description: Du kan bruge rapporten oversigten over budgetteret stilling og den detaljerede rapport over budgetteret stilling til at generere oplysninger om budgetterede stillinger under en budgetplan og det scenarie, du angiver.
author: velofog
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.search.industry: public sector
ms.author: twheeloc
ms.search.validFrom: 2019-8-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 128fa481940b21bbbc215cbff6086f5961d30ad4
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734349"
---
# <a name="forecast-position-reports-for-the-public-sector"></a>Rapporter over budgetteret stilling for den offentlige sektor

[!include [banner](../includes/banner.md)]

Du kan bruge rapporterne **Oversigt over budgetteret stilling** og **Detaljer for budgetteret stilling** til at generere oplysninger om budgetterede stillinger under en budgetplan og det scenarie, du angiver.  

Rapporten **Oversigt over budgetteret stilling** viser budgetterede stillingsomkostninger efter kontofordelinger. Omkostningerne til budgetterede stillinger vises grupperet efter deres tildelte kontofordelinger. Kostbeløbene omregnes med den procent, der er tildelt kontofordelingen. 

Rapporten **Detaljer for budgetteret stilling** indeholder de fleste oplysninger, der vises i formularen for budgetteret stilling. De kontofordelinger, der er tilknyttet budgetstillingen via økonomiske dimensioner og økonomiske dimensionsskabeloner, vises sammen med de omkostninger, der er knyttet til den enkelte fordelingskombination for den budgetterede stilling. 

Hvis du vil have vist flere oplysninger om en **Budgetteret stilling**, skal du vælge **stillingsnummeret** for at åbne siden **Budgetteret stilling**.

## <a name="filter-the-data-on-this-report"></a>Filtrere dataene i denne rapport

Når du opretter rapporten, vises følgende standardparametre.  Du kan bruge disse parametre til at filtrere de data, der vises i rapporten.  

| Felt | Beskrivelse |
| --------- | ------- |
| Budgetplansscenarie | Vælg det budgetplanscenarie, der skal vises i rapporten. <p> Budgetplanscenarier definerer kategorier af data for budgetplanerne. Du kan definere scenarier for budgetplaner for at understøtte monetære og andre måleenhedsklasser, f.eks. mængde. Eksempler på scenarier med monetære budgetplaner inkluderer Afdeling forrige år og Afdelingsforespørgsler. Eksempler på budgetplansscenarier, der bruger antal, omfatter forrige års supportopkald og antal fuldtidsækvivalenter. </p>  |
| Budgetplanlægningsproces | Vælg den budgetplanlægningsproces, der skal vises i rapporten.<p> Budgetplanlægningsprocesser bestemmer, hvordan budgetplaner kan opdateres, distribueres, gennemses og godkendes i organisationshierarkiet for budgettering. En budgetplanlægningsproces er knyttet til en budgetcyklus og en organisation via en juridisk enhed. </p> |
| Standardkontostruktur | Vælg standardkontostrukturen for visning af regnskabsdimensionerne på de budgetterede stillinger i den ønskede rækkefølge.|
| Afdeling | Vælg en afdeling, der skal vises i rapporten. Lad feltet være tomt for at køre rapporten for alle konti. |
| Kun ikke-udfyldte | Angiv denne indstilling til Ja for at udelade stillinger, der i øjeblikket er besat. |
| Undertryk total | Angiv denne indstilling til Ja for at udelade totaler i rapporten. |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
