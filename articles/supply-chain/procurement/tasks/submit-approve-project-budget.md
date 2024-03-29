---
title: Opret og indsend et projektbudgetarbejdsproces
description: Denne procedure viser, hvordan du opretter og indsender et budget for et projekt.
author: GalynaFedorova
ms.date: 11/22/2021
ms.topic: article
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e554fb578371f52f665ef348d6fa81fd27196a9e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671022"
---
# <a name="create-and-submit-a-project-budget-workflow"></a>Opret og indsend et projektbudgetarbejdsproces

[!include [banner](../../includes/banner.md)]

Når du opretter et projektbudget, kan du angive estimerede indtægter og omkostninger for et projekt og derefter bruge det til at styre de faktiske projekttransaktioner. Projektbudgettering kræver alle de oprindelige budgetter og revisioner sendes til en projektarbejdsgang til godkendelse. Arbejdsprocessen øger din kontrol over processen og budgettet, og der oprettes en post for ændringshistorikken. Når du [opretter et projekt](/dynamicsax-2012/appuser-itpro/create-a-project), skal du anvende denne procedure til at oprette og indsende budgettet.

1. Gå til **Moduler** > **Projektstyring og regnskab** > **Projekter** > **Alle projekter**.
1. Vælg projektet på listen.
1. Vælg fanen **Plan** på detaljesiden for projektet.
1. Vælg **Projektbudget** under **budgetgruppen**.
1. I oversigtspanelet **Generelt** skal du angive følgende oplysninger:
   - Indtast en værdi i feltet **Beskrivelse**.
   - Vælg indstilling for **Oprindeligt budget**.
   - Vælg indstilling for **Resterende budget**.
1. Udvid oversigtspanelet **Omkostninger**, og vælg **Ny**. Foretag derefter følgende indstillinger for at komme i gang:
   - Vælg en indstilling for **Transaktionstype**.
   - Vælg den relevante **Kategori**.
   - Angiv en værdi i **Oprindeligt budget**.
1. Udvid oversigtspanelet **Indtægter**, og vælg **Ny**. Foretag derefter følgende indstillinger for at komme i gang:
   - Vælg en indstilling for **Transaktionstype**.
   - Vælg en **Kategori**.
   - Angiv en værdi for **Oprindeligt budget**.
1. Vælg **Gem**.
1. Vælg **Arbejdsgang \> Overfør**.
1. På siden **Gennemse oprindelig budgetarbejdsgang – Overfør** skal du angive en **kommentar** og vælge **Overfør**.
