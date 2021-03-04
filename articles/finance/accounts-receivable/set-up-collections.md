---
title: Konfigurere rykkere
description: I denne artikel beskrives det, hvordan du konfigurerer inkassatorfunktionen
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f8e066b1df3eb3a26d488e1c014f4ae3f31395a
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2020
ms.locfileid: "4441780"
---
# <a name="set-up-collections"></a>Konfigurere rykkere

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du konfigurerer inkassatorfunktionen Du skal udføre nogle opsætningstrin, når du bruger rykkerfunktioner. Der er også nogle valgfrie funktioner, herunder kundepuljer og rykkerteams. 

- Definitioner af forældelsesperioder
- Øjebliksbilleder af aldersfordeling
- Kladdenavne
- Årsagskode for afskrivningstransaktioner
- Inkassoagenter
- Afskrivningskonto
- Oplysninger om NSF (ikke tilstrækkelige midler)
- Outlook-indstillinger til brugere af siden **Rykkere**
- E-mail-adresser

Disse punkter gennemgås mere detaljeret i resten af dette emne. 

<a name="set-up-aging-period-definitions"></a>Konfigurer definitioner af forældelsesperioder
-------------------------------

Konfigurer en definition af forældelsesperioder. En definition af forældelsesperioder definerer de kolonner, der vises på listesiderne **Aldersfordelte saldi**, **Rykkeraktiviteter** og **Rykkersager**. Den definerer også de perioder, der vises på siden **Rykkere**. Hvis der er oprettet en kundepulje, bruges definitionen på forældelsesperioder derfra. Hvis der ikke er oprettet nogen kundepuljer, bruges den standarddefinition af forældelsesperiode, der er angivet på siden **Debitorparametre**. Hvis der ikke er angivet en standarddefinition af forældelsesperiode, bruges den første definition af forældelsesperiode på siden **Definitioner af forældelsesperioder**.

## <a name="create-an-aging-snapshot"></a>Oprette et aldersfordelt øjebliksbillede
Opret poster for aldersfordelt øjebliksbillede for alle kunder eller for kunderne i kundepuljen. Oplysningerne om aldersfordelt øjebliksbillede vises på listesiden **Aldersfordelte saldi** og på siden **Rykkere**. Du skal oprette et aldersfordelt øjebliksbillede, før du kan bruge listesiden. Listesiden indeholder kun oplysninger om kunder, der allerede er oprettet et aldersfordelt øjebliksbillede for.

## <a name="optional-set-up-customer-pools"></a>Valgfri: Oprette kundepuljer
Du kan oprette kundepuljer, der repræsenterer grupper af kunder. Du kan bruge kundepuljer som filtre for de kundeoplysninger, der vises på **Rykkere**-listesiderne, på siden **Rykkere** eller ved oprettelse af aldersfordelte øjebliksbilleder.

## <a name="optional-create-a-collections-team"></a>Valgfri: Oprette et inkassatorteam
Hvis der er flere medarbejdere i virksomheder, der udfører rykkerarbejde, kan du oprette et inkassatorteam. Du kan vælge teamet på siden **Debitorparametre**. Hvis du ikke opretter et inkassatorteam, oprettes der automatisk et team, når du angiver inkassoagenter på siden **Inkassoagent**.

## <a name="set-up-a-collections-case-category"></a>Oprette en rykkersagskategori
Hvis du vil bruge sager til at organisere rykkerarbejdet, kan du oprette en sagskategori med kategoritypen **Rykkere**. Dette er kun nødvendigt, hvis du vil bruge sagsfunktionen på siden **Rykkere**.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Opret kladdenavne (udligning, afskrivning og NSF)
Opret de kladdenavne, der anvendes, når posteringer behandles på siden **Rykkere**. Denne behandling omfatter afstemning af en transaktion, afskrivning af en transaktion eller behandling af en NSF-betaling, dvs. en betaling med ikke tilstrækkelige midler.

