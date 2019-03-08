---
title: Rapporteringsindstillinger i Talent
description: I dette emne beskrives, hvordan du løser problemet, når en kunde ønsker at tilpasse Microsoft Dynamics 365 for Talent-rapporter eller oprette nye rapporter.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303792"
---
# <a name="reporting-options-in-talent"></a>Rapporteringsindstillinger i Talent

[!include [banner](includes/banner.md)]

**Miljøoplysninger**

Dette problem gælder for alle miljøer.

**Symptom**

Kunden vil gerne tilpasse Microsoft Dynamics 365 for Talent-rapporter eller oprette nye rapporter.

**Afgang**

Brugeren kan ikke tilpasse de integrerede Microsoft Power BI-rapporter.

**Løsning**

- De Core HR-data, der strømmer til Common Data Service for Apps, kan rapporteres via PowerApps CDS-forbindelsen til Power BI Desktop. Bemærk, at Common Data Service for Apps indeholder et undersæt af Core HR-data. Du kan finde flere oplysninger om Power BIog dashboards i [Oprette Power BI-rapporter og dashboards med PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Talent. Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.
- Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Talent leverer via Microsoft Office-integration.

**Langsigtet løsning**

Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Common Data Service for Apps.
