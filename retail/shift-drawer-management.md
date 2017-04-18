---
title: Styring af skift og kasseapparater
description: "Denne artikel forklarer, hvordan du konfigurerer og bruger de to typer af salg (POS) skiftehold - delt og enkeltstående retail punkt. Delte skift kan bruges af flere brugere på flere steder, hvorimod separate skift kun kan bruges af én arbejder ad gangen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 09c7fce1fa83d6a8d6391db667b7260d2a199390
ms.lasthandoff: 03/31/2017


---

# <a name="shift-and-cash-drawer-management"></a>Styring af skift og kasseapparater

Denne artikel forklarer, hvordan du konfigurerer og bruger de to typer af salg (POS) skiftehold - delt og enkeltstående retail punkt. Delte skift kan bruges af flere brugere på flere steder, hvorimod separate skift kun kan bruges af én arbejder ad gangen.

Der er to typer af POS-skift (Point Of Sale): separate og delte. Separate skift kan kun bruges af én arbejder ad gangen. Delte skift kan bruges af flere brugere på flere steder. Derfor skaber de grundlæggende et enkelt skift for flere arbejdere i en butik.

## <a name="standalone-shifts"></a>Enkeltstående skiftehold
Separate skift bruges i et traditionelt, fast POS-scenarie, hvor kontanter afstemmes uafhængigt for hvert POS-kasseapparat. For eksempel er der i en butik normalt flere faste POS-kasseapparater og en kasserer, der er tildelt til hvert kasseapparat. I sådanne tilfælde bruges der sandsynligvis et separat skift til hvert kasseapparat, og kassereren er ansvarlig for pengeskuffen eller fysiske kontanter for dette kasseapparat. Et separat skift omfatter alle aktiviteter for dette kasseapparat under kassererens holdskifte. Aktiviteter kan omfatte startbeløbet, der er deponeret i pengeskuffen, al fjernelse og tilføjelse af kontanter under aktiviteter som f.eks. indsættelser i banken og kassebeholdning, og kasseoptællingen i slutningen af skiftet.

### <a name="set-up-a-stand-alone-shift"></a>Oprette et separat skift

Et separat skift angives på kasseapparatniveau. I denne fremgangsmåde beskrives, hvordan du konfigurerer et separat skift for et POS-kasseapparat.

1.  Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**profiler for POS**&gt;**hardwareprofiler**.
2.  Vælg hardwareprofilen, der skal bruges til det separate skift.
3.  I oversigtspanelet **Kasseskuffe** skal du kontrollere, at indstillingen **Skuffe til delt skift** er indstillet til **Nej**.
4.  Click **Save**.
5.  Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**registrerer**.
6.  Vælg det kasseapparat, der kræver et separat skift, og klik derefter på **Rediger**.
7.  I feltet **Hardwareprofil** skal du vælge den hardwareprofil, du valgte i trin 2.
8.  Click **Save**.
9.  Klik på **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplan**.
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
Et delt skift bruges i et miljø, hvor flere kasserere deler et kasseapparat eller et sæt af kasseapparater i løbet af arbejdsdagen. Normalt bruges et delt skift i POS-miljøer på mobilenheder. I et mobilmiljø tildeles hver kasserer ikke en enkelt kasseapparat, som han eller hun er ansvarlig for. I stedet for skal alle kasserere kunne foretage et salg og tilføje kontanter til det nærmeste kasseapparat. I dette scenarie indgår de kasseapparater, der deles mellem kasserere, i et delt skift. Alle kasseapparater i et delt skift er inkluderet i det samme skift med henblik på aktiviteter, der vedrører kontantstyring for dette skift. Startbeløbet for skiftet bør derfor omfatte summen af alle kontanter i alle kasseapparater, der findes i det delte skift. Ligeledes skal kasseoptællingen være summen af alle kontanter i alle kasseapparater, der indgår i det delte skift. **Bemærk:** kun én delt Skift kan være åben ad gangen i hver butik. Delte skift og separate skift kan bruges i samme butik.

### <a name="set-up-a-shared-shift"></a>Konfigurere et delt skift

1.  Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**profiler for POS**&gt;**hardwareprofiler**.
2.  Vælg hardwareprofilen, der skal bruges til det delte skift.
3.  I oversigtspanelet **Kasseskuffe** skal du vælge indstillingen **Ja** for **Skuffe til delt skift**.
4.  Click **Save**.
5.  Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**registrerer**.
6.  Vælg det kasseapparat, der kræver et delt skift, og klik derefter på **Rediger**.
7.  I feltet **Hardwareprofil** skal du vælge den hardwareprofil, du valgte i trin 2.
8.  Click **Save**.
9.  Klik på **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplan**.
10. Vælg distributionsplanen **1090**, og klik derefter på **Kør nu** for at synkronisere ændringer i POS.

### <a name="use-a-shared-shift"></a>Bruge et delt skift

1.  Log på POS'et.
2.  Hvis POS'et endnu ikke er forbundet med en hardwarestation, skal du vælge **handling uden for pengeskuffe** og derefter vælge handlingen **Vælg hardwarestation** for at gøre en hardwarestation aktiv for det delte skift. Dette trin er kun obligatorisk første gang, et kasseapparat føjes til et miljø for et delt skift.
3.  Log af POS, og log derefter på igen.
4.  Vælg **Opret et nyt skift**.
5.  Vælg **Angiv startbeløb**.
6.  Angiv startbeløbet for alle kasseapparater i den butik, som er en del af det delte skift, og klik derefter på **Gem**.
    -   For at føje en del af startbeløbet til hver efterfølgende kasseapparat, skal du bruge handlingen **Vælg hardwarestation **for at aktivere hardwarestationen.
    -   For at føje en pengeskuffe til et bestemt kasseapparat, skal du bruge handlingen **Åbn kasseskuffe**.
    -   Fortsæt indtil alle kasseapparater i det delte skift har deres del af startbeløbet.

7.  Ved dagens slutning skal du åbne hvert kasseapparat og fjerne kontanterne.
8.  Når du har fjernet kontanterne fra det sidste kasseapparat, skal du tælle alle beløbene fra alle kasseapparater.
9.  Brug handlingen **Foretag kasseoptælling** til at optælle det samlede kontantbeløb fra alle kasseapparater, der indgår i det delte skift.
10. Brug handlingen **Luk skift** til at lukke det delte skift.


