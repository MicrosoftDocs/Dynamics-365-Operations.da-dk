---
title: Oprette posteringsprofiler for bankfaciliteter til garanti
description: Denne opgave opretter en bankfacilitet og bogføringsprofil, der er nødvendig til at behandle en garanti.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a7e60903e31d98e24f578dc381bb0b140944e07a88516a6a81bbba1b8981982
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742222"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Oprette posteringsprofiler for bankfaciliteter til garanti

[!include [banner](../../includes/banner.md)]

Denne opgave opretter en bankfacilitet og bogføringsprofil, der er nødvendig til at behandle en garanti.



Denne opgave bruger demofirmaet USMF. 




## <a name="general-ledger-parameter"></a>Finansparameter
1. Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre
2. Udvid sektionen Bankdokument.
3. Vælg garantiindstillingen Aktivér.
4. Klik på rullelisten i feltet Posteringsjournal for at åbne opslaget.
5. Find og vælg den ønskede post på listen.
6. Klik op linket i den valgte række på listen.
7. Klik på fanen Nummerserier.
    * Definer nummerseriekode for garantinummer og garantitransaktionsreferencer  
8. Klik på Gem.
9. Luk siden.

## <a name="create-bank-facility"></a>Oprette bankfacilitet
1. Gå til Kontant- og bankstyring > Opsætning > Bankfaciliteter
2. Klik på Ny.
3. Angiv navnet på bankfacilitetsgruppen for garantiposteringen i feltet Facilitetsgruppe.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Gem.
6. Klik på fanen Facilitetstyper.
7. Klik på Ny.
8. Angiv navnet på den bankfacilitetstype, der er relateret til bankfacilitetsaftalen, i feltet Facilitetstype.
9. Indtast en værdi i feltet Beskrivelse.
10. Klik på rullelisten i feltet Facilitetsgruppe for at åbne opslaget.
11. Find og vælg den ønskede post på listen.
12. Klik op linket i den valgte række på listen.
13. Vælg en indstilling i feltet Facilitetsart.
14. Klik på Gem.
15. Luk siden.

## <a name="bank-posting-profile"></a>Bankbogføringsprofil
1. Gå til Kontant- og bankstyring > Opsætning > Bogføringsprofil for bankdokumenter.
2. Klik på Ny.
3. Klik på rullelisten i feltet Konto/gruppenummer for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Vælg hovedkontoen til udligning i feltet Afregn konto.
7. Vælg kontoen til udgiftsposteringer i feltet Gebyrkonto.
8. Vælg kontoen til avanceposteringen feltet Margenkonto.
9. I feltet Afviklingskonto skal du vælge afviklingskontoen til garantitransaktionen. 
10. Klik på Gem.
11. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]