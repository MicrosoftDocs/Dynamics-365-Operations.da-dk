---
title: Redigere formater for at generere dokumenter, der har programdata
description: I dette emne forklares det, hvordan du designer konfigurationer af rapportering for at generere et elektronisk dokument og opdatere programdata.
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96b36f987457d6973a96e90d6978438df7c8c6e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754233"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Redigere formater for at generere dokumenter, der har programdata

[!include [banner](../../includes/banner.md)]

For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 3: Redigere model og tilknytning)".

I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument og opdatere programdata. I denne procedure skal redigere du ER-konfigurationerne, ikke kun for at begynde at bruge dem til at generere elektroniske dokumenter, men også for at opdatere programdata. Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af DEMF-datasættet.


## <a name="modify-format-to-collect-details-of-reporting"></a>Ændre format for at indsamle rapporteringsoplysninger
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Intrastat (model)' i træet.
3. Vælg 'Intrastat (model)\Intrastat (format)' i træet.
4. Klik på Designer.
5. Udvid 'Fil' i træet.
6. Udvid 'Fil\Erklæring' i træet.
7. Vælg 'Fil\Erklæring\Data' i træet.
8. Vælg 'Én mange' i feltet Multiplicitet.
    * Konfigurer dette formatelement for at arkivere oplysninger om Intrastat-rapporteringsprocessen. Dette element repræsenterer arkivets overskriftspost.  
9. Udvid 'Fil\Erklæring\Data' i træet.
10. Vælg 'Fil\Erklæring\Data\Element' i træet.
11. Vælg 'Nul mange' i feltet Multiplicitet.
    * Konfigurer dette formatelement for at arkivere oplysninger om Intrastat-rapporteringsprocessen. Dette element repræsenterer listen over arkiverede linjer.  
12. Udvid 'Fil\Erklæring\Data\Element' i træet.
13. Vælg 'Fil\Erklæring\Data\Element\Dim1' i træet.
14. Vælg Ja i feltet Udelukket.
    * Du skal ikke arkivere disse data, så du kan udelukke dette format element fra datakilden til Intrastat-rapporteringsdetaljer.  
15. Udvid 'Fil\Erklæring\Data\Element\Dim1' i træet.
16. Vælg 'Fil\Erklæring\Data\Element\Dim1\egenskab' i træet.
17. Vælg Ja i feltet Udelukket.
18. Vælg 'Fil\Erklæring\Data\Element\Dim1\dato' i træet.
19. Vælg Ja i feltet Udelukket.
20. Vælg 'Fil\Erklæring\Data\Element\Dim2' i træet.
21. Vælg Ja i feltet Udelukket.
22. Udvid 'Fil\Erklæring\Data\Element\Dim2' i træet.
23. Vælg 'Fil\Erklæring\Data\Element\Dim2\egenskab' i træet.
24. Vælg Ja i feltet Udelukket.
25. Vælg 'Fil\Erklæring\Data\Element\Dim2\kode' i træet.
26. Vælg Ja i feltet Udelukket.
27. Vælg 'Fil\Erklæring\Data\Element\Dim3' i træet.
    * Flere formateringselementer kan have samme navn. For eksempel Dim. Du kan ikke eksplicit genkende dem, når du bruger dette format som en datakilde til arkivering af Intrastat-rapporteringsdetaljer, så du skal definere de alternative navne til disse formatelementer.   
28. Skriv "Beløb" i feltet Navn.
    * Beløb  
29. Vælg 'Nøjagtig én' i feltet Multiplicitet.
30. Vælg 'Fil\Erklæring\Data\Element\Dim4' i træet.
31. Skriv "Vare" i feltet Navn.
    * Post  
32. Vælg 'Nøjagtig én' i feltet Multiplicitet.
    * Ud over designformatelementerne skal følgende Intrastat-rapporteringsdetaljer arkiveres: entydigt postidentifikationen for hver rapporteret vare og navnet på den oprettede fil. Da disse data ikke udfyldes i Intrastat-rapporten, skal du tilføje det format, der er relateret til disse detaljeelementer som datakildeelementer.  
33. Vælg 'Fil\Erklæring\Data' i træet.
34. Klik på Tilføj for at åbne dialogboksen.
35. Vælg 'Datakilde\Element' i træet.
36. Skriv "Filnavn" i feltet Navn.
    * Filnavn  
37. Vælg 'Streng' i feltet Datatype.
38. Klik på OK.
39. Vælg 'Fil\Erklæring\Data\Element' i træet.
40. Klik på Tilføj vare.
41. Skriv 'Varepost-id' i feltet Navn.
    * Varepost-id  