| Beskrivelse | Kladdetype     |
|-------------|------------------|
| Bosted  | Debitorbetaling |
| Afskrivning   | Dagligt            |
| NSF (Not sufficeint Funds - US)         | Debitorbetaling |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Opret en årsagskode for afskrivningstransaktioner
Konfigurer den standardårsagskode, der skal bruges, når posteringer afskrives på siden **Rykkere**. Du kan ændre koden under afskrivningsprocessen.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Oprette en mappe til vedhæftede filer til e-mails, og oprette e-mail-skabeloner
Hvis du vil sende e-mails fra siden **Rykkere**, der har vedhæftede filer i Microsoft Excel, kan du oprette valgfri e-mailskabeloner til disse mails.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Angive debitorparametre for rykkere
Angiv debitorparametre, der vises under fanen **Rykkere**.

## <a name="optional-set-up-collections-agents"></a>Valgfri: Oprette inkassoagenter
Hvis der er flere medarbejdere i virksomheder, der udfører rykkerarbejde, kan du oprette inkassoagenter. En inkassator er en arbejder, der er oprettet som bruger på siden **Brugerrelationer**. Du kan tildele kundepuljer (kundeforespørgsler) til inkassoagenter, for at de bedre kan organisere deres arbejde. Inkassatorerne føjes til teamet, der er valgt på siden **Debitorparametre**. Hvis der ikke er markeret et team på siden, oprettes der automatisk et nyt team med navnet **Rykkere**, og inkassatorerne føjes til dette team.

## <a name="set-up-a-writeoff-account"></a>Opret en afskrivningskonto
Opret den afskrivningskonto, der bruges til afskrivningsposten i finansmodulet, når en transaktion afskrives. Denne konto gemmes i debitorposteringsprofilen.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Oprette NSF-oplysninger for bankkonti
Opdater bankkonti, så de har den rette kladde, når NSF-betalinger identificeres på siden **Rykkere**. Under fanen **Valutastyring** i feltet **NSF-betalingskladde** skal du vælge en betalingskladde.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Angive Outlook-indstillinger til brugere af siden Rykkere
Før arbejdere kan oprette aktiviteter eller sende e-mails vha. siden **Rykkere**, skal du bekræfte, at konfigurationsnøglen for **Microsoft Outlook-synkronisering** er valgt, og at Outlook-synkronisering er konfigureret for arbejderne.

## <a name="set-up-email-and-addresses"></a>Konfigurere mail og adresser
Du kan bruge mail til at kommunikere med både kunder og sælgere om rykkerproblemer for at sende mails fra siden **Rykkere**. 

### <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Angive e-mail- og adresseindstillinger for rykkerkontaktpersoner hos kunden
Opret mailadresser for kundekontakter, hvis du vil sende mails til disse kontakter fra siden **Rykkere**. Rykkerkontakten bruges som standardkontaktperson i på siden **Rykkere**. Du kan angive en opgørelsesadresse til en kunde, hvis opgørelser skal sendes til en anden adresse end den primære adresse. 

I oversigtspanelet **Kredit og inkasso** for en kunde skal du i feltet **Kontaktperson ved rykker** vælge den person i kundens virksomhed, der arbejder sammen med din inkassoagent. Denne person bruges som standardkontakt på siden **Rykkere** og e-mails sendes til dem. 

> [!NOTE] 
> Hvis en rykkerkontaktperson ikke er angivet for en kunde, bruges den primære kontaktperson for kunden. Hvis en primær kontakt ikke er angivet, sendes mails til den første adresse, der vises på siden **Kontakter**.

### <a name="set-up-email-settings-for-salespeople"></a>Angive e-mail-indstillinger for sælgere
Opret mailadresser for sælgere, hvis du vil sende mails til disse sælgere fra siden **Rykkere**. Opret en e-mail-adresse til hver sælger i hver provisionssalgsgruppe. Den sælger, hvor afkrydsningsfeltet **Kontakt** er markeret, er den standardsælger, der får tilsendt e-mails. 

Hvis der ikke er angivet en sælger, bruges kundens primære sælger. Hvis der ikke er angivet en primær sælger, sendes e-mails til den første sælger, der vises på siden.


Du kan finde flere oplysninger under følgende emner:

 - [Oprette et rykkerforløb](tasks/create-collection-letter-sequence.md)

 - [Behandle rykkere](tasks/process-collection-letters.md)

 - [Gennemse oplysninger om rykkere](tasks/review-collections-information.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]