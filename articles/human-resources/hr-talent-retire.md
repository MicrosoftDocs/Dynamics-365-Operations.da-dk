---
title: Ophør af Dynamics 365 Talent - Attract og Onboard-apps
description: I dette emne beskrives ophøret af Dynamics 365 Talent – Attract og Onboard-apps.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: df33f35f66e356c3c2a99f0d81ebba1d0f34b5d9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069398"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Ophør af Dynamics 365 Talent: Attract og Onboard-apps


I december 2019 annoncerede vi ophøret af Dynamics 365 Talent – Attract og Onboard-apps den 1. februar 2022 , så kunderne fik to år til at planlægge.

Yderligere oplysninger om ophøret af disse apps finder du i:
 - [Ophør af Dynamics 365 Talent - Attract- og Dynamics 365 Talent: Onboard-apps](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Opbygge et mere vellykket personale med Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Vi vil fortsat understøtte Dynamics 365 Human Resources, som vil hjælpe vores kunder med at få den indsigt i arbejdsstyrken, der er nødvendig for at opbygge databaserede medarbejdererfaringer på tværs af flere områder, f.eks.:

- Kompensation
- Personalegoder
- Orlov og fravær
- Overholdelse af angivne standarder
- Payroll
- Tilbagemelding om ydeevne
- Uddannelse og certificering
- Selvbetjeningsprogrammer

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Ofte stillede spørgsmål om ophør af Dynamics 365 Talent-apps

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Hvad er brugeroplevelsen for både Dynamics 365 Talent - Attract og Onboard-apps fra 1. februar 2022?

Brugerne vil ikke kunne bruge programmerne og bliver omdirigeret til en ophørsside.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Kan kunder fortsætte med at eksportere data for både Dynamics 365 Talent - Attract and Onboard apps efter 1. februar 2022?
  
Nej, ophøret blev annonceret i december 2019, og de nødvendige eksportegenskaber blev leveret frem til 1. februar 2022. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Slettes kundens data med relation til både Dynamics 365 Talent - Attract og Onboard-apps i Dataverse efter 1. februar 2022?

Nej, enhederne i Dataverse forbliver i kundens Microsoft Dataverse-miljø selv efter ophør, medmindre løsningen Human Capital Management Talent slettes eller afinstalleres.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Jeg kender navnet på Talent-miljøet. Hvordan kan jeg se Attract og Onboard-data i Dataverse?

1.  Log på Power Apps: https://make.powerapps.com
2.  Vælg det miljø, hvor du vil have vist Attract og Onboard-data.
3.  Gå til **Dataverse > Tabeller**. 
4.  Skriv "msdyn_" i **Søg**. Hvis du får vist listen over tabeller, der starter med "msdyn_" + tabelnavne (eksempel: msdyn_candidate), har du fundet miljøet med Attract og Onboard-data.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Jeg kender ikke navnet på Talent-miljøet. Hvordan kan jeg finde miljøet, der indeholder dataene til programmerne Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard?

1)  Log på Power Platform Administration: https://admin.powerplatform.microsoft.com/
2)  Vælg **Miljøer**.
3)  Vælg et miljø, der skal evalueres.
4)  Vælg **Ressourcer > Dynamics 365-apps**.
5)  Hvis du kan se, at **HCM Talent**-løsningen er installeret, skulle der være gemt Attract- og Onboard-data i dette miljø. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> **HCM Talent**-løsningen bruges også i Dynamics 365 Human Resources.
