---
title: Konfigurere parametre for orlov og fravær
description: Dette emne beskriver, hvordan du definerer personaleparametre for orlov og fravær i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79052c550783dee1ba4091ad10bde4d79d7b905e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690688"
---
# <a name="configure-leave-and-absence-parameters"></a>Konfigurere parametre for orlov og fravær

>[!Important]
>De funktioner, der nævnes i dette emne, er i øjeblikket tilgængelige for kunder med enkeltstående Dynamics 365 Human Resources. Nogle eller alle funktionerne vil være tilgængelige som en del af en fremtidig version af Finance-infrastrukturen efter Finance-frigivelse 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Før du opretter orlovs- og fraværsplaner i Dynamics 365 Human Resources, er det en god ide at kontrollere indstillingerne for alle relaterede **Personaleparametre**, herunder:

- Nummerserie for orlovsanmodninger
- FMLA-indstillinger (Family Medical and Leave Act)
- Indstillinger for medarbejderselvbetjening for anmodninger om orlov og fravær
- Parametre for orlov og fravær

## <a name="view-and-change-human-resources-parameters"></a>Få vist og skift personaleparametre

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Human Resourcesparametre** under **Konfiguration**.

3. Under fanen **Nummerserier** skal du kontrollere **Nummerseriekode** for **Orlovsanmodnings-id** og ændre den efter behov. Denne indstilling bestemmer den rækkefølge, der bruges til automatisk tildeling af id'er til orlovsanmodninger.

4. Under fanen **FMLA** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.

5. Under fanen **Medarbejderselvbetjening** skal du angive, om ledere kan angive orlovs- og fraværsanmodninger på vegne af deres medarbejdere.

7. Vælg **Gem**.

>[!IMPORTANT]
>Visning af orlov og fravær på tværs af firmaer er i øjeblikket i prøveversion. Du skal aktivere det i dit **Sandkasse**-miljøet for at få vist indstillingen for orlov og fravær. Du kan finde flere oplysninger om aktivering af prøveversionsfunktioner i [Administrere funktioner](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>Få vist og skift delte parametre for personale

1. Vælg fanen **Links** på siden **Personalestyring**.

2. Vælg **Delte parametre for personale** under **Konfiguration**.

3. Vælg **Ja** under fanen **Forhåndsadgang** i **Visning af orlov på tværs af firmaet**, hvis du vil have, at orlov skal vises på tværs af firmaet.

4. Vælg **Gem**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Få vist og ændre parametre for orlov og fravær

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Parametre for orlov og fravær** under **Konfiguration**.

3. På fanen **Generelt** kan du angive følgende parametre:
 
    - Angiv **Enhed for orlov og fravær** til timer eller dage. Hvis du angiver dage, kan du vælge **Aktiver halv-dags definition**, så medarbejderne kan vælge første eller anden halvdel af dagen i deres anmodninger om fritid. 

    - Vælg **Ikrafttrædelsesdato for måneders tjeneste** for at indstille, hvornår periodiseringssatserne træder i kraft for orlovsplaner vha. måneders tjeneste.

    - Vælg **Saldoberegning** for at få vist saldi pr. dags dato eller pr. periodiseringsperiode. Hvis du vælger **Saldo pr. dags dato**, viser saldoen totalen for alle periodiseringer, justeringer og anmodninger pr. i dag. Hvis du vælger **Saldo pr. periodiseringsperiode**, viser saldoen totalen for alle periodiseringer, reguleringer og anmodninger pr. den periodiseringsperiode, der er defineret af frekvensen i orlovsplanen. 

    - Angiv **Starttidspunkt** for batchjobbet **Udløb af overførsel**.  
    
    - Vælg **Ja** for **Tillad medarbejderne at købe orlov** og **Tillad medarbejderne at sælge orlov**. Hvis du vælger **Ja** for disse indstillinger, kan du oprette politikker for køb og salg af orlov og give medarbejdere mulighed for at sende anmodninger om køb og salg af orlov.

## <a name="configure-calendar-parameters"></a>Konfigurere kalenderparametre

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Parametre for orlov og fravær** under **Konfiguration**.

3. Under fanen **Kalender** skal du ændre kalenderindstillingerne efter behov.

4. Vælg **Gem**.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
