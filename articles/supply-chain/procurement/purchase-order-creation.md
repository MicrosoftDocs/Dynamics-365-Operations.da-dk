---
title: Opret indkøbsordrer
description: I denne artikel beskrives den proces og de indstillinger, der gælder, når du opretter en indkøbsordre manuelt.
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb703ff7419a59aa174e16d8d988a96814e4fec6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572667"
---
# <a name="create-purchase-orders"></a>Opret indkøbsordrer

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

I denne artikel beskrives den proces og de indstillinger, der gælder, når du opretter en indkøbsordre manuelt.

Når du opretter en indkøbsordre (IO), angives generelle oplysninger om hele ordren i indkøbsordrehovedet, og du tilføjer derefter en eller flere linjer i indkøbsordren. I denne artikel beskrives nogle af de oftest brugte indstillinger, der er tilgængelige.  

Du kan også oprette IO'er ved at kopiere linjer fra et andet PO-dokument eller en salgsordre. Gør du det, kan du ændre fortegnet på lageret, på samme måde som når du ændrer fortegnet på en faktura for at angive kredit.  

Selvom du kan manuelt oprette IO'er, oprettes de mere typisk fra andre processer. Ordrer kan oprettes automatisk på grundlag af andre dokumenter, som rekvisitioner. De kan også oprettes som en del af varedisponeringsprocessen via planlagte IO'er. Hvis du bruger købsaftaler, kan IO'er oprettes under handlingen **Aftræksordre**. Der er mere også avancerede metoder til automatisk oprettelse af en indkøbsordre. For eksempel kan ordrer oprettes, når du bruger direkte levering eller interne ordrekæder.

## <a name="creating-a-purchase-order-header"></a>Oprettelse af et indkøbsordrehoved
Når du opretter en ny indkøbsordre, åbnes en dialogboks, hvor du kan indtaste de mest almindelige oplysninger til hovedet på indkøbsordren. Når du klikker på **OK** for at lukke dialogboksen, oprettes ordren, og du kan derefter angive yderligere oplysninger i hovedet.  

Det første, du skal overveje, når du opretter en indkøbsordre, er ordretypen. Typen **Indkøbsordre** bruges oftest. Men hvis du har brug for en kreditfaktura, kan du bruge typen **Returneret ordre**.  

Du skal angive leverandøren i feltet **Kreditorkonto**. Du kan søge på kontoen eller kreditornavnet for dette felt. Hvis en leverandør leverer fra flere steder, men bruger en enkelt fakturakonto, kan du vælge fakturakontoen i feltet **Fakturakonto** og derefter bruge kontoen sammen med forskellige kreditorkonti. Hvis du skal oprette en indkøbsordre for produkter, der ikke bestilles flere gange, kan du bruge indstillingen **Engangsleverandør**. Denne indstilling opretter automatisk en ny kreditorkonto, der er markeret som engangskonto, for at understøtte en senere oprydningsproces for engangskonti i **Kreditor**-modulet. Når du vælger en kreditorkonto, arver mange felter i indkøbsordrehovedet standardværdier fra de oplysninger, der er tilknyttet kreditorkontoen. For eksempel kopieres de standardlokationen for levering og lagersted fra kreditoroplysningerne. Du kan dog tilsidesætte disse standardværdier, hvis købet skal sendes til et andet sted.  

Hvis leverandøren har angivet et referencenummer for ordren, kan du registrere oplysningerne i feltet **Leverandørreference**. For ordrer, der returneres, skal du angive en værdi i feltet **RMA** for at henvise til leverandørens tilladelse til at behandle returneringen.  

Hvis en købsaftale er tilknyttet ordren, skal du angive disse oplysninger i feltet **Købsaftale**.  

Indkøbsordrehovedet indeholder også oplysninger om gebyrer, der gælder for hele ordren i stedet for de enkelte linjer. Gebyrer kan føjes automatisk til ordren, hvis der er oprettet automatiske gebyrer for kreditoren eller kreditorens gebyrgruppe. Du kan også manuelt føje gebyrer til ordrehovedet ved at klikke på **Vedligehold gebyrer** i handlingsruden.

