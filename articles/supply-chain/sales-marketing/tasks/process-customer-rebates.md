--- 
title: Generere og behandle debitorrabatter
description: "Denne fremgangsmåde viser, hvordan kunderabatter behandles fra generering af kravet til punktet, hvor de godkendes som periodiseringer til debitor."
author: omulvad
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 348793abc6d219f38bcdc2629b77343d93927005
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="generate-and-process-customer-rebates"></a>Generere og behandle debitorrabatter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan kunderabatter behandles fra generering af kravet til punktet, hvor de godkendes som periodiseringer til debitor. Det fører dig gennem et specifikt eksempel for at forklare, hvordan de forskellige betingelser på rabatlinjerne påvirker de endelige beløb, der krediteres til kunden. Du skal bruge USMF-demodatafirmaet og udføre følgende opgaver, før du starter guiden: (1) gå til siden Debitorparametre, og udvid fanen Priser og derefter fanen Prisdetaljer. Kontrollér, at indstillingen Aktivér prisdetaljer er angivet til Ja. (2) Gå til rabataftalesiden, og vælg debitorrabataftalen: USMF-000001. Hvis feltet Status for godkendelsesarbejdsgang ikke er angivet til Godkendt, skal du klikke på Validering i handlingsruden for at godkende den.


## <a name="review-a-customer-rebate-agreement"></a>Gennemse en debitorrabataftale
1. Gå til salg og marketing > Kunderabatter > Rabataftaler.
    * De næste par trin kigger på betingelserne for aftale USMF-000001. Dette gør det nemmere at forstå, hvordan kundekreditværdier beregnes senere i proceduren.  
    * Aftalen er for en individuel kunde, i dette eksempel kunde US-009.  
    * Rabatter gives til kunder, når de køber et bestemt produkt. I dette tilfælde har produktet varenummer T0020.   
    * Kundens salgsperformance, som rabatbeløbene beregnes mod, samles på en ugentlig basis.  
    * Indstillingen for "Pris taget fra" er brutto, hvilket betyder, at denne linjes salgsbeløb, på hvilket grundlag kravet anslås, ikke er fratrukket linjerabatten.  
    * Feltet Linjeskifttype for rabat viser metoden til beregning af rabatter. I dette tilfælde er de salgsmål, som rabatterne skal estimeres mod, angivet til mængde.   
    * Aftalelinjerne angiver rabatbeløbstypen, den faktiske rabatværdi og grænser. I dette eksempel vil kunden opnå en rabat på 20 kr. pr. enhed, der sælges, hvis det ugentlige køb af produktet ligger inden for 1 til 50 enheder, og en rabat på 40 kr. pr. enhed, der er solgt, når de køber over 50 enheder.  
2. Luk siden.

## <a name="generate-rebate-claims"></a>Generer rabatkrav
1. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
2. Klik på Ny.
    * For at efterligne den måde, som rabatkrav vil blive genereret på, er næste opgave at oprette en salgsordre, hvor produktet og antallet kvalificerer pågældende kunde til en rabat.  
3. Indtast eller vælg en værdi i feltet Kundekonto.
4. Klik på OK.
5. Indtast eller vælg en værdi i feltet Varenummer.
6. Angiv antallet til '40'.
7. Klik på Salgsordrelinje.
8. Klik på prisdetaljer.
    * Hvis denne mulighed ikke vises, skyldes det, at du ikke har angivet indstillingen Aktiver pris til Ja, før du startede guiden.  
9. Udvid afsnittet Rabatter.
    * Fanen Rabatter viser alle rabataftaler, der gælder for den aktuelle ordrelinje og viser den anslåede rabat. Bemærk, at de viste beløb kun er en angivelse af, hvilke fremtidige rabatkrav der kan være. De faktiske rabatbeløb kan være forskellige afhængigt af: den samlede salgsmængde opnået af kunden i henhold til en periodisk rabataftale, om kunden havde returneret hele eller delvise antal og om den relevante salgsordre blev faktureret.  
10. Luk siden.
11. Klik på Tilføj linje.
12. Indtast eller vælg en værdi i feltet Varenummer.
13. Angiv antallet til '60'.
14. Klik på Gem.
15. Klik på Faktura i handlingsruden.
16. Klik på Faktura.
17. Udvid sektionen Parametre.
18. Vælg "Alle" i feltet Antal.
19. Klik på OK.
20. Klik på OK.

## <a name="process-rebate-claims"></a>Behandl rabatkrav
1. Gå til Salg og marketing > Kunderabatter > Rabatter.
    * Siden Rabatter fungerer som et panel, hvor du kan gennemse, godkende og behandle rabatkrav. Du skal nu behandle krav, der blev oprettet ved fakturering af en salgsordre for kunde US-009, der er omfattet af rabataftalen USMF-000001.   
    * Den første linje repræsenterer et rabatkrav på 800 kr., som er baseret på salg af 40 enheder af vare T0020, beregnet til 20 kr. pr. enhed. Dette svarer til betingelserne i den første mængdereduktion i rabataftalen.  
    * Det andet krav til 2400 kr., som er baseret på salg af 60 enheder af vare T0020, beregnet til 40 kr. pr. enhed i henhold til den anden mængdereduktion i aftalen.  
    * Begge krav er i tilstanden "Skal beregnes". Det betyder, at de er knyttet til en aftale, der registrerer kundens salgsresultater med regelmæssige mellemrum, og at de skal beregnes igen at tage højde for den samlede salg inden for den pågældende periode.   
2. Klik på Opsaml.
3. Indtast eller vælg en værdi i feltet Kunde.
4. Vælg dags dato i feltet Startdato.
5. Klik på OK.
    * Som et resultat af, at funktionen Opsaml køres, er det anslåede kravbeløb nu reguleret til at tage højde for det faktum, at kundens samlede salg i den relevante periode er højere end da den første rabat blev genereret. Mere specifikt, fordi det samlede antal, der er købt, har nået 100 enheder, er kunden nu berettiget til 40 kr. pr. enhed (ifølge aftalens anden mængdereduktion) eller 400 kr. af det samlede rabatbeløb. Forskellen er registreret som en ny "kravregulering" for de ekstra 800 kr. Status for rabatkrav, der er medtaget i opdateringen Opsaml, er nu sat til Beregnet.   
6. Markér alle poster på listen.
7. Klik på Godkend.
8. Klik på Proces.
9. Indtast eller vælg en værdi i feltet Kunde.
10. Klik på OK.
    * Der vises en meddelelse, at rabatten blev behandlet, og status for kravene er blevet ændret til Markér. Det betyder, at som følge af en rabatperiodiseringskladde bogføres: a) kravene er nu overført til den midlertidige debitorsaldo som fradrag, b) periodiseringskonto for rabat er krediteret for at repræsentere de fremtidige betalingsforpligtelse mod kunden og c) rabatudgiftskontoen er debiteret i anerkendelse af omkostningen i forbindelse med salg.   


