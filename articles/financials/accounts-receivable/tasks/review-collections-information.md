---
title: Gennemse oplysninger om rykkere
description: Dette emne beskriver, hvordan du gennemgår oplysninger om rykkere samt forskellige konfigurationsindstillinger og rykkertransaktioner.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsPool, SysQueryForm, CustCollectionsAgent, OMTeamSelectMemberDialog, CustVendReportInterval, CustParameters, CustAgingSnapshot, CustVendAgingBucketLookUp, CustCollectionsPoolsListPage, CustCollectionsContactPart, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd606461b9d7198bda12e297598fae0cbf8b39a7
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855728"
---
# <a name="review-collections-information"></a>Gennemse oplysninger om rykkere

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emne beskriver, hvordan du gennemgår oplysninger om rykkere samt forskellige konfigurationsindstillinger og rykkertransaktioner. Denne procedure bruger demofirmaet USMF.

## <a name="create-customer-pools"></a>Oprette kundepuljer
1. I navigationsruden skal du gå til **Moduler > Kredit og inkasso > Opsætning > Kundepuljer**.
- Brug denne side til at konfigurere kundepuljer, som er forespørgsler, der definerer en gruppe debitorkonti, der kan vises og administreres for rykkere eller forældelsesprocesser. Brug kundepuljer til at filtrere oplysningerne på listesiden **Rykkere** og på relaterede listesider. Du kan også bruge kundepuljer til at filtrere de debitorkonti, der inkluderes ved oprettelsen af aldersfordelte øjebliksbilleder.  
- Du kan bruge kundepuljer til at filtrere de debitorkonti, der inkluderes ved oprettelsen af aldersfordelte øjebliksbilleder.  
2. Vælg **Ny**.
3. Indtast en værdi i feltet **Pulje-id**.
4. Indtast en værdi i feltet **Puljebeskrivelse**.
5. Klik på **Vælg puljekriterier**.
6. Skriv en værdi i feltet **Kriterier**.
7. Vælg **OK**.
8. Vælg **Eksempel på kundepulje**.

## <a name="create-collections-agents"></a>Oprette inkassatorer
1. I navigationsruden skal du gå til **Moduler > Kredit og inkasso > Opsætning > Inkassatorer**.  
- Brug denne side til at konfigurere arbejdere som inkassatorer og vælge at tildele dem kundepuljer. En *Inkassator* er en person, der arbejder sammen med kunderne om at sikre, at betalinger opkræves rettidigt.  
- De inkassatorer, der konfigureres på denne side, føjes automatisk til et inkassatorteam. Hvis et team er markeret i feltet **Team** på siden **Debitorparametre**, føjes inkassatorerne til dette team. Hvis der ikke er markeret et team, oprettes der automatisk et nyt team med navnet Rykkere, og inkassatorerne føjes til dette team.  
2. Vælg den ønskede inkassator, og vælg derefter **Tilføj på siden**.
3. I feltet **Pulje-ID** skal du vælge den ønskede post i rullemenuen.
4. Markér eller fjern markeringen i afkrydsningsfeltet **Standardpulje**.
- Vælg denne indstilling for at medtage alle kundepuljer i filterlister for den valgte inkassator. Hvis denne indstilling ikke er valgt, er kun de kundepuljer, der er tildelt inkassatoren, tilgængelige i filterlister.  

