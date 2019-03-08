---
title: Styring af skift og kasseapparater
description: I dette emne forklares, hvordan du opretter og bruger skiftehold i detail-POS.
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 7ad3c3fd17e88f364be12c122e2f5c155b7b9064
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "313008"
---
# <a name="shift-and-cash-drawer-management"></a>Styring af skift og kasseapparater

[!include [banner](includes/banner.md)]

I dette emne forklares, hvordan du opretter og bruger skiftehold i detail-POS.

I Microsoft Dynamics 365 for Retail, beskriver betegnelsen *Skift* samlingen af POS-transaktionsdata og aktiviteter mellem to tidspunkter. For hvert skifte sammenlignes det forventede pengebeløb med det beløb, der er optalt og indberettet.

Skiftehold åbnes typisk i begyndelsen af arbejdsdagen. På dette tidspunkt kan en bruger opgøre startbeløbet, som pengeskuffen indeholder. Salgstransaktioner udføres derefter i løbet af dagen. I slutningen af dagen, tælles kasseskuffen og slutbeløbene angives. Skiftet lukkes, og der oprettes en Z-rapport. Z-rapporten angiver, om der er overskud eller tab.

## <a name="typical-shift-scenarios"></a>Typiske skifteholdsscenarier

Retail indeholder flere konfigurationsindstillinger og POS-handlinger for at understøtte en lang række forretningsprocesser i slutningen af dagen for POS. I dette afsnit beskrives nogle typiske skifteholdsscenarier.

### <a name="fixed-till"></a>Fast pengeskuffe

Dette scenario er traditionelt anvendt oftest. Den bruges stadig i vidt omfang. I et skifte med "fast pengeskuffe" er skiftet og pengeskuffen knyttet til et bestemt kasseapparat. De flyttes ikke fra ét kasseapparat til et andet. Et skifte med "fast pengeskuffe" kan bruges af en enkelt bruger eller deles af flere brugere. Skifte med "fast pengeskuffe" kræver ikke nogen særlig konfiguration.

### <a name="floating-till"></a>Flydende pengeskuffe

I et skifte med "flydende pengeskuffe" kan skiftet og pengeskuffen flyttes fra ét kasseapparat til et andet. Selvom et kasseapparat kun kan have ét aktivt skift pr. pengeskuffe, kan skift afbrydes og derefter genoptages senere på et andet kasseapparat.

En butik har f.eks. to kasseapparater. Hvert kasseapparat åbnes i starten af dagen, når kassereren åbner et nyt skift og udleverer startbeløbet. Når én kasserer er klar til at holde pause, stopper vedkommende sit skift og fjerner pengeskuffen fra kasseapparatet. Kasseapparatet bliver derefter tilgængeligt for andre kasserere. En anden kasserer kan logge på og åbne sit eget skift på kasseapparatet. Når den første kasserers pause er slut, kan den pågældende kasserer genoptage sit skift, når et af de andre kasseapparater bliver tilgængelig. Skifte med "flydende pengeskuffe" kræver ikke nogen særlig konfiguration eller tilladelse.

### <a name="single-user"></a>Enkeltbruger

Mange detailhandlere foretrækker kun at tillade én bruger pr. skift, for at sikre det højeste niveau af pålidelighed med hensyn til kontanter i pengeskuffen. Hvis der kun er én bruger, der har tilladelse til at bruge den pengeskuffe, der er knyttet til et skift, er den pågældende bruger alene ansvarlig for eventuelle uoverensstemmelser. Hvis der er mere end én bruger på et skift, er det vanskeligt at bestemme, hvem der har foretaget en fejl, eller hvem der måske forsøger at stjæle fra pengeskuffen.

### <a name="multiple-users"></a>Flere brugere

Nogle detailhandlere er villige til at ofre det ekstra niveau af pålidelighed, som skift med enkeltbruger giver, og tillader flere brugere pr. skift. Denne metode bruges typisk, når der er flere brugere end tilgængelige kasseapparater, og behovet for fleksibilitet og hastighed opvejer risikoen for tab. Det bruges også typisk, når butikschefer ikke har deres egne skift, men efter behov bruger skiftene på et af kasseapparaterne. For at kunne logge på og bruge et skift, der blev åbnet af en anden bruger, skal en bruger have POS-rettigheden **Tillad logon på flere skifter**.

### <a name="shared-shift"></a>Delt skift

Konfigurationen "delt skift" giver detailhandlere mulighed for at have et enkelt skift på tværs af flere kasseapparater, pengeskuffer og brugere. Et delt skift har et enkelt startbeløb og et enkelt lukkebeløb, der opsummeres på tværs af alle pengeskuffer. Delte skift er især typiske, når der bruges mobile enheder. I dette scenario er der ikke reserveret en separat pengeskuffe til hvert kasseapparat. I stedet kan alle kasseapparater dele en pengeskuffe.

