---
title: "Systemdefinerede og brugerdefinerede tabelbegrænsninger"
description: "I denne artikel forklares de to typer tabelbegrænsninger for komponenter i en produktkonfigurationsmodel – brugerdefineret og systemdefineret. Tabelbegrænsninger repræsenterer matrixer af tilladte attributkombinationer, hvor hver række definerer et sæt mulige attributværdier."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b1d70a446bb4255375a36393778fe2ee6d6fa4e
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="system-defined-and-user-defined-table-constraints"></a>Systemdefinerede og brugerdefinerede tabelbegrænsninger

[!include[banner](../includes/banner.md)]


I denne artikel forklares de to typer tabelbegrænsninger for komponenter i en produktkonfigurationsmodel – brugerdefineret og systemdefineret. Tabelbegrænsninger repræsenterer matrixer af tilladte attributkombinationer, hvor hver række definerer et sæt mulige attributværdier.

Tabelbegrænsninger repræsenterer matrixer af kombinationerne af attributter, der er tilladt for komponenter i en produktkonfigurationsmodel. Hver række i tabellen definerer et sæt mulige værdier. Der findes to typer begrænsninger i en produktkonfigurationsmodel:

-   **Udtryksbegrænsning** – Opret et udtryk, der definerer forbindelser mellem attributter for at sikre, at der kun kan vælges kompatible værdier under produktkonfiguration.
-   **Tabelbegrænsning** – Opret en tabel, der definerer alle de kombinationer, der er tilladt for et bestemt sæt attributter. Der findes to typer tabelbegrænsninger: brugerdefinerede tabelbegrænsninger og systemdefinerede tabelbegrænsninger.

I denne artikel beskrives brugerdefinerede og systemdefinerede tabelbegrænsninger for komponenter i en produktkonfigurationsmodel.

## <a name="user-defined-table-constraints"></a>Brugerdefinerede tabelbegrænsninger
En begrænsning for en brugerdefineret tabel er en matrixtype, der kan bruges til at beskrive kombinationer af de attributværdier, der er defineret af attributtyper. Hvis du f.eks. producerer højttalere, kan du medtage kolonner til kabinetfinish og frontgitter i den brugerdefinerede tabelbegrænsning. Attributtypen for kabinetfinish har fire værdier, og attributtypen for frontgitter har tre værdier. Så hvis der ikke bruges betingelser, er der 4 × 3 = 12 mulige kombinationer. Men i dette eksempel er kun seks tilladte kombinationer, som vist i følgende tabel. Disse oplysninger vises under fanen **Tilladte kombinationer** på siden **Rediger tabelbegrænsning**.

| Kabinetfinish | Frontgitter |
|----------------|-------------|
| Sort          | Sort       |
| Sort          | Metal       |
| Egetræ            | Sort       |
| Rosentræ       | Hvid       |
| Hvid          | Sort       |
| Hvid          | Hvid       |

Brugerdefinerede tabelbegrænsninger defineres af statisk tabelinput, der fungerer på samme måde som en udtryksbegrænsning. Når du bruger en brugerdefineret tabelbegrænsning, er fordelen, at det ofte er nemmere at oprette tabellerne, og de er nemmere at forstå og vedligeholde end lange udtryksbegrænsninger.

## <a name="system-defined-table-constraints"></a>Systemdefinerede tabelbegrænsninger
En systemdefineret tabelbegrænsning opretter en dynamisk tilknytning mellem en attributtype og et felt i en tabel. Når en systemdefineret tabelbegrænsning medtages i en produktkonfigurationsmodel, sikrer tilknytningen, at dataene i tabellen vises i stedet for værdierne for attributtypen. Resultatet er en dynamisk begrænsning, fordi tabellens indhold kan ændres, f.eks. af andre moduler.  

Når du opretter en systemdefineret tabelbegrænsning, skal du vælge en tabel, eventuelt definere den forespørgsel, der skal bruges, og derefter knytte attributtyper til felterne i den valgte tabel. Felttyperne svar svare til attributtyperne.  

Før en tabelbegrænsning kan træde i kraft på en model til produktkonfiguration, skal tabelbegrænsningen medtages i en begrænsning på en af modellens komponenter. Fremgangsmåden er at oprette en ny begrænsning, vælge typen af tabelbegrænsning og derefter vælge den tabelbegrænsningsdefinition, der skal bruges. Endelig skal alle felter i tabelbegrænsningen knyttes til attributterne i produktkonfigurationsmodellen.

<a name="see-also"></a>Se også
--------

[Nøglebegreber i produktkonfigurationsmodeller](product-configuration-models.md)




