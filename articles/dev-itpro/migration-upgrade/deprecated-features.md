---
title: Fjernede eller frarådede funktioner
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet.
author: sericks007
manager: AnnBe
ms.date: 06/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9daba2449b6a20634c13117cedb6b63fcc8ee674
ms.sourcegitcommit: fcae2e7938d7dbd94b76b0948b084d90d5fc919c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/05/2019
ms.locfileid: "1620639"
---
# <a name="removed-or-deprecated-features"></a>Fjernede eller forældede funktioner

[!include [banner](../includes/banner.md)]

I dette emne beskrives funktioner, der er blevet fjernet eller frarådes for Dynamics 365 for Finance and Operations.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Fra og med Dynamics 365 for Finance and Operations-versionen fra juli 2017 med Platform update 8 er installationstyperne angivet for hver fjernet eller forældet funktion. Alle de tidligere versioner, der er nævnt i dette emne, understøtter kun installationer i skyen.

> Du kan finde detaljerede oplysninger om objekter i Finance and Operations i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations.

## <a name="dynamics-365-for-finance-and-operations-1004"></a>Dynamics 365 for Finance and Operations 10.0.4 

### <a name="france-fec-accounting-data-export-in-xml"></a>Frankrig: Eksport af FEC-regnskabsdata i XML-format

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Den **Franske FEC-revisionsfil**, som er erstattet af txt-format, er tilgængelig via **Finans** \> **Periodiske opgaver** \> **Dataeksport**.
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Finans |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet. Måltidsrammen for funktioner, der skal fjernes, er juli 2020. |

=======
## <a name="dynamics-365-for-finance-and-operations-1004-with-platform-update-28"></a>Dynamics 365 for Finance and Operations 10.0.4 med platformsopdatering 28

> [!IMPORTANT]
> Dynamics 365 for Finance and Operations 10.0.4 med platformsopdatering 28 er tilgængelig for brugere i målgruppen som en del af en eksempelversion. Indholdet og funktionaliteten kan blive ændret. Du kan finde flere oplysninger om frigivelser af eksempelversioner her: [Tilgængelighed af tjenesteopdatering](../../fin-and-ops/get-started/public-preview-releases.md).

### <a name="legacy-navigation-bar"></a>Gammel navigationslinje

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Overskriftsjustering med andre Dynamics- og Office-produkter. Yderligere oplysninger finder du i [Opdateret navigationslinje er nu tilpasset overskriften i Office](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/updatednavbar).
| **Erstattet af en anden funktion?**   | I platformsopdatering 24 blev der introduceret en navigationslinje med søgefunktionen. |
| **Produktområder, der er berørt**         | Webklient |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forælder: Fra og med april 2020 er den ældre navigationslinje ikke længere tilgængelig. Indtil dette tidspunkt kan kunder vende tilbage til den ældre navigationslinje via siden **Indstillinger for klientydelse**. |


## <a name="dynamics-365-for-finance-and-operations-1002-with-platform-update-26"></a>Dynamics 365 for Finance and Operations 10.0.2 med platformsopdatering 26

> [!IMPORTANT]
> Dynamics 365 for Finance and Operations 10.0.2 med platformsopdatering 26 er tilgængelig for brugere i målgruppen som en del af en eksempelversion. Indholdet og funktionaliteten kan blive ændret. Du kan finde flere oplysninger om frigivelser af eksempelversioner her: [Tilgængelighed af tjenesteopdatering](../../fin-and-ops/get-started/public-preview-releases.md).

