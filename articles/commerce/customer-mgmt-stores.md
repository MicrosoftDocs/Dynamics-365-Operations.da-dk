---
title: Kundestyring i butikker
description: Dette emne forklarer, hvordan detailforretninger kan aktivere kundestyringsegenskaber på POS i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 09caa7fa8f10d1afc44bb9343550bc633b8ec99a
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472219"
---
# <a name="customer-management-in-stores"></a>Kundestyring i butikker

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne forklarer, hvordan detailforretninger kan aktivere kundestyringsegenskaber på POS i Microsoft Dynamics 365 Commerce.

Det er vigtigt, at butiksmedarbejdere kan oprette og redigere kundeposter i POS. På den måde kan de hente alle opdateringer til kundeoplysninger, f.eks. e-mail-adresse, telefonnummer og adresse. Disse oplysninger er nyttige i downstream-systemer, f.eks. marketing, da effektiviteten af disse systemer afhænger af nøjagtigheden af deres kundedata.

Salgsmedarbejdere kan udløse arbejdsgangen til kundeoprettelse fra to kasseindtastningspunkter. De kan vælge en knap, der er knyttet til handlingen med **Tilføjelse af kunde**, eller de kan vælge **Opret kunde** på applinjen på søgeresultatsiden. I begge tilfælde vises dialogboksen **Ny kunde**, hvor salgsmedarbejdere kan angive de nødvendige kundeoplysninger, som f.eks. kundens navn, e-mail-adresse, telefonnummer, adresse og eventuelle yderligere oplysninger, der er relevante for virksomheden. Disse yderligere oplysninger kan registreres ved hjælp af de debitorattributter, der er tilknyttet debitoren. Du kan finde flere oplysninger om debitorattributter i [Debitorattributter](dev-itpro/customer-attributes.md).

Salgsmedarbejdere kan også hente sekundære e-mailadresser og telefonnumre. Derudover kan de hente kundens præference for modtagelse af marketingoplysninger via enhver af disse sekundære e-mailadresser eller telefonnumre. For at aktivere denne egenskab skal detailforretninger aktivere funktionen **Hent flere e-mails og telefonnumre og accept af marketing på disse kontaktpersoner** i arbejdsområdet til **Funktionsstyring** i Commerce Headquarters (**Systems administration \> Workspaces \> Funktionsstyring**).

## <a name="default-customer-properties"></a>Standardegenskaberne for debitorer

Detailhandlende kan bruge siden **Alle butikker i Commerce headquarters** (**Retail og Commerce \> Kanaler \> Butikker**) til at knytte en standardkunde til hver butik. Derefter kopieres de egenskaber, der er defineret for standardkunden, til alle nye kundeposter, der oprettes. I dialogboksen vises f.eks. **Opret debitor** egenskaber, der er nedarvet fra den standardkunde, der er tilknyttet butikken. Disse egenskaber omfatter **debitortype**, **debitorgruppe**, **kvitteringsindstilling**, **kvitteringsmail**, **valuta** og **sprog**. Alle **tilknytninger** (kundegrupper) nedarves også fra standardkunden. **Økonomiske dimensioner** nedarves dog fra den debitorgruppe, der er tilknyttet standarddebitoren, ikke fra selve standarddebitoren.

> [!NOTE]
> Værdien for **kvitteringsmailen** kopieres kun fra standardkunden, hvis kvitteringsmail-id'et ikke er angivet for de nyoprettede kunder. Det betyder, at hvis kvitteringsmail-id'et findes for standardkunden, får alle de kunder, der oprettes fra e-handelswebstedet, det samme kvitteringsmail-id, da der ikke er nogen brugergrænseflade, hvor kvitteringsmail-id'et kan hentes fra kunden. Vi anbefaler, at du lader feltet for **kvitteringsmail** være tomt for butikkens standardkunde og kun bruger det, hvis du har en forretningsproces, der afhænger af, at der findes en kvitteringsmailadresse. 

Salgsmedarbejdere kan hente flere adresser for en kunde. Kundens navn og telefonnummer nedarves fra de kontaktoplysninger, der er tilknyttet hver enkelt adresse. Oversigtspanelet **Adresser** for en kundepost indeholder et **Formål**-felt, som salgsmedarbejdere kan redigere. Hvis debitortypen er **Person**, er standardværdien **Startside**. Hvis debitortypen er **Organisation**, er standardværdien **Virksomhed**. Af andre værdier, der understøttes i dette felt kan nævnes **Startside**, **Kontor** og **Bogfør boks**. Værdien i feltet **Land** for en adresse nedarves fra den primære adresse, der er angivet på siden **Driftsenhed** i Commerce Headquarters hos **Organisationsadministration \> Organisationer \> Driftsenheder**.

## <a name="sync-customers-and-async-customers"></a>Synkronisere kunder og Async-kunder

> [VIGTIGT] Hvis POS skifter til offline, mens oprettelsestilstanden Async-debitor deaktiveres, skifter systemet automatisk til oprettelsestilstanden Async-debitor. Uanset, hvad du har valgt mellem oprettelse af Synkronisering og Async-kunde, skal Administratorer af Commerce headquarters derfor oprette og planlægge et batchjob, der gentages for **P-jobbet**, **synkroniser kunder og forretningspartnere fra jobbet async** (tidligere kaldet **Synkroniser kunder og forretningspartnere fra jobbet async mode)** og jobbet **1010**, så alle Async-kunder konverteres til Synkroniser kunder i Commerce Headquarters.

