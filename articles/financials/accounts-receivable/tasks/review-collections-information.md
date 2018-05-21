--- 
title: Gennemse oplysninger om rykkere
description: "Denne procedure fører dig gennem, hvordan du gennemgår rykkeroplysninger samt forskellige konfigurationsindstillinger og rykkerposteringer."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb0866505702ec5d047b6c8f3f0657aae787bedc
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="review-collections-information"></a>Gennemse oplysninger om rykkere

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fører dig gennem, hvordan du gennemgår rykkeroplysninger samt forskellige konfigurationsindstillinger og rykkerposteringer. Denne procedure bruger demofirmaet USMF.


## <a name="create-customer-pools"></a>Oprette kundepuljer
1. Gå til Kredit og inkasso > Opsætning > Kundepuljer.
    * Brug denne side til at konfigurere kundepuljer, som er forespørgsler, der definerer en gruppe debitorkonti, der kan vises og administreres for rykkere eller forældelsesprocesser. Brug kundepuljer til at filtrere oplysningerne på listesiden Rykkere og på relaterede listesider. Du kan også bruge kundepuljer til at filtrere de debitorkonti, der inkluderes ved oprettelsen af aldersfordelte øjebliksbilleder.  
    * Du kan bruge kundepuljer til at filtrere de debitorkonti, der inkluderes ved oprettelsen af aldersfordelte øjebliksbilleder.  
2. Klik på Ny.
3. Indtast en værdi i feltet Pulje-id.
4. Skriv en værdi i feltet Puljebeskrivelse.
5. Klik på Vælg puljekriterier.
6. Skriv en værdi i feltet Kriterier.
7. Klik på OK.
8. Klik på Eksempel på kundepulje.

## <a name="create-collections-agents"></a>Oprette inkassatorer
1. Gå til Kredit og inkasso > Opsætning > Inkassoagenter.
    * Brug denne side til at konfigurere arbejdere som inkassatorer og vælge at tildele dem kundepuljer. En inkassator er en person, der arbejder sammen med kunderne om at sikre, at betalinger opkræves rettidigt.  
    * De inkassatorer, der konfigureres på denne side, føjes automatisk til et inkassatorteam. Hvis et team er markeret i feltet Team på siden Debitorparametre, føjes inkassatorer til dette team. Hvis der ikke er markeret et team, oprettes der automatisk et nyt team med navnet Rykkere, og inkassatorerne føjes til dette team.  
2. Klik på Ny.
3. Klik på Tilføj.
4. Klik på Luk.
5. Klik på Tilføj.
6. Markér den valgte række på listen.
7. Klik på rullelisten i feltet Pulje-id for at åbne opslaget.
8. Find og vælg den ønskede post på listen.
9. Markér eller fjern markeringen i afkrydsningsfeltet Standardpulje.
    * Vælg denne indstilling for at medtage alle kundepuljer i filterlister for den valgte inkassator. Hvis denne indstilling ikke er valgt, er kun de kundepuljer, der er tildelt inkassatoren, tilgængelige i filterlister.  

## <a name="create-aging-period-definition"></a>Oprette definition af forældelsesperiode
1. Gå til Kredit > Opsætning > Definitioner af forældelsesperioder.
    * Du kan bruge definitioner af forældelsesperioder til at analysere forfaldsfordelingen for debitorkonti og kreditorkonti baseret på en dato, du angiver. Hver forældelsesperiode, du konfigurerer for definitionen af forældelsesperioder, svarer til en kolonne på listesiden eller i formen eller rapporten, når analysen udføres.  
