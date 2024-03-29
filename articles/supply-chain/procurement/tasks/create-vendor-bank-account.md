---
title: Oprette en bankkonto for kreditor
description: Denne procedure viser dig, hvordan du skal oprette en bankkonto for en leverandør.
author: GalynaFedorova
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b201f5eb2bf8eb496a761b6fc6ca729a46a85ce
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677836"
---
# <a name="create-a-vendor-bank-account"></a>Oprette en bankkonto for kreditor

[!include [banner](../../includes/banner.md)]

Denne procedure viser dig, hvordan du skal oprette en bankkonto for en leverandør. Du kan bruge denne procedure i USMF-demodatafirmaet.

1. Gå til **navigationsruden > Moduler > Indkøb og forsyning > Kreditorer > Alle kreditorer**.
2. Vælg den kreditor, du vil oprette en bankkonto for, og klik derefter på linket i feltet **Kreditors konto-id**.
3. Klik på **Krediter** i **Handlingsrude**.
4. Klik på **Bankkonti**.
5. Klik på **Ny** i **handlingsruden**.
6. Skriv en værdi i feltet **Bankkonto**. Dette id bruges til at identificere bankkontoen på kreditorposten.  
7. Skriv en værdi i feltet **Navn**.
8. Indtast eller vælg en værdi i feltet **Bankgrupper**.
9. I feltet **Registreringsnummertype** skal du vælge en indstilling. Det er den registreringsnummertype, der anvendes til internationale betalinger.  
10. Skriv en værdi i feltet **Bankkontonummer**.
11. Indtast en værdi i feltet **SWIFT-kode**.
12. Skriv en værdi i feltet **IBAN**.
    - IBAN-nummeret skal være i det korrekte format. Du kan f.eks. bruge DE89370400440532013000.  
    - Status for bankkontoen er Aktiv, hvis aktiv-datoen er nået, og udløbsdatoen ikke er overskredet. Den er også aktiv, hvis både feltet Aktiv-dato og feltet Udløbsdato er tomt. Hvis datoerne i både feltet Aktiv-dato og feltet Udløbsdato ligger i fremtiden, er elektroniske betalinger ikke tilgængelige. Andre betalingstyper er tilgængelige, og bankkontoen er aktiv.  
13. Udvid sektionen **Konfiguration**.
14. Indtast en værdi i feltet **Tekstkode**. Dette felt angiver en kode, der vises på modtagerens bankkontoudtog.  
15. Skriv en værdi i feltet **Meddelelse til bank**.
16. Skriv en værdi i feltet **Kursreference**. Det er referencenummeret til evt. termins- eller aftalekurs.
17. Indtast eller vælg en værdi i feltet **Valuta**. Når der udstedes adviseringer, indeholder dette afsnit en oversigt over deres status (ventende eller godkendt).  
18. Udvid sektionen **Adresse**.
19. Udvid afsnittet **Adviseringer**.
20. Udvid sektionen **Kontaktoplysninger**.
21. Indtast en værdi i feltet **Telefon**.
22. Luk siden.
23. Klik på **Rediger**.
24. Vis sektionen **Betaling**.
25. Vælg den konto, du lige har oprettet, i feltet **Bankkonto**.
26. Klik på **Gem**. Adressen kan være nedarvet fra bankgruppen, hvis der er angivet en, eller du kan tilføje den her.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]