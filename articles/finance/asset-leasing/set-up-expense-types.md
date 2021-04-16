---
title: Konfigurere udgiftstyper
description: Dette emne beskriver, hvordan du konfigurerer udgiftstyper i Aktivleasing.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b50f406c7411ff8ed990a312fde9c2fc0ba3c3db
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819692"
---
# <a name="set-up-expense-types"></a>Konfigurere udgiftstyper

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer udgiftstyper i Aktivleasing. Omkostninger, der ikke er repræsenteret af betalingsplanen, kaldes *udgiftsomkostninger*. Eksempler på disse omkostninger omfatter ejendomsskatter, omkostninger til fælles områdevedligeholdelse og forsikringsudgifter.

## <a name="add-an-administrative-expense-type"></a>Tilføje en administrativ udgiftstype

1. Gå til **Aktivleasing \> Konfiguration \> Udgiftstyper**.
2. Vælg **Ny**.
3. Angiv den nye udgiftstype og en beskrivelse i de relevante felter.

## <a name="assign-accounts-to-administrative-costs"></a>Tildele konti til administrative omkostninger

Derefter skal du knytte konti til udgiftstyperne. Disse konti debiteres, når posterne i udgiftsplanen bogføres. Modkontoen er angivet i **Betalingsplanlinjerne for udligningsomkostninger** på de enkelte leasingaftaler.

1. Gå til **Aktivleasing \> Opsætning \> Parametre til aktivleasing**.
2. Vælg udgiftstypen i feltet **Konti** i **Udligningsomkostninger** i feltet **Udgiftstype**.
3. Vælg **Tilføj**.
4. I feltet **Kartotekstype** skal du vælge den type, der skal knyttes til de administrative omkostninger.

    > [!NOTE]
    > Flere forskellige kartotekstyper kan knyttes til samme udgiftskonto.

5. I feltet **Kontokode** skal du angive, hvilke rettigheder kartoteket skal udlignes med:

    - **Alle** – Tildel kartoteket til alle leasingaftaler.
    - **Gruppe** – Tildel kartoteket til en bestemt leasinggruppe.
    - **Tabel** – Tildel kartoteket til specifikke leasingaftaler.

6. Hvis du har valgt **Gruppe** eller **Tabel** i feltet **Kontokode**, skal du vælge et kontonummer eller gruppenummer i feltet **Konto-/gruppenummer**.
7. I felterne skal du vælge hovedkontoen for finanskonto og hovedkonto for driftsleasingaftalen.

Når du har gennemført disse trin, kan du tilføje udgifter via linjerne **Betalingsplan for udførelsesomkostninger** på siden **leasingaftaledetaljer** for den valgte leasingaftale. Du kan også tilføje udgifter, når du opretter en ny leasingaftale.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]