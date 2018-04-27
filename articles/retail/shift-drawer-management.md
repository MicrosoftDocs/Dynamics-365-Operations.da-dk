---
title: Styring af skift og kasseapparater
description: "I denne artikel beskrives, hvordan du konfigurerer og bruger de to typer detail-POS-skift – delt og separat. Delte skift kan bruges af flere brugere på flere steder, hvorimod separate skift kun kan bruges af én arbejder ad gangen."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---

# <a name="shift-and-cash-drawer-management"></a>Styring af skift og kasseapparater

[!INCLUDE [banner](includes/banner.md)]

I denne artikel beskrives, hvordan du konfigurerer og bruger de to typer detail-POS-skift – delt og separat. Delte skift kan bruges af flere brugere på flere steder, hvorimod separate skift kun kan bruges af én arbejder ad gangen.

Der er to typer af POS-skift (Point Of Sale): separate og delte. Separate skift kan kun bruges af én arbejder ad gangen. Delte skift kan bruges af flere brugere på flere steder. Derfor skaber de grundlæggende et enkelt skift for flere arbejdere i en butik.

## <a name="standalone-shifts"></a>Separate skift
Separate skift bruges i et traditionelt, fast POS-scenarie, hvor kontanter afstemmes uafhængigt for hvert POS-kasseapparat. For eksempel er der i en butik normalt flere faste POS-kasseapparater og en kasserer, der er tildelt til hvert kasseapparat. I sådanne tilfælde bruges der sandsynligvis et separat skift til hvert kasseapparat, og kassereren er ansvarlig for pengeskuffen eller fysiske kontanter for dette kasseapparat. Et separat skift omfatter alle aktiviteter for dette kasseapparat under kassererens holdskifte. Aktiviteter kan omfatte startbeløbet, der er deponeret i pengeskuffen, al fjernelse og tilføjelse af kontanter under aktiviteter som f.eks. indsættelser i banken og kassebeholdning, og kasseoptællingen i slutningen af skiftet.

### <a name="set-up-a-stand-alone-shift"></a>Oprette et separat skift

Et separat skift angives på kasseapparatniveau. I denne fremgangsmåde beskrives, hvordan du konfigurerer et separat skift for et POS-kasseapparat.

1.  Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwareprofiler**.
2.  Vælg hardwareprofilen, der skal bruges til det separate skift.
3.  I oversigtspanelet **Kasseskuffe** skal du kontrollere, at indstillingen **Skuffe til delt skift** er indstillet til **Nej**.
4.  Klik på **Gem**.
5.  Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**.
6.  Vælg det kasseapparat, der kræver et separat skift, og klik derefter på **Rediger**.
7.  I feltet **Hardwareprofil** skal du vælge den hardwareprofil, du valgte i trin 2.
8.  Klik på **Gem**.
9.  Klik på **Detail** &gt; **Detail-it** &gt; **Distributionsplan**.
10. Vælg distributionsplanen **1090**, og klik derefter på **Kør nu** for at synkronisere ændringer i POS.

### <a name="use-a-stand-alone-shift"></a>Bruge et separat skift

1.  Log på POS'et.
2.  Hvis der ikke er nogen åbne skift, skal du vælge **Åbn et nyt skift**.
3.  Gå til aktiviteten **Angiv startbeløb**, og angiv det pengebeløb, der føjes til pengeskuffen ved arbejdsdagens begyndelse.
4.  Udfør transaktioner.
5.  Ved dagens slutning skal du vælge **Foretag kasseoptælling** for at optælle det beløb, der forbliver i kassen.
6.  Angiv kontantbeløbet, og klik derefter på **Gem** for at gemme kasseoptællingen.
7.  Vælg **Luk skift** at lukke skiftet.

**Bemærk:** Andre handlinger er tilgængelige under skiftet, afhængigt af de forretningsprocesser der findes. Handlingerne **Deponering til pengeskab**, **Indsættelse i banken** og **Fjernelse af betalingsmiddel** kan bruges til at fjerne penge fra pengeskuffen i dagens løb, eller før skiftet lukkes. Hvis der kommer til at mangle kontanter i en pengeskuffe, kan handlingen **Kassebeholdning** bruges til at tilføje kontanter i skuffen.

