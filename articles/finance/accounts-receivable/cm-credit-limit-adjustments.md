---
title: Reguleringer af kreditgrænse
description: I dette emne beskrives, hvordan du kan konfigurere og tilføje reguleringer af kreditgrænser.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f5e2fbe74d24c729711c6b96d5ff2b7f0c82922c
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015160"
---
# <a name="credit-limit-adjustments"></a>Reguleringer af kreditgrænse 

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Med reguleringer af kreditmaksimum kan kreditchefer opdatere kreditmaksimum og udløbsdatoer for en enkelt debitor, en gruppe debitorer eller alle debitorer via en bogføringsproces. Du kan tilføje poster for reguleringer af kreditmaksimum for at opdatere kunder og kundekreditgrupper, eller du kan bruge dem til at beregne automatiske kreditgrænser. Posterne kan derefter gennemses, sendes til godkendelse via en arbejdsgang og bogføres på debitorkonti.

## <a name="set-up-credit-limit-adjustments"></a>Konfigurere reguleringer af kreditmaksimum

Du kan oprette poster i reguleringskladde for kreditmaksimum på siden **Regulering af kreditmaksimum** (**Kreditstyring \> Reguleringer af kreditmaksimum \> Reguleringer af kreditmaksimum**).

1. Vælg **Ny**. Der oprettes en ny gruppe poster med et reguleringsnummer for kreditmaksimum.
2. Vælg reguleringstype for kreditmaksimum:

    - Vælg **Kreditgrænse** for at ændre debitorens kreditmaksimum.
    - Vælg **Midlertidig kreditgrænse** for at oprette et midlertidigt kreditmaksimum i stedet for at ændre debitorens aktuelle kreditmaksimum. Midlertidige kreditgrænser tilsidesætter en debitors kreditmaksimum i en angivet periode. Når perioden er slut, bruges debitorens kreditmaksimum igen.
3. Angiv en beskrivelse. 

Hvis afkrydsningsfeltet **Bogført** er markeret, er der anvendt kreditmaksimum. Feltet **Godkendelsesstatus** angiver kladdens arbejdsgangsstatus. Arbejdsgange er valgfrie.

### <a name="add-credit-limit-adjustments"></a>Tilføje reguleringer af kreditmaksimum

Hvis du vil tilføje reguleringer af kreditmaksimum manuelt, skal du vælge **Linjer** og derefter følge disse trin.

1. Hvis du vil tilføje en regulering af kreditmaksimum for en debitor, skal du bruge menuen **Debitorreguleringer**. Hvis du vil tilføje et kreditmaksimum for en kundekreditgruppe, skal du vælge **Reguleringer af kundekreditgruppe**.
2. Angiv den kundekonto på fakturaen, der skal opdateres med det nye kreditmaksimum. Hvis du valgte **Reguleringer af kundekreditgruppe** i trin 1, skal du angive kundekreditgruppen. Du kan ikke angive både en kundekonto og et kundekreditgruppe-id på samme kladdelinje.

    Den aktuelle kreditgrænse vises, og navnet vises automatisk.

3. Angiv det nye kreditmaksimum, der skal erstatte det aktuelle kreditmaksimum, når kreditmaksimumposten bogføres.
4. Angiv en dato for at definere den nye udløbsdato for kundens kreditmaksimum. Du skal angive en udløbsdato for kreditmaksimum, når du opretter en regulering af kreditmaksimum.

Feltet **Godkendelsesstatus** angiver arbejdsgangsstatus for kladdelinjen.

Hvis du ønsker, at kreditmaksimumreguleringerne skal genereres automatisk, kan du bruge menuen **Generér** i handlingsruden.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Tilføje reguleringer af midlertidig kreditgrænse

Hvis du vil tilføje reguleringer af midlertidige kreditgrænser manuelt, skal du følge disse trin for kladdelinjerne.

1. Hvis du vil tilføje en regulering af kreditmaksimum for en debitor, skal du bruge menuen **Debitorreguleringer**. Hvis du vil tilføje et kreditmaksimum for en kundekreditgruppe, skal du vælge **Reguleringer af kundekreditgruppe**.
2. Angiv den kundekonto på fakturaen, der skal opdateres med det nye kreditmaksimum. Hvis du valgte **Reguleringer af kundekreditgruppe** i trin 1, skal du angive kundekreditgruppen. Du kan ikke angive både en kundekonto og et kundekreditgruppe-id på samme kladdelinje.

    Hvis der allerede findes en aktiv eller fremtidig midlertidig kreditgrænse, vises de aktuelle datointervaller for den midlertidige kreditgrænse. Navnet vises automatisk.

3. Angiv det nye kreditmaksimum, der skal erstatte den aktuelle kreditgrænse.
4. Definer den periode, hvor det udvidede kreditmaksimum skal gælde, i felterne **Ny fra-dato** og **Ny til-dato**. Du skal angive udløbsdatoer for kreditmaksimum, når du opretter en reguleringskladde for kreditmaksimum.

Feltet **Godkendelsesstatus** angiver arbejdsgangsstatus for kladdelinjen.

## <a name="generate-credit-limit-adjustments"></a>Generere reguleringer af kreditmaksimum

