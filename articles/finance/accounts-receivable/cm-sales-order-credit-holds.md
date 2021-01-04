---
title: Kredit på hold for salgsordrer
description: Dette emne beskriver konfigurationen af regler, der bruges til at sætte salgsordrer på kredithold.
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 102ea4285407a4f4985cc8dd46ebc1ad21fc6f67
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441432"
---
# <a name="credit-holds-for-sales-orders"></a>Kredit på hold for salgsordrer
[!include [banner](../includes/banner.md)]

Dette emne beskriver konfigurationen af regler, der bruges til at sætte salgsordrer på kredithold. Blokeringsreglerne for kreditstyring kan gælde for en individuel kunde eller en kundegruppe. Blokeringsregler definerer svar i følgende tilfælde:

1. Antal dage over forfaldsdato
2. Status på konti
3. Betalingsbetingelse
4. Kreditgrænse er udløbet
5. Forfaldent beløb
6. Salgsordrebeløb
7. Del af tilgængelig kredit brugt

Derudover er der to parametre, der styrer andre scenarier, som blokerer for en salgsordre.

1. Ændring af betalingsbetingelser
2. Ændring af afregningsrabatter

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Konfigurere blokerings- og udelukkelsesregler

Når en kunde starter en salgstransaktion, gennemgås oplysningerne i salgsordren i forhold til en række blokeringsregler , der er med til at adgøre, om der skal gives kredit til kunden, og om salget kan gå videre. Du kan også definere udelukkelser, der tilsidesætter blokeringsreglerne, så en salgsordre kan behandles. Du kan konfigure blokerings- og udelukkelsesregler på siden **Kreditstyring > Konfiguration > Konfiguration af kreditstyring > Blokeringsregler**.

### <a name="days-overdue"></a>Dages forfald

Åbn fanen **Antal dage over forfaldsdato**, hvis blokeringsreglen gælder for en kunde med én eller flere fakturaer, der har været forfaldne i et bestemt antal dage.
1. Vælg det kundeinterval, som denne regel **gælder for**.
   - Vælg **Tabel**, hvis reglen gælder for en bestemt kunde.
   - Vælg **Gruppe**, hvis reglen gælder for en kundegruppe. 
   - Vælg **Alle**, hvis reglen gælder for alle kunder.
2. Når du har angivet intervallet, skal du angive den **Konto/gruppe**, der skal bruges i intervallet.
   - For intervallet **Tabel** giver opslaget en liste over kunder, der kan vælges. 
   - Vælg en **Gruppe**, hvis reglen gælder for en kundekreditgruppe.
   - Vælg **Alle**, hvis reglen gælder for alle kunder. 
3. Vælg **Risikogruppe** for at bruge kriterier til anvendelse af et kreditstyringshold på kunder, der er grupperet efter et fælles sæt faktorer, f.eks. deres Dun & Bradstreet-rangering, det antal år, de har drevet forretning, den tid, de har været din kunde osv.  
4. Vælg den regeltype, du konfigurerer. Indstillingen **Blokering** opretter en regel, der blokerer en ordre. Indstillingen **Udelukkelse** opretter en regel, der udelukker en anden regel fra at blokere en ordre. 
5. Vælg en **Værditype**. Standardværdien er et fast antal dage. Hvis du opretter en udelukkelse, kan du angive et fast antal dage eller et beløb i stedet. 
6. Angiv antallet af dage for **Forfalden**, der tillades for den valgte blokeringsregel, før en ordre sætte på kreditstyringshold til gennemsyn. Antallet af dage over forfaldsdato udgør et ekstra antal respitdage, der føjes til antallet af dage ud over betalingens forfaldsdato, som fakturaen kan have, før den betragtes som forfalden. Hvis du har angivet **Værditype** som et beløb for en udelukkelse, skal du angive et beløb og en valuta for det pågældende beløb.

### <a name="accounts-status"></a>Status på konti

Åbn fanen **Kontostatus**, hvis blokeringsreglen gælder for en kunde med den valgte kontostatus.
1. Vælg den regeltype, du konfigurerer.  **Blokering** opretter en regel, der blokerer en ordre. **Udelukkelse** opretter en regel, der udelukker en regel fra at blokere en ordre. 
2. Vælg den **Kontostatus**, der medfører, at reglen sætter en salgsordre på hold eller udelukker den.

### <a name="terms-of-payment"></a>Betalingsbetingelse

