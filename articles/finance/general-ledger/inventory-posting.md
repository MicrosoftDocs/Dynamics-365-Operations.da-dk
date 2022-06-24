---
title: Lagerpostering
description: Denne artikel forklarer fanen Lagerpostering på siden Lagerposteringsprofil.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 7fd507dd171b0d49673bdd0d0900b3f02dbcb65b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891545"
---
# <a name="inventory-posting"></a>Lagerpostering

Fanen **Lager** på siden **Lagerposteringsprofiler** bruges til at styre, hvordan lagertransaktioner bogføres i finansmodulet. Lagertransaktioner er transaktioner, der ikke oprettes ud fra salgsordrer, indkøbsordrer eller produktionsordrer. De bogfører automatisk de fysiske og økonomiske opdateringer på lageret samtidig. En undtagelse er flytteordrer, der adskiller fysiske og økonomiske opdateringer, når du afsender og modtager lagerbeholdning.

Følgende tabel indeholder nogle eksempler på lagertransaktioner.

| Transaktionstype | Tilgang eller afgang | Fysisk bogføring, økonomisk bogføring eller begge dele | Beskrivelse |
|---|---|---|---|
| Bevægelse | Begge | Begge | <p>En bevægelseskladde er en lagerkladde, som du kan bruge til at tilføje eller fjerne lagerbeholdning. Den fungerer ligesom en lagerreguleringskladde. En nøgleforskel er dog, at den hovedkonto, der modkonterer posten, er angivet.</p><p>Bevægelseskladden angiver primosaldi og engangsreguleringer, der skal udgiftsføres. Den bruges f.eks., når lagerbeholdning fjernes til en salgsprøve.</p><p>Når kladden bogføres, finder de fysiske og økonomiske opdateringer sted samtidig.</p><p>Positive antal på kladdelinjerne repræsenterer tilgange, og negative antal repræsenterer afgange.</p> |
| Lagerregulering | Begge | Begge | En lagerreguleringskladde bruges til at tilføje eller fjerne lagerbeholdning. Du kan ikke vælge en modkonto. Kun de konti, der er angivet på siden **Lagerposteringsprofil**, bruges til at opdatere finansposten. |
| Overførsel (kladde) | Begge | Begge | <p>En overførselskladde bruges til at flytte lager fra én lokation til en anden (ved hjælp af lagringsdimensioner). Den opdaterer produktoplysningerne på en lagertransaktion med nye produkt- eller sporingsdimensioner.</p><p>Med en overførselskladde oprettes én linje for flytningen af en vare. Denne linje har "fra"- og "til"-felter til lagerdimensionerne. Hver linje i en overførselskladde opretter to lagertransaktioner. Den ene transaktion oprettes for "fra"-lagertransaktioner. Den repræsenterer afgangen og har et negativt antal. Den anden transaktion oprettes for "til"-lagertransaktioner. Den repræsenterer tilgangen og har et positivt antal.</p><p>Overførselskladder opretter muligvis ikke et bilag, hvis flytningen af lageret betragtes som en ikke-økonomisk overførsel. Lagerdimensioner, der er forskellige for værdierne "fra" og "til", er ikke markeret med indstillingen **Økonomisk lager** på siden **Lagringsdimensionsgruppe** eller **Sporingsdimensionsgruppe**. Hvis indstillingen **Økonomisk lager** f.eks. ikke er markeret for dimensionen **Lokation**, og du flytter lager fra én lokation til en anden på samme sted og lagersted, oprettes der ikke et bilag.</p><p>Overførselskladder afviger fra overførselsordrer ved, at der ikke findes dokumenter til flytningen. Opdateringen udføres i én transaktion ved at bogføre kladden. Derimod kan en overførselsordre generere pluk- og forsendelsesdokumenter og kræver to opdateringer for at behandle transaktionen.</p> |
| Forsendelse af flytteordre | Emne | Begge | <p>Når du opretter en ny overførselsordre, har hver kombination af en linje og en lagerdimension to lagertransaktioner: en til forsendelsen af overførselsordren og en til tilgangen af overførselsordren. Når overførselsordren afsendes, opdateres to lagertransaktioner, og der oprettes to ekstra lagertransaktioner til varetransport, til i alt fire lagertransaktioner.</p><ol><li>Den første lagertransaktion bruges til at fjerne varen fra kildelagerstedet og -lokationen. Afgangsstatus for denne transaktion er **Solgt** for at angive, at varen ikke længere er tilgængelig på lagerstedet.</li><li>Den anden lagertransaktion bruges til at føje varen til det transitlagersted, der er valgt for det lagersted, som varen overføres fra. Denne transaktions tilgangsstatus er **Købt**.</li><li>Den tredje lagertransaktion er til overførsel fra transitlagerstedet til destinationslagerstedet. Afgangsstatussen for denne transaktion er **Reserveret fysisk**. Denne status sikrer, at varen ikke kan forbruges af en anden proces, mens den stadig er i transit.</li><li>Den fjerde lagertransaktion er for varemodtagelsen på destinationslagerstedet. Denne transaktions tilgangsstatus er **Bestilt**.</li></ol> |
| Modtagelse af flytteordre | Kvittering | Begge | Når der modtages en overførselsordre på destinationslagerstedet, opdateres lagerstatussen for den lagertransaktion, der er på transitlagerstedet (nummer 3 i foregående eksempel), til **Solgt**, og lagerstatus for lagertransaktionen for destinationslagerstedet opdateres til **Købt**. |
| Styklister | Begge | Begge | Du kan bruge en styklistekladde til at færdigmelde et produkt og forbruge de råvarer, der er forbrugt under processen, uden at bruge en produktionsordre. En styklistekladde indeholder typisk mindst én positiv linje for færdigvaren og en eller flere negative linjer for de råvarer, der forbruges. Linjen med færdigvare er en tilgang til lageret, hvorimod negative linjer er lagerafgange for råvarerne. Når du opretter en styklistekladde, er den første linje styklistehovedet, og efterfølgende linjer, der tilføjes, er styklistelinjerne. |
| Ændring af beholdningsejerskab | Begge | Begge | Kladden for ændring af beholdningsejerskab bruges til at ændre ejerskabet af konsignationslager fra leverandøren til din organisation. Kladder til ændring af lagerejerskab ligner lageroverførselskladder, fordi der er knyttet to lagertransaktioner til hver kombination af en linje og en lagerdimension. Den ene lagertransaktion fjerner lageret fra leverandøren i dimensionen **Ejerskab**, og den anden føjer varen til den juridiske enhed i **Ejerskab**-dimensionen. |
| Varemodtagelse | Kvittering | Fysisk | En varemodtagelseskladde bruges til at opdatere lagertilgangsstatussen til **Registreret**. Det bruges typisk til indkøbsordremodtagelse af varer og salgsordrereturneringer. |
| Produktionsindlagring | Kvittering | Fysisk | En produktionsindlagringskladde ligner en varemodtagelseskladde. Produktionsindlagring anvendes til modtagelse af færdigvarer fra en produktionsordre på lagerstedet. Når kladden bogføres, ændres status for lagertransaktionen til **Registreret**. |
| Tælling | Begge | Begge | En optællingskladde bruges til at registrere antallet af varer, der er optalt for en bestemt kombination af lagerdimensioner. Lagertransaktioner oprettes, når kladdelinjen har en optællingsdifference. En linje, der har et højere optalt antal, forårsager en tilgang til lageret. En linje, der har et lavere optalt antal, forårsager en afgang fra lageret. Linjer, hvor det optalte antal svarer til det forventede antal, har ingen lagertransaktioner. |
| Mærkatoptælling | Ikke relevant | Ikke relevant | En mærkatoptællingskladde bruges til at spore lagermærkater, der tildeles og bruges i en fuld lageroptælling. Du kan bruge kladden til at tildele et mærkatnummer til en bestemt kombination af en vare og en lagerdimension og til at spore mærkatets status under en fuld lagerbeholdning. Mærkatoptællingskladder opretter ikke lagertransaktioner |
| Kvalitetsordrer | Afgang | Fysisk | <p>En kvalitetsordre bruges til registrering af testresultaterne for et bestemt parti på lageret. Hver kvalitetsordre er relateret til en eksisterende lagertransaktion eller en del af en lagertransaktion.</p><p>En kvalitetsordre genererer en ny lagertransaktion i to situationer:</p><ul><li>Kvalitetsordren er markeret som **Destruktiv test** under fanen **Generelt**.</li><li>Kvalitetsordren er markeret som **Karantæne efter valideringsfejl** under fanen **Generelt**, og testen mislykkes under valideringen. Der oprettes to lagertransaktioner i dette tilfælde. Den ene lagertransaktion fjerner varen fra den oprindelige kombination af lagerdimension og lokation, og den anden føjer varen til karantænelagerstedet.</li></ul> |
| Karantæneordrer | Begge | Begge | <p>En karantæneordres lagertransaktioner er som en flytteordre. Et karantænelagersted bruges til at spore lageret. Der er to tilgangstransaktioner og to afgangstransaktioner.</p><p>Når ordren oprettes første gang, oprettes der to transaktioner. Tilgangstransaktionen har statussen **Bestilt** for det karantænelagersted, der er knyttet til det lagersted, hvor varen er placeret. Afgangstransaktionen har statussen **I bestilling** for det lagersted, hvor varen opbevares.</p><p>Når du starter karantæneordren, oprettes der to ekstra transaktioner, og de eksisterende transaktioner opdateres. Status for tilgangstransaktionen for karantænelagerstedet opdateres til **Modtaget**, og status for afgangstransaktionen for lagerstedet opdateres til **Trukket**.</p><p>De to nye transaktioner bruges til at angive den endelige flytning tilbage til lagerstedet. Tilgangstransaktionen har status af **Bestilt** for lagerstedet, og afgangstransaktionen har statussen **Reserveret fysisk** for karantænelagerstedet.</p><p>Når du færdigmelder en karantæneordre, repræsenterer denne handling den fysiske opdatering af karantæneordren. Tilgangsstatus på lagerstedet opdateres til **Modtaget**.</p><p>Når du afslutter karantæneordren, repræsenterer denne handling den økonomiske opdatering af karantæneordren. Status for afgangstransaktionerne opdateres til **Solgt**, og status for tilgangstransaktionerne opdateres til **Købt**.</p><p>Alternativt kan karantæneordren kasseres. Denne handling fjerner varen fra lageret. Når en karantæneordre kasseres, er der kun tre transaktioner tilbage. Tilgangstransaktionen for lagerstedet fjernes, og status for den resterende tilgangstransaktion opdateres til **Købt**. Status for de to afgangstransaktioner opdateres til **Solgt**. Denne handling er en fysisk og økonomisk opdatering af ordren.</p> |

