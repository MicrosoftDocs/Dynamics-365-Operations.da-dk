---
title: Føje datafelter til momskonfigurationer
description: Dette emne forklarer, hvordan du kan tilpasse momskonfigurationer ved at tilføje datafelter.
author: Kai-Cloud
ms.date: 10/21/2021
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
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 590c2d62995f260ba4277e1031349b0dc43f1417
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674894"
---
# <a name="add-data-fields-in-tax-configurations"></a>Føje datafelter til momskonfigurationer

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan tilpasse momskonfigurationer ved hjælp af [datafelter, der tilføjes i momsintegration](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Tilpasse momsdatamodellen

1. Gå i Microsoft Dynamics 365 Finance til **Elektronisk rapportering** > **Momskonfigurationer**.
2. Vælg **Datamodel til momsberegning** i konfigurationstræet. Vælg derefter **Opret konfiguration** i handlingsruden. 

  > [!NOTE] 
  > Hvis der ikke findes en konfigurationsudbyder, skal du oprette en og gøre den aktiv for momskonfigurationen. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
  
3. I dialogboksens rulleliste skal du vælge indstillingen **Momspligtig dokumentmodel, der er afledt af Navn: Datamodel til momsberegning, Microsoft**, angive et navn til den nye momsdatamodel og derefter vælge **Opret konfiguration**.
4. Vælg den momsdatamodel, du netop har oprettet, og vælg derefter **Designer** i handlingsruden.
5. Udvid datamodeltræet, vælg **Linjer**, og vælg derefter **Ny**.
6. Angiv et navn i dialogboksen **Opret node**, angiv en varetype, og vælg derefter **Tilføj**.
7. Tilføj eventuelle påkrævede kolonner.
8. Vælg **Gem** i handlingsruden, og vælg derefter **Fuldfør**.
9. Luk siden, og få vist den fuldførte version af momsdatamodellen.

## <a name="customize-the-tax-configuration"></a>Tilpasse momskonfigurationen

1. Gå i Finance til **Elektronisk rapportering** > **Momskonfigurationer**.
2. Vælg **Konfiguration af momsberegning** i konfigurationstræet. Vælg derefter **Opret konfiguration** i handlingsruden.
3. I dialogboksens rulleliste skal du vælge **Konfiguration af momstjeneste, der er afledt af Navn: Konfiguration af momsberegning, Microsoft**, angive et navn til den nye momskonfiguration og derefter vælge **Opret konfiguration**.
4. Vælg den momskonfiguration, du netop har oprettet, og vælg derefter **Designer** i handlingsruden.
5. Vælg den tilpassede momsdatamodel, du oprettede tidligere, i feltet **Datamodel** i sektionen **Egenskaber**.
6. Vælg den fuldførte version af momsdatamodellen i feltet **Datamodelversion**.
7. Vælg **Tilføj**, og tilføj de nødvendige momsforanstaltninger.
8. Vælg **Gem** i handlingsruden, og vælg derefter **Fuldfør**.
9. Luk siden, og se den fuldførte version af momskonfigurationen.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Implementere momsfunktioner i tilpasset momskonfigurationen

1. Gå i Regulatory Configuration Service (RCS) til **Globaliseringsfunktioner** > **Moms**.
2. Vælg **Tilføj**, angiv oplysninger om den nye funktion, og vælg derefter **Opret funktion**.
3. Vælg funktionen under fanen **Versioner**, og vælg derefter **Rediger**.
4. Under fanen **Generelt** skal du vælge den tilpassede momskonfiguration og -version i feltet **Konfigurationsversion**.
5. Vælg i dialogboksen **Administrer kolonner** de overskrifts- og linjekolonner, du vil medtage i den brugerdefinerede momsfunktion, og vælg derefter højre piletast for at føje dem til listen **Valgte kolonner**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
