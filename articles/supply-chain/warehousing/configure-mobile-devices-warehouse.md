---
title: Konfigurere mobilenheder til lagerstedsarbejde
description: Dette emne beskriver, hvordan du konfigurerer de menupunkter, som lagerarbejdere kan bruge til at udføre arbejde på en mobilenhed.
author: MarkusFogelberg
manager: tfehr
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ae7587fc46d2907241a5da3b6329465d77b3555
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383084"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a>Konfigurere mobilenheder til lagerstedsarbejde

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer de menupunkter, som lagerarbejdere kan bruge til at udføre arbejde på en mobilenhed.

> [!NOTE]
> Dette emne vedrører funktioner i Lagerstedsstyring. Den gælder ikke for funktioner i Lagerstyring. De menupunkter, der vises i menuerne på en mobilenhed for lagersted, er konfigureret på siden **Menupunkter i mobilenhed**. Da menupunkterne kan anbringes i forskellige menuer, er det nemt at konfigurere menustrukturer, så kun bestemte typer arbejde vises for bestemte brugere. Du kan konfigurere menupunkter til at gøre følgende opgaver:

-   Behandle en forespørgsel eller udføre en aktivitet, f.eks. udskrive en etiket, generere id-numre, starte en produktionsordre eller hurtigt søge efter oplysninger om varer på en lokalitet.
-   Oprette arbejde, der udføres via en anden proces. Hvis der f.eks. modtages en vare for en indkøbsordre, kan det oprette læg på lager-arbejde for en anden arbejder.
-   Udfør arbejde, der er oprettet af en anden proces (eksisterende arbejde), som læg på lager-arbejde, der blev oprettet, da der blev modtaget en vare for en indkøbsordre.

Når du vil oprettes et menupunkt for en aktivitet eller en undersøgelse, skal du indstille feltet **Tilstand** til **Indirekte**. En liste over **Aktivitetskode** indstillinger og bliver derefter tilgængelig, så du kan vælge typen af forespørgsel eller aktivitet, som menupunktet er til. Når du vil oprette et menupunkt for at generere lagerstedsarbejde, skal du indstille feltet **Tilstand** til **Arbejde**. En liste over **Arbejdsoprettelsesproces** indstillinger og bliver derefter tilgængelig. Hvis du vil oprette et menupunkt for at behandle eksisterende lagerstedsarbejde, skal du angive feltet **Tilstand** til **Arbejde** og derefter angive indstillingen **Brug eksisterende arbejde** til **Ja**. 

> [!NOTE]
> Flere felter kan være tilgængelige for menupunktet, afhængigt af den tilstand, du vælger for menupunktet, og om menupunktet bruges til at udføre eksisterende arbejde. Du kan finde oplysninger om valg af yderligere felter i afsnittet "Yderligere indstillinger for menupunkter" i denne artikel.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Konfigurere menupunkter for aktiviteter og forespørgsler
Hvis feltet **Tilstand** for et menupunkt er angivet til **Indirekte**, kan du oprette et menupunkt, der udfører en generel aktivitet eller forespørgsel, der ikke skaber arbejde. Af eksempler kan nævnes udskrivning af id-nummer og forespørgsler om varerne på en lokalitet. I følgende tabel vises de indstillinger, der er tilgængelige.