Vælg **Betalingsbetingelser**, hvis blokeringsreglen gælder for den valgte betalingsbetingelse.
1. Vælg den regeltype, du konfigurerer.  **Blokering** opretter en regel, der blokerer en ordre. **Udelukkelse** opretter en regel, der udelukker en regel fra at blokere en ordre. 
2. Vælg de **Betalingsbetingelser**, der medfører, at reglen sætter en salgsordre på hold eller udelukker den.

### <a name="credit-limit-expired"></a>Kreditgrænse er udløbet

Åbn fanen **Kreditmaks. udløbet**, hvis blokeringsreglen gælder for kunder med et kreditmaks., der er udløbet.
1. Vælg det kundeinterval, som denne regel **gælder for**.
   - Vælg **Tabel**, hvis reglen gælder for en bestemt kunde.
   - Vælg **Gruppe**, hvis reglen gælder for en kundegruppe. 
   - Vælg **Alle**, hvis reglen gælder for alle kunder.
2. Når du har angivet intervallet, skal du angive den **Konto/gruppe**, der bruges i intervallet.
   - For intervallet **Tabel** giver opslaget en liste over kunder, der kan vælges mellem. 
   - Vælg en **Gruppe**, hvis reglen gælder for en kundestyringsgruppe.
   - Vælg **Alle**, hvis reglen gælder for alle kunder. 
3. Vælg en **Risikogruppe** for yderligere at begrænse listen over kunder, der skal sættes på kreditstyringshold. 
4. Vælg den regeltype, du konfigurerer. 
   - Vælg **Blokering** for at oprette en regel, der blokerer en ordre. 
   - Vælg **Udelukkelse** for at oprette en regel, der udelukker en anden regel fra at blokere en ordre. 
5. Angiv **Antal dage kreditmaks. er udløbet** for den valgte blokeringsregel, før en ordre sættes på kreditstyringshold. Antallet af dage over forfaldsdato udgør de ekstra respitdage, der er føjet til det antal dage, kreditmaks. er udløbet.

### <a name="overdue-amount"></a>Forfaldent beløb

Åbn fanen **Forfaldent beløb**, hvis blokeringsreglen gælder for kunder med forfaldne beløb.
1. Vælg det kundeinterval, som denne regel **gælder for**.
   - Vælg **Tabel**, hvis reglen gælder for en bestemt kunde.
   - Vælg **Gruppe**, hvis reglen gælder for en kundegruppe. 
   - Vælg **Alle**, hvis reglen gælder for alle kunder.
2. Når du har angivet intervallet, skal du angive den **Konto/gruppe**, der bruges i intervallet.
   - For intervallet **Tabel** giver opslaget et kundeopslag. 
   - Vælg en **Gruppe**, hvis reglen gælder for en kundestyringsgruppe.
   - Vælg **Alle**, hvis reglen gælder for alle kunder. 
3. Vælg en **Risikogruppe**, hvis du yderligere vil begrænse listen over kunder, der skal sættes på kreditstyringshold. 
4. Vælg den regeltype, du konfigurerer. 
   - Vælg **Blokering** for at oprette en regel, der blokerer en ordre. 
   - Vælg **Udelukkelse** for at oprette en regel, der udelukker en anden regel fra at blokere en ordre. 
5. Angiv **Forfaldent beløb** for den valgte blokeringsregel, før en ordre sættes på kreditstyringshold til gennemsyn. 
6. Vælg den **Værditype**, der definerer den værditype, der skal bruges til også at teste, hvor meget af kreditmaks. der er brugt. Blokeringsregler kræver en procent, men en udelukkelse kan have et fast beløb eller en procentdel. Grænseværdien er relateret til kreditmaks.
7. Angiv **Grænseværdi for kreditmaks.** for den valgte regel, før en kunde sættes på kreditstyringshold. Dette kan være et beløb eller en procentdel, der er baseret på den valgte værditype i værditypen.
8. Reglen kontrollerer, at **Forfaldent beløb** er overskredet, og at **Grænseværdi for kreditmaks.** er overskredet. 

### <a name="sales-order"></a>Salgsordre 

Vælg **Salgsordre**, hvis blokeringsreglen gælder for værdien af salgsordren.
1. Vælg det kundeinterval, som denne regel **gælder for**.
   - Vælg **Tabel**, hvis reglen gælder for en bestemt kunde.
   - Vælg **Gruppe**, hvis reglen gælder for en kundegruppe. 
   - Vælg **Alle**, hvis reglen gælder for alle kunder.