### <a name="legacy-default-action-behavior"></a>Ældre standardhandlingers opførelse

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Den ældre opførelse for standardhandlinger i gitre resulterer i, at en uventet kolonne indeholder linket til standardhandlingen, efter at gitterkolonnerne er blevet omfordelt via tilpasning. Den nye funktion for standardtastaturhandlinger retter op på dette. Du kan finde yderligere oplysninger under [Standardtastaturhandlinger i gitre](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Erstattet af en anden funktion?**   | Indførelsen af en funktion til "standardtastaturhandlinger" blev påbegyndt i platformsopdatering 21. Denne funktion kan aktiveres på siden **Indstillinger for klientydelse**. |
| **Produktområder, der er berørt**         | Gitre i webklienten |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfasning: fra april 2020 vil standardtastaturhandlinger være standardindstillingen, såfremt der ikke forefindes en mekanisme, som kan gå tilbage til den ældre opførelse. |

### <a name="legacy-is-one-of-filtering-experience"></a>Ældre filtreringsoplevelse for "er en af"

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | "Er en af"-filtreringsoplevelsen blev redesignet i platformsopdatering 22, og planen er, at den med tiden skal være den eneste "er en af"-filtreringsoplevelse. |
| **Erstattet af en anden funktion?**   | I platformsopdatering 22 blev en ny og forbedret "er en af"-filtreringsoplevelse tilgængelig på siden **Indstillinger for klientydelse**. Du kan finde yderligere oplysninger under [Den optimerede filtreringsoplevelse "er en af"](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Produktområder, der er berørt**         | Webklient |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfasning: fra april 2020 vil den forbedrede "er en af"-oplevelse være standardopførelsen, såfremt der ikke forefindes en mekanisme, som kan gå tilbage til den ældre opførelse. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Parameter til at aktivere salgsordre for projektkontrakter med flere finansieringskilder
Understøttelse til at oprette projektbaserede salgsordre i de tilfælde, hvor projektkontrakten har flere finansieringskilder, er gjort mulig ved hjælp af indstillingen **Projektstyringsparametre** og **Tillad salgsordre for projekter med flere finansieringskilder**. Dette parameter er ikke aktiveret som standard. 

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Funktionen vil altid være aktiveret, når parametret fjernes. |
| **Erstattet af en anden funktion?**   | Nr. Funktionen til at understøtte projektbaserede salgsordre med flere finansieringskilder vil altid være aktiveret.   |
| **Produktområder, der er berørt**         |Parametret **Tillad salgsordre for projekter med flere finansieringskilder** bliver fjernet. Følgende metoder modificeres, når parametret er blevet fjernet: **ctrlSalesOrderTable**-metoden i **ProjStatusType**-klassen, **valideringsmetoden** for feltet **ProjId** og **kør**-metoden i formularen **SalescreateOrder**. Følgende metoder udfases, når parametret er blevet fjernet: **IsSalesOrderAllowedForMultipleFundingSources** i tabelfilen **ProjTable**, metoden **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** i tabelfilen **ProjTable**, datafeltet **AllowSalesOrdersForMultipleFundingSources** i formularen **ProjParameters** og filerne **ProjParameterEntity** samt den private metode **IsAssociatedToMultipleFundingSourcesContract** i tabelfilen **ProjTable**. |
| **Installationsindstilling**              | Alt  |
| **Status**                         | Udfasningen er planlagt til at finde sted sammen med frigivelsesbølgen i april 2020. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Ældre arbejdsgangsrapporter til sporing og forekomstens status

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ældre arbejdsgangsrapporter til sporing og forekomstens status udfases, da der ikke længere henvises hertil i navigationen. Navnene på rapporterne er WorkflowWorkflowInstanceByStatusReport og WorkflowWorkflowTrackingReport. |
| **Erstattet af en anden funktion?**   | Formularen for arbejdsgangshistorikken kan anvendes i stedet for. |
| **Produktområder, der er berørt**         | Webklient |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfasning: den fastsatte tidsramme for funktioner, der skal fjernes, er april 2020. |

## <a name="dynamics-365-for-finance-and-operations-1001-with-platform-update-25"></a>Dynamics 365 for Finance and Operations 10.0.1 med Platform update 25

> [!IMPORTANT]
> Dynamics 365 for Finance and Operations 10.0.1 med platformsopdatering 25 er tilgængelig for brugere, der er en del af målgruppen for en eksempelversion. Indholdet og funktionaliteten kan blive ændret. Du kan finde flere oplysninger om frigivelser af eksempelversioner her: [Tilgængelighed af tjenesteopdatering](../../fin-and-ops/get-started/public-preview-releases.md).

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Forældede API'er og ændringer, der potentielt kan give beskadigelser


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Afledning af interne klasser er udfaset

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Før platformsopdatering 25 var det muligt at oprette en klasse eller en tabel, som stammer fra en intern klasse/tabel, der er defineret i en anden pakke/modul. Dette er ikke en sikker kodepraksis. Fra og med platformsopdateringen 25 viser kompileren en advarsel. |
| **Erstattet af en anden funktion?**   | Advarslen fra kompileren erstattes af en fejlmeddelelse i platformsopdatering 26. Denne ændring er bagudkompatibel på kørselstidspunktet, hvilket betyder, at platformsopdatering 25 eller nyere kan installeres i et sandkasse- eller produktionsmiljø, uden at den brugerdefineret kode skal ændres. Denne ændring påvirker kun udviklings- og kompileringstiden.|
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfasning: advarslen ændres til en kompileringsfejl i platformsopdatering 26. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Tilsidesættelse af interne metoder udfases

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Forud for platformsopdatering 25 var det muligt at tilsidesætte en intern metode i en afledt klasse, som er defineret i en anden pakke/modul. Dette er ikke en sikker kodepraksis. Fra og med platformsopdateringen 25 viser kompileren en advarsel. |
| **Erstattet af en anden funktion?**   | Denne advarsel erstattes af en kompileringsfejl i platformsopdatering 26. Denne ændring er bagudkompatibel på kørselstidspunktet, hvilket betyder, at platformsopdatering 25 eller nyere kan installeres i et sandkasse- eller produktionsmiljø, uden at den brugerdefineret kode skal ændres. Denne ændring påvirker kun udviklings- og kompileringstiden. |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfasning: advarslen ændres til en kompileringsfejl i platformsopdatering 26. |


## <a name="dynamics-365-for-finance-and-operations-813-with-platform-update-23"></a>Dynamics 365 for Finance and Operations 8.1.3 med Platform update 23

### <a name="sql-server-reporting-services-reportviewer-control"></a>Kontrolelement til visning af rapporter i SQL Server Reporting Services
Kunderne kan anvende **Eksport**-handlingen, som er tilgængelig via det integrerede kontrolelement til visning af rapporter i SQL Server Reporting Services (SSRS), til at downloade dokumenter, der oprettes i Finance and Operations-programmer. Med denne HTML-baserede præsentation af rapporten får brugerne vist et ikke-sideinddelt eksempel på dokumentet.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | HTML-baserede eksempler er ikke-sideinddelte og gengiver derfor **ikke** de fysiske dokumenter, der i sidste ende produceres af Finance and Operations, nøjagtigt. Ved at integrere PDF som standardformatet til forretningsdokumenter fuldt ud vil brugerne kunne drage fordel af en moderne visningsoplevelse med forbedret ydeevne, når de udarbejder programrapporter. |
| **Erstattet af en anden funktion?**   | Fremadrettet bliver PDF-dokumenter standardformatet for rapporter, der gengives af Finance and Operations.   |
| **Produktområder, der er berørt**         | Denne ændring påvirker **ikke** kundescenarier, hvor rapporter distribueres elektronisk eller sendes direkte til printere.    |
| **Installationsindstilling**              | Alt  |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. Funktionen til automatisk forhåndsvisning af programrapporter ved hjælp af en integreret PDF-viewer er planlagt som en del af platformsopdateringen i maj 2019. |

### <a name="client-kpi-controls"></a>Klient-KPI-kontrolelementer
Integrerede nøgletal (KPI'er) kan modelleres i Visual Studio af en udvikler og yderligere tilpasses af slutbrugeren.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | De indbyggede klientkontrolelementer, der bruges til at definere KPI'er, har lav kundeinddragelse og kræver, at en udvikler kan tilføje sporbare målepunkter. |
| **Erstattet af en anden funktion?**   | PowerBI.com-tjenesten leverer førsteklasses værktøjer til at definere og administrere KPI'er, der er baseret på data fra eksterne kilder.  Vi planlægger i en kommende version at gøre det muligt for dig at integrere løsninger, som PowerBI.com er vært for, i programmets arbejdsområder.   |
| **Produktområder, der er berørt**         | Denne opdatering forhindrer, at udviklere kan introducere nye KPI-kontrolelementer i Visual Studio-designeren.    |
| **Installationsindstilling**              | Alt  |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Forældede API'er og ændringer, der kan give fremtidige beskadigelser

#### <a name="field-groups-containing-invalid-field-references"></a>Feltgrupper, der indeholder ugyldige feltreferencer

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Det er muligt for definitioner af tabelmetadata at have feltgrupper, der indeholder ugyldige referencer. Dette problem kategoriseres i øjeblikket som en *kompileradvarsel* i stedet for en *fejl*, hvilket betyder, at oprettelsen af den installerbare pakke og installationen kan fortsætte, uden at problemet rettes. Hvis pakken installeres, kan det medføre kørselsfejl i Økonomirapportering og SQL Server Reporting Services (SSRS). Sådan løser du problemet:<br><br>1. Fjern den ugyldige feltreference fra definitionen af tabelfeltgruppen.<br><br>2. Kompiler igen.<br><br>3. Kontroller, at eventuelle advarsler eller fejl er rettet. |
| **Erstattet af en anden funktion?**   | Denne advarsel erstattes af en kompileringsfejlmeddelelse fremover.  |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer. |
| **Installationsindstilling**              | Alle. |
| **Status**                         | Udfasning: advarslen vil fremadrettet være en fejlmeddelelse om kompileringstid. Vi satser i øjeblikket på Platform update 30. |

#### <a name="complete-list"></a>Komplet liste
For at få adgang til den komplette liste over API'er, der udfases, skal du se [Udfasning af metoder og metadataelementer](deprecation-deletion-apis.md).

## <a name="dynamics-365-for-finance-and-operations-81-with-platform-update-20"></a>Dynamics 365 for Finance and Operations 8.1 med Platform update 20

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Regler for batchoverførsel for kontoposter for reskontrokladde
Synkron overførselstilstand frarådes i finansparametrene.  Denne tilstand erstattes af asynkron og planlagt batch, der allerede findes som indstillinger for overførsel. Du kan finde flere oplysninger i bloggen [Finansparametre – Batchoverførselsregler](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Vi fjerner indstillingen for synkron på grund af indflydelse på ydeevnen i systemet. |
| **Erstattet af en anden funktion?**   | Asynkron og planlagt batch er indstillinger, der skal bruges i stedet for synkron.   |
| **Produktområder, der er berørt**         | Finans, kreditor, debitor, indkøb, udgift    |
| **Installationsindstilling**              | Alt  |
| **Status**                         | Forældet: Måltidsrammen for funktioner, der skal fjernes, er version 10.0.|

### <a name="electronic-reporting-for-russia"></a>Elektronisk rapportering for Rusland
Funktion til at konfigurere filformaterne .txt- og .xml for erklæringer. 

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet med elektronisk rapportering. |
| **Erstattet af en anden funktion?**   | Ja. |
| **Produktområder, der er berørt**         | Finans |
| **Installationsindstilling**              | Alt |
| **Status**                         | Fjernes fra og med Dynamics 365 for Finance and Operations 8.1 med Platform update 20. |

### <a name="financial-reports-generator-for-russia"></a>Generator til økonomiske rapporter for Rusland
Et værktøj til at konfigurere indsamling af data til regnskabs- og momsrapporter og eksportere data til XLS- og DOC-rapportskabeloner. Funktionelle dele: eksportere data til XLS- og DOC-rapportskabeloner, forespørgsler, faste forudsætninger fjernes. 

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Fjernede dele erstattes med elektronisk indberetning. |
| **Erstattet af en anden funktion?**   | Ja. Økonomirapporters brugergrænseflade for opsætning skal bruges til at opstille dataindsamlingsregler efter GL-konti eller momsregistre. Eksportere data til forskellige filtyper, faste forudsætninger og regler for forespørgselslignende indsamling bør være konfigureret i elektronisk rapportering. |
| **Produktområder, der er berørt**         | Finans. |
| **Installationsindstilling**              | Alt |
| **Status**                         | Fjernes fra og med Dynamics 365 for Finance and Operations 8.1 med Platform update 20. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Integration med eksterne udbydere for at sende elektronisk rapportering via kommunikationskanaler for Rusland
Funktion til eksport af genererede elektroniske filer med erklæringer til mappe for at sende dem til officielle udbydere af elektronisk rapportering samt tilbageimport af tilstand.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af elektroniske meddelelser, der kan konfigureres. |
| **Erstattet af en anden funktion?**   | Ja.  |
| **Produktområder, der er berørt**         | Finans, moms |
| **Installationsindstilling**              | Alt |
| **Status**                         | Fjernes fra og med Dynamics 365 for Finance and Operations 8.1 med Platform update 20. |


### <a name="profit-tax-register-wizard"></a>Guiden Registre over skat af overskud
Funktion til oprettelse af skabeloner for nye registre over skat af overskud. Denne funktion opretter X ++-objekter for nye registre, der derefter oprettes som skabeloner med den relevante beregningslogik tilføjet.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Funktionen er ikke kompatibel med Dynamics 365 for Finance and Operations-udvidelsesmodellen. |
| **Erstattet af en anden funktion?**   | Nr. |
| **Produktområder, der er berørt**         | Moms |
| **Installationsindstilling**              | Alt |
| **Status**                         | Fjernes fra og med Dynamics 365 for Finance and Operations 8.1 med Platform update 20. |


## <a name="dynamics-365-for-finance-and-operations-80-with-platform-update-15"></a>Dynamics 365 for Finance and Operations 8.0 med Platform update 15
Funktioner, der ikke er blevet fjernet eller forældet i denne version. Platform update 15 er kumulativ og indeholder nye eller ændrede funktioner fra Platform update 13, Platform update 14 og Platform update 15.

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 med Platform update 12

### <a name="personalized-product-recommendations"></a>Tilpassede produktanbefalinger 
Fra og med den 15. februar 2018 vil detailhandlere ikke længere kunne vise personlige produktanbefalinger på en POS-enhed. Du kan finde flere oplysninger under [Tilpassede produktanbefalinger](../../retail/personalized-product-recommendations.md).  

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Vi vil fjerne den aktuelle version af produktanbefalingstjenesten, fordi vi ændrer denne funktion og giver den en bedre algoritme og nyere detailrelaterede funktioner.  |
| **Erstattet af en anden funktion?**   | Nej Efter foråret 2018 er det dog planen at genintroducere denne funktion for at anvende en ny anbefalingstjeneste.   |
| **Produktområder, der er berørt**         | Tilpassede produktanbefalinger i POS.                                                    |
| **Installationsindstilling**              | Alt                                                                                      |
| **Status**                         |Fjernet fra og med den 15. februar 2018. Dette påvirker kunder, der kører Dynamics 365 for Operations 1611 og nyere.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Udvidelser af listen over elektroniske rapporteringsfunktioner (ER)
Muligheden for at introducere brugerdefinerede funktioner, der skal bruges i ER-udtryksgeneratoren (yderligere oplysninger finder du i [Udvide listen over elektroniske rapporteringsfunktioner](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)), understøttes ikke længere. På grund af ændringer af ER-API'er er API'en til kald af indbyggede funktioner fra ER-udtryksgeneratoren blevet intern og kan ikke længere udvides.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Kodeplomberingsinitiativ  |
| **Erstattet af en anden funktion?**   | Ingen. Hver gang der kræves en ny indbygget funktion, skal en ny anmodning om forlængelse adresseres til ER-strukturteamet.<br><br>Som en midlertidig løsning, mens den anmodede funktion er under udvikling af ER-teamet, kan den logik, der kræves, programmeres som en metode til en brugerdefineret programklasse. Denne metode kan benyttes i ER-udtrykket som en egenskab for den tilføjede ER-datakilde til den **Program\klasse**-type, der refererer til den pågældende brugerdefinerede programklasse.  |
| **Produktområder, der er berørt**         | Elektronisk rapporteringsstruktur                                                      |
| **Installationsindstilling**              | Alt                                                                                      |
| **Status**                         | Fjernes fra og med Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Rapporterne Lager pr. varegruppe og Lager aldersfordelt pr. lagerdimension

Disse to rapporter understøttes ikke længere i Finance and Operations. I stedet kan rapporten **Aldersfordelt lager** bruges til at forbedre brugeroplevelsen.

|   |  |
|--------------|-----------------------|
| **Årsagen til fjernelsen**       | Identiske funktioner  |
| **Erstattet af en anden funktion?** | Ja. De to rapporter er blevet erstattet af rapporten **Aldersfordelt lager**.     |
| **Produktområder, der er berørt**       | Lagerstyring, omkostningsstyring        |
| **Installationsindstilling**        | Alt|
| **Status**                       | Forældet: Menupunkterne for de to rapporter er blevet fjernet i version 7.3. Koden for rapporterne forbliver dog i produktet. Planen er at fjerne koden i en senere version. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Power BI-indholdspakker, der er tilgængelige på AppSource
Indholdspakkerne **Omkostningsstyring**, **Økonomisk performance** og **Retail Channel Performance**, der er tilgængelige på webstedet [Microsoft AppSource](https://appsource.microsoft.com), frarådes som følge af produktopdateringer i Microsoft Power BI. Systemadministrationsformularer, som bruges til at installere disse indholdspakker på PowerBI.com, er også forældede i Finance and Operations.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Produktopdateringer i Microsoft Power BI. |
| **Erstattet af en anden funktion?**   | Indholdspakkerne **Omkostningsstyring**, **Økonomisk performance** og **Retail Channel Performance**, der er tilgængelige på webstedet [AppSource](https://appsource.microsoft.com), bliver erstattet af analyseprogrammer, som giver mulighed for integration af løsninger på databaseniveau. Du kan finde flere oplysninger om analyseprogrammer i [Integreret Power BI i arbejdsområder](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Produktområder, der er berørt**         | Omkostningsstyring, Finans og Detail                                                                                               |
| **Installationsindstilling**              | Kun skyen (Integration med PowerBI.com understøttes ikke i lokale installationer).                                                                                                            |
| **Status**                         | Forældet: Måltidsrammen for fjernelse af funktioner er 2. kvartal 2018.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standardbrugergrænseflade i arbejdsområdet til datastyring

Standardbrugergrænsefladen i Datastyring er den gamle brugergrænseflade, som er den standardbrugergrænseflade, der vises for brugerne, når de besøger arbejdsområdet til datastyring.

|   |  |
|------------------|-------------------------|
| **Årsagen til forældelsen/fjernelsen** | Vi investerer i at give nye brugeroplevelser i den nye brugergrænseflade.             |
| **Erstattet af en anden funktion?**   | Den nye brugergrænseflade *Udvidet visning* erstatter den gamle brugergrænseflade.            |
| **Produktområder, der er berørt**         | Arbejdsområdet Datastyring                                                     |
| **Installationsindstilling**              | Alt                                                                           |
| **Status**                         | Forældet: Måltidsrammen for funktioner, der skal fjernes, er 2. kvartal 2018. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Punktafgifter, moms, servicemomskoden for Indien

Disse afgifter omfattes nu af indisk GST.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsagen til fjernelsen/forældelsen**       | Disse afgifter omfattes nu af indisk GST.                          |
| **Erstattet af en anden funktion?**            | Indisk GST                                                              |
| **Produktområder, der er berørt**                  | Skat                                                                     |
| **Installationsindstilling**                       | Alle moduler                                                   |
| **Status**                                  | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |    

### <a name="file-validation-utility-fvu-for-india"></a>Funktion til filvalidering (FVU) for Indien

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsagen til fjernelsen/forældelsen**       | Mangel på forbrug                                                  |
| **Erstattet af en anden funktion?**            | Nej                                                                      |
| **Produktområder, der er berørt**                  | Indisk A-skat                                                  |
| **Installationsindstilling**                       | Alle moduler                                                                    |
| **Status**                                  | Forældet: En dato for fjernelse er ikke angivet for denne funktion.   |        

### <a name="tdstcs-certificate-for-india"></a>TDS/TCS certifikat for Indien

Brugere kan hente denne formular på portalen for myndigheder.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsagen til fjernelsen/forældelsen**       | Mangel på forbrug                                                  |
| **Erstattet af en anden funktion?**            | Nej                                                                      |
| **Produktområder, der er berørt**                  | Indisk A-skat                                                  |
| **Installationsindstilling**                       | Alle moduler                                                                   |
| **Status**                                  | Forældet: En dato for fjernelse er ikke angivet for denne funktion.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Eksport/import (EXIM) tilskyndelsesordning for Indien


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsagen til fjernelsen/forældelsen**       | Mangel på forbrug                                                  |
| **Erstattet af en anden funktion?**            | Nej                                                                      |
| **Produktområder, der er berørt**                  | Import og eksport                                                       |
| **Installationsindstilling**                       | Alle moduler                                                                    |
| **Status**                                  | Forældet: En dato for fjernelse er ikke angivet for denne funktion.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Tilpassede produktanbefalinger 
Fra og med den 15. februar 2018 vil detailhandlere ikke længere kunne vise personlige produktanbefalinger på en POS-enhed. Du kan finde flere oplysninger under [Tilpassede produktanbefalinger](../../retail/personalized-product-recommendations.md).  

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Vi vil fjerne den aktuelle version af produktanbefalingstjenesten, fordi vi ændrer denne funktion og giver den en bedre algoritme og nyere detailrelaterede funktioner.  |
| **Erstattet af en anden funktion?**   | Nej Efter foråret 2018 er det dog planen at genintroducere denne funktion for at anvende en ny anbefalingstjeneste.   |
| **Produktområder, der er berørt**         | Tilpassede produktanbefalinger i POS.                                                    |
| **Installationsindstilling**              | Alt                                                                                      |
| **Status**                         |Fjernet fra og med den 15. februar 2018. Dette påvirker kunder, der kører Dynamics 365 for Retail 7.2 og nyere. |


## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Dynamics 365 for Finance and Operations, Enterprise Edition juli 2017 med Platform update 8

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Omregning af valuta for regnskabs- og rapporteringsvalutaer

Omregning af firmavaluta for regnskabs- og rapporteringsvalutaer blev indført, da euroen blev indført.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Begrænset brug og tilføjelse af funktionen Kopier den juridiske enhed som erstatning.      |
| **Erstattet af en anden funktion?**   | Nej, men funktionerne Kopier den juridisk enhed og Konfigurationer er tilføjet for at gøre det nemmere at flytte til et selskab med skiftende primære behov. |
| **Produktområder, der er berørt**         | Økonomistyring     |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.   |


### <a name="warehouse-mobile-devices-portal"></a>Warehouse Mobile Devices Portal

Warehouse Mobile Devices Portal (WMDP) er en enkeltstående komponent, der er beregnet til selvstændig installation i det lokale miljø. Denne komponent understøttes ikke længere i Finance and Operations. En oprindelig app, der forbedrer brugeroplevelsen, har erstattet WMDP-funktionaliteten.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Identiske funktioner.       |
| **Erstattet af en anden funktion?**   | Ja. Denne funktion er blevet erstattet af Finance and Operations - Lagersted. Du kan finde flere oplysninger om opsætning og forudsætninger i [Installere og konfigurere Microsoft Dynamics 365 for Finance and Operations – lager](../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Produktområder, der er berørt**         | Lokationsstyring, transportstyring     |
| **Installationsindstilling**              | Warehouse Mobile Devices Portal (WMDP) er en enkeltstående komponent, der er beregnet til selvstændig installation i det lokale miljø.               |
| **Status**                         | Forældet: Måltidsrammen for funktioner, der skal fjernes, er 4. kvartal 2019.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Avanceret sammenholdningsregel for bankafstemning til manuel sammenholdning

Den sammenholdningsregel, der blev brugt til at vælge og markere et bankdokument, da dokumenter blev sammenholdt manuelt i afstemningsarbejdsarket.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Begrænset brug.                                                                         |
| **Erstattet af en anden funktion?**   | Nej Kolonnefiltreringsfunktioner skal bruges til at finde dokumenter til afstemning. |
| **Produktområder, der er berørt**         | Kontant- og bankstyring                                                               |
| **Installationsindstilling**              | Alt                                                                                    |
| **Status**                         | Fjernet fra og med juli 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 med Platform update 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-betalingsformater for Spanien

Betalingsformater Consejo Superior Bancario blev tidligere brugt til at sende remitteringsfiler til banken for debitor- og kreditorbetalinger. Indholdet af disse formater blev tidligere bestemt af Asociación Española de Banca. Det dækker Cuaderno 19, 32, 58, 34.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.                                  |
| **Erstattet af en anden funktion?**   | Ja, ISO20022-overførsel og Direct Debit-betalingsformater for Spanien |
| **Produktområder, der er berørt**         | Debitor/kreditor                                    |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankoverførsel af betalinger for Litauen

Bankbetalingsoverførsler blev tidligere genereret og udskrevet ved hjælp af eksportformatet for betalingsoverførsler (LT) for Litauen. Det litauiske marked begyndte at bruge LITAS, det fælles elektroniske banksystem, i 2005.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.                        |
| **Erstattet af en anden funktion?**   | Ja, ISO20022-kreditoverførsel som betalingsformat for Litauen     |
| **Produktområder, der er berørt**         | Kreditor                                               |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remittering-betalingsformater for Norge

BBS Direkte Remittering-betalingsformater omfatter eksport af kundebetalingsopkrævning (Direct Debit) og import af returmeddelelse.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.  |
| **Erstattet af en anden funktion?**   | AvtaleGiro-kundebetalingsformater for Norge kan bruges til at oprette direct debit-meddelelser. Import af returmeddelelse vil blive implementeret i fremtidige versioner. |
| **Produktområder, der er berørt**         | Debitor/kreditor   |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Kontoplanværktøj for Spanien

Dette værktøj bruges, når en kontoplan i Spanien kræver omfattende ændringer. Brugere kan importere en ny kontoplan i Microsoft Excel- eller tekstformat og kan også importere regnskaber.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Begrænset brug                                                  |
| **Erstattet af en anden funktion?**   | Nej                                                             |
| **Produktområder, der er berørt**         | Finans                                                 |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80-betalingsformater for Belgien

Det gamle belgiske betalingsformat for betalingsopkrævning (Direct Debit).

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformatet bruges ikke længere.                          |
| **Erstattet af en anden funktion?**   | Ja, ISO 20022 Direct Debit-betalings format for Belgien         |
| **Produktområder, der er berørt**         | Debitor                                            |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG-betalingsformater for Schweiz

DTA/EZAG-formater integreres i ESR-systemet, fordi de kan overføre et referencenummer. Da referencenumre ikke er obligatoriske, kan disse formater bruges til at behandle alle kreditorbetalinger. Disse formater anvendes af virksomheder, der har en bankkonto et andet sted end "Postfinance".

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.                        |
| **Erstattet af en anden funktion?**   | Ja, ISO20022-kreditoverførsel som betalingsformat for Schweiz   |
| **Produktområder, der er berørt**         | Kreditor                                               |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-betalingsformat for Østrig

EDIFACT-DIRDEB-betalingsformat for betalingsopkrævning (Direct Debit).

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformatet bruges ikke længere.                          |
| **Erstattet af en anden funktion?**   | Ja, ISO 20022 Direct Debit-betalings format for Østrig         |
| **Produktområder, der er berørt**         | Debitor                                            |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="edivat-for-belgium"></a>EDIVAT for Belgien

EDIVAT er en forældet belgisk standard for elektronisk indberetning via sikker mail. Microsoft Dynamics AX 2012 bevarer den skrivebeskyttede løsning for at give adgang til de historiske data.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Funktionaliteten bruges ikke længere.                           |
| **Erstattet af en anden funktion?**   | Nej                                                             |
| **Produktområder, der er berørt**         | Finans                                                 |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL-betalingsimportformat for Norge

eGiro er baseret på den internationale FN standard EDIFACT CREMUL, (Multiple Credit Advice Message), der bruges til automatisk bogføring af betalinger fra kunder. I Microsoft Dynamics AX implementeres eGiro som et importformat for debitorbetaling.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformatet bruges ikke længere.                                                     |
| **Erstattet af en anden funktion?**   | Nej Formatet erstattes med ISO 20022-importformater i fremtidige versioner. |
| **Produktområder, der er berørt**         | Debitor                                                                       |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                            |

### <a name="external-inventory-for-poland"></a>Eksternt lager til Polen

Bevis for varer, der er taget fra en kreditor til salg uden køb. Varer, der kan håndteres i eksternt lager, som ikke påvirker standardlageret, og kan sælges og derefter købes automatisk. Denne proces opretter reelle lagerbevægelser.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af en anden funktion                                    |
| **Erstattet af en anden funktion?**   | Ja, kernefunktionalitet for indgående konsignation                |
| **Produktområder, der er berørt**         | Kreditor, Lagerstyring                         |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finansiel rapportgenerator for Østeuropa

Et værktøj bruges til at konfigurere indsamling af data til regnskabs- og momsrapporter og eksportere data til XLS og DOC rapportskabeloner.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Begrænset brug                                                                            |
| **Erstattet af en anden funktion?**   | Nej Værktøjet erstattes af elektroniske indberetningskonfigurationer i fremtidige udgivelser. |
| **Produktområder, der er berørt**         | Finans                                                                           |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import af debitorbetalingsposteringer til Finland

Du kan vælge et importformat til finske betalinger, der importerer debitorbetalingsposteringer fra en ekstern fil, der leveres af banken.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformatet bruges ikke længere.                                                     |
| **Erstattet af en anden funktion?**   | Nej Formatet erstattes med ISO 20022-importformater i fremtidige versioner. |
| **Produktområder, der er berørt**         | Debitor                                                                       |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import af betalingstransaktioner i en finanskladde til Finland

Et format, der er specifikt for Finland, bruges til import af regnskabstransaktioner i Finans.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformatet bruges ikke længere.                                                     |
| **Erstattet af en anden funktion?**   | Nej Formatet erstattes med ISO 20022-importformater i fremtidige versioner. |
| **Produktområder, der er berørt**         | Debitor                                                                       |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integration med Isabel synkroniseret (CIS) i Belgien

Isabel er rammen for elektroniske betalinger i Europa og er en de facto standard i Belgien.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Integration med Isabel-klient er blevet afbrudt.   |
| **Erstattet af en anden funktion?**   | Nej Betalingsformater, der ikke længere bruges, erstattes af ISO20022-kreditoverførselsbetalingsformat for Belgien. |
| **Produktområder, der er berørt**         | Kreditor     |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Ændringer i kontoplan og regnskabsregler for Spanien

Denne funktion bruges til ændringer i kontoplanen og regnskabsregler i Spanien. Den knytter konti for at hjælpe med at omdanne den gamle kontoplan til den nye kontoplan og sammenligner det foregående år med det nye regnskabsår, selvom de blev bogført på forskellige kontonumre.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Begrænset brug                                                  |
| **Erstattet af en anden funktion?**   | Nej                                                             |
| **Produktområder, der er berørt**         | Finans                                                 |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori-kreditorbetalingsformat

Gammelt italiensk betalingsformat for kreditoverførsler.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformatet bruges ikke længere.                          |
| **Erstattet af en anden funktion?**   | Ja, ISO20022-kreditoverførsel som betalingsformat for Italien         |
| **Produktområder, der er berørt**         | Kreditor                                               |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="payment-export-formats-for-estonia"></a>Formater til eksport af betalinger for Estland.

Telehansa- og Teleservice-formater bruges til eksport af bankens betaling.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.                        |
| **Erstattet af en anden funktion?**   | Ja, ISO20022-kreditoverførsel som betalingsformat for Estland       |
| **Produktområder, der er berørt**         | Kreditor                                               |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="payment-file-archive-for-norway"></a>Betalingsfilarkiv til Norge

Når betalingsfilerne genereres, arkiverer filarkivet automatisk alle filer, der oprettes, selv filer, der tidligere er skrevet eller læst.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af en anden funktion                                        |
| **Erstattet af en anden funktion?**   | Ja, elektronisk rapportering af arkiverede job                            |
| **Produktområder, der er berørt**         | Debitor, Kreditor og Virksomhedsadministration |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.     |

### <a name="payment-import-formats-for-estonia"></a>Formater til import af betalinger for Estland.

Telehansa- og TeleTeenus-formater bruges til import af bankens betaling.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.                                                    |
| **Erstattet af en anden funktion?**   | Nej Formaterne erstattes med ISO 20022-importformater i fremtidige versioner. |
| **Produktområder, der er berørt**         | Debitor                                                                        |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                             |

### <a name="payroll-information-in-human-resources"></a>Lønoplysninger i personale

Lønoplysninger personale

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Denne funktionalitet er blevet erstattet af grundlæggende løn- og personalesider.  |
| **Erstattet af en anden funktion?**   | **Frynsegoder**, **Indtjeninger** og andre relaterede sider, der tidligere var i amerikanske lønopgaver, er blevet ændret og er nu en del af den centrale personalekonfigurationen og støtter ekstern lønbehandling. Der opnås adgang til denne funktion ved hjælp af **Personale 1** \> **Løn**-konfigurationsnøglen. |
| **Produktområder, der er berørt**         | Personale, Løn   |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations version 1611.    |

### <a name="performance-management-goal-workflow"></a>Målarbejdsgang for performancestyring

Performancestyring omfatter målstyring og integration med performanceevalueringer.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Performancestyring er blevet ændret, og antallet af målsider blev reduceret for at forenkle processen.                 |
| **Erstattet af en anden funktion?**   | Nej Mål kan ses af ledere gennem Chefselvbetjening-portalen, og kan ændres og ses af chefen. |
| **Produktområder, der er berørt**         | Styring af menneskelig kapital       |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations version 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgirot- og Postgirot Utland-betalingsformater for Sverige

Postgirot- og Postgirot Utland-betalingsformater for Sverige.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.                        |
| **Erstattet af en anden funktion?**   | Ja, ISO20022-kreditoverførsel som betalingsformat for Sverige        |
| **Produktområder, der er berørt**         | Kreditor                                               |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="radio-frequency-identifier"></a>Radio Frequency Identification (RFID)

RFID (Radio Frequency Identification) er en teknologi til indsamling af data, hvor der bruges elektroniske mærkater til lagring af identifikationsdata og en læser uden krav om sigtelinje til registrering af disse data.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Lavt forbrug og begrænset funktionssæt.   |
| **Erstattet af en anden funktion?**   | Nej                                              |
| **Produktområder, der er berørt**         | Lagerstyring                            |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Rapport om fakturanummerering for Letland

Lettisk lovgivning indeholder særlige regler om, hvordan salgsfakturaer skal nummereres. Med funktionaliteten kan du tildele specifikke numre til salgsfakturaer, baseret på bruger eller brugergruppe. Derefter kan du generere en rapport eller en XML-fil. Du kan også udskrive en rapport om fakturanumre, der bruges.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Statsfakturanummerering skal ikke længere opretholdes. Rapporten om anvendte fakturanumre er ikke længere påkrævet. |
| **Erstattet af en anden funktion?**   | Nej       |
| **Produktområder, der er berørt**         | Debitor    |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Angiv navnene på chefen og den generelle revisor i en virksomhed til Litauen

Navnene på chefen og den generelle revisor i en virksomhed kan angives i firmaoplysningerne og bruges i forskellige lokale rapportudskrifter.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af en anden funktion                                     |
| **Erstattet af en anden funktion?**   | Ja, opsætning af embedsmænd kan bruges til samme formål.   |
| **Produktområder, der er berørt**         | Kreditor, Debitor, Kontant- og bankstyring |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.  |

### <a name="shipping-carrier-interface"></a>Fragtmandsgrænseflade

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Identiske funktioner   |
| **Erstattet af en anden funktion?**   | Delvist erstattet af Transportstyring |
| **Produktområder, der er berørt**         | Salg og marketing, Lagerstyring  |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations version 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>Telepay-betalingsformater for Norge

Telepay-betalingsformater omfatter kreditorbetalingseksport (pengeoverførsel) og kundebetalingsopkrævning (Direct Debit).

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.                                                        |
| **Erstattet af en anden funktion?**   | Ja, ISO20022-kreditoverførsel som betalingsformat og AvtaleGiro-debitorbetalingsformat til Norge |
| **Produktområder, der er berørt**         | Debitor/kreditor                                                          |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Eksportformater til kreditorbetalinger for Finland

Der findes to formater til eksport af betalinger for Finland. LM02 (FI) bruges til indenlandske betalinger, og LUM2 (FI) bruges til betaling til udlandet.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Betalingsformaterne bruges ikke længere.                        |
| **Erstattet af en anden funktion?**   | Ja, ISO20022-kreditoverførsel som betalingsformat for Finland       |
| **Produktområder, der er berørt**         | Kreditor                                               |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="warehouse-management-ii"></a>Lokationsstyring II

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Lagerstyring II-løsningen (WMS II), der er tilgængelig i modulet **Lagerstyring**, dublerer funktioner i det **Lagerstyring**-modul, der blev udgivet i Microsoft Dynamics AX 2012 R3.                                                                         |
| **Erstattet af en anden funktion?**   | **Lagerstyring**-modulet, der blev udgivet i AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 og Dynamics AX 2012 R3 CU9, erstatter funktionerne i Lagerstyring II. Det nye modul har mere avancerede funktioner og mere fleksible processer til styring af lagersted end dem, der blev tilbudt til Lagerstedsstyring II. |
| **Produktområder, der er berørt**         | Lagerstyring, salg og marketing, indkøb og forsyning   |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations version 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Påmindelser for arbejdere i Personale

Lønoplysninger personale

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Lav belastning                                                           |
| **Erstattet af en anden funktion?**   | Nej                                                                  |
| **Produktområder, der er berørt**         | Personale                                                     |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations version 1611 |

### <a name="workflow-for-creating-goals"></a>Arbejdsgang for oprettelse af mål

En arbejdsgang til styring af oprettelse af medarbejdermål er et af flere arbejdsgange, der kan hjælpe med at koordinere performancestyringsprocessen.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Performancestyring er blevet ændret fuldstændigt i Microsoft Dynamics 365 for Finance and Operations.     |
| **Erstattet af en anden funktion?**   | Den nyudviklede funktion til performancestyring giver bedre kontrol over indholdet af mål, de mål, der bruges til at spore forløbet, og den vedhæftede fil med yderligere dokumentation. Mål kan gemmes som skabeloner og genbruges derefter. Denne funktion kan hjælpe dig med at konfigurere yderligere mål for medarbejderne hurtigere. |
| **Produktområder, der er berørt**         | Styring af menneskelig kapital                 |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations version 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Mulighed for at annullere ændringer af en kreditorfaktura

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Performanceforbedring        |
| **Erstattet af en anden funktion?**   | Nej                             |
| **Produktområder, der er berørt**         | Kreditor               |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0 |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD og AxBC integrationer

I Application Integration Framework (AIF) kan data udveksles med eksterne systemer via forretningslogik, der vises som tjenester. Dynamics AX indeholder tjenester, der er baseret på dokumenter og .NET Business Connector (AxBC). Der oprettes et dokument ved hjælp af XML. XML-filen indeholder hovedoplysninger, der er tilføjet for at oprette en *meddelelse*, der kan overføres til eller fra Dynamics AX. Eksempler på dokumenter omfatter salgsordrer og indkøbsordrer. Næsten enhver enhed, f.eks. en kunde, kan dog være repræsenteret af et dokument. Tjenester, der er baseret på dokumenter, bruger **Axd \<Dokument\>**-klasser.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Arkitekturen i AIF og AxDs kan ikke skaleres til en skytjeneste. Der var problemer med ydeevnen omkring masseimport.                                        |
| **Erstattet af en anden funktion?**   | Denne funktion er erstattet af Struktur til dataimport/-eksport, som understøtter tilbagevendende masseimport/eksport. AxBC anbefaler vi, at du bruger tabellerne. |
| **Produktområder, der er berørt**         | AxDs, AxBCs og AIF   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0   |

### <a name="billing-code-rate-scripts"></a>Satsscripts for faktureringskode

Faktureringsscripts blev anvendt til at beregne faktureringssatser for faktureringskoder. Disse scripts krævede brugertilpasset udvikling i programmeringssproget C Sharp eller Visual Basic. I den aktuelle version af Dynamics AX er **satsscripts for faktureringskoder** ikke understøttet.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Understøttelsen af de brugerdefinerede C Sharp- eller Visual Basic-scripts blev ikke tilføjet i Dynamics AX 7.0. |
| **Erstattet af en anden funktion?**   | Nr.                                                                                      |
| **Produktområder, der er berørt**         | Den offentlige sektor, debitor                                    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0                                                          |

### <a name="boms-without-bom-versions"></a>Styklister uden styklisteversioner

Når **Styklisteversioner**-konfigurationsnøglen var deaktiveret, blev styklisteversioner skjult i alle formularer, og systemet ville gennemtvinge en 1:1 relation mellem frigivne produkter og styklister. **Styklisteversioner**-konfigurationsnøglen kan ikke være deaktiveret i den aktuelle version af Dynamics AX.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Når du bruger en konfigurationsnøgle til styring, skaleres styklisteversioner ikke i et skymiljø. |
| **Erstattet af en anden funktion?**   | Nej                                                                                      |
| **Produktområder, der er berørt**         | Administration af produktoplysninger, Lagerstyring                                    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0                                                          |

### <a name="brazilian-bordero"></a>Brasiliansk Bordero

Specifik betalingsmåde for brasilianske virksomheder

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Understøttelse af brasiliansk Bordero-betalingsmåde er blevet afbrudt fra brasiliansk lokalisering |
| **Erstattet af en anden funktion?**   | Nej   |
| **Produktområder, der er berørt**         | Kreditor   |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="brazilian-sintegra-statement"></a>Brasiliansk Sintegra-opgørelse

Momsangivelse for ICMS-moms

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Denne opgørelse er ikke længere gældende i visse brasilianske stater. |
| **Erstattet af en anden funktion?**   | Nej Brugere kan bruge generisk elektronisk rapporteringsværktøj for at konfigurere opgørelsen, hvis det er påkrævet under bestemte situationer. |
| **Produktområder, der er berørt**         | Regnskabsbøger    |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasiliansk SCAN-beredskabstilstand for NF-e

(SCAN) beredskabsmiljø bruges til at oprette, eksportere og importere status for en Nota Fiscal eletrônica (NF-e), når miljøet i Secretaria da Fazenda (SEFAZ) ikke er tilgængeligt.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Denne beredskabsmetode er ikke længere gældende i alle brasilianske stater |
| **Erstattet af en anden funktion?**   | Nej                                                                          |
| **Produktområder, der er berørt**         | Debitor                                                         |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.              |

### <a name="business-analyzer"></a>Forretningsanalyse

Med dette mobilprogram kan brugerne gennemse vigtige virksomhedsmål.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Denne funktion er blevet erstattet af en anden funktion.   |
| **Erstattet af en anden funktion?**   | Indholdspakken Overvågning af økonomisk performance til Microsoft Power BI omfatter vigtige økonomiske nøgletal, der tidligere var tilgængelige i Business Analyzer. |
| **Produktområder, der er berørt**         | Finans      |
| **Status**                         | Forældet: Brugen af Business Analyzer er forældet.    |

### <a name="business-statistics"></a>Handelsstatistik

Konfiguration af forespørgsler vedrørende handelsstatistik, som kan bidrage til analysen af organisationens performance

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ældre tilgang til business intelligence (BI), lavt forbrug og et begrænset funktionssæt |
| **Erstattet af en anden funktion?**   | Nye BI-løsninger til den aktuelle version af Dynamics AX                                      |
| **Produktområder, der er berørt**         | Indkøb og forsyning, Kreditor, Salg og marketing, Debitor.         |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Ændre dokumentdatofunktion i fakturagodkendelseskladde

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Lav belastning                                                               |
| **Erstattet af en anden funktion?**   | Ja. Bilagsdato på den bogførte kreditorpostering kan ændres. |
| **Produktområder, der er berørt**         | Kreditor                                                        |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03-betalingsformat for Nederlandene

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Formatet er ikke længere gældende i Nederlandene, fordi det er blevet erstattet af SEPA-funktioner. |
| **Erstattet af en anden funktion?**   | Eksport af SEPA-betalinger  |
| **Produktområder, der er berørt**         | Alle moduler     |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.   |

### <a name="compliance-center"></a>Overholdelsescenter

Overholdelsescenter var et Enterprise Portal-websted til administration af dokumentationskrav for overholdelsesinitiativer vedrørende Sarbanes-Oxley-loven.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Mangel på forbrug. Microsoft SharePoint indeholder samme egenskab, der var tilgængelig i Overholdelsescenter. |
| **Erstattet af en anden funktion?**   | Nej   |
| **Produktområder, der er berørt**         | Overholdelse og interne kontroller  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0    |

### <a name="connector-for-microsoft-dynamics"></a>Connector til Microsoft Dynamics

Dette værktøj blev brugt til at integrere vigtige data fra Microsoft Dynamics CRM i Microsoft Dynamics ERP-applikationer.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Denne funktion er blevet erstattet af en anden funktion. |
| **Erstattet af en anden funktion?**   | Common Data Service                                      |
| **Produktområder, der er berørt**         | Connector til Microsoft Dynamics                         |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Containerenhed og flerdimensionale beholdninger

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Identiske funktioner |
| **Erstattet af en anden funktion?**   | Ja. Denne funktionalitet er blevet erstattet af konsolideret batchordre-funktionssæt siden AX 2012. Denne funktion omfatter den konsoliderede disponible visning. |
| **Produktområder, der er berørt**         | Administration af produktoplysninger, Produktionsstyring, Lagerstyring, Salg og marketing  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0 |

### <a name="cue-group-metadata"></a>Køgruppemetadata

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Køgrupper blev brugt til at vise en eller flere køer i faktaboksområdet. Der var begrænset optagelse, og der var også problemer med ydeevnen, fordi en ændring af en post i en overordnet formular forårsagede en forespørgsel pr. kø i gruppen Kø. |
| **Erstattet af en anden funktion?**   | Nej      |
| **Produktområder, der er berørt**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0  |

### <a name="cue-metadata"></a>Kømetadata

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Kømetadata var begrænset til antals- eller beløbsoplysninger.    |
| **Erstattet af en anden funktion?**   | Feltmetadata blev indført for at give større fleksibilitet for modellering. Du kan f.eks. modellere aktuelle tæller-, navigations- og nøgletal (KPI'er). Metadata for antalsfelter er den direkte erstatning af Kømetadata. |
| **Produktområder, der er berørt**         | Alle moduler           |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Dansk checkformat

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Det danske checklayout format understøttes ikke længere, og rapporten er blevet fjernet fra lokaliseringen til dansk. |
| **Erstattet af en anden funktion?**   | Nej    |
| **Produktområder, der er berørt**         | Alle moduler    |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.  |

### <a name="data-partitions"></a>Datapartitioner

Datapartitioner giver en logisk adskillelse af dataene i Microsoft Dynamics AX-databasen.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Datapartitioner blev introduceret i Microsoft Dynamics AX 2012 R2 for at give mulighed for dataisolering. I et almindeligt scenarie har en virksomhed datterselskaber, og data fra ét datterselskab bør ikke være synlige for et andet datterselskab, selvom begge datterselskaber, der administreres af samme it-afdeling. Dog var ekstra scripts og indirekte administrationsomkostninger i hele programmet påkrævet for at oprette nye partitioner og udfylde dem med data og til sikkerhedskopiering af data på partitionen. I skyen, hvor vi har adgang til PaaS-databasetjenester (platform som en tjeneste) (Microsoft Azure, SQL Database), er det langt mere effektivt at bruge en database som isolationscontainer end at udføre isolation i programmet. Uanset om datapartitionering er påkrævet for datterselskaber, for flere lejere eller blot af skaleringsårsager, mener vi, at scenarierne kan håndteres bedre gennem flere Finance and Operations-forekomster. |
| **Erstattet af en anden funktion?**   | Kunder, der bruger datapartitioner, skal bruge flere forekomster af Finance and Operations, hvis separation på databaseniveau er af vigtighed.    |
| **Produktområder, der er berørt**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0  |


### <a name="database-and-file-share-storage-for-attachments"></a>Database- og filshare-lagring for vedhæftede filer

Microsoft Dynamics AX 2012 tillader lagring af vedhæftede filer i databasen og i filshares. Ingen af disse indstillinger understøttes længere.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Filsharelagring understøttes ikke længere, fordi skybaserede miljøer ikke kan kommunikere med lokale filshares. Databaselagring er forældet og erstattes af Azure Blob-lagring. Azure Blob-lagring svarer til lagring i databasen, fordi der kun er adgang til dokumenter via Dynamics 365 for Finance and Operations-klientformularer. Dette giver den ekstra fordel, at pladsen til lagring ikke har en negativ effekt på databasens ydeevne. Blob-lagring er standardlagringsmekanismen til dokumentstyring, og den fungerer med det samme. |
| **Erstattet af en anden funktion?**   | Databaselagring er forældet og erstattes af Azure Blob-lagring.   |
| **Produktområder, der er berørt**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0   |

### <a name="delimitation"></a>Afgrænsning

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ingen brug af funktionen blev ikke fundet. |
| **Erstattet af en anden funktion?**   | Nej                                     |
| **Produktområder, der er berørt**         | Tid og Fremmøde                    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0         |

### <a name="desktop-client"></a>Desktopklient

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Dynamics AX-klientoplevelsen er blevet ændret for at forbedre brugervenligheden på tværs af flere platforme og enheder.                      |
| **Erstattet af en anden funktion?**   | Den nye webklient er baseret på skrivebordsformularens metadata- og programmeringsmodel, der er blevet ændret for at give plads til en omfattende webplatform. |
| **Produktområder, der er berørt**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0   |

### <a name="direct-database-connection"></a>Direkte databaseforbindelse

I Dynamics AX 2012 R3 kunne Retail Modern POS forbindes direkte med kanaldatabasen på lignende måde som Enterprise POS. Dette var ud over den almindelige kommunikationsmetode for Retail Modern POS-kommunikation via Retail Server.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Direkte databaseforbindelse krævede lavere sikkerhedsprotokoller og blev primært brugt til at opnå den bedst mulige ydeevne. På grund af bedre ydeevne og sikkerhedsmæssige forbedringer i Finance and Operations medfører denne funktion nu flere problemer, end den løser. |
| **Erstattet af en anden funktion?**   | Nej Kun standard Retail Server-kommunikation understøttes nu.  |
| **Produktområder, der er berørt**         | Kanaldatabase/Retail Modern POS   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0  |

### <a name="dutch-swift-mt940"></a>Nederlandsk SWIFT MT940

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Generiske funktioner bruges nu i stedet for oversat funktionalitet.                    |
| **Erstattet af en anden funktion?**   | Ja, denne funktion er erstattet af funktionen Avanceret bankafstemning. |
| **Produktområder, der er berørt**         | Alle moduler                                                                              |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL-adresse for Tyskland)

Denne funktionalitet leverede XBRL-output (eXtensible Business Reporting Language), der er beregnet specifikt til den tyske eBilanz-taksonomi.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Mangel på forbrug  |
| **Erstattet af en anden funktion?**   | Denne funktion er ikke erstattet af en anden funktion, men flere specialiserede XBRL-pakker, der giver omfattende XBRL-funktionalitet, er tilgængelige for det tyske marked. |
| **Produktområder, der er berørt**         | Management Reporter      |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.  |

### <a name="enterprise-portal-client"></a>Enterprise Portal-klient

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Har fået tildelt en enkelt klientplatform.  |
| **Erstattet af en anden funktion?**   | Den nye webklient er baseret på skrivebordsformularens metadata- og programmeringsmodel, der er blevet ændret for at give plads til en omfattende webplatform. |
| **Produktområder, der er berørt**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0   |

### <a name="environmental-sustainability"></a>Miljømæssig bæredygtighed

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Lavt forbrug og begrænset funktionssæt  |
| **Erstattet af en anden funktion?**   | Nej              |
| **Produktområder, der er berørt**         | Overholdelse og interne kontroller, Kreditor  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0 |

### <a name="form-activex-and-managed-host-controls"></a>Kontrolelementer til ActiveX-formular og administrerede vært

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Kontrolelementerne til ActiveX og administreret vært er baseret på den forældede klient til stationære computere. |
| **Erstattet af en anden funktion?**   | Kontrolstruktur, som kan udvides, understøtter opbygning af nye kontrolelementer, der er baseret på HTML, CSS og JavaScript, og er en førsteklasses kontrol i Microsoft Visual Studio-værktøjsmiljøet. |
| **Produktområder, der er berørt**         | Alle moduler     |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0       |

### <a name="generate-prenotes-by-using-a-batch"></a>Opret adviseringer ved hjælp af en batch

Oprettelsen af adviseringer kan ikke udføres ved hjælp af et batch, men kan stadig udføres af en bruger.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Der findes ingen formular til at fastholde og vise den resulterende adviseringsfil, når den er oprettet ved hjælp af et batch. |
| **Erstattet af en anden funktion?**   | Der kan stadig oprettes adviseringer, og brugeren har kontrol over, hvor filen gemmes.   |
| **Produktområder, der er berørt**         | Kreditor, Debitor, Kontant- og bankstyring  |
| **Status**                         | Fjernet fra og med AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Tysk DTAUS betalingseksporter og kontoopgørelsesimport (totaler og transaktioner)

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Formatet er ikke længere gældende i Tyskland, fordi det er blevet erstattet af SEPA-funktioner (Single Euro Payments Area).                    |
| **Erstattet af en anden funktion?**   | Ja, denne funktionalitet er blevet erstattet af eksport af SEPA-betaling og avancerede bankafstemningsfunktioner til import af kontoudtog. |
| **Produktområder, der er berørt**         | Alle moduler  |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="german-dtazv-payment-format"></a>Tysk DTAZV-betalingsformat

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Formatet er ikke længere gældende i Tyskland, fordi det er blevet erstattet af SEPA-funktioner. |
| **Erstattet af en anden funktion?**   | Eksport af SEPA-betalinger    |
| **Produktområder, der er berørt**         | Alle moduler   |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.    |

### <a name="german-mt940-import"></a>Tysk MT940-import

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Generiske funktioner bruges nu i stedet for oversat funktionalitet.                    |
| **Erstattet af en anden funktion?**   | Ja, denne funktion er erstattet af funktionen Avanceret bankafstemning. |
| **Produktområder, der er berørt**         | Alle moduler                                                                              |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.                           |

### <a name="german-xml-eu-sales-list"></a>Tysk EU-listesystem i XML-format

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | XML-format til rapportering af tysk EU-listesystem understøttes ikke længere. Kun ELMA5-tekstfilformatet kan bruges til at sende rapporten for EU-listesystemet til de tyske skattemyndigheder. |
| **Erstattet af en anden funktion?**   | Nej         |
| **Produktområder, der er berørt**         | Skat        |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.   |

### <a name="gl-ssrs-reports"></a>GL SSRS-rapporter

Rapporter, der indeholder følgende menupunkter, er blevet fjernet: **Råbalanceoversigt**, **Detaljeret råbalance**, **Kontoplan**, **Revisionsspor**, **Saldi** og **Saldoliste**.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Økonomirapporter til Microsoft SQL Server Reporting Services (SSRS) er blevet erstattet af Management Reporter-funktioner og standardrapporter. |
| **Erstattet af en anden funktion?**   | Management Reporter (med navnet **Økonomirapportering** i den aktuelle version af Dynamics AX)    |
| **Produktområder, der er berørt**         | Finans   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart og FormPart-metadata

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | InfoPart og FormPart-metadata aktiverede oprettelsen af faktabokse for to forskellige klienter. |
| **Erstattet af en anden funktion?**   | InfoPart-metadata, som var en definition i forenklet form, er konverteret til en formular ved hjælp af opgraderingsværktøj. FormPart-metadata, som refererede til en formular, er erstattet af en mere direkte reference, der oprettes af opgraderingsværktøj. |
| **Produktområder, der er berørt**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0        |

### <a name="main-account-list-page"></a>Hovedkonto-listeside

En liste over konti for den juridiske enhed og relaterede saldooplysninger

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Saldooplysninger er tilgængelige på listesiden **Råbalance** pr. konto og dimension.  |
| **Erstattet af en anden funktion?**   | **Hovedkonti** indeholder den samme liste over konti, som listesiden **Hovedkonto** indeholdt. Gittervisningen i **Hovedkonti** viser også en endnu mindre, gitterlignende visning. |
| **Produktområder, der er berørt**         | Finans      |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaysia og Singapore bankpengestrømsrapport

Med denne funktion kan brugeren udskrive en pengestrømsanalyse, der viser transaktioner og detaljer i indgående og udgående pengestrømme for et bestemt datointerval for udvalgte bankkonti.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | De samme oplysninger kan fås fra bankposteringen Forespørgsel. |
| **Erstattet af en anden funktion?**   | Bankposteringen Forespørgsel                                            |
| **Produktområder, der er berørt**         | Kontant- og bankstyring                                                |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion.          |

### <a name="mexican-cfd-electronic-invoice"></a>Mexicansk elektronisk CFD-faktura.

Denne funktion muliggjorde oprettelse af mexicanske elektroniske fakturaer ved hjælp af CFD-metoden (Comprobante finansiel Digital), hvor virksomheden underskriver fakturaen ved at anmode om relateret tilladelse fra regeringen. Denne funktion leverer også en månedlig rapport, der omfatter alle de elektroniske fakturaer, der er udstedt i perioden.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Denne metode anvendes ikke længere. Generering af elektroniske fakturaer ved at bruge CFD-metoden er blevet udfaset af skattemyndighederne og erstattet af CFDI-metoden (Comprobante Fiscal Digital a través de Internet ), hvor undertegnelse er uddelegeret til tredjepartsudbyderen (PAC). Den månedlige rapport er blevet fjernet, og brugerne kan bruge en forespørgselsindstilling til at forhøre sig om historiske transaktioner. |
| **Erstattet af en anden funktion?**   | Nej    |
| **Produktområder, der er berørt**         | Debitor, Projekt   |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="mexico-realized-and-unrealized-vat"></a>Mexico, realiseret og ikke-realiseret købsmoms

Microsoft Dynamics AX 2012 administrerede ikke-realiseret købsmoms ved hjælp af Mexico-specifik funktionalitet til ikke-realiseret moms.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Identiske funktioner  |
| **Erstattet af en anden funktion?**   | Ja, denne funktion er erstattet af almindelig betinget momsfunktionalitet, der leveres af Kerne. |
| **Produktområder, der er berørt**         | Skat   |
| **Status**                         | Forældet: En dato for fjernelse er ikke angivet for denne funktion. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-integration


|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Denne funktion er blevet erstattet af Microsoft Exchange Server-integration. |
| **Erstattet af en anden funktion?**   | Ja                                                                            |
| **Produktområder, der er berørt**         | Sales and Marketing                                                            |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Privat blokering af lager- og lokationsstyringskladder

Lager- og lokalitetsstyringskladderne understøtte ikke længere muligheden for at markere en kladde som privat for den valgte bruger. Kun processen med at blokere kladder som private for brugergrupper og blokering under redigering understøttes.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ingen brug af funktionen blev ikke fundet. |
| **Erstattet af en anden funktion?**   | Nej                                     |
| **Produktområder, der er berørt**         | Lagerstyring                   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0         |

### <a name="product-builder"></a>Product Builder

Product Builder blev brugt til at konfigurere varer dynamisk fra en salgsordre, en indkøbsordre, en produktionsordre, et salgstilbud, et projekttilbud eller et varebehov. Baseret på en produktmodel, der havde modelvariabler, kunne brugeren vælge værdier, der opfyldte kundekrav og få en entydig produktvariant, der havde en stykliste og rute.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Product Builder viste X ++-kode for slutbrugere. Det understøttes ikke i den aktuelle version af Dynamics AX. Det er blevet fjernet for at undgå dobbelt vedligeholdelsesarbejde på overlappende kodebaser, hvor størrelsen kan tilpasses.  |
| **Erstattet af en anden funktion?**   | Ja. Begrænsningsbaseret konfiguration blev introduceret i Dynamics AX 2012, hvor afskrivningen af Product Builder i fremtidige versioner allerede blev offentliggjort. Den begrænsningsbaserede konfigurationsteknologi vælges på produktmasterne for at aktivere konfigurationen. Du kan finde flere oplysninger under [Bygge en produktkonfigurationsmodel](../../supply-chain/pim/build-product-configuration-model.md). |
| **Produktområder, der er berørt**         | Administration af produktoplysninger, Salg og marketing  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0      |

### <a name="production-floor-app"></a>Appen Production Floor
Dette er appen til tabletenheder, der kører Windows 8.1 RT og Windows 8.1 Pro.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Med ændringen af en webbaseret klient er det muligt at levere lignende funktionalitet via den oprindelige Dynamics AX 7.0-klient. Jobkortenheden indeholder en brugergrænseflade til produktionsanlægget, der er optimeret til touch- og tabletformfaktorer. |
| **Erstattet af en anden funktion?**   | Ja. Jobkortenheden, der er en oprindelig del af Dynamics AX 7.0.                                                                           |
| **Produktområder, der er berørt**         | Produktionsstyring                                                |
| **Status**                         | Forældet: Der er endnu ikke er fastsat en dato for fjernelse af denne funktion fra Microsoft Store.                                                |


### <a name="rename-product-dimension"></a>Omdøb produktdimension

Med denne funktion kan du ændre navnet på en af de tre standardproduktdimensioner (størrelse, farve eller typografi) til et navn, der passer bedre til virksomhedens behov. Omdøbning inkluderer alle de etiketter, hvor produktdimensionsnavnet blev brugt.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Den aktuelle version af Dynamics AX understøtter ikke ændringer af etiketter på kørselstidspunktet. |
| **Erstattet af en anden funktion?**   | Nej                                                                            |
| **Produktområder, der er berørt**         | Administration af produktoplysninger                                                |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0                                                |

### <a name="retail-server-connectivity-using-http"></a>Retail Server-forbindelse ved hjælp af HTTP

I Dynamics AX 2012 R3 kunne Retail Server fungere ved hjælp af HTTP-kommunikation (ikke-sikret). Dette var ud over standardkommunikationen via HTTPS.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | På grund af nye sikkerhedskrav understøttes nu kun sikret kommunikation ved hjælp af TLS 1.2 (eller nyere, afhængigt af tilgængelighed). Det selvbetjente installationsprogram konfigurerer automatisk computeren til denne kommunikation. |
| **Erstattet af en anden funktion?**   | Nej Kun standard HTTPS-kommunikation understøttes nu. |
| **Produktområder, der er berørt**         | Detailserver  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0 |

### <a name="role-center-pages"></a>Sider for rollebaserede områder

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Sider med det rollebaserede område var baseret på den forældede Enterprise Portal-platform, som er blevet erstattet af den nye webklientplatform i den aktuelle version af Dynamics AX. |
| **Erstattet af en anden funktion?**   | Den nye arbejdsområdeformularmønster giver brugere et procescentreret design, der giver nem adgang til ofte anvendte opgaver inden for denne proces.                       |
| **Produktområder, der er berørt**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Momsjurisdiktionsområder

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Lavt forbrug og begrænset funktionssæt |
| **Erstattet af en anden funktion?**   | Nej                                           |
| **Produktområder, der er berørt**         | Amerikansk moms                                 |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0               |

### <a name="sites-services"></a>Webstedstjenester

Med webstedstjenester kan du opbygge websteder, der udvider dine forretningsprocesser til internettet uden it-support.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Microsoft Azure-infrastrukturen, der bruges af Dynamics AX, indeholder nye funktioner, der kan bruges i stedet (f.eks Azure websteder). |
| **Erstattet af en anden funktion?**   | Nej   |
| **Produktområder, der er berørt**         | Rekruttering af personale, sagsstyring, anmodningen om tilbud, registrering af kreditorer, arbejdsområder til samarbejde for salgsmuligheder og kampagner  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0    |

### <a name="ssas-demand-forecasting-strategy"></a>Strategi for SSAS-behovsprognose

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Udformningen af funktionen understøttes ikke i den nye cloud-arkitektur. |
| **Erstattet af en anden funktion?**   | Strategi for Azure Machine Learning-behovsprognose                           |
| **Produktområder, der er berørt**         | Varedisponering                                                              |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Kreditorfakturapulje ekskl. bogføringsdetaljer

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Lav belastning. Denne funktionalitet er blevet erstattet af fakturajournalen med arbejdsgangens funktionalitet. |
| **Erstattet af en anden funktion?**   | Funktioner i arbejdsgang for fakturajournal.     |
| **Produktområder, der er berørt**         | Kreditor |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0    |


### <a name="virtual-company-accounts"></a>Virtuelle regnskaber

Funktionen til virtuelle regnskaber understøttes ikke længere i Dynamics AX. Funktionen til virtuelle regnskaber gør det muligt for brugere at oprette tabeller, der skulle deles med en række regnskaber. Du kan finde en beskrivelse af funktionen her: [Regnskaber og virtuelle regnskaber](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Funktionen fungerer ved at gruppere tabeller i samlinger, der er tildelt til virtuelle regnskaber, som er grupper af eksisterende "reelle" regnskaber. Forespørgsler oprettes, så alle regnskaber i det virtuelle regnskab kan få adgang til dataene i tabellerne i de tilknyttede tabelsamlinger.

|   |  | 
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | - Virtuelle regnskaber skal konfigureres, før data gemmes i tabellerne. Baglæns tilpasning af virtuelle regnskaber til en eksisterende installation er meget vanskeligt.<br><br>- Da der har været meget datanormalisering i den aktuelle version af Dynamics AX, er det blevet meget vanskeligt at vide, hvad der skal tilføjes i tabelsamlingen. For eksempel er det svært at vide, hvilke tabeller der skal deles. Alle de tabeller, der refereres til fra tabeller, der er i et virtuelt regnskab, skal også tilføjes. Grundet tabelnormalisering skal selv simple stamdata, der er spredt over flere tabeller, være en del af det virtuelle regnskab. Eventuelle fejl, der er foretaget her, vil medføre funktionelle problemer.<br><br>- Når en tabel er en del af et virtuelt regnskab, mister den oplysninger om oprindelsen af dataene, og kun det virtuelle regnskab registreres.   |
| **Erstattet af en anden funktion?** | Globale tabeller kan bruges til at gøre tabeller tilgængelige fra alle regnskaber. Der er i øjeblikket ingen erstatning. |   
| **Produktområder, der er berørt**       | Alle moduler |   
| **Status**                       | Fjernet fra og med Dynamics AX 7.0   |   

### <a name="windows-8-tablet-app"></a>App til Windows 8-tablet

Windows 8 tablet-appen leverede funktionalitet til udgiftsregistrering og -godkendelse.

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Finance and Operations er kompatibel med tablets. Der er ikke længere brug for tabletappen.    |
| **Erstattet af en anden funktion?**   | Nej          |
| **Produktområder, der er berørt**         | Udgiftsstyring   |
| **Status**                         | Fjernet: Denne funktion er kun tilgængelig for Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Arbejdsplanlægning

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Lav belastning |
| **Erstattet af en anden funktion?**   | Nej, men siden **Profilrelation**, som åbnes fra siden **Profilgrupper**, understøtter det samme forretningsscenario som den forældede **Arbejdsplanlægning**-side. |
| **Produktområder, der er berørt**         | Tid og Fremmøde     |
| **Status**                         | Koden er ikke blevet fjernet. Formularen, JmgWorkPlanner, blev dog ikke flyttet.    |

### <a name="x-financial-statements"></a>X++-regnskaber

|                                                 |                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Årsagen til forældelsen/fjernelsen</strong> |                         Denne funktion er blevet erstattet af en anden funktion.                         |
|  <strong>Erstattet af en anden funktion?</strong>  | Management Reporter (med navnet <strong>Økonomirapportering</strong> i den aktuelle version af Dynamics AX) |
|     <strong>Produktområder, der er berørt</strong>     |                                              Finans                                              |
|             <strong>Status</strong>             |                                      Fjernet fra og med Dynamics AX 2012                                      |