| Indstilling                      | Beskrivelse                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ingen                        | Denne standardværdi aktiverer ikke en aktivitet eller en forespørgsel.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Om                       | Få vist oplysninger om systemet, f.eks. versionsnummer, lagersteds-id og den arbejder, der i øjeblikket er logget på.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Skift lagersted            | Skift det lagersted, som en arbejder er logget på.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Lokationsforespørgsel            | Få vist oplysninger om alle varer og mængder for en lokalitet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Id-forespørgsel       | Få vist antallet af varer på en nummerplade og placeringen af nummerpladen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Start produktionsordre      | Start en produktionsordre.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Produktionsspild            | Angiv antallet af spild, som blev oprettet under produktionen for hver linje på styklisten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Sidste produktionspalle      | Angiv, at den sidste palle af varer er fremstillet til en produktionsordre, og at status for produktionsordren skal opdateres til **Færdigmeldt**. Status for de råvarer, der ikke blev forbrugt under produktionen, ændres tilbage fra **Plukket** til **I bestilling**, og varerne kan returneres til lageret.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Vareforespørgsel                | Scan en vare for at finde ud af, hvor det er på lager. Forespørgslen returnerer alle lokaliteter og antal for den scannede vare.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Genudskriv etiket               | Udskriv et id-nummer igen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Id-build         | Opret et overordnet id-nummer ved at kombinere flere id-numre på den lokalitet. Denne indstilling er nyttig, hvis du flytter flere id-numre på samme tid. Når det overordnede id-nummer er flyttet, skal du udføre en id-nummerpause, før du kan plukke varer fra hvert id-nummer. <p></p>**Tip!** Hvis du vil flytte et overordnet id-nummer, skal du bruge en mobilenhed, der er konfigureret til at oprette arbejde til bevægelser.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Id-pause         | Opdel et id-nummerbuild, så du kan plukke varer fra de id-numre, der var i buildet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Chaufførens check-in             | Hvis du bruger Transportstyring, kan du se, at der er kommet en chauffør, ved at scanne det udgående last-id, aftale-id eller leverance-id. I forbindelse med denne indstilling skal en last være knyttet til aftalen, og at status for lasten skal være **Indlæst**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Chaufførens check-ud            | Registrer, at en chauffør har fuldført aftalen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Ryd cachen med nummerserie | Slet numre i nummerserier fra cachen med nummerserier. Denne aktivitet udføres typisk af en systemadministrator for at løse cachingproblemer, når der bruges mobilenheder.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Skift batchdisposition    | Tillad, at en arbejder kan angive en batchdispositionskode for en vare og batch. Denne indstilling opdaterer den dispositionskode, der er angivet for batchen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Vis oversigt over åbent arbejde      | Vis en liste over tilgængeligt arbejde for en bestemt bruger. Brugeren kan derefter vælge arbejde, der skal udføres, og sendes videre til det. Denne liste er beregnet til at blive vist tabletenheder med en skærmstørrelse på 7 tommer eller derover. Når du vælger denne indstilling, bliver menupunkterne **Rediger forespørgsel** og **Feltliste** tilgængelige. På siden **Rediger forespørgsel** kan du angive kriterier for det arbejde, der vises på listen. På siden **Feltliste** kan du vælge, hvilke felter der skal vises på opgavelisten. Du kan f.eks. reducere antallet af felter, der vises, så brugeren hurtigere kan vælge den mest hensigtsmæssige workflowopgave. Du kan også vælge, hvor mange arbejdsposter der skal vises pr. side, i feltet **poster pr. side** i oversigtspanelet **Generelt**. Hvis indstillingen **Tillad, at brugere filtrerer arbejde efter transaktionstype** er markeret, inkluderer opgavelisten kontrolelementet **Filtrer arbejde**, så brugeren kan filtrere efter transaktionstype. Brugeren kan kun se arbejde på opgavelisten, som de har adgangstilladelse til. Du skal sikre, at brugere har tilladelse til en eller flere brugerstyrede menupunkter, der understøtter de specifikke opgaveklassetyper, som de skal have adgang til. Tilladelser kontrolleres, når en bruger forsøger at udføre arbejde på listen. |

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Konfigurer menupunkter for at oprette arbejde for en anden arbejder eller proces
Du kan konfigurere et menupunkt, der opretter arbejde for en anden arbejder, efter en indledende handling er udført på mobilenheden. Når én arbejder f.eks. bruger en mobilenhed til at modtage en vare, oprettes der læg på lager-arbejde for en anden arbejder. Hvis du vil konfigurere et menupunkt, der skaber arbejde, skal du gå til siden **Menupunkter i mobilenhed**, feltet **Tilstand** og vælge **Arbejde**. I følgende tabel er indstillingerne i feltet **Arbejdsoprettelsesproces** arrangeret efter arbejdsordretype.