2. Klik på Ny.
3. Indtast en værdi i feltet Definition på forældelsesperiode.
4. Skriv en værdi i feltet Beskrivelse.
    * Angiv periodens navn, enhed og intervallet for hver forældelsesperiode, der skal medtages i definitionen af forældelsesperiode. Linjen, der har 0 (nul) i feltet Enhed, angiver den dato, hvor analysen køres. Linjerne før nul vil have -1, og linjerne efter nul vil have 1 som standardangivelse i feltet Enhed, men de kan ændres.  Klik på knapperne Op og Ned for at flytte rundt på linjerne. Linjen 0 (nul) kan ikke flyttes.  
    * Placer markøren, hvor du vil indsætte en ny linje, og klik derefter på Tilføj.  
    * Vælg en indikator, der skal repræsentere forældelsesperioden i Rykkere-formularen og -listesiden. Du kan f.eks. vælge en grøn indikator for en aktuel periode, en gul indikator for en 30-dage-over-periode og en rød indikator for en 90-dage-over-periode.  
    * Vælg udskriftsretningen for definitionen af forældelsesperioder. Dette valg bestemmer den rækkefølge, som kolonnerne vises på Aldersfordelt saldoliste for kunder eller Aldersfordelt saldoliste for kreditorer.  Fremad – Udskriv kolonner i samme rækkefølge, som overskrifterne vises i, i tabellen, med den øverste række først.  Bagud – Udskriv kolonner i omvendt rækkefølge i forhold til den rækkefølge, som overskrifterne vises i tabellen, med den nederste række først.    

## <a name="setup-collections-parameters"></a>Konfigurer rykkerparametre
1. Gå til Kredit og inkasso > Opsætning > Debitorparametre.
2. Klik på fanen Rykkere.
3. Udvid eller skjul sektionen Inkassostandarder.
    * Vælg en definition af forældelsesperiode til det aldersfordelte standardøjebliksbillede, der bruges i formularen Rykkere.  
    * Vælg et team, som inkassatorer skal tildeles, i formularen Inkassator. Kun team med teamtypen Rykkere vises på listen.  
4. Udvid eller skjul sektionen Afskrivning.
    * Vælg det kladdenavn, der er konfigureret for finanskassekladder, som skal bruges, når en postering afskrives ved hjælp af formularen Rykkere eller relaterede listesider.  
    * Vælg den standardårsagskode, der skal bruges, når der oprettes afskrivningsposteringer ved hjælp af formularen Rykkere eller relaterede listesider.  
    * Vælg denne indstilling for at oprette en separat kladdelinje til momsbeløb, når der oprettes afskrivningstransaktioner ved hjælp af siden Rykkere eller relaterede listesider. Hvis du vælger denne indstilling, kan du let spore de momsbeløb, der vedrører afskrivningstransaktioner. Du kan spore momsbeløbene separat, så du lettere kan justere den skyldige moms for den berørte periode.  
5. Udvid eller skjul sektionen E-mail-skabelon.
    * Vælg den mailskabelon, der skal bruges, når du sender en mail ved hjælp af handlingen Mail > Posteringer for kontaktperson i formularen Rykkere.  
    * Vælg den e-mail-skabelon, der skal bruges, når du sender en kundeopgørelse som en vedhæftet fil i en e-mail ved hjælp af handlingen Mail > Opgørelse for kontaktperson i formularen Rykkere.  
    * Vælg den mailskabelon, der skal bruges, når du sender en mail ved hjælp af handlingen Mail > Posteringer for sælger i formularen Rykkere.  

## <a name="age-customer-balance"></a>Foræld debitorsaldo
1. Gå til Kredit > Periodiske opgaver > Æld debitorsaldi.
    * Vælg en definition af forældelsesperiode. Processen for det aldersfordelte øjebliksbillede forælder transaktioner efter de forældelsesperioder, der er defineret i den valgte definition af forældelsesperiode.  
    * Vælg en kundepulje, eller lad dette felt være tomt for at oprette et aldersfordelt øjebliksbillede for alle debitorer. Hvis du vælger en kundepulje, anvendes processen for aldersfordelt øjebliksbillede kun for de debitorkonti, der indgår i kundepuljen. Den valgte kundepulje skal være af typen aldersfordelt øjebliksbillede.  
    * Vælg den type dato, det aldersfordelte øjebliksbillede skal baseres på.    Posteringsdato – Foræld hver transaktion baseret på transaktionsdatoen.    Forfaldsdato – Foræld hver transaktion baseret på forfaldsdatoen.    Dokumentdato – Foræld hver transaktion baseret på dokumentdatoen.  
    * Vælg den type dato, der skal bruges som dags dato for det aldersfordelte øjebliksbillede. Forældelsesperioder beregnes på grundlag af denne dato.    Dags dato – Brug systemdatoen. Vælg denne indstilling, hvis behandling er indstillet til at ske som et tilbagevendende batchjob. Hvis du bruger denne dato, kan du køre det tilbagevendende batchjob periodisk, og systemdatoen på det tidspunkt anvendes.    Valgt dato – Brug en dato, du angiver. Hvis du vælger denne indstilling, skal du angive en forældelsesdato.  
