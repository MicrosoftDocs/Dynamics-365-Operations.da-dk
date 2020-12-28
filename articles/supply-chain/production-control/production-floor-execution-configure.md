---
title: Konfigurere grænsefladen til kørsel af produktionsudstyr
description: Dette emne beskriver, hvordan du opretter en eller flere konfigurationer til grænsefladen til kørsel af produktionsudstyr. Når du åbner grænsefladen til kørsel af produktionsudstyr, indlæser den automatisk en udvalgt konfiguration og et jobfilter, der er specifikt for browseren og enheden. I konfigurationen skal du angive de politikker, der skal gælde for en bestemt anvendelse.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: cf58a7d851577854d08bad70cff69794c3841a2d
ms.sourcegitcommit: 9dd2d38e76d4d93171315ec319e6ce7d51d4e6c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2020
ms.locfileid: "4012462"
---
# <a name="configure-the-production-floor-execution-interface"></a>Konfigurere grænsefladen til kørsel af produktionsudstyr

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Arbejderne i produktionen bruger grænsefladen til kørsel af produktionsudstyr til at registrere deres daglige arbejde, f.eks. hvornår de påbegynder et job, rapportere feedback om job, registrere indirekte aktiviteter og rapportere fravær. Disse registreringer er grundlaget for sporing af fremskridt og omkostninger ved produktionsordrer og til beregning af grundlaget for arbejdernes løn.

Når du åbner grænsefladen til kørsel af produktionsudstyr, indlæser den automatisk en udvalgt konfiguration og et jobfilter, der er specifikt for browseren og enheden. I konfigurationen skal du angive de politikker, der skal gælde for en bestemt anvendelse. Her er nogle anvendelseseksempler:

- På en enhed i firmaets ankomsthallen stempler medarbejderne ind, når de ankommer til kontoret, og ud, når de går hjem.
- På en enhed i produktionshallen registrerer maskinoperatørerne, hvornår de starter og afslutter job. De registrerer også pauser og indirekte aktiviteter.

I dette emne beskrives de forskellige indstillinger for konfiguration af jobkortenhederne.

## <a name="turn-on-new-features-in-feature-management"></a>Aktivere nye funktioner i funktionsstyring

Nogle af de indstillinger, der er beskrevet i dette emne, skal være aktiveret i systemet for at være tilgængelige for dig. Brug siden [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere en eller flere af de følgende funktioner efter behov.

### <a name="generate-license-plate"></a>Generér nummerplade

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rækkefølge):

1. Id for færdigmelding tilføjet i jobkortenheden
1. Aktivér automatisk generering af id-nummer ved færdigmelding i jobkortenheden

### <a name="print-label"></a>Udskriv label

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rækkefølge):

1. Id for færdigmelding tilføjet i jobkortenheden
1. Udskriv etiket fra jobkortenhed

### <a name="allow-locking-the-touch-screen"></a>Tillad låsning af berøringsskærmen

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere den følgende funktion i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- (Prøveversion) Funktion til låsning af jobkortenhed og jobkortterminal, så de kan renses

## <a name="work-with-production-floor-execution-configurations"></a>Arbejde med kørselskonfigurationer for produktionsudstyr

Når du vil oprette og vedligeholde enhedskonfigurationer, skal du gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**. På siden **Konfigurer kørsel af produktionsudstyr** vises en liste over eksisterende konfigurationer. Du kan udføre følgende opgaver på denne side:

- Vælg en konfiguration for produktionsudstyr, der er angivet i venstre kolonne, for at få vist og redigere den.
- Vælg **Ny** i handlingsruden for at føje en ny enhedskonfiguration til listen. Angiv et navn i feltet **Konfiguration** for at identificere den nye konfiguration. Det navn, du angiver, skal være entydig blandt alle enhedskonfigurationer, og du kan ikke redigere det senere.

Konfigurer derefter de forskellige indstillinger for den valgte enhedskonfiguration. Følgende felter er tilgængelige:

