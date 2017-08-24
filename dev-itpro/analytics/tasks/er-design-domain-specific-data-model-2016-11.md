--- 
title: "Designe en domænespecifik datamodel til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en datamodel til dokumenter til elektronisk betaling."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bf727b63ed86e7cc26d4fca630d97af88abb1804
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a>Designe en domænespecifik datamodel til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en datamodel til dokumenter til elektronisk betaling. Denne datamodel bruges senere som en datakilde, når du har oprettet formatet for betalingsdokumenterne.



I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer. Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Vælg konfigurationsudbyderen for eksempelvirksomheden, Litware, Inc. Hvis konfigurationsudbyderen ikke vises, skal du først fuldføre trinnene i proceduren "Oprette en konfigurationsudbyder og markere den som aktiv".  
2. Klik på Rapporteringskonfigurationer.
    * Du skal oprette en konfiguration, der indeholder en datamodel for dokumenter til elektronisk betaling. Denne datamodel bruges senere som en datakilde, når du har oprettet formatet for betalingsdokumenterne.  

## <a name="create-a-new-data-model-configuration"></a>Opret en ny datamodelkonfiguration
1. Klik på Opret konfiguration for at åbne dialogboksen.
2. Skriv "Betalinger (forenklet model)" i feltet Navn.
    * Betalinger (forenklet model)  
3. Skriv "Betalingsmodelkonfiguration" i feltet Beskrivelse.
    * Betalingsmodelkonfiguration  
    * Den aktive konfigurationsudbyder indsættes automatisk her. Denne udbyder vil kunne vedligeholde denne konfiguration. Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.  
4. Klik på "Opret konfiguration" for at fuldføre oprettelsen af konfigurationsopgaven

## <a name="create-a-data-model"></a>Opret en datamodel
    * Du er ved at oprette en ny datamodel for den valgte konfiguration. Denne konfigurationsversion får statussen Kladde.  
1. Klik på Designer.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Definer strukturen af en part, der deltager i en betalingsproces
1. Klik på Ny for at åbne dialogboksen Fjern.
2. Skriv "Part" i feltet Navn.
    * Part  
3. Klik på Tilføj.
4. Klik på Ny for at åbne dialogboksen Fjern.
5. Skriv "Navn" i feltet Navn.
    * Navn  
6. Vælg "Streng" i feltet Varetype.
7. Klik på Tilføj.
8. Skriv "Part" i feltet Søg.
    * Part  
9. Klik på Find forrige.

## <a name="define-the-bank-structure-for-this-model"></a>Definer bankstrukturen for denne model
1. Klik på Ny for at åbne dialogboksen Fjern.
2. Skriv "Agent" i feltet Navn.
    * Speditør  
3. Vælg "Post" i feltet Varetype.
4. Klik på Tilføj.
5. Angiv "Pengeinstitut (f.eks. bank), der servicerer en konto for parten (debitor/kreditor)" i feltet Beskrivelse.
    * Pengeinstitut (f.eks. bank), der servicerer en konto for parten (debitor/kreditor).  
6. Klik på Ny for at åbne dialogboksen Fjern.
7. Skriv "Navn" i feltet Navn.
    * Navn  
8. Vælg "Streng" i feltet Varetype.
9. Klik på Tilføj.
10. Klik på Ny for at åbne dialogboksen Fjern.
11. Skriv "SWIFT" i feltet Navn.
    * SWIFT  
12. Klik på Tilføj.
13. Skriv "Bankens identifikationskode" i feltet Beskrivelse.
    * Bankens identifikationskode  
14. Klik på Ny for at åbne dialogboksen Fjern.
15. Skriv "RoutingNumber" i feltet Navn.
    * RoutingNumber  
16. Klik på Tilføj.
17. Skriv "Registreringsnummer" i feltet Beskrivelse.
    * Registreringsnummer  
18. Klik på Find forrige.

## <a name="define-the-bank-account-structure-for-this-model"></a>Definer bankkontostrukturen for denne model
1. Klik på Ny for at åbne dialogboksen Fjern.
2. Skriv "Konto" i feltet Navn.
    * Konto  
3. Vælg "Post" i feltet Varetype.
4. Klik på Tilføj.
5. Skriv "Identifikation af en parts konto i et pengeinstitut (f.eks. en bank)." i feltet Beskrivelse.
    * Identifikation af en parts konto i et pengeinstitut (f.eks. en bank).  
6. Klik på Ny for at åbne dialogboksen Fjern.
7. Skriv "Valuta" feltet Navn.
    * Valuta  
8. Vælg "Streng" i feltet Varetype.
9. Klik på Tilføj.
10. Indtast "Valutakode" i feltet Beskrivelse.
    * Valutakode  
11. Klik på Ny for at åbne dialogboksen Fjern.
12. Skriv "Tal" i feltet Navn.
    * Tal  
13. Klik på Tilføj.
14. Klik på Ny for at åbne dialogboksen Fjern.
15. Skriv "IBAN" i feltet Navn.
    * IBAN  
16. Klik på Tilføj.
17. Skriv "Internationalt bankkontonummer" i feltet Beskrivelse.
    * Internationalt bankkontonummer  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Definer betalingsmeddelelsesstruktur for overførsel af kundekredittype.
