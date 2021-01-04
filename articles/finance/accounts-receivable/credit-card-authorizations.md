---
title: Opsætning, godkendelse og opsamling af kreditkort
description: Denne artikel indeholder en oversigt over kreditkortgodkendelse i Microsoft Dynamics 365 Finance. Den indeholder oplysninger om, hvordan du kan konfigurere en betalingstjeneste, føje et kreditkort til en salgsordre og erklære en tilladelse ugyldig.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0de35934e8bdb160f68f68dab118997d0141bf29
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441425"
---
# <a name="credit-card-setup-authorization-and-capture"></a>Opsætning, godkendelse og opsamling af kreditkort

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over kreditkortgodkendelse i Microsoft Dynamics 365 Finance. Den indeholder oplysninger om, hvordan du kan konfigurere en betalingstjeneste, føje et kreditkort til en salgsordre og erklære en tilladelse ugyldig.

<a name="setting-up-the-credit-card-payment-service"></a>Opsætning af kreditkortbetalingstjeneste
------------------------------------------

Hvis du vil bruge kreditkort, skal du konfigurere og aktivere en betalingstjeneste på siden Betalingstjenester. En betalingstjeneste fungerer som en bro mellem din juridiske enhed og den bank, der behandler en debitors kreditkort. Du skal arbejde med en udbyder af kreditkort, der er angivet i feltet Betalingsconnector, og konfigurere en konto hos denne udbyder. Du skal derefter konfigurere andre indstillinger på siden Betalingstjenester, konfigurere kreditkorttyper for American Express, Discover og MasterCard på siden Kreditkorttyper og aktivere udbyderen som standardudbyder. Du skal også følge disse trin for at fuldføre konfigurationen:
-   På siden Debitorparametre skal du angive parametre for brug af kreditkortgodkendelser.
-   På siden Betalingsbetingelser skal du konfigurere betalingsbetingelser for kreditkort. Vælg Kreditkort i feltet Betalingstype.
-   Angiv kreditkortoplysninger for debitorer på siden Debitorkreditkort.

## <a name="adding-a-new-credit-card"></a>Tilføje et nyt kreditkort
Du kan oprette nye kreditkortposter på siden Debitorer ved hjælp af Debitor, Opsætning, Kreditkort. Du kan også oprette kreditkortposter, når du angiver salgsordrer på siden Salgsordre ved hjælp af Administrer, Debitor, Kreditkort, Registrer.

<a name="adding-a-credit-card-to-a-sales-order"></a>Føje et kreditkort til en salgsordre
-------------------------------------

Du kan føje et kreditkort til en salgsordre ved at vælge et kreditkort i kreditkortopslaget på oversigtspanelet Prisen og rabatter på siden Salgsordre. Start godkendelsesprocessen ved at vælge Kreditkort og Godkend i handlingsruden på fanen Administrer.

<a name="authorizing-a-credit-card"></a>Godkende et kreditkort
-------------------------

Når et kreditkort godkendes, kontrolleres kortnummeret og kortholders navn, og den disponible saldo bekræftes. Kreditkortets kontrolnummer og kortindehaverens adresse kan eventuelt verificeres. Debitors disponible kreditsaldo reduceres derefter med fakturabeløbet. Betalingstjenesten sender oplysninger om, hvorvidt kreditkortet er godkendt eller afvist. Når salgsordren faktureres, trækkes (opsamles) fakturabeløbet på kreditkortet.

### <a name="card-verification-value"></a>Værdi for kontrolnummer på kreditkort

Du kan kræve at få oplyst kortets verifikationsværdi, der også kaldes kortets sikkerhedskode. I forbindelse med American Express er det en firecifret værdi. I forbindelse med Discover, MasterCard og Visa er det en trecifret værdi.

### <a name="address-verification"></a>Bekræftelse af adresse

Kontrol af adresseoplysninger sendes altid til betalingsudbyderen. Du kan vælge, hvor mange oplysninger der er nødvendige for, at en postering kan accepteres. Sørg for at tjekke med din udbyder for at finde ud af, om de kan acceptere disse oplysninger. Her er indstillingerne for bekræftelse af adresse:
-   **Acceptér altid postering** – Accepterer posteringen, uanset resultaterne af adressekontrollen.
-   **Kontoindehaver** – Sammenlign kortholderens navn på posteringen med oplysningerne fra kreditkortudstederen.
-   **Faktureringsadresse** – Sammenlign kortindehaverens navn og faktureringsadressen for posteringen med kreditkortudstederens oplysninger.
-   **Postnummer i faktureringsadresse** – Sammenlign kortindehaverens navn, faktureringsadresse og postnummer for posteringen med kreditkortudstederens oplysninger.

## <a name="data-support"></a>Dataunderstøttelse
For hver kreditkorttype, der understøttes, kan du angive niveauet af dataunderstøttelse. Niveauet styrer, hvor mange oplysninger om en transaktion der overføres til betalingstjenesten. Sørg for at tjekke med din udbyder for at finde ud af, om de kan stille sådanne oplysninger til rådighed. Her er indstillingerne for understøttelsen af data:
-   **Niveau 1** – Overfører posteringsdato, posteringsbeløb og beskrivelse.
-   **Niveau 2** – Overfører oplysninger fra niveau 1 samt afsendelses- og forhandleradresser og momsoplysninger.
-   **Niveau 3** – Overfører alle oplysninger fra niveau 2 samt ordrelinjeoplysninger.

## <a name="partial-payments"></a>Delvise betalinger
Hvis du leverer en del af en ordre, registreres beløbet til den delvise ordre, og tilladelsen, som gælder beløbet for hele ordren, lukkes. En ny godkendelse overføres derefter til det resterende beløb for den del af ordren, der ikke er leveret.

## <a name="voiding-an-authorization"></a>Annullere en godkendelse
Du kan ændre betalingsmåden for at annullere en kreditkortgodkendelse, til en anden metode, der ikke har en type af kreditkort.





