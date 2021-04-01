---
title: Sky- og kantskalaenheder til styring af arbejdsbyrder i produktion og lagersted
description: Dette emne indeholder oplysninger om sky- og kantskalaenheder til styring af arbejdsbyrder i produktion og lagersted.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: fb0d8e0226b11e93503979c202da917de1df6319
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240431"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Sky- og kantskalaenheder til styring af arbejdsbyrder i produktion og lagersted

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Sky- og kantskalaenheder gør det muligt at fordele arbejdsbyrder i produktion og lagersted mellem forskellige miljøer. Denne funktionalitet kan hjælpe med at forbedre ydeevnen, forhindre afbrydelse af tjenester og maksimere oppetid. Den kommer fra følgende tilføjelsesprogrammer:

- Tilføjelsesprogrammet Cloud Scale Unit til Dynamics 365 Supply Chain Management
- Tilføjelsesprogrammet Edge Scale Unit til Dynamics 365 Supply Chain Management

Firmaer, der arbejder med produktion og distribution, skal kunne køre vigtige forretningsprocesser døgnet rundt uden afbrydelse og med skalering. Sky- og kantskalaenheder gør det muligt for virksomheder at køre centrale, kritiske produktions- og lagerprocesser uden afbrydelse, selv når der er lejlighedsvise problemer med netværksforbindelse eller ventetid.

## <a name="public-preview-information"></a>Oplysninger om offentlig prøveversion

I prøveversionen findes ét miljø, der fungerer som en skybaseret hub af dit Dynamics 365 Supply Chain Management-miljø og et miljø, der fungerer som en skyskalaenhed.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Tilgængelighed af prøveversion

Prøveversionen af sky- og kantskalaenheder bliver tilgængelig for eksisterende kunder af Supply Chain Management i oktober 2020.

