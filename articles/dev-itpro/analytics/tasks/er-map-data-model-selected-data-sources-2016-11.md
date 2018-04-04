--- 
title: Tilknytte en datamodel til udvalgte datakilder til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan tilknytte en datamodel for elektronisk rapportering (ER) til valgte datakilder i Dynamics 365 for Finance and Operations, Enterprise edition (november 2016)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 13b7fe7f7bfe24bd275428e931993aa46ecb9945
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a>Tilknytte en datamodel til udvalgte datakilder til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan tilknytte en datamodel for elektronisk rapportering (ER) til valgte Dynamics 365 for Finance and Operations-datakilder. Denne modeltilknytning bruges senere som datakilde i en formatkonfiguration, der skal bruges til at administrere elektroniske betalingsdokumenter. I dette eksempel skal du tilknytte en datamodel for eksempelfirmaet Litware, Inc. til datakilder. For at fuldføre disse trin skal du først fuldføre trinnene i proceduren "Vælg datakilder til modeltilknytning".


## <a name="open-er-configurations-tree"></a>Åbn ER-konfigurationstræ
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Konfigurationer.

## <a name="select-created-model-mapping"></a>Vælg oprettet modeltilknytning
1. Vælg "Betalinger (forenklet mode)" i træet.
    * Kontrollér, at konfigurationen af modellen "Betalinger (forenklet model)" er oprettet på forhånd. Eller stop nu og vend tilbage efter du har fuldført opgaveguiden "Opret en ny konfiguration med det valgte domænes datamodel".  
2. Klik på Modeldesigner.
3. Klik på Tilknyt model til datakilde.
4. Vælg posten "CT-tilknytning".
    * CT-tilknytning  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Bind oprettede datakilder til datamodelelementer
