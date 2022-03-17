---
title: Skaler enheder i en distribueret hybridtopologi
description: Dette emne indeholder oplysninger om sky- og kantskalaenheder til styring af arbejdsbyrder i produktion og lagersted.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30f455f37b5161878cf9c864b92966aa74da051f
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376176"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>Skaler enheder i en distribueret hybridtopologi

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Skalaenhedsfunktionaliteten for Microsoft Dynamics 365 Supply Chain Management gøres tilgængelig for dig i henhold til de vilkår, der gælder for brugen af tjenesten. Yderligere oplysninger finder du i [Juridiske oplysninger om Microsoft Dynamics](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Når du aktiverer sky- og grænseskalaenheder, bliver du bedt om at bekræfte, at du forstår, at nogle af de data, der er relateret til konfigurationen og behandlingen af sky- og grænseskalaenheder, kan blive gemt i et datacenter, der ligger i USA. Du kan få mere at vide om databehandling af sky- og kantskalaenheder i afsnittet [Databehandling under administration af skalaenheder](#data-processing-management) senere i dette emne.

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>Forslag til kerneværdi for en distribueret hybridtopologi

Firmaer, der arbejder med produktion og distribution, skal kunne køre vigtige forretningsprocesser døgnet rundt uden afbrydelse og med skalering. Distribueret hybridtopologi gør det muligt for virksomheder at køre centrale, kritiske produktions- og lagerprocesser uden afbrydelse, selv når der er lejlighedsvise problemer med netværksforbindelse eller ventetid.

En distribueret hybridtopologi introducerer begrebet *skaleringsenheder*, der giver mulighed for distribution af arbejdsbyrder ved kørsel af shop floor og lagersted mellem forskellige miljøer. Denne funktionalitet kan hjælpe med at forbedre ydeevnen, forhindre afbrydelse af tjenester og maksimere oppetid. Der findes skalaenheder via følgende tilføjelsesprogrammer til dit Supply Chain Management-abonnement:

- Tilføjelsesprogrammet Cloud Scale Unit til Dynamics 365 Supply Chain Management
- Tilføjelsesprogrammet Edge Scale Unit til Dynamics 365 Supply Chain Management

Egenskaber til arbejdsbyrde frigives løbende via trinvise forbedringer.

## <a name="scale-units-and-dedicated-workloads"></a>Skalaenheder og dedikerede arbejdsbyrder

Skalaenheder udvider dit centrale Supply Chain Management-hubmiljø ved at tilføje dedikeret behandlingskapacitet. Skalaenheder kan køre i skyen. Alternativt kan de køre på [kanten](cloud-edge-edge-scale-units-lbd.md), i dit lokale miljø eller din lokale facilitet.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 med skalaenheder.":::

Skalaenheder giver modstandsdygtighed, pålidelighed og skalering for de tildelte arbejdsbyrder. Kantskalaenheder kan midlertidigt afbrydes fra skyens hubmiljø, og arbejderne fortsætter med at arbejde i den tildelte arbejdsbyrde i kanten.

En *arbejdsbyrde* er et defineret sæt forretningsfunktioner, der kan udtages og uddelegeres til en skalaenhed. Selvom arbejdsbyrden for Warehouse Management er frigivet, er arbejdsbyrden for produktionsudførelsen stadig en forhåndsversion.

Du kan konfigurere dit hubmiljø og skyskalaenheder for udvalgte arbejdsbyrder ved hjælp af [portalen til styring af skalaenhed](https://sum.dynamics.com). Du kan også tildele flere arbejdsbyrder pr. skalaenhed. Du kan finde oplysninger om forudsætningerne og begrænsningerne for skalaenheder i skyen i den aktuelle version i afsnittet [Forudsætninger og begrænsninger for enheder i skyen](#cloud-scale-unit-prerequisites) senere i dette emne.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Dedikerede arbejdsbyrdefaciliteter for Warehouse Management i en skalaenhed

Arbejdsbyrden for lokationsstyring giver lagerstedsoperationerne mulighed for at skalere og køre i et robust miljø, hvor du anvender isolerede vedligeholdelsesvinduer. Arbejdsbyrden ved lokationsstyring understøtter de fleste processer i virksomhedshubbens lokationsstyring. Du kan finde flere oplysninger under [Arbejdsbelastninger i forbindelse med Warehouse Management for sky- og edge-skaleringsenheder](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Dedikerede arbejdsbyrdefaciliteter for produktionskørsel i en skalaenhed

Arbejdsbyrden ved produktion giver følgende egenskaber:

- Maskinoperatører og tilsynsførende kan få adgang til den operationelle produktionsplan.
- Maskinoperatører kan holde planen opdateret ved at køre diskrete og procesproduktionsjob.
- Den tilsynsførende kan justere driftsplanen.
- Arbejderne kan få adgang til fremmøde og indstemplings- og udstemplingstid på kanten for at sikre en korrekt beregning af arbejderes løn.

Du kan finde flere oplysninger under [Arbejdsbelastninger i forbindelse med produktionsudførelse for sky- og edge-skaleringsenheder](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Overvejelser, før du aktiverer distribueret hybridtopologi for Supply Chain Management

Når du aktiverer den distribuerede hybridtopologi, skifter du dit skymiljø i Supply Chain Management, så det fungerer som en hub. Du kan også tilknytte yderligere miljøer, der er konfigureret som skalaenheder i skyen eller på kanten.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Forudsætninger og begrænsninger for skyskalaenheder

I den aktuelle version af skalaenheder er nogle egenskaber endnu ikke tilgængelige, men de tilføjes måske i trinvise frigivelser over tid.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Du skal være licenskunde hos Supply Chain Management

Hvis du vil onboarde den distribuerede topologi, skal du have en licens til Supply Chain Management. Dit eksisterende skymiljø bliver hubben i din hybridtopologi. Du kan erklære både sandkassemiljøer og produktionsmiljøer som hubmiljøer, og du kan tilføje skalaenheder i overensstemmelse med de tilføjelsesprogrammer, du anskaffer.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Dit eksisterende projekt skal administreres via den globale handelsversion af LCS

Dit eksisterende Microsoft Dynamics Lifecyle Services-projekt (LCS) skal opfylde følgende versionskrav:

- Projektet skal administreres via den globale handelsversion af LCS på [lcs.dynamics.com](https://lcs.dynamics.com).
- Lokale versioner af LCS (f.eks. [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) og [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) understøttes ikke.
- Offentlige myndigheders skyversioner af LCS understøttes ikke.
- Mooncake-versionen af LCS understøttes ikke.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Dit aktuelle produktionsmiljø skal være af typen Selvbetjening i LCS

Dit aktuelle produktionsmiljø skal være mærket med typen **Selvbetjening** i LCS. Denne type angiver, at lejeren af dit LCS-projekt allerede er konverteret, så den understøtter Azure Service Fabric-værtmodellen.

> [!IMPORTANT]
> Miljøtyper, der kører som infrastruktur som en tjeneste (IaaS), understøttes ikke. Disse miljøer mærkes typisk med typen **Microsoft-administreret** i LCS. Hvis du har miljøer af denne type, kan du samarbejde med din Microsoft-kontakt for at forstå migreringstidslinjen for typen **Selvbetjening**.

Microsoft er ved at skifte alle skymiljøer i Supply Chain Management fra en IaaS-model til en topologi, der har Service Fabric som vært. Denne flytning giver bedre skalerbarhed og gør servicestyring lettere. Derfor er implementerings- og vedligeholdelsesoperationerne hurtigere. På samme måde overføres tjenestekomponenter til begrebet mikroservice, og værtsmodellen for tjenesten [skifter](/virtualization/windowscontainers/about/containers-vs-vm) fra en virtuel maskine-model (VM) til en letvægtscontaineriseret arkitektur.

I sidste ende vil den samme Service Fabric-baserede containeriserede serviceinfrastruktur styrke både sky- og kantforekomster af tjenesten, uanset om en forekomst er en hub i skyen eller en skalaenhed i skyen eller på kantet.

Før du kan onboarde i den hybridtopologi, der understøtter skalaenheder, skal projektlejeren skiftes til værtsmodellen i Service Fabric. Desuden skal alle miljøer, der fungerer som hub, konverteres.

> [!TIP]
> Hvis du vil forespørge om status for din LCS-projektlejer, skal du finde miljøtypen i [LCS](https://lcs.dynamics.com/) eller kontakte din partner eller Microsoft-kontakt.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Lokale forretningsdatamiljøer (i det lokale miljø) understøttes ikke som hubs til skalaenheder

Lokale miljøer kan ikke fungere som hubs til skalaenheder. Hubmiljøer skal altid have en vært i skyen.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Egenskaberne for styring af skalaenheder er begrænsede

Administrationsfunktioner, der kan hjælpe med flytning af arbejdsbyrder, er begrænsede. Nogle styringshandlinger understøttes ikke på en selvbetjeningsmåde, og du skal muligvis anmode om support via din partner eller Microsoft-kontakt. Eksempler på dette er visse flytninger af arbejdsbyrden mellem skalaenheder og midlertidige ad hoc-flytninger i katastrofescenarier.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Målepunkter og mål er endnu ikke tilgængelige

Målepunkter og mål, der kan hjælpe dig med at vælge det bedste program til dine skalaenheder, er endnu ikke tilgængelige. Samarbejd med din Microsoft-kontakt eller implementeringspartner for at vælge det mest fordelagtige program.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Behandling af data under administration af skalaenheder

Når du aktiverer dit Dynamics 365-miljø for at understøtte den distribuerede hybridtopologi for sky- og kantskalaenheder, vil visse administrationstjenester kun have en vært i USA på samme måde som for LCS. Denne funktionsmåde påvirker overførsel og lagring af visse administrative og konfigurationsmæssige oplysninger, der bruges af [portalen til styring af skalaenhed](https://sum.dynamics.com). Her er nogle eksempler:

- Dine lejernavne og id'er
- Dine LCS-projekt-id'ere
- Mailadresser til administrator og projektejer, der bruges til at logge på
- Miljø-id'er for hubben og skalaenheder
- Konfigurationer af arbejdsbyrder, herunder navne og fysiske adresser på juridiske enheder og faciliteter, så topologien kan vises på et geografisk kort
- Indsamlede målepunkter (f.eks. ventetid og gennemløb), der vil blive vist på kortanalysesiden for at hjælpe dig med at vælge den mest fordelagtige brug af skalaenhederne

Data, der overføres til og gemmes i de amerikanske datacentre, slettes i henhold til Microsofts politikker for dataopbevaring. Beskyttelse af personlige oplysninger er vigtig for Microsoft. Du kan få mere at vide ved at læse vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Onboarde til den distribuerede hybridtopologi for Supply Chain Management

### <a name="try-out-the-distributed-hybrid-topology"></a>Afprøve distribueret hybridtopologi

Processen for onboarding til distribueret hybridtopologi har to stadier. I første stadie skal du [afprøve](cloud-edge-try-out.md) løsningen og validere dine tilpasninger for at sikre, at de fungerer i den distribuerede topologi, der har skalaenheder. (Du kan bruge eksisterende udviklingsmiljøer til at udføre valideringen). Derefter kan du fortsætte til anden fase, hvor du anskaffer produktionsmiljøer.

## <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Vælge din LCS-projektlejer og den detaljerede onboardingproces

Skalaenheder tilbydes i flere lagerenheder (SKU'er) og prisfastsættelsesindstillinger. Du kan derfor vælge den indstilling, der bedst opfylder dine planlagte månedlige krav til transaktionsvolumen og ydeevne.

> [!TIP]
> Hvis du vil identificere den størrelse, der passer bedst til dine behov, skal du samarbejde med din implementeringspartner og Microsoft om at forstå den månedlige transaktionsstørrelse, som du har brug for.

Startniveau-SKU'en kaldes *Grundlæggende*, og den mere ydende SKU kaldes *Standard*. Hver SKU er forudindlæst med et bestemt antal månedlige transaktioner. Du kan dog øge det månedlige transaktionsbudget ved at tilføje tilføjelsesprogrammer til overforbrug for hver SKU.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Tilføjelsesprogrammer til skyskalaenheder.":::

> [!NOTE]
> Tilføjelsesprogrammer med skalaenhed er ikke kombineret med et begrænset antal brugere. De er tilgængelige for alle brugere i dit eksisterende abonnement (forudsat, at administratoren har tildelt de nødvendige brugerroller til dem).

Købet af hvert tilføjelsesprogram til skalaenhed giver dig ikke kun en månedlig transaktionsvolumen, men giver dig også mulighed for at bruge et bestemt antal miljøpladser i LCS. For hvert Cloud Scale Unit-tilføjelsesprogram er du berettiget til én ny produktionsplads og én ny sandkasseplads. Under onboarding-processen tilføjes et nyt LCS-projekt med disse pladser. Brugsrettighederne til pladserne er bundet, så pladserne skal bruges som skalaenheder, der har en skyhub.

Tilføjelsesprogrammer til overforbrug berettiger dig ikke til nye pladser.

Hvis du vil have flere sandkassemiljøer, kan du købe ekstra almindelige sandkassepladser. Microsoft kan derefter hjælpe dig med at aktivere disse pladser som sandkasseskalaenheder for hybridtopologien.


Når du er færdig med at planlægge, hvordan du vil onboarde til den distribuerede hybridtopologi for Supply Chain Management, skal du bruge [portalen til styring af skalaenhed](https://aka.ms/SCMSUM) til at starte onboardingprocessen. Vælg fanen **Dynamics 365-lejere** i portalen. Den viser listen over de lejere, som din konto er en del af, og hvor du er ejer eller miljøadministrator for et LCS-projekt.

Hvis den lejer, du søger efter, ikke findes på denne liste, skal du gå til [LCS](https://lcs.dynamics.com/v2) og sørge for, at du enten er miljøadministrator eller projektejer af LCS-projektet for den pågældende lejer. Det er kun Azure Active Directory-konti (Azure AD) fra den valgte lejer, der er godkendt til at fuldføre tilmeldingen.

> [!NOTE]
> Når du har anvendt ændringer på LCS, kan det tage op til 30 minutter, før listen over lejere afspejler ændringerne.

For hver lejer vises onboardingstatus på listen.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Liste over lejere under fanen Dynamics 365-lejere.":::

Vælg **Klik her for at komme i gang** for at anmode om onboarding for LCS-lejeren. Du skal acceptere betingelserne. Du skal også angive en forretningsmailadresse, hvor Microsoft kan sende kommunikation, der er relateret til onboardingprocessen.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Indsende tilmelding for en lejer.":::

Microsoft vil gennemgå din anmodning og give dig besked om de næste trin ved at sende en mail til den adresse, du har angivet i tilmeldingsformularen. Microsoft vil arbejde tæt sammen med dig om at aktivere skalaenheder i hybridtopologien for dit forretningsscenarie.

Når onboarding er fuldført, kan du bruge porten til at konfigurere skalaenheder og arbejdsbyrder.

### <a name="manage-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Administrere skalaenheder og arbejdsbyrder ved hjælp af portalen til styring af skalaenhed

Gå til [portalen til styring af skalaenhed](https://aka.ms/SCMSUM), og log på ved hjælp af din lejerkonto. På siden **Konfigurer skalaenheder** kan du tilføje et hubmiljø, hvis det ikke allerede står på listen. Derefter kan du vælge den hub, du vil konfigurere med skalaenheder og arbejdsbelastninger.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Portalen til styring af skalaenhed, siden Konfigurer skalaenheder.":::

Hvis du vil tilføje en eller flere skalaenheder, der er tilgængelige i dine abonnementer, skal du vælge **Tilføj skalaenheder**.

Under fanen **Definerede arbejdsbyrder** skal du bruge knappen **Opret arbejdsbyrde** til at føje en arbejdsbyrde for Warehouse Management i en af skalaenhederne. For hver arbejdsbyrde skal du angive konteksten for de processer, der skal ejes af arbejdsbyrden. For arbejdsbyrder til Warehouse Management er konteksten et specifikt lagersted på en bestemt lokation og juridisk enhed.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Dialogboksen Definer arbejdsbyrder.":::

#### <a name="manage-workloads"></a><a name="manage-workloads"></a>Administrere arbejdsbyrder

Når en eller flere arbejdsbyrder er aktiveret, kan du bruge indstillingen **Administrer arbejdsbyrder** til at starte og administrere processer som dem, der er angivet i følgende tabel.

| Behandling | Beskrivelse |
|---|---|
| Afbryd kommunikation med skalaenhed midlertidigt | Afbryd pipeline-meddelelser midlertidigt mellem hub og en skalaenhed. Denne proces stopper kommunikationen og dræner datapipelinen mellem hub og skalaenheder. Du skal køre denne proces, før du kører en Supply Chain Management-servicehandling på enten hub eller skalaenheden, men du kan også bruge denne i andre situationer. |
| Fortsæt kommunikation med skalaenhed | Fortsæt pipeline-meddelelser mellem hub og en skalaenhed. Du skal f.eks. bruge denne proces, når du har kørt en serviceringshandling i Supply Chain Management på enten hub eller skalaenhed. |
| Opgrader arbejdsbyrder | Synkroniser nye funktioner mellem arbejdsbyrder i hub og skalaenhed. Du skal f.eks. bruge denne proces, når servicering har bevirket, at forespørgslerne til dataudveksling er ændret, og/eller har føjet nye tabeller eller felter til arbejdsbyrden. |
| Overfør arbejdsbyrder til en skalaenhed | Planlæg en arbejdsbyrde, der aktuelt kører i hub, og som skal flyttes til en skalaenhed. Når denne proces køres, flyder synkroniseringen af data, og både hub og skalaenhed indstilles til at skifte ejer af arbejdsbyrden. |
| Overfør skalaenhed til hub | Planlæg en arbejdsbyrde, der aktuelt kører på en skalaenhed, så den flyttes til hub. Når denne proces køres, flyder synkroniseringen af data, og både hub og skalaenhed indstilles til at skifte ejer af arbejdsbyrden.
| Nødoverførsel til hub | <p>Overfør straks en eksisterende arbejdsbyrde til hub. *Denne proces vil kun ændre ejerskabet af de data, der i øjeblikket er tilgængelige i hubben.*</p><p><strong>Advarsel:</strong> Denne proces kan medføre tab af data for ikke-synkroniserede data og fejl i forretningsprocessen. Den skal derfor kun bruges i nødstilfælde, hvor forretningsprocesser skal behandles i hubben, da skalaenheden har en afbrydelse, der ikke kan afhjælpes inden for en rimelig tid.</p> |
| Nedluk distribueret topologi | Fjern en skaleringsenhedsinstallation, og kør kun i hubben uden behandling af arbejdsbyrder. |

:::image type="content" source="media/sum-manage-workloads.png" alt-text="Skalaenhed og arbejdsbyrdestyring.":::

> [!TIP]
> Med tiden føjes der trinvise forbedringer til erfaringen med styring af skalaenhed, så det bliver nemmere at udføre styring af livscyklussen. De specifikke egenskaber for den aktuelle version er dokumenteret i en vejledning til onboarding, som er tilgængelig for kunder, der er i gang med onboarding til den distribuerede hybridtopologi for Supply Chain Management. <!-- KFM: Add a link to the handbook when it is published -->

## <a name="feature-management-considerations-for-workloads"></a>Overvejelser i forbindelse med funktionsstyring af arbejdsbyrder

Dette afsnit indeholder en forklaring på nogle vigtige aspekter, som du skal overveje, når du installerer arbejdsbyrder, tilføjer funktioner eller fjerner funktioner i en distribueret udrulning af hybridtopologi. Flere scenarier kan have indflydelse på, om du skal køre en [opgradering af arbejdsbyrden](#manage-workloads), efter at du har foretaget ændringer. Det skal du dog normalt gøre, når du opdaterer eller tilføjer nye dataudvekslingsforespørgsler, og/eller når du føjer nye tabeller eller felter til en tidligere installeret arbejdsbyrde.

### <a name="mandatory-features-for-installing-a-workload"></a>Obligatoriske funktioner til installation af arbejdsbyrde

Når du installerer en arbejdsbyrde, opretter installationsprocessen en definition af arbejdsbyrde, der indeholder oplysninger om de datatabeller, der bruges, når data synkroniseres mellem de to udrulninger. Oprettelsen af en definition af arbejdsbyrde håndteres automatisk på basis af de funktioner, der aktuelt er aktiveret i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Følgende tabel indeholder de funktioner, der skal aktiveres for at generere de arbejdsbyrdedefinitioner, der kræves for at køre et lagersted eller en produktionsbelastning.

| Obligatorisk funktion | Arbejdsbyrde |
|---|---|
| Automatisk tildeling af GUID'er i WHS-brugeroprettelse | Lagersted |
| Blokering af arbejde i hele organisationen | Lagersted |
| Etiketdetaljer om forsendelsesbølge | Lagersted |
| Understøttelse af skalaenhed på arbejdslister for lagerstedsapp | Lagersted |
| Produktionsudførelse | Fremstillingsvirksomhed |

Når du implementerer en arbejdsbyrde ved at bruge [værktøjer til udrulning af skalaenheden til udviklingsmiljøer med én boks](https://github.com/microsoft/SCMScaleUnitDevTools) eller [portalen til styring af skalaenhed](https://sum.dynamics.com), aktiveres alle de obligatoriske funktioner automatisk. Men hvis du f.eks. bruger en manuel testudrulning, der mangler en eller flere obligatoriske funktioner, mislykkes installationen af arbejdsbyrden, og du modtager en meddelelse med en oversigt over de manglende funktioner. Du skal derefter aktivere disse funktioner manuelt og aktivere arbejdsbyrdeinstallationen igen.

### <a name="enabling-or-disabling-features-that-have-data-synchronization-dependencies"></a>Aktivere eller deaktivere funktioner, der har datasynkroniseringsafhængigheder

Funktioner, der påvirker valget af data, der synkroniseres mellem hub'en og dens skalaenheder, har også indflydelse på, hvordan definitionen af arbejdsbyrde oprettes. Det er derfor vigtigt, at disse funktioner aktiveres, før du installerer arbejdsbyrden. Hvis du aktiverer denne funktionstype, mens du kører en arbejdsbyrde, skal du generere definitionen af arbejdsbyrde igen ved at køre en [opgradering af arbejdsbyrde](#manage-workloads), når du har aktiveret funktionen. Hvis du deaktiverer en funktion, der indeholder datasynkroniseringsafhængigheder, mens du kører en arbejdsbyrde, skal du køre en [opgradering af arbejdsbyrden](#manage-workloads) for at fjerne de relevante datasynkroniseringsoplysninger fra definitionen af arbejdsbyrden.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
