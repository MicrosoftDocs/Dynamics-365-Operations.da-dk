---
title: Kopiere kreditorer ved hjælp af delte nummerserier
description: Dette emne forklarer, hvordan du kan bruge delte nummerserier til at kopiere en kreditor til en anden juridisk enhed, men bevare det samme kreditor-id.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 33338c331a53586b325def398267ab10db23f78a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458682"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Kopiere kreditorer ved hjælp af delte nummerserier

[!include [banner](../includes/banner.md)]

Du kan bruge delte nummerserier til tildeling af kreditor-id'er. Delte nummerserier giver dig også mulighed for at kopiere kreditorer fra én juridisk enhed til en anden juridisk enhed, men du kan bruge de samme kreditor-id'er i begge juridiske enheder.

## <a name="setup"></a>Konfiguration

Funktionen aktiveres, når du bruger en delt nummerserie til tildeling af kreditor-id'er. Du skal bruge den samme nummerserie i hver juridisk enhed, du vil kopiere en kreditor til. Du kan ændre kreditornummerserien på siden **Kreditorparametre** for hver juridisk enhed. Vælg **Kreditor** \> **Konfiguration** \> **Kreditorparametre**, og vælg derefter fanen **Nummerserier**.

Du kan også angive kreditornummerserier for hver enkelt kreditorgruppe. Disse nummerserier skal også være delte. Nummerserien for en kreditorgruppe bruges først. Hvis der ikke er angivet nogen nummerserie for en kreditorgruppe, bruges den nummerserie, der er angivet på siden **Kreditorparametre**.

Du kan også kopiere kreditorer mellem juridiske enheder, hvis du bruger manuelle kreditor-id'er. Men hvis du forsøger at kopiere en kreditor til en juridisk enhed, hvor kreditor-id'et allerede findes, startes kopieringsprocessen ikke.

## <a name="copy-a-vendor"></a>Kopiere en leverandør

Hvis du vil kopiere en leverandør, skal du vælge **Ny** på listesiden **Alle leverandører** for at åbne siden **Alle leverandører, ny post**. Bemærk, at det nye leverandør-id ikke tildeles med det samme. Denne funktionsmåde adskiller sig fra funktionsmåden i tidligere versioner. Fordi du endnu ikke har valgt kreditorgruppen, kan systemet ikke bestemme den korrekte nummerserie, der skal bruges. Desuden kan det ikke bestemme, om du forsøger at oprette en ny kreditor eller kopiere en kreditor. Derfor tildeles kreditor-id'et først, når du vælger **Gem** nederst på siden.

Hvis du vil oprette en ny kreditor, kan du fortsætte med at udfylde alle felterne, som du plejer. Når du er færdig, og du vælger **Gem**, kan du se, at kreditor-id'et tildeles automatisk. Hvis du bruger manuelle nummerserier, kan du se, at dit manuelle kreditor-id bruges.

Hvis du vil kopiere en kreditor, skal du i feltet **Navn** angive et eller flere tegn, der repræsenterer den kreditor, du søger efter. En søgedialogboks viser en liste over parter, der kan repræsentere den kreditor, du søger efter. Når du vælger en af parterne, vises der flere oplysninger i højre side af dialogboksen:

- Fanen **Generelt** viser partens telefonnummer og adresse.
- Fanen **Roller** viser de roller, den valgte part kan have, og den juridiske enhed, hvor den har hver rolle.
- Fanen **Momsregistrerings-id** viser de momsregistrering-id'er, der er knyttet til parten.

Du kan kun kopiere en part, hvis den har en kreditorrolle, og hvis den har den pågældende rolle i en juridisk enhed, der ikke er den aktuelle juridiske enhed. Følg disse trin, når du har fundet en part, der opfylder disse kriterier.

1. Indstillingen **Kopiér kreditor** vises. Denne indstilling er som standard angivet til **Nej**. Hvis du vil kopiere kreditoren til den aktuelle juridiske enhed, skal du angive indstillingen til **Ja**. 
2. Feltet **Juridisk enhed** vises. Vælg den juridiske enhed, som kreditoren skal kopieres fra. Hvis kreditoren kun findes i én juridisk enhed, er feltet som standard angivet til den pågældende juridiske enhed.
3. Vælg **Vælg**. Den nye kreditor oprettes.

## <a name="validation"></a>Validering

Når du kopierer en kreditor, forsøger systemet at gemme oplysningerne om den nye kreditor. Validering køres for at kontrollere, at dataene, der blev kopieret, er korrekte. Du får en fejlmeddelelse for hver validering, hvor der opstår fejl. Fejlmeddelelserne forklarer, hvilke oplysninger der skal opdateres. Kopien af kreditoren kan ikke gemmes, før du retter alle valideringsfejl.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Kopiere en kreditor ved hjælp af søgefunktionen til SE-nummer

Du kan også kopiere kreditorer ved hjælp af søgefunktionen til SE-nummer, der findes i gruppen **Registrering** under fanen **Kreditor** i handlingsruden på siden **Alle kreditorer**. Dialogboksen **Søgning efter SE-nummer**, der vises, viser SE-numre, kreditor-id, kreditornavn og den juridiske enhed, hvor SE-id'et bruges. Du kan kun kopiere en kreditor, hvis den er i en juridisk enhed, der ikke er den aktuelle juridiske enhed. Følg disse trin, når du har valgt en kreditor, der opfylder dette kriterie.

1. Indstillingen **Kopiér kreditor** vises. Denne indstilling er som standard angivet til **Nej**. Hvis du vil kopiere kreditoren til den aktuelle juridiske enhed, skal du angive indstillingen til **Ja**.
2. Vælg **Vælg**. Den nye kreditor oprettes.