2. Klik på OK.

## <a name="view-aged-customer-balances"></a>Vise aldersfordelte debitorsaldi
1. Gå til Kredit > Rykkere > Aldersfordelte saldi.
    * Du kan bruge denne listeside til at få vist debitorsaldi og aldersfordelte beløb efter forældelsesperiode. Disse oplysninger gemmes i et aldersfordelt øjebliksbillede. Forældelsesperioderne bestemmes af den anvendte definition af forældelsesperioder. Definitionen af forældelsesperiode hentes fra kundepuljen, hvis der er angivet en til puljeforespørgslen. Hvis kundepuljen ikke indeholder en definition af forældelsesperiode, bruges den standarddefinition af forældelsesperiode, som er angivet i formen Debitorparametre.  
2. Udvid faktaboksen Kontakt.
    * Kundens rykkerkontakt.  
    * Standardsælger for kunden.  
3. Udvid faktaboksen Kreditmaks.
    * Brug faktaboksen Kreditoplysninger til at få vist oplysninger om kreditmaksimum og aktuel saldo for debitoren.  

## <a name="view-customer-collections-details"></a>Vis oplysninger om debitorrykkere
1. Klik op linket i den valgte række på listen.
2. Udvid faktaboksen Adresse.
3. Udvid faktaboksen Kontakt.
4. Udvid faktaboksen Aldersfordeling.
5. Udvid faktaboksen Kreditmaks.
6. Klik på Indsaml i handlingsruden.
    * Opdater det aldersfordelte øjebliksbillede for kunden med dags dato som den forældelsesdato, som posteringsdatoerne sammenlignes med. Hvis det aldersfordelte øjebliksbillede indeholder oplysninger om flere juridiske enheder, indeholder det opdaterede aldersfordelte øjebliksbillede oplysninger om den samme gruppe af juridiske enheder. Beløb gemmes i regnskabsvalutaen for den juridiske enhed, du er logget på, når du opdaterer det aldersfordelte øjebliksbillede.  
    * Vælg en definition af forældelsesperiode. Som standard vises den definition af forældelsesperiode, der er knyttet til det aldersfordelte øjebliksbillede for kunden. Definitionen af forældelsesperiode bruges til at styre de forældelsesperioder og -beløb, der vises i faktaboksene Aldersfordelte saldi og Kreditoplysninger.  
    * Åbn en menu, der indeholder følgende elementer: Regnskab – få vist beløbene i faktaboksene Aldersfordelte saldi og Kreditoplysninger i regnskabsvalutaen for den juridiske enhed.    Debitor – få vist beløbene i faktaboksene Aldersfordelte saldi og Kreditoplysninger i kundens valuta.  
    * Vælg en eller flere juridiske enheder i kundens aldersfordelte øjebliksbillede, som du vil have vist oplysninger om. De juridiske enheder, der vises på listen, blev valgt, da det aldersfordelte øjebliksbillede blev oprettet.  
    * Få vist kundens opgørelse i Microsoft Excel-format. Du kan vælge en startdato for den række posteringer, der skal medtages i opgørelsen, og bestemme, om kun åbne posteringer skal medtages, eller både åbne og udlignede posteringer. Hvis det aldersfordelte øjebliksbillede indeholder oplysninger om flere juridiske enheder, medtages posteringer for alle juridiske enheder.  
    * Åbn formularen Dokumenter, hvor du kan oprette eller redigere dokumenter eller noter.  
