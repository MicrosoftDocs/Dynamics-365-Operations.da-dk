---
title: Beregne kildeskat for fakturaer ved hjælp af kladder
description: Dette emne angiver trinnene til beregning af kildeskat (TDS – Tax Deducted at Source) i kladder.
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
ms.openlocfilehash: fde81efed6b8a72e2149056f0196e4f9d60e59f2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345513"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>Beregne kildeskat for fakturaer ved hjælp af kladder

[!include [banner](../includes/banner.md)]

Dette emne angiver trinnene til beregning af kildeskat (TDS – Tax Deducted at Source) i kladder.

Begynd med at åbne siden **Finanskladder** (**Finans > Kladdeposter > Finanskladder**).

[![Finanskladder.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Opret kladdelinjer ved hjælp af de kladdeformularer, der er vist i tabellen. Vælg kontotypen og modkontotypen, og angiv transaktionsbeløbet. 

   > [!NOTE]
   > På siden **Fakturagodkendelseskladde** skal du vælge **Find bilag** og vælge de fakturaer, der skal beregnes kildeskat på. Få vist de fakturaer, der er oprettet på siden **Fakturaregister** eller siden **Find bilag**.  

2. På siden **Kladdebilag** på fanen **Generelt** kan du få vist eller redigere den skattestandardgruppe, der er defineret for kreditoren eller debitoren, i feltet **Skattegruppe**. Det skattebeløb, der er beregnet på kladdelinjerne, er baseret på den formel, der er defineret for de kildeskattekoder, der er angivet i feltet **Skattegruppe**. 

   > [!NOTE]
   > Feltet **Gruppe for A-skat** og feltet **TCS-gruppe** bliver ikke tilgængeligt, når du vælger en kildeskattegruppe i feltet **Skattegruppe**. Feltet **Gruppe for A-skat** er kun tilgængeligt på siden **Finanskladde**. Kildeskat beregnes kun, hvis afkrydsningsfeltet **Beregn A-skat** er markeret for kreditoren eller debitoren på siden **Alle kreditorer** eller **Alle debitorer**.   

3. Vælg fanen **Skatteoplysninger**. Hvis det er nødvendigt, kan du vælge de alternative adresser til en virksomhed, som er oprettet for virksomheden i dette felt. Du kan få vist virksomhedens navn i feltet **Navn**, som findes under feltgruppen **Firmaoplysninger**. 

4. Få vist arten af vurderingskategorien for kreditoren eller debitoren i feltet **Art af vurdering**, som findes i feltgruppen **A-skat**. I feltet **Skattekontonummer** (**TAN**) kan du få vist skattekontonummeret for det valgte virksomhedsnavn, der vises.  

5. Vælg **A-skat** i menuen **A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**. Følgende felter vises i øverste rude på siden **Midlertidige transaktioner for A-skat**.

   - **Samlet beløb for A-skat** – Det samlede skattebeløb beregnet for transaktionen for kildeskattegruppen.

   - **Værdi** – Den samlede procentdel, der bruges til beregning af kildeskat for transaktionen. Den samlede procentdel er baseret på den formel, der er defineret for de kildeskattekoder, som er tilknyttet kildeskattegruppen.

   - **Reguleret beløb for A-skat i alt** – Det samlede regulerede skattebeløb for alle skattekoder i kildeskattegruppen.

   - **Kildeskat** – Hvis dette felt markeres, knyttes der en kildeskattegruppe til transaktionen.

  Felterne under fanen **Oversigt**, **Generelt** og **Regulering** på siden **Midlertidige transaktioner for A-skat** viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, der er tilknyttet kildeskattegruppen.

6. Vælg **Tærskel** for at åbne siden **Tærskel**. Få vist grænseværdien og den tærskel for fritagelse, der er defineret for den kildeskattekomponent, som er tilknyttet en bestemt kildeskattekode på denne side.

   Vælg **Formeldesigner** for at åbne formularen **Formeldesigner**. Få vist den formel, der er defineret for en bestemt kildeskattekode, på denne side. Luk **Formeldesigner** og siderne for **Midlertidige transaktioner for A-skat** for at vende tilbage til siden **Kladdebilag**.

8. Angiv de øvrige krævede oplysninger. Valider og bogfør kladden. Det skattebeløb, der er beregnet for indkøbsfakturaer, bogføres på kreditorkontoen. Det skattebeløb, der er beregnet for salgsfakturaer, bogføres på den debitorkonto, der er defineret for hver kildeskattekode i kildeskattegruppen. Kreditorkonti eller debitorkonti for kildeskattekoder er defineret på siden **Koder for A-skat**.

9. Vælg **Bogført A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**. I feltet **Værdi** vises den samlede procentdel, der anvendes til at beregne kildeskat for transaktionen.

   Felterne under fanen **Oversigt**, **Generelt** og **Beløb** på siden Midlertidige transaktioner for A-skat viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, der er tilknyttet kildeskattegruppen.
