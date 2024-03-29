---
title: Oprette returneringer i POS
description: Denne artikel beskriver, hvordan du starter returneringer for cash and carry-transaktioner eller kundeordrer i Microsoft Dynamics 365 Commerce POS-programmet.
author: hhainesms
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: a49e9abd0143d480cc1cafb05be5e995fb3cebdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856992"
---
# <a name="create-returns-in-pos"></a>Oprette returneringer i POS

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du starter returneringer for cash and carry-transaktioner eller kundeordrer i Microsoft Dynamics 365 Commerce POS-appen.

> [!NOTE]
> I Commerce version 10.0.20 og senere findes der en ny funktion med navnet **Samlet behandling af returneringer i POS**. Denne funktion udgør en mere konsistent og ensartet returproces i POS, uanset transaktionstypen (cash-and-carry-transaktion eller kundeordre) eller den oprindelige kanal, som ordren blev oprettet i. Det anbefales, at alle organisationer aktiverer denne nye funktion for at forbedre den overordnede pålidelighed af returneringsbehandling via POS.
>
> Når funktionen er aktiveret, kan den ikke deaktiveres.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Behandle returneringer ved hjælp af returtransaktionsoperationen

Det anbefales, at du føjer handlingen for returtransaktionen til dit POS-[skærmlayout](pos-screen-layouts.md). I versioner før Commerce version 10.0.20 understøtter handlingen for returtransaktionen kun behandling af returneringer for cash-and-carry-transaktioner. Når du har aktiveret funktionen **Samlet returneringsbehandling for POS** i Commerce version 10.0.20 eller senere, understøtter handlingen for returtransaktionen også behandlingen af returneringer fra kundeordrer, f.eks. "afhentning" eller "udbringning", som allerede er faktureret.

I forbindelse med returtransaktionen kan brugere søge efter en cash-and-carry-transaktion eller en kundeordre, der skal returneres mod, ved at angive et af følgende fire søgekriterier. Brugerne kan angive disse kriterier ved hjælp af enhedstastatur, skærmtastatur eller stregkodescanner.

- Modtagelses-id
- Ordrenummer
- Kanalreference-id (kaldes også ordrebekræftelses-id)
- Faktura-id

Hvis der findes en transaktion eller en ordre, der svarer til søgekriterierne, vises siden **Produkter, der kan returneres**. Her kan brugere angive de varer, der returneres. De kan også angive returantal og årsagskoder.

For hver ordrelinje på listen over returvarer viser POS oplysninger om det oprindelige købsantal og antallet fra eventuelle returneringer, der tidligere er behandlet. Det returantal, som en bruger angiver for en ordrelinje, skal være mindre end eller lig med værdien i feltet **Tilgængelig til returnering**.

![Siden Returvarer.](media/returnslist.png)

Under returneringen, hvis en bruger har det fysiske produkt, og det pågældende produkt har en stregkode, kan brugeren scanne stregkoden for at registrere returneringen. Hver scanning af stregkoden øger returantallet med én vare. Men hvis stregkodelabelen har et indlejret antal, vil dette antal blive angivet i feltet **Returnering nu**.

Brugerne kan også manuelt vælge varer, der skal returneres, på siden **Returvarer** og derefter opdatere feltet **Returnering nu** ved hjælp af detaljeruden til højre.

Hvis der angives det maksimale antal **Returnering nu** for en transaktion, kan brugeren vælge handlingen **Vælg alt** på POS-applinjen for at angive det maksimale antal, der kan returneres, på alle linjer.

For hver linje, der indeholder et antal **Returnering nu**, skal brugeren vælge en returårsagskode ved hjælp af detaljepanelet. For returneringer af cash-and-carry-transaktioner konfigureres returårsagskoder som infokoder i butikkens funktionalitetsprofil. I forbindelse med returneringer af kundeordrer konfigureres returårsagskoder på siden **Retur årsagskoder** i Dynamics 365 Commerce hovedkontoret.

Når returantallet og årsagskoden er angivet for hver vare, der skal returneres, kan brugeren vælge handlingen **Returner** på POS-applinjen for at fortsætte behandlingen. Siden POS-transaktion vises, hvor de returvarer, der blev valgt på forrige side, er føjet til indkøbsvognen. Varernes **Returnering nu**-antal vises som negative antalslinjer i transaktionen, og den samlede refusion beregnes.

Brugerne kan føje linjer til en returtransaktion, hvis de opretter en udvekslingsordre. Brugerne kan også føje flere ad hoc-returvarer til en returtransaktion ved at bruge handlingen **Returner produkt** for en valgt salgslinje med et positivt antal, som er tilføjet.