7. Klik på Kommuniker i handlingsruden.
    * Åbn Outlook, hvor du kan sende en mail til den kontakt, der er angivet i feltet Kontakt. Hvis en rykkerkontaktperson ikke er angivet, bruges den primære adresse på debitoren. Hvis en primær kontakt ikke er angivet, sendes mails til den første adresse, der vises i formularen Kontakter. De posteringer, der vælges, medtages som en vedhæftet fil. Den vedhæftede fil er i Excel-format og indeholder tre regneark. Du kan angive en mail-skabelon til meddelelser til kundekontakter i formularen Debitorparametre.  
    * Denne knap er ikke tilgængelig, hvis den kontaktperson, der vælges i denne form, ikke har konfigureret en e-mail-adresse.  
    * Forbered en opgørelse, og åbn Outlook, hvor du kan sende en mail med en vedhæftet fil til den adresse, der er angivet i feltet Kontakt. Hvis en rykkerkontaktperson ikke er angivet, bruges den primære adresse på debitoren. Hvis en primær kontakt ikke er angivet, sendes mails til den første adresse, der vises i formularen Kontakter.  
    * Denne knap er ikke tilgængelig, hvis den kontaktperson, der vælges i denne form, ikke har konfigureret en e-mail-adresse.  
    * Åbn Outlook, hvor du kan sende en e-mail til den medarbejder, der er angivet som sælger for den salgsgruppe, der er tildelt kunden. Hvis der er valgt posteringer, medtages de som en vedhæftet fil. Den vedhæftede fil er i Excel-format og indeholder to regneark. Du kan angive en mailskabelon til meddelelser til sælgere i formularen Debitorparametre.  
    * Denne knap er ikke tilgængelig, hvis den sælger, der vises i denne form, ikke har konfigureret en e-mail-adresse.  
    * Få vist og udfør handlinger på posteringer for debitoren. Hvis du bruger centraliserede betalinger, medtages oplysninger om alle de juridiske enheder, der er medtaget i kundens aldersfordelte øjebliksbillede. Du kan begrænse oplysningerne om den juridiske enhed ved hjælp af knappen Firma i gruppen Vælg i handlingsruden.  
    * Skift rykkerstatus for de valgte posteringer.    Ikke bestridt – Der har ikke fundet nogen rykkerhandlinger sted for posteringen.    Bestridt – Kunden har givet besked om, at der er et problem med posteringen.    Har lovet at betale – Kunden har accepteret at betale posteringsbeløbet.    Løst – Alle problemer med posteringen er løst, og det er derfor ikke nødvendigt med flere rykkerhandlinger.  
    * Åbn en menu, og vælg et af følgende punkter for at angive, hvilke posteringer der skal vises i denne formular: Åben – Vis kun de posteringer, der ikke er udlignet.    Åbne og lukkede – Få vist alle posteringer, både udlignede og ikke-udlignede.  
    * Udfør behandling af den valgte betaling som en NSF-betaling (Non-sufficient Funds – USA).    Denne knap er kun tilgængelig, hvis den valgte betaling er en betaling (en kreditsaldo uden en faktura), der er angivet i en betalingskladde, en bankkonto er tildelt posteringen, og betalingen ikke tidligere er annulleret.  
    * Afskriv de valgte posteringer.  
    * Markér de valgte posteringer til udligning med hinanden.  
    * Åbn formularen Originaldokument, hvor du kan få vist og udskrive dokumentet til den valgte postering.  
    * Åbn en menu, der indeholder følgende elementer: Rykkere – Vis kun aktiviteter, der er oprettet i formularen Rykkere.    Alle – Få vist alle aktiviteter for kunden, uanset hvor aktiviteterne er oprettet.  
    * Åbn en menu, der indeholder følgende elementer: Åbne – Vis kun aktiviteter, der ikke er lukket.    Åbne og lukkede – Få vist alle aktiviteter uanset deres status.  
    * Vælg en rykkersag, der er tildelt debitoren, eller lad dette felt være tomt. Hvis en sag er valgt, vises kun de posteringer og aktiviteter, der er knyttet til sagen, i denne form.  
8. Klik på Vis liste.
    * Vælg en debitorkonto, eller acceptér standardposten. Som standard er det den valgte debitorkonto på listesiden eller i den form, du åbnede denne form fra. Hvis du åbnede formen fra en listeside, er debitorerne på listen de debitorer, der er med i den rykkerpulje, der bruges på listesiden.  


