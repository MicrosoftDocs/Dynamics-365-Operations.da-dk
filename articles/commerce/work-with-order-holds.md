---
title: Konfigurere og arbejde med callcenterordrer på hold
description: I dette emne beskrives, hvordan du kan arbejde med ordrer på hold ved hjælp af Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans, MCROrderEventSetup, MCROrderEventTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b11dd48ac629910a82b4d5bfdf9889809b0d829d
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830117"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Konfigurere og arbejde med callcenter-ordrer på hold

[!include [banner](includes/banner.md)]

I dette emne beskrives de funktioner for ordrer på hold, som findes til callcenterordrer i Dynamics 365 Commerce.

## <a name="configuring-call-center-order-holds"></a>Konfigurere callcenterordrer på hold

Når du vil bruge funktionerne til callcenterordrer på hold, skal du først definere koder for ordrer på hold. Du kan oprette et sæt brugerdefinerede koder for ordrer på hold baseret på dine forretningsbehov ved at gå til **Salg og marketing** \> **Opsætning** \> **Salgsordrer** \> **Koder for ordrehold**. Du kan vælge at markere en af holdkoderne som standardholdkoden ved at vælge **Ja** i indstillingen **Standard for salgsordre** for den. Denne holdkode bliver brugt, hver gang en salgsordre sættes på hold. Hvis en salgsordre har reserveret lager, og reservationerne skal fjernes automatisk, hvis ordren er sat på hold af en bestemt årsag, skal du vælge **Ja** i indstillingen **Fjern lagerreservationer** for årsagskoderne.

Du kan angive typen af note, der hentes, når brugere, der sætter en salgsordre på hold, angiver valgfri noter, ved at gå til **Debitor** \> **Opsætning** \> **Debitorparametre** og derefter klikke på feltet **Notattype** under fanen **Generelt** i oversigtspanelet **Salgsopsætning**. Brug feltet **Salgsordrestatussen På hold** til at definere den farve, der skal bruges til at fremhæve salgsordrer, der er på hold, når de vises på siden **Kundeservice**.

Hvis du vil oprette et valgfrit sæt holdårsagskoder, skal du gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **Infokoder**. Disse infokoder kan bruges som sekundær årsagskode for at definere den primære holdkode yderligere. Vælg **Ny** for at oprette en årsagskode, og vælg derefter **Underordnede koder** for at definere listen over yderligere årsager. Hvis du vil sammenkæde infokoder, som du definerer til callcenterkanalen, skal du gå til **Retail og Commerce** \> **Kanaler** \> **Callcentre** \> **Alle callcentre**. Indstil feltet **Holdkode** i oversigtspanelet **Generelt**.

## <a name="putting-orders-on-hold"></a>Sætte ordrer på hold

Ordrer, som callcenterbrugere opretter i administrationsdelen af Commerce-programmet, kan sættes på hold manuelt eller automatisk i bestemte situationer.

Under ordreindtastningen, men før afsendelse og bekræftelse af ordren, vil callcenterbrugere måske sætte en ordre på hold manuelt for at forhindre, at den frigives til lageret til yderligere behandling. Den kunde, der afgiver ordren, er f.eks. muligvis ikke helt klar til at foretage bestillingen, eller måske mangler der kritiske data, der kræves for at behandle ordren.

På ordreindtastningssiden kan callcenterbrugeren sætte en ordre på hold ved hjælp af indstillingden **Ordrer på hold** under fanen **Salgsordre** i ordreindtastningsmenuen. Brugeren kan også vælge menupunktet **Hold** på siden **Salgsordreoversigt**, der vises, når han eller hun vælger **Fuldført** i en callcentersalgsordre.

I begge tilfælde vises siden **Ordrer på hold**. Brugeren kan derefter vælge **Ny** for at oprette en spærring for ordren. I feltet **Holdkode** skal brugeren vælge den kode, der bedst beskriver årsagen til spærringen. I feltet **Årsagskode** kan brugeren eventuelt vælge en tillægskode for at angive endnu en beskrivelse af spærringen.

