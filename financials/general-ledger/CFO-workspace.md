---
title: "Føje økonomiske dimensioner til arbejdsområdet Regnskabsdirektør"
description: "I dette emne forklares, hvordan du kan føje økonomiske dimensioner til arbejdsområdet Regnskabsdirektør, så de kan bruges til rapporter for finans- og budgetposteringer."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: da-dk
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Føje økonomiske dimensioner til arbejdsområdet Regnskabsdirektør

[!include[banner](../includes/banner.md)]

I dette emne forklares, hvordan du kan føje økonomiske dimensioner til arbejdsområdet Regnskabsdirektør (CFO), så de kan bruges til rapporter for finans- og budgetposteringer. Arbejdsområdet Regnskabsdirektør indeholder fanen **Oversigt** og fanen **Finansiel**. Rapporterne under disse to faner understøttes af to målpunkter: LedgerActivityMeasure og BudgetActivityMeasure. I opdateringen til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition fra juli 2017 er der en relation mellem disse to målpunkter og DimensionCombinationEntity-enheden. Derfor kan du vælge dimensioner.

1. I Finance and Operations skal du på siden **Enhedslager** opdatere målpunkterne **LedgerActivityMeasure** og **BudgetActivityMeasure**.
2. Åbn Application Explorer i Microsoft Visual Studio, og søg efter **LedgerCFO**.
3. Under **Resources** (Ressourcer) skal du åbne **LedgerCFOWorkspacePBIX**.
4. Når ressourcen åbnes i Microsoft Power BI Desktop, skal du vælge **Get Data** (Hent Data). Vælg **SQL Server-database**, og vælg derefter **Connect** (Forbind).
5. Angiv en navnet på serveren og **AxDW** som database. Vælg **DirectQuery**, og vælg derefter **OK**.
6. Søg efter og vælg **LedgerActivityMeasure\_DimensionCombination**, og vælg derefter **Indlæs**.

    > [!TIP]
    > I listen **Fields** (Felter) skal du omdøbe tabellen **Økonomiske dimensioner**, så den er nem at identificere.

7. Vælg **Administrer relationer**, og vælg derefter **Ny**.
8. Vælg i det første felt **Finansaktiviteter**, og vælg derefter **LedgerDimension**.
9. I det andet felt skal du vælge **LedgerActivityMeasure\_DimensionCombination** (eller **Financial dimensions** (Økonomiske dimensioner), hvis du omdøbte tabellen). Vælg hovedet **DimensionCombinationRECID**.
10. I feltet **Cardinality** (Kardinalitet) skal du vælge **Many to One** (Mange til en).
11. Vælg værdien **Single** (Enkelt) for **Cross filter direction** (Tværgående filterretning).
12. Vælg både **Aktivér denne relation** og **Antag referentiel integritet**, vælg **OK**, og vælg derefter **Luk**.

    [![Oprette en relation](./media/Create-relationship.png)](./media/Create-relationship.png)

13. I listen **Fields** (Felter) skal du nu kunne se tabellen og de tilgængelige økonomiske dimensioner. Træk de økonomiske dimensioner, du ønsker, til rapportniveaufilterne.
14. Gem ændringerne.
15. I applikationsobjekttræet (AOT) skal du højreklikke på projektet og derefter vælge **Synchronize** (Synkroniser).
16. Opbyg projektet, og åbn derefter programmet for at se resultaterne.

    [![Fuldført arbejdsområde](./media/workspace.png)](./media/workspace.png)

