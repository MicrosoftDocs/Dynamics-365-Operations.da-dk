---
title: Bruge grænser for kontantstyring
description: I dette emne forklares det, hvordan du bruger kontantstyring til at definere transaktionsgrænser, når der ikke er nogen kontantsaldo, eller en transaktion vil medføre, at kontantsaldoen falder under et foruddefineret beløb.
author: v-kiarnd
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-kiarnd
ms.search.validFrom: 2019-8-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3344ff472f1a844fe96953ff854e958316498339
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407657"
---
# <a name="use-cash-control-limits"></a>Bruge grænser for kontantstyring

[!include [banner](../includes/banner.md)]


I dette emne forklares det, hvordan du bruger kontantstyring til at definere transaktionsgrænser, når der ikke er nogen kontantsaldo, eller en transaktion vil medføre, at kontantsaldoen falder under et foruddefineret beløb.

Kontantstyring giver dig mulighed for at definere en grænse (tærskel) for at forhindre, at transaktioner bogføres, hvis der ikke er nogen kontantsaldo, eller hvis transaktionen vil medføre, at saldoen falder under den definerede grænse. Den konto, der er defineret i den anvendte bogføringsdefinition, evalueres, når transaktioner oprettes, redigeres og bogføres. Hvis der ikke er genereret en post, bruges den tilsvarende konto. Hvis bogføring af transaktionen vil medføre, at den relaterede kassekontosaldo falder under den grænse, der er defineret for kontoen, vises en fejlmeddelelse, og du skal ændre kontoen for at fortsætte. .

Du kan tillade, at bestemte brugergrupper tilsidesætter kontantstyring. Hvis kassekontosaldoen så falder under den definerede grænse, modtager brugere i de angivne brugergrupper en advarselsmeddelelse, men de kan fortsætte med at bogføre transaktionen. Brugerne kan tilsidesætte kontantstyring, hvis udgiften skal bogføres, før de midler, der skal betale for den, er modtaget, eller når der skal foretages en godkendt overførsel, men overførslen ikke er indtastet eller bogført endnu.

Grænsen for kontantstyring sammenlignes med saldoen for kontantstyring (kassekontosaldo minus alle bogførte, ubetalte kreditorfakturaer). Når saldoen for kontantstyring er mindre end grænsen for kontantstyring, er grænsen overskredet.

## <a name="set-up-cash-control"></a>Konfigurere kontantstyring

Udfør følgende trin for at konfigurere kontantstyring og kontantstyringskonti.

1. Gå til **Finans** \> **Opsætning Finans** \> **Finansparametre**.
2. Vælg den økonomiske dimensionsopsætning, der skal bruge validering af kontantstyringssaldi, i feltet **Økonomisk dimensionsopsætning** i gruppen **Kontantstyringsvalidering**.
3. Vælg den brugergruppe, der kan tilsidesætte kontantstyringen, i feltet **Tilsidesæt kontantstyring**. Brugere i denne sikkerhedsgruppe kan derefter bogføre transaktioner, der overskrider grænsen for kontantstyring.
4. Gå til **Finans** \> **Opsætning Finans** \> **Opsætning af bogføring** \> **Kontantstyring**.
5. Angiv indstillingen **Vis kontonavne** til **Ja** for at få vist kontonavnene for de kassekonti og kreditorkonti, du angiver i gitteret.
6. Angiv hver enkelt kassekonto.

Det anbefales, at du tilføjer alle økonomiske dimensionsstrenge for alle gyldige kassekonti. Du kan derefter angive, hvilke kassekonti der skal være underlagt kontantstyringsgrænsen.

7. Angiv den økonomiske dimensionsstreng for kassekontoen i feltet **Kassekonto**. Du skal angive fulde kontonumre.
8. Markér afkrydsningsfeltet **Deltag** for at angive, at den økonomiske dimensionsstreng for kassekontoen er underlagt kontantstyring. Disse kassekonti og de tilsvarende kreditorkonti valideres i forhold til konfigurationsreglerne for kontantstyring.
9. Valgfrit: I kontofeltet **Kreditor** kan du angive den økonomiske dimensionsstreng for kreditorkontoen, der bruges til kreditorfakturaer. Du skal angive et fuldt kontonummer.
10. I feltet **Grænseværdi** skal du angive det beløb, der skal forblive på kassekontoen for at bestå valideringen. Du kan angive et negativt tal, hvis kassekontoen kan overtrækkes (dvs. posteringsbeløb må være større end kontosaldoen).