42. Vælg 'Int64' i feltet Datatype.
43. Klik på OK.
44. Klik på fanen Tilknytning.
45. Vælg 'Fil\Erklæring\Data\Filnavn' i træet.
46. Klik på Bind.
47. Udvid 'model' i træet.
48. Udvid 'model\Transaktioner' i træet.
49. Vælg 'Fil\Erklæring\Data\Element = model.Transaktioner\Varepost-id' i træet.
50. Vælg 'model\Transaktioner\Varepost-id' i træet.
51. Klik på Bind.
52. Klik på Gem.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Ændre format for at huske rapporteringsoplysninger

1. Klik på Knyt format til model.
2. Klik på Ny.
3. Angiv eller vælg rodelementet 'Til opdatering af programdata' i feltet Definition.
    * Til opdatering af programdata.
4. Skriv 'Tilknytning for at opdatere data' i feltet Navn.
    * Tilknytning for at opdatere data  
5. Klik på Gem.
    * Denne tilknytning definerer, hvordan der indsamles oplysninger om Intrastat-rapporten i datamodellen, hvis struktur angives af det valgte rodelement 'Til opdatering af programdata'. Disse oplysninger, modeltilknytningen med rodelementet 'Til opdatering af programdata' og retningen 'Til destination' bruges til opdateringen af dataprogrammet. Opdateringen af programdataene starter umiddelbart efter, at den udgående Intrastat-rapport er oprettet. Opdateringen af programdataene kan springes over under kørslen, men datamodellen skal være tom (indeholde en liste over tomme poster).
6. Klik på Designer.
    * Det udgående Intrastat-rapportformat tilføjes som standard som en datakilde til denne modeltilknytning.  
    * Bind elementer i den designede rapport (vist som datakilde) til elementer i datamodellen, der filtreres baseret på rodelementet for den valgte model.  
7. Udvid 'Arkivér overskrift' i træet.
8. Udvid 'Arkivér overskrift\Arkivér linjer' i træet.
9. Udvid 'format' i træet.
10. Udvid 'format\Erklæring: XML-Element(Erklæring)' i træet.
11. Udvid 'format\Erklæring: XML-element(erklæring)\Data: XML-element 1..* (Data)' i træet.
12. Udvid 'format\Erklæring: XML-element(erklæring)\Data: XML-element 1..* (Data)\Element: XML Element 0..* (element)' i træet.
13. Udvid 'format\Erklæring: XML-element(erklæring)\Data: XML-element 1..* (Data)\Element: XML Element 0..* (element)\Dim3:XML Element 1..1 (beløb)' i træet.
14. Udvid 'format\Erklæring: XML-element(erklæring)\Data: XML-element 1..* (Data)\Element: XML Element 0..* (element)\Dim4:XML Element 1..1 (element)' i træet.
15. Vælg 'Arkivér overskrift\Antal linjer' i træet.
16. Klik på Rediger.
17. Vælg 'Liste\COUNT' i træet.
18. Klik på Tilføj funktion.
19. Udvid 'format' i træet.
20. Udvid 'format\Erklæring: XML-Element(Erklæring)' i træet.
21. Udvid `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)` i træet.
22. Vælg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)` i træet.
23. Klik på Tilføj datakilde.
24. Angiv 'COUNT(format.Declaration.Data.Item)' i feltet Formel.
    * COUNT(format. Declaration.Data.Item)  
25. Klik på Gem.
26. Luk siden.
27. Vælg 'Arkivér overskrift\Filnavn' i træet.
28. Vælg 'format\Erklæring: XML Element(Erklæring)\Data: XML Element 1..* (Data)\Filnavn: Elementstreng(Filnavn)' i træet.
29. Klik på Bind.
30. Vælg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)` i træet.
31. Vælg 'Arkivér overskrift\Arkivér linjer\Varenummer' i træet.
32. Klik på Bind.
33. Vælg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)` i træet.
34. Vælg 'Arkivér overskrift\Arkivér linjer\Beløb' i træet.
35. Klik på Bind.
36. Vælg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec ID: Item Int64(Commodity rec ID)` i træet.
37. Vælg 'Arkivér overskrift\Arkivér linjer\Varepost-id' i træet.
38. Klik på Bind.
39. Vælg 'Arkivér overskrift\Arkivér linjer' i træet.
40. Vælg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)` i træet.
41. Klik på Bind.
42. Vælg 'Arkivér overskrift' i træet.
43. Vælg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)` i træet.
44. Klik på Bind.
45. Klik på Gem.
46. Luk siden.
47. Luk siden.
48. Luk siden.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]