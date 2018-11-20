---
title: "Hvad er nyt eller ændret i Dynamics 365 for Talent Core HR (16. oktober 2018)"
description: "Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 2eb46f436305a4c81ea99553e4dc07288ee74008
ms.openlocfilehash: 7da597a682006cddb44ff9354813b07c15c1a449
ms.contentlocale: da-dk
ms.lasthandoff: 10/22/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a>Hvad er nyt eller ændret i Dynamics 365 for Talent Core HR (19. oktober 2018)

[!include[banner](includes/banner.md)]

**Build 8.1.1067**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.

## <a name="allow-managers-to-update-time-off-requests"></a>Tillade, at ledere kan opdatere anmodninger om fridage

Medarbejderens anmodninger fridage skal muligvis opdateres, når de er godkendt via arbejdsgangen. I mange tilfælde udfører lederen selv disse opdateringer på medarbejderens vegne. Denne nye funktion giver lederne muligheden for at opdatere planlagte fridage eller annullere anmodninger om fridage på vegne af deres medarbejdere. Denne funktion styres af parameteren **Arbejde på vegne af**, der kan angives på siden **Parametre for personale**. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>Tillade, at HR kan opdatere anmodninger om fridage

I lighed med funktionen ovenfor skal medarbejderes anmodninger om fridage muligvis opdateres af personale, når de tidligere er blevet godkendt via arbejdsgangen. Denne funktion gør det muligt for personale at opdatere anmodninger om fridage. Funktionen aktiveres i arbejdsområdet **Personer** og på siden **Arbejder** ved hjælp af en ny indstilling, **Vis fridag**. HR-brugere kan på disse sider få vist anmodninger og opdatere fridagstransaktioner svarende til, hvordan administratorer kan udføre disse handlinger.

Den sikkerhedsprogramadgangsrettighed, som styrer adgangen til denne funktion, er:
- Programadgangsrettighed: Vedligehold arbejderspecifikke orlovs- og fraværsprocesser.
- Rettighed: Vedligehold anmodninger om orlov og fravær for alle arbejdere.

## <a name="other-changes"></a>Andre ændringer
Der er foretaget følgende opdateringer i denne version:
- Ændringer af ansættelseshandlinger for arbejdere, så de er ikke længere "hænger fast" i tilstanden **Arbejdsgang er fuldført**.
- Ansættelsesposter kan nu oprettes uden en startdato for ansættelse.
- Registreringsdatoen i Dynamics 365 Talent for et kursus, der vises i medarbejderselvbetjeningsportalen, anvender nu tidszoneforskydning for datoen.
- Excel-filer kan importeres flere gange uden fejl ved hjælp af **medarbejderenhed**.

## <a name="known-issue"></a>Kendt problem

- **Problem**: Når du føjer en ny vedhæftet fil til en arbejder, bliver knapperne **Ny** og **Rediger** nedtonet. 
- **Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukket. Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil knapperne for vedhæftede filer blive aktiveret. (Dette problem vil blive løst i den næste platformsopdatering).

