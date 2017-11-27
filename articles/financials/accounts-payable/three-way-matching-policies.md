---
title: Trevejs-sammenholdelsespolitikker
description: "Dette emne indeholder eksempler på trevejs-sammenholdelse."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: da3099a07e3084bf49d03e0f4d421aebe9b39940
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="three-way-matching-policies"></a>Trevejs-sammenholdelsespolitikker

[!include[banner](../includes/banner.md)]


Dette emne indeholder eksempler på trevejs-sammenholdelse.

<a name="example-three-way-matching-for-items"></a>Eksempel: trevejs-sammenholdelsespolitik
-------------------------------------

**Oversigt:** Ken er controller i virksomhedens hovedkvarter i en juridisk enhed med navnet Fabrikam. Mads beslutter, at alle kreditorfakturaer, der er baseret på indkøbsordrer, skal sammenholdes med indkøbsordrelinjer (tovejs-sammenholdelse). For køb af varer, der skal bruges som anlægsaktiver, skal fakturaer sammenholdes med både indkøbsordrelinjer og produktkvitteringslinjerne (trevejs-sammenholdelse).

Fabrikam arbejder med flere juridiske enheder og medarbejdere i alle dele af verden. Efterhånden som omfanget af posteringerne øges, er der også stigende uoverensstemmelser mellem kvitteringer og fakturaer. Dette resulterer i aktiver, der afskrives. Fakturaer fra kreditorer betales, men processen omfatter ikke identificering af uoverensstemmelser, når der modtages færre varer, end der blev bestilt, eller når varer ikke modtages overhovedet. Udgifter øges også, fordi medarbejdere stadig skal bruge værktøjer og andre materialer til at udføre deres job. Mads ønsker at sikre, at leverandører leverer de produkter, der er bestilt, og at varerne modtages af Fabrikam-medarbejdere. Derfor kræver Mads tovejs- og trevejs-sammenholdelse for alle juridiske enheder i organisationen. Fakturasammenholdelse er med til at sikre, at problemer med varer, der er forsvundet, eller som ikke er modtaget, kan spores og løses. 

Fakturasammenholdelsespolitikkerne i dette eksempel kan hjælpe personer i følgende roller med at opfylde disse mål:

-   Mads er controller for Fabrikam-virksomheden. Han kan hjælpe personerne i organisationen med at identificere og løse problemer med bestilling, modtagelse og betaling for varer (varer og tjenesteydelser) fra kreditorer.
-   Karina og Pernille er regnskabschefer i kreditorafdelingen for Fabrikams division i USA. De kan gennemføre virksomhedspolitikker og sørge for, at fakturaer først betales, når fakturaerne er sammenholdt med indkøbsordren og modtagelsen af varer og tjenesteydelser, hvor det er relevant.
-   Thomas er produktionschef for Fabrikams division i USA. Han og andre produktionsmedarbejdere kan sørge for, at varer modtages, som de blev bestilt hos leverandører, og behandles, så medarbejderne har det, de skal bruge for at kunne udføre deres job.

### <a name="prerequisites"></a>Forudsætninger

-   Ken angiver sammenholdelsespolitikken på niveauet for den juridiske enhed til Trevejs-sammenholdelse.
-   Ken angiver til/fra for automatisk opdatering på overskriftens sammenholdelsesstatus i den juridiske enhed til Ja.
-   Ken angiver feltet Afstem pristotaler for den juridiske enhed til procent og angiver 15 % som toleranceprocenten.
-   Ken angiver sammenholdelsespolitikken på vareniveauet for vare 1500 – CNC Milicron-maskine til Trevejs-sammenholdelse. Denne vare er en anlægsvare, der bruges til fremstilling hos Fabrikam. Fakturaer for denne vare sammenholdes med indkøbsordrelinjer for priser og med produktkvitteringer for antal.
-   Thomas angiver en rekvisition for fem CNC Milicron-maskiner. Anja, en købsordreassistent hos Fabrikam, udsteder en indkøbsordre til en juridisk enhed, der hedder Contoso, om levering af varerne.

    | Varenummer                 | Antal | Enhedspris | Nettobeløb | Gebyrkode        | Gebyrværdi |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – CNC Milicron-maskine | 5        | 8.000,00   | 40.000,00  | Forsendelse og ekspedition | 3.000,00      |

-   Adam, en debitorassistent hos Contoso, gennemgår leverancer for ugen. Adam vælger forsendelsesposteringer for at fakturere Fabrikam for leveringen af CNC Milicron-maskiner. Adam inkluderer et gebyr for forsendelse og ekspedition. Fabrikam overvejer, om afgiften skal være en del af aktivets kostpris.

### <a name="scenario"></a>Situation

