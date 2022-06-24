---
title: Oprette fremdaterede checks
description: Denne artikel beskriver, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e045648230aba7965ed68fbc499f73e077caceed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870301"
---
# <a name="set-up-postdated-checks"></a>Oprette fremdaterede checks

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger. Du kan også angive clearingkonti for udstedte kontrol, modtagne checks og A-skat. Fremdaterede checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato. Du kan angive, om checken skal afspejles i regnskaberne før dens forfaldsdato.



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
18. Klik på Gem.
19. Luk siden.
> [!NOTE]
> Hvis du vil kunne bogføre en fremdateret check på en bankkonto, når sessionsdatoen er større end eller lig med forfaldsdatoen, skal du aktivere funktionen **Forfaldsdatovalidering af bogføring af betalingskladde med fremdaterede checks på bankkontoen**. Denne funktion giver dig mulighed for at bogføre betalingskladder for kreditorer eller debitorer med fremdaterede checks, når sessionsdatoen er større end eller lig med forfaldsdatoen.
> 
> Når du angiver **Betalingsmåde** (**Kreditor > Opsætning af betaling > Betalingsmåder**), skal du ikke udfylde **Mellemkonto**. I dette tilfælde udfyldes modkontoen med den bankkonto, der er angivet i **Betalingsmåde**.
>  
> Når funktionen er aktiveret, og sessionsdatoen er mindre end forfaldsdatoen, vises følgende fejlmeddelelse, når du bogfører en betalingskladde "Forfaldsdato skal være mindre eller lig med sessionsdatoen, hvis modkontotypen er Bank". Hvis funktionen ikke er aktiveret, kan du bogføre en betalingskladde med en fremdateret check, når sessionsdatoen er mindre end forfaldsdatoen.
> Denne funktion er tilgængelig i version 10.0.21 eller nyere.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
