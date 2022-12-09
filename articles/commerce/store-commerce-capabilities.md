---
title: Store Commerce-appfunktioner
description: Denne artikel beskriver de funktioner, som er tilgængelige i Store Commerce-appen til Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788506"
---
# <a name="store-commerce-app-capabilities"></a>Store Commerce-appfunktioner

[!include [banner](includes/banner.md)]

Store Commerce-appen er den moderne POS-oplevelse til Microsoft Dynamics 365 Commerce. Det giver virksomheder mulighed for at behandle transaktioner i butikken og administrere drift som f.eks. lager- og ordreprocessen. Appen giver også firmaer mulighed for at administrere kunderelationer med fordelskunder og kundeaktiviteter. 

Store Commerce-appen, der styres af Commerce Scale Unit (CSU), leverer en komplet omnikanalløsning. En kunde kan f.eks. købe et produkt online og afhente det i en nærliggende butik og dermed fortsætte med indkøb på tværs af kanaler uden at miste data. 

Denne artikel giver et overblik over egenskaberne i Store Commerce-appen.

## <a name="platform"></a>Platform

| Egenskab | Beskrivende tekst | Dokumentation | Supplerende indhold |
|---|---|---|---|
| Omnikanal | Dynamics 365 Commerce leverer en omfattende omnikanalløsning, der forener administrations-, butiks-, callcenter- og digitale erfaringer. | [Overblik](index.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Headless Commerce | Commerce Scale Unit er vært for konsolløst Commerce-program. Konsolløst Commerce-program fungerer som det centrale punkt for al handelsforretningslogik og en styrer en komplet omnikanalløsning. | <p>[Arkitektonisk oversigt](commerce-architecture.md)</p><p>[Konsolløs arkitektur](dev-itpro/retail-server-architecture.md)</p> | [Teknisk gennemgang](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce Headquarters | Commerce headquarters indeholder back-office-funktioner, der giver mulighed for at konfigurere produkter, medarbejdere, forretningsprocesser, priser og andre funktioner, der kræves for virksomheden. | [Arkitektonisk oversigt](commerce-architecture.md) | |
| POS (salgssted) | Store Commerce-appen er POS-oplevelsen for Dynamics 365 Commerce. Den indeholder rige funktioner og omfattende POS-egenskaber, der hjælper salgsmedarbejdere, ekspedienter og chefer med at levere fremragende kundeservice. Desuden indeholder den flere implementeringsindstillinger til detailforretninger, hjælper med at forbedre ydeevnen og giver forbedret administration af programlivscyklus (ALM). | [Store Commerce-app](dev-itpro/store-commerce.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Video](https://youtu.be/7B332XH_zfs)</p><p>[Overføre fra MPOS til Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Skyinstallation | Flere forekomster af Commerce Scale Units kan implementeres med henblik på belastningsfordeling og geografisk afstand. | [Skyinstallation](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Lokal installation | Ved hjælp af en installation af lokale firmadata kan Commerce-kunder have mere ejerskab over og administration af et Dynamics 365-miljø. | [Lokal installation](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Enhedsstyring

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Flere formfaktorer | Store Commerce-appen understøttes på flere enhedsformfaktorer, f.eks. computere, tablets og mobilenheder. Med den dynamiske brugergrænseflade kan layoutet ændres automatisk og tilpasses skærmstørrelsen. | [Visuelle konfigurationer](pos-screen-layouts.md) |  |
| Tværplatform | Store Commerce-appen understøttes på internettet, Windows, iOS og Android-platforme. | [Platforme](dev-itpro/hybridapp.md) | |
| Branding | Skærmdesigneren giver dig mulighed for at tilpasse skærmlayout, så de opfylder dine forretningsbehov. Desuden kan der oprettes temaer, layout, farver og billeder baseret på medarbejderroller, og derefter kan de deles på tværs af brugerne, så de har ensartethed og brugervenlighed. | [Visuelle konfigurationer](pos-screen-layouts.md) | [Video](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topologi | Forskellige topologier i butikken understøttes baseret på netværkstilgængelighed. | <p>[Topologi](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Infografik](dev-itpro/retail-in-store-topology.md)</p> | |
| Styring af flere enheder | Det er nemt at administrere flere enheder på tværs af butikker fra Commerce headquarters. | [Aktivering](set-up-activation-accounts-validate-devices-hq.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Medarbejderstyring

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Logon | Hver butiksmedarbejder kan have et dedikeret logon. Typerne for logon omfatter brugernavn, stregkode, magnetstribelæser (MSR), biometrik og Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Udvidet logon](extended-logon.md)</p> | |
| Rettigheder | Medarbejdere understøttes på forskellige rettighedsniveauer, f.eks. tilladelser til at oprette ordrer og tilladelse til at redigere ordrer. | [Rettigheder](tasks/create-pos-permission-groups.md) | |
| Tids- og fremmødestyring | Fremmøde kan administreres ved hjælp af funktionen Tidsur. Fremmødedata kan behandles i løn ved hjælp af Dynamics 365 Human Resources-appen. | [Tidsstyring](retail-time-attendance.md) | |
| Salgsprovision | Salg kan spores efter sælger for at beregne provision eller andre incitamenter. | [Provision i standardvaluta](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Merchandizing

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Sortimentsstyring | Markedsføringschefer kan sortere produkter, så de er parat til salg i en bestemt kanal og i en bestemt periode. | [Udvalg](assortments.md) | |
| Kataloger | Markedsføringschefer kan administrere kataloger for at identificere de produkter, de vil tilbyde med katalogspecifik prissætning. | [Kataloger](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Kategori- og produktstyring | I Commerce headquarters kan markedsføringschefer oprette produkter med varianter, attributter, en måleenhed osv. De kan også definere en kategorihierarki for at organisere produkter. | [Produkt](retail-hierarchies.md) | |
| Bundter | Markedsføringschefer kan gruppere produkter, så de sælges som et bundt eller en pakke. | [Pakker](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Infokoder | Brug infokoder til at bede kassereren om at angive oplysninger under forskellige handlinger på POS, f.eks. varesalg, varereturnering eller kundevalg. | [Infokoder](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Tilknyttede varer | Brug tilknyttede varer til mersalg, når en vare føjes til transaktionen. | [Tilknyttede varer](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Garantier | Udvidede garantier kan sælges sammen med produkter. | [Garanti](extended-warranty.md) | |
| Labeludskrivning | Labels kan genereres med produktoplysninger som batchnummer, serienummer og udløbsdato. | [Labeludskrivning](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Salgsassistance

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Produktgennemgang | Gennemse produkter efter kategori. | [Produkthierarki](retail-hierarchies.md) | |
| Produktsøgning | Søg efter produkter efter navn, og forfin søgninger ved hjælp af produktattributter som f.eks. mærke, pris og materiale. Denne egenskab drives af Azure Cognitive Search. | [Skybaseret søgning](cloud-powered-search-overview.md) | |
| Siden Produktdetaljer | Sider med detaljerede produktoplysninger kan indeholde billeder, en beskrivelse, produktattributter og anbefalede produkter. Anbefalinger leveres af anbefalingstjenesten. | | |
| Sammenlign produkter | Sammenlign flere produkter, og hjælp kunderne med at vælge en vare og føje den til en transaktion. | | |
| Uendelig gang | Du kan nemt søge efter lager i andre butikker og oprette ordrer. | [Lagersøgning](pos-inventory-lookup-operation.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Anbefalinger | Mersalg og krydssalg af produkter ved hjælp af anbefalingstjenesten. Denne tjeneste anvender patenteret teknologi til at foreslå anbefalinger baseret på indkøbstendenser og karakteristika som nyankomne, lignende udseende og mest solgte. Disse anbefalinger er tilgængelige på sider med produktoplysninger, siden **Kundeoplysninger** og siden **Transaktioner**. | [Anbefalinger](product-recommendations.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Kunderelation

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Kundestyring | Opret, rediger og administrer kundekonti. Kundekonti kan administreres i asynkron tilstand for at undgå behandling i realtid. | [Administration](customer-mgmt-stores.md) | |
| Kundeattributter | Du kan bruge struktur for kundeattributter til at registrere flere kunderelaterede data på basis af forretningsbehov. | [Attributter](dev-itpro/customer-attributes.md) | |
| Siden med kundeoplysninger | En side med detaljerede kundeoplysninger indeholder en omnikanalvisning af kundens interaktioner på tværs af alle kanaler. Disse interaktioner omfatter indkøb, ønskelister og fordelskundepoint. | | |
| Oversigt over skybaseret kundesøgning | Søg efter kunder ud fra navn, telefonnummer, mailadresse, fordelskundekort, adresse osv. | [Skybaseret søgning](pos-search-improvements.md#customer-search) | |
| Fordelskunde og belønninger | Kunder kan deltage i fordelskundeprogrammer og optjene og indløse fordelskundepoint på tværs af kanaler. | [Fordel](set-up-customer-loyalty-program.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| Kundeaktiviteter | Administrer nøglekunder ved hjælp af en klientbog, og spor aktiviteter og noter i kundeprofilen. Dynamics 365 Customer Insights-integration gør det muligt for butiksmedarbejderne at få tip til den næste egnede handling for hver kunde. | [Kundeaktiviteter](clienteling-overview.md#activities-and-notes) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>Priser og rabatter

| Egenskab | Beskrivende tekst | Dokumentation | Supplerende indhold |
|---|---|---|---|
| Handelsaftaler | Prischefer kan bruge samhandelsaftaler til at definere særlige priser baseret på langfristede aftaler for specifikke kunder. | [Prissætning](price-management.md)| [Video](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Salgsaftaler | Prissætningsansvarlige kan bruge salgsaftaler til at definere kontraktbaserede priser i B2B-handelsscenarier (Business-to-Business). | [Prissætning](price-management.md) | |
| Prisjusteringer | Prissætningsansvarlige kan bruge prisregulering til at oprette, spore og administrere prisreduktioner for produkterne over tid. | [Prisjusteringer](price-adjustments-discounts.md) | |
| Rabatter | Prissætningsansvarlige kan konfigurere flere rabattyper for at køre forskellige kampagner. Disse rabatter omfatter simple rabatter, antalsrabatter, grænserabatter, miks- og matchrabatter, tilbudsbaserede rabatter og forsendelsesrabatter. | [Rabatter](retail-discounts-overview.md) | |
| Kuponer | Prissætningsansvarlige kan konfigurere kuponkoder eller stregkoder, knytte dem til rabatter og fordele dem til kunder. Salgsmedarbejdere kan føje kuponer til salgstransaktioner eller fjerne dem. | [Kuponer](coupons.md) | |
| Prisgrupper | Prissætningsansvarlige kan bruge prisgruppefunktionaliteten til at definere kontekstafhængige priser baseret på kanaler, kataloger, tilknytninger eller fordelskundeprogrammer. | [Prissætning](price-management.md) | |
| Tilgængelige opprioriteringer | Salgsmedarbejdere kan nemt slå tilgængelige kampagner for produkter op i butikken, produkter, der er føjet til en transaktion, osv. | [Prissætningsfunktioner](pos-pricing-functions.md) | |
| Pristjek | Salgsmedarbejdere kan hurtigt kontrollere aktive salgspriser på produkter i butikken. | [Prissætningsfunktioner](pos-pricing-functions.md) | |
| Prisændringer | Salgsmedarbejdere, der har de nødvendige tilladelser, kan tilsidesætte systemkonfigurerede eller beregnede priser. | [Prissætningsfunktioner](pos-pricing-functions.md) | |
| Manuelle rabatter | Salgsmedarbejdere, der har de nødvendige tilladelser, kan anvende manuelle rabatter på salgstransaktioner eller salgslinjer. | [Prissætningsfunktioner](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektroniske betalinger

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Kredit og debet | Store Commerce-appen understøtter større betalinger med kredit- og debetkort via Adyen-betalingsgateway og ordreopfyldelse via PayPal. Betalings-SDK giver mulighed for eksterne gateway-forbindelser, der understøttes af uafhængig softwareleverandørers integrationer. | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[Betalinger](payment-methods.md)</p> | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Understøttelse af digital tegnebog | Store Commerce-appen understøtter betalinger via digitale betalingsmåder, hvor der ikke bruges BIN-intervaller (Bank Identification Number), som de traditionelle kredit- og debetkort gør. Betalingsmåder kan knyttes til digitale betalingsmåder, som f.eks. Adyen. | [Tegnebog](wallets.md) | |
| Understøttelse af gavekort | bankens identifikationsnummer Dynamics 365-gavekort, gemte værdiløsninger (SVS) og Givex-gavekort. Gavekort kan købes og indløses i en ordre. | [Gavekort](dev-itpro/gift-card.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Beskyttelse mod svindel | Dynamics 365 Fraud Protection hjælper dig med at forhindre svindelaktivitet og identificere steder, hvor svindel måske kan opdages. | [Fraud Protection](dev-itpro/dfp.md) | [Video](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Moms og gebyrer

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Moms | Store Commerce-appen understøtter mange typer af indirekte skatter, som f.eks. moms, moms af varer og ydelser (GST), stykbaseret gebyrer og A-skat. | [Moms](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Gebyrer | Gebyrer kan konfigureres på linjeniveau, på overskriftsniveau, som auto-gebyrer, efter kanal osv. | [Tillæg](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Ordrebehandling og -opfyldelse

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Ordreoprettelse | Der kan oprettes en ordre til forsendelse eller afhentning i en nærliggende butik. Der kan leveres tidsintervaller for afhentning. | [Overblik](customer-orders-overview.md) | |
| Ordreændring | En ordre kan redigeres, returneres, annulleres osv. | <p>[Annuller](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Returvarer](pos-returns.md)</p> | |
| Søge | Søg efter og filtrer ordrer ved hjælp af ordrespecifikke oplysninger. | [Søge](enhancedorderrecall.md) | |
| Ordreattributter | Du kan bruge struktur for ordreattributter til at registrere flere ordrerelaterede data på basis af forretningsbehov. | [Attributter](dev-itpro/order-attributes.md) | |
| Direkte levering | Varer kan markeres til direkte levering af en leverandør til en kundes adresse. Direkte levering kaldes også "drop shipping". | [Direkte levering](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Tilbud | Butiksmedarbejdere kan oprette tilbud til kunder og kan angive en særlig pris, manuel rabat og en gyldighedsdato for tilbuddet. | [Tilbud](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Opfyldelse | Butikker kan plukke, pakke og afsende ordrer. En følgeseddel kan føjes til de pakker, der er klar til forsendelse. | [Opfyldelse](order-fulfillment-overview.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[Video](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| Fordelt ordrestyring | Store Commerce-appen understøtter optimering af intelligent ordreopfyldelse, hvor forretningsstrategier kan konfigureres ud fra arten af virksomheden, typen af kunde, oprindelsen til en ordre og leveringsmetoden for en ordre. | [DOM](dom.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>Lagerstyring

| Egenskab | Beskrivende tekst | Dokumentation | Supplerende indhold |
|---|---|---|---|
| Bestilling efter ordre | Strømlin distributionen af disponibel lagerbeholdning fra et distributionscenter til flere butikker eller lagersteder. | [Bestilling efter ordre](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Cross-docking | Strømlin distributionen af lager på indgående indkøbsordrer til flere butikker eller lagersteder. | [Direkte levering](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Indgående lager | Modtag lager fra en leverandør via en indkøbsordre eller fra et andet lagersted via en flytteordre. Opret en indgående indkøbsordre eller flytteordreanmodning. | [Indgående](pos-inbound-inventory-operation.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Udgående lager | Afsend lager til et andet lagersted via en flytteordre, og opret en anmodning om udgående flytteordre. | [Udgående](pos-outbound-inventory-operation.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Lagersøgning | Kontrollér den disponible lagerbeholdning for produkter på tværs af butikker og lagersteder, og kontrollér DTT-lageret (disponibel til tilsagn) på fremtidige datoer. | [Lagersøgning](pos-inventory-lookup-operation.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Lagerregulering | Juster lagerbeholdningen til eller fra et butikslagersted for at opfylde bestemte forretningsbehov uden at bruge et salg, en tilgang eller en genoptælling. | [Lagerregulering](work-with-store-inventory.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Lagerstatus | Optæl det fysiske lager, og juster systembogføringslager, så det svarer til det. | [Tælling](work-with-store-inventory.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| Lagerbevægelse | Flytte lager mellem lokationer i en butik. | [Bevægelse](work-with-store-inventory.md) | <p>[Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>Finans

| Egenskab | Beskrivende tekst | Dokumentation | Supplerende indhold |
|---|---|---|---|
| Likviditetsstyring | Store Commerce-appen understøtter håndtering af kontanter og andre angivne tilbud i butikken. Desuden kan afstemning af skift i butikken aktiveres for avancerede funktioner til kontantstyring. | [Indløsning](cash-mgmt.md) | |
| Regnskaber og afstemninger | Kontant- og transaktionstransaktioner for en butik registreres i Commerce headquarters via bogføringsprocesserne for opgørelser. | [Opgørelser](retail-statements.md) | |
| Indtægts- og udgiftstransaktioner | Du kan behandle kontantbeholdningsposteringer i butikken og registrere indtægter, der ikke kommer på den traditionelle måde, f.eks. tabte og fundne penge, andelen af omsætningen fra en café i din forretning og tæpperens. | [Opgørelser](retail-statements.md) | |
| Fakturabetalinger | Indlæs betalinger på fakturaer. | [Fakturaer](payinvoice.md) | |

## <a name="employee-productivity"></a>Medarbejderproduktivitet

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Opgavestyring | Opret opgavelister og -opgaver, og tildel dem til butikker og medarbejdere. Spor status for opgaver på tværs af butikker. Der findes problemfri integration med Microsoft Teams. | <p>[Opgavestyring](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Video](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Hardware og ydre enheder

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Tilslutte eksterne enheder | Tilslut eksterne enheder som printere, pengeskuffer, scannere og betalingsenheder på en POS-terminal. | [Eksterne enheder](retail-peripherals-overview.md) ||
| Dele eksterne enheder | Kvitteringsprintere, pengeskuffer og betalingsenheder kan deles mellem mange terminaler ved at forbinde dem til en delt hardwarestation. | <p>[Hardwarestation](retail-peripherals-overview.md) ||
| POS og ekstern simulator | Den eksterne simulator understøtter test af scenarier, der normalt kræver fysiske ydre POS-enheder. Den indeholder også en POS-simulator, der giver mulighed for at teste kompatibiliteten af fysiske eksterne enheder, uden at du er nødt til at installere POS-klienten. | [Simulator](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Modtagelser

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Udskrive kvitteringer | Kvitteringer af forskellige typer, f.eks. salgskvittering, kreditkortkvittering, gavekortskvittering og fakturaer, kan udskrives som standard eller efter kassererbekræftelse ved kassen. De kan også udskrives fra kladden igen. | [Udskriver](receipt-templates-printing.md) | |
| E-mailkvitteringer | Kvitteringer kan sendes via mail fra POS, når betaling ved kassen er gennemført. | [E-mail](email-receipts.md) | |
| Designe kvitteringer | Butikskvitteringer kan tilpasses, så de viser data og layout, der er relevante for detail- og transaktionstypen. Kvitteringer kan også udvides, så de viser brugerdefinerede data, der kræves af forhandleren. | [Design](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Understøtte offline

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Uden problemer offline | Problemfri offline giver dig mulighed for at fortsætte med at handle, også selvom internetforbindelser er begrænsede eller ikke tilgængelige. Du kan bruge dataekskludering til at reducere datastørrelsen for offlinedatabaser og maksimere ydeevnen. | [Offline](pos-operations.md) | |
| Ydeevnebaseret skift | Skift til offline, når fald i ydeevnen registreres. | [Offline](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI) |
| Offline-dashboard | Dashboardet for **Offlinestatus** viser offlinestatus, fejl og detaljer om dataene for hver enhed. Derfor er det nemt at administrere status for mange enheder. | [Offline](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Udvidelsesmuligheder

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Commerce Headquarters | Løsningerne i Commerce headquarters kan tilpasses ved at tilføje eller redigere forretningsprocesser. Commerce headquarters understøtter brugen af metadata og en kodebaseret udvidelsesmodel for at tilføje brugerdefinerede funktioner. Den kan nemt integreres i eksterne løsninger. | [Overblik](dev-itpro/extend-customer-cdx-package.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Konsolløs handel | API-strukturen til den udvidelige omnikanal kan bruges til at tilpasse og tilføje forretningslogik. API'er, der har anmodningshandlere, og udvidelsesmønstre både før og efter udløser. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | Commerce SDK indeholder kode, kodeeksempler, skabeloner og værktøjer, som skal bruges til udvidelse eller tilpasning af Dynamics 365 Commerce-funktioner. SDK publiceres på forskellige lagre (repos) i GitHub, afhængigt af udvidelseskomponenterne. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| POS | Store Commerce-appen kan udvides uafhængigt ved hjælp af POS-udvidelsesfunktionen i Commerce SDK. Strukturen understøtter tilpasning af brugeroplevelsen, arbejdsgange og forretningslogik. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [Teknisk gennemgang](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Rapportering

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Salgsrapporter | Salgsrapporter efter medarbejder, kasseapparat, betalingstype, returneringer, produkt osv. er tilgængelige for butikschefer. Cheferne kan se disse rapporter og bruge dem til at fordele provision og identificere produkttendenser. | | |

## <a name="diagnostics"></a>Diagnosticering

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Operational Insights | Oplysninger om pålidelighed og ydeevne af butiksservice er tilgængelige i kundens Application Insights-abonnement. Der er avancerede overvågnings- og varslingsfunktioner. | | |
| Tilstandskontrol | Tilgængeligheden af eksterne enheder, der er tilsluttet en POS, kan kontrolleres ved at køre tilstandskontrollen. Individuelle eksterne problemer kan derefter rettes og kontrolleres. | [Tilstandskontrol](pos-healthcheck.md) | [Video](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globalisering

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Understøttelse på flere markeder | Markedsspecifikke funktioner som regnskabsintegration, GST, avanceret fakturering og forudbetalinger understøttes som standard. Denne egenskab dækker adskillige markeder i Europa, Nord- og Sydamerika, Rusland, Asien, Saudi-Arabien osv. | [Globalisering](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Overholdelse af angivne standarder

| Egenskab | Beskrivende tekst | Dokument | Supplerende indhold |
|---|---|---|---|
| Microsoft-standarder | Store Commerce-appen opfylder Microsoft-standarder for sikkerhed, beskyttelse af personlige oplysninger, tilgængelighed, generel forordning om databeskyttelse (GDPR), EU-datagrænsen osv. | | |

