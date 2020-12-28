---
title: Konfigurere callcenterets leveringsmåder og -gebyrer
description: I dette emne beskrives, hvordan du konfigurerer leveringsmåder og gebyrer for en callcenterordre i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9919e76b5e3eb1a43c5a0ecd5dda1462bedad4f2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410985"
---
# <a name="configure-call-center-delivery-modes-and-charges"></a>Konfigurere callcenterets leveringsmåder og -gebyrer

[!INCLUDE [banner](includes/banner.md)]

Når der afgives en salgsordre i Dynamics 365 Commerce, og den person, der afgav salgsordren, er tilknyttet en callcenterkanal, bruges logik og regler til at validere leveringsmåden og beregne gebyrer for ordren.

Når du opretter en salgsordre, kan du vælge en leveringsmåde i salgsordrehovedet og på salgsordrelinjerne. Som standard bruges den leveringsmåde, som du vælger i hovedet, til alle salgsordrelinjer. Du kan imidlertid tilsidesætte standardleveringsmåden for de enkelte salgslinjer efter behov. Du kan også definere en leveringsmåde i en kundepost. Når ordren er oprettet for kunden, bruges denne leveringsmåde som standard i salgsordrehovedet.

Commerce har funktioner, som brugerne kan bruge til at begrænse de leveringsmåder, der kan bruges af en kanal, de leveringsmåder, der kan bruges til et produkt, og de leveringsmåder, der gælder for bestemte forsendelsesdestinationer. Der kan også defineres gebyrer, så yderligere gebyrer kan føjes til en kundes ordre, afhængigt af hvilke leveringsmåder der er valgt for salgsordren, og ordrens samlede værdi.

## <a name="define-delivery-modes"></a>Definere leveringsmåder

Før du angiver, hvilke leveringsmåder der kan bruges til callcenterordrer, og definerer de tilknyttede regler og gebyrer, skal du definere leveringsmåderne. Gå til **Salg og marketing \> Konfiguration \> Distribution \> Leveringsmåder**. Vælg **Ny** for at oprette en ny leveringsmåde. Du kan også vælge en eksisterende leveringsmåde på listen og derefter vælge **Rediger** for at foretage ændringer.

I feltet **Leveringsmåde** kan du angive en kombination af alfanumeriske tegn baseret på dine forretningsbehov. Du kan derefter bruge feltet **Beskrivelse** til at levere yderligere kontekst. Felterne **Gebyrgruppe** og **Fremskynd** er valgfri og beskrives mere detaljeret senere i dette emne.

I oversigtspanelet **Commerce-kanaler** kan du tilføje de kanaler, der skal kunne bruge leveringsmåden, når der oprettes salgstransaktioner i denne kanal.

I oversigtspanelet **Produkter** kan du angive, hvilke produkter og/eller produktkategorier leveringsmåden kan bruges til, og hvilke den ikke kan bruges til. Hvis et produkt f.eks. ikke kan leveres med fly på grund af begrænsninger som følge af farlige materialer, skal du sørge for, at produktet eller produktkategorien er udelukket fra alle de leveringsmåder, der involverer transport med fly.

I oversigtspanelet **Adresser** kan du angive, hvilke lande eller områder leveringsmåden kan bruges til, og hvilke den ikke kan bruges til. For eksempel kan ordrer, der leveres til Hawaii eller Alaska, ikke leveres med vognmand. Disse stater skal derfor udelukkes fra leveringsmåder, der er knyttet til en vognmandstjeneste, men kan medtages i leveringsmåder, der er knyttet til flyleveringstjenester.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Validere leveringsmåder for en callcenterordre

Når leveringsmåderne er defineret, skal du køre batchjobbet **Behandling af leveringsmåder**. Dette job gør leveringsmåderne tilgængelige, så de kan bruges i salgsordreprocesser for kanaler. Du kan køre jobbet **Behandling af leveringsmåder** ved at gå til **Detail og Commerce \> Retail og Commerce IT \> Behandling af leveringsmåder**. Dette job skal køres, hver gang der føjes nye leveringsmåder til en kanal, eller der foretages ændringer af eksisterende relationer for leveringsmåde/kanal.

Når du har kørt batchjobbet **Behandling af leveringsmåder**, kan du gå til **Retail og Commerce \> Kanaler \> Call centre \> Alle call centre**. På siden **Alle call centre** skal du i handlingsruden under fanen **Konfigurer** vælge **Leveringsmåder**. På siden **Leveringsmåder** kan du se alle gyldige leveringsmåder for den valgte callcenterkanal. For at redigere eksisterende leveringsmåder eller tilføje nye leveringsmåder skal du vælge **Administrer leveringsmåder**. Bemærk, at jobbet **Behandling af leveringsmåder** skal køres, hver gang der foretages ændringer.