## <a name="fixed-receipt-price-posting"></a>Bogføring af fast tilgangspris

Fast tilgangspris giver dig mulighed for at bruge en standardkostpris for et produkt. Den er et alternativ til at vælge indstillingen **Standardomkostning** på siden **Varemodelgruppe** for en vare. Den væsentligste forskel, når du bruger en fast tilgangspris, er, at den kostpris, der aktuelt er konfigureret, vil blive brugt for varen, når tilgangen til lageret bogføres. Der findes ingen værdireguleringsproces for en fast tilgangspris. Når der bogføres en økonomisk opdatering, bruges den aktuelle kostpris på bogføringstidspunktet. Hvis den kostpris, der bruges ved tilgangen, og fakturaen er forskellig, bogføres afvigelsen på driftskontiene for den faste tilgangspris.

Hvis du vil bruge en fast tilgangspris for et produkt, skal du fuldføre følgende konfiguration:

- På siden **Varemodelgruppe** skal afkrydsningsfeltet **Bogfør fysisk lager** være markeret for den vare, der er valgt på lagertransaktionslinjen.
- Markér feltet **Fast tilgangspris** på siden **Varemodelgruppe**.
- På siden **Lagerposteringsprofil** skal du angive hovedkonti for følgende posteringstyper:

    - Vind ved fast tilgangspris
    - Tab ved fast tilgangspris

