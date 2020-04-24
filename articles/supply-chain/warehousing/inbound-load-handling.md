---
title: Lagerekspedition af indgående laster for indkøbsordrer
description: I dette emne beskrives lagerekspeditionsprocessen for indgående laster for indkøbsordrer.
author: omulvad
manager: AnnBe
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 709a75a259b1f8daa5b72e76b56942573c403f43
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261312"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Lagerekspedition af indgående laster for indkøbsordrer

I dette emne beskrives lagerekspeditionsprocessen for indgående laster for indkøbsordrer.

For hver indgående last skal systemet allerede indeholde en relateret salgsordre, og det kan også indeholde en relateret lastspecifikation og/eller transportplan. Du kan få flere oplysninger om, hvordan du opretter og administrerer indgående laster, i [Forretningsproces: Planlægge transport for indgående laster](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Oversigt: Sådan opretter, registrerer og modtager du indgående laster

I følgende illustration vises det typiske flow for håndtering af indgående laster, der har indkøbsordreantal, når de ankommer til lagerstedet.

![Processen til håndtering af indgående last](media/inbound-process.png "Processen til håndtering af indgående last")

1. **Leverandøren bekræfter indkøbsordren.**

    Processen starter, når der angives en indkøbsordre i systemet og derefter leveres til en leverandør, som bekræfter ordren. Indkøbsordren skal findes, før du kan oprette en indgående lastpost. Du kan dog oprette den indgående last, selvom ordren ikke er bekræftet. Du kan få flere oplysninger i [Godkende og bekræfte indkøbsordrer](../procurement/purchase-order-approval-confirmation.md).

1. **Der oprettes en indgående lastpost, som skal bruges til at planlægge modtagelsen og dens indhold.**

    Posten for indgående last repræsenterer en leverandørforsendelse af en eller flere indkøbsordrer. Lasten forventes at ankomme til lagerstedet som én fysisk transportenhed (f.eks. en truckload). Posten for indgående last bruges til planlægningsformål, og gør det muligt for logistikkoordinatoren at spore status af lasten fra leverandøren. Den bruges også til at registrere ordrelinjeantal og styre status via lagerstedsoperationer, som f.eks. modtagelse og læg-på-lager-arbejde. Laster kan oprettes enten automatisk eller manuelt, og de kan baseres på en indkøbsordre eller en ASN (Advanced Shipment Notice) fra leverandøren. Du kan få flere oplysninger i [Oprette eller redigere en indgående last](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Leverandøren bekræfter lastens afsendelse.**

    Når leverandøren sender lasten, bekræfter logistikkoordinatoren på modtagelseslagerstedet lastforsendelsen. Hvis modtagerfirmaet bruger modulet **Transportstyring**, vil den indgående afsendelsesbekræftelse udløse andre laststyringsprocesser, der er knyttet til indgående laster. Du kan få flere oplysninger i [Bekræfte en last til levering](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **Lasten ankommer til lagerstedet, og arbejdere registrerer antallet.**

    Når en truckload ankommer til lagermodtagelsesområdet, registrerer lagermedarbejderne lastantallet. Når modulet **Lokationsstyring** bruges, udfører arbejdere registreringen ved hjælp af mobilenheder. Du kan få flere oplysninger i [Produktkvittering mod indkøbsordrer – registrering](../procurement/product-receipt-against-purchase-orders.md#registration) og afsnittet [Registrere varer, der ankommer under en indgående last](#register-item-quantities-arriving).

1. **Det registrerede lastantal bogføres i forhold til indkøbsordrer.**

    Når lastantallet er registreret som ankommet, skal dette antal bogføres som produktkvittering i firmaets lagerbeholdning for at registrere den fysiske lagerforøgelse. Du kan finde flere oplysninger i [Produktkvittering mod indkøbsordrer – produktkvittering](../procurement/product-receipt-against-purchase-orders.md#product-receipt) og [Bogføring af registrerede produktantal i forhold til indkøbsordrer](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Registrere vareantallet, der ankommer til en indgående last

Microsoft Dynamics 365 Supply Chain Management understøtter flere driftsmetoder til registrering af bestilte produkter. Derfor kan du konfigurere systemet, så det passer til dine specifikke forretningskrav. I dette afsnit beskrives, hvordan du registrerer antallet af indgående varer ved hjælp af en mobil enhed, når den avancerede lokationsstyring er slået til i systemet. Der er dog en alternativ rute, som er baseret på at bruge varemodtagelseskladden i stedet for en mobil enhed. Du kan få flere oplysninger i [Registrere varer for en vare med aktiveret avanceret lagerstyring ved hjælp af en varemodtagelseskladde](tasks/register-items-advanced-warehousing.md).

Når der først ankommer en indgående last på lagerstedet, skal lagermedarbejderne registrere de vareantal, der er medtaget i forsendelsen. De bruger som regel håndholdte scannere. Denne arbejdsgang er kun tilgængelig, hvis følgende varer findes i systemet:

- **En indgående lastpost, som beskriver de vareantal, der forventes i forsendelsen**

    Leverandøren bekræfter typisk posten for indgående last, før forsendelsen ankommer til lagerstedet. Derfor har lasten en status som _Afsendt_. Lagermedarbejderne kan dog også registrere varernes antal for laster, der har status som _Åben_ eller _Modtaget_.

- **En mobil enheds menu, der er konfigureret til at understøtte modtagelse af last**

    Appen [Dynamics 365 for Finance and Operations – Lagersted](install-configure-warehousing-app.md) til mobile enheder understøtter følgende arbejdsoprettelsesprocesser:

    - Modtagelse af varelast
    - Modtagelse af lagervare og placering på lager
    - Modtagelse af blandet id'er, hvor feltet **Kildedokumentlinjens identifikationsmetode** for den mobile enheds menupunkt er indstillet til _Modtagelse af varelast_. Du kan få flere oplysninger i [Modtagelse af blandede nummerplader](mixed-license-plate-receiving.md).
    - Modtagelse og opbevaring af blandede nummerplader, hvor feltet **Kildedokumentlinjens identifikationsmetode** for den mobile enheds menupunkt er indstillet til _Modtagelse af varelast_. Du kan få flere oplysninger i [Modtagelse af blandede nummerplader](mixed-license-plate-receiving.md).

    > [!NOTE]
    > Uanset hvilken proces der oprettes, genererer systemet arbejde for at tage de antal, der er registreret på modtagelsesstedet, og placere dem på den almindelige lagerplacering. Når processen _Modtagelse af lagervare og placering på lager_ eller _Modtagelse af blandede id'er og placering på lager_ bruges, vil den arbejder, der registrerede lastantallet, også blive instrueret af enheden til at udføre læg-på-lager-arbejdet som del af registreringsopgaven. Modsat processerne _Modtagelse af varelast.._ og _Modtagelse af blandede nummerplader_ vil antagelsen derimod være, at læg-på-lager-arbejdet udføres separat fra registreringsopgaven.

- **En arbejdsskabelon, der definerer pluk og placer-arbejde for indkommende laster**

    Denne vare er relateret til de forrige varer. Du skal have mindst én arbejdsskabelon for arbejdsordretypen _Indkøbsordre_, og den skal indeholde et sæt pluk/placer-arbejdstyper.

Den mobile enhed fører lagerstedets modtagende medarbejder gennem flowet for registrering af lastantallet. Dette flow omfatter som minimum følgende trin for hvert last-id:

1. Angiv last-id'et.
2. Angiv varenummeret for en modtaget vare.
3. Angiv antallet af det varenummer, der er modtaget.
4. Angiv id-nummeret for varens første placering, hvis systemet ikke er konfigureret til at generere dette nummer automatisk.
5. Tryk på **OK**.

Når arbejderen har fuldført disse trin, foretager systemet følgende opdateringer i de relevante enheder, forudsat at indkøbsordrelinjens antal ankom på én last, og alle lastantal er registreret:

| Enhed | Opdateringer | Bemærk! |
|---|---|---|
| Læs | Feltet **Arbejdsoprettet antal** på lastlinjen opdateres, så det registrerede antal vises. | Værdien **Laststatus**forbliver _Leveret_ eller _Åben_, hvis der ikke er kørt en leveringsbekræftelse for lasten. Hvis der er startet mindst én linje med læg-på-lager-arbejdet, ændres den til _Under behandling_. |
| Lagertransaktion for en indkøbsordre, der har tilknyttede lastantal er registreret for |<p>Følgende felter er opdateret:</p><ul><li>Feltet <b>Modtagelse</b> er angivet til <i>Registreret</i>.</li><li>Feltet <b>Sted</b> opdateres med modtagelsesområdets lokationskode. (Denne kode angives i feltet <b>Standardplacering for modtagelse</b> for hvert lagersted.)</li><li>Feltet <b>Id-nummer</b> opdateres med nummeret på det id-nummer, der blev angivet eller genereret under registreringen.</li><li>Feltet <b>Last-id</b> opdateres med nummeret på den last, som antallet er registreret i forhold til. (Se noten.)</li></ul> | Muligheden for at sammenkæde indkøbsordrens lagertransaktion og de antal, der er registreret mod lasten, blev introduceret i version 10.0.9 som en valgfri funktion med navnet _Knyt indkøbsordre lagertransaktioner med last_. Denne funktion er specielt fordelagtig i driftsstrømme, hvor en enkelt ordre af købte varer leveres som flere laster, eller når en last indeholder antal for flere indkøbsordrer. |
| Læg-på-lager | Arbejdet oprettes på baggrund af en arbejdsskabelon for at give arbejderen besked på at flytte de registrerede antal fra det modtagende sted til en almindelig lagerplacering. | Valget af lagerplacering styres af direktivet Læg-på-lagerstedet. Hvis der ikke er defineret et steddirektiv, er læg-på-lager-placeringen i arbejdet tom. |

Bemærk, at lagermedarbejderne kan registrere modtagelsen af en indkøbsordre med en eller flere tilknyttede laster uden at bruge processen _Modtagelse af varelast_. Følgende metoder er tilgængelige:

- **På mobilenheden:** Brug processerne _Indkøbsordrelinje til modtagelse_ og _Indkøbsordrelinje til modtagelse og læg på lager_. (Hvis der findes mere end én last for indkøbsordrelinjeantallet, kan arbejderen ikke bruge processen _Indkøbsordrelinje til modtagelse_. I stedet bliver arbejderen bedt om at bruge den enhedshandling, der er knyttet til processen _Modtagelse af varelast_.)
- **På klienten:** Brug varemodtagelseskladden.
- **På klienten:** Brug handlingen **Registrering**, der kan åbnes fra indkøbsordrelinjen.

> [!NOTE]
> Hvis indkøbsordremodtagelsen registreres vha. en af de foregående metoder, oprettes der ikke en sammenkædning mellem indkøbsordrens lagertransaktion og lasten, også selvom funktionen _Knyt indkøbsordre lagertransaktioner med last_ er aktiveret. En undtagelse fra denne regel er, når du bruger indstillingen **Indkøbsordrelinje til modtagelse** og kun én last har en anden status end _Modtaget_ for ordrelinjen.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Håndtere uoverensstemmelser ved registrering af indgående lastantal

Lagermedarbejdere kan foretage en delvis registrering af lastantallets modtagelse. Hver delvise lastantalsmodtagelse opretter derefter en separat lagertransaktion, der har en modtagelsesstatus som _Registreret_ for det registrerede antal, og parti-id'et henviser til den oprindelige indkøbsordrelinje.

#### <a name="load-under-receiving"></a>Last under modtagelse

Når en last ankommer, og hvis vareantallet er mindre end de antal, der er angivet i lastposten, kan lagermodtagelsesmedarbejdere arbejde direkte i klienten for at bekræfte denne uoverensstemmelse ved at reducere antallet på lastlinjen, så det svarer til det faktiske antal, der er ankommet og registreret.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Overmodtagelse af last

Overmodtagelse sker, når en last ankommer, og vareantallet overstiger det forventede antal for lastlinjen. Du kan styre, om og til hvilken grad af overmodtagelse, der tillades under lasten, registreres.

Brug feltet **Overmodtagelse af last** for de relevante menupunkter i den mobile enhed til at bestemme, hvad der sker, når en lagermedarbejder forsøger at registrere en overlevering. Dette felt er tilgængeligt for menupunkter i den mobile enhed, der bruger følgende typer af processer til arbejdsoprettelse:

- Modtagelse af varelast
- Modtagelse af lagervare og placering på lager
- Modtagelse af blandet nummerplade (hvor feltet **Kildedokumentlinjens identifikationsmetode** er indstillet til _Modtagelse af varelast_)
- Modtagelse af nummerplade og placering på lager (hvor feltet **Kildedokumentlinjens identifikationsmetode** er indstillet til _Modtagelse af varelast_)

I følgende tabel beskrives de indstillinger, der er tilgængelige for feltet **Overmodtagelse af last**.

| Værdi | Beskrivende tekst |
|---|---|
| Tillad | Arbejdere kan registrere modtagelsen af antal, der overstiger det resterende ikke-registrerede antal for en valgt last, men kun hvis det samlede registrerede antal ikke overstiger antallet på den indkøbsordrelinje, der er knyttet til lasten (efter justering for overleveringsprocenten). |
| Blokér | <p>Arbejdere kan registrere modtagelsen af antal, der overstiger det resterende ikke-registrerede antal for en valgt last (efter regulering for overleveringsprocenten). En arbejder, der forsøger at foretage registreringen af modtagelserne, får en fejl og kan ikke fortsætte, før han eller hun registrerer et antal, der er lig med eller mindre end det resterende ikke-registrerede lastantal.</p><p>Værdien af overleveringsprocenten på en lastlinje kopieres som standard fra den tilknyttede indkøbsordrelinje. Når feltet <b>Overmodtagelse af last</b> er angivet til <i>Bloker</i>, bruger systemet værdien af overleveringsprocenten til at beregne det samlede antal, der kan registreres for en lastlinje. Denne værdi kan dog overskrives til individuelle laster efter behov. Denne funktionsmåde bliver relevant under modtagelsesflows, hvor dele eller alt det ekstra antal, der repræsenterer ordrelinjens overleveringsprocent, fordeles forholdsmæssigt over flere laster. Her er et eksempelscenarie:</p><ul><li>Der er flere laster for én indkøbsordrelinje.</li><li>Indkøbsordrelinjen har en overleveringsprocent, der er større end 0 (nul).</li><li>Der er allerede registreret antal i forhold til en eller flere laster, uden at overleveringsprocenten tages i betragtning.</li><li>Overleveringsantallet ankommer til den sidste last.</li></ul><p>I dette scenarie kan en mobil enhed bruges til kun at registrere overskydende antal for den sidste last, hvis lagerchefen øger overleveringsprocenten for den relevante lastlinje fra standardværdien til en værdi, der er stor nok til, at hele overleveringen kan registreres med den endelige last.</p> |
| Blokér kun for lukkede laster | Arbejdere kan modtage for meget lastlinjeantal til åbne laster, men ikke for laster, der har status som _Modtaget_. |

> [!NOTE]
> Standardværdien for feltet **Overmodtagelse af last** er _Tilladt_. Når denne værdi bruges, matcher funktionaliteten den standardfunktionsmåde, der var tilgængelig, før funktionen _Overmodtagelse af lastantal_ blev introduceret i version 10.0.11.

### <a name="put-away-the-registered-quantities"></a>Lægge de registrerede antal på lager

Når registreringen er fuldført på mobilenheden, opdaterer handlingen _Registrering af antallets modtagelse_ lagerbeholdnings- og lagerposter for at angive, at antallene nu er på modtagerens lagersted og er tilgængelige til reservation. Et firmas lageroperationer kræver dog typisk, at antallet flyttes fra modtagelsesområdet til det almindelige lager, så de efterfølgende plukprocesser kan finde sted. Instruktioner til læg-på-lager-aktiviteten hentes i det læg-på-lager-arbejde, der oprettes automatisk, når den indgående last registreres som modtaget.

Når lagermedarbejderen har fuldført læg-på-lager-arbejdet, registrerer og sporer systemet resultatet ved at opdatere flere enheder, som det er opsummeret i følgende tabel.

| Enhed | Opdateringer | Bemærk! |
|---|---|---|
| Læs | <p>Følgende felter er opdateret:</p><ul><li>Værdien <b>Laststatus</b> ændres til <i>Under behandling</i>.</li><li>Værdien <b>Arbejdsstatus</b> ændres til <i>100,00 % udført arbejde</i>.</li></ul> | Værdien **Laststatus** ændres til _Under behandling_, når arbejderen starter læg-på-lager-opgaven for mindst én linje af læg-på-lager-arbejde. |
| Lagertransaktioner for arbejde, som tilknyttede antal er lagt på lager for | Felterne **Modtagelse** og **Sted** og andre relevante felter opdateres for at afspejle bevægelsen fra det modtagende sted til lagerstedet. | Værdien **Modtagelsestilstand** for indkøbsordrens lagertransaktionen forbliver _Registreret_. |
| Læg-på-lager | Værdien **Arbejdsstatus** er ændret til _Lukket_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Bogfør de efterregistrerede antal i forhold til indkøbsordrer

Når indgående produktantal er registreret i systemet, bliver de tilgængelige for reservation i forbindelse med salg og andre udgående og interne operationer. Systemet opdaterer dog ikke (midlertidige) lagerkonti. Denne opdatering kan kun udføres, når Operations-teamet bogfører de registrerede produktkvitteringer.

Hvis medlemmer af Operations-teamet vil åbne en side, hvor de kan bogføre en produktkvittering, kan de følge _et_ af disse trin:

- Åbn den relevante lastpost, og vælg derefter handlingen **Produktkvittering**.
- Gå til **Lokationsstyring \> Periodiske opgaver \> Opdater produktkvitteringer**, og angiv derefter den last, der skal bogføres, i feltet **Last-id**.
- Åbn den relevante indkøbsordre, og vælg derefter handlingen **Produktkvittering**.
- Gå til **Indkøb og forsyning \> Indkøbsordrer \> Modtage produkter \> Konterer produktkvittering**.

Handlingen **Produktkvittering**, der er tilgængelig på siden **Last** (og på den tilsvarende side for opdateringsjobbet, siden **Opdater produktkvitteringer**), kan kun opdatere mængder for produktkvitteringer på indkøbsordreantal, der har status som _Registreret_. Handlingen **Produktkvittering**, der er tilgængelig på siden **Indkøbsordre**, kan imidlertid inkludere antal i begge behandlingsstatusser (_Bestilt_ og _Registreret_). Den kan også styre omfanget af bogføringen af produktkvitteringen vha. yderligere parametre, f.eks. _Modtagelse nu-antal_ og _Registreret antal og tjenester_.

Det er kun ordrer med statussen _Bekræftet_, der kan være produktkvitteringsbogført. For indkøbsordrer, der ikke er bekræftet, vises handlingen **Produktkvittering** som værende ikke tilgængelig.

### <a name="post-registered-quantities-from-the-load-page"></a>Bogfør registrerede antal fra siden Last

Til produktkvitteringsbogførte registrerede antal fra siden **Last**, skal følgende forudsætninger være gældende:

- Lasten skal have mindst én antals enhed, der har status _Registreret_.
- Lastens status skal være _Afsendt_.
- Den indkøbsordre, der er knyttet til lasten, skal have status _Bekræftet_.

> [!NOTE]
> Hvis lastens status ikke er angivet til _Afsendt_, vil systemet automatisk bekræfte lasten, før opdateringen af produktkvitteringen køres. (Lastens status angives til _Afsendt_, når en bruger registrerer lastens indkommende forsendelse.)

Til produktkvitteringsbogføring af de indkomne registreringer, der er knyttet til en valgt last, vælger medarbejderen handlingen **Produktkvittering** på siden **Last**. Den side, der åbnes, har følgende vigtige oplysninger:

- Feltet **Antal** i sektionen **Parametre** under fanen **Indstillinger** viser det _registrerede antal_. Der er ingen andre indstillinger her.
- I gitteret på panelet **Oversigt** vises alle de indkøbsordrer, der er medtaget i den valgte last.
- I gitteret på panelet **Linjer** vises alle de ordrelinjer, der har et registreret antal.

> [!NOTE]
> Antallet af ordrelinjer, der vises under fanen **Linje**, beregnes forskelligt, afhængigt af om funktionen _Tillad, at flere produktkvitteringer pr. last_ er tilgængelig og slået til i din version af Supply Chain Management.
>
> | Version | Udregning |
> |---|---|
> | Versioner før version 10.0.10 og nyere versioner, hvor funktionen _Tillad, at flere produktkvitteringer pr. last_ ikke er slået til | Linjeantallet er det samlede antal af registrerede antal _for den pågældende indkøbsordrelinje_, uanset om registreringen blev foretaget over flere laster uafhængigt af lasten, fra en mobil enhed eller fra klienten. |
> | Version 10.0.10 og nyere versioner, hvor funktionen _Tillad, at flere produktkvitteringer pr. last_ ikke er slået til | Linjeantallet er det samlede beløb for alle registrerede antal _for den lastpost_, som handlingen **Produktkvitteringsbogføring** blev startet fra. |

Når brugeren vælger **OK** til at bekræfte produktkvitteringsbogføringen, udfører systemet følgende nøgleopdateringer på de relevante enheder.

| Enhed | Opdateringer |
|---|---|
| Lagertransaktion på den indkøbsordre, som der er medtaget linjeantal for i posteringsområdet | <p>Følgende felter opdateres (Bemærk, at der også er flere andre opdateringer):</p><ul><li>Feltet <b>Modtagelse</b> er angivet til <i>Modtaget</i>.</li><li>Feltet <b>Fysisk dato</b> opdateres med bogføringsdatoen.</li></ul> |
| Last, som brugeren bogførte produktkvitteringen fra | Opdateringer af laster afhænger af den anvendte version og indstillingen af feltet **Tillad flere produktkvitteringer pr. last**. Reglerne er beskrevet i den tabel, der vises senere i dette afsnit. |

I feltet **Tillad flere produktkvitteringer pr. last** kan virksomheder vælge en politik for indgående last. Afhængigt af deres driftsstrømme kan virksomheder vælge at tillade eller ikke acceptere flere produktkvitteringsbogføringer for samme last. Det anbefales, at logistikchefen har angivet feltet **Tillad flere produktkvitteringer pr. last** til en af følgende værdier:

- **Nej** – Vælg denne værdi, hvis lagermodtagelsesassistenten altid registrerer alle ordreantal, der ankommer til hver last inden for en angivet tidsramme. Hvis der ikke registreres lastantal, antager systemet, at de ikke blev modtaget eller ikke var i lasten, og derfor ikke bør betragtes som del af lasten. Den produktkvitteringsbogføring, der køres fra en last, bruger samme antagelse. Ud over produktkvittering – hvis du opdaterer alle registrerede antal (hovedfunktionen), deklarerer den den samlede og lukkede last til yderligere behandling. Hvis det er tilfældet, opdateres alle lastlinjeantal automatisk til de registrerede antal, lastlinjer uden registrerede antal slettes, og status for last ændres til _Modtaget_.
- **Ja** – Vælg denne værdi, hvis lagermodtagelsesassistenter kræver mere tid til at registrere alle de antal, der er ankommet, men i mellemtiden skal du foretage produktkvitteringsbogføring af de antal, der allerede er blevet registreret. I dette tilfælde vil logistikchefen sørge for, at en last er åben, selvom produktkvitteringsbogføringsjobbet er udført, så resterende lastantal kan registreres og produktkvitteringer kan opdateres regelmæssigt til Finans.
- **Prompt** – Vælg denne værdi, hvis praksis for lastmodtagelsen er blandet, og der kræves en beslutning, hver gang der køres en produktkvitteringsbogføring.

I følgende tabel vises en oversigt over effekterne af indstillingen **Tillad flere produktkvitteringer pr. last**.

| Tillad flere produktkvitteringer pr. last | Lastantal | Laststatus | Bemærk! |
|---|---|---|---|
| Når dette felt ikke er tilgængeligt (versioner før 10.0.10) | <p>Lastantallet angives, så det svarer til det registrerede antal.</p><p>Hvis lastantallet opdateres til 0 (nul), hvilket betyder, at der ikke er foretaget nogen registrering, slettes lastlinjen.</p><p>Hvis der ikke er nogen lastlinjer på lasten, slettes lasten.</p> | _Modtaget_ | Hvis der findes flere laster for ordrelinjens registrerede antal, er det kun den status for lasten, som modtagelsen blev bogført fra, der opdateres til _Modtaget_. |
| Ingen | <p>Lastantallet angives, så det svarer til det registrerede antal, der er knyttet til last-id'et.</p><p>Hvis der ikke er registreret noget last-id for lagertransaktionen, svarer funktionsmåden til versioner før 10.0.10.</p> | _Modtaget_ | |
| Ja | Ingen opdateringer | _Modtaget_, hvis det samlede registrerede lastantal er lig med eller større end lastantallet | |
| Ja | Ingen opdateringer | _Afsendt_ eller _Under behandling_, hvis det samlede registrerede lastantal er mindre end lastantallet | |

Når feltet **Laststatus** er indstillet til _Modtaget_, kan der ikke foretages flere produktkvitteringsposteringer for den pågældende last. Arbejderen kan dog registrere det resterende ordreantal i forhold til den modtagne last under følgende betingelser. (Du kan finde flere oplysninger i afsnittet [Last over modtagelse](#load-over-receiving) tidligere i dette emne.)

- Versionen af Supply Chain Management er ældre end version 10.0.11.
- Funktionen _Overmodtagelse af lastantal_ er slået til, og feltet **Overmodtagelse af lastlinjeantal** i menupunktet på den mobile enhed for handlingen Modtagelse af varelast er angivet til _Tillad_.

Til produktkvitteringsbogføringer, som yderligere registrerede lastantal i forhold til en last, der har status som _Modtaget_, skal brugeren udføre bogføringshandlingen fra den tilknyttede indkøbsordre.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Bogfør registrerede antal fra siden Indkøbsordre

Til produktkvitteringsbogføringer af registrerede antal på siden **Indkøbsordre**, fuldfører brugeren følgende opgaver, før han eller hun vælger handlingen **Produktkvittering**:

- Indstil feltet **Antal** i sektionen **Parametre** under fanen **Indstillinger** til _Registreret antal_.
- I feltet **Produktkvittering** skal du angive numrene på de indkøbsordrer, der er medtaget i bogføringen.

> [!NOTE]
> Det linjeantal, som vil blive medtaget i bogføringsområdet, er det samlede antal af registrerede antal for indkøbsordrelinjen, uanset om registreringen af antal blev foretaget over flere laster uafhængigt af lasten, fra en mobil enhed eller fra klienten. Den samme regel gælder, når produktkvitteringsbogføringen køres fra en last, hvis den udføres, hvor feltet **Tillad flere produktkvitteringer pr. last** ikke er tilgængeligt eller ikke er aktiveret.

Når brugeren vælger **OK** til at bekræfte produktkvitteringsbogføringen, udfører systemet følgende nøgleopdateringer på de relevante enheder.

| Enhed | Opdateringer |
|---|---|
| Lagertransaktion på den indkøbsordre, som der er medtaget linjeantal for i posteringsområdet | <p>Følgende felter opdateres (Bemærk, at der også er flere andre opdateringer):</p><ul><li>Feltet <b>Modtagelse</b> er angivet til <i>Modtaget</i>.</li><li>Feltet <b>Fysisk dato</b> opdateres med datoen for produktkvitteringsbogføringen.</li></ul> |
| Læs | Opdateringer til lasten afhænger af, om feltet **Tillad flere produktkvitteringer pr. last** er tilgængeligt og aktiveret. Reglerne er beskrevet i næste tabel. |

I følgende tabel vises en oversigt over effekterne af indstillingen **Tillad flere produktkvitteringer pr. last**.

| Tillad flere produktkvitteringer pr. last | Lastantal | Laststatus | Bemærk! |
|---|---|---|---|
| Når dette felt er deaktiveret eller ikke tilgængeligt (i versioner før 10.0.10) | Ingen opdateringer | Der foretages ingen opdateringer. (Status forbliver _Åben_, _Leveret_ eller _Under behandling_.) | Da produktkvitteringsbogføringen startes fra en indkøbsordre, indeholder opdateringslogikken ikke oplysninger om tilknytningen mellem de registrerede antal i området og de laster, som registreringen blev registreret i. Derfor kan den ikke vælge lasten for statusopdateringen. |
| Aktiv | Ingen opdateringer | <p>En af følgende handlinger sker:</p><ul><li>Status ændres til <i>Modtaget</i>, hvis det samlede modtagne og indkøbte antal af indkøbsordrens lagertransaktioner er større end eller lig med antallet af den last, som de er tilknyttet.</li><li>Status forbliver <i>Åben</i>, <i>Leveret</i>eller <i>Under behandling</i>, hvis den forrige betingelse ikke opfyldes for alle linjerne i lasten.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Vælg den relevante indstilling for produktkvitteringsbogføringen til dine logistik operationer

Som tidligere beskrevet indeholder systemet to indstillinger for produktkvitteringsbogføring. Du kan få adgang til indstillingerne på følgende steder:

- På siden **Last** eller fra menuen **Lokationsstyring \> Periodiske opgaver** som et opdateringsjob
- På siden **Indkøbsordre** eller fra menuen **Indkøb og forsyning \> Indkøbsordrer \> Modtage produkter** som et opdateringsjob

Virksomheder, der bruger laster til at planlægge og administrere transport og lagerhåndtering af deres indgående ordrer, anbefales at bruge følgende funktioner, der er beregnet til at fungere sammen med laster:

- **Modtagelse af varelast**-handlinger på deres lagersteds mobile enheder for at registrere modtagelsen af produktantallet i forhold til lasten
- **Produktkvitteringsbogføring**-handlinger, der startes fra en last, for at opdatere lagerregnskabet

> [!NOTE]
> Andre funktioner til registrering af antal og produktkvitteringsbogføring kan bruges til at understøtte de tilsvarende indgående driftsprocesser. Hvis du imidlertid bruger dem med det samme eller i stedet for de særlige lastfokuserede funktioner, kan du risikere at kompromittere datanøjagtigheden af lastposterne og dermed fjerne af lastens styringsstrømmene.

## <a name="example-scenarios"></a>Eksempelscenarier

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Forbered systemet til at køre eksempelscenarierne

Hvis du vil gennemgå de eksempelscenarier, der er beskrevet i dette afsnit, skal du først sørge for, at alle nødvendige funktioner er aktiveret i systemet. De nødvendige demonstrationsdata skal også være tilgængelige i systemet.

#### <a name="turn-on-the-required-features"></a>Slå de påkrævede funktioner til

Disse scenarier kræver funktionen _Flere produktkvitteringsbogføringer pr. last_ og dens nødvendige funktion. Administratorer kan aktivere disse funktioner ved at følge disse trin.

1. Åbn arbejdsområdet **Administration af funktioner**. (Du kan få flere oplysninger om, hvordan du finder og bruger dette arbejdsområde, i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)

1. Slå funktionen _Knyt indkøbsordre lagertransaktioner med last_ til, som vises på følgende måde:

    - **Modul:** _Lokationsstyring_
    - **Funktionsnavn**_: Knyt indkøbsordre lagertransaktioner med last_

1. Slå funktionen _Flere produktkvitteringsposteringer pr. last_ til, som vises på følgende måde:

    - **Modul:** _Lokationsstyring_
    - **Funktionsnavn**_: Flere produktkvitteringsbogføringer pr. last_

#### <a name="enable-sample-data"></a>Aktivér eksempeldata

Hvis du vil arbejde gennem disse scenarier ved hjælp af de angivne eksempelposter og -værdier, skal du bruge et system, hvor standarddemodataene er installeret. Du skal også vælge den juridiske enhed **USMF**, før du starter.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Tilføj et menupunkt til modtagelse af varelast, når der bruges en mobil enhed

Før lagermodtagelsesassistenter kan bruge en mobil enhed til at registrere indgående lager, der er knyttet til en last, skal du oprette et menupunkt på en mobil enhed til dette formål.

I dette afsnit skal du oprette et menupunkt på den mobil enhed og føje det til en eksisterende menu. En lagermedarbejder kan derefter vælge menupunktet i appen Lagersted.

1. Gå til **Lokationsstyring \> Opsætning \> Mobil enhed \> Menupunkter i mobilenhed**, og kontrollér, at din mobile enheds menu indeholder et menupunkt, der har følgende indstillinger:

    - **Tilstand:**_Arbejde_
    - **Arbejdsoprettelsesproces:** _Modtagelse af varelast_
    - **Generer nummerplade:** _Ja_

    Du kan bruge standardværdierne til de andre indstillinger.

    ![Indstillinger for Menupunkt på mobilenhed](media/inbound-mobile-menu-items.png "Indstillinger for Menupunkt på mobilenhed")

    Du kan få flere oplysninger om, hvordan du konfigurerer menupunkter på mobilenheder, i [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md).

2. Når du har konfigureret menupunktet, skal du gå til **Lokationsstyring \> Opsætning \> Mobil enhed \> Menupunkter i mobilenhed**, og føje det til menustrukturen for dine mobile enheder.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>Eksempelscenarie 1: Registrere en last, hvor nogle varer mangler

Dette scenarie viser, hvordan du registrerer antal for en indgående last, hvor ikke alle de forventede antal er til stede. Derefter vises det, hvordan produktkvitteringen bogføres for indkøbsordren.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Opret en last for at planlægge modtagelsen af en indkøbsordre

I denne procedure skal du oprette en indkøbsordre manuelt og en tilhørende last. Derefter skal du opdatere lasten for at simulere, at den er blevet afsendt fra leverandøren (som opdaterer lastens status). Lagerplanlæggerne kan derefter filtrere laster efter **Laststatus** for at finde forventede indgående laster.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Vælg **Ny**.
1. Angiv feltet **Kreditorkonto** i dialogboksen **Opret indkøbsordre** til _1001_.
1. Vælg **OK** for at lukke dialogboksen og oprette indkøbsordren..
1. Den nye indkøbsordre indeholder allerede en linje under **Indkøbsordrelinjer**. Angiv følgende værdier for denne linje:

    - **Varenummer:** _A0001_
    - **Lagersted:** _24_
    - **Antal:** _10_

1. Vælg **Handlinger \> Bekræft** på fanen **Køb** i handlingsruden. Ordrens status er nu _Bekræftet_.
1. Vælg **Handlinger \> Panelet Lastplanlægning** på fanen **Lagersted** i handlingsruden.
1. På siden **Panelet Lastplanlægning** skal du på fanen **Udbud og efterspørgsel** i handlingsruden vælge **Tilføj \> Til ny last**.
1. I dialogboksen **Tilknytning af lastskabelon** skal du indstille feltet **Lastskabelons-id** til _20' Container_.
1. Vælg **OK** for at lukke dialogboksen og vende tilbage til panelet.
1. Vælg **Last-id** i afsnittet **Laster** for at åbne den netop oprettede last.
1. Gennemse lastoverskriften og linjeoplysningerne, og læg mærke til følgende punkter:

    - Feltet I **Laststatus** i oversigtspanelet **Last** er angivet til _Åben_.
    - I afsnittet **Lastlinjer** er der en enkelt linje, hvor feltet **Antal** er indstillet til _10_, og feltet **Arbejdsoprettet antal** er indstillet til _0_ (nul).

    ![Lastdetaljer](media/inbound-load-details.png "Lastdetaljer")

1. På fanen **Lever og modtag** i handlingsruden skal du vælge **Bekræft \> Indkommende forsendelse**. Bemærk, at **Laststatus** er ændret til _Leveret_.
1. Noter værdien i **Last-id-**, så du kan bruge den i den næste procedure.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Registrere modtagelsen af de antal, der er ankommet ved lasten

Når lasten ankommer til lagermodtagelsesområdet, registrerer den modtagende medarbejder lastantallet på en mobil enhed.

1. Brug din mobile enhed til at logge på lagersted 24. (I standarddemodataene skal du logge på ved at bruge _24_ som bruger-id og _1_ som adgangskode.)
1. Vælg menupunktet _Modtagelse af varelast_, som du har oprettet for dette scenarie.
1. Følg vejledningen til dataindtastning på skærmen for at angive følgende værdier. (Ordren kan variere, afhængigt af den mobile enhed eller emulator, du bruger.)

    - **Last** – Angiv det last-id, du oprettede i den foregående procedure.
    - **Vare** – Angiv _A0001_, som er den vare, der forventes til denne last.
    - **Antal** – Angiv _9_ som det faktiske antal, der findes på lasten. Bemærk, at dette antal er mindre end det forventede antal.

1. Fortsæt med at gå gennem arbejdsgangen, så alle andre felter er tomme eller angivet til standardværdierne, indtil enheden meddeleler dig, at arbejdet er fuldført.

Opgaven til modtagelse af lasten er nu fuldført, og den modtagende medarbejder kan gå videre til den næste opgave. Lagermodtagelsespersonalet vil imidlertid i sidste ende gennemgå lastposten og vil kunne se, at det modtagne antal var mindre end det forventede antal. De vil derefter fuldføre følgende procedure ved hjælp af webklienten.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Find den last, du lige har modtaget, på listen. (Du skal muligvis markere afkrydsningsfeltet **Vis lukket** for at medtage de indgående laster, der har laststatussen _Leveret_.) Vælg derefter linket i kolonnen **Last-id** for at åbne lasten.
1. Bemærk i lastposten, at værdien for **Laststatus** stadig er _Afsendt_, men værdien **Arbejdsoprettet antal** på lastlinjen er ændret til _9_.
1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Find det køb, du netop har modtaget, på listen, og vælg derefter linket i kolonnen **Indkøbsordre** for at åbne ordren.
\
1. På oversigtspanelet **Indkøbsordrelinjer** skal du vælge **Lager \> Vis \> Transaktioner**.
1. Gennemse detaljerne i de to indkøbsordretransaktioner. (Du skal muligvis tilpasse siden **Lagertransaktioner**, for at feltet **Last-id** vises i gitteret). Der vises to transaktioner:

    - Den transaktion, der har en modtagelse i statussen _Registreret_, repræsenterer det registrerings antal på _9_, som er blevet kørt mod en bestemt last, ved hjælp af den mobile enhed. **Last-id** er knyttet til den pågældende transaktion.
    - Den transaktion, der har en modtagelse i statussen _Bestilt_, repræsenterer det resterende ikke-registrerede ordrelinjeantal på _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Produktkvitteringsbogfør de registrerede lastantal i forhold til indkøbsordrer

I denne procedure skal du følge op på produktkvitteringsbogføringer af den lagerbeholdning, du har registreret for en last. Det betyder, at den modtagne lagerbeholdning og dens relaterede omkostninger vil blive føjet til firmaets Finans.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Find den last, du har modtaget, på listen. (Du skal muligvis markere afkrydsningsfeltet **Vis lukket** for at medtage de indgående laster, der har laststatussen _Leveret_.) Vælg derefter linket i kolonnen **Last-id** for at åbne lasten.
1. På fanen **Lever og modtag** i handlingsruden skal du vælge **Modtag \> Produktkvittering**. Klik på **Ja**, hvis du bliver bedt om at bekræfte handlingen.
1. Undersøge gitteret i oversigtspanelet **Linjer**i dialogboksen **Konterer produktkvittering**. Den indkøbsordrelinje, som antallet er registreret for i forhold til den valgte last, burde vises.

    > [!NOTE]
    > I versioner, hvor funktionen _Flere produktkvitteringsbogføringer pr. last_ ikke er tilgængelig eller ikke er aktiveret, vil det standardantal, der vises i gitteret for **Lastlinjer**, være det samlede antal, der er registreret på tværs af alle laster, som er knyttet til indkøbsordrelinjen.

1. Undersøg feltet **Produktkvittering** i gitteret på oversigtspanelet **Oversigt**. Bemærk, at det er indstillet til et tal, der indeholder id'et for den valgte last.
1. Vælg **OK** for at bogføre produktkvitteringen og lukke dialogboksen **Produktkvitteringsbogføring**.
1. Du vender tilbage til lastoplysningerne. Bemærk følgende punkter:

    - Feltet **Laststatus** er nu angivet til _Modtaget_.
    - På lastlinjen er værdien **Antal** for lasten ændret fra _10_ til _9_ stk. for at matche det registrerede antal, men værdien **Arbejdsoprettet antal** forbliver _9_.

Hvis indkøbsteamet ikke forventer, at leverandøren leverer det resterende ordreantal på 1, kan det lukke ordren ved at opdatere linjens leveringsrest til _0_. Hvis det imidlertid ikke er registreret, at det manglende stykke er ankommet på den oprindelige last, kan lagermedarbejderne udføre en af følgende handlinger:

- Registrer antallet i forhold til samme last. I dette tilfælde vil feltet **Laststatus** blive nulstillet til _Leveret_, og værdien for **Arbejdsoprettet antal** opdateres til _10_. Dette valg kan kun vælges i følgende situationer:

    - Funktionen _Overmodtagelse af lastantal_ er ikke tilgængelig eller er ikke aktiveret.
    - Funktionen _Overmodtagelse af lastantal_ er tilgængelig og aktiveret, og feltet **Overmodtagelse af lastlinjeantal** er indstillet til _Tillad_.

- Føj antallet til en ny eller eksisterende last, og behandl det på normal vis.
- Registrer og/eller modtag antallet på en måde, der ikke involverer håndtering af last.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>Eksempelscenarie 2: Registrer antal, der ankommer til flere indgående laster, hvor der mangler nogle varer

I dette scenarie opdeles en indgående forsendelse, der er knyttet til en enkelt indkøbsordrelinje, i to laster. En indkøbsordrelinje kan f.eks. opdeles i flere laster på grund af fysiske lastbegrænsninger i vægt og/eller volumen.

I dette scenarie vises også, hvordan du kan behandle flere produktkvitteringsbogføringer for samme last. Du skal registrere antal, der er et resultat af flere indgående laster, men antallet svarer ikke til de forventede antal. De omkostningsopdateringer, der udføres via produktkvitteringsbogføring, udføres flere gange for den samme last.

#### <a name="set-up-load-receiving-policies"></a>Konfigurere politikker for lastmodtagelse

I denne procedure skal du aktivere flere produktkvitteringsbogføringer fra samme last.

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Under fanen **Laster** skal du angive feltet **Tillad flere produktkvitteringer pr, last**  til _Ja_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Opret to laster for at planlægge modtagelsen af en indkøbsordre

I denne procedure skal du oprette en indkøbsordre og to laster. Derefter skal du manuelt opdatere hver last for at simulere, at den er blevet afsendt af leverandøren (som opdaterer lastens status). Lagerplanlæggerne kan derefter filtrere laster efter **Laststatus** for at finde forventede indgående laster.

Du får også at vide, hvordan du angiver indkøbsordrelinjen, så du kan modtage et antal, der er 20 % mere end det antal, der er angivet for linjen.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Vælg **Ny**.
1. I oversigtspanelet **Leverandør** skal du angive feltet **Kreditorkonto** til _1001_ og derefter vælge **OK**.
1. Din nye indkøbsordre åbnes og indeholder en tom linje i gitteret for **Indkøbsordrelinjer**. Angiv følgende værdier for denne ordrelinje:

    - **Varenummer:** _A0001_
    - **Lagersted:** _24_
    - **Antal:** _10_

1. I oversigtspanelet **Linjedetaljer** under fanen **Levering** skal du angive feltet **Overlevering** til _20_.
1. Vælg **Handlinger \> Bekræft** på fanen **Køb** i handlingsruden. Ordrens status er nu _Bekræftet_.
1. Vælg **Handlinger \> Panelet Lastplanlægning** på fanen **Lagersted** i handlingsruden.
1. På siden **Panelet Lastplanlægning** skal du på fanen **Udbud og efterspørgsel** i handlingsruden vælge **Tilføj \> Til ny last**.
1. I dialogboksen **Tilknytning af lastskabelon** skal du indstille feltet **Lastskabelons-id** til _20' Container_. Under fanen **Detaljer** skal du ændre værdien **Antal** fra _10_ til _5_ for delvist at tilføje indkøbsordrelinjeantallet.
1. Vælg **OK** for at anvende dine indstillinger og dialogboksen.
1. Gentag trin 8 til 10 for at oprette en ekstra last. Denne gang er feltet **Antal** allerede indstillet til _5_.
1. På siden **Panelet Lastplanlægning** i gitteret **Laster** skal du vælge værdien **Last-id** for den første last, du har oprettet. Siden **Lastoplysninger** vises og viser den valgte last. Følg disse trin:

    1. På fanen **Lever og modtag** i handlingsruden skal du vælge **Bekræft \> Indkommende forsendelse**.
    1. Bemærk, at værdien **Laststatus** er ændret til _Leveret_.
    1. Klik på knappen Luk for at vende tilbage siden **Panelet Lastplanlægning**.

1. Gentag det foregående trin for den anden last, du oprettede.
1. Notér de to værdier for **Last-id-**, der vises i gitteret **Laster**.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Registrer delvis modtagelse af de antal, der er ankommet under første last, og bogfør de registrerede lastantal

Når laster ankommer til lagermodtagelsesområdet, registrerer den modtagende medarbejder lastantallet på en mobil enhed. For den registrerede lagerbeholdning, der er knyttet til en last, opdateres kostprisen derefter i virksomhedens Finans ved at bogføre modtagelsen for indkøbsordreproduktet baseret på lasten.

Denne procedure viser, hvordan den modtagende medarbejder vil registrere lastantal på en mobil enhed.

1. Brug din mobile enhed til at logge på lagersted 24. (I standarddemodataene skal du logge på ved at bruge _24_ som bruger-id og _1_ som adgangskode.)
1. Vælg menupunktet _Modtagelse af varelast_, som du har oprettet for dette scenarie.
1. Følg vejledningen til dataindtastning på skærmen for at angive følgende værdier. (Ordren kan variere, afhængigt af den mobile enhed eller emulator, du bruger.)

    - **Last** – Angiv det første last-id, du oprettede i den foregående procedure.
    - **Vare** – Angiv _A0001_, som er den vare, der forventes til denne last.
    - **Antal** – Skriv _3_. Bemærk, at dette antal er mindre end det forventede antal. I dette scenarie skal du forestille dig, at du som modtagende medarbejder ikke har tid til at registrere alle antal for denne last. Senere i denne procedure vil du registrere de resterende stykenheder ved at gentage dette trin og angive feltet **Antal** til _2_.

1. Fortsæt med at gå gennem arbejdsgangen, så alle andre felter er tomme eller angivet til standardværdierne, indtil enheden meddeleler dig, at arbejdet er fuldført.
1. Gå til **Lokationsstyring \> Laster \> Alle laster** i webklienten.
1. Find den last, du netop har modtaget, på listen, og vælg værdien **Last-id-** for at åbne lasten. Bemærk, at værdien for **Laststatus** stadig er _Afsendt_, men værdien **Arbejdsoprettet antal** på lastlinjen er ændret til _3_.
1. På fanen **Lever og modtag** i handlingsruden skal du vælge **Modtag \> Produktkvittering**. Klik på **Ja**, hvis du bliver bedt om at bekræfte handlingen.
1. Gennemse, men undlad at ændre de værdier, der vises, i dialogboksen **Produktkvitteringsbogføring**, og vælg derefter **OK**.
1. Du vender tilbage til siden **Lastoplysninger** for den valgte last. Bemærk følgende punkter:

    - Feltet **Laststatus** er fortsat indstillet til _Afsendt_.
    - På lastlinjen er værdien **Antal** for lasten stadigvæk _5_ stk., hvilket er det oprindelige lastantal, og værdien **Arbejdsoprettet antal** er stadigvæk _3_.

1. Udfør registreringen af det resterende antal i denne last ved at gentage denne procedure. I trin 3 skal du dog angive feltet **Antal** til _2_.

Den modtagende opgave for den første last er nu fuldført. Der er oprettet to produktkvitteringskladder, én for hver af de to opdateringer af produktkvitteringen, som du har kørt.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Registrer modtagelsen af de antal, der er ankommet på den anden last og kontoen for det overleverede antal

I dette scenarie vil den modtagende medarbejder registrere et indgående antal, der overstiger det antal, der findes på lasten. Overmodtagelse vil være tilladt, fordi systemet er konfigureret til at tillade overlevering.

1. Brug din mobile enhed til at logge på lagersted 24. (I standarddemodataene skal du logge på ved at bruge _24_ som bruger-id og _1_ som adgangskode.)
1. Vælg menupunktet _Modtagelse af varelast_, som du har oprettet for dette scenarie.
1. Følg vejledningen til dataindtastning på skærmen for at angive følgende værdier. (Ordren kan variere, afhængigt af den mobile enhed eller emulator, du bruger.)

    - **Last** – Angiv det andet last-id, som du oprettede tidligere.
    - **Vare** – Angiv _A0001_, som er den vare, der forventes til denne last.
    - **Antal** – Angiv _7_, der er det resterende antal, som kreditoren har tilladelse til at levere som en del af det samlede indkøbsordreantal på 12 (hvor 10 er det oprindelige ordreantal, og 2 er det tilladte antal for overlevering på 20 %). Husk, at 5 stk. allerede er registreret i forhold til den første last.

Den anden last er nu opdateret med antallet af 7 og kan være produktkvitteringsopdateret baseret på dette antal.