Du kan også få kreditmaksimum reguleret automatisk. Vælg **Generér** i handlingsruden, og vælg derefter en af følgende indstillinger:

- Fra eksisterende debitor
- Fra eksisterende kundekreditgruppe
- Automatiske kreditgrænser

### <a name="from-existing-customer"></a>Fra eksisterende debitor

Du kan oprette kladdelinjer fra eksisterende debitorer. Når du vælger **Generer \> Fra eksisterende debitor**, vises en dialogboks, hvor du kan angive kriterier for valg af debitorer og beregning af de nye grænser.

1. Angiv en reguleringsværdi for at tilføje eller fratrække et beløb fra kreditgrænsen. Angiv en negativ værdi for at reducere den aktuelle kreditgrænse eller en positiv værdi for at øge den.
2. I feltet **Værditype** skal du vælge, hvordan den værdi, du har angivet i trin 1, skal bruges til beregning af den nye kreditgrænse:

    - Vælg **Fast værdi** for at ændre kreditmaksimum med et beløb.
    - Vælg **Procent** for at ændre kreditmaksimum med en procentdel.

3. Angiv en værdi, der bruges til at afrunde det beregnede kreditmaksimum. Skriv f.eks. **10,00** for at afrunde kreditmaksimum til de nærmeste 10,00 valutaenheder.
4. Indstil feltet **Afrundingsform** for at angive, om resten skal rundes op eller ned.
5. Vælg den metode, der bruges til at regulere datoer.

    - Hvis du vælger **Absolut**, kan du angive datoer, der definerer datointervallet for kreditgrænserne.
    - Hvis du vælger **Relativ**, kan du angive forskydningsdatoer for intervallet. Det aktuelle datointerval for kreditgrænsen bliver reguleret af forskydningen.

6. Brug oversigtspanelet **Poster, der skal indgå** til at filtrere listen over debitorer, der er medtaget. Hvis du ikke medtager filtre, genereres der kreditmaksimumposter for alle debitorer.
7. Vælg **OK** for at oprette reguleringsposterne for kreditmaksimum.

### <a name="from-existing-customer-credit-group"></a>Fra eksisterende kundekreditgruppe

Du kan oprette kladdelinjer fra eksisterende kundekreditgrupper. Når du vælger **Generer \> Fra eksisterende kundekreditgruppe**, vises en dialogboks, hvor du kan angive kriterier for valg af kundekreditgrupper og beregning af de nye grænser. Kriterierne er de samme, som bruges til at oprette kladdelinjer fra eksisterende kunder. Se trinnene i forrige afsnit.

### <a name="automatic-credit-limits"></a>Automatiske kreditgrænser

Du kan oprette automatiske kreditgrænser for at definere og opdatere kundens kreditmaksimum. De automatiske kreditgrænser oprettes for en risikogruppe, og de er baseret på de specifikke værdier, der bruges i resultatgrupperne. Du kan bruge disse automatiske kreditgrænser til at oprette poster for kreditmaksimum. Hvis en kunde er tildelt en bestemt risikogruppe, og kundens kreditoplysninger svarer til kriterierne for et automatisk kreditmaksimum, oprettes der en reguleringspost for kreditmaksimum.

#### <a name="create-automatic-credit-limits"></a>Oprette automatiske kreditgrænser

Du opretter automatiske kreditgrænser ved hjælp af kreditmaksimumreguleringer. Når du vælger **Generér \> Automatiske kreditgrænser**, vises der en dialogboks, hvor du kan angive en udløbsdato for de nye kreditgrænser, der oprettes på baggrund af de risikogrupper, som debitorer er tildelt til. Når du har gjort det, skal du vælge **OK** for at oprette reguleringslinjerne for kreditmaksimum.

### <a name="post-adjustments"></a>Bogføre reguleringer

Når du har oprettet reguleringslinjer for kreditmaksimum, kan du bruge knappen **Bogfør** i handlingsruden til at bogføre posterne og opdatere kundekreditmaksimum. Men hvis du har konfigureret en arbejdsgang, skal du vælge **Arbejdsgang \> Send** i handlingsruden for at sende kladden til godkendelse.

### <a name="credit-limit-adjustments-workflows"></a>Arbejdsgange for regulering af kreditmaksimum

Arbejdsgangene for **Reguleringer af kreditmaksimum** kan bruges til at sende kreditmaksimumreguleringer via en godkendelsesproces i en arbejdsgang. Du kan oprette to arbejdsgange på siden **Arbejdsgang for kreditstyring** (**Kreditstyring \> Konfiguration \> Arbejdsgang for kreditstyring**):

- **Reguleringer af kreditmaksimum** – Denne arbejdsgang kan bruges til at godkende poster på hovedniveau.
- **Reguleringslinje for kreditmaksimum** – Denne arbejdsgang kan bruges til at godkende reguleringsposterne, så posterne kan godkendes af forskellige personer, baseret på kriterierne i arbejdsgangen.

> [!NOTE]
> Når du opretter arbejdsgangen **Reguleringer af kreditmaksimum**, kan du konfigurere den, så reguleringerne automatisk bogføres, efter at linjerne er godkendt. Du skal blot medtage opgaven **Bogfør kladde automatisk** i arbejdsgangen.
