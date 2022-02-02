---
title: Grundlæggende ændring i ICMS-DIF-momsberegningerne for produkter fra leverandører i andre delstater
description: Dette emne indeholder en beskrivelse af konfigurationen af beregninger af ICMS-DIF-momstypen, når der modtages et regnskabsdokument i den brasilianske delstat Rio Grande do Sul (RS) eller São Paulo (SP).
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 16f78b85567e6d08c588e621119513ff070bf618
ms.sourcegitcommit: 68655c5673aef9892063e5913ffee6bfc3817387
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2022
ms.locfileid: "8016164"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Grundlæggende ændring i ICMS-DIF-momsberegningerne for produkter fra leverandører i andre delstater

Dette emne beskriver konfigurationen af beregninger af **ICMS-DIF**-momstypen, når der modtages et regnskabsdokument i den brasilianske delstat Rio Grande do Sul (RS) eller São Paulo (SP).

Ifølge definitionen i delstatens lovgivning skal den ICMS (Imposto sobre Circulação de Mercadorias e Serviços), der opkræves, følge denne regel:

*ICMS at indsamle* = ([(*Operationsbeløb* - *ICMS fra kilde*) ÷ (1 - *intern ICMS %*)] × *intern ICMS %*) – *ICMS-beløb fra kilde*

## <a name="example"></a>Eksempel

Et brasiliansk firma i delstaten RS modtager et regnskabsdokument for et køb hos en leverandør i delstaten SP. Firmaet skal opkræve den procentvise difference i ICMS mellem RS-delstaten (18 procent) og SP-delstaten (12 procent). Basis skal dog beregnes i overensstemmelse med den foregående regel.

- **Operationsbeløb:** 1.000,00 brasilianske real (R$ 1.000,00)
- **ICMS mellem delstater:** R$ 120,00
- **ICMS-procent i RS-delstaten:** 18 procent
- **ICMS, der skal opkræves i RS-delstaten:** (\[(1.000 – 120) ÷ (1 – 0,18)\] × 0,18 ) – 120 = R$ 73,17 

## <a name="resolution"></a>Løsning

Hvis du vil beregne differential ICMS (ICMS-DIF) i overensstemmelse med RS-delstatens regler, skal du konfigurere momskoder og en momsgruppe på følgende måde:

1. Opret en momskode, som skal modtage ICMS på 12 procent (for den anden delstat). Denne kode bruges til registrering af momsbeløbet fra kreditoren.
2. Opret en momskode for at opkræve ICMS-DIF. Denne momskode skal have et procentbeløb på 18 procent (for din egen delstat) for at definere forskellen mellem 18 og 12 procent. Angiv momstypen til **ICMS-DIF**. Momskoden skal defineres på følgende måde i beregningsparametrene:

    - Vælg **Procent af bruttobeløb** i feltet **Oprindelse**.
    - Vælg **Nettobeløb pr. linje** eller **Nettobeløb for fakturasaldo** i feltet **Beregningsgrundlag**.
    - Definer skattekoden, så den har en regnskabsværdi på **3**. På denne måde oprettes reguleringsposteringen automatisk, når modulet **Regnskabsbøger** er aktiveret.
    - I konfigurationen af momsgruppen skal du vælge indstillingen **Importmoms** for momskoden **ICMS-DIF**.
