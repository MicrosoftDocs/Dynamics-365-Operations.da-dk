---
title: EUR-00002 Generere en EU Intrastat-opgørelse
description: Denne procedure fører dig gennem de trin, der kræves for at eksportere Intrastat-opgørelsen i det elektroniske filformat og gennemse opgørelsens data i et Excel-format.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2aba5caaaf0fbee511e1a293b09fa8301bb6831
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407714"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a>EUR-00002 Generere en EU Intrastat-opgørelse

[!include [banner](../../includes/banner.md)]

Denne procedure fører dig gennem de trin, der kræves for at eksportere Intrastat-opgørelsen i det elektroniske filformat og gennemse opgørelsens data i et Excel-format. 

Før du kan udføre denne procedure, skal du overføre transaktioner til Intrastat. 

Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.


## <a name="import-configurations-with-settings"></a>Importere konfigurationer med indstillinger
1. Gå til Arbejdsområder > Elektronisk rapportering
2. Klik på Angiv som aktiv.
3. Klik på Lagre.
4. Klik på Åbn.
5. Åbn kolonnefilteret Konfigurationsnavn.
6. Anvend et filter til feltet "Konfigurationsnavn" med værdien "Intrastat (DE)" ved hjælp af filteroperatøren "begynder med".
    * Du bør vælge det konfigurationsnavn, der gælder for landets/områdets juridiske enhed. Denne procedure bruger den tyske juridiske enhed (DEMF) som et eksempel, og derfor bør "Intrastat (DE)" vælges.  
    * Klik på Importér, og klik derefter på Ja.  
7. Åbn kolonnefilteret Konfigurationsnavn.
8. Anvend et filter til feltet "Konfigurationsnavn" med værdien "Intrastat-rapport" ved hjælp af filteroperatøren "begynder med".
    * Klik på Importér, og klik derefter på Ja.  

## <a name="set-up-foreign-trade-parameters"></a>Konfigurere udenrigshandelsparametre
1. Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre
2. Udvid sektionen Elektronisk rapportering.
3. Indtast eller vælg værdien Intrastat (DE) i feltet Filformattilknytning.
4. Indtast eller vælg værdien Intrastat-rapport i feltet Rapportformattilknytning.
5. Udvid sektionen Afrundingsregler.
    * Du skal oprette afrundingsregler, der anvendes i dit land/område til Intrastat-rapportering.  
6. Indtast et tal i feltet Afrundingsregel.
    * Indtast for eksempel afrundingspræcisionen '0,01'.  
7. Indtast et tal i feltet Antal decimaler for beløb.
    * Indtast for eksempel '2'.  
8. Vælg en indstilling i feltet Afrunding under 1 kg.
    * Vælg for eksempel 'Afrunding op til 1 kg'.  
9. Indtast et tal i feltet Afrundingsregel.
    * Indtast for eksempel '1' for at afrunde vægten til heltallet.  
10. Udvid sektionen Minimumsgrænse.
11. Angiv et tal i feltet Vægt.
    * Indtast for eksempel '10' som minimal vægt.  
12. Angiv et tal i feltet Beløb.
    * Indtast for eksempel '200' som minimalt beløb.  
13. Indtast eller vælg en værdi i feltet Vare.

## <a name="set-up-compression-of-intrastat"></a>Konfigurere komprimering af Intrastat
1. Gå til Skat > Konfiguration > Udenrigshandel > Komprimering af Intrastat.
2. Klik på Fjern.
3. Find og vælg den ønskede post på listen.
    * Vælg for eksempel Vare i sektionen Tilgængelige.  
4. Klik på Tilføj.

## <a name="generate-intrastat-declaration"></a>Generere Intrastat-opgørelse
1. Gå til Skat > Erklæringer > Udenrigshandel > Intrastat
2. Klik på Valider.
    * Valideringen udføres i henhold til feltet Checkkonfiguration på siden Udenrigshandelsparametre.  
3. Klik på OK.
4. Klik på Opdater.
5. Klik på Minimumsgrænse
6. Angiv en dato i feltet Startdato.
    * Indtast for eksempel '1. januar 2015'.  
7. Vælg Ja i feltet Komprimer.
8. Indtast en dato i feltet Slutdato.
    * Indtast for eksempel '31. januar 2015'.  
9. Klik på OK.
10. Klik på Opdater.
11. Klik på Komprimer.
    * Denne komprimering sker i overensstemmelse med konfigurationen af Komprimering af Intrastat.  
12. Angiv en dato i feltet Startdato.
    * Indtast for eksempel '1. januar 2015'.  
13. Indtast en dato i feltet Slutdato.
    * Indtast for eksempel '31. januar 2015'.  
14. Klik på OK.
15. Klik på Opdater.
16. Klik på Regenerer sekvensnumre.
17. Klik på OK.
18. Klik på Output.
19. Klik på Rapport.
20. Indtast den første dato i rapporteringsperioden i feltet Fra dato.
    * Indstil for eksempel datoen til 1. januar 2015.  
21. Indtast en dato i feltet Til dato.
    * Indtast for eksempel '31. januar 2015'.  
22. Vælg Ja i feltet Generer fil.
23. Skriv en værdi i feltet Filnavn.
24. Vælg Ja i feltet Generer rapport.
25. Skriv en værdi i feltet Raportfilnavn.
26. Vælg en indstilling i feltet Retning.
    * Vælg for eksempel 'Udførsel'.  
27. Klik på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]