1.  Claus, en arbejder i modtagelsesafdelingen hos Fabrikam, modtager det samlede antal maskiner, der leveres fra Contoso. Han angiver antallet 5 ved modtagelse af produkterne. Da indkøbsordren er blevet fuldt modtaget, ændres status for indkøbsordren til Modtaget.
2.  Pernille, kreditorkoordinator hos Fabrikam, indtaster og kontrollerer den faktura, der er sendt af Contoso. Hun kontrollerer følgende oplysninger:
    -   For varer, der kræver trevejs-sammenholdelse, svarer antallet på fakturalinjen til det antal, der blev modtaget. Det modtagne antal angives på den produktkvittering, der sammenholdes med fakturaen.
    -   For varer, der kræver tovejs- eller trevejs-sammenholdelse, er priserne på fakturalinjen inden for de tolerancer, der er defineret i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Dette omfatter følgende typer prissammenholdelse:
        -   Sammenholdelse af nettoenhedspriser – Nettoenhedsprisen på fakturalinjen svarer til nettoenhedsprisen på indkøbsordrelinjen, dvs. den er inden for den tilladte toleranceprocent. I dette eksempel er tolerancen for nettoenhedsprisen +8 %.
        -   Sammenholdelse af pristotaler – Nettobeløbet på fakturalinjen svarer til nettobeløbet på indkøbsordrelinjen, dvs. den er inden for tilladt toleranceprocent, beløb eller tilladt procent og beløb. I dette eksempel er tolerancen for sammenholdelse af pristotaler +15 %.

Papirfakturaen fra Contoso indeholder følgende oplysninger.

| Vare                        | Antal | Enhedspris | Nettobeløb |
|-----------------------------|----------|------------|------------|
| 1500 – CNC Milicron-maskine | 5        | 8.100,00   | 40.500,00  |
| Forsendelse og håndtering       |          |            | 4.000,00   |
| Skat                         |          |            | 0,00       |
| Samlet                       |          |            | 44.500,00  |

Fakturalinjen indeholder følgende oplysninger i Finance and Operations.

| varenummer                 | Antal | Enhedspris | Linjenettobeløb | Sammenholdelsespolitik    | Antal afstemte produktkvitteringer | Prisafstemning | Pristotalafstemning |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – CNC Milicron-maskine | 5        | 8.100,00   | 40.500,00       | Trevejs-sammenholdelse | Bestået                         | Bestået      | Bestået            |

Da denne linje opfylder kravene under processen til fakturasammenholdelse, kan fakturaen bogføres.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a>Eksempel: Trevejssammenholdelse for kombinationer med varer og leverandører
Oversigt: Mads er controller i virksomhedens hovedkvarter i en juridisk enhed med navnet Fabrikam. Mads beslutter, at alle fakturaer, der er baseret på indkøbsordrer, skal sammenholdes med indkøbsordrelinjer (tovejs-sammenholdelse). Gitte er bogholder for Fabrikams division i Malaysia. Hun angiver, at de markerede varer, der er bestilt hos bestemte leverandører i Malaysia, skal sammenholdes med indkøbsordrelinjerne og produktkvitteringslinjerne (trevejs-sammenholdelse). Hun kan også tilsidesætte sammenholdelsespolitikken på et højere sammenholdelsesniveau for bestemte indkøbsordrer. 

Antal og beløb er små, og der har været problemer med levering fra nogle leverandører i Malaysia. Gitte angiver derfor kontrolniveauet for bestemte kombinationer af varer og leverandører fra Malaysia til trevejs-sammenholdelse. 

Fakturasammenholdelsespolitikkerne i dette eksempel kan hjælpe personer i følgende roller med at opfylde disse mål:
-   Mads er controller for Fabrikam-virksomheden. Han kan hjælpe personerne i organisationen med at identificere og løse problemer med bestilling, modtagelse og betaling for varer (varer og tjenesteydelser) fra kreditorer.
-   Gitte er bogholder for Fabrikams division i Malaysia. Hun kan gennemføre virksomhedspolitikker og sørge for, at fakturaer først betales, når de er sammenholdt med indkøbsordrelinjer og produktkvitteringer for modtagelse af varer og tjenesteydelser. Hun kan også øge kontrolniveauet til trevejs-sammenholdelse for bestemte varer for at styre de driftsmæssige omkostninger.

### <a name="prerequisites"></a>Forudsætninger

