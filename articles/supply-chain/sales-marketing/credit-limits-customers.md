---
title: Kreditmaksimum for debitorer
description: Denne artikel indeholder en oversigt over, hvordan kreditmaksimum fungerer i Microsoft Dynamics 365 for Finance and Operations.
author: omulvad
manager: AnnBe
ms.date: 09/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e00828ea24434da6dfd7443153b007ea728375f3
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="credit-limits-for-customers"></a>Kreditmaksimum for debitorer

[!INCLUDE [banner](../includes/banner.md)]

Ved at angive et kreditmaksimum kan du angive det maksimale kreditbeløb, der kan gives til dine kunder. Hvis der er angivet et kreditmaksimum, kontrolleres det automatisk, når en bruger forsøger at opdatere et dokument. Hvis kreditmaksimum overskrides, vises en meddelelse til brugeren. Denne artikel indeholder en oversigt over, hvordan kreditmaksimum fungerer, og det indeholder svar på følgende spørgsmål:

-   Hvilke dokumenter og processer kan jeg kontrollere kreditmaksimum for?

-   Hvor kan jeg konfigurere den måde, kundens resterende kredit beregnes på?

-   Hvor bruges der oplysninger om en kundes resterende kredit?

-   Hvor kan jeg angive, om der kræves identifikation, for at der kan gives kredit til en kunde, og det kreditmaksimumbeløb, der kræver identifikation?

-   Hvor kan jeg angive, om der skal vises en advarsel eller fejlmeddelelse, hvis kreditmaksimum er overskredet?

-   Hvordan kan jeg angive kreditmaksimum for en bestemt kunde?

-   Hvordan kontrollerer jeg manuelt kreditmaksimum i salgsordrer?

**Hvilke dokumenter og processer kan jeg kontrollere kreditmaksimum for?**

Brug formularen **Debitorparametre** til at angive, hvilke dokumenter, der skal kontrolleres for kreditmaksimum. Du skal være medlem af sikkerhedsrollen Systemadministrator (- SYSADMIN-) for at foretage ændringer i denne form. Du kan kontrollere kreditmaksimum for følgende dokumenter og processer:

-   Fakturaer for salgsordrer, når du bogfører fakturaer

-   Følgesedler for salgsordrer, når du opdaterer følgesedler

-   Salgsordrer, når du tilføjer linjer i formularen **Salgsordre**

-   Salgsordrer, når de er oprettet via en tjeneste

-   Fritekstfakturaer, når du bogfører fakturaerne

Kreditmaksimum kontrolleres automatisk, hvis en af følgende indstillinger er angivet:

-   I formularen **Debitorparametre** angives feltet **Kreditmaks.type** til alt andet end **Ingen**. Kreditmaksimum kontrolleres for alle kunder.

-   I formularen **Debitorparametre** er feltet **Kreditmaks.type** angivet til **Ingen**, men **Tvungen kreditmaks.** er markeret for en kunde i formularen **Debitorer**. Kreditmaksimum kontrolleres kun for bestemte kunder.

Hvis du vil kontrollere kreditmaksimum for følgende dokumenter, skal du angive yderligere indstillinger.

|    Dokument                                    |    Yderligere indstilling                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Fritekstfaktura                         |    I formularen Debitorparametre i området Kreditvurdering skal du vælge Kontrollér kreditmaks. på fritekstfaktura.     |
|    Salgsordre (angivet manuelt)            |    I formularen Debitorparametre i området Kreditvurdering skal du vælge Kontrollér kreditmaks. på salgsordre.           |
|    Salgsordre (modtaget elektronisk)     |    I formularen Debitorparametre i området AIF skal du vælge Kontrollér kreditmaks. for salgsordrer.                     |

**Hvor kan jeg konfigurere den måde, en kundes resterende kredit beregnes på?**

Du kan konfigurere Dynamics 365 til at beregne en kundes resterende kredit på en af følgende måder:

-   Sammenlign kreditmaksimum med debitorsaldoen.

