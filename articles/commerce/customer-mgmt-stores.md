---
title: Kundestyring i butikker
description: Dette emne forklarer, hvordan detailforretninger kan aktivere kundestyringsegenskaber på POS i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
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
ms.openlocfilehash: 5a352ba479ca5e635ef521b99f31bd26d5d837ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687327"
---
# <a name="customer-management-in-stores"></a>Kundestyring i butikker

[!include [banner](includes/banner.md)]

Dette emne forklarer, hvordan detailforretninger kan aktivere kundestyringsegenskaber på POS i Microsoft Dynamics 365 Commerce.

Det er vigtigt, at butiksmedarbejdere kan oprette og redigere kundeposter i POS. På den måde kan de hente alle opdateringer til kundeoplysninger, f.eks. e-mail-adresse, telefonnummer og adresse. Disse oplysninger er nyttige i downstream-systemer, f.eks. marketing, da effektiviteten af disse systemer afhænger af nøjagtigheden af deres kundedata.

Salgsmedarbejdere kan udløse arbejdsgangen til kundeoprettelse fra to kasseindtastningspunkter. De kan vælge en knap, der er knyttet til handlingen med **Tilføjelse af kunde**, eller de kan vælge **Opret kunde** på applinjen på søgeresultatsiden. I begge tilfælde vises dialogboksen **Ny kunde**, hvor salgsmedarbejdere kan angive de nødvendige kundeoplysninger, som f.eks. kundens navn, e-mail-adresse, telefonnummer, adresse og eventuelle yderligere oplysninger, der er relevante for virksomheden. Disse yderligere oplysninger kan registreres ved hjælp af de debitorattributter, der er tilknyttet debitoren. Du kan finde flere oplysninger om debitorattributter i [Debitorattributter](dev-itpro/customer-attributes.md).

Salgsmedarbejdere kan også hente sekundære e-mailadresser og telefonnumre. Derudover kan de hente kundens præference for modtagelse af marketingoplysninger via enhver af disse sekundære e-mailadresser eller telefonnumre. For at aktivere denne egenskab skal detailforretninger aktivere funktionen **Hent flere e-mails og telefonnumre og accept af marketing på disse kontaktpersoner** i arbejdsområdet til **Funktionsstyring** i Commerce Headquarters (**Systems administration \> Workspaces \> Funktionsstyring**).

## <a name="default-customer-properties"></a>Standardegenskaberne for debitorer

Detailhandlende kan bruge siden **Alle butikker i Commerce headquarters** (**Retail og Commerce \> Kanaler \> Butikker**) til at knytte en standardkunde til hver butik. Derefter kopieres de egenskaber, der er defineret for standardkunden, til alle nye kundeposter, der oprettes. I dialogboksen vises f.eks. **Opret debitor** egenskaber, der er nedarvet fra den standardkunde, der er tilknyttet butikken. Disse egenskaber omfatter **debitortype**, **debitorgruppe**, **kvitteringsindstilling**, **kvitteringsmail**, **valuta** og **sprog**. Alle **tilknytninger** (kundegrupper) nedarves også fra standardkunden. **Økonomiske dimensioner** nedarves dog fra den debitorgruppe, der er tilknyttet standarddebitoren, ikke fra selve standarddebitoren.

> [!NOTE]
> Værdien for **kvitteringsmailen** kopieres kun fra standardkunden, hvis kvitteringsmail-id'et ikke er angivet for de nyoprettede kunder. Det betyder, at hvis kvitteringsmail-id'et findes for standardkunden, får alle de kunder, der oprettes fra e-handelswebstedet, det samme kvitteringsmail-id, da der ikke er nogen brugergrænseflade, hvor kvitteringsmail-id'et kan hentes fra kunden. Vi anbefaler, at du lader feltet for **kvitteringsmail** være tomt for butikkens standardkunde og kun bruger det, hvis du har en forretningsproces, der afhænger af, at der findes en kvitteringsmailadresse. 

Salgsmedarbejdere kan hente flere adresser for en kunde. Kundens navn og telefonnummer nedarves fra de kontaktoplysninger, der er tilknyttet hver enkelt adresse. Oversigtspanelet **Adresser** for en kundepost indeholder et **Formål**-felt, som salgsmedarbejdere kan redigere. Hvis debitortypen er **Person**, er standardværdien **Startside**. Hvis debitortypen er **Organisation**, er standardværdien **Virksomhed**. Af andre værdier, der understøttes i dette felt kan nævnes **Startside**, **Kontor** og **Bogfør boks**. Værdien i feltet **Land** for en adresse nedarves fra den primære adresse, der er angivet på siden **Driftsenhed** i Commerce Headquarters hos **Organisationsadministration \> Organisationer \> Driftsenheder**.



## <a name="additional-resources"></a>Yderligere ressourcer

[Oprettelsestilstand for asynkron kunde](async-customer-mode.md)

[Konvertere asynkrone kunder til synkrone kunder](convert-async-to-sync.md)

[Debitorattributter](dev-itpro/customer-attributes.md)

[Offline-dataudelukkelse](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