-   Ken angiver sammenholdelsespolitikken på niveauet for den juridiske enhed til Tovejs-sammenholdelse.
-   Ken angiver feltet Afstem pristotaler for den juridiske enhed til procent og angiver 10 % som toleranceprocenten.
-   Mads angiver tolerancen for enhedspriser for alle varer til 2 %.
-   Cassie angiver sammenholdelsespolitikken for kombinationen af varer og kreditor for varen PH2500 – Computer og kreditor Contoso til Trevejs-sammenholdelse.
-   Anja, en indkøbsordreassistent i Fabrikams division i Malaysia, udsteder indkøbsordrer til Contoso om at levere tre varer, som vist i følgende tabel. Når hun opretter indkøbsordren, tilsidesætter hun sammenholdelsespolitikken for den trådløse mus, så den er angives til trevejs-sammenholdelse i stedet for tovejs-sammenholdelse.

    | Varenummer           | Antal | Enhedspris | Nettobeløb | Sammenholdelsespolitik (standardpost) | Sammenholdelsespolitik (på indkøbsordrelinjen) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – Computer     | 2        | 2.500,00   | 5.000,00   | Trevejs-sammenholdelse              | Trevejs-sammenholdelse                           |
    | MM01 – Trådløs mus | 2        | 40,00      | 80,00      | Tovejs-sammenholdelse                | Trevejs-sammenholdelse                           |
    | USB-drev             | 200      | 10,00      | 2.000,00   | Tovejs-sammenholdelse                | Tovejs-sammenholdelse                             |

### <a name="scenario"></a>Scenarie

1.  Varerne ankommer. Claus, en arbejder i modtagelsesafdelingen i Fabrikams division i Malaysia, afbrydes og bogfører ikke produktkvitteringen med det samme.
2.  Pernille, kreditorkoordinator hos Fabrikam, indtaster og kontrollerer den faktura, der er sendt af Contoso. Hun kontrollerer følgende oplysninger:
    -   For varer, der kræver trevejs-sammenholdelse, svarer antallet på fakturalinjen til det antal, der blev modtaget. Det modtagne antal angives på den produktkvittering, der sammenholdes med fakturaen.
    -   For varer, der kræver tovejs- eller trevejs-sammenholdelse, er priserne på fakturalinjen inden for de tolerancer, der er defineret i Finance and Operations. Dette omfatter følgende typer prissammenholdelse:
        -   Sammenholdelse af nettoenhedspriser – Nettoenhedsprisen på fakturalinjen svarer til nettoenhedsprisen på indkøbsordrelinjen, dvs. den er inden for den tilladte toleranceprocent. I dette eksempel er tolerancen for nettoenhedsprisen +2 %.
        -   Sammenholdelse af pristotaler – Nettobeløbet på fakturalinjen svarer til nettobeløbet på indkøbsordrelinjen, dvs. den er inden for tilladt toleranceprocent, beløb eller tilladt procent og beløb. I dette eksempel er tolerancen for sammenholdelse af pristotaler +10 %.

Papirfakturaen fra Contoso indeholder følgende oplysninger.

| Vare                  | Antal | Enhedspris | Nettobeløb |
|-----------------------|----------|------------|------------|
| PH2500 – Computer     | 2        | 2.500,00   | 5.000,00   |
| MM01 – Trådløs mus | 2        | 41,00      | 82,00      |
| USB-drev             | 200      | 10,05      | 2.010,00   |
| Faktura i alt         |          |            | 7.092,00   |

Fakturalinjen indeholder følgende oplysninger i Finance and Operations.

| varenummer           | Antal | Enhedspris | Linjenettobeløb | Sammenholdelsespolitik    | Antal afstemte produktkvitteringer | Prisafstemning | Pristotalafstemning |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – Computer     | 2        | 2.500,00   | 5.000,00        | Trevejs-sammenholdelse | Mislykkedes                         | Bestået      | Bestået            |
| MM01 – Trådløs mus | 2        | 41,00      | 82,00           | Trevejs-sammenholdelse | Mislykkedes                         | Mislykkedes      | Bestået            |
| USB-drev             | 200      | 10,05      | 2010,00         | Tovejs-sammenholdelse   |                                | Bestået      | Bestået            |

Bemærk følgende varer:
-   For PH2500 – Computerlinje indeholder kolonnen Antal afstemte produktkvitteringer et advarselsikon, fordi fakturalinjen ikke er sammenholdt med en produktkvittering.
-   For MM01 – Trådløs mus-linje indeholder kolonnen Antal afstemte produktkvitteringer et advarselsikon, fordi fakturalinjen ikke er sammenholdt med en produktkvittering. Kolonnen Sammenhold enhedspriser indeholder et advarselsikon, fordi tolerancen for nettoenhedspriser på 2 % er overskredet.
-   For linjen USB-drev er kolonnen Antal afstemte produktkvitteringer tom, fordi tovejs-sammenholdelse ikke stemmer overens med antal på fakturalinje og produktkvitteringslinjer.

Hvis godkendelse er påkrævet for fakturaer, der skal bogføres med uoverensstemmelser efter en fakturasammenholdelse, skal til/fra-feltet Godkend bogføring med matchningafvigelse på siden Detaljer om fakturasammenholdelse markeres, før fakturaen kan bogføres med fejl ved sammenholdelse af pris og fejl ved sammenholdelse af antal. Hvis godkendelse ikke er nødvendig, kan behandling af fakturaen fortsætte, hvis der ikke er andre bogføringsfejl.


Du kan finde flere oplysninger under [Fakturasammenholdelse for Kreditor](accounts-payable-invoice-matching.md).




