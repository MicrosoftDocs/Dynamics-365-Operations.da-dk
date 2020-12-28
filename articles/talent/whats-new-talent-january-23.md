---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (23. januar 2019)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f97462f088fc1a3cb94f2a34204fc09f1cd66fb0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460634"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent - Core HR (23. januar 2019)

**Build 8.1.2121**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.

## <a name="changes"></a>Ændringer

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>Import af fast løn for medarbejdere fungerer ikke, når du opretter nye poster for fast løn
Er der foretaget en ændring af den enhed for fast løn til medarbejdere, så kompensationsniveauet hentes ved import. Før denne version blev der vist en meddelelse, som angav, at niveauet var påkrævet.

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>Fjerne feltet med minimumsaldo fra dialogboksen til anmodning om fridag
Feltet **Mindste saldo** er blevet fjernet fra dialogboksen **Anmodning om fridage**. Denne ændring påvirker alle de områder, hvor der kan anmodes om fridage.

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>Dataopgradering for kompensationsniveauer, der ikke opdateres i alle scenarier
Er der foretaget en ændring, der opdaterer kompensationsniveauet i planer for fast løn. Denne ændring angiver en værdi for kompensationsniveauet i planer for faste løn for det job, der er tildelt til medarbejderen.

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>Lønoplysninger på siden Administrer ændringer er kun tilgængelige, når brugeren er logget på som systemadministrator.
Denne ændring giver medarbejdere med rollen Lønadministrator adgang til lønoplysninger på siden **Tidslinje for ændringer > Administrere ændringer** for stillingen.

### <a name="job-fields-default-to-positions"></a>Jobfelter får som standard værdien stillinger
Når jobbet ændres for en stilling, anvendes stillingsværdien for jobfelter som standard. Der vises en meddelelse med mulighed for at acceptere standardværdierne eller beholde de eksisterende værdier for disse felter.

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>Prøvetiden og kalenderen vises ikke for kommende medarbejdere.
Med denne ændring er felterne **Prøvetid** og **Kalender** blevet føjet til siden **Administrer ændringer**, så kommende og tidligere medarbejdere kan indtaste data.

### <a name="platform-update-23-for-finance-and-operations"></a>Platform update 23 til Finance and Operations
Rettelser af mindre programfejl er inkluderet som en del af platformsopdatering 23 til Finance and Operations. Du kan finde flere oplysninger i [Nyheder eller ændringer i Dynamics 365 Finance and Operations platformsopdatering 23 (januar 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23). 