1. Klik på Ny for at åbne dialogboksen Fjern.
2. Skriv "Modelrod" i feltet Ny node som felt.
3. Skriv "CustomerCreditTransferInitiation" i feltet Navn.
    * Vælg CustomerCreditTransferInitiation  
4. Klik på Tilføj.
5. Skriv "CustomerCreditTransferInitiation" i feltet Søg.
    * Vælg CustomerCreditTransferInitiation  
6. Klik på Find forrige.
7. Klik på Ny for at åbne dialogboksen Fjern.
8. Skriv "MessageIdentification" i feltet Navn.
    * MessageIdentification  
9. Klik på Tilføj.
10. Angiv "Punkt til punkt-referencen, som tildelt af den instruerende part (og sendt til den næste part) for at identificere en meddelelse." i feltet Beskrivelse.
    * Punkt til punkt-referencen, som tildelt af den instruerende part (og sendt til den næste part) for at identificere en meddelelse.  
11. Klik på Ny for at åbne dialogboksen Fjern.
12. Skriv "ProcessingDateTime" i feltet Navn.
    * ProcessingDateTime  
13. Vælg "DateTime" i feltet Varetype.
14. Klik på Tilføj.
15. Angiv "Dato og klokkeslæt, hvor betalingsmeddelelsen blev oprettet." i feltet Beskrivelse.
    * Dato og klokkeslæt, hvor betalingsmeddelelsen blev oprettet.  
16. Klik på Ny for at åbne dialogboksen Fjern.
    * Definer betalingstransaktionen for denne model.  
17. Skriv "Betalinger" i feltet Navn.
    * Betalinger  
18. Vælg "Liste over poster" i feltet Varetype.
19. Klik på Tilføj.
20. Angiv "Betalingslinjer for den aktuelle meddelelse" i feltet Navn.
    * Betalingslinjer for den aktuelle meddelelse  
21. Klik på Ny for at åbne dialogboksen Fjern.
22. Skriv "Kreditor" i feltet Navn.
    * Kreditor  
23. Vælg "Post" i feltet Varetype.
24. Klik på Tilføj.
25. Angiv "Part, til hvem et beløb er forfaldent." i feltet Beskrivelse.
    * Part, til hvem et beløb er forfaldent.  
26. Klik på Skift varereference.
27. Skriv "Part" i feltet Søg.
    * Part  
28. Klik på Find næste.
29. Klik på OK.
30. Skriv "Betalinger" i feltet Søg.
    * Betalinger  
31. Klik på Find næste.
32. Klik på Ny for at åbne dialogboksen Fjern.
33. Skriv "Debitor"i feltet Navn.
    * Debitor  
34. Klik på Tilføj.
35. Angiv "Part, der skylder et beløb til (den endelige) kreditor." i feltet Beskrivelse.
    * Part, der skylder et beløb til (den endelige) kreditor.  
36. Klik på Skift varereference.
37. Skriv "Part" i feltet Søg.
    * Part  
38. Klik på Find næste.
39. Klik på OK.
40. Klik på Find næste.
41. Klik på Ny for at åbne dialogboksen Fjern.
42. Skriv "Beskrivelse" i feltet Navn.
    * Betegnelse  
43. Vælg "Streng" i feltet Varetype.
44. Klik på Tilføj.
45. Klik på Ny for at åbne dialogboksen Fjern.
46. Skriv "Valuta" feltet Navn.
    * Valuta  
47. Klik på Tilføj.
48. Indtast "Valutakode" i feltet Beskrivelse.
    * Valutakode  
49. Klik på Ny for at åbne dialogboksen Fjern.
50. Angiv "TransactionDate" i feltet Navn.
    * TransactionDate  
51. Vælg "Dato" i feltet Varetype.
52. Klik på Tilføj.
53. Angiv "Posteringsdato" i feltet Beskrivelse.
    * Posteringsdato  
54. Klik på Ny for at åbne dialogboksen Fjern.
55. Skriv "InstructedAmount" i feltet Navn.
    * InstructedAmount  
56. Vælg "Kommatal" i feltet Varetype.
57. Klik på Tilføj.
58. Angiv "Det beløb, der skal flyttes mellem debitor og kreditor, før fratrækning af gebyrer" i feltet Beskrivelse. Beløbet skal angives i den valuta, som bestilt af den startende part.
    * Det beløb, der skal flyttes mellem debitor og kreditor, før fratrækning af gebyrer. Beløbet skal angives i den valuta, som bestilt af den startende part.  
59. Klik på Ny for at åbne dialogboksen Fjern.
60. Skriv "End2EndID" i feltet Navn.
    * End2EndID  
61. Vælg "Streng" i feltet Varetype.
62. Klik på Tilføj.
63. Angiv "Den entydige identifikation, der er tildelt af den startende part" i feltet Beskrivelse. Denne identifikation overføres, uændret, i hele slutpunkt til slutpunkt-kæden.
    * Den entydige identifikation, der er tildelt af den startende part. Denne identifikation overføres, uændret, i hele slutpunkt til slutpunkt-kæden.  
64. Skriv "PaymentModel" i feltet Navn.
    * Navnet på PaymentModel justeres med foruddefinerede grænseflader for betalingsformer.  
65. Klik på Gem.
66. Luk siden.


