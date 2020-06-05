---
title: Generere og behandle debitorrabatter
description: Denne fremgangsmåde viser, hvordan kunderabatter behandles fra generering af kravet til punktet, hvor de godkendes som periodiseringer til debitor.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c77129abc5c93d7b11445bdaa2c4851d73bb0b62
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383590"
---
# <a name="generate-and-process-customer-rebates"></a>Generere og behandle debitorrabatter

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan kunderabatter behandles fra generering af kravet til punktet, hvor de godkendes som periodiseringer til debitor. Det fører dig gennem et specifikt eksempel for at forklare, hvordan de forskellige betingelser på rabatlinjerne påvirker de endelige beløb, der krediteres til kunden. Du skal bruge USMF-demodatafirmaet og udføre følgende opgaver, før du starter guiden: (1) gå til siden Debitorparametre, og udvid fanen Priser og derefter fanen Prisdetaljer. Kontrollér, at indstillingen Aktivér prisdetaljer er angivet til Ja. (2) Gå til rabataftalesiden, og vælg debitorrabataftalen: USMF-000001. Hvis feltet Status for godkendelsesarbejdsgang ikke er angivet til Godkendt, skal du klikke på Validering i handlingsruden for at godkende den.


## <a name="review-a-customer-rebate-agreement"></a>Gennemse en debitorrabataftale
1. Gå til **Navigationsrude > Moduler > Salg og marketing > Kunderabatter > Rabataftaler**.
    - De næste par trin kigger på betingelserne for aftale USMF-000001. Dette gør det nemmere at forstå, hvordan kundekreditværdier beregnes senere i proceduren.  
    - Aftalen er for en individuel kunde, i dette eksempel kunde US-009.  
    - Rabatter gives til kunder, når de køber et bestemt produkt. I dette tilfælde har produktet varenummer T0020.   
    - Kundens salgsperformance, som rabatbeløbene beregnes mod, samles på en ugentlig basis.  
    - Indstillingen for "Pris taget fra" er brutto, hvilket betyder, at denne linjes salgsbeløb, på hvilket grundlag kravet anslås, ikke er fratrukket linjerabatten.  
    - Feltet Linjeskifttype for rabat viser metoden til beregning af rabatter. I dette tilfælde er de salgsmål, som rabatterne skal estimeres mod, angivet til mængde.   
    - Aftalelinjerne angiver rabatbeløbstypen, den faktiske rabatværdi og grænser. I dette eksempel vil kunden opnå en rabat på 20 kr. pr. enhed, der sælges, hvis det ugentlige køb af produktet ligger inden for 1 til 50 enheder, og en rabat på 40 kr. pr. enhed, der er solgt, når de køber over 50 enheder.  
2. Luk siden.

## <a name="generate-rebate-claims"></a>Generer rabatkrav
1. Gå til **Navigationsrude > Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer**.
2. Klik på **Ny**. For at efterligne den måde, som rabatkrav vil blive genereret på, er næste opgave at oprette en salgsordre, hvor produktet og antallet kvalificerer pågældende kunde til en rabat.    
3. Indtast eller vælg en værdi i feltet **Debitorkonto**.
4. Klik på **OK**.
5. Indtast eller vælg en værdi i feltet **Varenummer**.
6. Angiv **Antal** til '40'.
7. I afsnittet **Salgsordrelinjer** skal du klikke på **Salgsordrelinjen**.
8. Klik på **Prisdetaljer**. Hvis denne mulighed ikke vises, skyldes det, at du ikke har angivet indstillingen **Aktivér prisdetaljer** til 'Ja', før du startede guiden.     
9. Udvid afsnittet **Rabatter**. Fanen **Rabatter** viser alle rabataftaler, der gælder for den aktuelle ordrelinje, og viser det anslåede rabatbeløb. Bemærk, at de viste beløb kun er en angivelse af, hvilke fremtidige rabatkrav der kan være. De faktiske rabatbeløb kan være forskellige afhængigt af: den samlede salgsmængde opnået af kunden i henhold til en periodisk rabataftale, om kunden havde returneret hele eller delvise antal og om den relevante salgsordre blev faktureret.
10. Luk siden.
11. Klik på **Tilføj linje**.
12. Indtast eller vælg en værdi i feltet **Varenummer**.
13. Angiv **Antal** til '60'.
14. Klik på **Gem**.
15. Klik på **Faktura** i **handlingsruden**.
16. Klik på **Faktura**.
17. Udvid sektionen **Parametre**.
18. Vælg "Alle" i feltet **Antal**.
19. Klik på **OK**.
20. Klik på **OK**.

## <a name="process-rebate-claims"></a>Behandl rabatkrav
1. Gå til **Navigationsrude > Moduler > Salg og marketing > Kunderabatter > Rabatter**.
    - Siden Rabatter fungerer som et panel, hvor du kan gennemse, godkende og behandle rabatkrav. Du skal nu behandle krav, der blev oprettet ved fakturering af en salgsordre for kunde US-009, der er omfattet af rabataftalen USMF-000001.   
    - Den første linje repræsenterer et rabatkrav på 800 kr., som er baseret på salg af 40 enheder af vare T0020, beregnet til 20 kr. pr. enhed. Dette svarer til betingelserne i den første mængdereduktion i rabataftalen.  
    - Det andet krav til 2400 kr., som er baseret på salg af 60 enheder af vare T0020, beregnet til 40 kr. pr. enhed i henhold til den anden mængdereduktion i aftalen.  
    - Begge krav er i tilstanden "Skal beregnes". Det betyder, at de er knyttet til en aftale, der registrerer kundens salgsresultater med regelmæssige mellemrum, og at de skal beregnes igen at tage højde for den samlede salg inden for den pågældende periode.   
2. Klik på **Opsaml**.
3. Indtast eller vælg en værdi i feltet **Kunde**.
4. Vælg dags dato i feltet **Startdato**.
5. Klik på **OK**. Som et resultat af, at funktionen **Opsaml** køres, er det anslåede kravbeløb nu reguleret til at tage højde for det faktum, at kundens samlede salg i den relevante periode er højere end, da den første rabat blev genereret. Mere specifikt, fordi det samlede antal, der er købt, har nået 100 enheder, er kunden nu berettiget til 40 kr. pr. enhed (ifølge aftalens anden mængdereduktion) eller 400 kr. af det samlede rabatbeløb. Forskellen er registreret som en ny "kravregulering" for de ekstra 800 kr. Status for rabatkrav, der er medtaget i opdateringen Opsaml, er nu sat til Beregnet. 
6. Markér alle poster på listen.
7. Klik på **Godkend**.
8. Klik på **Behandl**.
9. Indtast eller vælg en værdi i feltet **Kunde**.
10. Klik på **OK**. Der vises en meddelelse, at rabatten blev behandlet, og status for kravene er blevet ændret til Markér. Det betyder, at der bogføres en rabatperiodiseringskladde:
    - Kravene er nu blevet overført til den midlertidige debitorsaldo som fradrag.
    - Rabatperiodiseringskontoen er blevet krediteret som en repræsentation af det fremtidige passiv for kunden.
    - Rabatudgiftskontoen er blevet debiteret som anerkendelse af de omkostninger, der er påløbet i forbindelse med salg.   