## <a name="shared-shifts"></a>Delte skift
Et delt skift bruges i et miljø, hvor flere kasserere deler et kasseapparat eller et sæt af kasseapparater i løbet af arbejdsdagen. Normalt bruges et delt skift i POS-miljøer på mobilenheder. I et mobilmiljø tildeles hver kasserer ikke en enkelt kasseapparat, som han eller hun er ansvarlig for. I stedet for skal alle kasserere kunne foretage et salg og tilføje kontanter til det nærmeste kasseapparat. I dette scenarie indgår de kasseapparater, der deles mellem kasserere, i et delt skift. Alle kasseapparater i et delt skift er inkluderet i det samme skift med henblik på aktiviteter, der vedrører kontantstyring for dette skift. Startbeløbet for skiftet bør derfor omfatte summen af alle kontanter i alle kasseapparater, der findes i det delte skift. Ligeledes skal kasseoptællingen være summen af alle kontanter i alle kasseapparater, der indgår i det delte skift. **Bemærk:** Kun ét delt skift kan være åbent ad gangen i hver butik. Delte skift og separate skift kan bruges i samme butik.

### <a name="set-up-a-shared-shift"></a>Konfigurere et delt skift

1.  Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwareprofiler**.
2.  Vælg hardwareprofilen, der skal bruges til det delte skift.
3.  I oversigtspanelet **Kasseskuffe** skal du vælge indstillingen **Ja** for **Skuffe til delt skift**.
4.  Klik på **Gem**.
5.  Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**.
6.  Vælg det kasseapparat, der kræver et delt skift, og klik derefter på **Rediger**.
7.  I feltet **Hardwareprofil** skal du vælge den hardwareprofil, du valgte i trin 2.
8.  Klik på **Gem**.
9.  Klik på **Detail** &gt; **Detail-it** &gt; **Distributionsplan**.
10. Vælg distributionsplanen **1090**, og klik derefter på **Kør nu** for at synkronisere ændringer i POS.

### <a name="use-a-shared-shift"></a>Bruge et delt skift

1.  Log på POS'et.
2.  Hvis POS'et endnu ikke er forbundet med en hardwarestation, skal du vælge **handling uden for pengeskuffe** og derefter vælge handlingen **Vælg hardwarestation** for at gøre en hardwarestation aktiv for det delte skift. Dette trin er kun obligatorisk første gang, et kasseapparat føjes til et miljø for et delt skift.
3.  Log af POS, og log derefter på igen.
4.  Vælg **Opret et nyt skift**.
5.  Vælg **Angiv startbeløb**.
6.  Angiv startbeløbet for alle kasseapparater i den butik, som er en del af det delte skift, og klik derefter på **Gem**.
    -   For at føje en del af startbeløbet til hver efterfølgende kasseapparat, skal du bruge handlingen **Vælg hardwarestation** for at aktivere hardwarestationen.
    -   For at føje en pengeskuffe til et bestemt kasseapparat, skal du bruge handlingen **Åbn kasseskuffe**.
    -   Fortsæt indtil alle kasseapparater i det delte skift har deres del af startbeløbet.

7.  Ved dagens slutning skal du åbne hvert kasseapparat og fjerne kontanterne.
8.  Når du har fjernet kontanterne fra det sidste kasseapparat, skal du tælle alle beløbene fra alle kasseapparater.
9.  Brug handlingen **Foretag kasseoptælling** til at optælle det samlede kontantbeløb fra alle kasseapparater, der indgår i det delte skift.
10. Brug handlingen **Luk skift** til at lukke det delte skift.

## <a name="shift-operations"></a>Operationer for skift
Der kan foretages forskellige handlinger for at ændre tilstanden for et skift eller for at forøge eller formindske det pengebeløb, der i skuffen. Afsnittet nedenfor beskriver disse operationer for skift til Dynamics 365 for Retail Modern POS og Cloud POS.

**Åbne skift**

POS kræver, at en bruger har et aktivt åbent skift for at udføre operationer, der resulterer i en økonomisk transaktion, f.eks. et salg, en returnering eller en kundeordre.  

Når der logges på POS, kontrollerer systemet først, om brugeren har et aktivt skift tilgængeligt på det aktuelle kasseapparat. Hvis det ikke er tilfældet, kan brugeren derefter vælge at åbne et nyt skift, genoptage et eksisterende skift eller fortsætte med at logge på i tilstanden "uden pengeskuffe", afhængigt af systemkonfigurationen og den pågældendes tilladelse.

