---
title: Redigere modeller og tilknytninger til at generere dokumenter, der har programdata
description: For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 2 - Generere dokumenter)".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5df6128228b9ff620c606c550c5eb7a6039b915
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182295"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>Redigere modeller og tilknytninger til at generere dokumenter, der har programdata

[!include [task guide banner](../../includes/task-guide-banner.md)]

For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 2: Generere dokumenter)". 

I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument og opdatere programdata. I denne procedure skal redigere du ER-konfigurationerne for at begynde at bruge dem til at generere elektroniske dokumenter og opdatere programdata. Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af DEMF-datasættet.


## <a name="modify-data-model"></a>Rediger datamodel
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Vælg 'Intrastat (model)' i træet.
    * Du skal udvide brugen af datamodellen. Ud over at bruge den som datakilde for at generere Intrastat-rapporten, bruges datamodellen til at indsamle oplysninger om Intrastat-rapporteringsprocessen. Oplysningerne bruges derefter til at opdatere programdata.   
3. Klik på Designer.
4. Klik på Ny for at åbne dialogboksen Fjern.
5. Skriv "Modelrod" i feltet Ny node som felt.
6. Skriv 'Til opdatering af programdata' i feltet Navn.
    * Til opdatering af programdata  
7. Klik på Tilføj.
8. Vælg 'Til opdatering af programdata' i træet.
    * Det nye rodelement tilføjes for at angive det dataflow, der skal bruges til at flytte data fra Intrastat-rapporten (brugt som datakilde) til programtabellerne (opdateringsdestinationen). Bemærk, at de forskellige rodelementer skal bruges til at hente data, der bogføres i det udgående dokument, og til at hente data fra det dokument, der bruges til at opdatere programdata.   
9. Klik på Ny for at åbne dialogboksen Fjern.
10. Skriv 'Arkivoverskrift' i feltet Navn.
    * Arkivoverskrift  
11. Vælg "Liste over poster" i feltet Varetype.
12. Klik på Tilføj.
    * Eftersom du skal oprette en post for hver Intrastat-rapport, der oprettes, skal du oprette et nyt element til den.  
13. Klik på Ny for at åbne dialogboksen Fjern.
14. Skriv "Filnavn" i feltet Navn.
    * Filnavn  
15. Vælg "Streng" i feltet Varetype.
16. Klik på Tilføj.
17. Klik på Ny for at åbne dialogboksen Fjern.
18. Skriv "Antal linjer" i feltet Navn.
    * Antal linjer  
19. Vælg "Heltal" i feltet Varetype.
20. Klik på Tilføj.
    * Tilføj dette element for at repræsenterer antallet af Intrastat-posteringer, der rapporteres i den aktuelle rapporteringsproces.  
21. Klik på Ny for at åbne dialogboksen Fjern.
22. Skriv 'Arkivér linjer' i feltet Navn.
    * Arkivér linjer  
23. Vælg "Liste over poster" i feltet Varetype.
24. Klik på Tilføj.
    * Tilføj dette element for at repræsenterer listen over Intrastat-posteringer, der rapporteres i den aktuelle rapporteringsproces.  
25. Klik på Ny for at åbne dialogboksen Fjern.
26. Skriv "Beløb" i feltet Navn.
    * Beløb  
27. Vælg "Kommatal" i feltet Varetype.
28. Klik på Tilføj.
29. Klik på Ny for at åbne dialogboksen Fjern.
30. Skriv 'Varepost-id' i feltet Navn.
    * Varepost-id  
31. Vælg 'Int64' i feltet Varetype.
32. Klik på Tilføj.
33. Klik på Ny for at åbne dialogboksen Fjern.
34. Skriv 'Varenummer' i feltet Navn.
    * varenummer  
35. Vælg "Streng" i feltet Varetype.
36. Klik på Tilføj.
37. Klik på Gem.
38. Luk siden.

## <a name="modify-model-mapping"></a>Rediger modeltilknytning
1. Udvid 'Intrastat (model)' i træet.
2. Vælg 'Intrastat (model)\Intrastat (tilknytning)' i træet.
    * Rediger den eksisterende modeltilknytning for at begynde at bruge den til opdateringen af programdata og arkivere Intrastat-rapporteringsdetaljer.  
3. Klik på Designer.
4. Klik på Ny.
5. Skriv 'Opdater arkiv' i feltet Navn.
    * Opdater arkiv  
6. Vælg 'Til destination' i feltet Retning.
7. Klik på Gem.
    * Denne nye tilknytning angiver det dataflow, der skal bruges til at flytte data (Intrastat-rapporteringsdetaljer) fra datamodellen til programtabellerne (opdateringsdestinationen). Bemærk, at en anden models rodelementer skal bruges til at hente data fra programmet til rapporteringsprocessen og derefter bruge dataene fra datamodellen til programdataopdateringen.   