> [!NOTE]
> Handlingen **Returner produkt** i POS angiver ikke nogen validering i forhold til nogen af de oprindelige transaktioner og tillader, at ethvert produkt returneres. Det anbefales derfor, at kun autoriserede brugere får tilladelse til at udføre denne handling, eller at der kræves en ledertilsidesættelse, hvis denne handling bruges.

Hvis en refusion skal betales ved kassen, kan organisationer konfigurere [politikker for refundering](refund_policy_returns.md), der begrænser de betalingsmåder, der kan bruges til at refundere kunder. Hvis den oprindelige transaktion blev betalt med kreditkort, afhængig af betalingsprocessoren og systemkonfigurationen, kan brugerne have mulighed for at [udstede en refusion til det oprindelige kort](dev-itpro/linked-refunds.md). I dette tilfælde kan refusionen behandles, uden at kunden skal stryge kreditkortet igennem igen. Det oprindelige betalingstoken bruges til at udstede refusionen.

## <a name="other-return-options-in-pos"></a>Andre returindstillinger i POS

Når funktionen **Samlet behandling af returneringer i POS** er aktiveret, kan brugerne også bruge handlingen **Vis kladde** i POS til at starte en returnering af en cash-and-carry-transaktion eller en kundeordre. Derefter kan de vælge en transaktion i kladden og derefter vælge **Retur**-handlingen på POS-applinjen. Denne handling er kun tilgængelig, hvis der er returlinjer i ordren. Den starter den samme brugeroplevelse som handlingen **Returtransaktion**.

Brugerne kan også bruge handlingen **Tilbagekaldsordre** i POS til at søge efter og tilbagekalde kundeordrer. (Denne operation kan ikke bruges til cash-and-carry-transaktioner). I dette tilfælde kan du bruge **Retur**-handlingen på POS-applinjen, når en kundeordre er valgt, til at starte en returnering for kundeordren. Denne handling er kun tilgængelig, hvis der er returlinjer i ordren. Den starter den samme brugeroplevelse som handlingen **Returtransaktion** eller **Vis kladde**.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Returordrer bogføres i Commerce Headquarters som salgsordrer 

Når funktionen **Samlet behandling af returneringer i POS** er aktiveret, skrives alle returneringer, der oprettes i POS, til Commerce Headquarters som salgsordrer, der har negative linjer. I versioner af Commerce før version 10.0.20 kan brugere vælge, om returordrer skal bogføres som salgsordrer med negative linjer, eller om de skal være returordrer, der oprettes via RMA-processen (Return Merchandise Authorization). 

I funktionen **Samlet behandling af returneringer i POS** er det frarådet at bruge RMA-processen til at oprette returneringer i POS. Når denne funktion er aktiveret, oprettes alle returneringer som salgsordrer med negative linjer.

## <a name="offline-return-processing-improvements"></a>Forbedringer af offline returbehandling

I de fleste tilfælde, når en returnering behandles i POS, forsøger systemet at foretage en realtidstjenestes (RTS) opkald til Commerce Headquarters for at validere de aktuelle mængder, der er tilgængelige til returnering. Med denne validering forhindres det, at kunden forsøger at returnere den samme vare flere steder.

Til håndtering af situationer, hvor RTS-opkaldet ikke kan foretages på grund af netværks- eller forbindelsesproblemer, er der oprettet en proces, der bruges til periodisk synkronisering af returantalsdata fra Commerce Headquarters til en butiks kanaldatabase. Denne sporing på kanalsiden hjælper med at sikre, at de **Tilgængelig til returnering**-antal, som er vist i POS, er nogenlunde nøjagtige, også når POS er offline. Det sikrer også, at POS kan fortsætte med at validere oplysningerne på kanalsiden for at hjælpe med at forhindre falske returneringer.

Hvis du vil bruge offline returprocessen på den rigtige måde, skal organisationer planlægge batchjobbet **Opdater returantal** i Commerce Headquarters, så det køres ofte. Det anbefales, at dette job køres med samme frekvens som det P-job, der trækker nye transaktioner fra Commerce-kanaler til Commerce Headquarters.

Jobbet **Opdater returantal** beregner det antal, der er tilgængeligt for returnering for alle salgsordrer i Commerce Headquarters. De data, som jobbet beregner, skal derefter sendes til kanaldatabaser, så butikskanalerne kan opdateres. Distributionsjobbet **Returantal** (1200) bruges til dette formål. Da data om returantal synkroniseres fra Commerce Headquarters, og der behandles en returnering i POS, men det ikke er muligt at sende et RTS-opkald, kan POS bruge returoplysningerne på kanalsiden til at validere de **Tilgængelige til returnering**-antal for en bestemt salgslinje.