-   Sammenlign kreditmaksimum med debitorsaldoen og beløb på følgeseddel.

-   Sammenlign kreditmaksimum med debitorsaldoen og alle åbne posteringsaktiviteter. Dette omfatter beløb på følgesedler og salgsordrebeløb.

Brug formularen **Debitorparametre** til at angive de oplysninger, der skal sammenlignes med. Du skal være medlem af sikkerhedsrollen Systemadministrator (- SYSADMIN-) for at foretage ændringer i denne form. I feltet **Kreditmaks.type** skal du vælge, om der skal udføres kontrol af kreditmaksimum, og hvilke transaktionsoplysninger der skal medtages, når kreditmaksimum kontrolleres. Vælg mellem følgende indstillinger:

-   **Ingen** – Kontrollér ikke kreditmaksimum. Du kan tilsidesætte denne indstilling for en bestemt kunde ved at markere afkrydsningsfeltet **Kreditmaks.type** i formularen **Debitorer**. Hvis du gør det, kontrolleres kreditmaksimum i forhold til debitorsaldoen.

-   **Saldo** - Kreditmaksimum kontrolleres i forhold til debitorsaldoen.

-   **Saldo + følgeseddel eller produktkvittering** – Kreditmaksimum kontrolleres i forhold til debitorsaldoen og leverancer.

-   **Saldo+Alt** – Kreditmaks. kontrolleres i forhold til debitorsaldoen, leverancer og åbne ordrer.

**Hvor bruges der oplysninger om en kundes resterende kredit?**