Hvis delte skift skal bruges i en butik, skal pengeskuffen konfigureres som en "skuffe til delt skift" på **Detail \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler \> Kasseskuffe**. Brugere skal desuden have rettigheder til et eller flere af de delte skift (Tillad administration af delt skift og Tillad brug af delt skift).

> [!NOTE]
> Der kan kun være ét delt skift åbent ad gangen i hver butik. Delte skift og separate skift kan bruges i samme butik.

## <a name="shift-and-drawer-operations"></a>Skift- og skuffehandlinger

Der kan foretages forskellige handlinger for at ændre tilstanden for et skift eller for at forøge eller formindske det pengebeløb, der i pengeskuffen. I dette afsnit beskrives disse Skift-operationer for Microsoft Dynamics 365 for Retail Modern POS og Cloud POS.

### <a name="open-shift"></a>Åbne skift

POS-enheden kræver, at en bruger har et aktivt åbent skift for at kunne udføre operationer, der resulterer i en økonomisk transaktion, f.eks. et salg, en returnering eller en kundeordre.

Når en bruger logger på POS-enheden, kontrollerer systemet først, om et aktiv skift er tilgængeligt for den pågældende bruger på det aktuelle kasseapparat. Hvis der ikke er noget aktivt skift, kan brugeren åbne et nyt skift, genoptage et eksisterende skift eller logge på i tilstanden "uden pengeskuffe", afhængigt af systemkonfigurationen og brugerens rettigheder.

### <a name="declare-start-amount"></a>Angiv startbeløb

Denne handling er ofte den første handling, der udføres i et skift, der netop er åbnet. Til denne handling angiver brugerne startbeløbet for kontanter i kasseskuffen for skiftet. Denne handling er vigtigt, da beregningen af overskud/underskud, der sker, når et skift lukkes, tager hensyn til startbeløbet.

### <a name="float-entry"></a>Kassebeholdning

*Flydende tilgange* er ikke-salgstransaktioner, der udføres i et aktivt skift for at øge mængden af kontanter i pengeskuffen. Et typisk eksempel på en flydende tilgang er en transaktion, hvor der tilføjes yderligere byttepenge til kasseskuffen, når den er ved at være tom.

### <a name="tender-removal"></a>Fjernelse af betalingsmiddel

*Fjernelse af betalingsmidler* er ikke-salgstransaktioner, der udføres i et aktivt skift for at reducere mængden af kontanter i pengeskuffen. Denne handling bruges oftest sammen med en handling med flydende tilgang på et andet skift. Hvis kasseapparat 1 f.eks. mangler byttepenge, så fortager brugeren på kasseapparat 2 en fjernelse af betalingsmiddel for at reducere beløbet i vedkommendes pengeskuffe. Brugeren på kasseapparatet 1 foretager derefter en flydende tilgang for at øge beløbet i vedkommendes pengeskuffe.

### <a name="suspend-shift"></a>Afbryd skifte

Brugere kan afbryde deres aktive skift for at frigøre det aktuelle kasseapparat til en anden bruger, eller for at flytte deres skift til et andet kasseapparat (i dette tilfælde kaldes skiftet ofte kaldet et skift med "flydende pengeskuffe").

Afbrydelse af et skift forhindrer eventuelle nye transaktioner eller ændringer af skiftet, indtil det genoptages.

### <a name="resume-shift"></a>Genoptag skift

Denne handling giver brugerne mulighed for at genoptage et tidligere afbrudt skift på ethvert kasseapparat, der ikke allerede har et aktivt skift.

### <a name="tender-declaration"></a>Kasseoptælling

Denne handling udføres for at angive det samlede pengebeløb, der i øjeblikket er i pengeskuffen. Brugerne udfører oftest denne handling, før de lukker et skift. Dette angivne beløb sammenlignes med det forventede beløb for skiftet, for at beregne overskuds-/underskudsbeløbet.

### <a name="safe-drop"></a>Deponering til pengeskab

Deponeringer til pengeskab kan udføres når som helst på et aktivt skift. Denne handling fjerner penge fra pengeskuffen, så de kan overføres til en mere sikker placering, f.eks. et pengeskab i baglokalet. Det samlede beløb, der er registreret til deponering i pengeskab, indgår stadig i totalerne for skiftet, men det skal ikke tælles med som en del af kasseoptællingen.

### <a name="bank-drop"></a>Indsættelse i banken

