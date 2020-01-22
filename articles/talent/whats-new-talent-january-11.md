---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (11. januar 2019)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899168"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent - Core HR (11. januar 2019)

**Build 8.1.2100**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.

## <a name="changes"></a>Ændringer

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Validere fraværsanmodninger ved at budgettere disponibel balance
Ændringer i denne version gør det muligt for medarbejdere at bede om fremtidig orlov uden at trække fra deres aktuelle saldo. Standardarbejdsprocesser bruges til alle fremtidige anmodninger. Du kan få flere oplysninger ved at læse [Periodisering af fravær baseret på antal arbejdstimer](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Se budgetteret orlovssaldo i ESS og Personer
Med denne funktion kan personale, ledere og medarbejdere få vist saldi for fremtidige orlovsperioder. Medarbejdere kan få vist fremtidige saldi i arbejdsområdet **Employee Self-Service**, og HR har adgang til de samme oplysninger ved hjælp af arbejdsområdet **Personer**.

### <a name="notifications-for-changing-leave-balances"></a>Beskeder om ændring af orlovssaldi
Orlovssaldi viser den aktuelle saldo for medarbejdere. Fremtidige saldi kan ses i arbejdsområderne **Employee Self-Service** og **Personer** ved at angive en "pr. dato" til beregning af den budgetterede balance.

Navigation til visning af budgetterede saldi er blevet tilføjet i følgende områder:
  - **Fridage**-kort i arbejdsområdet **Employee Self-Service**.
  - **Orlov og fravær**-kort i arbejdsområdet **Chefselvbetjening**.
  - **Orlov og fravær**-siden i arbejdsområdet **Personer**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Tillade decimaler i planer for variabel kompensation (kontantplaner)
Variable kontantbonusser og -planer har nu den ekstra fleksibilitet for beløb og tilsidesættelser for værdier med decimale beløb.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Datoerne i Tilmelding til variabel kompensation, kan ikke ændres, når planen er gemt.
Denne ændring giver mulighed for at opdatere slutdatoen for planen kan (udvidet eller udløbet), når planen er blevet gemt. Du kan stadig aktivere eller deaktivere planer, uafhængigt af start- og slutdatoer.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Lønoplysninger, der er tilgængelige for den, der er tildelt sikkerhedsrollen lønadministrator
Rollen Lønadministrator er blevet opdateret, så der er adgang til lønoplysninger under anmodningsprocessen.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Medarbejderselvbetjening | Stillingshierarki-detailudledning fra felt kan ikke hente overordnet node
Der er foretaget ændringer for at fjerne en fejl, der opstår, når du tilføjer stillingshierarkiet til nye arbejdsområder og navigerer i organisationsstrukturen.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Ny valideringsmeddelelse, når personalenummerserie er i brug
Der er foretaget en ændring for at præcisere, hvad problemet er, når du ansætter en medarbejder, og det næste personalenummer er i brug.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Arbejdsområdet til medarbejderselvbetjening valgt som startside
Når arbejdsområdet **Medarbejderselvbetjening** indledningsvis vælges som startside for en bruger, og brugeren ikke er tildelt medarbejderrollen, omdirigerer systemet til standarddashboardet.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Årsagskode for fratrædelse opdaterer stillingstildelingspost
Årsagskoden for fratrædelse opdaterer nu stillingstildelingen, når du afskediger en medarbejder og afslutter stillingen. 
