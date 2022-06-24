---
title: Konfigurer nummerserier for detailopgørelser
description: Denne artikel beskriver, hvordan du konfigurerer de nummerserier, der kræves til detailopgørelser i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 5c4eb872ec2151a9f4ac5462ad43dd03a6705487
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879997"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Konfigurer nummerserier for detailopgørelser

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel beskriver, hvordan du konfigurerer de nummerserier, der kræves til detailopgørelser i Microsoft Dynamics 365 Commerce.

Der bruges to typer momsgrupper i Dynamics 365 Commerce: 

- **Transaktionsopgørelser** er beregnet til at blive oprettet og bogført med høj frekvens. De bruges til at bogføre alle ikke-økonomiske transaktioner i butikken til Dynamics 365 Commerce Headquarters. 
- **Regnskaber** er beregnet til at blive oprettet og bogført én gang pr. arbejdsdag. De omfatter kun lukkede skift fra de detailbutikker, der er overført til Commerce Headquarters via p-jobbet.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Konfigurere en nummerserie for lageropgørelse

Når du har fuldført opsætningen af en detailbutik i Commerce Headquarters, skal du konfigurere en entydig nummerserie, der skal bruges til opgørelser under oprettelsen af opgørelsen.

Udfør følgende trin for at konfigurere en nummerserie for lageropgørelse i Commerce.

1. Gå til **Organisationsadministration \> Nummerserier \> Nummerserier**.
1. Vælg **Ny \> Nummerserie** for at oprette en ny post.
1. Angiv en nummerseriekode i feltet **Nummerseriekode** i oversigtspanelet **Identifikation**.
1. Indtast et navn i feltet **Nummersekvensnavn**.
1. Vælg **Driftsenhed** i feltet **Område** i oversigtspanelet **Intervalparametre**.
1. Vælg den butik, som nummerserien skal bruge i feltet **Driftsenhed**.
1. Definer segmenterne i oversigtspanelet **Segmenter**.
1. Angiv feltet **Område** til **Detailbutik** i oversigtspanelet **Referencer**.
1. Angiv **referencefeltet** til **opgørelsesnummer**, og vælg derefter **OK**.

    ![Oversigtspanelerne Identifikation, Områdeparametre, Segmenter og Referencer på siden Nummerserier.](media/retail-statements-num-seq-setup-01.png)

1. I sektionen **Nummertildeling** i oversigtspanelet **Generelt** skal du opdatere felterne **Mindste** og **Største**, så de svarer til længden på det **alfanumeriske** segment, som du har defineret i oversigtspanelet **Segmenter**.
1. I oversigtspanelet **Ydeevne** anbefales det, at du angiver indstillingen **Fortildeling** til **Ja**, og feltet **Antal numre** til **25**.

    ![Oversigtspanelerne Generelt og Ydeevne på siden Nummerserier.](media/retail-statements-num-seq-setup-02.png)

1. Hvis du har foretaget ændringer, skal du vælge **Gem** i handlingsruden for at gemme dem.
