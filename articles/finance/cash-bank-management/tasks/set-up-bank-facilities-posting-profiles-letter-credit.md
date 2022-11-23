---
title: Oprette posteringsprofiler for bankfaciliteter til remburs
description: Denne procedure gennemgår oprettelsen af en bankfacilitet og posteringsprofil, der bruges til at behandle remburser.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779456"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Oprette posteringsprofiler for bankfaciliteter til remburs

[!include [banner](../../includes/banner.md)]

Denne procedure gennemgår oprettelsen af en bankfacilitet og posteringsprofil, der bruges til at behandle remburser. 

Disse opgaver bruger demofirmaet 'USMF'.


## <a name="general-ledger-parameter"></a>Finansparameter
1. Gå til **Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre**.
2. Udvid sektionen **Bankdokument**.
3. Vælg indstillingen **Aktivér importremburs**.
4. Vælg indstillingen **Aktivér eksportremburs**.
5. Klik på **Gem**.
6. Luk siden.

## <a name="create-bank-facility"></a>Oprette bankfacilitet
1. Gå til **Kontant- og bankstyring > Opsætning > Bankfaciliteter**.
2. Klik på **Ny**.
3. Angiv navnet på bankfacilitetsgruppen i feltet **Facilitetsgruppe**.
4. Angiv beskrivelsen af bankfacilitetsgruppen i feltet **Beskrivelse**.
5. Klik på **Gem**.
6. Klik på fanen **Facilitetstyper**.
7. Klik på **Ny**.
8. I feltet **Facilitetstype** skal du angive en entydig kode.
9. Indtast en værdi i feltet **Beskrivelse**.
10. Klik på rullelisten i feltet **Facilitetsgruppe** for at åbne opslaget.
11. Find og vælg den ønskede post på listen.
12. Klik op linket i den valgte række på listen.
13. Vælg bankfacilitetens art i feltet **Facilitetsart**.
14. Klik på **Gem**.
15. Luk siden.

## <a name="bank-posting-profile"></a>Bankbogføringsprofil
1. Gå til **Kontant- og bankstyring > Opsætning > Bogføringsprofil for bankdokumenter**.
2. Klik på **Ny**.
3. Klik på rullelisten i feltet **Konto/gruppenummer** for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Vælg hovedkontoen til udligning.
    * Denne konto bruges til beregning af likviditetsbudgettet.  
7. Vælg kontoen til udgiftsposteringer i feltet **Gebyrkonto**.
8. Vælg kontoen til avanceposteringer i feltet **Margenkonto**.
    * Denne konto debiteres, når startdepositummet bogføres, og krediteres, når betalingen bogføres.  
9. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
