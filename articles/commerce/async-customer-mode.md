---
title: Oprettelsestilstand for asynkron kunde
description: Denne artikel beskriver den asynkrone oprettelsestilstand for kunder i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 1ac1bc842d5d12ece8951ffed18157e6f9b50d14
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228717"
---
# <a name="asynchronous-customer-creation-mode"></a>Oprettelsestilstand for asynkron kunde

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel beskriver den asynkrone oprettelsestilstand for kunder i Microsoft Dynamics 365 Commerce.

Inden for handel findes der to kundeoprettelsesmåder: synkron og asynkron. Kunder oprettes som standard synkront. Det vil sige, at de oprettes i Commerce headquarters i realtid. Det er en fordel med synkron kundeoprettelsestilstand, fordi nye kunder med det samme kan søges på tværs af kanaler. Det har dog også noget at gøre. Da den genererer [Commerce Data Exchange: Realtidsserviceopkald](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, kan ydeevnen påvirkes, hvis der foretages mange samtidige opkald til oprettelse af kunder.

Hvis indstillingen **Opret kunde i async-tilstand** er angivet til **Ja** i butikkens funktionalitetsprofil (**Retail og Commerce \> Konfiguration af kanal \> Konfiguration af onlinebutik \> Funktionalitetsprofiler**), bruges Realtidsserviceopkald ikke til at oprette kundeposter i kanaldatabasen. Den asynkrone kundeoprettelsestilstand har ingen indflydelse på Commerce Headquarters-ydeevne. Der tildeles et midlertidigt globalt entydigt id (GUID) til alle nye asynkrone kundeposter, der bruges som debitorkonto-id. Dette GUID vises ikke for brugere af POS. Disse brugere får i stedet vist **Ventende synkronisering** som debitorkonto-id'et.

> [!IMPORTANT]
> Hvis POS skifter til offline, og selvom asynkron kundeoprettelsestilstand er deaktiveret, opretter systemet automatisk kunder asynkront. Derfor skal administratorer af Commerce headquarters, uanset dit valg mellem synkron og asynkron kundeoprettelse, oprette og planlægge et tilbagevendende batchjob til **P-job**, jobbet **Synkroniser kunder og forretningspartnere fra asynkron tilstand** og **1010**-jobbet, så alle asynkrone kunder konverteres til synkrone kunder i Commerce headquarters.

## <a name="async-customer-limitations"></a>Async-kundebegrænsninger

Funktionaliteten for asynkron kunde har i øjeblikket følgende begrænsning:

- Fordelskundekort kan ikke udstedes til asynkrone kunder, medmindre det nye debitorkonto-id er synkroniseret tilbage til kanalen.

## <a name="async-customer-enhancements"></a>Forbedringer af asynkrone kunder

For at hjælpe organisationer med at bruge oprettelsestilstanden asynkron kunde til at administrere kunder og til at reducere kommunikation i realtid med Commerce headquarters er følgende forbedringer blevet rullet ud for at give paritet mellem synkron og asynkron tilstand i kanaler. 

| Funktionsforbedring | Commerce-version | Funktionsdetaljer |
|---|---|---|
| Forbedringer af ydeevnen, når kundeoplysninger hentes fra kanaldatabasen | 10.0.20 og nyere | For at forbedre ydeevnen opdeles kundeenheden i mindre enheder. Derefter henter systemet kun de nødvendige oplysninger fra kanaldatabasen. |
| Mulighed for at oprette adresse asynkront under udtjekning | 10.0.22 og nyere | <p>Funktionsskift: **Aktivér asynkron oprettelse af kundeadresser**</p><p>Funktionsdetaljer:</p><ul><li>Mulighed for at tilføje adresser uden at foretage realtidsserviceopkald til Commerce headquarters</li><li>Mulighed for entydig identifikation af adresser i kanaldatabasen uden brug af et post-id (**RecId**-værdi)</li><li>Sporing af tidsstempel for oprettelse af adresser</li><li>Synkronisering af adresser i Commerce headquarters</li></ul><p>Denne funktion påvirker både synkrone kunder og asynkrone kunder. Hvis du vil redigere adresser asynkront udover at oprette dem asynkront, skal du aktivere funktionen **Redigering af kunder i asynkron tilstand**.</p> |
| Aktivér paritet mellem synkron og asynkron oprettelse af kunder. | 10.0.24 og nyere | <p>Funktionsskift: **Aktivér udvidet asynkron kundeoprettelse**</p><p>Funktionsoplysninger: Mulighed for at hente yderligere oplysninger, f.eks. titel, tilknytninger fra standardkunden og sekundære kontaktoplysninger (telefonnummer og mailadresse), mens du opretter kunder asynkront</p> |
| Brugervenlige fejlmeddelelser | 10.0.28 og nyere | Disse forbedringer er med til at højne brugervenlige fejlmeddelelser, hvis en bruger ikke kan redigere oplysningerne med det samme under synkroniseringen. Du aktiverer disse forbedringer ved at bruge **Tillad, at visse brugergrænsefladeelementer ikke kan ændres af en asynkron kunde** ved **Webstedsindstillinger \> Udvidelser** i Commerce-webstedsgenerator. |
| Mulighed for at redigere kundeoplysninger asynkront | 10.0.29 og nyere | <p>Funktionsskift: **Aktivér redigering af kunder i asynkron tilstand**</p><p>Funktionsdetaljer: Mulighed for at redigere kundedata asynkront</p><p>Du kan finde svar på almindelige spørgsmål om problemer, der vedrører redigering af kundeoplysninger asynkront, under [Ofte stillede spørgsmål om asynkron oprettelsestilstand for kunde](async-customer-mode-faq.md).</p> |

### <a name="feature-switch-hierarchy"></a>Hierarki for funktionsskift

På grund af hierarki for funktionsskift skal du, før du aktiverer funktionen **Aktivér redigering af kunder i asynkron tilstand**, aktivere følgende funktioner: 

- **Ydelsesforbedringer for kundeordrer og kundetransaktioner** – Denne funktion er obligatorisk siden version 10.0.28 af Commerce. 
- **Aktivér udvidet asynkron kundeoprettelse**
- **Aktivér asynkron oprettelse af kundeadresser**

Du kan finde svar på almindelige fejlfindingsspørgsmål i [Ofte stillede spørgsmål om asynkron oprettelsestilstand for kunde](async-customer-mode-faq.md). 

Når du har aktiveret ovennævnte funktioner, skal du planlægge et tilbagevendende batchjob til **P-jobbet**, jobbet **Synkroniser kunder og forretningspartnere fra asynkron tilstand** og **1010**-jobbet, så alle asynkrone kunder konverteres til synkrone kunder i Commerce Headquarters.

### <a name="customer-creation-in-pos-offline-mode"></a>Kundeoprettelse i POS-offlinetilstand

Som nævnt tidligere: Hvis POS skifter til offline, og selvom oprettelsestilstanden for asynkron kunde er deaktiveret, opretter systemet automatisk kunder asynkront. Derfor skal administratorer af Commerce Headquarters oprette og planlægge et tilbagevendende batchjob til **P-jobbet**, jobbet **Synkroniser kunder og forretningspartnere fra asynkron tilstand** og **1010**-jobbet, så alle asynkrone kunder konverteres til synkrone kunder i Commerce Headquarters.

> [!NOTE]
> Hvis indstillingen **Filtrering af delte kundedatatabeller** er angivet til **Ja** på siden **Commerce channel-skema** (**Retail og Commerce \> Headquarters setup \> Commerce-planlægger \> Kanaldatabasegruppe**), er kundeposter ikke oprettet i POS-offline-tilstand. Du kan finde flere oplysninger under [Offline-dataudelukkelser](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Yderligere ressourcer

[Kundestyring i butikker](customer-mgmt-stores.md)

[Konvertere asynkrone kunder til synkrone kunder](convert-async-to-sync.md)

[Debitorattributter](dev-itpro/customer-attributes.md)

[Offline-dataudelukkelse](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
