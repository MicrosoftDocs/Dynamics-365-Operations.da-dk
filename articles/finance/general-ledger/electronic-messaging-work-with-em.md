---
title: Arbejde med funktionen elektroniske beskeder
description: Denne artikel indeholder en oversigt og oplysninger om arbejde med elektroniske meddelelser (EM).
author: liza-golub
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b61c119a06e1a7281d3adb67e043d2f7002cbea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880695"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Arbejde med de elektroniske meddelelsesfunktioner

[!include [banner](../includes/banner.md)]

Hvis du arbejder på meddelelsesniveau, er siden **Elektroniske meddelelser** (**Moms** \> **Forespørgsler og rapporter** \> **Elektroniske meddelelser** \> **Elektroniske meddelelser**) mest nyttig. Hvis du arbejder på dataindsamlings- eller meddelelseselementniveau, er siden **Elementer i elektronisk meddelelse** (**Moms** \> **Forespørgsler og rapporter** \> **Elektroniske meddelelser** \> **Elementer i elektronisk meddelelse**) mest nyttig.

## <a name="electronic-messages"></a>Elektroniske meddelelser

Siden **Elektroniske meddelelser** viser den behandling, der er tilgængelige for dig, afhængigt af din rolle. Sikkerhedsroller knyttes til behandlingen under konfigurationen af behandlingen. For hver behandling, der er tilgængelige for dig, viser siden elektroniske meddelelser og oplysninger, der er knyttet til dem.

I oversigtspanelet **Meddelelser** vises elektroniske meddelelser for den valgte behandling. Du kan, afhængigt af den valgte meddelelses status og den foruddefinerede behandling, køre visse handlinger ved at anvende knapperne over gitteret:

- **Ny** – Denne knap er knyttet til handlinger af typen **Opret meddelelse**.
- **Slet** - Denne knap er tilgængelig, hvis afkrydsningsfeltet **Tillad sletning** er markeret for den aktuelle status for den valgte meddelelse.
- **Indsaml data** – Denne knap er tilknyttet handlinger af typen **Udfyld poster**.
- **Generér rapport** – Denne knap er knyttet til handlinger af typen **Meddelelse om eksport af elektronisk rapportering**.
- **Send rapport** – Denne knap er knyttet til handlinger af typen **Webtjeneste**.
- **Importer svar** – Denne knap er tilknyttet handlinger af typen **Import af elektronisk rapportering**.
- **Opdater status** – Denne knap er knyttet til handlinger af typen **Behandling af bruger på meddelelsesniveau**.
- **Meddelelseselementer** – Åbn siden **Elementer i elektronisk meddelelse**.

I oversigtspanelet **Handlingslog** vises oplysninger om de handlinger, der er udført for den valgte meddelelse. Hvis en handling har medført en fejl, vedhæftes oplysninger om fejlen den tilknyttede linje i gitteret. For at gennemse oplysningerne om fejlen skal du markere linjen i gitteret og dernæst trykke på **Vedhæft fil** (symbolet med en papirklip) i øverste højre hjørne af siden.

I oversigtspanelet **Yderligere meddelelsesfelter** vises de ekstra felter, der er defineret for meddelelser i opsætningen af behandlingen. Oversigtspanelet i disse ekstra felter vises også.

I oversigtspanelet **Meddelelseselementer** vises alle de meddelelseselementer, der vedrører den valgte meddelelse. Du kan, afhængigt af det valgte meddelelseselements status, køre visse handlinger ved at anvende knapperne over gitteret:

- **Slet** – Denne knap er tilgængelig, hvis afkrydsningsfeltet **Tillad sletning** er markeret for den aktuelle status for det valgte meddelelseselement.
- **Opdater status** – Denne knap er knyttet til handlinger af typen **Brugerbehandling**.
- **Originaldokument** – Åbner en side, som viser det oprindelige dokument for det valgte meddelelseselement.

Alle de rapporter, der allerede er genereret og modtaget for en meddelelse, vedhæftes den pågældende meddelelse. For at gennemse de vedhæftede filer, der er relateret til en meddelelse, skal du vælge meddelelsen og dernæst trykke på **Vedhæft fil** (symbolet med en papirklip) i øverste højre hjørne af siden.

![Knappen Vedhæftet fil](media/attachment-icon.png)

Siden **Vedhæftede filer** viser alle de vedhæftede filer, der er relateret til den valgte meddelelse. For at få vist en fil skal du vælge den på listen til venstre og derefter vælge **Åbn** i handlingsruden.

![Knappen Åbn](media/open-button.png)

Du kan ligeledes gennemse de vedhæftede filer, der er relateret til en specifik handling, som tidligere er blevet kørt for en meddelelse. Vælg meddelelsen i oversigtspanelet **Meddelelser** på siden **Elektroniske meddelelser**. Vælg handlingen i oversigtspanelet **Handlingslog**, og vælg derefter knappen **Vedhæftet fil** (symbolet for papirklipssymbolet) øverst til højre på siden.

Du kan også køre enten hele behandlingen eller kun en bestemt handling ved at vælge **Kør behandling** i handlingsruden.

## <a name="electronic-message-items"></a>Elementer i elektronisk meddelelse

Siden **Elementer i elektronisk meddelelse** viser alle meddelelseselementer og en log over de handlinger, der er udført for hvert meddelelseselement. Siden viser også de ekstra felter, der er defineret for meddelelseselementer, og værdierne i disse ekstra felter.

I følgende tabel beskrives felterne under fanen **Meddelelseselementer**.

