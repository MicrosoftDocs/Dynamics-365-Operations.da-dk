---
title: Konfigurere indbetalingskortformat for projektfakturaer
description: Virksomheder vedhæfter normalt udskrevne indbetalingskort til fakturaer for at hjælpe kunderne og angive en betalingsreference til brug ved bogføring og betaling.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f32975a9ad6887a4396bdceb37b27a6f08ca30c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832438"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Konfigurere indbetalingskortformat for projektfakturaer

[!include [banner](../../includes/banner.md)]

Virksomheder vedhæfter normalt udskrevne indbetalingskort til fakturaer for at hjælpe kunderne og angive en betalingsreference til brug ved bogføring og betaling. Indbetalingskortet kan bruges til projekt- eller servicefakturaer, rykkere, rentenotaer og kontoopgørelser samt til salgsfakturaer og fritekstfakturaer. For at generere indbetalingskort skal du først oprette et kreditor-id-nummer og formater for vedhæftningen af indbetalingskortet.

Denne procedure bruger demofirmaet DEMF. 

Denne funktionalitet er kun tilgængelig for juridiske enheder, hvis primære adresse er i Danmark.


## <a name="set-up-a-creditor-id-number"></a>Oprette et kreditor-id-nummer
1. Gå til Virksomhedsadministration > Organisationer > Juridiske enheder.
2. Udvid eller skjul sektionen Bankkontooplysninger.
3. Klik på Rediger.
4. Skriv en værdi i feltet FI-kreditor-id.
5. Klik på Gem.
6. Luk siden.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Oprette et indbetalingskortformat for debitorer, notaer, rykkere og opgørelser
1. Gå til Debitor > Opsætning > Formularer > Formularopsætning.
2. Klik på fanen Faktura.
3. Vælg en indstilling i feltet Tilknyttet betalingsbilag på debitorfaktura.
    * Ingen – Udskriv ikke et indbetalingskort. Vælg denne indstilling, hvis indbetalingsbeløbet er i en anden valuta end danske kroner (DKK).   FIK 751 – Udskriv et FIK 751-indbetalingskort, hvis du har tænkt dig at skrive betalingsbeløbet og forfaldsdatoen på indbetalingskortet i hånden.   FIK 752 – Udskriv et FIK 752-indbetalingskort, hvis du har tænkt dig at bruge et computergenereret indbetalingskort, hvor betalingsbeløb og forfaldsdato er fortrykt.  
4. Klik på Gem.
5. Klik på fanen Fritekstfaktura.
6. Vælg en indstilling i feltet Tilknyttet betalingsbilag på fritekstfaktura.
    * Ingen – Udskriv ikke et indbetalingskort. Vælg denne indstilling, hvis indbetalingsbeløbet er i en anden valuta end danske kroner (DKK).   FIK 751 – Udskriv et FIK 751-indbetalingskort, hvis du har tænkt dig at skrive betalingsbeløbet og forfaldsdatoen på indbetalingskortet i hånden.   FIK 752 – Udskriv et FIK 752-indbetalingskort, hvis du har tænkt dig at bruge et computergenereret indbetalingskort, hvor betalingsbeløb og forfaldsdato er fortrykt.  
7. Klik på Gem.
8. Klik på fanen Rentenota.
9. Vælg en indstilling i feltet Tilknyttet betalingsbilag på rentenota.
    * Ingen – Udskriv ikke et indbetalingskort. Vælg denne indstilling, hvis indbetalingsbeløbet er i en anden valuta end danske kroner (DKK).   FIK 751 – Udskriv et FIK 751-indbetalingskort, hvis du har tænkt dig at skrive betalingsbeløbet og forfaldsdatoen på indbetalingskortet i hånden.   FIK 752 – Udskriv et FIK 752-indbetalingskort, hvis du har tænkt dig at bruge et computergenereret indbetalingskort, hvor betalingsbeløb og forfaldsdato er fortrykt.  
10. Klik på Gem.
11. Klik på fanen Rykker.
12. Vælg en indstilling i feltet Tilknyttet betalingsbilag på rykker.
    * Ingen – Udskriv ikke et indbetalingskort. Vælg denne indstilling, hvis indbetalingsbeløbet er i en anden valuta end danske kroner (DKK).   FIK 751 – Udskriv et FIK 751-indbetalingskort, hvis du har tænkt dig at skrive betalingsbeløbet og forfaldsdatoen på indbetalingskortet i hånden.   FIK 752 – Udskriv et FIK 752-indbetalingskort, hvis du har tænkt dig at bruge et computergenereret indbetalingskort, hvor betalingsbeløb og forfaldsdato er fortrykt.  
13. Klik på Gem.
14. Klik på fanen Kontoudtog.
15. Vælg en indstilling i feltet Tilknyttet betalingsbilag på kontoudtog.
    * Ingen – Udskriv ikke et indbetalingskort. Vælg denne indstilling, hvis indbetalingsbeløbet er i en anden valuta end danske kroner (DKK).   FIK 751 – Udskriv et FIK 751-indbetalingskort, hvis du har tænkt dig at skrive betalingsbeløbet og forfaldsdatoen på indbetalingskortet i hånden.   FIK 752 – Udskriv et FIK 752-indbetalingskort, hvis du har tænkt dig at bruge et computergenereret indbetalingskort, hvor betalingsbeløb og forfaldsdato er fortrykt.  
16. Klik på Gem.
17. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]