2. Når du har angivet intervallet, skal du angive den **Konto/gruppe**, der bruges i intervallet.
   - For intervallet **Tabel** giver opslaget et kundeopslag. 
   - Vælg en **Gruppe**, hvis reglen gælder for en kundestyringsgruppe.
   - Vælg **Alle**, hvis reglen gælder for alle kunder. 
3. Vælg en **Risikogruppe**, hvis du yderligere vil begrænse listen over kunder, der skal sættes på kreditstyringshold. 
4. Vælg den regeltype, du konfigurerer.  
   - Vælg **Blokering** for at oprette en regel, der blokerer en ordre. 
   - Vælg **Udelukkelse** for at oprette en regel, der udelukker en anden regel fra at blokere en ordre. 
5. Angiv **Salgsordrebeløb** for den valgte blokeringsregel, før en ordre sættes på kreditstyringshold. 

Reglen for salgsordren indeholder en ekstra indstilling, der tilsidesætter alle andre regler. Hvis du vil oprette en udelukkelse, der frigiver salgsordren uden at tage højde for andre regler, skal du markere afkrydsningsfeltet **Frigiv salgsordre** på udelukkelseslinjen.

### <a name="credit-limit-used"></a>Brugt kreditgrænse

Vælg **Anvendt kreditmaks.**, hvis blokeringsreglen gælder for kundens anvendte kreditmaks.beløb.
1. Vælg det kundeinterval, som denne regel **gælder for**.
   - Vælg **Tabel**, hvis reglen gælder for en bestemt kunde.
   - Vælg **Gruppe**, hvis reglen gælder for en kundegruppe. 
   - Vælg **Alle**, hvis reglen gælder for alle kunder.
2. Når du har angivet intervallet, skal du angive den **Konto/gruppe**, der bruges i intervallet.
   - For intervallet **Tabel** giver opslaget et kundeopslag. 
   - Vælg en **Gruppe**, hvis reglen gælder for en kundestyringsgruppe.
   - Vælg **Alle**, hvis reglen gælder for alle kunder. 
3. Vælg en **Risikogruppe**, hvis du yderligere vil begrænse listen over kunder, der skal sættes på kreditstyringshold. 
4. Vælg den regeltype, du konfigurerer.
   - Vælg **Blokering** for at oprette en regel, der blokerer en ordre. 
   - Vælg **Udelukkelse** for at oprette en regel, der udelukker en anden regel fra at blokere en ordre. 
5. Vælg den **Resterende grænseværdi**, som definerer den procentdel af kreditmaks., der blokerer salgsordren. Hvis værdien af en ordre øger det kreditmaks.beløb, der er brugt over procentdelen, sættes ordren på hold. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Sætte en salgsordre på hold ud fra andre kriterier
  
### <a name="rank-payment-terms"></a>Ranger betalingsbetingelser  

Du kan tvinge reglerne for kreditstyring til at træde i kraft, når betalingsbetingelser ændres. Du skal rangere betalingsbetingelserne og tildele dem en rangeringsværdi. Hvis du ændrer betalingsbetingelserne i ordren til betalingsbetingelser, der er rangeret højere end de gamle betalingsbetingelser, sendes ordren til kreditstyring og kræver godkendelse.

Du kan konfigurere rangeringen af betalingsbetingelser på siden **Kreditstyring > Konfiguration > Konfiguration af kreditstyring > Ranger betalingsbetingelser**.

1. Vælg de betalingsbetingelser i feltet **Betalingsbetingelser**, der skal rangeres. Når du vælger en betingelse, vises beskrivelsen i feltet **Beskrivelse**.
2. Vælg betingelsens rangering i feltet **Rangering**. Værdierne er alle relative i forhold til hinanden, så du kan bruge 1,2,3 eller 10,20,30. Du kan også bruge den samme værdi for de fleste betalingsbetingelser, så det kun er én eller to betalingsbetingelser, der udløser kreditkontrollen.

### <a name="rank-settlement-discounts"></a>Ranger udligningsrabatter   

Du kan tvinge reglerne for kreditstyring til at træde i kraft, når afregningsrabatter ændres. Du skal rangere afregningsrabatterne og tildele dem en rangeringsværdi. Hvis du ændrer afregningsrabatterne i ordren til afregningsrabatter, der er rangeret højere end de gamle afregningsrabatter, sendes ordren til kreditstyring og kræver godkendelse.

Du kan konfigurere rangeringen af betalingsbetingelser på siden **Kreditstyring > Konfiguration > Konfiguration af kreditstyring > Ranger afregningsrabatter**.

