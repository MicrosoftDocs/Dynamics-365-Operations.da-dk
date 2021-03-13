---
title: Rapporteringsindstillinger
description: I denne artikel emne beskrives det, hvordan du løser problemet, når en kunde ønsker at tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111900"
---
# <a name="reporting-options"></a>Rapporteringsindstillinger

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Miljøoplysninger**

Dette problem gælder for alle miljøer.

**Symptom**

Kunden vil gerne tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.

**Afgang**

Brugeren kan ikke tilpasse de integrerede Microsoft Power BI-rapporter.

**Løsning**

- Human Resources-data, der sendes til Dataverse, kan indrapporteres via Power Apps Dataverse-connector til Power BI Desktop. Bemærk, at Dataverse indeholder et undersæt af Human Resources-data. Du kan finde flere oplysninger om Power BI og dashboards under [Oprette Power BI-rapporter og dashboards med Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Human Resources. Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.
- Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Human Resources leverer via Microsoft Office-integration.

**Langsigtet løsning**

Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Dataverse.
