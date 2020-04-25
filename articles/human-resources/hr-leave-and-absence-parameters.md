---
title: Konfigurere parametre for orlov og fravær
description: Definer personaleparametre for orlov og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb992cbfbed33f88e125d3a8b721f8815414599a
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197975"
---
# <a name="configure-leave-and-absence-parameters"></a>Konfigurere parametre for orlov og fravær

Før du opretter orlovs- og fraværsplaner i Dynamics 365 Human Resources, er det en god ide at kontrollere indstillingerne for alle relaterede personaleparametre, herunder:

- Nummerserie for orlovsanmodninger
- FMLA-indstillinger (Family Medical and Leave Act)
- Indstillinger for medarbejderselvbetjening for anmodninger om orlov og fravær
- Parametre for orlov og fravær

## <a name="view-and-change-human-resources-parameters"></a>Få vist og skift personaleparametre

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Personaleparametre** under **Konfiguration**.

3. Under fanen **Nummerserier** skal du kontrollere **Nummerseriekode** for **Orlovsanmodnings-id** og ændre den efter behov. Denne indstilling bestemmer den rækkefølge, der bruges til automatisk tildeling af id'er til orlovsanmodninger.

4. Under fanen **FMLA** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.

5. Under fanen **Medarbejderselvbetjening** skal du angive, om ledere kan angive orlovs- og fraværsanmodninger på vegne af deres medarbejdere.

6. Under fanen **Orlov og fravær** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.

7. Vælg **Gem**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Få vist og ændre parametre for orlov og fravær

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Parametre for orlov og fravær** under **Konfiguration**.

3. På fanen **Generelt** kan du angive følgende parametre:
 
    - Angiv **Enhed for orlov og fravær** til timer eller dage. Hvis du angiver dage, kan du vælge **Aktiver halv-dags definition**, så medarbejderne kan vælge første eller anden halvdel af dagen i deres anmodninger om fritid. 

    - Vælg **Ikrafttrædelsesdato for måneders tjeneste** for at indstille, hvornår periodiseringssatserne træder i kraft for orlovsplaner vha. måneders tjeneste.

    - Vælg **Saldoberegning** for at få vist saldi pr. dags dato eller pr. periodiseringsperiode. Hvis du vælger **Saldo pr. dags dato**, viser saldoen totalen for alle periodiseringer, justeringer og anmodninger pr. i dag. Hvis du vælger **Saldo pr. periodiseringsperiode**, viser saldoen totalen for alle periodiseringer, reguleringer og anmodninger pr. den periodiseringsperiode, der er defineret af frekvensen i orlovsplanen. 

## <a name="configure-calendar-parameters"></a>Konfigurere kalenderparametre

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Parametre for orlov og fravær** under **Konfiguration**.

3. Under fanen **Kalender** skal du ændre kalenderindstillingerne efter behov.

4. Vælg **Gem**.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
