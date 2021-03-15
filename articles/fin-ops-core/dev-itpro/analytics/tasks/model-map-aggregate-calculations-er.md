---
title: Bruge modeltilknytningskonfiguration til samlede beregninger på databaseniveau
description: Dette emne beskriver, hvordan du kan designe en ny modeltilknytningskonfiguration til elektronisk rapportering og bruge indbyggede ER-funktioner til effektive samlede beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a392697f6b91bc6555d0d72d09ecd7da32e1a3f
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094259"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Bruge modeltilknytningskonfiguration til samlede beregninger på databaseniveau

[!include [banner](../../includes/banner.md)]

Denne procedure indeholder oplysninger om, hvordan du designer en ny modeltilknytningskonfiguration til elektronisk rapportering (ER) og bruger indbyggede ER-funktioner til effektive samlede beregninger. I denne procedure skal du oprette en konfiguration til eksempelfirmaet Litware, Inc. 

Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af ethvert datasæt.

 For at fuldføre disse trin, skal du først fuldføre trinnene i proceduren "ER forbedrer effektiviteten ved samlede beregninger ved at udføre dem på databaseniveau (Del 1: Forbered konfigurationer)".

1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Intrastat-model' i træet.
3. Vælg 'Intrastat-model\Intrastat-eksempeltilknytning' i træet.
4. Klik på Designer.
5. Klik på Designer.
6. Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.
7. Klik på Tilføj rod.
    * Tilføj en ny datakilde, der repræsenterer poster, du vil gruppere.  
8. Skriv "Transaktioner" i feltet Navn.
    * Poster  
9. Skriv "Intrastat" i feltet Tabel.
    * Intrastat  
10. Klik på OK.
11. Vælg 'Funktioner\Gruppér efter' i træet.
    * Denne datakildetype bruges til at introducere en ny datakilde på kørselstidspunktet til at gruppere poster og beregne de krævede summeringer.  
12. Klik på Tilføj rod.
13. Skriv 'TransactionsGroups' i feltet Navn.
    * TransactionsGroups  
14. Klik på Rediger gruppe efter.
15. Vælg "Transaktioner" i træet.
    * Vælg den tilføjede datakilde af typen 'Liste over poster', der repræsenterer de poster, du vil gruppere.  
16. Klik på Tilføj et felt til.
17. Klik på Hvad skal grupperes.
18. Udvid "Transaktioner" i træet.
19. Vælg "Transaktioner\Retning" i træet.
20. Klik på Tilføj et felt til.
21. Klik på Grupperede felter.
    * Marker feltet for at angive grupperingsniveauet. Ud fra dette valg returnerer datakilden på kørselstidspunktet så mange grupper af transaktioner, som der er retningskoder, der vil blive opfyldt i Intrastat-tabellen.  
22. Vælg 'Transaktioner\Fakturabeløb(AmountMST)' i træet.
    * Marker feltet for at angive kilden til beregning af aggregering.  
23. Klik på Tilføj et felt til.
24. Klik på Aggregeringsfelter.
25. Markér den valgte række på listen.
26. Vælg 'Sum' i feltet Metode.
    * Vælg aggregeringstypen.  
27. Skriv 'SumOfAmountMST' i feltet Navn.
    * Angiv navnet på denne aggregering i datakilden, der er konfigureret.  
28. Klik på Gem.
    * Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i SQL-databasen.  
29. Luk siden.
30. Klik på OK.
31. Udvid "Totaler" i træet.
32. Udvid 'TransactionsGroups' i træet.
33. Udvid "TransactionsGroups\aggregerede" i træet.
34. Vælg 'TransactionsGroups\aggregerede\SumOfAmountMST' i træet.
35. Vælg 'Totaler\Fakturaværdi i alt(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.
36. Klik på Bind.
    * Baseret på denne indstilling vil denne datakilde beregne summen af værdierne i feltet 'AmountMST' for de enkelte grupper af transaktioner. Denne aggregeringsberegning vil være tilgængelig som elementet TransactionsGroups.aggregated.TotalAmount.  
37. Udvid 'TransactionsGroups' i træet.
38. Vælg "TransactionsGroups" i træet.
39. Klik på Rediger.
40. Klik på Rediger gruppe efter.
41. Udvid "Transaktioner" i træet.
42. Vælg 'Transaktioner\Fakturabeløb(AmountMST)' i træet.
43. Klik på Tilføj et felt til.
44. Klik på Aggregeringsfelter.
45. Markér den valgte række på listen.
46. Vælg 'Maks.' i feltet Metode.
47. Skriv 'MaxOfAmountMST' i feltet Navn.
48. Klik på Gem.
    * Udførelse af GROUPBY-datakilder kan på nuværende tidspunkt oversættes til SQL-databaseniveauet med visse begrænsninger. Oversættelsen kan foretages for begge datakilder af typen 'Liste over poster' eller for datakilder, der er repræsenteret som et udtryk, der bruger funktionen FILTER. Den kan også udføres, når kun én sammenlægning er konfigureret til et enkelt felt i grupperingsposterne.  
    * Bemærk, at selvom der var konfigureret mere end én aggregering til feltet AmountMST, angiver feltet 'Udførelse' stadig, at denne gruppering udføres på kørselstidspunktet i SQL-databasen. Det skyldes, at kun én aggregering er bundet til datamodelelementet, og det bruges på kørselstidspunktet til at hente data fra denne datakilde.  
49. Luk siden.
50. Klik på OK.
51. Udvid 'TransactionsGroups' i træet.
52. Udvid "TransactionsGroups\aggregerede" i træet.
53. Vælg 'TransactionsGroups\aggregerede\MaxOfAmountMST' i træet.
54. Vælg 'Totaler\Total statistisk værdi(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.
55. Klik på Bind.
56. Udvid 'TransactionsGroups' i træet.
57. Vælg "TransactionsGroups" i træet.
58. Klik på Rediger.
59. Klik på Rediger gruppe efter.
    * Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i hukommelsen, fordi begge aggregeringer af det samme felt er bundet til datamodelelementerne.   
60. Markér eller fjern markeringen af alle rækker på listen.
61. Klik på Slet.
62. Klik på Ja.
63. Klik på Slet.
64. Klik på Ja.
65. Klik på Tilføj et felt til.
66. Klik på Hvad skal grupperes.
67. Udvid 'Varepost(Intrastat)' i træet.
68. Klik på Gem.
    * Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i hukommelsen, selv om der er ikke defineret nogen aggregeringer, og den valgte datakilde af typen 'Tabelposter' refererer til samme 'Intrastat'-tabel. Det skyldes, at datakilden indeholder nogle beregnede felter, som endnu ikke kan oversættes til SQL-databaseniveauet.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]