1. Vælg den **Kasserabat**, du vil rangere. **Beskrivelsen** af afregningsrabatten vises.
2. Vælg værdien for **Rangering**. Værdierne er alle relative i forhold til hinanden, så du kan bruge 1,2,3 eller 10,20,30. Du kan også bruge den samme værdi for de fleste afregningsrabatter, så det kun er én eller to afregningsrabatter, der udløser kreditkontrollen.

## <a name="sequence-the-application-of-rules"></a>Anbringe anvendelse af regler i rækkefølge

Regler køres i en bestemt rækkefølge, som du ændrer alt efter organisationens behov. 

- Én forekomst af reglerne for udelukkelse af en salgsordre giver dig mulighed for at tilsidesætte alle regler, der kan blokere en salgsordre. Opret en regel for udelukkelse af en salgsordre, og vælg indstillingen **Frigiv salgsordrepluk**. Ordren sættes ikke på hold, hvis denne udelukkelsesregel er sand, og der ikke vil blive kontrolleret andre regler.
- Blokeringsregler kan sætte ordren på hold.
- Udelukkelsesregler køres efter blokeringsregler. Udelukkelsesregler påvirker kun den regel, de er defineret for. 
- Blokerings- og udelukkelsesregler køres i Tabel, derefter Gruppe og slutteligt Alle ordrer. På grund af denne behandlingsrækkefølge er det muligt at have en blokeringsregel på niveauet Alle, der ikke køres, fordi der køres en udelukkelsesregel på niveauet Tabel eller Gruppe.
- Udelukkelser tilsidesætter ikke blokeringsreglen, hvis de findes på samme niveau. F.eks. tilsidesætter en udelukkelsesregel på gruppeniveauet ikke blokeringsreglen på gruppeniveauet. Du behøver at ikke konfigurere udelukkelser på niveauet Alle ud over som som angivet ovenfor med den enkelte forekomst af udelukkelsesreglen for salgsordren. 

Funktionen af reglen **Anvendt kreditmaks.** ændres baseret på indstillingerne for parameteren **Kontrollér kreditmaks. på salgsordre** i parameterformen Kredit og inkasso.
- Hvis parameteren er angivet til Nej, køres reglen for Anvendt kreditmaks. ikke.
- Hvis parameteren er angivet til Ja, og **Besked ved overskridelse af kreditmaks.** er angivet til advarsel, vises der en advarsel, når kreditmaks. er overskredet. Reglerne for **Anvendt kreditmaks.** køres for at se, om du har regler, der skal køres. I dette scenarie vil du dog normalt ikke have brug for at tilføje nogen regler.
- Hvis parameteren er angivet til Ja, og **Besked ved overskridelse af kreditmaks.** er angivet til fejl, kontrolleres kreditmaks., og ordren sættes på hold, hvis kreditmaks. overskrides. Reglerne for **Anvendt kreditmaks.** køres desuden for at se, om der er andre regler, der skal køres. Der vises ikke en fejlmeddelelse, men blokeringsårsagen for **Kreditmaks. overskredet** vil blive vist. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Indstillinger, der ændrer måden, hvorpå en ordre sættes på hold

Ordrer kan udelukkes fra kreditstyring, selvom der er konfigureret regler. 

- Hvis du ændrer indstillingerne **Udeluk kunde fra kreditstyring** i oversigtspanelet **Alle kunder > Vælg en kunde > Kredit og inkasso** til **Ja**, behandles der ingen ordrer for den pågældende kunde
- Hvis du ændrer værdien **Udeluk fra kreditstyring** på **salgsordrehovedet** på **oversigtspanelet Kreditstyring** til **Ja**, behandles reglerne for kreditstyring ikke. Denne indstilling kan kun udføres af kreditmedarbejderen eller kreditchefen.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Behandle ordrer på hold ved hjælp af listen over kreditstyringshold

Listen over kreditstyringshold giver kreditchefer en oversigt over alle salgsordrer, der er sat på hold, og giver dem mulighed for at fjerne pågældende hold, når de kreditmæssige problemer er afhjulpet. Siden **Liste over kreditstyringshold** viser alle salgsordrer, der er sat på hold. Du kan få vist listen over hold på siden **Alle kredithold** (**Kreditstyring > Liste over kreditstyringshold> Alle kredithold**).
Salgsordrer fra alle juridiske enheder sendes til samme liste over kreditstyringshold og giver en centraliseret oversigt over alle de transaktioner, der kræver opmærksomhed. Brugere kan kun se oplysninger for de juridiske enheder, de har adgang til.