## <a name="create-aging-period-definition"></a>Oprette definition af forældelsesperiode
1. I navigationsruden skal du gå til **Moduler > Kredit og inkasso > Opsætning > Definitioner af forældelsesperioder**.
- Du kan bruge definitioner af forældelsesperioder til at analysere forfaldsfordelingen for debitorkonti og kreditorkonti baseret på en dato, du angiver. Hver forældelsesperiode, du konfigurerer for definitionen af forældelsesperioder, svarer til en kolonne på listesiden eller i formen eller rapporten, når analysen udføres.  
2. Vælg **Ny**.
3. Indtast en værdi i feltet **Definition af forældelsesperiode**.
4. Indtast en værdi i feltet **Beskrivelse**.
- Angiv periodens navn, enhed og intervallet for hver forældelsesperiode, der skal medtages i definitionen af forældelsesperiode. Linjen, der har 0 (nul) i feltet Enhed, angiver den dato, hvor analysen køres. Linjerne før nul vil have -1, og linjerne efter nul vil have 1 som standardangivelse i feltet Enhed, men de kan ændres. Vælg **Op** og **Ned** for at omarrangere linjerne. Linjen 0 (nul) kan ikke flyttes.  
- Placer markøren, hvor du vil indsætte en ny linje, og vælg derefter på **Tilføj**.  
- Vælg en indikator, der skal repræsentere forældelsesperioden i **Rykker**-formularen og listesiden. Du kan f.eks. vælge en grøn indikator for en aktuel periode, en gul indikator for en 30-dage-over-periode og en rød indikator for en 90-dage-over-periode.  
- Vælg udskriftsretningen for definitionen af forældelsesperioder. Dette valg bestemmer den rækkefølge, som kolonnerne vises på Aldersfordelt saldoliste for kunder eller Aldersfordelt saldoliste for kreditorer.  
  - Fremad – Udskriv kolonner i samme rækkefølge, som overskrifterne vises i, i tabellen, med den øverste række først.  
  - Bagud – Udskriv kolonner i omvendt rækkefølge i forhold til den rækkefølge, som overskrifterne vises i tabellen, med den nederste række først.    

## <a name="setup-collections-parameters"></a>Konfigurer rykkerparametre
1. I navigationsruden skal du gå til **Moduler > Kredit og inkasso > Opsætning > Debitorparametre**.
2. Vælg fanen **Rykkere**.
3. Udvid eller skjul sektionen **Inkassostandarder**.
- Vælg en definition af forældelsesperioden til det aldersfordelte standardøjebliksbillede, der bruges i formularen **Rykkere**.  
- Vælg et team, som inkassatorerne skal tildeles, i formularen **Inkassator**. Kun team med teamtypen Rykkere vises på listen.  
4. Udvid eller skjul sektionen **Afskrivning**.
- Vælg det kladdenavn, der er konfigureret for finanskassekladder, og som skal bruges, når en transaktion afskrives ved hjælp af formularen **Rykkere** eller relaterede listesider.  
- Vælg den standardårsagskode, der skal bruges, når der oprettes afskrivningstransaktioner ved hjælp af formularen **Rykkere** eller relaterede listesider.  
- Vælg denne indstilling for at oprette en separat kladdelinje til momsbeløb, når der oprettes afskrivningstransaktioner ved hjælp af siden **Rykkere** eller relaterede listesider. Hvis du vælger denne indstilling, kan du let spore de momsbeløb, der vedrører afskrivningstransaktioner. Du kan spore momsbeløbene separat, så du lettere kan justere den skyldige moms for den berørte periode.  
5. Udvid eller skjul sektionen **E-mail-skabelon**.
- Vælg den e-mailskabelon, der skal bruges, når du sender en e-mail ved hjælp af handlingen **E-mail > Transaktioner** til kontaktpersonen i formularen **Rykkere**.  
- Vælg den e-mail-skabelon, der skal bruges, når du sender en kundeopgørelse som en vedhæftet fil i en e-mail ved hjælp af handlingen **E-mail > Opgørelse** til kontaktpersonen i formularen **Rykkere**.  
- Vælg den e-mailskabelon, der skal bruges, når du sender en e-mail ved hjælp af handlingen **E-mail > Transaktioner** til sælgeren i formularen **Rykkere**.  

## <a name="age-customer-balance"></a>Foræld debitorsaldo
1. I navigationsruden skal du gå til **Moduler > Kredit og inkasso > Periodiske opgaver > Aldersfordel kundesaldi**.
- Vælg en definition af forældelsesperiode. Processen for det aldersfordelte øjebliksbillede forælder transaktioner efter de forældelsesperioder, der er defineret i den valgte definition af forældelsesperiode.  
- Vælg en kundepulje, eller lad dette felt være tomt for at oprette et aldersfordelt øjebliksbillede for alle debitorer. Hvis du vælger en kundepulje, anvendes processen for aldersfordelt øjebliksbillede kun for de debitorkonti, der indgår i kundepuljen. Den valgte kundepulje skal være af typen aldersfordelt øjebliksbillede.  
- Vælg den type dato, det aldersfordelte øjebliksbillede skal baseres på.  
  - Posteringsdato – Foræld hver transaktion baseret på transaktionsdatoen.    
  - Forfaldsdato – Foræld hver transaktion baseret på forfaldsdatoen.    
  - Dokumentdato – Foræld hver transaktion baseret på dokumentdatoen.  
