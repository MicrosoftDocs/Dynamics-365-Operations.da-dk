---
title: Beregne skattefakturaer ved hjælp af formularerne Indkøbsordre og Salgsordre
description: Denne artikel angiver trinnene til beregning af kildeskat (TDS – Tax Deducted at Source) for forskellige typer fakturaer.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 72883741ee7eed6b0296736c80dd648c882ae53e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853279"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Beregne skattefakturaer ved hjælp af formularerne Indkøbsordre og Salgsordre

[!include [banner](../includes/banner.md)]

Denne artikel angiver trinnene til beregning af kildeskat (TDS – Tax Deducted at Source) for forskellige typer fakturaer ved hjælp af siderne **Indkøbsordre**, **Indkøbskladde**, **Rammeordre** og **Salgsordre**.

1. Opret en indkøbsordre, indkøbskladde, købsrammeordre eller en salgsordre ved hjælp af den viste side. Angiv de relevante oplysninger.

2. Vælg fanen **Opsætning** for at få vist arten af kreditorens eller debitorens vurdering. Disse oplysninger vises i feltet **Art af vurdering** under feltgruppen **Gruppe for A-skat**.

3. I feltet **Skattegruppe** kan du få vist eller redigere den skattestandardgruppe, der er defineret for kreditoren eller debitoren.

   > [!NOTE]
   > Feltet **TCS-gruppe** er ikke tilgængeligt, når du vælger en kildeskattegruppe i feltet **Kildeskattegruppe**. Kildeskat beregnes kun, hvis afkrydsningsfeltet **Beregn A-skat** er markeret for kreditoren eller debitoren på siden **Alle kreditorer** eller **Alle debitorer**.  

4. Opret varelinjer under fanen **Linjer**, og angiv de krævede oplysninger.

5. Vælg fanen **Opsætning** (linjeniveau) for at få vist eller ændre den kildeskattegruppe, der er defineret på overskriftsniveau. Skattegruppen vises i feltet **Skattegruppe**, som findes under feltgruppen **Gruppe for A-skat**.

6. Vælg fanen **Skatteoplysninger**, og vælg alternative adresser, der er oprettet for det firmanavn, der vises i dette felt. Firmanavnet vises i feltet **Navn**, som findes under feltgruppen **Firmaoplysninger**. 

   Det amerikanske skattenavn for det valgte firma vises i feltet **Skattekontonummer** (**TAN**) under feltgruppen **A-skat**. 

7. Vælg **A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**. Få vist følgende felter i øverste rude på siden **Midlertidige transaktioner for A-skat**.

   - **Samlet** **beløb** **af** **A**-**skat** – Det samlede skattebeløb beregnet for transaktionen for kildeskattegruppen.

   - **Værdi** – Den samlede procentdel, der bruges til beregning af kildeskat for transaktionen. Den samlede procentdel er baseret på den formel, der er defineret for de kildeskattekoder, som er tilknyttet kildeskattegruppen.

   - **Reguleret beløb for A-skat i alt** – Det samlede regulerede skattebeløb for alle skattekoder i kildeskattegruppen.

   - **Kildeskat** – Hvis dette felt markeres, knyttes der en kildeskattegruppe til transaktionen.

Felterne under fanen **Oversigt**, **Generelt** og **Regulering** på siden **Midlertidige transaktioner for A-skat** viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, der er tilknyttet kildeskattegruppen.

8. Vælg **Tærskel** for at åbne siden **Tærskel**. Få vist den grænseværdi, der er defineret for kildeskattekomponenten, som er tilknyttet en bestemt kildeskattekode på denne side.

9. Vælg **Formeldesigner** for at åbne siden **Formeldesigner**. Få vist den formel, der er defineret for en bestemt kildeskattekode, på denne side. 

10. Bogfør fakturaen. Det skattebeløb, der er beregnet for indkøbsfakturaer, bogføres på kreditorkontoen, og det skattebeløb, der er beregnet på salgsfakturaer, bogføres på den debitorkonto, der er defineret for hver kildeskattekode i kildeskattegruppen. Kreditorkonti eller debitorkonti for kildeskattekoder er defineret på siden **Koder for A-skat**.

11. Vælg knappen **Forespørgsel** **> Faktura > Bogført A-skat** for at åbne siden **Transaktioner for A-skat**. Du kan få vist den samlede procentdel, der er anvendt til at beregne skatteværdier for transaktionen, i feltet **Værdi**.

Felterne under fanen **Oversigt**, **Generelt** og **Beløb** på siden **Transaktioner for A-skat** viser oplysningerne om den kildeskat, der er beregnet for transaktionen. Få vist skatteberegningsoplysningerne for hver kildeskattekode, der er tilknyttet kildeskattegruppen.