En salgsordre kan sættes på listen over hold af følgende årsager:
1. Kunden har en faktura, der har været forfalden i et bestemt antal dage. 
2. Ordren har en bestemt kontostatus.
3. Ordren har bestemte betalingsbetingelser.
4. Kunden har et udløbet kreditmaks.
5. Kunden har et forfaldent beløb og har brugt en bestemt procentdel af kreditmaks.
6. Salgsordren overskrider et bestemt beløb.
7. Kunden har overskredet en vis procentdel af kreditmaks.
8. Betalingsbetingelserne afviger fra standardbetalingsbetingelserne for kunden.
9. Afregningsrabatterne afviger fra standardafregningsrabatten for kunden.

Blokeringsårsagen vises for hver salgsordre på listen over hold. Hvis der er mere end én årsag til pågældende hold, vises årsagen som **Flere**. Du kan bruge menuen **Blokeringsårsager** i handlingsruden for at få vist alle årsagerne til, at salgsordren blev sat på hold. Du kan også få vist **Blokeringsårsager** i en faktaboks.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Frigive ordrer fra listen over hold til behandling

Når du har undersøgt årsagerne til pågældende hold, og du har afhjulpet dem, kan du frigive salgsordrerne til yderligere behandling.

1) Vælg en linje på listen over hold. Du kan frigive flere ordrer ved at vælge mere end én linje.
2) Vælg en **Frigivelsesårsag** for den ordre, der er valgt til frigivelse.  
3) Vælg en **Dato for gennemsyn** for hver ordre, der er valgt til frigivelse.  
4) Vælg menuen **Frigiv** i handlingsruden for at frigive en ordre. Denne menu er kun tilgængelig, når der er valgt transaktioner. Brugeren får vist to muligheder:
   - Vælg **Med bogføring** for at fjerne pågældende hold, og bogfør dokumentet ved at bruge samme bogføringsproces, der blev brugt, da det blev sat på hold. Hvis salgsordrebekræftelsen f.eks. blev sat på hold, fuldføres salgsordrebekræftelsen efter frigivelsen. Bogføringen af salgsordren vises, så brugeren kan bogføre bekræftelsen.
   - Vælg **Uden bogføring** for at fjerne pågældende hold uden yderligere behandling. Salgsordren kan bogføres manuelt.

### <a name="rejecting-orders-in-the-hold-list"></a>Afvise ordrer på listen over hold
Du kan bruge menuen **Afvis** i handlingsruden for at afvise en salgsordre.
1. Vælg en linje på listen over hold. Du kan frigive flere ordrer ved at vælge mere end én linje.
2. Ordren fjernes fra listen over hold, og salgsordrehovedet opdateres for at vise, at ordren blev afvist.

### <a name="automatically-releasing-credit-management-holds"></a>Automatisk frigivelse af kreditstyringshold
Salgsordrer sættes på listen over hold baseret på blokeringsreglerne. Nogle årsager til pågældende hold kan dog ændres med tiden, hvis salgsordren forbliver på listen over hold i en vis periode. En kunde kan f.eks. betale sin regning og derved frigøre kreditmaks. 

Du kan bruge menuen **Evaluer til frigivelse** for at gennemgå salgsordrerne på listen over hold og automatisk frigive dem, hvis årsagen til hold er afhjulpet.
1.  Vælg menuen **Evaluer til frigivelse**.
2.  Vælg **Behandl blokeringsregler** for at gennemgå alle salgsordrerne. Vælg **Behandl blokeringsregler for valgte linjer** for kun at få vist de linjer, du har valgt.
3. Der vises en skyder, så du kan vælge en enkelt kunde. Lad rullelisten over kunder stå tom for alle kunder. 
4. Når du klikker på OK, køres processen i baggrunden, og du kan fortsætte med at arbejde på andre opgaver. Hvis du vælger batchproces, før du klikker på OK, køres processen i batch, når du klikker på OK. Det kan tage noget tid at behandle de ordrer, der er på hold på listen, så du kan bruge Opdater for opdatere statussen for ordrerne. 
5.  Hvis en blokeringsårsag ikke længere er tilgængelig for en ordre, betragtes blokeringsårsagen som ikke længere værende gyldig, og du vil ikke længere kunne se en markering ud for årsagen, når du får vist blokeringsårsagerne.
6.  Hvis alle blokeringsårsagerne er ryddet, tilføjes en ny årsag, **Klar til frigivelse**, på listen over blokeringsårsager. Salgsordren kan frigives automatisk.
7.  Hvis parameteren **Frigiv automatisk** på fanen **Kredit og inkasso > Konfiguration > Parametre for Kredit og inkasso > Kredit > Frigiv automatisk** er angivet til **Med bogføring**, vil du blive bedt om at bogføre ved hjælp af bogføringsformen for det dokument, der blev blokeret.
8.  Hvis parameteren **Frigiv automatisk** på fanen **Kredit og inkasso > Konfiguration > Parametre for Kredit og inkasso > Kredit > Frigiv automatisk** er angivet til **Uden bogføring**, skal du bogføre ordren manuelt.