- Vælg den type dato, der skal bruges som dags dato for det aldersfordelte øjebliksbillede. Forældelsesperioder beregnes på grundlag af denne dato.    
  - Dags dato – Brug systemdatoen. Vælg denne indstilling, hvis behandling er indstillet til at ske som et tilbagevendende batchjob. Hvis du bruger denne dato, kan du køre det tilbagevendende batchjob periodisk, og systemdatoen på det tidspunkt anvendes.    
  - Valgt dato – Brug en dato, du angiver. Hvis du vælger denne indstilling, skal du angive en forældelsesdato.  
2. Vælg **OK**.

## <a name="view-aged-customer-balances"></a>Vise aldersfordelte debitorsaldi
1. I navigationsruden skal du gå til **Moduler > Kredit og inkasso > Opsætning > Aldersfordelte saldi**.
- Du kan bruge denne listeside til at få vist debitorsaldi og aldersfordelte beløb efter forældelsesperiode. Disse oplysninger gemmes i et aldersfordelt øjebliksbillede. Forældelsesperioderne bestemmes af den anvendte definition af forældelsesperioder. Definitionen af forældelsesperiode hentes fra kundepuljen, hvis der er angivet en til puljeforespørgslen. Hvis kundepuljen ikke indeholder en definition af forældelsesperiode, bruges den standarddefinition af forældelsesperiode, som er angivet i formen Debitorparametre.  
2. Udvid faktaboksen **Kontakt**. Her kan du se kontaktoplysningerne:
- Kundens rykkerkontakt.  
- Standardsælger for kunden.  
3. Udvid faktaboksen **Kreditmaks.**.
- Brug faktaboksen **Kreditoplysninger** til at få vist oplysninger om kreditmaks. og debitors aktuelle saldo.  

## <a name="view-customer-collections-details"></a>Vis oplysninger om debitorrykkere
1. Kontroller, at den ønskede post er valgt.
2. Udvid faktaboksene **Adresse**, **Kontakt**, **Aldersfordelt** og **Kreditmaks.** for at få vist de givne oplysninger.
3. Vælg **Indsaml** i handlingsruden.
- Opdater det aldersfordelte øjebliksbillede for kunden med dags dato som den forældelsesdato, som posteringsdatoerne sammenlignes med. Hvis det aldersfordelte øjebliksbillede indeholder oplysninger om flere juridiske enheder, indeholder det opdaterede aldersfordelte øjebliksbillede oplysninger om den samme gruppe af juridiske enheder. Beløb gemmes i regnskabsvalutaen for den juridiske enhed, du er logget på, når du opdaterer det aldersfordelte øjebliksbillede.  
- Vælg en definition af forældelsesperiode. Som standard vises den definition af forældelsesperiode, der er knyttet til det aldersfordelte øjebliksbillede for kunden. Definitionen af forældelsesperioden bruges til at styre de forældelsesperioder og -beløb, der vises i faktaboksene **Aldersfordelte saldi** og **Kreditoplysninger**.  
- Åbn en menu, der indeholder følgende elementer:    
  - Virksomhed – Se beløb i faktaboksene Aldersfordelte saldi og Kreditoplysninger i den juridiske enheds regnskabsvaluta.  
  - Debitor – få vist beløbene i faktaboksene Aldersfordelte saldi og Kreditoplysninger i kundens valuta.  