## <a name="view-accounts-in-cash-control"></a>Vise konti i kontantstyring

Du kan se den aktuelle saldo for de konti, du har defineret, på siden **Konfiguration af kontantstyring**. Gå til **Finans** \> **Forespørgsler** \> **Forespørgsel om kontantstyring**.

Forespørgslen indeholder følgende oplysninger:

- Den aktuelle kassekontosaldo
- Saldoen for alle bogførte, ubetalte kreditorfakturaer, der er anvendt på kassekontoens tilsvarende kreditorkonto
- Kontantstyringssaldoen eller den aktuelle kassekontosaldo minus alle bogførte, ubetalte kreditorfakturaer
- Grænsen for kontantstyring, så du kan sammenligne den med saldoen for kontantstyringen og fastlægge, om betaling af kreditorfakturaerne vil medføre, at kassekontoens saldo falder under kontantstyringsgrænsen.

## <a name="process-transactions-by-using-cash-control-validation"></a>Behandle transaktioner ved hjælp af validering af kontantstyring

Kassekontosaldi valideres for kreditorfakturaer og avancerede finansposter. Linjeelementbeløbet valideres i forhold til de kassekonti og kreditorkonti, som linjens økonomiske dimensioner er knyttet til.

[!NOTE] Budgetstyring er adskilt fra kontantstyring og kan vise ikke-relaterede fejl.

Hvis kontantstyringsgrænsen bliver overskredet, vises der en fejlmeddelelse. Fejlen forhindrer yderligere behandling af fakturaen, medmindre en tilsidesættelse af en kontantstyring er tilladt.

## <a name="vendor-invoice-workflow"></a>Arbejdsgang for kreditorfaktura

### <a name="the-workflow-is-set-up-for-autoposting"></a>Arbejdsgangen er konfigureret til automatisk bogføring

Når du bruger kontantstyringsfunktionen sammen med arbejdsgangen for kreditorfakturaer i Kreditor, og arbejdsgangen er konfigureret til automatisk bogføring, kontrollerer systemet, at den bruger, der sender kreditorfakturaen, har rettigheder til at tilsidesætte grænsen for kontantstyring i trinnet Automatisk bogføring.

Hvis fakturaen vil overskride kontantstyringsgrænsen, og brugeren har tilsidesættende rettigheder, bogføres fakturaen automatisk som en del af arbejdsgangsprocessen. Hvis brugeren ikke har tilsidesættende rettigheder, vises der en fejlmeddelelse i arbejdsgangshistorikken for den relaterede kreditorfaktura. I dette tilfælde kan fakturaen kun behandles korrekt via bogføring, hvis en af følgende betingelser er opfyldt:

- En bruger, der har tilsidesættende rettigheder, sender fakturaen igen
- Fakturaen er ændret, så der bruges en anden kassekonto
- Saldoen for kontantstyring er ændret

### <a name="the-workflow-isnt-set-up-for-autoposting"></a>Arbejdsgangen er ikke konfigureret til automatisk bogføring

Når du bruger kontantstyringsfunktionen sammen med arbejdsgangen for kreditorfakturaer i Kreditor, og arbejdsgangen ikke er konfigureret til automatisk bogføring, kan en bruger, der har tilsidesættende rettigheder, sende en faktura til arbejdsgangen. Valideringen i kontantstyringen udføres igen, når fakturaen bogføres. Den anden validering udføres, fordi kontantsaldiene kan ændres mellem det tidspunkt, hvor fakturaen sendes til arbejdsgangen, og det tidspunkt, hvor fakturaen bogføres.

Hvis fakturaen vil overskride grænsen for kontantstyring, og brugeren ikke har tilsidesættende rettigheder, vises der en fejlmeddelelse, og fakturaen kan ikke sendes til arbejdsgangen. I dette tilfælde kan fakturaen kun sendes korrekt, hvis en af følgende betingelser er opfyldt:

- En bruger, der har tilsidesættende rettigheder, sender fakturaen igen
- Fakturaen er ændret, så der bruges en anden kassekonto
- Saldoen for kontantstyring er ændret
