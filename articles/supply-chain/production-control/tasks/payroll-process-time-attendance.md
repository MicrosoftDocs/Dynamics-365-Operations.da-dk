---
title: Aktivere lønproces for tid og fremmøde
description: Denne procedure viser, hvordan lønprocessen for tid og fremmøde aktiveres.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3b196e25699c43dbac06e950aae0ad8a9457a8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566545"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Aktivere lønproces for tid og fremmøde

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan lønprocessen for tid og fremmøde aktiveres. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Opret en lønart med en relateret lønsats
1. Tid og fremmøde > Opsætning > Løn > Lønarter
2. Klik på Ny.
3. Indtast en værdi i feltet Lønart.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Gem.
6. Klik på Satser.
    * Satser for lønarter defineres for bestemte tidsintervaller og kan være angivet for individuelle arbejdere. Det er ikke altid nødvendigt at oprette satser til lønarterne i tid og fremmøde. Disse oplysninger findes muligvis i det lønsystem, der bruges til at oprette løn.  
7. Klik på Ny.
8. Markér den valgte række på listen.
9. Indtast et tal i satsfeltet.
10. Klik på Gem.

## <a name="create-a-pay-agreement"></a>Opret en lønaftale
1. Luk siden.
2. Luk siden.
3. Gå til Lønaftaler.
    * Tid og fremmøde > Opsætning > Lønaftaler  
4. Klik på Ny.
5. Indtast en værdi i feltet Lønaftale.
6. Skriv en værdi i feltet Beskrivelse.
7. Klik på Gem.
8. Klik på Aftalelinjer.
9. Klik på Ny.
10. Markér den valgte række på listen.
11. Indtast eller vælg en værdi i feltet Profiltype.
12. Indtast eller vælg en værdi i feltet Lønart.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Opret lønaftale for tidsregistreringsarbejder
1. Luk siden.
2. Luk siden.
3. Gå til Arbejdere, der registrerer tid.
    * Tid og fremmøde > Opsætning > Arbejdere, der registrerer tid  
4. Klik op linket i den valgte række på listen.
5. Klik på fanen Ansættelse.
6. Udvid sektionen Tidsregistrering.
7. Klik på Rediger.
8. Indtast eller vælg en værdi i feltet Lønaftale.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]