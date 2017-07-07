---
title: "Cross-docking fra produktionsordrer til forsendelsesområder | Microsoft Docs"
description: "I dette emne beskrives, hvordan du administrerer cross-docking-processen på materiale, der færdigmeldes fra en produktionslinje til et forsendelsesområde."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 0b5541b6752da0c73e4309951ecabc0793f24289
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Cross-docking fra produktionsordrer til forsendelsesområder

I dette emne beskrives, hvordan du administrerer cross-docking-processen på materiale, der færdigmeldes fra en produktionslinje til et forsendelsesområde.

<a name="introduction"></a>Introduktion
------------

Direkte levering fra produktion til et forsendelsesområde er relevant for producenter, der producerer store mængder og ideelt ønsker at levere de færdige produkter, så snart de er færdigmeldt fra produktionslinjerne. Formålet er at levere produkterne til distributionscentre, der fysisk er placeret tæt på det sted, kunden efterspørger, i stedet for at opbygge et lager hos producenten.

Hvis der ikke er et umiddelbart behov for et produkt, skal det lægges på lager på lagerlokationer på produktionsstedet. Denne proces kaldes også *mulighed for cross-docking* og angiver, at hvis der er et behov for levering af produktet, skal denne mulighed bruges i stedet for at lægge produktet på lager til intern opbevaring.

I følgende eksempel vises tre varianter af en proces, der starter i slutningen af produktionslinjen (2).

Et produkt er færdigmeldt til produktionsforsendelsesstedet (3), og en truck afhenter pallen på dette sted (3).

-   Hvis der er en planlagt aktivitet (6) til flytning af produktet fra produktion (1) til et distributionscenter (7), angiver systemet, truckchaufføren skal sætte pallen ved en lagerport (4).
-   Hvis der allerede tildelt en trailer til lagerporten, anmodes chaufføren om at laste produktet direkte på traileren.
-   Hvis der ikke er nogen planlagt aktivitet til flytning af produktet, anmodes chaufføren om at lægge produktet på lager et sted på det interne lagersted (5).

