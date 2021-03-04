---
title: Garantier
description: Denne artikel indeholder oplysninger om garantier. I en garanti accepterer en bank at betale et bestemt pengebeløb til en person, hvis en af bankens kunder misligholder en betaling eller en forpligtelse til den pågældende person.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3dbf08679c165258a4a4027bf1cf73484d9efd3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441607"
---
# <a name="letters-of-guarantee"></a>Garantier

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om garantier. I en garanti accepterer en bank at betale et bestemt pengebeløb til en person, hvis en af bankens kunder misligholder en betaling eller en forpligtelse til den pågældende person. 

En garanti er en aftale med en bank (kautionisten) om at betale et angivet beløb til en anden person (beneficianten), hvis en banks kunde (hovedparten) misligholder en betaling eller en forpligtelse over for beneficianten. Garantier kan ikke overdrages. De gælder kun for den beneficiant, der er nævnt i aftalen. Hovedparten kan anmode om en forøgelse eller reducering af værdien af en garanti med forbehold for betingelserne i aftalen. 

Hvis du vil afvikle en garanti, skal beneficianten indsende den originale garanti og informere banken før udløbsdatoen. Derefter betaler banken det forfaldne beløb til beneficiantens konto i overensstemmelse med betingelserne i garantien. Banken hensætter en procentdel af betalingen som avance. Procentdelen aftales og angives i aftalens betingelser. 

Du kan oprette en kode, der sporer formålet med garantien. Du kan også angive de grunde, der kan være knyttet til garantien, når brevet er annulleret. Du kan se formålskoder og bankårsager på siderne **Betalingsformålskoder** og **Bankårsager**. 

Du kan bruge siden **Garanti** til at udføre disse opgaver:

-   Opret korrekte finansposter, og fjern manuelle indtastninger.
-   Registrer alle monetære og ikke-monetære transaktioner, og spor saldi i garantier.
-   Registrer og spor status og udløb for garantier.
-   Opret en rapport, der viser de banker, som ligger inde med garantier.

Nedenstående tabel indeholder beskrivelser af de handlinger, du kan for en garanti.

| Handling              | Formål                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| Send til bank      | Send garantianmodningen til banken.                                                                       |
| Modtag fra bank   | Når banken accepterer den sendte anmodning, skal du have garantien udleveret fra banken.                            |
| Giv til beneficianten | Når du modtager anmodningen fra banken, skal du levere garantien til beneficianten.              |
| øg værdien      | Hvis beneficianten og hovedparten er enige om det, kan den pengemæssige værdi øges.                                                  |
| Reducer værdien      | Hvis beneficianten og hovedparten er enige om det, kan den pengemæssige værdi reduceres.                                                  |
| Forlæng              | Når du leverer garantien til beneficianten, kan du forlænge gyldighedsperioden, hvis det er nødvendigt. |
| Annullér              | Når det formål, der var grundlag for anmodningen om garantien, ikke længere gælder, annulleres aftalen.                  |
| Udfør afvikling           | Når beneficianten overdrager garantien til banken, udbetales garantien.                      |


Du kan finde flere oplysninger under følgende emner:

[Garantipostering](tasks/letter-guarantee-transaction.md)

[Oprette posteringsprofiler for bankfaciliteter til garanti](tasks/set-up-bank-facilities-posting-profiles.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]