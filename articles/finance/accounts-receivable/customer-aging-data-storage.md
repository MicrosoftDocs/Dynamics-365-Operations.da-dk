---
title: Lager af aldersfordelte debitordata
description: Dette emne indeholder en beskrivelse af processen til brug af eksternt lager til aldersfordelte kundedata. Du kan køre processen til lagring af aldersfordelte debitordata for at gøre outputtet tilgængeligt for eksport til et eksternt system.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecd4f5359019e3c4778e21cc4946b9998cd519f
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817421"
---
# <a name="customer-aging-data-storage"></a>Lager af aldersfordelte debitordata

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne indeholder en beskrivelse af processen til brug af eksternt lager til aldersfordelte kundedata. Du kan køre processen til lagring af aldersfordelte debitordata i Microsoft Dynamics 365 Finance for at gøre outputtet tilgængeligt for eksport til et eksternt system. Når du kører processen, vil de samme indstillinger for aldersfordelte rapporter, som er tilgængelige i systemet, være tilgængelige for eksterne systemer. Oplysningerne medtages altid i de eksporterede data.

Det kan være nyttigt at gøre aldersfordelte debitordata tilgængelige for et eksternt system til lagring i tilfælde, hvor outputtet indeholder mange debitorer og/eller mange transaktioner. Hvis der times ud af den eksisterende **aldersfordelte saldorapport for debitorer**, fordi der er for mange data til at blive udskrevet, kan denne funktion bruges som alternativ til at hente de samme data.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Aktivere funktionen til lagring af aldersfordelte debitordata

Før du kan bruge denne funktion, skal du aktivere den i dit system. Administratorer kan bruge indstillingerne i Funktionsstyring til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** Kredit og rykkere
- **Funktionsnavn:** Lagring af aldersfordelte debitordata

## <a name="run-the-customer-aging-data-storage-process"></a>Kær funktionen til lagring af aldersfordelte debitordata

1. Gå til **Kredit og inkasso \> Forespørgsler og rapporter \> Debitor \> Lagring af aldersfordelte debitordata**.
2. Vælg **Ny**.
3. Angiv et navn til processen i feltet **Navn**.
4. Angiv de resterende parametre efter behov.

    > [!NOTE]
    > Posteringsdetaljer medtages altid, og behandlingen udføres altid i et batchjob.

5. Vælg **OK**.
6. Opdater siden til **lagring af aldersfordelte debitordata** for at få vist værdierne for **batchnavn** og **batchkørselstid**, der vises sammen med værdien for **behandlingsstatus**. Når batchjobbet er fuldført, angives feltet **Behandlingsstatus** til **Afsluttet**, og feltet **Antal forældelseslinjer** angives. Hvis batchjobbet gentages, er feltet **Behandlingsstatus** angivet til **Venter**.
7. Vælg **filterknappen** ud for feltet **Antal forældelseslinjer** for at gennemse de filtre, der er blevet tilføjet for batchjobbet.

Siden **Lagring af aldersfordelte debitordata** indeholder ikke resultaterne. Dataenheden til **lagring af debitordata** giver dig dog mulighed for at eksportere outputtet til et hvilket som helst format, som Datastyring understøtter.

> [!NOTE]
> Før du eksporterer, skal du tilføje et filter for at begrænse de eksporterede resultater til den seneste forældelse. Tilføj f.eks. følgende kriterier for at returnere den seneste batchkørsel:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> Alternativt kan du tilføje følgende kriterier for at returnere den seneste batchkørsel for den aktuelle bruger:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())