## <a name="adding-purchase-order-lines"></a>Tilføjelse af indkøbsordrelinjer
IO'er kan være for fysiske produkter eller ydelser. En indstilling i lagermodelgruppen bestemmer, om et bestemt varenummer gælder for et produkt eller en ydelse. Den vare, der er købt, angives normalt af et nummer. Men hvis ordren er på produkter eller ydelser, der forbruges direkte, du kan også angive varen ved hjælp af en indkøbskategori.  

IO-linjer indeholder mange felter, men mange af disse felter har en standardværdi eller en værdi, der er nedarvet fra ordrehovedet. Der er angivet ekstra felter, når du vælger et produkt eller en ydelse. Felterne, som oftest angives manuelt, omfatter felter for varenummer, antal og ønsket leveringsdato. Oplysninger om enhedspris og rabatter er også meget vigtigt, men værdierne i disse felter, bestemmes ofte af handelsaftaler eller købsaftaler.  

Når du vælger et produkt, kan du søge på hele eller en del af produktets navn i stedet for ved hjælp af varenummeret. Hvis produktet har flere varianter, som f.eks. forskellige størrelser, kan du se en oversigt over de tilgængelige varianter ved hjælp af funktionen **Tilføj linjer** eller ved hjælp af det opslag, der findes i feltet **Variantnummer**.  

Du skal ofte angive flere dimensioner for den vare, der er valgt på hver indkøbsordrelinje. Hvilke dimensioner der skal angives afhænger af de dimensionsgrupper, der er tildelt til den overordnede produktmasterdefinition. For eksempel skal du ofte angive et sted og lagersted for at angive den lokalitet, som produktet skal leveres til. Du kan identificere produktvarianter ved at angive et variantnummer eller ved at indtaste værdier for en eller flere produktdimensioner som f.eks. farve, størrelse, konfiguration eller typografi. Sporingsdimensioner, f.eks. batch og serienummer, gør det muligt entydigt at identificere hvert lagerparti. Når du har oprettet en ordre, kan du hente dimensionsværdier i ordren ved hjælp af handlingen **Registrering**. For eksempel har du bestilt et antal på fem styk af en vare. Senere kan du registrere, at tre af disse er sorte, og to af dem er blå. Denne metode er et alternativ til hentning af dimensionsoplysninger under modtagelsesregistreringen.  

Du kan kontrollere detaljerne for lagerposteringsstatussen for produkter på lager. For eksempel kan du kontrollere den disponible lagerbeholdning for nemmere at kunne lagerbeslutte, hvor meget der skal bestilles. Alternativt kan du kontrollere lagerstatus for et bestilt antal for at se, om registrering af indgående ankomst har fundet sted.  

En indkøbsordrelinje, der bruges til at returnere et produkt til leverandøren, har et negativt antal. Du kan vælge et bestemt parti, som skal returneres, ved hjælp af handlingen **Reservation**.  

Nogle gange kan du opdele det antal, du har bestilt, så forskellige dele af det leveres på forskellige datoer. Du kan konfigurere disse leverancer ved hjælp af handlingen **Leveranceplan**, som er tilgængelig i menuen **Indkøbsordrelinje** i visningen **Linjer**.  

Gebyrer kan føjes automatisk til indkøbsordrelinjer, hvis der er oprettet automatiske gebyrer for kreditoren eller kreditorgebyrgruppen og for varen eller varegebyrgruppen. Dog mere typisk tilføjes gebyrer manuelt på ordrelinjeniveau. Når du vil tilføje et gebyr, skal du åbne siden **Vedligehold gebyrer** ved hjælp af handlingen **Vedligehold gebyrer** i menuen **Finans** i visningen **Linjer**. Fordelen ved at tilføje gebyrer direkte på ordrelinjeniveau er, at gebyret kan tildeles som en lageromkostning. Du kan konfigurere gebyrkoder til kontoproduktomkostninger ved at bruge debetindstillingen **Vare**. Disse typer af gebyrer, der skal fordeles fra indkøbsordrehovedets linjer, før ordren kan bekræftes. For eksempel kan du fordele gebyrer, der er baseret på antallet på hver linje. Gebyrkategorien påvirker også, hvordan gebyrer efterkalkuleres. For eksempel angiver faste gebyrer et fast beløb, og procentbaserede gebyrer beregnes som en procentdel af nettobeløbet for ordrelinjen. IO'er kan tildeles til en belastning, og belastningen kan indeholde et overslag over de forventede udgifter til transportomkostningerne. Du kan tildele denne udgift fra belastningen tilbage til IO-linjerne.