<table>
<tbody>
<tr>
<th>Arbejdsordretype</th>
<th>Indstilling</th>
<th>Beskrivelse</th>
</tr>
<tr>
<td rowspan="8">Indkøbsordre</td>
<td>Indkøbsordrelinje til modtagelse</td>
<td>Registrer modtagelsen af et antal af en vare ved hjælp af indkøbsordrenummeret og linjenummer på indkøbsordren, og opret læg på lager-arbejde for en anden arbejder.</td>
</tr>
<tr>
<td>Indkøbsordrelinje til modtagelse og læg på lager</td>
<td>Registrer modtagelsen af et antal af en vare ved hjælp af indkøbsordrenummeret og linjenummer på indkøbsordren, og læg varerne på lager. Den samme medarbejder udfører begge handlinger.</td>
</tr>
<tr>
<td>Indkøbsordrevare til modtagelse</td>
<td>Registrer modtagelsen af et antal af en vare for en indkøbsordre ved at registrere indkøbsordrenummeret og varenummer og oprette læg på lager-arbejde for en anden arbejder.</td>
</tr>
<tr>
<td>Indkøbsordrevare til modtagelse og læg på lager</td>
<td>Registrer modtagelsen af et antal af en vare for en indkøbsordre ved at registrere indkøbsordrenummeret og lægge varen på lager. Den samme medarbejder udfører begge handlinger.</td>
</tr>
<tr>
<td>Nummerplade til modtagelse</td>
<td>Modtag en indgående Advance Shipping Notice (ASN) ved hjælp af id.</td>
</tr>
<tr>
<td>Modtagelse af nummerplade og placering på lager</td>
<td>Modtag en indgående Advance Shipping Notice (ASN) ved hjælp af id og læg den på lager.</td>
</tr>
<tr>
<td>Modtagelse af varelast</td>
<td>Registrer modtagelsen af et antal for en last ved hjælp af last-id, og opret læg på lager-arbejde for en anden arbejder. Varenummeret og produktdimensionerne svarer til modtagelsen på indkøbsordrelinjerne.</td>
</tr>
<tr>
<td>Modtagelse af lagervare og placering på lager</td>
<td>Registrer modtagelsen af en last ved hjælp af last-id, og læg varerne på lager. Varenummeret og produktdimensionerne svarer til modtagelsen på indkøbsordrelinjerne. Den samme medarbejder udfører begge handlinger.</td>
</tr>
<tr>
<td rowspan="2">Returner ordre</td>
<td>Modtagelse af returordre</td>
<td>Registrer modtagelsen af et antal af en vare ved at registrere RMA-nummeret, og opret læg på lager-arbejde for en anden arbejder.</td>
</tr>
<tr>
<td>Modtagelse af returordre og placering på lager</td>
<td>Registrer modtagelsen af et antal af en vare ved at registrere RMA-nummeret, og læg varerne på lager. Den samme medarbejder udfører begge handlinger.</td>
</tr>
<tr>
<td rowspan="6">Overførselsordre</td>
<td>Varemodtagelse i flytteordre</td>
<td>Registrer modtagelsen af et antal af en vare, og opret læg på lager-arbejde for en anden arbejder.

<strong>Bemærk!</strong> Brug denne indstilling, hvis varerne er leveret fra et lagersted, der ikke er aktiveret til lagerprocesser.</td>
</tr>
<tr>
<td>Modtagelse af vare i flytteordre og placering på lager</td>
<td>Registrer modtagelsen af et antal af en vare, og læg varerne på lager. Den samme medarbejder udfører begge handlinger.

<strong>Bemærk!</strong> Brug denne indstilling, hvis varerne er leveret fra et lagersted, der ikke er aktiveret til lagerprocesser.</td>
</tr>
<tr>
<td>Modtagelse af linje i flytteordre</td>
<td>Registrer modtagelsen af et antal af en vare, og opret læg på lager-arbejde for en anden arbejder.</td>
</tr>
<tr>
<td>Flytteordrelinje til modtagelse og placering på lager</td>
<td>Registrer modtagelsen af et antal af en vare, og læg varerne på lager. Den samme medarbejder udfører begge handlinger.</td>
</tr>
<tr>
<td>Nummerplade til modtagelse</td>
<td>Modtag en indgående Advance Shipping Notice (ASN) ved hjælp af id.</td>
</tr>
<tr>
<td>Modtagelse af nummerplade og placering på lager</td>
<td>Modtag en indgående Advance Shipping Notice (ASN) ved hjælp af id og læg den på lager.</td>
</tr>
<tr>
<td rowspan="4">Produktion</td>
<td>Færdigmelding</td>
<td>Registrer et antal af en færdigvare, der er færdig til produktion, og opret læg på lager-arbejde for en anden arbejder. Antallet kan være nogle af eller hele det antal, der er planlagt til produktion.</td>
</tr>
<tr>
<td>Færdigmeld, og læg på lager</td>
<td>Registrer et antal af en færdigvare, der er færdig til produktion, og læg varerne på lager. Antallet kan være nogle af eller hele det antal, der er planlagt til produktion. Den samme medarbejder udfører begge handlinger.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Angiv, at en kanban er fuldført, og opret læg på lager-arbejde for en anden arbejder.</td>
</tr>
<tr>
<td>Kanban-læg på lager</td>
<td>Angiv, at en kanban er fuldført, og læg varerne på lager. Den samme medarbejder udfører begge handlinger.</td>
</tr>
<tr>
<td rowspan="5">Lager</td>
<td>Flytning</td>
<td>Registrer, at varerne er blevet flyttet fra én lokalitet til en anden. Arbejderen angiver den lokalitet, varerne er flyttet fra, og hvor de er flyttet til.</td>
</tr>
<tr>
<td>Karantæne</td>
<td>Skift status for den disponible lagerbeholdning for et id eller lokalitet for at gøre beskadigede eller manglende lagervarer, ikke-tilgængelige.</td>
</tr>
<tr>
<td>Bevægelse efter skabelon</td>
<td>Flyt varer fra én lokalitet til en anden på en måde, der er delvist automatisk. Medarbejderen vælger den lokalitet, varer skal flyttes fra, og systemet bruger lokalitetsvejledningen til at bestemme, hvor varerne skal flyttes til.</td>
</tr>
<tr>
<td>Overførsel af lagersted</td>
<td>Registrer, at varerne er blevet overført fra ét lagersted til et andet. Denne indstilling kræver, at arbejderen kan udføre arbejde på begge lagersteder.