- Vælg en eller flere juridiske enheder i kundens aldersfordelte øjebliksbillede, som du vil have vist oplysninger om. De juridiske enheder, der vises på listen, blev valgt, da det aldersfordelte øjebliksbillede blev oprettet.  
- Få vist kundens opgørelse i Microsoft Excel-format. Du kan vælge en startdato for den række posteringer, der skal medtages i opgørelsen, og bestemme, om kun åbne posteringer skal medtages, eller både åbne og udlignede posteringer. Hvis det aldersfordelte øjebliksbillede indeholder oplysninger om flere juridiske enheder, medtages posteringer for alle juridiske enheder.  
- Åbn formularen **Dokumenter**, hvor du kan oprette eller redigere dokumenter eller noter.  
4. Klik på **Kommuniker** i handlingsruden.  
- Åbn Outlook, hvor du kan sende en mail til den kontakt, der er angivet i feltet Kontakt. Hvis en rykkerkontaktperson ikke er angivet, bruges den primære adresse på debitoren. Hvis en primær kontakt ikke er angivet, sendes e-mails til den første adresse, der vises i formularen **Kontakter**. De posteringer, der vælges, medtages som en vedhæftet fil. Den vedhæftede fil er i Excel-format og indeholder tre regneark. Du kan angive en e-mail-skabelon til meddelelser til kundekontakter i formularen **Debitorparametre**.  
- Denne knap er ikke tilgængelig, hvis den kontaktperson, der vælges i denne form, ikke har konfigureret en e-mail-adresse.  
- Udarbejd en opgørelse, og åbn Outlook, hvor du kan sende en e-mail med en vedhæftet fil til den adresse, der er angivet i feltet **Kontakt**. Hvis en rykkerkontaktperson ikke er angivet, bruges den primære adresse på debitoren. Hvis en primær kontakt ikke er angivet, sendes e-mails til den første adresse, der vises i formularen **Kontakter**.  
- Denne knap er ikke tilgængelig, hvis den kontaktperson, der vælges i denne form, ikke har konfigureret en e-mail-adresse.  
- Åbn Outlook, hvor du kan sende en e-mail til den medarbejder, der er angivet som sælger for den salgsgruppe, der er tildelt kunden. Hvis der er valgt posteringer, medtages de som en vedhæftet fil. Den vedhæftede fil er i Excel-format og indeholder to regneark. Du kan angive en e-mailskabelon til meddelelser til sælgere i formularen **Debitorparametre**.  
- Denne knap er ikke tilgængelig, hvis den sælger, der vises i denne form, ikke har konfigureret en e-mail-adresse.  
- Få vist og udfør handlinger på posteringer for debitoren. Hvis du bruger centraliserede betalinger, medtages oplysninger om alle de juridiske enheder, der er medtaget i kundens aldersfordelte øjebliksbillede. Du kan begrænse oplysningerne om den juridiske enhed ved at vælge **Virksomhed** i handlingsrudens **Vælg** gruppe.  
- Skift rykkerstatus for de valgte posteringer.    
  - Ikke bestridt – Der har ikke fundet nogen rykkerhandlinger sted for posteringen.    
  - Bestridt – Kunden har givet besked om, at der er et problem med posteringen.    
  - Har lovet at betale – Kunden har accepteret at betale posteringsbeløbet.    
  - Løst – Alle problemer med posteringen er løst, og det er derfor ikke nødvendigt med flere rykkerhandlinger.  
- Åbn en menu, og vælg et af følgende punkter for at angive, hvilke transaktioner der skal vises i denne formular:    
  - Åbne – Se kun de transaktioner, der ikke er udlignet.    
  - Åbne og lukkede – Få vist alle posteringer, både udlignede og ikke-udlignede.  
- Udfør behandling af den valgte betaling som en NSF-betaling (Non-sufficient Funds – USA).    
  - Denne knap er kun tilgængelig, hvis den valgte betaling er en betaling (en kreditsaldo uden en faktura), der er angivet i en betalingskladde, en bankkonto er tildelt posteringen, og betalingen ikke tidligere er annulleret.  
- Afskriv de valgte posteringer.  
- Markér de valgte posteringer til udligning med hinanden.  
- Åbn formularen **Originaldokument**, hvor du kan se og udskrive dokumentet til den valgte transaktion.  
- Åbn en **menu**, der indeholder følgende elementer:    
  - Rykkere – Se kun de aktiviteter, der er oprettet i formularen Rykkere.    
  - Alle – Få vist alle aktiviteter for kunden, uanset hvor aktiviteterne er oprettet.  
- Åbn en **menu**, der indeholder følgende elementer:    
  - Åbne – Se kun de aktiviteter, der ikke er lukkede.    
  - Åbne og lukkede – Få vist alle aktiviteter uanset deres status.  
- Vælg en rykkersag, der er tildelt debitoren, eller lad dette felt være tomt. Hvis en sag er valgt, vises kun de posteringer og aktiviteter, der er knyttet til sagen, i denne form.  
5. Vælg **Vis liste**.
- Vælg en debitorkonto, eller acceptér standardposten. Som standard er det den valgte debitorkonto på listesiden eller i den form, du åbnede denne form fra. Hvis du åbnede formen fra en listeside, er debitorerne på listen de debitorer, der er med i den rykkerpulje, der bruges på listesiden.  