- **Afmelding ved gå** – Vælg *Ja* i denne indstilling for at bede arbejdere om at rapportere feedback om igangværende job, når de stempler ud. Når der er valgt *Nej* i denne indstilling, bliver arbejderne ikke bedt om at gøre dette.
- **Lås medarbejder** – Når der er valgt *Nej* i denne indstilling, bliver arbejderne logget af umiddelbart efter, at de har foretaget en registrering (f.eks. et nyt job). Enheden vender derefter tilbage til logonsiden. Når der er valgt *Ja* i denne indstilling, forbliver arbejderne logget på jobkortenheden. Men en arbejder kan logge af manuelt, så en anden arbejder kan logge på, mens jobkortenheden fortsætter med at køre under den samme systembrugerkonto. Du kan finde flere oplysninger om disse typer konti under [Tildelte brugere](config-job-card-device.md#assigned-users).
- **Brug det faktiske registreringstidspunkt** – Vælg *Ja* i denne indstilling for at indstille tidspunktet for hver ny registrering til netop det tidspunkt, hvor arbejderen afsendte registreringen. Når der er valgt *Nej* i denne indstilling, bruges logontidspunktet i stedet. Du skal normalt vælge *Ja* i denne indstilling, hvis du har valgt **Ja** i indstillingerne **Lås medarbejder** og/eller *Enkelt arbejder* , i de tilfælde hvor arbejderne ofte forbliver logget ind i længere perioder.
- **Enkelt arbejder** – Vælg *Ja* i denne indstilling, hvis kun én arbejder bruger en jobkortenhed, hvor denne konfiguration er aktiv. Når der er valgt *Ja* i denne indstilling, er **Lås medarbejder** også automatisk indstillet til *Ja*. Derudover fjerner denne indstilling kravet (og muligheden) for, at arbejderen logger på ved hjælp af et kort-ID (eller anden lignende id). I stedet logger medarbejderen på Microsoft Dynamics 365 Supply Chain Management ved hjælp af en systembrugerkonto, der er knyttet til en *tidsregistreret arbejder* (fra tabellen *arbejdere* ), og som bliver logget på jobkortenheden som den pågældende arbejder på samme tid.
- **Tillad låsning af berøringsskærm** – Angiv denne indstilling til *Ja* for at give arbejderne mulighed for at låse berøringsskærmen på jobkortenheden, så de kan rense den. Når denne indstilling er angivet til *Ja* , tilføjes knappen **Lås skærm for rensning** på logonsiden. Når en arbejder vælger denne knap, låses berøringsskærmen midlertidigt for at forhindre utilsigtet input. Der vises også en nedtællingstimer. Arbejderen kan derefter rense enheden og skærmen på sikker vis. Når nedtællingen er fuldført, låses berøringsskærmen automatisk op.
- **Varighed af låst skærm** – Når indstillingen **Tillad låsning af berøringsskærm** er sat til *Ja* , kan du bruge denne indstilling til at angive, hvor mange sekunder berøringsskærmen skal låses for rensning. Varigheden skal være mellem 5 og 120 sekunder.
- **Generér nummerplade** – Angiv denne indstilling til *Ja* for at generere en ny nummerplade, hver gang en arbejder bruger jobkortenheden til færdigmelding. Nummeret på nummerpladen genereres ud fra en nummerserie, der er konfigureret på siden **Parametre til lokationsstyring**. Når der er valgt *Nej* i denne indstilling, skal arbejderne angive en eksisterende nummerplade, når de rapporterer færdigmeldt.
- **Udskriv label** – Angiv denne indstilling til *Ja* for at udskrive en nummerpladelabel, når en arbejder bruger jobkortenheden til færdigmelding. Konfigurationen af labelen foretages i dokumentruten som beskrevet i [Dokumentrutelayout for nummerpladelabels](../warehousing/document-routing-layout-for-license-plates.md).

## <a name="clean-up-job-configurations"></a>Rydde op i jobkonfigurationer

Når shop floor-supervisor konfigurerer grænsefladen til kørsel af produktionsudstyr, vælger han eller hun en konfiguration og et jobfilter. Disse valg gemmes i en referencetabel i Supply Chain Management, og browseren bruger et id, der er gemt i en lokal cookie, til at finde den rigtige række i den pågældende tabel. Tabellen registrerer også den dato og det klokkeslæt, hvor en arbejder senest loggede på hver enkelt enhed.

Et batchjob renser regelmæssigt poster i referencetabellen for enheder, der ikke har logget nogen aktiviteter i de sidste 60 dage. Du kan også til enhver tid manuelt rense posterne ved at følge disse trin.

1. Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**.
1. Vælg **Ryd op i klientkonfigurationer** i handlingsruden.
1. I dialogboksen **Ryd op i klientkonfigurationer** skal du indstille feltet **Antal dage** til det antal dage uden aktivitet (før i dag), der skal tages i betragtning. Du vil fjerne alle konfigurationer og logonposter for enheder, der ikke har været aktive i den pågældende periode.
1. Vælg **OK** for at rydde op i de relevante konfigurationer baseret på indstillingen **Antal dage**.