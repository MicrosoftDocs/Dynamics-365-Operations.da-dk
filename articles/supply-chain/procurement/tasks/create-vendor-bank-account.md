--- 
title: Oprette en bankkonto for kreditor
description: "Denne procedure viser dig, hvordan du skal oprette en bankkonto for en leverandør."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: adb759c59d7275e7323dbb760de56acdef2e3cff
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-bank-account"></a>Oprette en bankkonto for kreditor

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser dig, hvordan du skal oprette en bankkonto for en leverandør. Du kan bruge denne procedure i USMF-demodatafirmaet.

1. Gå til Indkøb og forsyning > Kreditorer > Alle kreditorer.
2. Vælg den kreditor, du vil oprette en bankkonto for, og klik derefter på linket på kreditors konto-id.
3. Klik på Kreditor i handlingsruden.
4. Klik på Bankkonti.
5. Klik på Ny.
6. Skriv en værdi i feltet Bankkonto.
    * Dette id bruges til at identificere bankkontoen på kreditorposten.  
7. Skriv en værdi i feltet Navn.
8. Indtast eller vælg en værdi i feltet Bankgrupper.
9. I feltet Registreringsnummertype skal du vælge en indstilling.
    * Det er den registreringsnummertype, der anvendes til internationale betalinger.  
10. Skriv en værdi i feltet Bankkontonummer.
11. Indtast en værdi i feltet SWIFT-kode.
12. Skriv en værdi i feltet IBAN.
    * IBAN-nummeret skal være i det korrekte format. Du kan f.eks. bruge DE89370400440532013000.  
    * Status for bankkontoen er Aktiv, hvis aktiv-datoen er nået, og udløbsdatoen ikke er overskredet. Den er også aktiv, hvis både feltet Aktiv-dato og feltet Udløbsdato er tomt. Hvis datoerne i både feltet Aktiv-dato og feltet Udløbsdato ligger i fremtiden, er elektroniske betalinger ikke tilgængelige. Andre betalingstyper er tilgængelige, og bankkontoen er aktiv.  
13. Udvid sektionen Konfiguration.
14. Indtast en værdi i feltet Tekstkode.
    * Dette felt angiver en kode, der vises på modtagerens bankkontoudtog.  
15. Skriv en værdi i feltet Meddelelse til bank.
16. Skriv en værdi i feltet Kursreference.
    * Det er referencenummeret til evt. termins- eller aftalekurs.  
17. Indtast eller vælg en værdi i feltet Valuta.
    * Når der udstedes adviseringer, indeholder dette afsnit en oversigt over deres status (ventende eller godkendt).  
18. Udvid sektionen Adresse.
19. Udvid afsnittet Adviseringer.
20. Udvid eller skjul sektionen Kontaktoplysninger.
21. Indtast en værdi i feltet Telefon.
22. Luk siden.
23. Klik på Rediger.
24. Vis sektionen Betaling.
25. Vælg den konto, du lige har oprettet, i feltet Bankkonto.
26. Klik på Gem.
    * Adressen kan være nedarvet fra bankgruppen, hvis der er angivet en, eller du kan tilføje den her.  


