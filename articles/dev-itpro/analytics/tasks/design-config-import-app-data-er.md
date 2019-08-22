---
title: Designe ER- konfigurationer til at fortolke indgående dokumenter
description: I denne procedure forklares det, hvordan du designer konfigurationer af elektronisk rapportering (ER) for at analysere et elektronisk dokument.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23004930d2377a3d647435b53b6809cd500f44ac
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741349"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Designe ER- konfigurationer til at fortolke indgående dokumenter

[!include [task guide banner](../../includes/task-guide-banner.md)]

I denne procedure forklares det, hvordan du designer konfigurationer af elektronisk rapportering (ER) for at analysere et elektronisk dokument. I denne procedure skal du importere de nødvendige ER-konfigurationer, der er oprettet til eksempelfirmaet Litware, Inc., og bruge dem til at analysere indgående elektroniske dokumenter. For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv".

Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler. 

Disse trin kan udføres ved hjælp af ethvert datasæt. Før du går i gang, skal du hente og gemme de filer, der er anført i emnet "Analysere indgående dokumenter for at opdatere programdata" (https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents). Filerne er: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren "Oprette en konfigurationsudbyder og markere den som aktiv".  
2. Klik på Rapporteringskonfigurationer.
    * Følgende scenario skal bruges til at få vist egenskaberne for fortolkning af indgående elektroniske dokumenter i XML-format: ERP-programmet (Dynamics 365 for Finance and Operations) anmoder om data fra webtjenesten (f.eks. http://efsta.org/ EFSTA-regnskabsservice) og fortolker indgående svar for at opdatere programdata tilsvarende. For at opnå den mest effektive fortolkningsmåde bruges et enkelt ER-format til trods for, at forventede indgående dokumenter i XML-format har en anderledes struktur.   

## <a name="import-and-review-er-configurations"></a>Importere og gennemse ER-konfigurationer
Importér den ER-modelkonfiguration, der indeholder den eksempeldatamodel, der er udviklet til at gemme oplysningerne om den indgående fil.  
1. Klik på Udveksling.
2. Klik på Indlæs fra XML-fil.
    * Klik på Gennemse, og vælg filen EFSTA model.xml.  
3. Klik på OK.
4. Vælg 'EFSTA model' i træet.
5. Klik på Designer.
    * Gennemse strukturen af den importerede datamodel. Bemærk, at optællingen enumType er defineret til at genkende følgende typer servicesvar: til at få en bekræftelse om transaktionens afsendelse, til at få oplysninger om den sidst afsendte postering og til at genkende svartyper, der ikke understøttes.   
6. Udvid 'Svar' i træet.
    * Bemærk, at rodelementet 'Svar' er defineret for at angive, hvilken type data der skal tages fra et understøttet servicesvar for at opdatere programdata i overensstemmelse hermed.   
7. Luk siden.
    * Du vil importere ER-formatkonfigurationen, der angiver, hvordan indgående dokumenter skal fortolkes for at gemme data i ER-datamodellen.   
8. Klik på Udveksling.
9. Klik på Indlæs fra XML-fil.
    * Klik på Gennemse, og vælg filen EFSTA format.xml.  
10. Klik på OK.
11. Vælg 'udvid EFSTA model' i træet.
12. Vælg 'EFSTA model\EFSTA format' i træet.
13. Klik på Designer.
14. Klik på Udvid/skjul.
    * Bemærk, at CASE-formatelementet bruges som rod og indeholder tre indlejrede FILE-elementer, hvilket betyder, at dette format er udformet til at analysere indgående filer af flere formater.  
15. Vælg 'Svar\Afslutning af transaktionen\TraC' i træet.
    * Bemærk, at svaret om den sendte postering starter fra rodelementet 'TraC'.   
16. Vælg 'Svar\Sidste transaktionsanmodning\Tra' i træet.
    * Bemærk, at svaret om den sidst sendte postering starter fra rodelementet 'Tra'.   
17. Vælg 'Svar\Uventet svar\Tekst' i træet.
    * Det tredje FILE-element med indlejret TEXT-element er tilføjet for at genkende andre former for svar, der afviger fra ovennævnte.   
18. Klik på Knyt format til model.
    * Denne modeltilknytning indeholder definitionen på dataflow til at gemme oplysninger om det fortolkede indgående dokument med brug af datamodellens elementer.  
19. Klik på Designer.
20. Udvid 'format' i træet.
21. Udvid 'format\Svar: Case(Responses)' i træet.
    * Gennemse strukturen af 'format'-datakilden. Bemærk, at alle tre svartyper tilbydes separat.   
22. Vælg 'format\Svar: Case(Responses)\aType' i træet.
    * Datakildeelementet 'aType' er føjet til for at angive svartypen og er bundet til datamodelelementet 'Type'.  
23. Klik på fanen Valideringer.
24. Vælg 'Type = format.Responses.aType' i træet.
    * Bemærk, at ER-valideringen er konfigureret for at informere brugeren om situationen, når svarstrukturen ikke stemmer overens med bekræftelsen om indsendelse af transaktionen eller oplysningerne om den sidste indsendte postering (ikke-understøttet svarsag).   
25. Luk siden.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Kør modeltilknytning af ER-format, der er konfigureret til fortolkning af indgående filer
Du skal køre den oprettede modeltilknytning til testformål for at se, hvordan det konfigurerede ER-format vil fortolke indgående servicesvar. Dette trin bruger forskellige XML-filer til at simulere forskellige typer webtjenestesvar.   
1. Åbn filen Response1.xml i en XML-læser, f.eks. en webbrowser. Bemærk, at denne fil indeholder bekræftelsesoplysninger om den fuldførte postering ('TraC' er rodelementet).   
2. Klik på Kør.
    * Klik på Gennemse, og vælg filen Response1.xml.  
3. Klik på OK.
    * Gennemse det genererede output. Bemærk, at svartypen er korrekt genkendt og fortolket (ERModelEnumDataSourceHandler#EFSTA model#enumType#C betyder sag med transaktionsfuldførelse).   
    * Åbn filen Response2.xml i en XML-læser. Bemærk, at denne fil indeholder oplysninger om den sidst indsendte postering ('Tra' er rodelementet).   
4. Klik på Kør.
    * Klik på Gennemse, og vælg filen Response2.xml.  
5. Klik på OK.
    * Gennemse det genererede output. Bemærk, at svartypen er korrekt genkendt og fortolket (ERModelEnumDataSourceHandler#EFSTA model#enumType#R betyder sag med genstart af system).   
    * Åbn filen Response3.xml i en XML-læser. Bemærk, at denne fil starter fra TraZ-rodelementet, og at denne struktur ikke er konfigureret ved brug af ER-formatet.   
6. Klik på Kør.
    * Klik på Gennemse, og vælg filen Response3.xml.  
7. Klik på OK.
    * Gennemse det genererede output. Bemærk, at svartypen er korrekt genkendt og ikke er understøttet (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Den tilsvarende meddelelse er blevet placeret i infologgen (i henhold til ER-valideringsindstillingen), og det meste af datamodellen er ikke udfyldt.   
    * Åbn filen Response4.xml i en XML-læser. Bemærk, at strukturen i denne fil næsten er den samme som i Response1.xml, der blev fortolket korrekt, med undtagelse af rækkefølgen af indlejrede elementer i rodelementet 'TraC'.   
8. Klik på Kør.
    * Klik på Gennemse, og vælg filen Response4.xml.  
9. Klik på OK.
    * Gennemse det genererede output. Bemærk, at svartypen er korrekt genkendt og ikke er understøttet (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Den tilsvarende meddelelse er blevet placeret i infologgen, og det meste af datamodellen er ikke udfyldt. Det skyldes, at den aktuelle indstilling af dette ER-format forudsætter en bestemt rækkefølge af indlejrede elementer til rodelementet i den indgående fil.   
10. Luk siden.
11. Vælg 'Svar\Afslutning af transaktionen\TraC' i træet.
12. I rækkefølgen Parsing af indlejrede elementer felt, skal du vælge 'Alle'.
    * Vælg Alle i feltet 'Parsingrækkefølge for indlejrede elementer' for at tillade enhver sekvens af indlejrede elementer for dette rod XML-element.  
13. Klik på Gem.
14. Klik på Knyt format til model.
15. Klik på Kør.
    * Klik på Gennemse, og vælg filen Response4.xml.  
16. Klik på OK.
    * Gennemse det genererede output. Bemærk, at svartypen nu er korrekt genkendt som ens med filen Response1.xml.  

