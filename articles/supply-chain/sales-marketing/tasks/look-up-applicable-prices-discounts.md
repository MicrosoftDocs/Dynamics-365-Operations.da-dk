---
title: Slå gældende priser og rabatter op
description: Denne fremgangsmåde viser, hvordan du finder pris og/eller rabat for et produkt, der er gyldig for en bestemt debitor, uden at oprette en salgsordre.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cfdbda55c2f83ee2b470cab8a5e4f9ce728b852
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424429"
---
# <a name="look-up-applicable-prices-and-discounts"></a>Slå gældende priser og rabatter op

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du finder pris og/eller rabat for et produkt, der er gyldig for en bestemt debitor, uden at oprette en salgsordre. Proceduren fører dig gennem et specifikt eksempel, og du skal følge eksemplet med USMF-demofirmaet for at vælge de nødvendige værdier.


## <a name="find-the-applicable-price"></a>Find den gældende pris
1. Gå til Salg og marketing > Priser og rabatter > Find priser.
2. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
3. Find og vælg debitor US-001 på listen.
4. Klik op linket i den valgte række på listen.
5. Skriv 'T0004' i feltet Varenummer.
    * Feltet Mængde er som standard indstillet til 1. Men, hvis du kender størrelsen på den ordre, som debitoren har til hensigt at placere for det pågældende produkt, skal du angive denne værdi i stedet. Disse oplysninger er relevante, hvis samhandelsaftaler med debitoren har mængdereduktioner, dvs. produktets pris afhænger af den minimummængde, der er købt.  
6. Indtast en dato for, hvornår debitoren forventer at afgive en ordre, i feltet Dato. 
    * Datoen kan være dags dato eller en dato i fremtiden.  
    * Systemet returnerer nu den pris, der gælder for det valgte produkt, når det er købt af den valgte debitor på den valgte dato med en bestemt mængde. Hvis debitor US-001 f.eks. har købt 1 enhed af produkt T0004 i dag, vil debitoren blive opkrævet 350 kr. pr. enhed. Prisen kommer fra en eksisterende og aktiv samhandelsaftale med debitoren.      Andre felter på siden giver flere detaljer om produktpris og produktomkostninger (hvis konfigureret på produktmasteren) samt beregner rentabilitet.  
    * Hvis indstillingen Vis relaterede produktvarianter er valgt, betyder det, at der er flere samhandelsaftaler for produktets varianter.  
7. Klik i afkrydsningsfeltet Vis relaterede produktvarianter.
    * En liste over produktvarianterne vises sammen med oplysninger om deres dimensioner.  
8. Markér den linje, der repræsenterer farven Hvid, på listen.
    * Bemærk, at produktprisen nu er forskellig fra den, der blev vist tidligere, da den ikke var angivet pr. dimension.  
9. Klik på Vis salgspriser.
    * Siden Pris (salg) viser alle de samhandelsaftaler, der gælder for produktet, herunder dets varianter.  
10. Luk siden.

## <a name="find-the-applicable-discount"></a>Find den gældende rabat
Kontrollér, at feltet Debitorkonto indeholder debitornummer US-001   
1. Skriv 'T0012' i feltet Varenummer.
    * Sørg for, at feltet Mængde er angivet til 1.  
    * De følgende oplysninger om priser, der vises for produkt T0012, kommer fra en eller flere samhandelsaftaler: prisen pr. enhed er 1.000 kr., og rabatprocenten er 5.  
2. Angiv antallet til '20'.
    * Den øgede ordremængde medfører den linjerabat, der tilbydes debitoren, så denne vil skifte fra 5 til 7 procent.  
    * Det forventede Nettobeløb beregnes baseret på enhedspris, rabat og samlede mængde.  
3. Klik på Vis linjerabat.
    * Der er to linjerabataftaler for produkt T0012, der angiver en rabat på 5 procents rabat for en ordrelinjemængde fra 1 til 10, og 7 procents rabat på ordremængder over 10. Bemærk, at rabatterne anvendes på en gruppe af produkter, i dette eksempel Gruppekode 01, hvor produkt T0012 er medlem.  
4. Luk siden.