Hvis du fra oktober vil have adgang til prøveversion 10.0.15/Platform update 39 til implementering i dit [Microsoft Dynamics Lifecycle Services-miljø (LCS)](https://lcs.dynamics.com/v2), skal du være en del af programmet for tidlig adgang til prøveversionen (også kaldet PEAP) til Supply Chain Management. Du kan deltage i PEAP, hvis du allerede er medlem af det bredere [Dynamics Insider Program](https://experience.dynamics.com/insider). Du skal blot vælge det specifikke program, der kaldes "Finance & Operations: prøveversion af program med tidlig adgang (PEAP)."

> [!IMPORTANT]
> Skalaenheden til Supply Chain Management er kun tilgængelig, hvis du accepterer [Cloud + Edge-prøveversion til Finance and Operations-vilkår](https://Aka.ms/SCMCnETerms).

### <a name="data-processing-for-the-preview"></a>Databehandling til prøveversion

Under den offentlige prøveversion vil visse administrationstjenester kun have en vært i USA. Når funktionen bliver generelt tilgængelig, vil disse administrationstjenester dog være tilgængelige i alle de geografiske områder, der understøttes af Supply Chain Management. Dette påvirker overførslen og lagringen af administrative oplysninger, der bruges af skalaenhedens styring, herunder:

- Dine lejernavne og id'er
- Dine LCS-projekt-id'ere
- Administratormails, der bruges til at logge på
- Miljø-id'er for hub- og skalaenheder
- Konfigurationer af arbejdsbyrder
- Indsamlede målepunkter (f.eks. ventetid og gennemløb), som vises på kortanalysesiden

Data, der overføres til og gemmes i amerikanske datacentre, vil blive slettet, når dine prøveversionsmiljøer lukkes.

### <a name="sign-up-for-the-preview"></a>Tilmeld dig prøveversionen

Hvis du vil tilmelde dig til Cloud- og Edge-prøveversionen til Supply Chain Management, skal din organisation allerede have et aktivt Supply Chain Management-skymiljø.

Egenskaberne for skalaenheden er i øjeblikket en offentlig prøveversion. Når du tilmelder dig, skal du bruge en brugerkonto på den pågældende lejer. Du skal også være projektejer eller miljøadministrator i LCS for et aktivt Dynamics 365 LCS-projekt i den pågældende lejer.

Når du tilmelder dig prøveversionen, skal du vælge en lejer og gennemgå tilmeldingstrinnene. Så snart Microsoft kan tildele prøveversionskapacitet, sender vi dig en mail, der omfatter oplysninger om klargøring og kampagnekoder for to miljøer (en hub og en skalaenhed) for det relevante LCS-projekt. Du kan derefter implementere de to miljøer som sandkassemiljøer på niveau 2. Disse miljøer vil være gyldige 60 dage fra kampagnekodernes oprettelsesdato. Du bør ikke bruge de to miljøer, før det trin, der er beskrevet i næste afsnit, er fuldført.

Når du har bekræftet med Microsoft, at de to miljøer er implementeret ved hjælp af kampagnekoderne, vil et af miljøerne blive konfigureret til at fungere som en hub, og det andet vil blive konfigureret til at fungere som en skalaenhed. Du kan derefter konfigurere skalaenhederne og implementere udvalgt lokationsstyring og produktionsbelastninger ved at bruge [portalen til styring af skalaenhed](https://aka.ms/SCMSUM).

Miljøer i prøveversionen vil automatisk blive slettet efter 60 dage. De vil dog muligvis blive slettet hurtigere, hvis det ser ud til, at de ikke bruges. Når dine prøveversionsmiljøer er blevet slettet, kan du tilmelde dig og stille dig i kø til en ny installation af prøveversion.

Hvis du vil tilmelde dig prøveversionen, skal du gå til [portalen til styring af skalaenhed](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Begrænsninger, der gælder i prøveversionsperioden

> [!IMPORTANT]
> I den første fase af prøveversionsprogrammet til denne funktion understøtter Microsoft kun hubber, der har skyskalaenheder, ikke hubber, der har kantskalaenheder. Kantskalaenheder er installeret lokalt og forventes at blive tilgængelige under en kommende fase af programmet.

Da sky- og kantskalaenheder er en prøveversionsfunktion, er de tjenester, der er knyttet til dem, aktuelt tilgængelige i et begrænset antal lande og områder. Ved at aktivere sky- og kantskalaenheder bekræfter du, at du forstår, at nogle af de data, der er relateret til konfigurationen og behandlingen af sky- og kantskalaenheder, kan blive gemt i et datacenter, der ligger i USA. Ved at aktivere sky- og kantskalaenheder accepterer du også [Cloud + Edge-prøveversion til Finance and Operations-vilkårene](https://Aka.ms/SCMCnETerms). Du kan få mere at vide om sky- og kantskalaenheder i [dokumentationen](https://aka.ms/scmcne).

Beskyttelse af personlige oplysninger er vigtig for Microsoft. Læs vores [erklæring om beskyttelse af personlige oplysninger](https://aka.ms/privacy) for at få mere at vide.

> [!IMPORTANT]
> Nogle forretningsfunktioner understøttes ikke fuldt ud i den offentlige prøveversion, når der anvendes arbejdsbyrder på skalaenheder. Yderligere oplysninger om de funktionelle arbejdsbyrder finder du senere i dette emne.

## <a name="scale-units-and-dedicated-workloads"></a>Skalaenheder og dedikerede arbejdsbyrder

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 med skalaenheder":::

Skalaenheder udvider dit centrale Supply Chain Management-hubmiljø ved at tilføje dedikeret behandlingskapacitet. Skalaenheder kan køre i skyen. Alternativt kan de køre på kanten i dit lokale miljø. Skalaenheder kan midlertidigt blive koblet fra hubmiljøet. Når de er tilsluttet, modtager skalaenheder alle de oplysninger, der kræves for at køre den dedikerede behandling af tildelte arbejdsbelastninger.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Indstillinger for skalaenhed i den offentlige prøveversion":::

For den offentlige prøveversion kan du konfigurere et hubmiljø med udvalgte arbejdsbelastninger i en skyskalaenhed ved hjælp af portalen til styring af skalaenhed. Deltagere med prøveversion, der har adgang til lokale forretningsdata i det lokale miljø, kan også konfigurere LBD-miljøet som en kantskalaenhed.

En arbejdsbyrde er et defineret sæt forretningsfunktioner, der kan udtages og uddelegeres til en skalaenhed. I øjeblikket indeholder prøveversionsfunktionerne to typer arbejdsbelastninger:

- Produktionsudførelse
- Lagerstedsstyring

Du kan tildele en af hver type arbejdsbelastning pr. skalaenhed. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Dedikerede arbejdsbyrdefaciliteter for produktionskørsel i en skalaenhed

Til produktionskørsel giver sky- og kantskalaenheder følgende funktioner, også selvom der ikke er forbindelse mellem kantenhederne og skyen:

- Maskinoperatører og tilsynsførende kan få adgang til den operationelle produktionsplan.
- Maskinoperatører kan holde planen opdateret ved at køre diskrete og procesproduktionsjob.
- Den tilsynsførende kan justere driftsplanen.
- Arbejderne kan få adgang til fremmøde og indstemplings- og udstemplingstid på kanten for at sikre en korrekt beregning af arbejderes løn.

Du kan finde flere oplysninger under [oplysninger om arbejdsbelastning i produktionens skalaenhed](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Dedikerede arbejdsbyrdefaciliteter for lokationsstyring i en skalaenhed

Til lokationsstyring giver sky- og kantskalaenheder følgende funktioner, også selvom der ikke er forbindelse mellem kantenhederne og skyen:

- Behandlingen af udvalgte bølgemetoder aktiveres for salgsordrer og behovsgenopfyldning.
- Lagermedarbejdere kan køre salgs-og behovsgenopfyldning som lagerarbejde ved hjælp af lagerstedsappen.
- Lagermedarbejdere kan forespørge på disponibel lagerbeholdning ved hjælp af lagerstedsappen.
- Lagermedarbejdere kan oprette og køre lagerbevægelser ved hjælp af lagerstedsappen.
- Lagermedarbejdere kan registrere indkøbsordrer og udføre læg på lager med lagerstedsappen.

Du kan finde flere oplysninger under [oplysninger om arbejdsbelastning i lagerstedets skalaenhed](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Onboarde skalaenheder til dit Supply Chain Management-miljø

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Installere prøveversionen til sky- og kantskalaenheder

I følgende illustration vises processen for tilmelding og klargøring af den offentlige prøveversion af skyskalaenheder.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Tilmeldingstrin for prøveversion":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>Vælg din LCS-projektlejer og den detaljerede prøveversionsproces

I den offentlige prøveversion viser [portalen til styring af skalaenhed](https://aka.ms/SCMSUM) listen over de lejere, som din konto er en del af, og hvor du er ejer eller miljøadministrator for et LCS-projekt.

Hvis den lejer, du søger efter, ikke findes på denne liste, skal du gå til [LCS](https://lcs.dynamics.com/v2) og sørge for, at du enten er miljøadministrator eller projektejer af LCS-projektet for den pågældende lejer. Bemærk, at det kun er Azure Active Directory-konti (Azure AD) fra den valgte lejer, der er godkendt til at fuldføre tilmeldingen.

> [!NOTE]
> Når du har anvendt ændringer på LCS, kan det tage op til 30 minutter, før listen over lejere afspejler ændringerne.

For hver lejer vises tilmeldingsstatus på listen.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Tilmeld for en lejer":::

Vælg linket **Klik her for at tilmelde dig** for at tilmelde din LCS-lejer til deltagelse i prøveversionen. Du skal acceptere betingelserne. Du skal også angive en forretningsmailadresse, hvor Microsoft kan sende kommunikation, der er relateret til prøveversionens tilmeldingsproces.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Indsende tilmelding for en lejer":::

Microsoft vil gennemgå din anmodning og give dig besked om de næste trin ved at sende en mail til den adresse, du har angivet i tilmeldingsformularen.

Når du har fået adgang til prøveversionsprogrammet, vil du modtage to kampagnekoder til dit LCS-projekt. Du kan nu bruge disse kampagnekoder til at implementere to miljøer i LCS. Miljøerne skal bruge PEAP version 10.0.15 eller nyere. Når du er færdig med at anvende kampagnekoderne, skal du give Microsoft besked (som oplyst), så vi kan fuldføre aktiveringen af miljøerne til prøveversionsfunktionerne. Microsoft vil give dig besked, når dette konfigurationstrin er fuldført.

Du kan nu konfigurere skalaenheder og arbejdsbelastninger i dit prøveversionsmiljø.

> [!IMPORTANT]
> Når du konfigurerer skyskalaenheder, kan du [udføre alle nødvendige trin i portalen til styring af skalaenhed](#scale-unit-manager-portal).
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Administrere skyskalaenheder og arbejdsbyrder ved hjælp af portalen til styring af skalaenhed

Gå til [portalen til styring af skalaenhed](https://aka.ms/SCMSUM), og log på ved hjælp af din lejerkonto. På siden **Konfigurer skalaenheder** kan du tilføje et hubmiljø, hvis det ikke allerede står på listen. Derefter kan du vælge den hub, du vil konfigurere med skalaenheder og arbejdsbelastninger.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Skalaenhed og arbejdsbyrdestyring":::

Hvis du vil tilføje en eller flere skalaenheder, der er tilgængelige i topologien, skal du vælge **Tilføj skalaenheder**. I prøveversionen kan du se den skyskalaenhed, som du har installeret fra en af de kampagnekoder, du har modtaget som en del af prøveversionsprogrammet.

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Under fanen **Definerede arbejdsbyrder** skal du bruge knappen **Opret arbejdsbyrde** til at føje en arbejdsbyrde for lokationsstyring eller produktionskørsel til en af skalaenhederne. For hver arbejdsbyrde skal du angive konteksten for de processer, der skal ejes af arbejdsbyrden. For arbejdsbyrder til lokationsstyring er konteksten et specifikt lagersted på en bestemt lokation og juridisk enhed. For arbejdsbyrder til produktionskørsel er konteksten et specifikt sted i en juridisk enhed.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Oprettelse af arbejdsbyrde":::

> [!IMPORTANT]
> Portalen til styring af skalaenhed i prøveversionen giver dig ikke mulighed for at fjerne arbejdsbyrder fra skalaenheder eller fjerne tildeling af en skalaenhed fra en hub, når tildelingen er udført. Hvis du skal fjerne en tildeling, skal du kontakte din kontaktperson for programstyring af prøveversionen.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]