Inden for handel findes der to kundeoprettelsesmåder: Synkron (eller Sync) og asynkron (eller Async). Kunder oprettes som standard synkront. Det vil sige, at de oprettes i Commerce Headquarters i realtid. Det er en fordel at synkronisere kundeoprettelsestilstanden, fordi nye kunder med det samme kan søges på tværs af kanaler. Det har dog også noget at gøre. Da den genererer [Commerce Data Exchange: Realtidsserviceopkald](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, kan ydeevnen påvirkes, hvis der foretages mange samtidige opkald til oprettelse af kunder.

Hvis indstillingen **Opret kunde i async-tilstand** er angivet til **Ja** i butikkens funktionalitetsprofil (**Retail og Commerce \> Konfiguration af kanal \> Konfiguration af onlinebutik \> Funktionalitetsprofiler**), bruges Realtidsserviceopkald ikke til at oprette kundeposter i kanaldatabasen. Oprettelsestilstanden Async-debitor har ingen indflydelse på Commerce Headquarters-performance. Der tildeles et midlertidigt globalt entydigt id til alle nye Async-debitorkonti og bruges som debitorkonto-id. Dette GUID-navn vises ikke til kassebrugere. Disse brugere får i stedet vist **Ventende synkronisering** som debitorkonto-id'et. 

### <a name="convert-async-customers-to-sync-customers"></a>Konverter Async-kunder til Sync-kunder

Hvis du vil konvertere Async-kunder til Sync-kunder, skal du først køre **P-jobbet** for at sende Async-kunder til Commerce Headquarters. Kør derefter jobbet **Synkroniser kunder og forretningspartnere fra jobbet async-tilstand** (tidligere kaldet **Synkroniser kunder og forretningspartnere fra jobbet async)** for at oprette debitorkonto-id'er. Endelig skal du køre jobbet **1010** for at synkronisere de nye kundekonto-id'er med kanalerne.

### <a name="async-customer-limitations"></a>Async-kundebegrænsninger

Funktionaliteten Async customer har i øjeblikket følgende begrænsninger:

- Async-debitorposter kan ikke redigeres, medmindre kunden er oprettet i Commerce Headquarters, og det nye debitorkonto-id er synkroniseret tilbage til kanalen. Derfor kan adressen ikke gemmes for en Async-kunde, før den pågældende kunde er synkroniseret til Commerce Headquarters, da tilføjelsen af en kundeadresse implementeres internt som en redigeringshandling i kundeprofilen. Men hvis funktionen til **asynkron oprettelse af kundeadresser** er aktiveret, kan kundeadresserne også gemmes til Async-kunder.
- Tilknytninger kan ikke knyttes til Async-kunder. Nye Async-kunder arver derfor ikke tilknytninger fra standardkunden.
- Fordelskundekort kan ikke udstedes til Async-kunder, medmindre det nye debitorkonto-id er synkroniseret tilbage til kanalen.
- Sekundære e-mail-adresser og telefonnumre kan ikke registreres for Async-kunder.

Selvom nogle af de tidligere nævnte begrænsninger kan gøre dig opmærksom på at vælge indstillingen Synkroniser kunde for din virksomhed, arbejder handelsteamet på at gøre egenskaberne for Async-kunder mere synkroniserede kundeegenskaber. I forbindelse med frigivelsen af Commerce version 10.0.22 vil en ny funktion til **asynkron oprettelse af kundeadresser**, som du kan aktivere i arbejdsområdet til **funktionsstyring** asynkront gemme nyoprettede kundeadresser til både Synkronisering af kunder og asynkrone kunder. Du kan gemme disse adresser i kundeprofilen i Commerce Headquarters ved at planlægge et tilbagevendende batchjob til **P-job**, **Synkroniser kunder og forretningspartnere fra jobbet med async-tilstand** og **1010**-jobbet, så alle Async-kunder konverteres til Sync-kunder i Commerce Headquarters.

### <a name="customer-creation-in-pos-offline-mode"></a>Kundeoprettelse i POS-offlinetilstand

Hvis POS skifter til offline, mens oprettelsestilstanden Async-debitor deaktiveres, skifter systemet automatisk til oprettelsestilstanden Async-debitor. Derfor skal administratorer af Commerce Headquarters oprette og planlægge et tilbagevendende batchjob til **P-job**, **synkroniser kunder og forretningspartnere fra jobbet med async-tilstand** og **1010**-jobbet, så alle Async-kunder konverteres til Sync-kunder i Commerce Headquarters.

> [!NOTE]
> Hvis indstillingen **Filtrering af delte kundedatatabeller** er angivet til **Ja** på siden **Commerce channel-skema** (**Retail og Commerce \> Headquarters setup \> Commerce-planlægger \> Kanaldatabasegruppe**), er kundeposter ikke oprettet i POS-offline-tilstand. Du kan finde flere oplysninger under [Offline-dataudelukkelser](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Yderligere ressourcer

[Debitorattributter](dev-itpro/customer-attributes.md)

[Offline-dataudelukkelse](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
