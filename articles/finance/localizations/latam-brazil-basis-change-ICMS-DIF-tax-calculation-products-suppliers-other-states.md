---
title: Grundlæggende ændring i ICMS-DIF-momsberegningerne for produkter fra leverandører i andre delstater
description: Denne artikel indeholder en beskrivelse af konfigurationen af beregninger af ICMS-DIF-momstypen, når der modtages et regnskabsdokument i den brasilianske delstat Rio Grande do Sul (RS) eller São Paulo (SP).
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218643"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Grundlæggende ændring (dobbelt basis) i ICMS-DIF-momsberegningerne for produkter fra leverandører i andre delstater

Denne artikel beskriver konfigurationen af beregninger af **ICMS-DIF**-momstypen, når der modtages et regnskabsdokument i den brasilianske delstat Rio Grande do Sul (RS) eller São Paulo (SP).

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
    - Vælg **Nettobeløb pr. linje** i feltet **Beregningsgrundlag**.
    - Definer skattekoden, så den har en regnskabsværdi på **3**. På denne måde oprettes reguleringsposteringen automatisk, når modulet **Regnskabsbøger** er aktiveret.
    - I konfigurationen af momsgruppen skal du vælge indstillingen **Importmoms** for momskoden **ICMS-DIF**.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Brug deltaafgiftssatsen i konfigurationen af dobbeltbasis ICMS-DIF-momskoderne

Når de tidligere beskrevne indstillinger bruges, beregnes **ICMS-DIF**-momskoden som dobbeltbasisreglen. Den nominelle momssats bliver dog 18 procent, hvilket er forskelligt fra satsen på 6 procent i den simple basisregel. Denne difference forårsager uoverensstemmelsesproblemer i regnskabsdokumenter og momsrapportering. Fra og med Microsoft Dynamics 365 Finance version 10.0.29 kan du aktivere **(Brasilien) Konfigurer deltaafgiftssatsen i ICMS-DIF-momskoden for dobbelt basissagen** i **Funktionsstyring** for at fjerne uoverensstemmelsen.

- Ud over at udføre trinnene i forrige afsnit skal du vælge **ICMS 12**-momskoden i feltet **Moms på moms**.
- Angiv momssatsen for **ICMS-DIF**-momskoden til 18 procent. Feltet **Procent/Beløb** viser den nominelle momssats på 6 procent.

> [!NOTE]
> Momskoderne **ICMS-DIF** og **ICMS 12** skal tildeles samme momsgruppe.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Grundlæggende ændring (dobbelt basis) i ICMS-DIF-momsberegningerne for produkter til ikke-momspligtige forbrugere (DIFAL) i andre delstater

Aktivér funktionen **(Brasilien) Dobbelt basisberegning for ICMS-DIFAL i salgstransaktioner** i **Funktionsstyring** for at understøtte basisændringen af ICMS-DIF ved handel til ikke-momspligtige forbrugere fra en anden delstat. ICMS-DIF-prøvemomskoden træder i kraft i salgsordre- og fritekstfakturaposteringer.

Aktivér **(Brasilien) Dobbelt basisberegning for ICMS-DIFAL i IPI-sager** i **Funktionsstyring** for at understøtte scenarier, hvor handel til ikke-momspligtige forbrugere fra en anden delstat også er ansvarlig for Imposto sobre Produtos Industrializados (IPI). Momsbeløbet for IPI-momskoden registreres og anvendes på momsgrundlaget i ICMS-DIFAL.

- I overskriften på salgsordren eller fritekstfakturaen i oversigtspanelet **Regnskabsoplysninger** skal indstillingen **Endelig bruger** angives til **Ja**.
- I overskriften på købsordren eller leverandørfakturaen i oversigtspanelet **Regnskabsoplysninger** skal indstillingen **Brug og forbrug** angives til **Ja**.