<strong>Bemærk!</strong> Dette menupunkt kræver en standardlageroverførselskladde, hvor feltet <strong>Bilagsudstedelse</strong> er angivet til <strong>Postering</strong>.</td>
</tr>
<tr>
<td>Indlæsning af nummerplade</td>
<td>Brug denne indstilling, når du konfigurerer lagerstedet for første gang. Søg efter alle id'er på alle lokaliteter på lagerstedet. Lokaliteterne skal være id-kontrolleret. Du kan ikke bruge denne indstilling, hvis <strong>Serienummer</strong> eller <strong>Batchnummer</strong> er anført over <strong>Lokalitet</strong> i lagerreservationshierarkiet.</td>
</tr>
<tr>
<td rowspan="3">Cyklusoptælling</td>
<td>Regulering ind</td>
<td>Øg antallet af varer på lager. Angiv lokalitet, id, vare, antal, måleenhed og status.</td>
</tr>
<tr>
<td>Regulering ud</td>
<td>Reducer antallet af varer på lager. Angiv lagerets lokalitet, id, vare, antal, måleenhed og status.</td>
</tr>
<tr>
<td>Spotcyklusoptælling</td>
<td>Start en optælling for en lokalitet. Arbejderen skal tælle alle varer på lokaliteten. Når resultatet af en tælling er mindre end det forventede antal, betragtes det manglende antal som et tab.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Konfigurer menupunkter til behandling af eksisterende arbejde
Udover at oprette menupunkter til oprettelse af lagerstedsarbejde kan du angive menupunkter til behandling af arbejde, der allerede er oprettet. Angiv feltet **Tilstand** til **Arbejde**, og vælg indstillingen **Brug eksisterende arbejde**. Nogle yderligere indstillinger bliver derefter tilgængelige under fanen **Generelt**. Du kan styre adgangen til menupunktet ved at tildele en eller flere arbejdsklasser i oversigtspanelet **Arbejdsklasse**. Arbejdsklasserne definerer det arbejde, som menupunktet kan behandle. Arbejdsklassen kan også bruges til at give adgang til bestemte brugerroller eller til at adskille behandling for forskellige typer operationer. I følgende tabel forklares de indstillinger, der er tilgængelige. Indstillingen kan vælges under feltet **Ledet af** på siden **Menupunkter i mobilenhed**. 

<table>




