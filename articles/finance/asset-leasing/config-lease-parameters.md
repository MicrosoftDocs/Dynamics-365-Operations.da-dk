---
title: Konfigurere leasingparametre (prøveversion)
description: Dette emne beskriver konfigurationsindstillingerne for aktivleasing, f. eks. sikkerhedsoplysninger og regnskabsindstillinger.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a644b3c9d9ed4fc86a816af1ab338b96b1aa7ad
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968071"
---
# <a name="configure-lease-parameters"></a>Konfigurere leasingparametre

[!include [banner](../includes/banner.md)]

Flere konfigurationsindstillinger har indflydelse på, hvordan aktivleasing fungerer. Disse indstillinger omfatter kladdenavne, generelle parametre og indstillinger for posteringsprofil.

1. Gå til **Aktivleasing \> Opsætning \> Parametre til aktivleasing**.
2. Under fanen **Leasingaftaler** skal du vælge oversigtspanelet **Generelt**.

    Parameteren **Tillad manuel klassificeringstilsidesættelse** bestemmer, om leasingklassifikationen kan tilsidesættes, før betalingsplanen bekræftes.

    Parameteren **Batch på tværs af enheder** bestemmer, om du kan bogføre i andre juridiske enheder fra den aktuelle juridiske enhed. Hvis denne parameter er slået til, kan du oprette kladdeposteringer for de juridiske enheder, du har adgang til.

3. Angiv indstillingen til **Tillad sletning af bekræftede leasingaftaler** til **Ja** for at tillade, at leasingaftaler, der har bekræftede betalingsplaner, skal slettes. Leasingaftaler kan ikke slettes, hvis der er knyttet bogførte eller ikke-bogførte posteringer til dem, uanset indstillingen af denne funktion. Du kan ikke gendanne en leasingaftales post, efter at den er slettet. Hvis du overfører poster til en slettet leasingaftale, enten manuelt eller gennem dataenheder, behandles de overførte oplysninger som nye, ikke som en opdatering til en eksisterende leasingaftale.

    Hvis du angiver denne indstilling til **Ja**, og kartotekets overførselstype er **Kumulativ catch-up-indstilling A eller B**, indstiller systemet feltet for **Trinvis lånerate** til værdien af feltet **Trinvis lånerate ved overgang** på siden **Opsætning af kartotek**. Hvis denne indstilling er angivet til **Nej**, angives satsen for hovedleasingaftalen til værdien i feltet **Trinvis lånesats** på siden **Kartotekoplysninger**, uanset hvilken overførselstype kartoteket er.

4. Angiv indstillingen **Tillad tilbageførsler af afskrivning på det lukkede kartotek** til **Ja**, hvis du vil tillade, at afskrivningsudgiftsposteringerne tilbageføres. Udgiftsposteringer kan tilbageføres, også selvom kartotekets version er lukket.

    > [!NOTE]
    > Det anbefales, at du beholder denne indstilling angivet til **Nej**. Indstillingen af denne funktion bruges som en validering og kontrol for at forhindre, at et lukket kartotek afskrives ved en fejltagelse. Hvis du holder indstillingen angivet til **Nej**, kan du hjælpe med at bevare den bogførte nettoværdi og fremtidige afskrivningsberegninger.

5. Angiv indstillingen **Tillad opdeling af betalingsbeløb** til **Ja** for at tillade en opdeling af betalingsbeløbene i oversigtspanelet **Betalingsplanlinjer** på siden **Leasing**. Typerne af betalingsopdelinger defineres under **Opsætning** på siden **Betalingsbeløbstyper**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