1. Klik på Designer.
2. Vælg "Afviklingsdato og klokkeslæt(ProcessingDateTime)" i træet.
3. Vælg "Afviklingsdato(ProcessingDateTime)" i træet.
4. Klik på Bind.
5. Vælg "Identifikation for betalingsmeddelelse(MessageIdentification)" i træet.
6. Udvid "Transaktioner" i træet.
7. Vælg "Transaktioner\Journalbatchnummer(JournalNum)" i træet.
8. Klik på Bind.
9. Vælg "Betalinger" i træet.
10. Vælg "Transaktioner}" i træet.
11. Klik på Bind.
12. Udvid "Betalinger= Transaktioner" i træet.
13. Udvid "Betalinger= Transaktioner\Kreditor" i træet.
14. Udvid "Betalinger= Transaktioner\Kreditor\Konto" i træet.
15. Vælg "Betalinger= Transaktioner\Kreditor\Konto\Valutakode(Currency)" i træet.
16. Udvid "Transaktioner\vendBankAccountInTransactionCompany()" i træet.
17. Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)" i træet.
18. Klik på Bind.
19. Vælg "Betalinger= Transaktioner\Kreditor\Konto\IBAN-kode(IBAN)" i træet.
20. Vælg "Transaktioner\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)" i træet.
21. Klik på Bind.
22. Vælg "Betalinger= Transaktioner\Kreditor\Konto\Nummer" i træet.
23. Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Bankkontonummer(AccountNum)" i træet.
24. Klik på Bind.
25. Udvid "Betalinger= Transaktioner\Kreditor\Speditør" i træet.
26. Vælg "Betalinger= Transaktioner\Kreditor\Konto\Speditør\Navn" i træet.
27. Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Navn" i træet.
28. Klik på Bind.
29. Vælg "Betalinger = Transaktioner\Kreditor\Speditør\Registreringsnummer(RoutingNumber)" i træet.
30. Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Registreringsnummer(RegistrationNum)" i træet.
31. Klik på Bind.
32. Vælg "Betalinger= Transaktioner\Kreditor\Speditør\SWIFT-kode(SWIFT)" i træet.
33. Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Swift-kode/SWIFTNo)" i træet.
34. Klik på Bind.
35. Vælg "Betalinger= Transaktioner\Kreditor\Navn" i træet.
36. Udvid "Transaktioner\findVendTable()" i træet.
37. Vælg "Transaktioner\findVendTable()\ame()" i træet.
38. Klik på Bind.
39. Vælg "Betalinger= Transaktioner\Valutakode(Currency)" i træet.
40. Udvid "Transaktioner\>Relations" i træet.
41. Udvid "Transaktioner\>Relationer\Valutatabel(Currency)" i træet.
42. Vælg "Transaktioner\>Relationer\Valutatabel (Currency)\Valutakode(CurrencyCodeISO)" i træet.
43. Klik på Bind.
44. Udvid "Betalinger= Transaktioner\Debitor" i træet.
45. Udvid "Betalinger= Transaktioner\Debitor\Konto" i træet.
46. Vælg "Betalinger= Transaktioner\Debitor\Konto\Valutakode(Currency)" i træet.
47. Vælg "Bankkonto(BankAccount)" i træet.
48. Udvid "Bankkonto(BankAccount)" i træet.
49. Vælg "Bankkonto(BankAccount)\Valuta(CurrencyCode)" i træet.
50. Klik på Bind.
51. Vælg "Bankkonto(BankAccount)\IBAN" i træet.
52. Vælg "Betalinger= Transaktioner\Debitor\Konto\IBAN-kode(IBAN)" i træet.
53. Klik på Bind.
54. Vælg "Betalinger= Transaktioner\Debitor\Konto\Nummer" i træet.
55. Vælg "Bankkonto(BankAccount)\Bankkontonummer(AccountNum)" i træet.
56. Klik på Bind.
57. Udvid "Betalinger= Transaktioner\Debitor\Speditør" i træet.
58. Vælg "Betalinger= Transaktioner\Debitor\Speditør\Navn" i træet.
59. Vælg "Bankkonto(BankAccount)\Navn" i træet.
60. Klik på Bind.
61. Vælg "Betalinger = Transaktioner\Debitor\Speditør\Registreringsnummer(RoutingNumber)" i træet.
62. Vælg "Bankkonto(BankAccount)\Registreringsnummer(RegistrationNum)" i træet.
63. Klik på Bind.
64. Vælg "Betalinger= Transaktioner\Debitor\Speditør\SWIFT-kode(SWIFT)" i træet.
65. Vælg "Bankkonto(BankAccount)\SWIFT-kode(SWIFTNo)" i træet.
66. Klik på Bind.
67. Vælg "Betalinger= Transaktioner\Debitor\Navn" i træet.
68. Vælg 'Firmaoplysninger(Company)' i træet.
69. Udvid "Firmaoplysninger(Company)" i træet.
70. Vælg "Firmaoplysninger(Company)\Navn" i træet.
71. Klik på Bind.
72. Vælg "Betalinger= Transaktioner\Beskrivelse" i træet.
73. Vælg "Transaktioner\Beskrivelse(Txt)" i træet.
74. Klik på Bind.
75. Vælg "Betalinger= Transaktioner\Slutpunkt til slutpunkt-identifikationskode(End2EndID)" i træet".
76. Vælg "Transaktioner\$EndToEndID" i træet.
77. Klik på Bind.
78. Vælg "Betalinger= Transaktioner\Instrueret beløb(InstructedAmount)" i træet.
79. Vælg "Transaktioner\$Amount" i træet.
80. Klik på Bind.
81. Vælg "Betalinger= Transaktioner\Posteringsdato(TransactionDate)" i træet.
82. Vælg "Transaktioner\Dato(TransDate)" i træet.
83. Klik på Bind.

## <a name="validate-created-mapping"></a>Valider oprettet tilknytning
1. Klik på Valider.
    * Valider den nye tilknytning for at sikre, at alle bindinger er i orden.  
2. Klik på pilen for at vise eller skjule sektionen Fejlliste.
3. Klik på Gem.
4. Luk siden.
5. Luk siden.
6. Luk siden.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Ændr status for den aktuelle version af modelkonfiguration
1. Klik på Skift status.
    * Skift status for den designede modelkonfiguration – fra Kladde til Fuldført for at gøre den tilgængelig for oprettelse af betalingsformatdesign.  
2. Klik på Fuldført.
    * Vælg Fuldfør.  
3. Skriv en værdi i feltet Beskrivelse.
    * For eksempel "version 1".  
4. Klik på OK.
5. Vælg den færdige version af den aktuelle konfiguration.
    * Bemærk, at den oprettede konfiguration gemmes som fuldført version 1.  