<thead>
<tr class="header">
<th>Indstilling</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ingen</td>
<td>Denne standardværdi behandler ikke arbejde.</td>
</tr>
<tr class="even">
<td>Systembaseret</td>
<td>Supply Chain Management bestemmer, hvilken type arbejde der tildeles en arbejder, og den rækkefølge, som arbejderen skal udføre arbejdet i. Når du vælger denne indstilling, kan du klikke på <strong>Systembaseret arbejde</strong> i handlingsruden for at åbne siden <strong>Systembaseret sorteringsrækkefølge</strong>, hvor du kan angive sorteringskriterier for arbejdet. Sorteringskriteriet styrer den rækkefølge, som arbejderen skal udføre arbejdet i. Du kan tilføje så mange kriterier, som du behøver.</td>
</tr>
<tr class="odd">
<td>Brugerbaseret</td>
<td>Medarbejderen vælger det arbejde, der skal udføres, og den rækkefølge, det skal udføres i.</td>
</tr>
<tr class="even">
<td>Brugergruppering</td>
<td>Arbejderen grupperer manuelt arbejde. Denne indstilling er f.eks. nyttig, når en arbejder kan plukke flere varer ad gangen på en lokalitet. Når arbejderen har plukket alle de ønskede varer, kan han eller hun lægge varerne på lager.</td>
</tr>
<tr class="odd">
<td>Systemgruppering</td>
<td>Supply Chain Management grupperer arbejde for arbejderen, afhængigt af et angivet felt. Plukkearbejde grupperes f.eks., når en arbejder scanner et forsendelses-id, last-id eller en anden værdi, der kan forbinde de enkelte arbejdsenheder. Hvis du vælger denne indstilling, skal følgende felter angives:
<ul>
<li><strong>Systemgrupperingsfelt</strong> – Vælg det felt, som arbejderen scanner for at gruppere arbejdet.</li>
<li><strong>Systemgrupperingslabel</strong> – Indtast tekst for at informere medarbejderen om, hvad der skal scannes, for at gruppere arbejde.</li>
</ul></td>
</tr>
<tr class="even">
<td>Valideret brugerstyret</td>
<td>Medarbejderen vælger det arbejde, der udføres, når arbejdet er knyttet til en større enhed som en last eller forsendelse. Arbejderen bestemmer den rækkefølge, som varerne plukkes i. Hvis du vælger denne indstilling, skal følgende felter angives:
<ul>
<li><strong>Valideret brugerstyret felt</strong> – Vælg det felt, som arbejderen scanner for at gruppere arbejdet.</li>
<li><strong>Valideret brugerstyret label</strong> – Angiv den tekst, der informerer arbejderen om, hvad der skal scannes, når plukkearbejde er grupperet af systemet.</li>
</ul>
Denne indstilling er f.eks. nyttig, når flere paller er klargjort for en last. Hvis du vælger <strong>LoadId</strong> i feltet <strong>Valideret brugerstyret label</strong>, kan arbejderen plukke en hvilken som helst palle, der er knyttet til lasten. Arbejderen modtager en fejlmeddelelse, hvis han eller hun scanner en vare, der ikke er knyttet til lasten.</td>
</tr>
<tr class="odd">
<td>Klyngepluk</td>
<td>Arbejderen grupperer arbejde i klynger. Klynger giver arbejdere mulighed for at plukke varer fra en enkelt lokalitet for flere arbejdsordrer på samme tid.</td>
</tr>
<tr class="even">
<td>Gruppering af cyklusoptælling</td>
<td>Arbejderen vælger en zone, et arbejdsområde eller en lokalitet, og Supply Chain Management tildeler arbejde baseret på valget. Hvis du vælger denne indstilling, kan du også klikke på <strong>Cyklusoptælling</strong> i handlingsruden for at angive yderligere oplysninger, der skal vises, og du kan også angive det antal gange, arbejderen skal gentage optællingen, hvis der konstateres en forskel.</td>
</tr>
 <tr class="odd">
<td>Lastning af transport</td>
<td>Denne funktion tillader flere lagermedarbejdere at laste lageret fra de samme eller forskellige laster på den samme lastbil med laster, der er helt eller delvist leveret.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Yderligere indstillinger for menupunkter
Der er flere tilgængelige indstillinger til menupunkter på siden **Menupunkter i mobilenhed**. Indstillingerne varierer, afhængigt af den proces som du konfigurerer for menupunktet. 

Indstillingerne er beskrevet i følgende tabel.

<table>




