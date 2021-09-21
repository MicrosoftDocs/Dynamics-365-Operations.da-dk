---
title: Du kan ikke finde dialogboksen til rullelisten "Arbejdsgang" for lagerkladder
description: Du kan ikke finde dialogboksen til rullelisten "Arbejdsgang" på kladdesiden, eller relaterede arbejdsgangshandlinger er ikke tilgængelige
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475886"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Du kan ikke finde dialogboksen til rullelisten "Arbejdsgang" for lagerkladder

## <a name="symptoms"></a>Symptomer

Du kan ikke finde dialogboksen til rullelisten **Arbejdsgang** på kladdesiden, eller relaterede arbejdsgangshandlinger er ikke tilgængelige.

Dette problem kan forekomme af tre årsager som beskrevet i følgende afsnit.

## <a name="resolution-1"></a>Løsning 1

Hvis problemet gælder for alle brugere, kan det være på grund af, at godkendelsesarbejdsgangen ikke er tildelt kladdenavnet. Følg disse trin for at løse dette problem.

1. Gå til **Lagerstyring &gt; Konfiguration &gt; Kladdenavne &gt; Lager**.
1. Vælg et kladdenavn i listeruden for at åbne indstillingerne.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Godkendelsesarbejdsgang** til *Ja*. Klik på **Ja**, hvis du bliver bedt om at bekræfte ændringen.
1. I feltet **Arbejdsgang** skal du vælge den arbejdsgang, du vil bruge til det valgte kladdenavn.

## <a name="resolution-2"></a>Løsning 2

Hvis arbejdsgangen bruger tilpasset kode, kan der opstå problemer, efter du har opgraderet systemet. I kladdearbejdsgangen kan knappen **Send** f.eks. være nedtonet, så du ikke kan vælge den for at godkende en afsendelse.

Hvis knappen **Send** er nedtonet, er arbejdsgangen måske blevet tilpasset, hvilket betyder, at metoden for arbejdsgangen `canSubmitToWorkflow()` i `FormDataUtil` er blevet udvidet. Du kan løse dette problem ved at ændre den måde, hvorpå du udvider metoden for `canSubmitToWorkflow()` til at bruge strukturen, i følgende eksempel.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Løsning 3

Hvis problemet kun gælder for nogle få bestemte brugere, har disse brugere muligvis ikke de sikkerhedsrettigheder, der er nødvendige for at køre arbejdsgangshandlinger i lagerkladder. Kontrollér, at hver påvirket bruger har sikkerhedsrettigheden *Vedligehold arbejdsgang for lagerkladder*. Denne rettighed er som standard tildelt en opgave med samme navn, og denne opgave anvendes til rollerne *Lagerarbejder* og *Lagerchef*.
