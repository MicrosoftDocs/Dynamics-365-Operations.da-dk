---
title: Foretage fejlfinding af lagerstedsarbejde
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsarbejde i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3015ec777953cedb5a5d8eea873ed1043cac04cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970225"
---
# <a name="troubleshoot-warehouse-work"></a>Foretage fejlfinding af lagerstedsarbejde

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsarbejde i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Jeg kan ikke flytte id'er, der har serienummervarer, når blank afgang og blank tilgang er tilladt i sporingsdimensionsgruppen.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke flytte et id ved at bruge menupunktet **Bevægelse**, hvis serienummeret har indstillingen *Blank afgang tilladt* og *Blank tilgang tilladt* i sporingsdimensionsgruppen, og hvis der er flere id'er på samme lokation, hvoraf nogle har serienumre og nogle ikke har dem.

### <a name="issue-resolution"></a>Problemløsning

Dette problem løses af de ændringer, der implementeres i [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Disse ændringer gør feltet **Serienummer** valgfrit, når blank tilgang og blank afgang er tilladt.

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Jeg modtager følgende fejlmeddelelse i lagerstedsappen, når jeg behandler bevægelser: "Lagerejeren %1 er ikke tilladt i denne proces".

### <a name="issue-description"></a>Problembeskrivelse

Sporingsdimensionen **Ejer** mangler, når lagerstedsappen bruges til at foretage bevægelser. En almindelig lageroverførselskladde fra Supply Chain Management-klienten ser ud til at fungere efter hensigten og kan kun bogføres, hvis dimensionen **Ejer** er udfyldt.

### <a name="issue-resolution"></a>Problemløsning

Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. I øjeblikket understøtter lagerstyringsprocesser kun det lager, der ejes af den juridiske enhed.
