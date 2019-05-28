---
title: Nummerserier
description: Talserier bruges til generering af læselige, entydige identifikatorer for masterdataposter og transaktionsposter, der kræver identifikatorer.
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7dadbe811e385ea6d5802c03381093d6693b23ba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560561"
---
# <a name="number-sequences"></a>Nummerserier

[!include [banner](../includes/banner.md)]

Talserier bruges til generering af læselige, entydige identifikatorer for masterdataposter og transaktionsposter, der kræver identifikatorer. En masterdatapost eller transaktionspost, der kræver et id, kaldes en *reference*.

Før du kan oprette nye poster for en reference, skal du konfigurere en nummerserie og knytte den til referencen. Det anbefales, at du bruger de sider, der findes i **Virksomhedsadministration**, til at konfigurere nummerserier. Hvis der kræves modulspecifikke indstillinger, kan du bruge parametersiden i et modul til at angive nummerserier for referencen i det pågældende modul. I **Debitor** og **Kreditor** kan du f.eks. konfigurere nummerseriegrupper, hvis du vil tildele specifikke nummerserier til specifikke debitorer eller kreditorer.

Når du konfigurerer en nummerserie, skal du angive et område, som definerer, hvilken organisation der bruger nummerserien. Området kan være **Delt**, **Firma**, **Juridisk enhed** eller **Driftsenhed**. Områderne **Juridisk enhed** og **Firma** kan også kombineres med **Regnskabskalenderperiode**, så der oprettes endnu mere specifikke nummerserier.

Nummerserieformater består af segmenter. Nummerserier med et andet område end **Delt** kan indeholde segmenter, der svarer til området. En nummerserie med området **Juridisk enhed** kan f.eks. indeholde et segment for en juridisk enhed. Hvis du medtager et områdesegment i nummerserieformatet, kan du identificere området for en specifik post ved at se på postens nummer.

