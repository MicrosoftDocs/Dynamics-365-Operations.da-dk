--- 
title: Oprette fremdaterede checks
description: "I dette emne beskrives, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d83713f9d54b396a10894995024ac1c8dd47a6f1
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-postdated-checks"></a>Oprette fremdaterede checks

[!include[task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger. Du kan også angive clearingkonti for udstedte kontrol, modtagne checks og A-skat. Fremdaterede checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato. Du kan angive, om checken skal afspejles i regnskaberne før dens forfaldsdato.



Rollen for denne procedure er Kasserer. Denne procedure bruger demofirmaet USMF.


## <a name="set-up-postdated-checks"></a>Oprette fremdaterede checks
1. Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre
2. Klik på fanen Fremdaterede checks.
3. Marker eller fjern markeringen af afkrydsningsfeltet Aktivér fremdaterede checks.
4. Marker eller fjern markeringen i afkrydsningsfeltet Bogfør kladdeposteringer for fremdaterede checks.
5. Angiv de ønskede værdier i feltet Clearingkonto til udstedte checks.
6. Angiv de ønskede værdier i feltet Clearingkonto til modtagne checks.
7. Skriv en værdi i feltet Finanskladde til clearingposteringer.
8. Skriv en værdi i feltet Overfør fremdaterede checks til denne kreditorbetalingskladde.
9. Angiv de ønskede værdier i feltet Clearingkonto til A-skat.
10. Klik på Gem.
11. Luk siden.
12. Gå til Kreditor > Opsætning af betaling > Betalingsmåder.
13. Klik på Ny.
14. Indtast en værdi i feltet Betalingsmåde.
15. Vælg indstillingen Bogføring af fremdateret checkclearing for at angive, at checkbeløbet bogføres på en clearingkonto.
16. Vælg "Bank" i feltet Kontotype.
    * Modkontoen for betalingsmetoden bliver en bank.  
17. I feltet Betalingskonto skal du specificere de ønskede værdier.
    * Vælg den bankkonto, der bruges til at fratrække fakturabeløbet.  
18. Luk siden.
19. Gå til Debitor > Opsætning af betaling > Betalingsmetoder
20. Klik på Ny.
21. Indtast en værdi i feltet Betalingsmåde.
22. Vælg indstillingen Bogføring af fremdateret checkclearing for at angive, at checkbeløbet bogføres på en clearingkonto.
23. Vælg "Bank" i feltet Kontotype.
    * Modkontoen for betalingsmetoden bliver en bank.  
24. I feltet Betalingskonto skal du specificere de ønskede værdier.
    * Vælg den bankkonto, der bruges til at fratrække fakturabeløbet.  
25. Luk siden.

