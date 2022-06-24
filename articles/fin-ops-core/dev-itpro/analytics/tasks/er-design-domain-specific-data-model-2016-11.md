---
title: Design ER-domænespecifik datamodel
description: Denne artikel beskriver, hvordan du opretter en ny ER-konfiguration (elektronisk rapportering), der indeholder en datamodel til elektroniske betalingsdokumenter.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c923ed6ec817d1f4ae6cd956c06b2156a6a61311
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908436"
---
# <a name="er-design-domain-specific-data-model"></a>Design ER-domænespecifik datamodel

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en datamodel til dokumenter til elektronisk betaling. Denne datamodel bruges senere som en datakilde, når du har oprettet formatet for betalingsdokumenterne.

I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer. Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.

    Vælg konfigurationsudbyderen for eksempelvirksomheden, 'Litware, Inc'. Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".  
    
2. Klik på Rapporteringskonfigurationer.

    Du skal oprette en konfiguration, der indeholder en datamodel for dokumenter til elektronisk betaling. Denne datamodel bruges senere som en datakilde, når du har oprettet formatet for betalingsdokumenterne.  

## <a name="create-a-new-data-model-configuration"></a>Opret en ny datamodelkonfiguration
1. Klik på Opret konfiguration for at åbne dialogboksen.
2. Skriv "Betalinger (forenklet model)" i feltet Navn.
3. Skriv "Betalingsmodelkonfiguration" i feltet Beskrivelse.

    Den aktive konfigurationsudbyder indsættes automatisk her. Denne udbyder vil kunne vedligeholde denne konfiguration. Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.  

4. Klik på "Opret konfiguration" for at fuldføre oprettelsen af konfigurationsopgaven

## <a name="create-a-data-model"></a>Opret en datamodel
Du er ved at oprette en ny datamodel for den valgte konfiguration. Denne konfigurationsversion får statussen Kladde.  
1. Klik på Designer.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Definer strukturen af en part, der deltager i en betalingsproces
1. Klik på Ny for at åbne dialogboksen Fjern.
2. Skriv "Part" i feltet Navn.
3. Klik på Tilføj.
4. Klik på Ny for at åbne dialogboksen Fjern.
5. Skriv "Navn" i feltet Navn.
6. Vælg "Streng" i feltet Varetype.
7. Klik på Tilføj.
8. Skriv "Part" i feltet Søg.
9. Klik på Find forrige.

## <a name="define-the-bank-structure-for-this-model"></a>Definer bankstrukturen for denne model
1. Klik på Ny for at åbne dialogboksen Fjern.
2. Skriv "Agent" i feltet Navn.
3. Vælg "Post" i feltet Varetype.
4. Klik på Tilføj.
5. Angiv "Pengeinstitut (f.eks. bank), der servicerer en konto for parten (debitor/kreditor)" i feltet Beskrivelse.

    Pengeinstitut (f.eks. bank), der servicerer en konto for parten (debitor/kreditor).  

6. Klik på Ny for at åbne dialogboksen Fjern.
7. Skriv "Navn" i feltet Navn. 
8. Vælg "Streng" i feltet Varetype.
9. Klik på Tilføj.
10. Klik på Ny for at åbne dialogboksen Fjern.
11. Skriv "SWIFT" i feltet Navn.
12. Klik på Tilføj.
13. Skriv "Bankens identifikationskode" i feltet Beskrivelse. 
14. Klik på Ny for at åbne dialogboksen Fjern.
15. Skriv "RoutingNumber" i feltet Navn.
16. Klik på Tilføj.
17. Skriv "Registreringsnummer" i feltet Beskrivelse.
18. Klik på Find forrige.

## <a name="define-the-bank-account-structure-for-this-model"></a>Definer bankkontostrukturen for denne model
1. Klik på Ny for at åbne dialogboksen Fjern.
2. Skriv "Konto" i feltet Navn. 
3. Vælg "Post" i feltet Varetype.
4. Klik på Tilføj.
5. Skriv "Identifikation af en parts konto i et pengeinstitut (f.eks. en bank)." i feltet Beskrivelse.

    Identifikation af en parts konto i et pengeinstitut (f.eks. en bank).  