## <a name="define-charges-for-delivery-services"></a>Definere gebyrer for leveringen af varerne

Når der oprettes salgsordrer for kunder, kan et firma tilføje gebyrer, der beregnes automatisk baseret på de leveringsmåder, der er valgt for ordren. Disse gebyrer kan konfigureres, så de er ens for alle kunder og leveringsmåder. Gebyrerne kan også variere, afhængigt af kunden og/eller de leveringsmåder, der er valgt for salgsordren.

Du kan definere gebyrerne ved at gå til **Retail og Commerce \> Konfiguration af kanal \> Gebyrer \> Automatiske gebyrer**. Vælg **Ny** for at tilføje nye gebyrer. Du kan også vælge en eksisterende post og derefter vælge **Rediger**.

Gebyrer kan defineres, så de beregnes på niveauet for ordrehovedet eller ordrelinjerne. Brug feltet **Niveau** til at vælge det ønskede niveau.

Gebyrer kan defineres for en specifik kunde, en kundegruppe eller alle kunder. I feltet **Kontokode** skal du vælge **Tabel** for at definere gebyrer, der kun anvendes på en bestemt kunde. Vælg **Gruppe** for at definere gebyrer for en specifik kundegruppe. Vælg **Alle** for at anvende gebyrerne for hver kunde, der afgiver en salgsordre, der bruger den relaterede leveringsmåde. Hvis du har valgt **Tabel** eller **Gruppe** i feltet **Kontokode**, skal du vælge kunden eller kundegruppen i feltet **Kontorelation**.

Gebyrer kan konfigureres, så de anvendes til en bestemt leveringsmåde, en leveringsmådegruppe eller alle leveringsmåder. Hvis du vælger **Tabel** i feltet **Kode for leveringsmåde**, skal du vælge en bestemt leveringsmåde i feltet **Leveringsmåderelation** felt. Hvis du vælger **Gruppe**, skal du vælge en leveringsmådegruppe i feltet **Leveringsmåderelation**. Leveringmådegrupper defineres i **Retail og Commerce \> Konfiguration af kanal \> Gebyrer \> Leveringsgebyrgrupper**. De kan derefter knyttes til en eller flere leveringsmåder på siden **Leveringsmåder**. Hvis du vælger en gruppe, når du definerer gebyrer, bruger leveringsmåder, der er knyttet til den valgte leveringsgruppe, de pågældende gebyrer. Endelig, hvis du vælger **Alle** i feltet **Kode for leveringsmåde**, bruger alle leveringsmåder gebyrerne. Derfor skal du ikke vælge en værdi i feltet **Leveringsmåderelation**.

I sektionen **Linjer** kan du definere en eller flere gebyrer efter valuta, som du ønsker. Gebyrer skal knyttes til en gebyrkode, der definerer de økonomiske bogføringsregler for gebyret. Feltet **Kategori** bruges til at definere, hvordan gebyrer beregnes. Eksempelvis hvis debitorer skal faktureres et fast beløb på $9,95 for levering af en ordre med en bestemt leveringsmåde, skal du bruge kategorien **Fast**. Hvis virksomheden beslutter at debitere kunderne en procentdel af ordrens samlede værdi til dækning af leveringsgebyrer, skal du bruge kategorien **Procent**. Det faktiske kundegebyr, defineres i feltet **Gebyrværdi**.

Firmaer konfigurerer ofte lagdelte gebyrer. I så fald er det beløb, som kunderne betaler for levering, baseret på ordreværdien. Du kan konfigurere lagdelte gebyrer ved at angive værdier i felterne **Fra beløb** og **Til beløb** ud over at definere selve gebyret i feltet **Gebyrværdi**. Ved ordrer, der har en værdi på mindre end $50, trækker en forhandler f.eks. $5,95 ved levering med vognmand. Ved ordrer med en værdi, der er lig med eller større end $50, men mindre end $100, opkræver detailhandleren $7,95 i gebyr. Ved ordrer med en værdi, der er lig med eller større end $100, leverer detailhandleren uden at opkræve gebyr. I følgende illustration vises konfigurationen af disse gebyrer.

![Eksempel på faste lagdelte gebyrer](media/fixedtieredcharges.png)

Du kan bruge en blanding af kategorier for gebyrer, afhængigt af virksomhedens behov. Ved alle ordrer, der har en værdi på f.eks. mindre end $100, trækkes et fast gebyr på $9,95 for levering. Ved ordrer, der har en værdi, der er lig med eller større end $100, beregnes leveringsgebyrer på 5 procent af ordreværdien. I følgende illustration vises konfigurationen af disse gebyrer.