<table>
<thead>
<tr>
<th>Felt</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Afvikling</td>
<td>Navnet på den behandling, der blev brugt til at oprette meddelelseselementet.</td>
</tr>
<tr>
<td>Meddelelseselement</td>
<td>Id'et for meddelelseselementet. Dette id tildeles automatisk baseret på den <b>Meddelelseselement</b>-nummerserie, der er defineret på siden <b>Finansparametre</b>.</td>
</tr>
<tr>
<td>Meddelelseselementdato</td>
<td>Den dato, hvor meddelelsen blev oprettet.</td>
</tr>
<tr>
<td>Typen af meddelelseselement</td>
<td>Meddelelseselementtypen. Flere typer meddelelseselementer kan konfigureres til samme behandling (f.eks. <b>Indgående fakturaer</b> og <b>Udgående fakturaer</b>). Dette felt kan kun udfyldes automatisk, når en faktura føjes til tabellen Meddelelseselementer.</td>
</tr>
<tr>
<td>Status for meddelelseselement</td>
<td><p>Den faktiske status for meddelelseselementet. De tilgængelige statusser afhænger af typen af meddelelseselement. Her er nogle eksempler:</p>
<ul>
<li><b>Udfyldt</b> – Der blev føjet en post til tabellen Meddelelseselement.</li>
<li><b>Evalueret</b> – Der blev beregnet yderligere attributter for meddelelseselementet.</li>
<li><b>Rapporteret</b> – Meddelelseselementet blev føjet til en rapport.</li>
<li><b>Udelukket</b> – Denne status kan være nyttig, hvis du udelader visse meddelelseselementer fra en rapport, før den er eksporteret.</li>
</ul>
</td>
</tr>
<tr>
<td>Overførselsdato</td>
<td>Til behandling, der automatisk sender en rapport, der er oprettet uden for systemet, på den dato, da meddelelseselementet blev sendt.</td>
</tr>
<tr>
<td>Dokumentnummer</td>
<td>Dette felt udfyldes automatisk på grundlag af opsætningen af handlingen Udfyld poster. Dette felt kan kun udfyldes automatisk, når en faktura føjes til tabellen Meddelelseselementer.</td>
</tr>
<tr>
<td>Kontonummer</td>
<td>Kontonummeret for en kunde eller leverandør eller en anden feltværdi afhængigt af det felt, der er defineret i handlingen til at udfylde poster. Dette felt kan kun udfyldes automatisk, når en faktura føjes til tabellen Meddelelseselementer.</td>
</tr>
<tr>
<td>Melding</td>
<td>Nummeret på meddelelsen. Dette nummer tildeles automatisk baseret på den <b>Meddelelse</b>-nummerserie, der er defineret på siden <b>Finansparametre</b>.</td>
</tr>
<tr>
<td>Meddelelsesstatus</td>
<td>Den faktiske status for den elektroniske meddelelse.</td>
</tr>
<tr>
<td>Næste handling</td>
<td>De næste handlinger, der kan påbegyndes for meddelelseselementets aktuelle status.</td>
</tr>
</tbody>
</table>

Fanen **Ekstra felter** viser de ekstra felter for det valgte meddelelseselement og deres værdier.

### <a name="run-processing"></a>Kør behandling

Vælg **Kør behandling** i handlingsruden for at køre behandlingen af meddelelseselementer. For at køre en bestemt handling skal du i dialogboksen **Kør behandling** vælge **Ja** i indstillingen **Vælg handling** og derefter vælge en handling. For at køre hele behandlingen skal du lade indstillingen **Vælg handling** være angivet til **Nej**.

### <a name="generate-report"></a>Generér rapport

Vælg **Opret efterspørgsel** i handlingsruden. Denne knap er knyttet til handlinger af typen **Eksport af elektronisk rapportering**.

### <a name="update-status"></a>Opdatering af status

Vælg **Opdater status** i handlingsruden for at opdatere status for en eller flere meddelelseselementer. I dialogboksen **Opdater status** skal du bruge oversigtspanelet **Poster, der skal indgå** til at vælge de meddelelseselementer, der skal opdateres. Sørg for, at du definerer udvælgelseskriterierne korrekt, da meddelelseselementers status opdateres i henhold til disse kriterier, den indledende status for den valgte handling og **Ny status**-værdien, du angiver. Når en statusopdatering er fuldført, vil det være vanskeligt at fastslå, hvilke elementer der er blev opdateret. Det vil derfor være vanskeligt at tilbageføre statusopdateringen.

### <a name="electronic-messages"></a>Elektroniske meddelelser

Vælg **Elektroniske meddelelser** i handlingsruden for at gennemse en elektronisk meddelelse, der er relateret til det valgte meddelelseselement.

Du kan ligeledes gennemse alle de filer, der er relateret til et specifikt meddelelseselement. Vælg feltet **Meddelelse** for meddelelseselementet, eller vælg **Elektroniske meddelelser** i handlingsruden. Dernæst skal du på siden **Elektronisk meddelelse** vælge den meddelelse, du ønsker at gennemse filer for, og efterfølgende trykke på knappen **Vedhæft fil** (symbolet med en papirklip) i øverste højre hjørne af siden.

Siden **Vedhæftede filer** viser alle vedhæftede filer, der er relateret til meddelelsen. For at få vist en fil skal du vælge den på listen til venstre og derefter vælge **Åbn** i handlingsruden.

### <a name="original-document"></a>Originaldokument

Vælg **Originaldokument** i handlingsruden for at åbne det oprindelige dokument for det valgte meddelelseselement.
