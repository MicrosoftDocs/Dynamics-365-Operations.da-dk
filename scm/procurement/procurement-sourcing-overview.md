---
title: "Oversigt over indkøb og forsyning"
description: "Denne artikel indeholder en oversigt over den funktionalitet, der er tilgængelig i modulet Indkøb og forsyning."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3669de6314e65c78ce5d401dae2e7481ec38b68
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="procurement-and-sourcing-overview"></a>Oversigt over indkøb og forsyning

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en oversigt over den funktionalitet, der er tilgængelig i modulet Indkøb og forsyning.

Indkøb og forsyning dækker alle trin fra at identificere behov for produkter og tjenester gennem indkøb af produktet, kvittering, fakturering og behandling af betalinger med kreditorer. Indkøbsprocesser kan konfigureres mod specifikke forretningsmæssige behov ved at definere indkøbspolitikker og arbejdsgange.

## <a name="identifying-a-need-for-product-and-services"></a>Identificere behov for produkter og tjenester
Behovet for produkter eller tjenesteydelser kan opstå ud fra *rekvisitioner*, for eksempel, når en medarbejder rekvirerer et produkt. *Produktkataloger * kan være sat op til at vejlede i valget af tilgængelige produkter, der kan vælges mellem, eller anmodninger kan foretages for produkter, der ikke er endnu gjort tilgængelige i et katalog, så indkøbsafdelingen får mulighed for at overveje, hvordan produktet kan leveres.  

*Forbrugsgrænser* kan bruges til at begrænse rekvisitionsforbruget, og *indkøbsarbejdsgangen* tilføjer mulighed for at kræve godkendelse, før bestilling sker. Det er også muligt at angive fordeling af budgetmidler, hvis det er nødvendigt.  
  
Indkøbsafdelingen identificerer leverandører til påkrævede produkter og tjenester, og dette kan omfatte, at der sendes en *tilbudsanmodning* til flere potentielle leverandører. Det er muligt at dele specifikationerne for det produkt, der anmodes om, og potentielle leverandører kan se disse for at finde ud af, om de kan levere et produkt, der overholder dem. Kreditorer returnerer deres bud, som derefter gennemgås af indkøbsafdelingen, før de vælger den leverandør, de vil købe fra.  

Indkøbsordrer omfatter en mulighed for at sende en *indkøbsforespørgsel* til leverandøren som et alternativ til en mere omfattende tilbudsanmodningsproces. Indkøbsforespørgslen kan bruges til at oprette betingelser som f.eks. priser, rabatter og leveringsdato for ordren. Hvis kreditorer er konfigureret til at bruge **Kreditor**-portalen, deaktiveres funktion til indkøbsforespørgsel. I stedet deles ordren på **kreditorportalenleverandør**, og når der er sendt en *bekræftelsesanmodning*, kan kreditoren sende ordren direkte.  

*Kreditorkataloger* kan bruges til at indsamle oplysninger om det produktudvalg, som kreditorerne kan levere. Kreditorer kan udgive deres eget katalog, så det er nemmere at holde kataloget opdateret. Det er muligt at vedhæfte en *godkendt kreditorliste* til et produkt, og dette kan være en hjælp under valg af kreditorer, når der åbnes nye indkøbsordrer, og forhindre brug af utilsigtede kreditorer.

## <a name="procurement"></a>Indkøb
*Indkøbsordrer* kan oprettes på en række forskellige måder, herunder:

-   Som et resultat af varedisponering, som har identificeret et behov, der kræver et køb. Denne proces opretter indkøbsordreforslag, og når de er frigivet, oprettes indkøbsordrer.
-   Via behandlingen af indkøbsrekvisitioner, der resulterer i indkøb.
-   Via behandling af købsaftaler, hvor indkøbsordrer oprettes som frigivne ordrer fra aftalerne. Dette bruges normalt, når købsaftaler bruges til at repræsentere rammeordrer.
-   Manuelt, når den indkøbsordre, der er oprettet, ikke er baseret på et andet dokument.

Indkøbsordrer, der er konfigureret med *købsgodkendelsesarbejdsgange*, kræver godkendelse, før de registreres som godkendt, og dette er påkrævet, før ordren kan behandles yderligere.  

Købsordrer *bekræftes* for at angive, at der er oprettet en aftale med kreditoren. Indkøbsordren kommer derefter gradvist gennem forskellige statusser, indtil den til sidst bliver faktureret eller annulleret.  

Når du opretter en indkøbsordre, udfyldes mange af felterne på forhånd med værdier, der kommer fra de oplysninger, der er gemt om kreditoren på siden **Kreditorer**. Det betyder, at der er et begrænset antal felter, du skal udfylde på indkøbsordren, selvom du kan vælge at tilsidesætte standardværdierne.

### <a name="prices-and-discounts"></a>Priser og rabatter