![Eksempel på blandede lagdelte gebyrer](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Anvende leveringsmåder under ordreindtastning i et callcenter

Når der oprettes en ny salgsordre, skal der angives en værdi i feltet **Leveringsmåde** i oversigtspanelet **Levering** i salgsordrehovedet. Dette felt kan blive udfyldt automatisk baseret på standardværdier i kundeposten.

Den leveringsmåde, der er defineret i ordrehovedet, kopieres automatisk til salgsordrelinjerne, efterhånden som de oprettes. Du kan dog ændre opsætningen af leveringsmåden for et bestemt linjeelement under fanen **Levering** i sektionen **Linjedetaljer** på siden for salgsordreindtastningen.

Hvis den valgte leveringsmåde ikke er gyldig for produktet eller den leveringsadresse, der er defineret for ordren eller ordrelinjen, vises der en fejlmeddelelse. Derefter skal du vælge en leveringsmåde, der er defineret til at understøtte den pågældende produkt- eller adressekonfiguration.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Beregning af leveringsgebyrer under ordreindtastning

Hvis indstillingen **Aktivér ordrefuldførelse** er slået til for din callcenterkanal, beregnes forsendelsesgebyrer automatisk for salgsordrer, når brugerne vælger **Fuldført**. Følgende meddelelse vises øverst på siden **Salgsordreoversigt**: "Lagdelte gebyrer er beregnet". De gebyrer, der er beregnet, føjes til værdien i feltet **Salg i alt**. I oversigtspanelet **Beløb** i feltet **Gebyrer** vises det samlede beløb for alle de gebyrer, der er beregnet for ordren og linjerne. Du kan se en mere detaljeret opdeling af gebyrerne ved at vælge **Ordre** på siden **Salgsordreoversigt** og derefter vælge indstillingen **Gebyrer** for at få vist, tilføje eller rediger gebyrerne. Bemærk, at beregningen af leveringsgebyrer i ordrehovedet er baseret på den leveringsmåde, der er knyttet til hovedet. Leveringsgebyrer på linjeniveau beregnes ud fra den leveringsmåde, der er konfigureret for salgslinjen. Hvis der bruges flere leveringsmåder på forskellige linjer, bliver der muligvis anvendt flere gebyrer, som lægges sammen. Derefter vises det samlede beløb i feltet **Gebyrer** på siden **Salgsordreoversigt**.

Hvis indstillingen **Aktivér ordrefuldførelse** er slået fra, skal brugerne manuelt udløse beregningen af gebyrer. På siden **Salgsordre** i handlingsruden skal du vælge **Lagdelte gebyrer** under fanen **Sælg** i gruppen **Beregn**. Meddelelsen "Lagdelte gebyrer er beregnet" vises. Du kan derefter vælge indstillingen **Gebyrer** under fanen **Sælg** for at få vist, redigere eller slette de beregnede gebyrer.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Bruge fremskyndede leveringsmåder til callcenterordrer

Du kan også knytte en fremskyndelseskode til en leveringsmåde, som du konfigurerer. Denne kode bruges som et sorterings- og rapporteringværktøj ved prioritering. Det udløser i øjeblikket ikke yderligere gebyrer, der skal anvendes på ordren. Hvis du vil angive fremskyndelseskoder, skal du gå til **Salgs- og marketing \> Opsætning \> Distribution \> Fremskynd koder**.

Ved der for eksempel skal leveres med fly næste arbejdsdag, skal pluk udføres på lagerstedet inden kl. 13 hver dag. I så fald kan der oprettes en fremskyndelseskode, som kan knyttes til enhver leveringsmåde for næste arbejdsdag, der er konfigureret i systemet. Når lagerstedet opretter sin plukbølge, kan den relevante fremskyndelseskode i feltet **Fremskynd** bruges som et filter, så pluk kun køres for ordrer, der har de leveringsmåder, der er knyttet til koden.

Desuden, når der angives en callcenterordre, kan en fremskyndelseskode manuelt anvendes på salgsordrehovedet eller på en enkelt salgsordrelinje. Koden kan igen bruges til sorterings- eller rapporteringsformål. Nogle gange skal en ordre håndteres omhyggeligt på grund af et kundeserviceproblem. I dette tilfælde kan der anvendes en bestemt fremskyndelseskode på ordrehovedet eller -linjerne for at identificere og prioritere ordren under ordreopfyldningsprocessen.
