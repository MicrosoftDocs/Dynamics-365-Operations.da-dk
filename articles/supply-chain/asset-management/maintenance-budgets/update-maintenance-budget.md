---
title: Opdatere vedligeholdelsesbudgetter
description: Dette emne forklarer, hvordan du opdaterer et vedligeholdelsesbudget i Styring af aktiver.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87c054cb96d56e40e35ee44142396f59d61395263ff41232423f6c7911478b0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724934"
---
# <a name="update-maintenance-budgets"></a>Opdatere vedligeholdelsesbudgetter

[!include [banner](../../includes/banner.md)]

 

Siden **Vedligeholdelsesbudgetlinjer** viser alle de budgetlinjer, der er oprettet for det budget, der er valgt på siden **Vedligeholdelsesbudgetter**. (Yderligere oplysninger finder du under [Oprette vedligeholdelsesbudgetter](create-maintenance-budget.md)). Du kan genberegne og regulere vedligeholdelsesbudgetlinjer, indtil vedligeholdelsesbudgettet er godkendt. Når budgetperioden er overskredet, og omkostningerne er bogført i Styring af aktiver, kan du også opdatere budgetlinjerne med faktiske omkostninger.

## <a name="recalculate-a-maintenance-budget"></a>Genberegne et vedligeholdelsesbudget

Du kan genberegne et vedligeholdelsesbudget på siden **Vedligeholdelsesbudgetlinjer**. Når du genberegner et vedligeholdelsesbudget, slettes de eksisterende budgetlinjer, og der udføres en ny beregning.

1. Vælg **Genberegn** på siden **Vedligeholdelsesbudgetlinjer**.
2. Foretag de nødvendige ændringer for den nye beregning i dialogboksen **Genberegn budget**, og vælg derefter **OK**.

Nye budgetlinjer oprettes ud fra de værdier, du angiver.

## <a name="adjust-budget-lines"></a>Justere budgetlinjer

I stedet for at genberegne hele vedligeholdelsesbudgettet kan du regulere udvalgte linjer, der er relateret til budgetomkostninger.

1. Vælg de linjer, som budgetomkostningerne skal opdateres for, på siden **Vedligeholdelsesbudgetlinjer**.
2. Vælg **Juster**.
3. Hvis du vil føje et beløb til de valgte linjer, skal du markere afkrydsningsfeltet **Tilføj omkostninger** og derefter angive værdien i feltet **Tilføj værdi**.
4. Hvis du vil gange budgetomkostningen på de valgte budgetlinjer med en faktor, skal du markere afkrydsningsfeltet **Multiplicer omkostninger** og angive faktoren i feltet **Multiplikationsværdi**.

    Hvis du f.eks. indtaster **1,2** i feltet **Multiplikationsværdi**, øger du budgetomkostningerne på de valgte linjer med 20 procent. Hvis du angiver **0,7**, reducerer du budgetomkostningerne på de valgte linjer med 30 procent.

5. Vælg **OK**.

De valgte budgetlinjer opdateres i henhold til de værdier, du angiver i trin 3 eller 4.

## <a name="update-actual-costs"></a>Opdatere faktiske omkostninger

Når datoerne på budgetlinjerne er overskredet, og faktiske omkostninger er bogført i Styring af aktiver, kan du opdatere vedligeholdelsesbudgettet med de faktiske omkostninger.

1. Vælg **Opdater omkostning** på siden **Vedligeholdelsesbudgetlinjer**.
2. Vælg **OK** i dialogboksen **Beregn faktiske omkostninger**.

Felterne for **Faktiske omkostninger** på budgetlinjerne opdateres, hvis de faktiske omkostninger er blevet bogført. Der kan genereres nye budgetlinjer, hvis der er oprettet nye aktivtyper, siden du oprettede budgettet, og om disse aktivtyper er blevet brugt på aktiver, der er oprettet arbejdsordrer for, og hvor der er blevet bogført relaterede omkostninger. Nye budgetlinjer viser kun faktiske omkostninger, da der ikke er beregnet budgetomkostninger for dem.

> [!NOTE]
> Hvis du vil have vist en oversigt over de faktiske omkostninger inddelt i forebyggende og korrigerende omkostninger og investeringsomkostninger, kan du foretage en beregning for den samme periode på siden **Omkostningsstyring for aktiv**. 

## <a name="manually-add-budget-lines"></a>Tilføje budgetlinjer manuelt

På siden **Vedligeholdelsesbudgetlinjer** kan du manuelt tilføje en ny budgetlinje ved at vælge **Ny** og derefter foretage valg på linjen. Her er nogle eksempler på situationer, hvor denne metode kan være nyttig:

- Du ved, at der i øjeblikket planlægges fornyelse af udstyr for nogle aktiver, men at der endnu ikke er oprettet relaterede job i Styring af aktiver. Du vil dog gerne have, at budgetomkostninger for disse job skal indgå i vedligeholdelsesbudgettet.
- Der er blevet oprettet nye aktiver eller aktivtyper, siden du lagde vedligeholdelsesbudgettet, men der er endnu ikke konfigureret vedligeholdelsesplaner for disse aktiver eller aktivtyper. Du vil dog gerne have, at budgetomkostninger for disse aktivtyper skal indgå i vedligeholdelsesbudgettet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]