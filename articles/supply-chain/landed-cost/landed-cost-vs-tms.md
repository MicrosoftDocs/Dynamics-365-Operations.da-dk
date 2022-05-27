---
title: Landingsomkostninger sammenlignet med Transportstyring
description: Microsoft Dynamics 365 Supply Chain Management leverer to forskellige moduler til arbejdet med transport, Transportstyring (TMS) og landingsomkostninger. I dette emne opsummeres de funktioner, som de to moduler har til fælles, og der fremhæver forskellene mellem dem.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8c59d7d1887986d308cb591ece077cff9f4648a5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690366"
---
# <a name="landed-cost-vs-transportation-management"></a>Landingsomkostninger sammenlignet med Transportstyring

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management leverer to forskellige moduler til arbejdet med transport: **Transportstyring** (TMS) og **Landingsomkostninger**. I dette emne opsummeres de funktioner, som de to moduler har til fælles, og der fremhæver forskellene mellem dem. Du kan bruge disse oplysninger til at afgøre, hvilket modul der passer bedst til din forretningspraksis. Det kan være, at nogle forretningsmetoder fungerer bedre med TMS, mens andre fungerer bedst med landingsomkostninger. Derefter kan du vælge at bruge ét modul eksklusivt, afhængigt af dine forretningsbehov, eller du kan kombinere de to moduler.

Dette emne er ikke en omfattende gennemgang af alle funktionerne i modulerne. I stedet fremhæves den tilgængelige funktionalitet i forbindelse med transport af varer fra en leverandør til din virksomheds lagersted, hvor de kan forbruges.

## <a name="terminology-reference-data-and-reporting-differences"></a>Terminologi, referencedata og rapporteringsforskelle

### <a name="terminology-comparison"></a>Sammenligning af terminologi

TMS og landingsomkostninger bruger forskellige begreber for lignende begreber. I følgende tabel opsummeres disse begreber og deres anvendelse i de to moduler.

| TMS-begreb | Begreb for landingsomkostninger | Bemærkninger |
|----------|------------------|-------|
| **Last**<p>En *last* er en samling forsendelser, der transporteres samtidigt i samme transportenhed (f.eks. en lastbil eller et skib). Laster kan enten være indgående eller udgående.</p> | **Fragt**<p>Typisk er *fragt* et enkelt fartøj, der er ude på en enkelt *rejse*. En fragt kan indeholde flere *forsendelsescontainere*, og den kan også omfatte indgående ordrer fra forskellige juridiske enheder i din organisation. Fragter kan kun være indgående.</p> | TMS bruger også begrebet *fragtnummer*, der henviser til et informationsfelt, hvor du kan angive en identifikator. Der er dog ikke knyttet nogen funktioner til TMS-feltet, og det er ikke knyttet til begrebet *fragt* i landingsomkostninger. |
| **Rute**<p>En *rute* er den fysiske sti for en transport fra oprindelsessted til destination.</p> | **Rejse**<p>En *rejse* er den fysiske sti for en transport fra oprindelsessted til destination. Hver fragt skal tilknyttes en rejse.</p> | |
| **Rutesegmenter**<p>En rute kan have flere *rutesegmenter*, som hver især repræsenterer et trin på rejsen. En rute kan omfatte flere fragtmænd eller tjenester, som hver især betragtes som et rutesegment.</p> | **Etaper**<p>En rejse kan have flere *etaper*, som hver især repræsenterer et trin på rejsen. En etape kan være en del af transport, håndtering af afgifter eller en anden aktivitet.</p> | |
| **Containere**<p>En *container* kan være en hvilken som helst slags pakke eller emballage, der bruges af TMS.</p> | **Forsendelsescontainere**<p>En *forsendelsescontainer* er en bogstavelig, fysisk forsendelsescontainer, som den kendes fra containerskibe.</p> | |
| **Varekoder**<p>I TMS (og andre steder i Supply Chain Management) identificerer *varekoder* forskellige varetyper. De kan påvirke tariffer, håndteringen af farlige materialer osv.</p> | **Varekoder**<p>I landingsomkostninger oprettes *varekoder* på niveauet for den juridiske enhed. De bruges mest til rapportering.</p> | Landingsomkostninger kan også bruge de varekoder, der bruges til TMS og andre steder i Supply Chain Management. Varekoderne for landingsomkostninger bruges dog kun af landingsomkostninger. |