### <a name="credit-management-approval-workflow"></a>Arbejdsgang for godkendelse af kreditstyring

Du kan også oprette **Arbejdsgange for kreditstyring** for at styre frigivelsen af kredithold. Når du har konfigureret en arbejdsgang på siden **Kreditstyring > Konfiguration > Arbejdsgange for kreditstyring**, sendes de ordrer, der er markeret til frigivelse eller afvisning, til arbejdsgangen, hvor de skal godkendes først, før de frigives eller afvises. 

Hvis du medtager opgaverne til frigivelse med bogføring eller frigivelse uden at bogføre i arbejdsgangen, frigiver godkendelsen af arbejdsgangen også salgsordren. Men hvis der opstår en fejl i frigivelsesprocessen pga. manglende konfigurationsoplysninger eller andre årsager, skal du tilbagekalde salgsordren fra arbejdsgangen, løse det problem, der forårsagede fejlen, og derefter sende ordren til arbejdsgangen igen.

Hvis du ikke medtager opgaverne til frigivelse med bogføring eller frigivelse uden at bogføre i arbejdsgangen, giver godkendelsesprocessen for arbejdsgangen dig blot mulighed for at frigive salgsordren manuelt, når godkendelsen er fuldført.

### <a name="forced-credit-hold"></a>Tvunget kredithold  
  
På visse tidspunkter kan det være nødvendigt at blokere salgsordrer, selvom ordren ikke opfylder kriterierne i blokeringsreglerne. En kreditchef kan f.eks. få besked om et ikke-kreditrelateret problem med kunden og beslutte at sætte ordrer manuelt på hold, umiddelbart indtil problemet er løst. Du kan manuelt gennemtvinge en salgsordre til at sættes på hold, hvis pågældende situation opstår.

1. Åbn den salgsordre, du vil sætte på hold.  
2. Vælg **Gennemtving kredithold** på fanen **Kreditstyring** i handlingsruden **Kreditstyring**.
3. Vælg **Årsag til gennemtvunget hold**.
4. Klik på **OK**. Salgsordren returneres til listen over kreditstyringshold.

Du kan også gennemtvinge, at flere ordrer skal sættes på hold på siden **Kreditstyring > Periodiske opgaver > Gennemtving kredithold**. Du kan f.eks. sætte alle salgsordrer på hold for en bestemt kunde.
1. Vælg **Årsag til gennemtvunget hold**. 
2. Klik **Poster, der skal indgå** for at vælge de salgsordrer, der skal sættes på hold. 
3. Klik på **OK** for at behandle de valgte salgsordrer.

Salgsordrer, der er gennemtvunget på hold, kan ikke behandles med arbejdsgangen.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Frigivelse af ordrer, der er føjet til listen over kreditstyringshold med et gennemtvunget kredithold
Salgsordrer med en årsag til gennemtvunget hold kan ikke frigives automatisk. Hvis salgsordren er gennemtvunget på hold, og du har brugt en proces, der automatisk frigiver salgsordrer, vises salgsordren som **Klar til frigivelse** og forbliver på listen over hold. Du skal bruge menuen **Frigiv** til at frigive ordren.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Understøttelse af fritekstfakturaer, ordrer og projektfakturaer i Kreditstyring 
Kreditstyring kan i øjeblikket kun bruges til salgsordrer. Fritekstfakturaer, POS-salgsordrer og callcenter-ordrer bruger det midlertidige kreditmaks. og den forsikring/de garantier, du tilføjer, til at regulere kreditmaks. De bruger ikke blokeringsreglerne, og de sættes ikke på listen over, hvis der er et problem med kreditmaks.

Projektfakturaer understøttes ikke i kreditstyring.