## <a name="purchase-order-actions"></a>Indkøbsordrehandlinger
Når du har føjet hovedet og linjerne til indkøbsordren, skal du ofte udføre yderligere trin, før ordren er klar til at blive bekræftet. Da der findes så mange muligheder, kan det være nyttigt at bruge [Handlingssøgning](../../fin-and-ops/get-started/action-search.md) til at finde det relevante menupunkt.  

Du kan konfigurere produkter i ordren, så de får supplerende varer. Supplerende varer er varer, der skal eller kan købes sammen med andre produkter. Supplerende produkter kan tilføjes gratis, som ledsageprodukter, eller du vil muligvis kunne afgøre, om du vil føje til ordren eller ej. Når hver ordrelinje er tilføjet, kan du gennemse de supplerende varer. Dog vil det nok være mere praktisk at gennemgå og tilføje relevante supplerende varer til alle ordrelinjer ved hjælp af siden **Supplerende varer**, som du kan åbne fra handlingsruden.  

Rabatter føjes normalt til linjer, når de oprettes. Nogle rabatter gælder dog for hele ordren:

-   Handlingen **Slutrabat** beregner en slutrabatprocent, som anvendes på hele ordren. Du må ikke forveksle denne rabat med kasserabatprocenten. Kasserabatter anvendes, når fakturaen er betalt, og de afhænger af, om betalingen sker på en bestemt dato.
-   Hvis en samkøbsrabat gælder, skal du bruge handlingen **Samkøbsrabat** til at beregne og tildele den til ordren. Samkøbsrabatter er rabatter, der kan tilbydes, hvis en blanding af varer på ordren overstiger en fælles tærskel. Kun få virksomheder bruger denne type rabat.

Gebyrer, der har en gebyrkode, der bruger debettypen **Vare**, skal være tildelt til linjeniveauet, før ordren kan bekræftes. Det kan være praktisk at tildele disse gebyrer på ordrehovedniveau, så du kan angive det samlede gebyrbeløb. Men i dette tilfælde skal gebyret derefter fordeles på hver linje, før ordren kan bekræftes. Du kan bruge handlingen **Fordel gebyrer** til at opdele beløb fra de gebyrer, der er tildelt på hovedniveau, på ordrelinjerne. Gebyrer kan opdeles i henhold til nettobeløbet for hver linje i overensstemmelse med det antal, der er bestilt, eller jævnt fordelt på ordrelinjerne. Når du har fordelt gebyrer på linjerne, fjernes gebyret fra ordrehovedet.  

IO'er kan konfigureres til at kræve, at budgetmidler fordeles på ordren, før den kan behandles. I dette tilfælde kan du bruge handlingen **Budgetkontrol** til at fordele budgettet.  

Du skal muligvis forsinke fuldførelsen af en indkøbsordre. For eksempel kan du kræve yderligere oplysninger om produkter eller ydelser, eller du skal muligvis have tilladelse til forbruget. Der er flere måder at holde en ordre tilbage. For eksempel kan du vente med at bekræfte ordren. Hvis en arbejdsgang til ændringsstyring anvendes, skal du ikke sende ordren til godkendelse. Hvis du må blokere alle ordrer for en bestemt kreditor, kan du også markere kreditoren som **På hold**, for at der kan udføres behandling på kreditormasteren. Der findes også tilfælde, der kan forhindre, at ordren behandles. Behandling kan for eksempel være forhindret, hvis kreditmaksimum er overskredet, eller hvis de krævede budgetmidler ikke er tilgængelige.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oversigt over indkøbsordrer](purchase-order-overview.md)

[Godkendelse og bekræftelse af indkøbsordre](purchase-order-approval-confirmation.md)

[Produktkvittering sammenlignet med indkøbsordrer](product-receipt-against-purchase-orders.md)

[Oversigt over kreditorfakturaer](../../financials/accounts-payable/vendor-invoices-overview.md)