[![](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Konfigurere cross-docking
Du konfigurerer cross-docking-processen i **arbejdspolitikker**. En arbejdspolitik omfatter en arbejdsordretype, sted og produkt. I følgende eksempel er cross-docking konfigureret for produkt X og sted Y.

#### <a name="work-order-types"></a>Arbejdsordretyper

-   Arbejdsordretype: Færdigvarer lagt på lager
-   Metode til oprettelse af arbejde: cross docking
-   Navn på politik for cross-docking: Flytteordrer

#### <a name="inventory-locations"></a>Lagerlokationer

-   Lagersted: 51
-   Adresse: Y

#### <a name="products"></a>Produkter

-   Varenummer: X

I øjeblikket kan cross-docking konfigureres til kun to arbejdsordretyper:

-   Færdige varer, læg på lager
-   Samprodukt og biprodukt, læg på lager

I **politik for cross-docking** definerer du, hvilke dokumenttyper der kan anvendes til cross-docking. Den eneste dokumenttype, der understøttes i øjeblikket, er **Flytteordrer**. I følgende eksempel vises konfigurationen af en politik for cross-docking.

### <a name="cross-docking-policy-name-transfer-order"></a>Navn på politik for cross-docking: Flytteordre

-   Løbenummer: 10
-   Arbejdsordretype: Flytteafgang
-   Cross-docking-behov kræver lokation: Falsk
-   Strategi for cross-docking: Dato og klokkeslæt

### <a name="sequence-number"></a>Løbenummer

**Løbenummer** angiver dokumenttypens prioritering. Den eneste dokumenttype, der understøttes i øjeblikket, er **Flytteafgang**. Løbenummeret er derfor kun relevant, når flere arbejdstyper understøttes.

### <a name="cross-docking-policy"></a>Politik for cross-docking

Politikken for cross-docking angiver også politikken for prioriteringen af flytteordrebehov. Hvis der findes flere flytteordrer for samme produkt, bestemmer den planlagte dato og klokkeslæt, der er angivet for belastningen, og som er knyttet til flytteordren, prioriteringen af ordrerne. Planlagt dato og klokkeslæt kan angives direkte på belastningen, eller det kan angives på en **aftaletidsplan**, der er tilknyttet belastningen. Prioriteringen bestemmes af den cross-docking-strategien. Der er i øjeblikket kun én strategi: **Dato og klokkeslæt**.

### <a name="cross-docking-demand-requires-location"></a>Cross-docking-behov kræver lokation

I politikken for cross-docking kan du angive et kriterium, så flytteordrer skal have tildelt en placering for at være berettiget til cross-docking. Dette kriterium angives i feltet **Cross-docking-behov kræver lokation**. Stedet i aftaletidsplanen, der er tilknyttet belastningen, bruges som den endelige placering for de varer, der afsendes direkte (cross-docked). Den endelige placering for de varer, der afsendes direkte, bestemmes af lokationsvejledningen for **Flytteafgang** for ordretypen **Læg på lager**. Du kan være nyttigt at angive feltet **Cross-docking-behov kræver lokation** i et scenarie, hvor færdigvarerne kun skal afsendes direkte, hvis der er tildelt en trailer til lagerporten. I dette scenarie flyttes varerne direkte fra produktionslinjen til traileren. Når en trailer er tildelt til lagerporten, tildeler en bruger placeringen til aftaletidsplanen, og lokationen bliver derfor gjort tilgængelig for cross-docking. I følgende afsnit gennemgås to eksempler.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Scenarie 1 – Cross-docking fra produktionsordrer til flytteordrer

Når et produkt er færdigmeldt på produktionslinjen, flyttes det til en lagerportplacering, hvor det lastes på en truck og overføres til et distributionscenter. Brug firma-USMF.

1.  Aktivér en ny nummerserie til cross-docking. Gå til siden **Nummerserier**, og vælg knappen **Generér**. En guide hjælper dig gennem processen.
2.  Opret en politik for cross-docking. Gå til siden **Politik for cross-docking**, og opret en ny politik med navnet **Cross-docking til flytteordre**. Bemærk, at den eneste arbejdsordretype, som du kan vælge, er **Flytteafgang**, og den eneste tilgængelige cross-docking-strategi er **Dato og klokkeslæt**.
3.  Opret en arbejdspolitik. Gå til siden **Arbejdspolitikker**, og opret en ny arbejdspolitik med navnet **Direkte levering L0101**.
4.  Konfigurer belastninger, så de oprettes automatisk for flytteordrer. Konfigurer belastninger i lagerstedsparametre, så de oprettes automatisk, når der oprettes flytteordrer. En belastning er en forudsætning for at gøre flytteordren berettiget til cross-docking.
5.  Konfigurer tilknytningen af varelast. Gå til siden **Tilknytning af varelast**, og opret en standardbelastningsskabelon for varegruppen **CarAudio**. Denne tilknytning indsætter automatisk belastningsskabelonen på belastningen, når flytteordren er oprettet.
6.  Opret en flytteordre. Opret flytteordre for varenummer L0101. Antal = 20.
7.  Frigiv flytteordren fra lastplanlægningspanelet. Under fanen **Send** skal du vælge menupunktet for lastplanlægningspanelet, og i menuen **Frigiv** på belastningslinjen skal du vælge **Frigiv til lagersted**. Der findes nu en åben bølgelinje af typen **Flytteafgang** for flytteordren.
8.  Opret en produktionsordre. Gå til listesiden **Produktionsordren**, og opret en produktionsordre for produktet L0101. Antal = 20. Estimer og start produktionsordren. Bemærk, at feltet **Bogfør plukliste nu** forbliver indstillet til **Nej**.
9.  Færdigmeld fra mobilenheden. Gå til mobilenhedsportalen, og vælg menupunktet **Færdigmeld, og læg på lager**. Færdigmeld nu L0101 fra den håndholdte enhed. Bemærk, at læg på lager-lokationen er **BAYDOOR**. Denne placering findes i lokationsvejledningen **Flytteafgang** for arbejdsordretypen **Læg på lager**. Bemærk også arbejde af typen **Flytteafgang** er oprettet og fuldført. Gå til flytteordrens arbejdsdetaljer for at kontrollere arbejdet.
10. Prøv nu at starte 20 styk yderligere på produktionsordren, og prøv derefter at færdigmelde 20 styk ved hjælp af den håndholdte enhed. Denne gang foreslås **LP-001** som læg på lager-sted. Denne placering kan findes i lokationsvejledningen for **Færdige varer, læg på lager**. Lokationsvejledningen bruges, fordi der ikke findes nogen mulighed for salgsmulighed. Flytteordren for LP-001 blev fuldstændig opfyldt i den første cross-docking-aktivitet.

Arbejde af typen **Færdige varer, læg på lager** blev oprettet og behandlet.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Scenarie 2 - Cross-docking fra produktion til at flytteordrer med en aftaletidsplan

Når et produkt er færdigmeldt på produktionslinjen, overføres det til en lagerportplacering, der identificeres af en aftaletidsplan for lagerportplaceringerne. Brug firma-USMF.

1.  Skift politik for cross-docking. Rediger den politik for cross-docking, du oprettede i scenarie 1, ved at markere afkrydsningsfeltet **Cross-docking-behov kræver lokation**.
2.  Opret en ny flytteordre.
3.  Åbn **Panelet Lastplanlægning**.
4.  Fra panelet Lastplanlægning skal du gå til afsnittet **Laster** og vælge **Aftaletidsplan** i menuen **Transport** for at oprette en ny aftaletidsplan. Bemærk, at aftaletidsplanen har en henvisning til flytteordren i feltet **Ordrenummer**. I feltet **Planlagt startdato/-klokkeslæt på lokationen** kan du angive dato og klokkeslæt for aftalen. Datoen og klokkeslættet bliver brugt, når cross-docking-behovet prioriteres under cross-docking-processen. Den dato og det klokkeslæt, du angiver i dette felt, opdaterer feltet **Dato og klokkeslæt for den planlagte forsendelse af lasten** på den tilsvarende belastning. Lokationen i oversigtspanelet **Forsendelsesdetaljer** bestemmer, hvilket sted flytteordren leveres på.
5.  På **Panelet Lastplanlægning** frigivelse til lagerstedet.
6.  Opret en produktionsordre for varenummer **L0101**, og indstil status til **Startet** med et antal på 20.
7.  Færdigmeld fra mobilenheden.
8.  Gå til mobilenhedsportalen, og vælg menupunktet **Færdigmeld, og læg på lager**.
9.  Færdigmeld varenummer **L0101** fra den håndholdte enhed. Bemærk, at læg på lager-lokationen nu er **BAYDOOR 2**. Denne placering findes i aftaletidsplanen i stedet for i lokationsvejledningen **Tilgang for overførsel**.

### <a name="additional-information"></a>Yderligere oplysninger

-   Cross-docking-scenariet understøttes for batch- og seriekontrollerede varer, begge med de batch- og serienummerdimensioner, der er defineret over og under placeringen i reservationshierarkiet.
-   Det antal, der færdigmeldes, kan ikke opdeles for et flytteordrebehov, der er lavere. Eksempelvis hvis 20 styk færdigmeldes, og der findes en flytteordre for 5 styk, og bliver flytteordren ikke taget i betragtning til cross-docking.



