---
title: Synkroniseringsproblemer med asynkron ordre
description: Denne artikel indeholder en beskrivelse af almindelige årsager til fejl under oprettelse af asynkron ordre i Microsoft Dynamics 365 Commerce og indeholder fejlfindingstrin, der kan hjælpe systembrugere og partnere med at forstå, hvad der gik galt.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815750"
---
# <a name="asynchronous-order-synchronization-issues"></a>Synkroniseringsproblemer med asynkron ordre

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en beskrivelse af almindelige årsager til fejl under oprettelse af asynkron ordre i Microsoft Dynamics 365 Commerce og indeholder fejlfindingstrin, der kan hjælpe systembrugere og partnere med at forstå, hvad der gik galt.

## <a name="symptom"></a>Symptom

Asynkrone ordrer, der oprettes fra Dynamics 365 Commerce-e-handel eller POS, afspejles ikke i Commerce headquarters.

## <a name="troubleshooting"></a>Fejlfinding

Ordreoprettelse kan mislykkes i headquarters af forskellige årsager, afhængigt af det stadie ordreoprettelsesprocessen mislykkes i. Følgende fejlfindingstrin gennemgår de mulige rodårsager.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Kontrollér, at den transaktion, der er relateret til den asynkrone ordre, er nået til headquarters

I forbindelse med e-handelsordrer skal du i headquarters gå til **Retail og Commerce \> Forespørgsler og rapporter \> Transaktioner i onlinebutik**. Hvis du har et bekræftelsesnummer til ordren, skal du filtrere transaktionerne ved at angive bekræftelsesnummeret i feltet **Kanalreference-id**. Hvis du ikke har bekræftelsesnummeret, skal du filtrere transaktionerne ved at angive kundens kontonummer.

For POS-ordrer skal du åbne siden **Butikstransaktioner** og filtrere posterne efter kvitteringsnummer eller debitorkontonummer. Hvis transaktionen ikke blev fundet, skal du køre jobbet **P-0001** for kanaltransaktioner, der synkroniserer transaktionerne fra kanalerne til headquarters. Hvis jobbet **P-0001** mislykkes, skal du åbne en supportanmodning for jobfejlen. Hvis jobbet **P-0001** lykkes, men transaktionerne stadig ikke vises i headquarters, skal du åbne en supportanmodning med de relevante oplysninger.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Kontrollér synkroniseringsstatus, hvis transaktionen findes i headquarters, men ikke er tilknyttet en salgsordre

Hvis transaktionen findes i headquarters, men salgsordren ikke er oprettet, skal du åbne siden **Transaktioner i onlinebutik** og vælge oversigtspanelet **Synkroniseringsstatus**. Hvis jobbet **Synkroniser ordrer** har forsøgt at synkronisere denne transaktion, skal feltet **Ventende ordrestatus** vise statussen **Fuldført** eller **Ikke udført**. Hvis statussen er **Fuldført**, skal salgsordrefeltet være til stede på denne transaktion. Hvis status er **Ikke udført**, kan du se fejloplysningerne i feltet **Oplysninger om ordrefejl** i oversigtspanelet **Synkroniseringsstatus**. Hvis ingen af disse statusser vises, er der ikke gjort forsøg på at behandle transaktionen. I dette tilfælde kan du vælge **Synkroniser ordre** øverst på siden for at køre synkroniseringsjobbet.

Sørg for, at jobbet **Synkroniser ordrer** er planlagt til at køre periodisk, så der kan oprettes asynkrone transaktioner som ordrer i headquarters.

Følgende afsnit indeholder oplysninger om nogle af de almindelige fejl og rettelsesforslag.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Feltet Oplysninger om ordrefejl viser følgende fejlmeddelelse: "Nummerserien er overskredet"

Nummerserier bruges til at oprette salgsordrer i headquarters. Hvis alle de numre, der er tilladt for en nummerserie, er opbrugt, genererer systemet denne fejlmeddelelse. Den nummerserie, der er brugt til at oprette salgsordrer, findes i **Debitorparametre \> Nummerserier \> Salgsordre**. Du kan rette denne fejl ved at rette den eksisterende nummerserie eller erstatte den med en ny nummerserie.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>I feltet Oplysninger om ordrefejl vises følgende fejlmeddelelse: "Der skal være en standardbetalingstjeneste til behandling af kreditkorttransaktioner"

Du kan rette denne fejl ved at kontrollere, at der er defineret en standardbetaling i headquarters. Hvis der ikke er defineret en standardbetaling, skal du definere den. Gå til **Debitor \> Betalingsopsætning \> Betalingstjenester**, og sørg for, at **Standardprocessor til nye kreditkort** er angivet til **Ja** for én betalingstjeneste.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Feltet Oplysninger om ordrefejl viser en fejlmeddelelse om kontostrukturen

Teksten i fejlmeddelelsen om kontostrukturen kan variere, som det ses i følgende eksempler. Fejlene har dog en fælles rodårsag, der er relateret til kontostrukturens konfiguration.

- "Bogføringsresultater for kladdebatchnummer 0009656328 Bilag ARP-000959899 1.00 for bilag ARP-000959899 i firmaets usrt bogføres som en overbetaling eller underbetaling"
- "Bogføringsresultater for kladdebatchnummer 0009656328 Bilag ARP-000959899 Bilag ARP-000959901 Kontostruktur, for kombinationen 618160, er ikke gyldigt for delt Firmahovedkontoen i Finans"
- "Bogføringsresultater for kladdebatchnummer 0009656328 Bilag ARP-000959899 Bilag ARP-000959901 Rapporteret fra firmakonti usrt"
- "Bogføringsresultater for kladdebatchnummer, 0009656328 Bilag ARP-000959899 Bogføring er annulleret"
    
Du kan rette disse fejl ved at gennemgå kontostrukturerne for nøjagtighed. Du kan finde flere oplysninger under [Konfigurere kontostrukturer](/dynamics365/finance/general-ledger/configure-account-structures).
    
Når fejlen er rettet, skal du vælge den mislykkede transaktion og derefter vælge **Synkroniser ordre** øverst på siden for at køre synkroniseringsjobbet.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Andre typer fejl, der kan kræve, at transaktionsdataene bliver rettet

Hvis du vil rette andre typer fejl, der kan kræve, at transaktionsdataene skal rettes, kan du bruge funktionen "rediger og overvåg transaktioner". Der er flere oplysninger i [Redigere og overvåge transaktioner](../edit-order-trans.md).
