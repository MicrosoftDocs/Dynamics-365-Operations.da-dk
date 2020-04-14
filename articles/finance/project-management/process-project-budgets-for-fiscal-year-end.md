---
title: Overføre projektbudgetter ved regnskabsårets afslutning
description: Denne artikel indeholder oplysninger om, hvordan du kan overføre resterende budgetbeløb til fremtidige år og oprette budgetregisteroplysninger.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172324"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Overføre projektbudgetter ved regnskabsårets afslutning

[!include [banner](../includes/banner.md)]

Når du arbejder på et projekt, der strækker sig over flere år, kan du have resterende budgetbeløb ved regnskabsårets afslutning. Du kan overføre de resterende budgetbeløb til et fremtidigt år og oprette budgetregisteroplysninger for beløbene i de tilknyttede finanskonti. Før du overfører restbeløbene, skal du gennemgå og analysere de resterende budgetbeløb.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Gennemgå og analysere resterende budgetbeløb

Udfør nedenstående trin for at gennemse budgetbeløbene ved årsafslutningen for projekter, men uden at overføre beløbene.

1. Gå til **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overførte budgetter**. 
2. Kontroller, at **Overfør resterende projektbudgetbeløb** ikke er aktiveret under fanen **Indstillinger for årsafslutning** på siden **Proces for projektbudgetoverførsel**.
3. Vælg det regnskabsår, du vil have vist det resterende budgetbeløb for, i feltet **Projektbudgetår** under fanen **Parametre**. 
4. Vælg det regnskabsår, du vil have vist de resterende budgetbeløb for, i feltet **Nyt regnskabsår**. 
5. Vælg **Resterende budget** i feltet **Fra budgetmodel**. 
6. Hvis du vil inkludere projekter, der opfylder dine valgte kriterier, uden at der er et resterende budget, skal du vælge **Vis nul resterende**.  
7. Under fanen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle budgetter, der opfylder dine valgte kriterier, og derefter vælge **Behandl**. 
8. Hvis du opretter en databaseforespørgsel, der indlæser en bestemt gruppe budgetter i ruden, skal du vælge **Hent valgte budgetter**.

Yderligere oplysninger om en bestemt linje i ruden finder du ved at markere linjen og derefter vælge **Vis budgetoplysninger** eller **Vis konti**.

## <a name="carry-forward-remaining-budget-amounts"></a>Overføre resterende budgetbeløb 

Når du behandler de resterende budgetbeløb, kan du oprette posteringer i finansbogholderiet for de beløb, du overfører. Hvis du vil oprette finansposteringer, skal du udføre trinnene i afsnittet [Overføre budgetbeløb og oprette finansposteringer](#carry-forward). 

> [!NOTE]
> De budgetbeløb, der overføres, overføres til den budgetmodel, der er valgt som overført budgetmodel på siden **Budgetmodeller**.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Overføre budgetbeløb og oprette finansposteringer

1.  Vælg **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overførte budgetter**. 
2. På siden **Proces for projektbudgetoverførsel** skal du vælge **Årsafslutning** og derefter aktivere **Overfør resterende projektbudgetbeløb** og **Opret budgetregisterposter i Finans**. 
3. Vælg følgende i feltgruppen **Projektparametre** under fanen **Parametre**:

   - **Projektbudgetår**: Vælg starten af det regnskabsår, du vil have vist de resterende budgetbeløb for. 
   - **Drift**: Opret driftsposter i Finans. 
   -  **IGVF**: Opret IGVF-transaktioner (igangværende arbejde) i Finans.
   -  **Løn**: Opret lønfordelingsposteringer i Finans. 

5. Angiv følgende oplysninger i feltgruppen **Finans**: 

   - Vælg det regnskabsår, du vil overføre de resterende budgetbeløb i projekterne til, i feltet **Nyt regnskabsår**. Standardværdien er ét år efter værdien i feltet **Projektbudgetår**.
   -  Vælg den periode, du vil oprette budgetregisteroplysningerne i finansbogholderiet for, i feltet **Overførselsperiode**. Dette er typisk den første periode i det nye regnskabsår.

6. Angiv følgende oplysninger i feltgruppen **Kopiér til/fra**:

   - Vælg i feltet **Fra budgetmodel** den projektbudgetmodel, der er knyttet til de resterende budgetbeløb, som du vil overføre for projekterne. 
   - Vælg i feltet **Til finansbudgetmodel** den finansbudgetmodel, der er knyttet til de budgetbeløb, som du vil overføre til finansbogholderiet. 
   -  Vælg **Overfør salgsvaluta**, hvis du vil bruge projektets salgsvaluta til de finansposteringer, der oprettes, når du overfører budgetbeløbene i projekterne. Når indstillingen ikke er markeret, bruger posteringerne regnskabsvalutaen. 
   -  Vælg **Vis nul resterende** for at inkludere projekter, der ikke indeholder resterende budgetbeløb, men lever op til de øvrige kriterier, som du vælger i de projekter, der vises i den nederste rude.

7. Under fanen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle budgetter, der opfylder de kriterier, du har valgt. Hvis du foretrækker at oprette en databaseforespørgsel, der indlæser en bestemt gruppe projektbudgetter i ruden, skal du vælge **Hent valgte budgetter**.
8. For hvert projekt, du vil behandle, skal du vælge indstillingen i starten af projektlinjen.

    > [!TIP]
    > Hvis du vil vælge alle eller de fleste af projekterne, skal du markere afkrydsningsfeltet øverst til venstre. Hvis du vil udelade behandlingen af et projekt, skal du fjerne markeringen for dette projekt.

9. Hvis du vil overføre de resterende budgetbeløb for de valgte projekter til det valgte regnskabsår og oprette budgetregisteroplysninger i finansbogholderiet, skal du vælge **Behandl**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Overføre budgetbeløb uden at oprette finansposteringer

1. Gå til **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overførte budgetter**.
2. Vælg **Overfør resterende projektbudgetbeløb** ikke er aktiveret i feltet **Indstillinger for årsafslutning** på siden **Proces for projektbudgetoverførsel**.
3. Vælg det regnskabsår, du vil have vist de resterende budgetbeløb for, i feltet **Projektbudgetår** i gruppen **Parametre**.
4. Angiv følgende oplysninger i gruppen **Kopiér til/fra**:

   - Vælg i feltet **Fra budgetmodel** den projektbudgetmodel, der er knyttet til de resterende budgetbeløb, som du vil overføre for projekterne. 
   - Vælg **Vis nul resterende**, hvis du vil inkludere projekter, der opfylder dine valgte kriterier, uden at der er et resterende budget.
   - I gruppen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle budgetter, der opfylder de kriterier, du har valgt. Hvis du opretter en databaseforespørgsel, der indlæser en bestemt gruppe projektbudgetter i ruden, skal du vælge **Hent valgte budgetter**.

5. For hvert projekt, du vil behandle, skal du vælge indstillingen i starten af projektlinjen. 
6. Vælg **Behandl** for at overføre de resterende budgetbeløb i de valgte projekter til det valgte regnskabsår.