Når der ikke kan foretages RTS-opkald, og POS bruger data fra kanalsiden til returneringsvalidering, får brugerne vist en advarsel om, at de opretter en "offline" returnering. De er derfor opmærksom på, at det **Tilgængelig til returnering**-antal, der vises i POS, er forældet og ikke længere nøjagtigt, afhængigt af hvornår jobbet **Opdater returantal** sidst blev behandlet og synkroniseret med kanalen.

En kunde har f.eks. for nylig behandlet en returnering af en ordrelinje i en anden kanal, men disse data er endnu ikke synkroniseret til kanaldatabaserne via jobbet **Opdater returantal**. Kunden går derefter til en anden butik og forsøger at returnere den samme vare igen. I dette tilfælde vil POS tillade, at varen returneres igen, hvis butikken ikke kan foretage et RTS-opkald til Commerce Headquarters for at hente returdata i realtid. Brugeren advares dog om, at de oplysninger, der bruges til at validere returneringen, muligvis er forældede. Den meddelelse, brugeren modtager, er kun en advarselsmeddelelse. Den forhindrer ikke brugeren i at fortsætte med at behandle returneringen.

Hvis oplysningerne på kanalsiden af en eller anden grund ikke er opdateret, og der behandles en offline returnering af et antal, der overstiger det faktiske **disponible antal til returnering**, kan der genereres en fejl, når bogføring af opgørelsen køres for at oprette transaktionen i Commerce headquarters.

> [!NOTE]
> Når funktionen **Samlet behandling af returneringer i POS** er aktiveret, bliver nye valgfrie funktioner, der understøtter valideringen af serialiserede produktreturneringer, tilgængelige. Du kan finde flere oplysninger under [Returnere serienummerstyrede produkter i POS](POS-serial-returns.md).

## <a name="version-details"></a>Versionsdetaljer

Følgende liste indeholder de mindste versionskrav for de forskellige komponenter.
- Commerce Headquarters: Version 10.0.20
- Commerce Scale Unit (CSU): Version 9.30
- POS: Version 9.30

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Aktivér beregning af passende moms for returneringer med delvist antal

Denne funktion sikrer, at momsen i sidste ende er lig med det oprindeligt opkrævede momsbeløb, når en ordre returneres ved hjælp af flere fakturaer.

1. Gå til arbejdsområdet **Funktionsstyring**, og søg efter **Aktivér beregning af passende moms for returneringer med delvist antal**.
1. Vælg **Aktivér beregning af passende moms for returneringer med delvist antal**, og klik derefter på **Aktivér**.

## <a name="set-up-return-locations-for-retail-stores"></a>Konfigurere returneringslokaliteter for detailbutikker

I Commerce kan du konfigurere returneringslokaliteter, der er baseret på detailinfokoder og årsagskoder for salg og marketing. Kassereren identificerer ofte årsagen til en returnering, når en kunde returnerer et køb. Du kan angive, at returnerede produkter skal tildeles til forskellige returneringslokaliteter på lageret ud fra kassererens svar på infokoder og årsagskoder, der vises på POS'en i -kasseapparatet.

En kunde returnerer f.eks. et defekt produkt, og kassereren behandler returtransaktionen. Når Retail POS viser infokoden for returneringer, vælger kassereren underkoden for defekte returneringer. Det returnerede produkt tildeles derefter automatisk til en bestemt returlokation.

En returneringsplacering kan være en butik, et lagersted, en lokalitet i en butik eller et lagersted eller en bestemt palle, afhængigt af de lokaliteter, som din organisation har oprettet. Du kan knytte de enkelte returneringslokaliteter til én eller flere detailinfokoder dog salg og marketing-årsagskoder.

### <a name="prerequisites"></a>Forudsætninger

Inden du kan konfigurere returneringslokaliteter, skal du konfigurere følgende elementer:

- **Detailinfokoder** – Beskeder på POS-kasseapparatet, der er angivet i modulet **Detail**. Du kan finde flere oplysninger i [Konfigurere oplysningskoder](/dynamicsax-2012/appuser-itpro/setting-up-info-codes).
- **Årsagskoder for salg og marketing** – Beskeder på POS-kasseapparatet, der er angivet i modulet **Salg og marketing**. Du kan finde flere oplysninger i [Konfigurere årsagskoder](/dynamicsax-2012/appuser-itpro/set-up-return-reason-codes).
- **Lagerlokationer** – De steder, hvor lagerbeholdningen opbevares. Du kan finde flere oplysninger i [Konfigurere Lagerlokationer](/dynamicsax-2012/appuser-itpro/about-locations).
    
### <a name="set-up-return-locations"></a>Konfigurer returneringslokationer