I oversigtspanelet **Noter** i feltet **Holdnoter** kan brugeren angive yderligere, fritformulerede noter med yderligere kontekst eller oplysninger om spærringen. Disse noter kan hjælpe andre brugere, der senere gennemser eller arbejder med ordren på hold.

Når holdoplysningerne er angivet og gemt, kan brugeren lukke siden **Ordrer på hold**. Brugeren returneres derefter til salgsordreindtastningssiden. Hvis der ikke kræves yderligere handlinger på salgsordren, kan brugeren lukke salgsordreindtastningssiden.

Hvis flaget **Aktivér ordrefuldførelse** er aktiveret i callcenterkanalen, skal betaling ikke nødvendigvis anvendes på en ordre, der er sat på hold. Ved en salgsordre, der ikke er sat på hold, kan brugerne derimod ikke forlade indtastningssiden, før betalingen er foretaget. Betalingen skal naturligvis foretages, før spærringen af ordren ophæves.

Desuden kan callcenterbrugere sætte manuel svindelhold på ordrer, der af en eller anden grund er mistænkelige. Ordrer kan også sættes på hold automatisk, når de matcher aktive svindelkriterier og -regler. Du kan finde flere oplysninger om denne type ordrehold i [Konfigurere advarsler om svindel](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Visning og styring af ordrer, der er sat på hold

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Vise oplysninger om hold for en enkelt salgsordre

På siden **Kundeservice** kan brugerne visuelt identificere ordrer, der er på hold, fordi ordrelinjerne er markeret med en bestemt farve. Denne farve er defineret af feltet **Salgsordrestatussen På hold** på siden **Debitorparametre**.

> [!NOTE]
> Hvis linjen er markeret på siden, markeringsfarven ikke synlig.

Brugerne kan også få vist detaljerede statusoplysninger for en salgsordre for at få at vide, om ordren er på hold. Du kan få adgang til de detaljerede statusoplysninger fra siden **Alle salgsordrer** eller **Kundeservice**. Hvis en ordre er på hold, er flaget **Udfør ikke behandling** indstillet for den, og **Detaljeret status**-feltet viser status som enten **På hold** eller **Svindelhold**, afhængigt af scenariet.

For at få vist detaljerne for individuelle ordrehold kan brugerne åbne en detaljeret visning af siden **Ordrehold** fra siden **Kundeservice** ved hjælp af menuen **Indstillinger** for den valgte ordre. Brugerne kan også få adgang til denne visning fra siden **Alle salgsordrer** ved at vælge menupunktet **Ordrer på hold** under fanen **Salgsordre**.

### <a name="viewing-all-orders-that-are-on-hold"></a>Visning af alle ordrer, der er sat på hold

For at få vist alle ordrer, der er blevet sat på hold manuelt eller automatisk, kan du gå til **Retail og Commerce** \> **Kunder** \> **Ordrer på hold**.

Panelet **Odrer på hold** indeholder en listevisning af alle ordrer, der er sat på hold på grund af manuelle eller svindelrelaterede holdhandlinger. Ved at udnytte standardfiltrerings- og sorteringsindstillingerne på siden, kan brugerne oprette visninger, hvor de kan arbejde med eller håndtere bestemte holdkoder, som de er ansvarlige for at gennemgå. Panelet **Ordrer på hold** angiver også antallet af dage, en ordre har været på hold. Disse oplysninger kan hjælpe brugerne med at prioritere køen.

Hvis du vil have en mere detaljeret oversigt over de ordrer, der er på hold, kan du klikke på **Ordrer på hold** i menuen. Denne visning indeholder oplysninger om kunden, eventuelle noter, der er anvendt på ordre-, kunde- eller holdhandlingen. Visningen indeholder også oplysninger om årsagen til automatisk spærring, hvis ordren blev sat på hold, fordi den svarede til en svindelregel.

Fra både listevisningen og den detaljerede visning af siden **Ordrer på hold** kan brugerne få vist eller rediger yderligere ordrerelaterede oplysninger, f.eks. betalinger, totaler og noter.

Indstillingerne under fanen **Hold på udtjekning** kan være nyttige, hvis flere brugere i virksomheden arbejder på holdkøen på samme tid. Ved at vælge indstillingen **Check ud** kan brugerne angive, at de arbejder med at gennemse og undersøge ordrespærringen. På denne måde spilder andre brugere ikke tiden ved at forsøge at udføre det samme arbejde. Fra den detaljerede visning af siden **Ordrer på hold** kan brugere få vist oplysninger om datoen og klokkeslæt for udtjekning og den bruger, der er tjekkede holdposten ud.

Når en holdpost er tjekket ud, er det kun den bruger, der tjekkede den ud, der kan fjerne udtjekningen. Denne begrænsning er beregnet til at forhindre brugere i at tage poster, som andre brugere allerede arbejder på. For at frigive en ordre tilbage i køen, så andre brugere kan arbejde på den, skal den bruger, der tjekkede posten ud, vælge indstillingen **Ryd udtjekning**.

> [!NOTE]
> Spærringen ophæves ikke, når udtjekningen fjernes.

I nogle situationer, f.eks. når en bruger er syg eller har forladt virksomheden, kan poster, der er tjekket ud til den pågældende bruger, tildeles til en anden bruger. En leder kan tildele poster igen ved hjælp af indstillingen **Tilsidesæt udtjekning**.

## <a name="releasing-orders-that-are-on-hold"></a>Frigive ordrer, der er sat på hold

I både listevisningen og den detaljerede visning af siden **Ordrer på hold** indeholder fanen **Ryd på hold** indstillinger, der bruges til at frigive en ordre på hold. Brug indstillingen **Ryd På hold** for at frigive en ordre fra den valgte holdkode.

Callcenterordrer kræver betaling. Derfor kan et hold ikke fjernes helt, hvis betalingen ikke er anvendt på ordren. På siden **Call center-parametre** skal du kontrollere, at parameteren **Send efter rydning** under fanen **Spærringer** er aktiveret. Med denne indstilling kan du sikre, at en ryddet ordre på hold gennemgår den korrekte ordreindgivelseslogik til validering og godkendelse af betalinger. Hvis der mangler betalinger, får brugeren en fejlmeddelelse, og holdkoden ryddes ikke.

Hvis parameteren **Send efter rydning** ikke er angivet, skal brugerne vælge indstillingen **Ryd og send** i menuen **Ryd på hold** for at sikre, at ordren gennemgår alle påkrævede betalingsvalideringer. Hvis ordreafgivelsen mislykkes, når flaget **Aktivér ordrefuldførelse** flag er aktiveret i callcenterkanalen, frigives ordren fra sin holdstatus, men **Udfør ikke behandling**-flaget bliver ikke fjernet. Ordren bliver derfor ikke frigivet til lageret, før de korrekte betalinger er blevet anvendt og valideret.

Hvis brugeren vil fjerne en spærring, men foretage flere ændringer af ordren, før den frigives til yderligere behandling, kan han eller hun vælge indstillingen **Ryd og rediger**. Denne indstilling fjerner holdkoden og åbner oplysningerne om salgsordren, så brugerne kan foretage yderligere ændringer i ordren. Brugerne kan også anvende betaling og sende salgsordren via betalingsvalideringslogik, når flaget **Aktivér ordrefuldførelse** er aktiveret i callcenterkanalen.

## <a name="reporting-options"></a>Rapporteringsindstillinger

Gå til **Retail og Commerce** \> **Forespørgsler og rapporter** \> **Call center-rapporter** \> **Rapport over ordrer på hold** for at køre en rapport om ordrehold efter datointerval, holdkode eller andre relaterede kriterier.