<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tillad opdeling af arbejde</td>
<td>Vælg denne indstilling for at give brugerne mulighed for at lægge varer for en arbejdsordre i mere end ét destinations-id. Denne indstilling er f.eks. nyttig, når et destinations-id er fuldt, og arbejderen skal tilføje de resterende varer i et andet id. Arbejderen kan klikke på <strong>Fuld</strong> for at angive, at id'et er fuldt, og stoppe med at modtage plukkearbejde for det. Læg på lager-lokaliteten for de plukkede varer vises derefter, og plukkearbejdet, der allerede er udført, flyttes til en ny arbejdsordre. Det resterende plukkearbejde destinations-id'et forbliver på den oprindelige arbejdsordre.</td>
</tr>
<tr class="even">
<td>Forankring</td>
<td>Vælg denne indstilling for at give arbejdere mulighed for at angive en lokalitet, der tilsidesætter den foreslåede midlertidige lokalitet eller lastlokaliteten. Alt det resterende læg på lager-arbejde ledes hen til den nye lokalitet. Denne indstilling er f.eks. nyttig, når en arbejder, der skal lægge varer på lager for ordre nr. 1 på en midlertidig lokalitet ved Dock 1, ikke kan, fordi en tidligere last ikke er fjernet fra lokalitet. I stedet for at vente på, at den midlertidige placering for Dock 1 bliver tilgængelig, kan arbejderen beslutte at bruge den midlertidige placering for Dock 2. I givet fald tilsidesætter arbejderen den foreslåede midlertidige placering. Placeringslokaliteten for alle resterende varer for arbejdsordren opdateres derefter til den midlertidige lokalitet på Dock 2. Hvis du vælger denne indstilling, skal du angive feltet <strong>Foretag forankring efter</strong>.</td>
</tr>
<tr class="odd">
<td>Foretag forankring efter</td>
<td>Hvis du bruger forankring, skal du angive, om du vil forankre ved levering eller ved belastning.</td>
</tr>
<tr class="even">
<td>Id for arbejdsrevisionsskabelon</td>
<td>Vælg den skabelon til arbejdsrevision, som skal afbryde arbejdsprocessen for dette menupunkt, så en anden handling kan udføres. Hvis dette menupunkt f.eks. er for indgående arbejde, kan revisionsskabelonen kræve, at arbejderen kontrollerer temperaturen i leveringscontaineren. Det tidspunkt, hvor processen afbrydes, er angivet på revisionsskabelonen. Dette tidspunkt kan f.eks. være, arbejdet sættes i gang eller afsluttes, eller når status ændres.</td>
</tr>
<tr class="odd">
<td>Klyngeprofil-id</td>
<td>Vælg den klyngeprofil, der skal bruges til klyngepluk. Klyngeprofil indeholder indstillinger, f.eks. om der automatisk skal oprettes klynger, navnene på placeringerne og antallet af arbejdsenheder, de kan tildeles, hvornår klynger skal opdeles i individuelle arbejdsenheder, og om bekræftelse er påkrævet. Dette felt er kun tilgængeligt, hvis <strong>Klyngepluk</strong> er valgt i feltet <strong>Ledet af</strong>.</td>
</tr>
<tr class="even">
<td>Optæl først det samlede vareantal</td>
<td>Vælg denne indstilling for at kræve, at en arbejder skal tælle det samlede antal først under en optælling. Hvis der konstateres en forskel, skal arbejderen angive yderligere oplysninger, som id-nummer, batchnummer og serienumre.</td>
</tr>
<tr class="odd">
<td>Opret bevægelse</td>
<td>Markér denne indstilling for at give en arbejder mulighed for at oprette arbejde for en bevægelse, men uden at arbejderen skal udføre arbejdet med det samme. Denne indstilling er f.eks. nyttig, hvis der er udført kvalitetskontrol, og inspektøren ønsker, at varen skal flyttes fra området til kvalitetskontrol.</td>
</tr>
<tr class="even">
<td>Vejledningskode</td>
<td>Hvis du vil bruge en bestemt lokalitetsvejledning, skal du vælge den vejledningskode, der er tilknyttet lokalitetsvejledningen. Dette felt er tilgængeligt, når du opretter arbejde, og processen for oprettelsen af arbejde er <strong>Bevægelse efter skabelon</strong>.</td>
</tr>
<tr class="odd">
<td>Deaktiver cyklusoptællingsgrænser</td>
<td>Markér denne indstilling for at ignorere cyklusoptællingsgrænserne. Hvis du markerer denne indstilling, oprettes der ikke cyklusoptællingsarbejde, når grænseværdierne overskrides.</td>
</tr>
<tr class="even">
<td>Få vist batchdispositionskode</td>
<td>Vælg denne indstilling for at få vist batchdispositionskoder. Du kan f.eks. få vist batchdispositionskoder, når du modtager en returneret batch. Arbejdere kan derefter vurdere status for eller kvaliteten af en batch og vælge den relevante kode. Reglerne for batchdispositionskoden bestemmer, om batchen vil være tilgængelig for andre lagerprocesser. Hvis du ikke vælger denne indstilling, bruges en af følgende batchdispositionskoder:
<ul>
<li>Hvis du modtager et nyt batchnummer, bruges den standard batchdispositionskode, der er angivet i varemodelgruppen.</li>
<li>Den batchdispositionskode, der allerede er tildelt til batchen, bruges.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vis dispositionskode</td>
<td>Vælg denne indstilling for at få vist dispositionskoder. Du kan f.eks. få vist dispositionskoder, når du modtager returvarer. Arbejdere kan derefter vurdere status for eller kvaliteten af varerne og vælge den relevante kode. Reglerne for dispositionskoden bestemmer, om varerne vil være tilgængelige for andre lagerprocesser.</td>
</tr>
<tr class="even">
<td>Vis lagerstatus</td>
<td>Markér denne indstilling for at få vist status for varer på lager. Denne indstilling er tilgængelig for alle menupunkter, der bruger eksisterende arbejde, undtagen cyklusoptælling.</td>
</tr>
<tr class="odd">
<td>Vis oversigt over plukskærm</td>
<td>Markér denne indstilling for kun at få vist en oversigt over plukkearbejde for den valgte arbejdsordre. Oversigten vises, indtil den første arbejdslinje er behandlet for arbejdsordren.</td>
</tr>
<tr class="even">
<td>Generér nummerplade</td>
<td>Markér denne indstilling for at generere et entydigt id-nummer baseret på den valgte nummerserie. Du kan f.eks. generere et id-nummer for varer, der modtages for indkøbsordrer.</td>
</tr>
<tr class="odd">
<td>Gruppér vareplacering</td>
<td>Markér denne indstilling for at gruppere læg på lager-arbejdet. Denne indstilling er tilgængelig, når arbejdet er grupperet af arbejderen eller af Supply Chain Management. Når arbejderen er færdig med alt plukkearbejdet i gruppen, oprettes der læg på lager-arbejde for den samme gruppe</td>
</tr>
<tr class="even">
<td>Lagerreguleringstyper</td>
<td>Vælg den lagerreguleringstype, der bestemmer, hvilken lageroptællingskladde der bruges til at bogføre reguleringen, og om der skal fjernes reservationer. Dette felt er kun tilgængeligt for processerne <strong>Regulering ind</strong> eller <strong>Regulering ud</strong> til oprettelse af arbejde.</td>
</tr>
<tr class="odd">
<td>Tilsidesæt batchnummer</td>
<td>Markér denne indstilling for at give arbejdere, der rapporterer en mængde som færdig for en produktionsordre, mulighed for at indføre et batchnummer, der adskiller sig fra det batchnummer, der er knyttet til produktionsordren.</td>
</tr>
<tr class="even">
<td>Tilsidesæt mål-id</td>
<td>Vælg denne indstilling for at give arbejdere mulighed for at angive et destinations-id-nummer, der er forskellig fra det foreslåede destinations-id-nummer. Brug denne indstilling, når det første pluk for en arbejdsordre er for hele mængden af en vare med id-nummeret. Denne indstilling er f.eks. nyttigt ved genbrug af en palle.</td>
</tr>
<tr class="odd">
<td>Pluk og pak</td>
<td>Vælg denne indstilling for at give arbejdere mulighed for at kombinere arbejde for en salgsordre eller en last i en enkelt arbejdsenhed. En arbejder kan kun udføre arbejde for salgsordren eller lasten. Denne indstilling er f.eks. nyttigt, når du skal øge et antal for en salgsordre, efter at last, levering og arbejde er oprettet for salgsordren. Denne indstilling er tilgængelig, når menupunktet bruger eksisterende arbejde, og arbejdet er videreført af brugeren eller systemet.</td>
</tr>
<tr class="even">
<td>Pluk den ældste batch</td>
<td>Angiv, om arbejderen skal plukke den ældste batch på en lokalitet først. Følgende valgmuligheder er tilgængelige:
<ul>
<li><strong>Ingen</strong> – Arbejderen kan plukke en hvilken som helst batch på lokaliteten. Arbejderen får ingen meddelelse.</li>
<li><strong>Advar</strong> – Arbejderen kan plukke en hvilken som helst batch på lokaliteten, men der vises en advarsel, hvis en batch ikke er den ældste.</li>
<li><strong>Gennemtving</strong> – Arbejderen skal plukke den ældste batch på lokaliteten. Arbejderen modtager en fejlmeddelelse, hvis en batch ikke er den ældste batch. <strong>Bemærk!</strong> Denne indstilling er kun relevant, hvis <strong>Batchnummer</strong> er lavere end <strong>Lokalitet</strong> i det reservationshierarki, der er knyttet til varen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Udskriv label</td>
<td>Markér denne indstilling for at tillade, at arbejdere udskriver id-numre.</td>
</tr>
<tr class="even">
<td>Systemgrupperingsfelt</td>
<td>Markér det felt, der bestemmer, hvordan Supply Chain Management grupperer plukkearbejde for arbejdere. Hvis du f.eks. vælger feltet <strong>ShipmentId</strong>, scanner arbejderen forsendelses-id for at gruppere plukkearbejdet. Alt arbejde for forsendelsen knyttes derefter til arbejderen. Dette felt kræver, at du opretter et menupunkt, der bruger eksisterende arbejde, der er grupperet af systemet. Du skal også skrive tekst i feltet <strong>Systemgrupperingslabel</strong> for at informere medarbejderen om, hvad der skal scannes.</td>
</tr>
<tr class="odd">
<td>Systemgrupperingslabel</td>
<td>Skriv den tekst, der informerer arbejderen om, hvad der skal scannes, når plukkearbejde er grupperet af Supply Chain Management. Hvis du f.eks. bruger feltet <strong>ShipmentId</strong> til at gruppere plukkearbejde efter forsendelse, kan du skrive <strong>Forsendelses-id</strong> i feltet. Dette felt kræver, at du opretter et menupunkt, der bruger eksisterende arbejde, der er grupperet af systemet. Du skal også vælge det felt, der skal grupperes efter, i feltet <strong>Systemgrupperingsfelt</strong>.</td>
</tr>
<tr class="even">
<td>Brug standarddata</td>
<td>Vælg denne indstilling for at aktivere knappen <strong>Standarddata</strong> i handlingsrunden, hvor du kan vælge felter, der viser de data, som en arbejder typisk skal bruge i det daglige arbejde. Denne indstilling er f.eks. nyttig, hvis en arbejder ofte plukker varer fra samme lokalitet. Du kan vælge feltet <strong>Fra lokalitet</strong> for at få vist lokaliteten som standard.</td>
</tr>
<tr class="odd">
<td>Valideret brugerstyret felt</td>
<td>Vælg det felt, som arbejderen scanner for at gruppere arbejdet. Hvis du f.eks. vælger <strong>LoadId</strong>, kan en arbejder vælge ethvert arbejde, der er tilknyttet en valgt last. Du skal også skrive tekst i feltet <strong>Valideret brugerstyret label</strong> for at informere medarbejderen om, hvad der skal scannes.</td>
</tr>
<tr class="even">
<td>Valideret brugerstyret label</td>
<td>Angiv den tekst, der informerer arbejderen om, hvad der skal scannes, når plukkearbejde er grupperet af et valideret brugerstyret felt. Hvis du f.eks. bruger feltet <strong>LoadId</strong> til at gruppere plukkearbejde efter last, kan du skrive <strong>Last-id</strong> i feltet.</td>
</tr>
<tr class="odd">
<td>Kode for arbejdsskabelon</td>
<td>Vælg den arbejdsskabelon, der skal oprette arbejdet for en proces. Hvis du f.eks. modtager en vare for en indkøbsordre, oprettes læg på lager-arbejdet baseret på arbejdsskabelonen. Hvis du ikke vælger en arbejdsskabelon, tildeler Supply Chain Management en skabelon baseret på forespørgselskriterier. Yderligere oplysninger om arbejdsskabeloner finder du under <a href="control-warehouse-location-directives.md">Styre lagerarbejde med arbejdsskabeloner og lokalitetsdirektiver</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Kræv, at arbejdere bekræfter produkt, lokalitet eller antal, når de plukker varer
Du kan konfigurere arbejdsbekræftelser, der kræver, at en arbejder bruger en mobilenhed til at registrere lokaliteten eller antallet, når han eller hun udfører arbejde på lagerstedet. Arbejdsbekræftelser hjælper med at sikre, at arbejderen er på den korrekte lokalitet eller håndterer det korrekte antal varer. Du kan også aktivere Supply Chain Management for at bekræfte arbejderens registrering automatisk. Hvis du aktiverer automatisk bekræftelse, kan du ikke også kræve bekræftelser for lokalitet eller antal. Arbejdsbekræftelser inkluderer også produkter og produktvarianter. Derudover kan du registrere bekræftelser ved at scanne en stregkode. For at bekræfte produkter og produktvarianter skal du angive et id for produktet eller produktvarianten. Dette id kan være produkt-id, produktsøgnings-id, eksternt id, GTIN eller stregkode. Når du angiver id'et eller scanner stregkoden, vises dimensionerne for produktvarianten på mobilenheden. 