8. Klik på Designer.
9. Vælg 'Datamodel\Datamodel' i træet.
    * Tilføj den krævede datakilde. Dette er den datamodel, der indeholder oplysninger om de rapporterede Intrastat-transaktioner, der skal arkiveres.  
10. Klik på Tilføj rod.
11. Skriv 'model' i feltet Navn.
    * model  
12. Angiv eller vælg værdien 'Til opdatering af programdata' i feltet Definition.
    * Til opdatering af programdata  
13. Klik på OK.
14. Udvid 'model' i træet.
15. Vælg "Funktioner\Beregnet felt" i træet.
16. Vælg 'model\Arkivér overskrift' i træet.
17. Klik på Tilføj.
    * Datakilden skal tilføjes, fordi du skal optælle Intrastat-posteringer, der er rapporteret til arkivering.  
18. Skriv 'Optalte linjer' i feltet Navn.
    * Optalte linjer  
19. Klik på Rediger formel.
20. Vælg 'Liste\ENUMERATE' i træet.
21. Klik på Tilføj funktion.
22. Udvid 'model' i træet.
23. Udvid 'model\Arkivér overskrift' i træet.
24. Vælg 'model\Arkivér overskrift\Arkivér linjer' i træet.
25. Klik på Tilføj datakilde.
26. Angiv 'ENUMERATE(model.'Arkivér overskrift.'Arkivér linjer)' i feltet Formel.
    * ENUMERATE(model. 'Arkivoverskrift'.' Arkivér linjer)  
27. Klik på Gem.
28. Luk siden.
29. Klik på OK.
30. Klik på Tilføj destination.
    * Tilføj programtabeller som krævede destinationer, der skal opdateres for at arkivere oplysninger om rapporterede Intrastat-transaktioner.  
31. Skriv 'Arkiv' i feltet Navn.
    * Arkivér  
32. Gå til feltet Tabelnavn, og skriv 'IntrastatArchiveGeneral'.
    * IntrastatArchiveGeneral  
    * Behold posthandlingen "Indsæt", så du kan tilføje poster under arkiveringen af detaljer for hver Intrastat-rapporteringsproces.  
33. Vælg Ja i feltet Postinfolog.
    * Vælg Ja for at få oplysninger om problemer med programdataopdateringen.  
34. Vælg Ja i feltet Undlad validering af posthandling.
    * Vælg Ja for at forhindre valideringsfejl for det tomme felt 'Id for Intrastat-arkiv'. Dette sker, når der er tilføjet poster, baseret på rækkefølgen af talindstillinger, der er konfigureret for denne tabel i formularen Udenrigshandelsparametre.  
35. Klik på OK.
    * Bind elementer i den tilføjede datakilde (den filtrerede model, der er baseret på det valgte rodelement) til elementer fra den tilføjede destination.  
36. Udvid 'Arkivér' i træet.
37. Udvid 'Arkivér\<Relationer' i træet.
38. Udvid 'Arkivér\<Relationer\IntrastatArchiveDetail' i træet.
39. Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Beløb(AmountMST)' i træet.
40. Udvid 'model\Arkivér overskrift\Optalte linjer' i træet.
41. Udvid 'model\Arkivér overskrift\Optalte linjer\Værdi' i træet.
42. Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Beløb' i træet.
43. Klik på Bind.
44. Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Vare(IntrastatCommodity)' i træet.
45. Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Varepost-id' i træet.
46. Klik på Bind.
47. Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Varenummer(ItemId)' i træet.
48. Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Varenummer' i træet.
49. Klik på Bind.
50. Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Linjenummer(LineNumber)' i træet.
51. Vælg 'model\Arkivér overskrift\Optalte linjer\Nummer' i træet.
52. Klik på Bind.
53. Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail' i træet.
54. Vælg 'model\Arkivér overskrift\Optalte linjer' i træet.
55. Klik på Bind.
56. Vælg 'Arkivér\Filnavn(FileName)' i træet.
57. Vælg 'model\Arkivér overskrift\Filnavn' i træet.
58. Klik på Bind.
59. Vælg 'Arkivér\Antal linjer(NumberOfLines)' i træet.
60. Vælg 'model\Arkivér overskrift\Antal linjer' i træet.
61. Klik på Bind.
62. Vælg 'Arkivér' i træet.
63. Vælg 'model\Arkivér overskrift' i træet.
64. Klik på Bind.
65. Klik på Gem.
66. Luk siden.
67. Luk siden.

