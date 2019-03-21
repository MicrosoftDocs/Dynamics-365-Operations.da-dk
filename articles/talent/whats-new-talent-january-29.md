---
title: Nyheder eller ændringer i Dynamics 365 for Talent (31. januar 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ab43bab53afd979d64099425f0582f6c1bb5a8b0
ms.sourcegitcommit: 383a344deb5abf48584ea2ee7774b8dbbbec49b3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/08/2019
ms.locfileid: "377844"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (31. januar 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 for Talent.

**Build 8.1.2128**

## <a name="core-hr-changes"></a>Ændringer af Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Fridage, der er brugt på orlovskort, tager ikke datoer i orlovsplan i betragtning
For de medarbejdere, der har orlovsplaner, der ikke følger et kalenderår, viser kortet **Taget** nu fridage, der er anvendt i det orlovsår, der er defineret i planen. Hvis en organisations orlovsår f.eks. går fra 1. juni til 30. maj, og en medarbejder har taget 3 dage i december, viser kortet **Taget** 3 dage den 15. januar. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Periodiserede beløb, der ikke svarer til datogrundlaget for niveauet
Der er føjet nye indstillinger til orlov og fravær (**Personale** parametre) for at gøre det muligt for kunder at bestemme, hvornår medarbejdernes dato for Måneders tjeneste er gældende. Datoen er slutningen af måneden for visse organisationer, men for andre kan det være starten af den efterfølgende måned. F.eks. kan én organisation bevilge fridage fra d. 31. december, mens en anden gør det fra den 1. januar. Med denne indstilling kan du vælge, hvornår bevillingen skal ske. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Arbejderansættelseshandlinger går i stå i "Arbejdsgang er fuldført"-tilstand
Der er foretaget ændringer til løsningen af et problem, hvor et lille antal arbejdsgange sluttede med statussen "Arbejdsgang er fuldført". Nye arbejdsgange skal nu flyttes til tilstanden "Fuldført", når arbejdsgangen er fuldført. Arbejdsgange i en Arbejdsgang afsluttet-status, overflyttes til en fejlstatus for at tillade opdatering eller fjernelse, hvis det er nødvendigt. 