Benyt følgende fremgangsmåde for at konfigurere returneringslokaliteter.

1. Gå til **Detail og Commerce \> Kanalkonfiguration \> Lagersteder**, og vælg et lagersted.
1. I feltet **Standardreturlokation** i oversigtspanelet **Detail** skal du vælge den lagerlokation, der skal bruges til returneringer, hvor infokoderne eller årsagskoderne ikke er knyttet til returlokationerne.
1. I feltet **Standardreturpalle** i oversigtspanelet Detail skal du vælge den palle, der skal bruges til returneringer, hvor infokoderne eller årsagskoderne ikke er knyttet til returlokationerne.
1. Gå til **Detail og Commerce \> Lagerstyring \> Returlokationer**.
1. Vælg **Ny** for at oprette en ny lagerreturneringspolitik.
1. Angiv et entydigt navn og en beskrivelse for returneringslokaliteten.

    > [!NOTE]
    > Navnet angives automatisk, hvis der er oprettet en nummerserie for returneringslokaliteter.

1. I oversigtspanelet **Generelt** skal du angive indstillingen **Udskriv labels** til **Ja**, hvis du vil udskrive labels for alle de produkter, der er tilknyttet returlokationer.
1. Angiv **Bloker lager** til **Ja** for at tage de returnerede produkter i standardreturneringslokaliteten ud af lageret og forhindre, at de bliver solgt.
1. Hvis du vil tilknytte specifikke detail infokoder og underkoder til returplaceringer, skal du følge disse trin:

    1. Vælg **Tilføj** i oversigtspanelet **Detailoplysningskoder**.
    1. Vælg en **Infokode** for returneringer i feltet.
    1. I feltet **Underkode** skal du vælge en underkode for årsagen til returneringen. Angiv en beskrivelse af den valgte underkode i feltet **Beskrivelse**.
    1. Vælg den butik, hvor infokoden bruges, i feltet **Butik**.
    1. Brug felterne **Lagersted**, **Lokalitet** og **Palle-id** til at angive en returlokation. For eksempel hvis du vil angive et bestemt sted i en butik, skal du vælge en butik i feltet **Butik** og en lokalitet i feltet **Lokation**.
    1. Marker afkrydsningsfeltet **Bloker lager** for at tage returnerede produkter ud fra lageret og forhindre, at de bliver solgt.

1. Hvis du vil tilknytte specifikke salgs- og marketingårsagskoder til returplaceringer, skal du følge disse trin:

    1. Vælg **Tilføj** i oversigtspanelet **Salgs- og marketing årsagskoder**.
    1. Vælg en ny årsagskode for returneringer i feltet **Årsagskode**. Angiv en beskrivelse af den valgte årsagskode i feltet **Beskrivelse**.
    1. Vælg den butik, hvor årsagskoden bruges, i feltet **Butik**.
    1. Brug felterne **Lagersted**, **Lokalitet** og **Palle-id** til at angive en returlokation. For eksempel hvis du vil angive en bestemt palle på en lokalitet på et lagersted, skal du vælge et lagersted i feltet **Lagersted**, en lokalitet i feltet **Lokation** og en palle i feltet **Palle-id**.
    1. Marker afkrydsningsfeltet **Bloker lager** for at tage returnerede produkter ud fra lageret og forhindre, at de bliver solgt.

    > [!NOTE]
    > Hvis der bruges en politik for returlokation for et element, men den returårsagen, som kassereren vælger, ikke svarer til nogen kode, der er angivet i oversigtspanelet **Detail infokoder** eller **årsagskoder for salg og marketing**, sendes varen til den standardreturlokation, der er defineret på **lagerstedssiden**. Indstillingen af afkrydsningsfeltet **Bloker lager** i oversigtspanelet **Generelt** på siden **Returlokation** bestemmer desuden, om den returnerede vare skal være lagerspærret.

1. Gå til **Detail og Commerce \> Commerce-produkthierarki**.
1. Vælg en returlokation i feltet **Returlokation** i oversigtspanelet **Administrer egenskaber for lagerkategorier**. Da der kan defineres flere politikker for returplacering for samme butik, bestemmer den værdi, du vælger her, den politik for returplacering, der bruges.

## <a name="additional-resources"></a>Yderligere ressourcer

[Returnere serienummerstyrede produkter i POS](POS-serial-returns.md)

[Sammenkædede refusioner af tidligere godkendte og bekræftede transaktioner](dev-itpro/linked-refunds.md)

[Oprette og opdatere en politik for returneringer og refusion for en kanal](refund_policy_returns.md)

[Visuelle konfigurationer af POS-brugergrænseflade](pos-screen-layouts.md)
