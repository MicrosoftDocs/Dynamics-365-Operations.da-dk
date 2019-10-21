---
title: Nyheder eller ændringer i Dynamics 365 Talent (7. februar 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4005a8745e46a23fe16b94cab7b7aeb20f84035
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009756"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (7. februar 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="interview-scheduling-enhancements"></a>Forbedringer af samtaleplanlægning
Der er foretaget forbedringer af samtaleplanlægningen fra start til slut. Du kan nu se kalendertilgængeligheden for en intern kandidat og bruge den interne kandidats kalender til anbefalinger i tidsplanen. Yderligere oplysninger finder du i [Samtaleplanlægning og tilbagemelding](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Jobopslag på LinkedIn – problem med firmauoverensstemmelse er rettet
Et problem er løst, hvor job, der er opslået på LinkedIn fra Attract, blev vist under det forkerte firmanavn. Yderligere oplysninger finder du i [Oprette, godkende og opslå job i Attract](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>URL-adresse til karrierewebsted, der vises i administratorindstillinger
URL-adressen til startsiden for karrierewebsted vises nu i **Administratorindstillinger** under **Administration af karrierewebsted**.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

**Build 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Flere kompensationsniveauer understøttes for job
Denne ændring giver mulighed for, at der kan defineres mere end ét kompensationsniveau for et job og dermed for afgrænsning af medarbejderens faste løn, som kan variere mellem planer, når der bruges samme job. 

F.eks.:    
*Job* - Kontoadministrator *Tilknyttede kompensationsniveauer:* B1 og B2 - Hvert niveau har et defineret interval af værdier. B1 = Min 50.000, Mid 60.000, Maks 75.000 og B2 = Min 65.000, Mid 74.000, Maks 85.000. Ved oprettelse af fast løn for medarbejdere, der er baseret på de definerede berettigelsesregler, kan hver faste lønstruktur nu henvise til samme job og forskellige niveauer af jobbet. Dette giver mulighed for, at strukturer kan defineres i forskellige områder/firmaer og henvise til det samme job, men forskellige begrænsninger, uden at det er nødvendigt at duplikere job for at tage højde for disse forskelle.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Feltet Kompensationsniveau er føjet til enheden Fast løn til medarbejder 
Med denne opdatering er enheden Fast løn til medarbejder blevet opdateret, så den omfatter feltet **Kompensationsniveau**. Denne tilføjelse gør det nemmere at opdatere medarbejderens faste lønstrukturer. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Opdatere jobfamilie ved opdatering og oprettelse af nye stillinger
Når du ændrer jobbet i en stilling, får **Jobfamilie** nu standardindstillingen baseret på det job, der er valgt.

### <a name="performance-improvements-when-rendering-workspaces"></a>Forbedringer af ydeevnen ved gengivelse af arbejdsområder
Analysefaner i arbejdsområder indlæses nu kun ved adgang til disse sider. Der vises en indikator under den indledende gengivelse af siden i øverste venstre hjørne af siden.