Udover segmenter, der svarer til områder, kan nummerserieformater indeholde segmenter af typen **Konstant** og **Alfanumerisk**. Et **Konstant** segment indeholder et sæt af bogstaver, tal eller tegn, der ikke ændres. Et **Alfanumerisk** segment indeholder et sæt af bogstaver eller tal, hvis værdi øges, hver gang der bruges et tal. Brug et taltegn (\#) for at angive stigende tal, og tegnet & for stigende bogstaver. Formatet \#\#\#\#\#\_2017 giver f.eks. serien 00001\_2017, 00002\_2017 osv.

## <a name="number-sequence-examples"></a>Eksempler på nummerserier

I følgende eksempler vises det, hvordan segmenter bruges til oprettelse af nummerserieformater. Eksemplerne viser nærmere bestemt virkningerne af at bruge områdesegmenter.

### <a name="expense-report-numbers"></a>Udgiftsrapportnumre

I det følgende eksempel konfigureres der udgiftsrapportnumre for den juridiske enhed med navnet **CS**.

- **Område:** Rejser og udgifter
- **Reference:** Udgiftsrapportnummer
- **Omfang:** Juridisk enhed
- **Juridisk enhed:** CS

| Segmenter  | Segmenttype | Værdi     |
|-----------|--------------|-----------|
| Segment 1 | Juridisk enhed | CS        |
| Segment 2 | Konstant     | -UDGIFT- |
| Segment 3 | Alfanumerisk | \#\#\#\#  |

**Eksempel på formateret nummer**: CS-UDGIFT-0039

Du kan konfigurere et lignende nummerserieformat til andre juridiske enheder. Hvis du f.eks. kun ændrer værdien af segmentet juridisk enhed for den juridiske enhed **RW**, vil det formaterede nummer være RW-UDGIFT-0039. Du kan også ændre hele nummerserieformatet for andre juridiske enheder. Du kan f.eks. udelade området juridisk enhed, så der oprettes et formateret nummer som f.eks. Udg-0001.

### <a name="sales-order-numbers"></a>Salgsordrenumre

I følgende eksempel konfigureres der salgsordrenumre for firma-id'et **CEU**.

- **Område:** Salg
- **Reference:** Salgsordre
- **Omfang:** Firma
- **Firma:** CEU

| Segmenter  | Segmenttype | Værdi    |
|-----------|--------------|----------|
| Segment 1 | Konstant     | SO-      |
| Segment 2 | Alfanumerisk | \#\#\#\# |

**Eksempel på formateret nummer**: SO-0029

Selvom der ikke er angivet et områdesegment, genstartes nummereringen for hvert firma-id. Hvis du bruger samme format for alle firma-id'er, bruges de samme numre i hvert firma. Salgsordrenummeret SO-0029 kan f.eks. bruges i hvert firma. Du kan også ændre hele nummerserieformatet for andre firma-id'er.

### <a name="purchase-requisition-numbers"></a>Indkøbsrekvisitionsnumre

I det følgende eksempel gælder indkøbsrekvisitionsnumre for hele organisationen.

- **Område:** Indkøb
- **Reference:** Indkøbsrekvisition
- **Omfang:** Delt

| Segmenter  | Segmenttype | Værdi    |
|-----------|--------------|----------|
| Segment 1 | Konstant     | Rek      |
| Segment 2 | Alfanumerisk | \#\#\#\# |

**Eksempel på formateret nummer**: Req0052

Da omfanget er **Delt**, bruges nummerserieformatet i hele organisationen. Du kan ikke konfigurere forskellige nummerserieformater for forskellige dele af organisationen.

## <a name="performance-considerations-for-number-sequences"></a>Overvejelser vedrørende ydeevne for nummerserier

Overvej følgende oplysninger, som vedrører, hvordan konfigurationen af nummerserier kan påvirke systemets ydeevne, før du konfigurerer nummerserier.

### <a name="continuous-and-non-continuous-number-sequences"></a>Fortløbende og ikke-fortløbende nummerserier

Nummerserier kan være fortløbende eller ikke-fortløbende. En fortløbende nummerserie springer ingen numre over, men numrene vil muligvis ikke blive brugt i rækkefølge. Numre fra en ikke-fortløbende nummerserie bruges i rækkefølge, men nummerserien kan springe numre over. Hvis f.eks. en bruger annullerer en postering, genereres der et nummer, men det bruges ikke. I en fortløbende nummerserie, vil dette nummer blive brugt igen senere. I en ikke-fortløbende nummerserie bruges nummeret ikke.

Fortløbende nummerserier er typisk påkrævet for eksterne dokumenter, som f.eks. indkøbsordrer, salgsordrer og fakturaer. Dog kan forløbende nummerserier have alvorlig indvirkning på systemets svartider, fordi systemet skal anmode om et nummer fra databasen, hver gang der oprettes et nyt dokument eller en ny post.

Hvis du bruger en ikke-fortløbende nummerserie, kan du aktivere **Forudallokering** i oversigtspanelet **Ydeevne** på siden **Nummerserier**. Når du angiver et antal numre, der skal forudallokeres, vælger systemet disse numre og gemmer dem i hukommelsen. Der anmodes kun om nye numre fra databasen, når den forudallokerede mængde numre er brugt op.

Hvis ikke der er lovmæssige krav, der foreskriver brug af fortløbende nummerserier, anbefales det, at du bruger ikke-forløbende nummerserier for at opnå bedre ydeevne.

### <a name="automatic-cleanup-of-number-sequences"></a>Automatisk oprydning af nummerserier

Hvis der opstår strømafbrydelse, programfejl eller anden uventet defekt, kan systemet ikke automatisk genbruge numre til fortløbende nummerserier. Du kan køre oprydningsprocessen manuelt eller automatisk for at finde de tabte numre.

Husk at tage serverbelastningen i betragtning, når du planlægger oprydningsprocessen. Det anbefales, at du udfører oprydningen som et batchjob uden for spidsbelastningstidspunkter.