### <a name="some-reference-data-isnt-shared"></a>Nogle referencedata deles ikke

TMS og landingsomkostninger deler ikke referencedata for enheder som f.eks. omkostningsopsætning, rejser og etaper. Hvis du bruger begge moduler, skal du genoprette de ikke-delte referencedata.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Interne rapporter fungerer ikke med varer undervejs

Følgende rapporter fungerer ikke sammen med funktionen for varer undervejs, som landingsomkostninger gør:

- [Rapport over interne varer undervejs i alt](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Rapport over interne varer undervejs i alt](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

I disse rapporter antages det, at varer er undervejs, så snart du udsteder en salgsfølgeseddel, og at de overføres til lageret fra transit ved modtagelse. Varer undervejs behandles dog ikke på denne måde. Hvis du bruger varerne undervejs og funktionerne for intern handel sammen, vil resultatet af begge disse rapporter derfor være forkerte.

## <a name="using-the-two-modules-together"></a>Brug af de to moduler sammen

Du kan bruge TMS til både indgående og udgående operationer. Selvom landingsomkostninger har de fleste af de samme grundlæggende funktioner som TMS til indgående operationer, tilføjer den også visse funktioner. Derfor kan du overveje at bruge TMS til udgående operationer og landingsomkostninger til indgående operationer.

Generelt anbefales det ikke, at du bruger begge moduler til indgående operationer. Du skal bruge det modul, der opfylder dine behov bedst. Hvis du bruger de to moduler sammen, må du ikke dele kildedokumenter mellem dem. Du må f.eks. ikke bruge samme indkøbsordre til både en last i TMS og en fragt i landingsomkostninger. Du skal især sikre dig, at du ikke konfigurerer systemet til automatisk at oprette indgående last. Hvis varer fra indkøbsordrer indgår i en fragt, kan de ikke håndteres som en del af en last.

## <a name="goods-in-transit"></a>Varer undervejs

Et af de primære funktioner i landingsomkostninger er muligheden for at behandle varer undervejs. Behandlingen af varer undervejs giver dig mulighed for at tage økonomisk ejerskab af afsendte varer, før de fysisk modtages på destinationslagerstedet. Varer undervejs skal ofte behandles i forbindelse med international handel.

### <a name="tms-goods-in-transit-features"></a>TMS-funktioner til varer undervejs

TMS understøtter i øjeblikket ikke behandling af varer undervejs.

### <a name="landed-cost-goods-in-transit-features"></a>Funktioner for varer undervejs i landingsomkostninger

Behandling af varer undervejs er en primær funktion i landingsomkostninger og indeholder følgende funktioner:

- **Lagersteder for varer undervejs** – Et lagersted for varer undervejs kan knyttes til hvert lagersted i Supply Chain Management. Varer overføres til lagersteder for varer undervejs, når den oprindelige indkøbsordre faktureres. Varer, der fysisk reserveres, bliver først disponible til forbrug, når de modtages på deres fysiske lagersted. Du kan derfor tage økonomisk ejerskab over varer ved at fakturere indkøbsordren.
- **Finanskonto for varer undervejs** – Landingsomkostninger føjer en bestemt finansposteringskonto til posteringsprofilen for indkøbsordren til behandling af varer undervejs. Denne finanskonto for varer undervejs fungerer som en konto af typen "varer, der er faktureret, men ikke modtaget". Når den oprindelige indkøbsordre faktureres, og ordrer for varer undervejs oprettes, bogføres omkostningen for den direkte indkøbsordre på finanskontoen for varer undervejs, indtil varerne modtages på deres endelige fysiske lokation.
- **Opdateringer af sporingskontrol** – Ordrer for varer undervejs understøtter sporingskontrolfunktionen i landingsomkostninger. Sporingskontrol giver dig mulighed for at opdatere den forventede ankomstdato for varer, mens de er undervejs. Sporingskontrol opdaterer derefter fragten og de tilknyttede indkøbsordrelinjer. Den forventede leveringsdato er derefter tilgængelig for varedisponering og logistik.
- **Udløser af over-/undertransaktioner** – Hvis der forekommer en afvigelse mellem de forventede varer på en fragtlinje og de faktiske varer, der modtages på lagerstedet, løser landingsomkostningen det ved at oprette over- og/eller undertransaktioner. Du kan derefter administrere disse transaktioner på baggrund af den måde, du vil behandle dem på, enten via en indkøbsordre eller en bevægelseskladde. Over- og undertransaktionerne udgør et link tilbage til fragten, den oprindelige indkøbsordre og den nye bevægelseskladde eller indkøbsordre for afvigelsen.
- **Ordrer for varer undervejs** – Landingsomkostninger introducerer et nyt kildedokument, der kaldes en *ordre for varer undervejs*. En ordre for varer undervejs giver dig mulighed for at fakturere den oprindelige indkøbsordre for at tage økonomisk ejerskab af varerne. Når indkøbsordren faktureres, oprettes det nye kildedokument for hver indkøbsordrelinje, der har en kombination af lagerdimensioner. Varerne flyttes derefter fysisk til et lagersted for varer undervejs, hvor de fysisk reserveres mod varerne i transitordren og ikke kan forbruges, medmindre der modtages ordrer for varer undervejs.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Diverse gebyrer og forsendelsesomkostninger

Et af de vigtigste aspekter ved forsendelse og forsendelsesstyring af varer er at anerkende de indirekte omkostninger, der er knyttet til forsendelser. Disse indirekte omkostninger er ikke de direkte lageromkostninger, der er tilknyttet en indkøbsordre og en forsendelse eller fragt. I stedet er de ekstraomkostninger, der introduceres af arten af varebevægelserne fra leverandøren til din organisation. Disse omkostninger kan omfatte fragtomkostninger, der er knyttet til forsendelse af varer fra en fysisk lokalitet til en anden, eller toldafgifter, der er knyttet til import af varer fra en udenlandsk leverandør.

Landingsomkostninger håndterer disse omkostninger ved at oprette en ny type omkostningsstruktur, der kaldes *automatiske omkostninger*. TMS håndterer disse omkostninger ved hjælp af gebyrfunktionen.

### <a name="tms-charge-and-cost-features"></a>TMS-funktioner for gebyrer og omkostninger

TMS bruger diverse gebyrer til at administrere ekstraomkostninger for laster, der tildeles de relaterede kildedokumentlinjer. Disse diverse gebyrer kan angives på niveauet for enten indkøbsordrelinjen eller indkøbsordrehovedet.

I TMS kan diverse gebyrer fordeles eller inddeles efter vægt, volumen eller antal på lageret. Gebyrer kan inddeles i fragt- eller tillægsgebyrer. Der kræves yderligere udvikling for at kunne anvende flere fordelingsmetoder i TMS.

### <a name="landed-cost-charge-and-cost-features"></a>Funktioner i landingsomkostninger for gebyrer og omkostninger

Landingsomkostninger indeholder et sæt omkostningsfunktioner, der håndterer de ekstra omkostninger, der er knyttet til forsendelse af varer. Disse omkostninger kaldes automatiske omkostninger, og de anvendes på tidspunktet for den første forsendelsesfakturering ved hjælp af det forkalkulerede omkostningsbeløb. Hver omkostningstype administreres i sin egen postering. Når de faktiske fakturaer for indirekte omkostninger er bogført, opdateres de forkalkulerede omkostninger automatisk, så de afspejler de faktiske omkostninger.

Desuden kan de indirekte omkostninger, der er knyttet til forsendelse af varer, faktureres under fragten fra oprindelseshavnen, eller når varerne er modtaget. Denne egenskab giver større fleksibilitet i forbrug af varer.

I følgende liste skitseres nogle begreber med hensyn til gebyr- og omkostningsfunktioner i landingsomkostninger:

- **Omkostningsområde** – Omkostninger og gebyrer kan tildeles forskellige niveauer, eller *omkostningsområder*, afhængigt af fragten. Omkostningen kan anvendes på fragtniveau og opdeles for hver vare i fragten. Derudover kan omkostninger anvendes på niveauet for containeren, indkøbsordren, varen eller flytteordren. Hvert omkostningsgebyr kan administreres separat på tværs af de forskellige områder og opdeles i en omkostning pr. vare.
- **Fordelingsmetoder** – Der findes flere fordelingsmetoder i landingsomkostninger. Omkostningsgebyrer kan fordeles efter antal, beløb, værdi, vægt, volumen, mål eller et brugerdefineret volumenmål.
- **Kontrol af clearing/afvigelse** – Omkostningsgebyrer konfigureres som deres egen omkostningskodetype i landingsomkostninger. Hver omkostningskodetype giver dig mulighed for at definere en clearingkonto for forkalkulerede omkostningsgebyrer samt konti til periodiserings- og indkøbsprisafvigelse for afvigelser i estimerede omkostninger i forhold til faktiske omkostninger. Når de estimerede omkostninger først bogføres, krediteres clearingkontoen. Når de faktiske fakturaer er bogført, bogføres de faktiske kostbeløb, og de forkalkulerede omkostninger debiteres på clearingkontoen.

## <a name="matching-freight-bills-and-invoices"></a>Afstemning af fragtbreve og fakturaer

### <a name="tms-bill-and-invoice-matching-features"></a>TMS-funktioner til sammenholdelse af fragtbrev og faktura

TMS kan matche fragtbreve, der indeholder forkalkulerede omkostninger og fakturaer, med de faktiske fragtomkostninger. Fakturaer kan modtages enten elektronisk eller på papir. Matchning af afvigelse mellem de forkalkulerede omkostninger og faktiske omkostninger påvirker ikke lagervurderingen.

Du kan finde flere oplysninger i [Afstemme fragt i transportstyring](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Funktioner i landingsomkostninger til sammenholdelse af fragtbrev og faktura

Landingsomkostninger kan matche fragtbreve med estimerede omkostningsgebyrer og kan fakturere de faktiske omkostningsgebyrer til de forkalkulerede omkostninger. På faktureringstidspunktet findes fragtgebyrer i en fakturakladde, og de forkalkulerede omkostninger fjernes fra clearingkontoen. Desuden bogføres de faktiske kostgebyrer i forhold til vareforbrug for varen sammen med afvigelserne mellem de estimerede gebyrer og de faktiske gebyrer. Denne funktionalitet giver mulighed for fleksibilitet i faktureringsprocessen.

## <a name="tracking"></a>Sporing

Et vigtigt element i både TMS og landingsomkostninger er muligheden for at spore varer og identificere, hvor de er på rejsen fra oprindelsesstedet til det endelige destinationslagersted. Sporing giver dig mulighed for at følge og opdatere, hvor varerne befinder sig, og hvornår de forventes at ankomme til lagerstedet til forbrug. Ud over varernes status under rejsen angiver landingsomkostninger forventede og faktiske datoer for hvert trin i rejsen.

### <a name="tms-tracking-features"></a>TMS-sporingsfunktioner

TMS indeholder begrænsede funktioner til sporing af indgående laster. Den viser datoer og gør det muligt at opbygge en integration for at finde den nøjagtige position (f.eks. på siden **Transportstatus**).

For hvert rutesegment kan du angive estimerede tidsplaner og modtagelsestider.

### <a name="landed-cost-tracking-features"></a>Funktioner til sporing i landingsomkostninger

Landingsomkostninger kan give sporingskontrol for hver fragt fra oprindelseshavnen til den endelige destination. Sporingskontrol angiver statussen for fragten. Statussen angiver, om fragten sejler, er i toldinspektion eller i lokal levering på vej til det endelige lagersted. Status kan angives på niveauet for indkøbsordrelinjen, containeren og fragthovedet. Du har derfor mere detaljeret kontrol.

Der er desuden knyttet en bekræftet forventet dato, der er baseret på angivne leveringstider, til hvert trin af en rejse. De bekræftede og forventede leveringsdatoer føjes til indkøbsordrelinjen og varer i transitordrer og kan bruges til varedisponering og logistik. Ud over de forventede datoer kan de faktiske datoer opdateres. De efterfølgende trin i en rejse opdateres derefter tilsvarende.

## <a name="multi-leg-journeys"></a>Rejser med flere etaper

Rejsebegrebet identificerer, hvor varerne er i processen, og bestemmer varernes status, mens de er undervejs. Varerne kan gennemgå flere forskellige etaper på en rejse, og du kan knytte forskellige omkostninger til et bestemt etape. Det kan f.eks. være en fragtomkostning for skibsfragt og lokale transportomkostninger for transport af varerne fra havnen til destinationen.

### <a name="tms-multi-leg-journey-features"></a>TMS-funktioner til rejse i flere etaper

I TMS kan ruter opdeles i rutesegmenter, der repræsenterer rejser i flere etaper. TMS kan fordele spotsatser og tillægsgebyrer til de enkelte rutesegmenter.

Du kan finde flere oplysninger i [Planlægge fragttransportruter med flere stop](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Funktioner i landingsomkostninger til rejse i flere etaper

Landingsomkostninger har en ramme til flytning af varer fra oprindelsesstedet til destinationen via en række etaper, som er stop eller trin i en rejse. Etaperne kombineres for at oprette rejseskabeloner, der fastlægger, hvordan varerne flyttes fra leverandøren til din organisation.

På hver etape af rejsen kan du yderligere definere statussen for hver indkøbsordrelinje og de leveringstider, der er knyttet til den. Den kombinerede leveringstid for alle disse etaper bruges til at identificere den forventede leveringsdato. Behandling af varer undervejs er dog påkrævet, hvis rejse i flere etaper skal anvendes. Varernes fragtrejse administreres i en tabel, der er specifik for landingsomkostninger.

## <a name="receiving-by-container"></a>Modtagelse af container

Det kan være vigtigt at håndtere, hvordan varer fordeles og opbevares i et fartøj. Det er en god ide at opbevare varerne i én container eller flere containere i et fartøj. Når der modtages varer, modtages de i containere, og der kan ske modtagelse af forskellige containere på forskellige tidspunkter eller på forskellige datoer.

Både TMS og landingsomkostninger giver mulighed for at administrere varemodtagelsen i en container. TMS bruger begrebet last til at administrere de varer, indkøbsordrer og flytteordrer, der er knyttet til en forsendelsescontainer. TMS understøtter modtagelse på basis af en emballagestruktur, der modtages via en ASN (Advance Shipping Notice). Landingsomkostninger bruger begrebet forsendelsescontainere til behandling af indkøbsordrer og styring af indirekte omkostninger, der er tilknyttet en container på et fartøj.

### <a name="tms-receiving-by-container-features"></a>TMS-funktioner til modtagelse af container

TMS understøtter indgående ASN'er, alle modtagelsesvarianter via mobilappen Lokationsstyring og alle modtagelsesmetoder via Supply Chain Management-klienten.

### <a name="landed-cost-receiving-by-container-features"></a>Funktioner i landingsomkostninger til modtagelse af container

For at understøtte modtagelse af container opretter landingsomkostninger forsendelsescontainerposter og knytter indkøbsordrer til en bestemt forsendelsescontainer ved hjælp af container-id'et. Indirekte omkostninger kan derefter anvendes på den pågældende forsendelsescontainer og fordeles, så de er knyttet til de relevante indkøbsordrer.

Containere i landingsomkostninger kan modtages via en ny type tilgang, der kaldes en *kvittering for varer undervejs*, via modtagelseskladder eller via modtagelse i mobilenhed. Når der bruges modtagelseskladder, kan antal initialiseres fra ordren for varerne undervejs eller fra de oprindelige indkøbsordrelinjer i containeren. Landingsomkostninger omfatter to arbejdstyper til modtagelse via mobilappen Lokationsstyring.

Landingsomkostninger angiver ikke ASN for den elektroniske varemodtagelse. Derudover understøtter den ikke flow i mobilappen Lokationsstyring, der behandler lastmodtagelse, modtagelse af nummerplader eller modtagelse af en blandet nummerplade.

## <a name="rate-shopping-by-vendor"></a>Indhentning og visning af forsendelsessatser efter leverandør

Med indhentning og visning af forsendelsessatser kan et firma vælge en transportleverandør ud fra den laveste pris, den hurtigste rute eller en kombination af begge dele.

### <a name="tms-rate-shopping-features"></a>Tms-funktioner til indhentning og visning af forsendelsessatser

TMS giver dig mulighed for at identificere leverandør- og ruteløsninger til indgående og udgående ordrer. For eksempel kan du identificere den hurtigste rute eller den billigste sats for en forsendelse.

TMS understøtter optimering af fuld indhentning og visning af forsendelsessatser og fragt via satsrutepanelet, fleksible rangeringsindstillinger via rangeringsprogrammet, en API til integration med eksterne parter og understøttelse af volumenvægt.

Du kan finde flere oplysninger i [Programmer til transportstyring](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Funktioner i landingsomkostninger til indhentning og visning af forsendelsessatser

Landingsomkostninger giver kun begrænset understøttelse af indhentning og visning af forsendelsessatser efter leverandør. Selvom du kan angive speditørværdier, sammenligner Landingsomkostninger dem ikke på tværs af flere leverandører.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Chaufførens ind- og udtjekning med planlægning af aftale

Med chaufførens ind- og udtjekning kan systemet overvåge modtagelser og forhindre trængsel ved laststationerne.

### <a name="tms-driver-check-incheck-out-features"></a>TMS-funktioner til chaufførs ind- og udtjekning

TMS giver dig mulighed for at oprette *aftaler*. En aftale repræsenterer hændelser, der indtræffer på en dok til modtagelse af en indkøbsordre, levering af en salgsordre eller behandling af en indgående eller udgående last på en bestemt dato og klokkeslæt. Aftaler sikrer, at dokke er ledige til pålæsning og aflæsning af varer, og de forhindrer situationer, hvor flere fragtmænd ankommer til en lokation på samme tid.

Systemet understøtter, at chauffører kan tjekke ind ved en bestemt dokport.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Funktioner i landingsomkostninger til chaufførs ind- og udtjekning

Landingsomkostninger kan lagre estimater for den dato og det klokkeslæt, hvor en container bliver leveret.

## <a name="transfer-orders-and-additional-costs"></a>Flytteordrer og yderligere omkostninger

Virksomheder skal ofte kunne overføre varer mellem lagersteder. Når denne type overførsel indtræffer, er der knyttet omkostninger til den, og du ønsker måske at registrere disse omkostninger. I Landingsomkostninger kan flytteordrer føjes til en fragt eller et fartøj for at spore varebevægelser fra ét lagersted eller sted til et andet, estimere leveringstiden og den forventede leveringsdato og føje indirekte omkostninger til flytningen af varer.

### <a name="tms-transfer-order-cost-features"></a>TMS-funktioner til omkostninger for flytteordrer

TMS understøtter oprettelse af fragtgebyrer, der er tilknyttet flytninger. Selvom disse gebyrer kan ses fra flytteordren, føjes landingsomkostningerne ikke til vareomkostningerne. Fragtafstemning understøttes ved oprettelse af et fragtbrev, der er baseret på disse gebyrer. Dette fragtbrev sammenholdes derefter med en kreditorfragtfaktura.

### <a name="landed-cost-transfer-order-cost-features"></a>Funktioner i landingsomkostninger for flytteordrer

I landingsomkostninger kan du føje flytteordrer til en fragt eller et fartøj. På denne måde kan du føje forsendelsesomkostninger til fragten som lagerudligninger på tidspunktet for modtagelse af flytteordren. De indirekte omkostninger kan faktureres for de faktiske omkostninger og spores i forhold til en fragt for at opdatere vareforbruget. Selvom flytteordrer ikke bruger varer behandling af varer undervejs i standardfrigivelsen, kan de føjes til fragt. Landingsomkostningerne lægges til de samlede omkostninger for hver vare.