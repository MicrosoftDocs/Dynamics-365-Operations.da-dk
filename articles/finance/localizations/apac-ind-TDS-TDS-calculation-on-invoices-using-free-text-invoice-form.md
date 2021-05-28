---
title: Beregning af kildeskat på fakturaer fra siden Fritekstfaktura
description: Dette emne beskriver, hvordan du beregner kildeskat på fakturaer ved hjælp af siden Fritekstfaktura.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023124"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>Beregning af kildeskat på fakturaer fra siden Fritekstfaktura

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du beregner kildeskat på fakturaer ved hjælp af siden **Fritekstfaktura**.

1. Gå til **Debitor \> Fakturaer \> Alle fritekstfakturaer**.

    [![Siden Fritekstfaktura](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Vælg **Ny** for at oprette en fritekstfaktura, og angive de krævede oplysninger.
3. Vælg fanen **Faktura**. I feltet **Art af vurdering** i sektionen **Gruppe for A-skat** vises vurderingskatagorien for debitoren.
4. I feltet **Kildeskattegruppe** kan du gennemse eller ændre den standardgruppe for kildeskat, der er defineret for debitoren.

    > [!NOTE]
    > Når du vælger en værdi i feltet **Kildeskattegruppe** bliver feltet **Kildeskattegruppe** utilgængeligt. Kildeskat beregnes kun, hvis indstillingen **Beregn A-skat** er angivet til **Ja** for debitoren på siden **Alle debitorer**.

5. På fanen **Skatteoplysninger** i sektionen **Firmaoplysninger** i feltet **Navn** skal du vælge virksomhedens navn for en alternativ adresse, som er angivet for virksomheden.

    I sektionen **A-skat** viser feltet **Skattekontonummer (TAN)** skattekontonummeret (TAN – Tax Account Number) for den valgte virksomhed.

6. Opret fakturalinjer under fanen **Fakturalinjer**, og angiv de krævede oplysninger.

    I sektionen **Gruppe for A-skat** viser feltet **Skattekontonummer (TAN)** skattekontonummeret, og feltet **Kildeskattegruppe** viser gruppen for kildeskat.

7. Vælg **A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**. Den øverste del af denne side indeholder følgende felter:

    - **Samlet beløb for A-skat** – Den samlede kildeskat er beregnet for transaktionen for kildeskattegruppen.
    - **Værdi** – Den samlede procentdel, der er brugt til beregning af kildeskat for transaktionen. Den samlede procentdel er baseret på den formel, der er defineret for kildeskattekoderne og er tilknyttet kildeskattegruppen.
    - **Reguleret beløb for A-skat i alt** – Det samlede regulerede skattebeløb for alle skattekoder i kildeskattegruppen.
    - **Kildeskat** – Et markeret afkrydsningsfelt angiver, at der er knyttet en kildeskattegruppe til transaktionen.

    Felterne under fanen **Oversigt**, **Generelt** og **Regulering** viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, som er tilknyttet kildeskattegruppen.

8. Vælg **Tærskel** for at åbne siden **Tærskel**, hvor du kan gennemse den grænseværdi, der er defineret for den skattekomponent, som er tilknyttet en specifik kildeskattekode.
9. Vælg **Formeldesigner** for at åbne siden **Formeldesigner**, hvor du kan gennemse den formel, der er defineret for en specifik kildeskattekode.
10. Bogfør fritekstfakturaen. Det skattebeløb, der er beregnet for fritekstfakturaen, bogføres på den debitorkonto, der er defineret for hver kildeskattekode i kildeskattegruppen. Kreditorkonti for kildeskattekoder er defineret på siden **Koder for A-skat**.
11. Vælg **Bogført A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**. Feltet **Værdi** viser den samlede procentdel, der er brugt til beregning af kildeskat for transaktionen.

    Felterne under fanen **Oversigt**, **Generelt** og **Beløb** viser de skattebeløb, der blev beregnet på fakturalinjerne.

12. Gennemse beregningsoplysningerne for kildeskat for hver kildeskattekode, der er tilknyttet kildeskattegruppen.
