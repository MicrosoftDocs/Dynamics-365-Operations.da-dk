---
title: Konfigurer en produktkonfigurationsmodel
description: I denne artikel beskrives trinnene til oprettelse og oprettelse af en produktkonfigurationsmodel.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 8504eb789b0d449cf2e29d4314d189dc0b8a6b43
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---

# <a name="set-up-a-product-configuration-model"></a>Konfigurer en produktkonfigurationsmodel

[!include [banner](../includes/banner.md)]

I denne artikel beskrives trinnene til oprettelse og oprettelse af en produktkonfigurationsmodel.

| Opgave                                                        | Betegnelse                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opret en produktmaster.                                    | Opret en produktmaster fra listen **Produktmaster**. Frigiv produktmasteren til alle relevante firmaer. For en produktmaster, der bruges som en version til en produktkonfigurationsmodel eller som en underkomponent, skal **begrænsningsbaseret konfiguration** vælges som konfigurationsteknologi, og konfigurationsdimensionen må kun vælges for produktdimensionsgruppen. |
| Opret komponenter.                                          | Opret komponenter på siden **Komponenter**. Komponenter er byggesten i en produktkonfigurationsmodel og kan genbruges i flere forskellige produktkonfigurationsmodeller.                                                                                                                                                                                                                      |
| Opret attributtyper.                                     | Opret attributtyper på siden **Attributtyper**. Attributtyper angiver det sæt datatyper til alle attributter, der bruges i produktkonfigurationsmodeller. Attributter af typen **Boolesk**, **Tekst** med en fast liste og **Heltal** med en række typer angiver det sæt værdier, der er tilgængelige, når du konfigurerer en produktvariant baseret på en produktkonfigurationsmodel.       |
| Opret en produktkonfigurationsmodel.                       | Opret en produktkonfigurationsmodel på siden **Ny model til produktkonfiguration**.                                                                                                                                                                                                                                                                                                              |
| Føj attributter til en produktkonfigurationsmodel.            | Opret en attribut på oversigtspanelet **Attributter** på siden **Detaljer om begrænsningsbaseret model til produktkonfiguration**. Attributter beskriver funktionerne i produktkonfigurationsmodellen.                                                                                                                                                                                                       |
| Føj begrænsninger til en produktkonfigurationsmodel.           | Opret begrænsninger på oversigtspanelet **Begrænsninger** på siden **Detaljer om begrænsningsbaseret model til produktkonfiguration**. Begrænsninger er betingelser, som skal opfyldes af en produktkonfiguration. Begrænsninger kan enten være udtryksbegrænsninger eller tabelbegrænsninger.                                                                                                                                 |
| Føj en underkomponenter til en produktkonfigurationsmodel.         | Opret underkomponenter på oversigtspanelet **Underkomponenter** på siden **Detaljer om begrænsningsbaseret model til produktkonfiguration**. Underkomponenter er relateret til komponenter, og de er knyttet til varer, der repræsenterer underkomponenten.                                                                                                                                                                       |
| Føj brugerkrav til en produktkonfigurationsmodel.     | Brugerkrav ligner underkomponenter, men de henviser ikke til et element. Du kan opfatte brugerkrav som en fantomstykliste. Alle styklistelinjer eller ruteoperationer, der er placeret direkte under brugerkravet, er skjult i den overordnede komponent.                                                                                                                       |
| Føj styklistelinjer til en produktkonfigurationsmodel.             | Opret styklistelinjer på oversigtspanelet **Styklistelinjer** på siden **Detaljer om begrænsningsbaseret model til produktkonfiguration**. Styklistelinjer repræsenterer en del, der kræves for at bygge en variant af produktet.                                                                                                                                                                                                 |
| Føj ruteoperationer til en produktkonfigurationsmodel.      | Opret ruteoperationer på oversigtspanelet **Ruteoperationer** på siden **Detaljer om begrænsningsbaseret model til produktkonfiguration**. Ruteoperationer repræsenterer et trin i en række trin, der udføres for at bygge en variant af produktet.                                                                                                                                                    |
| Opret en aktiv version for en produktkonfigurationsmodel. | Opret en aktiv version af produktkonfigurationsmodellen på siden **Versioner**. En version er relationen mellem en produktkonfigurationsmodel og en produktmaster. En produktkonfigurationsmodel, der har en aktiv version, kan være konfigureret fra en salgsordre, et salgstilbud, en produktionsordre eller en indkøbsordre.                                                               |
| Test en produktkonfigurationsmodel.                         | Test produktkonfigurationsmodellen enten fra siden **Detaljer om begrænsningsbaseret model til produktkonfiguration** eller fra siden **Liste over produktkonfigurationsmodeller**. Test af produktkonfigurationsmodeller simulerer produktmodelkonfigurationsprocessen, der finder sted under håndteringen af ordren.                                                                                                |
| Opret en skabelon til produktkonfigurationsmodeller.                | Opret en skabelon til produktkonfigurationsmodeller på siden **Konfigurationsskabeloner**. En konfigurationsskabelon indeholder værdier til attributter i produktkonfigurationsmodellen. Vælg attributværdier på siden **Konfigurer linje**. Du kan vælge at indlæse en skabelon til produktkonfigurationsmodeller under konfiguration af produktmodellen.                                                   |
| Konfigurer et element.                                          | Produktkonfigurationsmodeller kan konfigureres fra en salgsordre, et salgstilbud, en produktionsordre eller en indkøbsordre.                                                                                                                                                                                                                                                                           |