I følgende tabel beskrives de forskellige arbejdstyper, som du kan bruge sammen med arbejdsbekræftelser.

| Indstilling                 | Beskrivelse                                                                |
|------------------------|----------------------------------------------------------------------------|
| Pluk                   | Kræv bekræftelse ved pluk af varer.                                |
| Læg på lager                    | Kræv bekræftelse, når du lægger varer på en lokalitet.                     |
| Optælling               | Kræv bekræftelse under cyklusoptælling.                                |
| Reguleringer            | Kræv bekræftelse, når du justerer lagerantal.               |
| Brugerdefineret_                 | Kræv bekræftelse for brugerdefinerede arbejde.                                      |
| Karantæne             | Kræv bekræftelse, når du flytter varer til karantæne.                   |
| Id-opbygning | Kræv bekræftelse, når du konsoliderer varerne for at opbygge et id. |
| Udskriv                  | Kræv bekræftelse, når du udskriver id-numre.                |
| Statusændring          | Kræv bekræftelse, når status for lageret ændres.              |

**Bemærk!** Du kan kun kræve bekræftelse af produkt for arbejdstyperne pluk og læg på lager.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Konfigurere et menupunkt på en mobilenhed til at udføre arbejde af typen indkøbsordre](tasks/set-up-mobile-device-menu.md)

[Konfigurere et menupunkt for mobilenheden til registrering af modtagne varer](tasks/set-up-mobile-device-menu-item-register-received-items.md)

[Lagerstatusser](../inventory/inventory-statuses.md)