Oplysninger om en kundes saldo og resterende kreditbeløb beregnes og gemmes, når du opretter et aldersfordelt øjebliksbillede, og de vises i formularen **Rykkere**. De beløb, der vises i formularen **Rykkere**, indeholder muligvis ikke alle transaktionsaktiviteter, før der oprettes et nyt aldersfordelt øjebliksbillede. Du kan finde flere oplysninger under [Rykkere og kredit i debitorparametre](https://technet.microsoft.com/en-us/library/hh209221.aspx).

Oplysninger om en kundes saldo og resterende kreditbeløb beregnes, når salgsordrer, følgesedler og fakturaer opdateres, afhængigt af de dokumenter der er valgt. Hvis beløbet på det dokument, du arbejder med, medfører, at kreditmaksimum overskrides, vises der en meddelelse.

**Hvor kan jeg angive, om der kræves identifikation, for at der kan gives kredit til en kunde, og den kreditmaksimum, der kræver identifikation?**

Brug formularen **Debitorparametre** til at angive, om der skal kræves identifikation, og det kreditmaksimumbeløb, der kræver identifikation.
Du skal være medlem af sikkerhedsrollen Systemadministrator (- SYSADMIN-) for at foretage ændringer i denne form.

|    Felt                                    |    Betegnelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Kræv identifikation ved kredit     |    Vælg den type identifikation, der skal angives for de kunder, din juridiske enhed yder kredit til. Den indstilling, du vælger i dette felt bestemmer, hvornår og hvilken type oplysninger der kræves i offentlige id-felter i formularen Debitorer: Nej – intet offentligt tildelte id er påkrævet, uanset kundens kreditmaksimum.     Ja – Der kræves et licensnummer eller anden identifikation, der er udstedt af myndighederne, hvis kundens kreditmaksimum er større end eller lig med nul.     Minimumsgrænse – Der kræves et licensnummer eller anden identifikation, der er udstedt af myndighederne, hvis kundens kreditmaksimum er større end eller lig med den grænse, der er angivet i feltet Maksimum i denne formular.        |
|    Maksimum                                    |    Angiv det kreditmaksimum, hvor et licensnummer eller anden identifikation udstedt af myndighederne, kræves for kunder.    Skriv f.eks. 2000 for at kræve, at der angives et identifikationsnummer, f.eks. kørekortnummer, for kunder med et kreditmaksimum på 2.000 eller højere.    Dette felt er tilgængeligt, hvis du har valgt Minimumsgrænse i feltet Kræv identifikation ved kredit.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Hvor kan jeg angive, om der skal vises en advarsel eller fejlmeddelelse, hvis kreditmaksimum er overskredet?**

Brug formularen **Debitorparametre** til at angive, om der skal vises en advarsel eller fejlmeddelelse, hvis kreditmaksimum er overskredet. Denne advarsel eller fejlmeddelelse vises, når en bruger indtaster eller bogfører oplysninger, eller den medtages i en log, hvis dokumenterne behandles af en elektronisk tjeneste. Du skal være medlem af sikkerhedsrollen Systemadministrator (- SYSADMIN-) for at foretage ændringer i denne form.

|    Felt                                                               |    Betegnelse                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Besked ved overskridelse af kreditmaksimum (i området kreditvurdering)     |    Vælg, hvordan meddelelser om kreditmaksimum, der overskrides, skal vises for brugere. Vælg en af følgende indstillinger: Fejl – en fejlmeddelelse vises. Dette standser normalt den aktuelle handling, og konflikten skal løses, inden processen kan fortsætte.     Advarsel – Der vises en advarsel, men processen kan fortsætte.                     |
|    Besked ved overskridelse af kreditmaksimum (i området AIF)               |    Vælg, hvordan meddelelser om overskridelse af et kreditmaksimum skal leveres i en log. Vælg mellem følgende indstillinger: Fejl – Der vises en fejlmeddelelse i formularen Undtagelser, og dokumentet behandles ikke, før fejlen er løst.     Advarsel – Der vises en advarsel i formularen Undtagelser , men processen kan fortsætte.        |

**Hvordan kan jeg angive kreditmaksimumbeløbet for en bestemt kunde?**

Brug formularen **Debitorer** til at angive kreditmaksimumbeløbet for en bestemt kunde. Du skal være medlem af en sikkerhedsrolle, der er tildelt rettigheden Vedligehold debitormaster(CustCustomersMaintain), for at foretage ændringer i denne form.

1.  Klik på **Debitor** \> **Generelt** \> **Kunder** \> **Alle kunder**. Dobbeltklik på en debitorkonto.

2.  I formularen **Debitorer** skal du i handlingsruden klikke på **Rediger**.

3.  Angiv et valutabeløb i feltet **Kreditmaks.**. Denne værdi skal være større end nul (0) og vil blive brugt som kreditmaksimumbeløb.

4.  Hvis det er nødvendigt, skal du angive et licensnummer eller anden identifikation, der er udstedt af myndighederne, i feltet **CPR**..

> [!NOTE]
> I formularen **Debitorparametre** vælges typisk en kreditmaksimumtype. Men, hvis kreditmaksimumtypen er angivet til **Ingen**, skal du også markere afkrydsningsfeltet **Tvungen kreditmaks.** i formularen **Debitorer** for at kontrollere debitorens kreditmaksimum i forhold til debitorsaldoen. Du kan finde flere oplysninger om kreditmaksimumtyper under "Hvilke dokumenter og processer kan jeg kontrollere kreditmaksimum for?" i dette emne. 

**Hvordan kontrollerer jeg manuelt kreditmaksimum i salgsordrer?**

I visse tilfælde skal du kontrollere en debitors kreditmaksimum manuelt. Du kan f.eks. manuelt kontrollere en kundes kreditmaksimum, før du begynder at indtaste en salgsordre. Du kan bruge formularen **Salgsordre** til at kontrollere kreditmaksimum manuelt. Du skal være medlem af en sikkerhedsrolle, der er tildelt rettigheden Vedligehold salgsordre SalesOrderMaintain), for at foretage ændringer i denne form.

1.  Klik på **Salg og marketing** \> **Generelt** \> **Salgsordrer** \> **Alle salgsordrer**. Dobbeltklik på en salgsordre.

2.  I formularen **Salgsordre** skal du i handlingsruden under fanen **Administrer** klikke på **Kontrollér kreditmaks.**.

