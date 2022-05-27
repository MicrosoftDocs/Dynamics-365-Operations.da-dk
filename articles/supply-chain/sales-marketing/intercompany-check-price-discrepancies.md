---
title: Kontroller uoverensstemmelser i pris i interne ordrer
description: Dette emne forklarer, hvordan du kontrollerer uoverensstemmelser i pris i interne ordrer
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3167077e653f2316f5ce54c2a07ef9c2978ecebb
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678312"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Kontroller uoverensstemmelser i pris i interne ordrer

[!include [banner](../../includes/banner.md)]

Du kan bruge denne fremgangsmåde til at kontrollere for uoverensstemmelser i priser i interne ordrer.

1. Gå til **Indkøb og forsyning \> Periodisk \> Oprydning \> Kontrollere uoverensstemmelser i pris i interne ordrer**.
1. Opret evt. et batchjob, og vælg derefter på **OK** for at kontrollere priserne og rabatterne for interne salgs- og indkøbsordrer. Ellers skal du vælge **Annuller** for at lukke siden uden at udføre kontrollen.

    > [!TIP]
    > Hvis der opstår synkroniseringsproblemer eller problemer med priser, vil disse blive vist i en informationsmeddelelsen. Du kan udskrive informationsmeddelelsen som reference.

1. Dobbeltklik på informationsmeddelelsen, og vælg den relevante linje for at åbne ordren i den aktuelle juridiske enhed. Åbn ordren i den relaterede juridiske enhed ved at vælge **Intern** og derefter **intern indkøbsordre** eller **intern salgsordre**.

    > [!NOTE]
    > Sådan tillades en opdatering af interne ordre:
    >
    > 1. Gå til **Debitorer \> Kunder \> Alle kunder**.
    > 1. Vælg fanen **Generelt** i handlingsruden, og vælg derefter **Intern handel**.
    > 1. Vælg **politikker for indkøbsordrer** eller **salgsordrer** på siden **Intern handel**.
    > 1. Marker **Tillad prisredigering**, og **tillad rabatredigering** i begge områder.

1. Åbn den relevante interne ordre, hvor du vil opbevare prisen.
1. For hver ordrelinje skal du redigere feltet **Enhedspris** og derefter ændre den tilbage til den oprindelige værdi. Juster feltet **Rabat** for linjen frem og tilbage, og juster felterne **Indkøbsgebyrer** eller **Salgsgebyrer** tilbage og frem. Ved at justere værdierne frem og tilbage udløses en synkronisering af priser, rabatter og gebyrer fra denne interne ordrelinje til den tilknyttede interne ordrelinje, så de synkroniseres automatisk.

    > [!NOTE]
    > Denne synkronisering er kun gyldig, hvis den interne salgsordre ikke er blevet faktureret. Hvis den interne salgsordre er blevet fakturabogført og der er oprettet en debitorfakturakladde, skal du foretage eventuelle ændringer direkte i de interne indkøbsordrelinjer ved at angive priser, rabatter og gebyrer, der svarer til priser, rabatter og gebyrer i den interne debitorfakturajournal. Hvis du ikke gør dette, kan den interne indkøbsordre ikke fakturabogføres, da ordretotalerne ikke vil stemme overens.

1. Gentag processen, indtil alle interne indkøbs- og salgsordrer er synkroniseret.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