Du kan finde flere oplysninger under [Fast tilgangspris](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Bogføring af fastvægt

Fastvægtprodukter bruges ofte i brancher som f.eks. fødevareindustrien, hvor produkter kan variere efter vægt eller størrelse, eller begge. Fastvægtprodukter bruger to måleenheder: en lagerenhed og en fastvægtenhed. Vægten af lagervaren, når den leveres på et lagersted, kan afvige fra vægten, når lagervaren sendes fra lagerstedet. Behandlingen af fastvægtprodukter justerer lagerbeholdningen.

Hvis der er en afvigelse i fastvægten, bogføres forskellene på de konti, der er angivet i felterne **Fastvægttab** og **Fastvægtavance** på siden **Lagerposteringsprofil**. Normalt er den samme hovedkonto angivet i begge felter.

I følgende tabel vises eksempler på standardbogføringstyper med eksempler på hovedkonti og beskrivelser.

- Kolonnen "Debet/Kredit?" angiver, om posteringen typisk bogfører debet- eller kreditbeløb. I nogle tilfælde kan en transaktion enten bogføre et debet- eller kreditbeløb.
- I kolonnen "Clearingkonto" angives, at bogføringstypen er en clearingkonto. Det betyder, at det beløb, der bogføres på denne konto, automatisk tilbageføres, når en senere transaktion bogføres.
- I kolonnen "P/F" angives bogføringstypen. "P" repræsenterer fysisk bogføring, og "F" repræsenterer økonomisk bogføring.
- I kolonnen "Følg" angives, om hovedkontoen for bogføringstypen typisk er den samme som hovedkontoen for en anden bogføringstype. Den angiver specifikt den bogføringstype, der typisk bruges til bogføringen.

> [!NOTE]
> Hovedkonti og hovedkontonavne i tabellen er kun forslag. Det anbefales, at du arbejder sammen med bogholderen for at finde den bedste konfiguration til virksomhedens behov.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | P/F | Følg | Beskrivende tekst |
|---|---|---|---|---|---|---|---|---|
| Fastvægt - tabskonto | 510520 | Lagerregulering | Udgift | | Nej | Begge | Fastvægt - profitkonto | Denne konto bruges, når du bogfører en lagertransaktion, hvor fastvægtbeløbet er lavere. |
| Fastvægt - profitkonto | 510520 | Lagerregulering | Udgift | | Nej | Begge | Fastvægt - tabskonto | Denne konto bruges, når du bogfører en lagertransaktion, hvor fastvægtbeløbet er højere. |

Du kan finde flere oplysninger om fastvægtprodukter under [Om fastvægtprodukter](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) og [Behandling af fastvægtprodukt med lokationsstyring](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Bogføring af overførsel fra lager til anlægsaktiv

Lager til anlægsaktivkladde (**Anlægsaktiver** \> **Kladder** \> **Lager til anlægsaktivkladde**) bruges til at flytte varer fra lageret og konvertere dem til anlægsaktiver. Du kan finde flere oplysninger under [Integration af anlægsaktiver](/fixed-assets/fixed-asset-integration.md).

I følgende tabel vises eksempler på standardbogføringstyper med eksempler på hovedkonti og beskrivelser.

- Kolonnen "Debet/Kredit?" angiver, om posteringen typisk bogfører debet- eller kreditbeløb. I nogle tilfælde kan en transaktion enten bogføre et debet- eller kreditbeløb.
- I kolonnen "Clearingkonto" angives, at bogføringstypen er en clearingkonto. Det betyder, at det beløb, der bogføres på denne konto, automatisk tilbageføres, når en senere transaktion bogføres.
- I kolonnen "P/F" angives bogføringstypen. "P" repræsenterer fysisk bogføring, og "F" repræsenterer økonomisk bogføring.
- I kolonnen "Følg" angives, om hovedkontoen for bogføringstypen typisk er den samme som hovedkontoen for en anden bogføringstype. Den angiver specifikt den bogføringstype, der typisk bruges til bogføringen.

> [!NOTE]
> Hovedkonti og hovedkontonavne i tabellen er kun forslag. Det anbefales, at du arbejder sammen med bogholderen for at finde den bedste konfiguration til virksomhedens behov.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | P/F | Følg | Beskrivende tekst |
|---|---|---|---|---|---|---|---|---|
| Anlægsaktivafgang | 180100 | Materielle anlægsaktiver | Aktiv | Kredit | Nej | Begge | Ikke relevant | Denne konto bruges, når du bogfører en lager til anlægsaktivkladde for at fjerne en vare fra lageret og konvertere den til et anlægsaktiv. |

## <a name="moving-average-posting"></a>Bogføring af glidende gennemsnit

Glidende gennemsnit er en tidsubegrænset efterkalkulationsmetode, der er baseret på princippet for gennemsnit. Omkostningerne for lagerafgange ændres ikke, når indkøbsomkostningen gør det. Differencen er aktiveret og baseret på en proportional beregning. Det beløb, der er tilbage, udgiftsføres.

I følgende tabel vises eksempler på standardbogføringstyper med eksempler på hovedkonti og beskrivelser.

- Kolonnen "Debet/Kredit?" angiver, om posteringen typisk bogfører debet- eller kreditbeløb. I nogle tilfælde kan en transaktion enten bogføre et debet- eller kreditbeløb.
- I kolonnen "Clearingkonto" angives, at bogføringstypen er en clearingkonto. Det betyder, at det beløb, der bogføres på denne konto, automatisk tilbageføres, når en senere transaktion bogføres.
- I kolonnen "P/F" angives bogføringstypen. "P" repræsenterer fysisk bogføring, og "F" repræsenterer økonomisk bogføring.
- I kolonnen "Følg" angives, om hovedkontoen for bogføringstypen typisk er den samme som hovedkontoen for en anden bogføringstype. Den angiver specifikt den bogføringstype, der typisk bruges til bogføringen.

> [!NOTE]
> Hovedkonti og hovedkontonavne i tabellen er kun forslag. Det anbefales, at du arbejder sammen med bogholderen for at finde den bedste konfiguration til virksomhedens behov.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | P/F | Følg | Beskrivende tekst |
|---|---|---|---|---|---|---|---|---|
| Prisdifference for glidende gennemsnit | 510600 | Prisdifference for glidende gennemsnit | Udgift | Begge | Nej | Begge | Ikke relevant | Denne konto bruges, når der er forskel på omkostningen mellem tilgangen og fakturaen. |
| Værdiregulering for glidende gennemsnit | 510610 | Værdiregulering med glidende gennemsnit | Udgift | Begge | Nej | Begge | Ikke relevant | Denne konto bruges, når du regulerer den glidende gennemsnitlige omkostning for et produkt. |

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfiguration af posteringsprofil

I følgende tabel vises eksempler på standardbogføringstyper med eksempler på hovedkonti og beskrivelser.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | P/F | Følg | Beskrivende tekst |
|---|---|---|---|---|---|---|---|---|
| Lagerafgang | 140100 | Materialelager | Aktiv | Kredit | Nej | Begge | Lagertilgang | Denne konto bruges, når en lagertransaktion, der bogføres, er en afgang (negativt antal) og ikke vedrører salg, indkøb eller produktion. Modkontoen til denne konto er kontoen Lagerudgifter, tab. Denne konto repræsenterer typisk lageret i balancen. |
| Lagerudgifter, tab | 510100 | Lagerdrift | Udgift | Debet | Nej | Begge | Lagerudgifter, overskud | Denne konto bruges, når en lagertransaktion, der bogføres, er en afgang (negativt antal) og ikke vedrører salg, indkøb eller produktion. Modkontoen til denne konto er kontoen Lagerafgang. |
| Lagertilgang | 140100 | Materialelager | Aktiv | Debet | Nej | Begge | Lagerafgang | Denne konto bruges, når en lagertransaktion, der bogføres, er en tilgang (positivt antal) og ikke vedrører salg, indkøb eller produktion. Modkontoen til denne konto er kontoen Lagerudgifter, overskud. Denne konto repræsenterer typisk lageret i balancen. |
| Lagerudgifter, overskud | 510100 | Lagerdrift | Udgift | Kredit | Nej | Begge | Lagerudgifter, tab | Denne konto bruges, når en lagertransaktion, der bogføres, er en tilgang (positivt antal) og ikke vedrører salg, indkøb eller produktion. Modkontoen til denne konto er kontoen Lagertilgang. |
| Intern kreditorpostering mellem enheder | 231500 | Internt mellem enheder – kreditor | Passiv | Debet | Nej | Begge | | Denne konto bruges, når der overføres lager mellem lagerdimensioner som f.eks. lokationer, og omkostningen for en vare er forskellig fra lokation til lokation. |
| Intern debitorpostering mellem enheder | 131500 | Internt mellem enheder – debitor | Aktiv | Kredit | Nej | Begge | | Denne konto bruges, når der overføres lager mellem lagerdimensioner som f.eks. lokationer, og omkostningen for en vare er forskellig fra lokation til lokation. |