Priser og rabatter Indeholder oplysninger om priser, rabatter og rabatbetingelser, der tilbydes. Priser og rabatter kan repræsenteres som *samhandels**aftaler*. Samhandelsaftaler repræsenterer kreditorprislister med priser eller rabatter og har et bestemt sæt datoer, hvor aftalen er gyldig. Priser og rabatter kan forhandles og repræsenteres via *indkøbsaftaler *med betingelser som f.eks. forpligtelser til at købe visse enheder eller for et vist pengebeløb som en forudsætning for de aftalte vilkår. *Rabataftaler* kan indgås med kreditorer, hvor indkøb af bestemte produkter eller grupper af produkter kan udløse en rabat fra kreditoren afhængigt af indkøbsbeløbet eller -mængden.

### <a name="delivery-options"></a>Indstillinger for levering

Der er forskellige muligheder for den leveringsproces, der er knyttet til en indkøbsordre. Bestilte produkter kan opdeles i *leveringsplaner*, hvor dele af det bestilte antal kan være planlagt til levering på forskellige datoer. Levering kan også omfatte *direkte levering*, der initieres fra en salgsordre, som automatiserer oprettelsen af følgesedlen for salgsordren, på samme tid som produktkvitteringen registreres på indkøbsordren. Indkøbsordrer kan også indgå i en *interne ordrekæde*, der også kaldes interne indkøbsordrer, hvor produkter bestilles fra en tilsvarende intern salgsordre. I denne situation er visse trin automatiseret på tværs af de to relaterede interne ordrer.

### <a name="supplementary-items"></a>Supplerende varer

Produkter, kan konfigureres til at omfatte *supplerende varer*. Dette er at foreslå produkter, der er relateret til det produkt, der er ved at blive bestilt. Yderligere produkter kan blive påkrævet eller være valgfrie. I nogle tilfælde kan supplerende varer tilføjes som gratis produkter, der følger med ved købet af andre produkter.

### <a name="purchase-order-charges"></a>Indkøbsordregebyrer

Gebyrer kan blive tildelt til indkøbsordren. Dette kan ske automatisk via konfiguration af automatiske gebyrer eller ved manuelt at tilføje gebyrer. Gebyrer kan tildeles til en ordre på hovedniveau eller på ordrelinjeniveau. Bogføring af gebyrer kan konfigureres på forskellige måder. Du kan for eksempel oprette et gebyr, der bogføres som en omkostning for produktet. Hvis du gør dette, skal gebyrerne tildeles på ordrelinjeniveau, før ordren kan bekræftes. Der er en indstilling, der kan hjælpe med at fordele gebyrer fra ordrehovedet til linjerne.

## <a name="product-receipt-and-invoicing"></a>Modtagelse og fakturering af produkter
Indkøbsordrer, der omfatter fysiske produkter, kræver almindeligvis, at *ankomstsregistrering* skal ske på et lagersted, og herefter registreres en *produktmodtagelse* for ordren. Indkøbsordrer med produkter, der opfylder indkøbsrekvisitioner, kan konfigureres, så den medarbejder, der har anmodet om produkterne, også skal forelægge en *bekræftelse af modtagelse*.  

Nogle indkøbsordrer omfatter produkter, tjenester eller andre ikke-fysiske produkter, hvor modtagelsen på et lager ikke er nødvendig. Produkter kan oprettes som tjenester, eller *indkøbskategorier* kan bruges direkte på indkøbsordren for sådanne ordrer. Med disse ordrer springes bogføring af produktmodtagelsen nogle gange over, og ordren faktureres direkte. Registreringen af produktmodtagelsen kan også udføres på indkøbsordren uden forudgående ankomstsregistrering.  

Modtagelse af produkter kan resultere i automatisk forbrug i forbindelse med et bestemt formål. Dette omfatter stiltiende forbrug med direkte levering, forbrug i forhold til et projekt eller bogføring af produktet som et anlægsaktiv.  

Når *kreditorfakturaer* modtages fra kreditoren, kan de først registreres i *fakturaregistret* uafhængigt af indkøbsordren og senere godkendes som en post mod indkøbsordre. Registrering af kreditorfakturaen med købsordren omfatter afstemning af produktmodtagelsen mod fakturaen.  

*Regnskabsfordelinger* kan være angivet på indkøbsordren for at beskrive, hvordan bogføring skal udføres i Finans, og kan også definere, hvordan fordeling af budgetmidler opnås, når denne er medtaget i konfigurationen.  

Fakturerede indkøbsordrer registrerer passivet på kreditorkontoen i kreditorer, hvorfra *kreditor**betalingen* kan behandles.

## <a name="vendor-performance"></a>Leverandørperformance
Ydeevne og gennemgang af indkøb understøttes via *indkøbs- og kreditorapporter,* som indeholder forbrugsanalyse og analyse af kreditorydeevne.




