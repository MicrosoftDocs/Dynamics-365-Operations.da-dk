---
title: Oprette en skabelon til en fritekstfaktura
description: Denne procedure viser, hvordan du opretter en skabelon til en fritekstfaktura.
author: abruer
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1477227228ae9f79314d1e3b6da73446d660d108
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753686"
---
# <a name="create-a-free-text-invoice-template"></a>Oprette en skabelon til en fritekstfaktura

[!include [banner](../includes/banner.md)]

I denne gennemgang skal du bruge USMF-demoregnskabet. Denne procedure er beregnet til den bruger, der er ansvarlig for håndtering og behandling af debitorfakturaer.

## <a name="create-a-template"></a>Opret en skabelon

1. Gå til Debitor > Fakturaer > Tilbagevendende fakturaer > Skabeloner til fritekstfakturaer.
    * Du kan bruge denne form til at oprette skabeloner til fritekstfakturaer, som kan indeholde fakturalinjer, gebyrer, en regnskabsfordelingsskabelon og oplysninger om finanskonti.  
2. Klik på "Ny" for at oprette en ny skabelon til en fritekstfaktura.
3. Skriv en værdi i feltet Skabelonnavn.
    * "Skabelonnavn" identificerer entydigt en skabelon til fritekstfakturaer. To skabeloner kan ikke have samme "Skabelonnavn".  
4. Indtast en beskrivelse af skabelonen i feltet Beskrivelse.
5. Udvid fanen Fakturalinjer.
6. Angiv en beskrivelse af fakturalinjen i feltet Beskrivelse.
7. Vælg en omsætningskonto i feltet Hovedkonto.
    * Du kan vælge en modkonto for en debitorkreditering for det samlede fakturabeløb på siden Debitorposteringsprofiler.  
8. Klik på rullelisten i feltet Momsgruppe for at åbne opslaget.
    * Momsgruppen for den aktuelle fakturalinje er standardmomsgruppen for debitorkontoen.  
9. Klik op linket i den valgte række på listen.
10. Vælg varemomsgruppen for den aktuelle fakturalinje i feltet Varemomsgruppe.
11. Klik op linket i den valgte række på listen.
12. Angiv eller få vist prisen pr. enhed for fakturalinjen i feltet Enhedspris.
    * Dette beløb ganges automatisk med feltet Antal for at bestemme beløbet på fakturalinjen.  
13. Føj en ny linje til skabelon til fritekstfakturaer.
14. Angiv en beskrivelse af fakturalinjen i feltet Beskrivelse.
15. Vælg en omsætningskonto i feltet Hovedkonto.
    * Du kan vælge en modkonto for en debitorkreditering for det samlede fakturabeløb på siden Debitorposteringsprofiler.  
16. Klik på rullelisten i feltet Momsgruppe for at åbne opslaget.
    * Momsgruppen for den aktuelle fakturalinje er standardmomsgruppen for debitorkontoen.  
17. Klik op linket i den valgte række på listen.
18. Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.
    * Varemomsgruppen for den aktuelle fakturalinje.  
19. Klik op linket i den valgte række på listen.
20. Angiv eller få vist antallet af enheder for fakturalinjen
    * Dette tal ganges med værdien i feltet Enhedspris for at bestemme beløbet på fakturalinjen.  
21. Angiv eller få vist prisen pr. enhed for fakturalinjen. 
    * Dette beløb ganges med værdien i feltet Antal for at bestemme beløbet på fakturalinjen.  
22. Få vist og rediger regnskabsfordelinger for en enkelt linje og eventuelle underordnede linjer.
    * Regnskabsfordelinger bruges til at definere, hvordan et beløb skal håndteres regnskabsmæssigt, f.eks. hvordan indtægt, skat eller afgifter håndteres på en fritekstfaktura.  
23. Opdater regnskabsfordelingerne for den valgte fakturalinje.
24. Klik på Luk.

## <a name="save-a-free-text-invoice-as-a-template"></a>Gemme en fritekstfaktura som en skabelon
Du kan også gemme en eksisterende fritekstfaktura som en skabelon. Når du vælger Gem i skabelon under fanen faktura, kan du angive et navn og en beskrivelse af skabelonen. Hvis der findes allerede en skabelon med dette navn, vises en meddelelse om, at der allerede findes en skabelon med dette navn. Du kan stadig klikke på OK for at erstatte den. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
