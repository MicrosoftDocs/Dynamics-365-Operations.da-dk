---
title: Rapporteringsindstillinger i Talent
description: I dette emne beskrives, hvordan du løser problemet, når en kunde ønsker at tilpasse Microsoft Dynamics 365 for Talent-rapporter eller oprette nye rapporter.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e7348a515b08523c15aa8f74d5616a3daf645b7
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741792"
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

- De Core HR-data, der sendes til Common Data Service, kan indrapporteres via PowerApps' Common Data Service-connector til Power BI Desktop. Bemærk, at Common Data Service indeholder et undersæt af Core HR-data. Du kan finde flere oplysninger om Power BIog dashboards i [Oprette Power BI-rapporter og dashboards med PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Talent. Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.
- Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Talent leverer via Microsoft Office-integration.

**Langsigtet løsning**

Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Common Data Service.