**Angiv startbeløb**

Denne handling er ofte den første handling, der udføres i et skift, der netop er åbnet. Brugerne angiver startbeløbet for kontanter i kasseskuffen for skiftet. Det er vigtigt, da beregningen af over/under beløb i kassen, der foretages, når et skift lukkes, tager udgangspunkt i dette beløb.

**Kassebeholdning**

Flydende poster er ikke-salgstransaktioner, der udføres i et aktivt skift, og de øger mængden af kontanter i kasseskuffen. Et almindeligt eksempel på en flydende tilgang kan være tilføjelsen af yderligere byttepenge til kasseskuffen, når den er ved at være tom.

**Fjernelse af betalingsmiddel**

Fjernelse af betalingsmidler er ikke-salgstransaktioner, der udføres i et aktivt skift for at reducere mængden af kontanter i kasseskuffen. Dette bruges som regel sammen med en flydende tilgang på et andet skift. Hvis kasseskuffe 1 f.eks. mangler byttepenge, så fortager brugeren på kasseskuffe 2 en fjernelse af betalingsmiddel for at reducere beløbet i kasseskuffen. Brugeren på kasseapparat 1 udfører derfor en flydende tilgang for at øge beløbet i kasseskuffen.

**Afbryd skifte**

Brugere kan afbryde deres aktive skift for at frigøre det aktuelle kasseapparat til en anden bruger, eller for at flytte deres skift til et andet kasseapparat (dette kaldes ofte kaldet en "flydende pengeskuffe"). 

Afbrydelse af skiftet forhindrer eventuelle nye transaktioner eller ændringer af skiftet, indtil det genoptages.

**Genoptag skift**

Denne handling giver en bruger mulighed for at genoptage et tidligere afbrudt skift på et kasseapparat, der ikke allerede har et aktivt skift.

**Kasseoptælling**

Kasseoptællingen er en handling, som brugeren udfører for at angive det samlede pengebeløb, der i øjeblikket er i kassen, oftest før lukningen af skiftet. Dette er den værdi, der sammenlignes med det forventede skift, for at beregne over/under beløb.

**Deponering til pengeskab**

Deponeringer til pengeskab kan udføres når som helst på et aktivt skift. Denne handling fjerner penge fra kassen, så den kan overføres til en mere sikker placering, f.eks. et pengeskab i baglokalet. Det samlede beløb, der er registreret til deponering i pengeskab, indgår stadig i totalerne for skiftet, men det skal ikke tælles med som en del af kasseoptællingen.

**Indsættelse i banken**

I lighed med deponering til pengeskab udføres indsættelser i banken også på aktive skift. Denne handling fjerner penge fra skiftet for at forberede bankindbetalingen.

**Luk skifte uden kontrol**

Et skjult lukket skift er et skift, der ikke længere er aktivt, men som endnu ikke er helt lukket. Skjulte lukkede skift kan ikke genoptages som et afbrudt skift, men procedurer, f.eks. angivelse af startbeløb og kasseoptællinger, kan udføres på et senere tidspunkt eller fra et andet kasseapparat.

Skjulte lukkede skift bruges ofte til at frigøre et kasseapparat til en ny bruger eller et nyt skift, uden at der først skal foretages fuld optælling, afstemning og lukning af skiftet. 

**Luk skift**

Denne handling beregner totaler for skift, over/under beløb og færdiggør derefter et aktivt eller et skjult lukket skift. Lukkede skift kan ikke genoptages eller ændres.  

**Administrer skift**

Denne handling giver brugerne mulighed for at få vist alle aktive, afbrudte eller skjulte lukkede skift. Afhængigt af deres rettigheder kan brugerne udføre deres endelige lukningsprocedurer, f.eks. kasseoptælling og lukning af skjulte lukkede skift. Denne handling tillader også brugere at få vist og slette ugyldige skift i de sjældne tilfælde, hvor et skift er efterladt i fejlbehæftet tilstand efter omstilling mellem offline- og onlinetilstand. Disse ugyldige skift indeholder ikke nogen økonomiske oplysninger eller transaktionsdata, der skal bruges til afstemning. 