6. Klik på Ny for at åbne dialogboksen Fjern.
7. Skriv "Valuta" feltet Navn. 
8. Vælg "Streng" i feltet Varetype.
9. Klik på Tilføj.
10. Indtast "Valutakode" i feltet Beskrivelse.
11. Klik på Ny for at åbne dialogboksen Fjern.
12. Skriv "Tal" i feltet Navn. 
13. Klik på Tilføj.
14. Klik på Ny for at åbne dialogboksen Fjern.
15. Skriv "IBAN" i feltet Navn. 
16. Klik på Tilføj.
17. Skriv "Internationalt bankkontonummer" i feltet Beskrivelse.

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Definer betalingsmeddelelsesstruktur for overførsel af kundekredittype.
1. Klik på Ny for at åbne dialogboksen Fjern.
2. Skriv "Modelrod" i feltet Ny node som felt.
3. Skriv "CustomerCreditTransferInitiation" i feltet Navn.
4. Klik på Tilføj.
5. Skriv "CustomerCreditTransferInitiation" i feltet Søg. 
6. Klik på Find forrige.
7. Klik på Ny for at åbne dialogboksen Fjern.
8. Skriv "MessageIdentification" i feltet Navn. 
9. Klik på Tilføj.
10. Angiv "Punkt til punkt-referencen, som tildelt af den instruerende part (og sendt til den næste part) for at identificere en meddelelse." i feltet Beskrivelse.

    Punkt til punkt-referencen, som tildelt af den instruerende part (og sendt til den næste part) for at identificere en meddelelse.  

11. Klik på Ny for at åbne dialogboksen Fjern.
12. Skriv "ProcessingDateTime" i feltet Navn.
13. Vælg "DateTime" i feltet Varetype.
14. Klik på Tilføj.
15. Angiv "Dato og klokkeslæt, hvor betalingsmeddelelsen blev oprettet." i feltet Beskrivelse. 
16. Klik på Ny for at åbne dialogboksen Fjern.

    Definer betalingstransaktionen for denne model.  

17. Skriv "Betalinger" i feltet Navn.
18. Vælg "Liste over poster" i feltet Varetype.
19. Klik på Tilføj.
20. Angiv "Betalingslinjer for den aktuelle meddelelse" i feltet Navn.
21. Klik på Ny for at åbne dialogboksen Fjern.
22. Skriv "Kreditor" i feltet Navn. 
23. Vælg "Post" i feltet Varetype.
24. Klik på Tilføj.
25. Angiv "Part, til hvem et beløb er forfaldent." i feltet Beskrivelse. 
26. Klik på Skift varereference.
27. Skriv "Part" i feltet Søg.
28. Klik på Find næste.
29. Klik på OK.
30. Skriv "Betalinger" i feltet Søg.
31. Klik på Find næste.
32. Klik på Ny for at åbne dialogboksen Fjern.
33. Skriv "Debitor"i feltet Navn. 
34. Klik på Tilføj.
35. Angiv "Part, der skylder et beløb til (den endelige) kreditor." i feltet Beskrivelse.
36. Klik på Skift varereference.
37. Skriv "Part" i feltet Søg.
38. Klik på Find næste.
39. Klik på OK.
40. Klik på Find næste.
41. Klik på Ny for at åbne dialogboksen Fjern.
42. Skriv "Beskrivelse" i feltet Navn.
43. Vælg "Streng" i feltet Varetype.
44. Klik på Tilføj.
45. Klik på Ny for at åbne dialogboksen Fjern.
46. Skriv "Valuta" feltet Navn.
47. Klik på Tilføj.
48. Indtast "Valutakode" i feltet Beskrivelse.
49. Klik på Ny for at åbne dialogboksen Fjern.
50. Angiv "TransactionDate" i feltet Navn. 
51. Vælg "Dato" i feltet Varetype.
52. Klik på Tilføj.
53. Angiv "Posteringsdato" i feltet Beskrivelse. 
54. Klik på Ny for at åbne dialogboksen Fjern.
55. Skriv "InstructedAmount" i feltet Navn.  
56. Vælg "Kommatal" i feltet Varetype.
57. Klik på Tilføj.
58. Angiv "Det beløb, der skal flyttes mellem debitor og kreditor, før fratrækning af gebyrer" i feltet Beskrivelse. Beløbet skal angives i den valuta, som bestilt af den startende part.

    Det beløb, der skal flyttes mellem debitor og kreditor, før fratrækning af gebyrer. Beløbet skal angives i den valuta, som bestilt af den startende part.  

59. Klik på Ny for at åbne dialogboksen Fjern.
60. Skriv "End2EndID" i feltet Navn. 
61. Vælg "Streng" i feltet Varetype.
62. Klik på Tilføj.
63. Angiv "Den entydige identifikation, der er tildelt af den startende part" i feltet Beskrivelse. Denne identifikation overføres, uændret, i hele slutpunkt til slutpunkt-kæden. 
64. Skriv "PaymentModel" i feltet Navn.

    Navnet på PaymentModel justeres med foruddefinerede grænseflader for betalingsformer.  

65. Klik på Gem.
66. Luk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
