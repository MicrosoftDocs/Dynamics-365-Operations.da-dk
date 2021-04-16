---
title: Designe ER- konfigurationer til at fortolke indgående dokumenter
description: I denne procedure forklares det, hvordan du designer konfigurationer af elektronisk rapportering (ER) for at analysere et elektronisk dokument.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b503c17b395c2ef45ca4d74c8573d859509c503
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745055"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Designe ER- konfigurationer til at fortolke indgående dokumenter

[!include [banner](../../includes/banner.md)]

I denne procedure forklares det, hvordan du designer konfigurationer af elektronisk rapportering (ER) for at analysere et elektronisk dokument. I denne procedure skal du importere de nødvendige ER-konfigurationer, der er oprettet til eksempelfirmaet Litware, Inc., og bruge dem til at analysere indgående elektroniske dokumenter. For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv".

Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler.

Disse trin kan udføres ved hjælp af ethvert datasæt. Før du går i gang, skal du hente og gemme de filer, der er anført i emnet "Analysere indgående dokumenter for at opdatere programdata" ([Analysere indgående dokumenter](../parse-incoming-electronic-documents.md)). Filerne er: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".
2. Vælg Rapporteringskonfigurationer.
    * Følgende scenario skal bruges til at få vist egenskaberne for fortolkning af indgående elektroniske dokumenter i XML-format: ERP-programmet anmoder om data fra webtjenesten (f.eks. [efsta](http://efsta.org/)-regnskabsservice) og fortolker indgående svar for at opdatere programdata tilsvarende. For at opnå den mest effektive fortolkningsmåde bruges et enkelt ER-format til trods for, at forventede indgående dokumenter i XML-format har en anderledes struktur.

## <a name="import-and-review-er-configurations"></a>Importere og gennemse ER-konfigurationer

Importér den ER-modelkonfiguration, der indeholder den eksempeldatamodel, der er udviklet til at gemme oplysningerne om den indgående fil.

1. Vælg Udveksling.
2. Vælg Indlæs fra XML-fil.
    * Vælg Gennemse, og vælg filen EFSTA model.xml.
3. Vælg OK.
4. Vælg 'EFSTA model' i træet.
5. Vælg Designer.
    * Gennemse strukturen af den importerede datamodel. Optællingen enumType er defineret til at genkende følgende typer servicesvar: til at få en bekræftelse om transaktionens afsendelse, til at få oplysninger om den sidst afsendte postering og til at genkende svartyper, der ikke understøttes.
6. Udvid 'Svar' i træet.
    * Rodelementet 'Svar' er defineret for at angive, hvilken type data der skal tages fra et understøttet servicesvar for at opdatere programdata i overensstemmelse hermed.
7. Luk siden.
    * Du vil importere ER-formatkonfigurationen, der angiver, hvordan indgående dokumenter skal fortolkes for at gemme data i ER-datamodellen.
8. Vælg Udveksling.
9. Vælg Indlæs fra XML-fil.
    * Vælg Gennemse, og vælg filen EFSTA format.xml.
10. Vælg OK.
11. Vælg 'udvid EFSTA model' i træet.
12. Vælg 'EFSTA model\EFSTA format' i træet.
13. Vælg Designer.
14. Vælg Udvid/skjul.
    * CASE-formatelementet bruges som rod og indeholder tre indlejrede FILE-elementer, hvilket betyder, at dette format er udformet til at analysere indgående filer af flere formater.
15. Vælg 'Svar\Afslutning af transaktionen\TraC' i træet.
    * Svaret om den sendte postering starter fra rodelementet 'TraC'.
16. Vælg 'Svar\Sidste transaktionsanmodning\Tra' i træet.
    * Svaret om den senest sendte postering starter fra rodelementet 'Era'.
17. Vælg 'Svar\Uventet svar\Tekst' i træet.
    * Det tredje FILE-element med indlejret TEXT-element er tilføjet for at genkende andre former for svar, der afviger fra ovennævnte.
18. Vælg Knyt format til model.
    * Denne modeltilknytning indeholder definitionen på dataflow til at gemme oplysninger om det fortolkede indgående dokument med brug af datamodellens elementer.
19. Vælg Designer.
20. Udvid 'format' i træet.
21. Udvid 'format\Svar: Case(Responses)' i træet.
    * Gennemse strukturen af 'format'-datakilden. Alle tre svartyper tilbydes separat.
22. Vælg 'format\Svar: Case(Responses)\aType' i træet.
    * Datakildeelementet 'aType' er føjet til for at angive svartypen og er bundet til datamodelelementet 'Type'.
23. Vælg fanen Valideringer.
24. Vælg 'Type = format.Responses.aType' i træet.
    * ER-valideringen er konfigureret for at informere brugeren om situationen, når svarstrukturen ikke stemmer overens med bekræftelsen om indsendelse af transaktionen eller oplysningerne om den sidste indsendte postering (ikke-understøttet svarsag).
25. Luk siden.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Kør modeltilknytning af ER-format, der er konfigureret til fortolkning af indgående filer

Du skal køre den oprettede modeltilknytning til testformål for at se, hvordan det konfigurerede ER-format vil fortolke indgående servicesvar. Dette trin bruger forskellige XML-filer til at simulere forskellige typer webtjenestesvar.

1. Åbn filen Response1.xml i en XML-læser, f.eks. en webbrowser. Denne fil indeholder bekræftelsesoplysninger om den fuldførte postering ('TraC' er rodelementet).
2. Vælg Kør.
    * Vælg Gennemse, og vælg filen Response1.xml.
3. Vælg OK.
    * Gennemse det genererede output. Svartypen er korrekt genkendt og fortolket (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` betyder afslutning af transaktionen).
    * Åbn filen Response2.xml i en XML-læser. Denne fil indeholder oplysninger om den sidst indsendte transaktion (`Tra` er rodelementet).
4. Vælg Kør.
    * Vælg Gennemse, og vælg filen Response2.xml.
5. Vælg OK.
    * Gennemse det genererede output. Svartypen er korrekt genkendt og fortolket (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` betyder genstart af systemet).
    * Åbn filen Response3.xml i en XML-læser. Denne fil starter fra TraZ-rodelementet, og denne struktur er ikke konfigureret ved brug af ER-formatet.
6. Vælg Kør.
    * Vælg Gennemse, og vælg filen Response3.xml.
7. Vælg OK.
    * Gennemse det genererede output. Svartypen er korrekt registreret som ikke-understøttet (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Den tilsvarende meddelelse er blevet placeret i infologgen (i henhold til ER-valideringsindstillingen), og det meste af datamodellen er ikke udfyldt.
    * Åbn filen Response4.xml i en XML-læser. Strukturen i denne fil er næsten den samme som i Response1.xml, der blev fortolket korrekt, med undtagelse af rækkefølgen af indlejrede elementer i rodelementet 'TraC'.
8. Vælg Kør.
    * Vælg Gennemse, og vælg filen Response4.xml.
9. Vælg OK.
    * Gennemse det genererede output. Svartypen er korrekt registreret som ikke-understøttet (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Den tilsvarende meddelelse er blevet placeret i infologgen, og det meste af datamodellen er ikke udfyldt. Denne funktionsmåde skyldes, at den aktuelle indstilling af dette ER-format forudsætter en bestemt rækkefølge af indlejrede elementer til rodelementet i den indgående fil.
10. Luk siden.
11. Vælg 'Svar\Afslutning af transaktionen\TraC' i træet.
12. I rækkefølgen Parsing af indlejrede elementer felt, skal du vælge 'Alle'.
    * Vælg Alle i feltet 'Parsingrækkefølge for indlejrede elementer' for at tillade enhver sekvens af indlejrede elementer for dette rod XML-element.
13. Vælg Gem.
14. Vælg Knyt format til model.
15. Vælg Kør.
    * Vælg Gennemse, og vælg filen Response4.xml.
16. Vælg OK.
    * Gennemse det genererede output. Svartypen nu er korrekt genkendt som ens med filen Response1.xml.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]