I lighed med deponering til pengeskab udføres indsættelser i banken også på aktive skift. Denne handling fjerner penge fra skiftet for at forberede bankindbetalingen.

### <a name="blind-close-shift"></a>Luk skifte uden kontrol

*Skift lukket uden kontrol* er ikke længere er aktive, men er ikke blevet lukket helt. I modsætning til afbrudte skift kan skift lukket uden kontrol ikke genoptages. Men handlinger som f.eks. angiv startbeløb og kasseoptælling kan udføres på dem senere eller fra et andet kasseapparat.

Skift lukket uden kontrol bruges ofte til at frigøre et kasseapparat til en ny bruger eller et nyt skift, uden at der først skal foretages fuld optælling, afstemning og lukning af skiftet.

### <a name="close-shift"></a>Luk skift

Denne handling beregner totaler for skift, overskuds-/underskudsbeløb og færdiggør derefter et aktivt skift eller et skift lukket uden kontrol. Afhængigt af brugerens rettigheder udskrives der også en Z-rapport for skiftet. Lukkede skift kan ikke genoptages eller ændres.

### <a name="print-x"></a>Udskriv X

Denne handling genererer og udskriver en X-rapport for det aktuelle aktive skift.

### <a name="reprint-z"></a>Udskriv Z igen

Denne handling udskriver den sidste Z-rapport igen, som systemet genererede, da et skift blev lukket.

### <a name="manage-shifts"></a>Administrer skift

Denne handling giver brugerne mulighed for at få vist alle aktive eller afbrudte skift eller skift lukket uden kontrol. Afhængigt af deres rettigheder kan brugerne udføre deres endelige lukningsprocedurer, f.eks. kasseoptælling og lukning af skifthandlinger for skift lukket uden kontrol. Denne handling giver også brugerne mulighed for at få vist og slette ugyldige skift i de sjældne tilfælde, hvor skift er efterladt i fejlbehæftet tilstand efter en omstilling mellem offline- og onlinetilstand. Disse ugyldige skift indeholder ikke nogen økonomiske oplysninger eller transaktionsdata, der skal bruges til afstemning.

## <a name="shift-and-drawer-permissions"></a>Rettigheder til skift og kasseskuffe

De følgende POS-rettigheder påvirker, hvad en bruger kan og ikke kan i forskellige situationer:

- **Tillad lukning uden kontrol**
- **Tillad udskrivning af X-rapport**
- **Tillad udskrivning af Z-rapport**
- **Tillad kasseoptælling**
- **Tillad variabel beskrivelse**
- **Åbn kasseskuffe uden salg**
- **Tillad logon på flere skifter** – Denne rettighed giver brugeren mulighed for at logge på og bruge et skift, som en anden bruger åbnede. Brugere, der ikke har denne rettighed, kan kun logge på og bruge skift, de har åbnet.
- **Tillad administration af delt skift** – Brugere skal have denne rettighed for at åbne eller lukke et delt skift.
- **Tillad brug af delt skift** – Brugere skal have denne rettighed for at kunne logge på og bruge et delt skift.

## <a name="back-office-end-of-day-considerations"></a>Overvejelser i forbindelse med back-office-afslutning af dagen

Den måde, som skift og kasseskuffeafstemning bruges på i POS-enheden, er forskellig fra den måde, som transaktionsdata opsummeres på ved beregningen af opgørelsen. Det er vigtigt, at du forstår denne forskel. Afhængigt af konfigurationen og dine forretningsprocesser, kan skiftdataene i POS-enheden (Z-rapporten) og en beregnet back office-opgørelse give forskellige resultater. Denne forskel betyder ikke nødvendigvis, at enten skiftdataene eller den beregnede opgørelse er forkert, eller at der er problemer med dataene. Det betyder blot, at de angivne parametre muligvis medtager flere eller færre posteringer, eller at posteringerne er blevet summeret på forskellige måder.

Selvom hver detailhandler har forskellige forretningsbehov, anbefales det, at du konfigurerer systemet på følgende måde for at undgå situationer, hvor der forekomme differencer af denne type:

Gå til **Detail \> Kanaler \> Detailbutikker \> Alle detailbutikker \> Opgørelse/ultimo**, og for hver butik skal du angive både feltet **Opgørelsesmetode** og feltet **Lukkemetode** til **Skift**.

Denne opsætning hjælper med til at sikre, at back office-opgørelser medtager de samme posteringer som skift på POS-enehden, og at dataene opsummeres efter dette skift.

Yderligere oplysninger om opgørelse og lukkemetoder finder du i [Gemme konfigurationer for detailopgørelser](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).
