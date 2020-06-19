---
title: Rapporteringsindstillinger
description: I denne artikel emne beskrives det, hvordan du løser problemet, når en kunde ønsker at tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431009"
---
# <a name="reporting-options"></a>Rapporteringsindstillinger

**Miljøoplysninger**

Dette problem gælder for alle miljøer.

**Symptom**

Kunden vil gerne tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.

**Afgang**

Brugeren kan ikke tilpasse de integrerede Microsoft Power BI-rapporter.

**Løsning**

- Personale-data, der sendes til Common Data Service, kan indrapporteres via Power Apps Common Data Service-connector til Power BI Desktop. Bemærk, at Common Data Service indeholder et undersæt af Personale-data. Du kan finde flere oplysninger om Power BI og dashboards under [Oprette Power BI-rapporter og dashboards med Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Personale. Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.
- Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Personale leverer via Microsoft Office-integration.

**Langsigtet løsning**

Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Common Data Service.
