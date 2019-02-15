---
title: Kopiere debitorer ved hjælp af delte nummerserier
description: Dette emne forklarer, hvordan du kan bruge delte nummerserier til at kopiere en debitor til en anden juridisk enhed, men bevare det samme debitor-id.
author: mikefalkner
manager: aolson
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7a1e6c6e3a995ad745522d58960e850d72c2ee57
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "302043"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Kopiere debitorer ved hjælp af delte nummerserier

[!include [banner](../includes/banner.md)]

Du kan bruge delte nummerserier til tildeling af debitor-id'er. Delte nummerserier giver dig også mulighed for at kopiere debitorer fra én juridisk enhed til en anden juridisk enhed, men du kan bruge de samme debitor-id'er i begge juridiske enheder.

## <a name="setup"></a>Konfiguration

Funktionen er aktiveret, når du bruger en delt nummerserie til tildeling af debitor-id'er. Du skal bruge den samme nummerserie i hver juridisk enhed, du vil kopiere en debitor til. Du kan ændre debitornummerserien på siden **Debitorparametre** for hver juridisk enhed. Vælg **Debitor** \> **Parametre**, og vælg derefter fanen **Nummerserier**.

Du kan også angive debitornummerserier for hver enkelt debitorgruppe. Disse nummerserier skal også være delte. Nummerserien for en debitorgruppe bruges først. Hvis der ikke er angivet nogen nummerserie for en debitorgruppe, bruges den nummerserie, der er angivet på siden **Debitorparametre**.

Du kan også kopiere debitorer mellem juridiske enheder, hvis du bruger manuelle debitor-id'er. Men hvis du forsøger at kopiere en debitor til en juridisk enhed, hvor debitor-id'et allerede findes, startes kopieringsprocessen ikke.

## <a name="copy-a-customer"></a>Kopiere en debitor

Hvis du vil kopiere en debitor, skal du vælge **Ny** på listesiden **Alle debitorer** for at åbne dialogboksen **Opret debitor**. Bemærk, at det nye debitor-id ikke tildeles med det samme. Denne funktionsmåde adskiller sig fra funktionsmåden i tidligere versioner af Microsoft Dynamics 365 for Finance and Operations. Fordi du endnu ikke har valgt debitorgruppen, kan systemet ikke bestemme den korrekte nummerserie, der skal bruges. Desuden kan det ikke bestemme, om du forsøger at oprette en ny debitor eller kopiere en debitor. Derfor tildeles debitor-id'et først, når du vælger **Gem** nederst i dialogboksen.

Hvis du vil oprette en ny debitor, kan du fortsætte med at udfylde alle felterne, som du plejer. Når du er færdig, og du vælger **Gem**, kan du se, at debitor-id'et tildeles automatisk. Hvis du bruger manuelle nummerserier, kan du se, at dit manuelle debitor-id bruges.

Hvis du vil kopiere en debitor, skal du i feltet **Navn** angive et eller flere tegn, der repræsenterer den debitor, du søger efter. En søgedialogboks viser en liste over parter, der kan repræsentere den debitor, du søger efter. Når du vælger en af parterne, vises der flere oplysninger i højre side af dialogboksen:

- Fanen **Generelt** viser partens telefonnummer og adresse.
- Fanen **Roller** viser de roller, den valgte part kan have, og den juridiske enhed, hvor den har hver rolle.
- Fanen **Momsregistrerings-id** viser de momsregistrering-id'er, der er knyttet til parten.

Du kan kun kopiere en part, hvis den har en debitorrolle, og hvis den har den pågældende rolle i en juridisk enhed, der ikke er den aktuelle juridiske enhed. Følg disse trin, når du har fundet en part, der opfylder disse kriterier.

1. Indstillingen **Kopiér debitor** vises. Denne indstilling er som standard angivet til **Nej**. Hvis du vil kopiere debitoren til den aktuelle juridiske enhed, skal du angive indstillingen til **Ja**. 
2. Feltet **Juridisk enhed** vises. Vælg den juridiske enhed, som debitoren skal kopieres fra. Hvis debitoren kun findes i én juridisk enhed, er feltet som standard angivet til den pågældende juridiske enhed.
3. Vælg **Vælg**. Den nye debitor oprettes.

## <a name="validation"></a>Validering

Når du kopierer en debitor, forsøger systemet at gemme oplysningerne om den nye debitor. Validering køres for at kontrollere, at dataene, der blev kopieret, er korrekte. Du får en fejlmeddelelse for hver validering, hvor der opstår fejl. Fejlmeddelelserne forklarer, hvilke oplysninger der skal opdateres. Kopien af debitoren kan ikke gemmes, før du retter alle valideringsfejl.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Kopiere en debitor ved hjælp af søgefunktionen til SE-nummer

Du kan også kopiere debitorer ved hjælp af søgefunktionen til SE-nummer, der findes i gruppen **Registrering** under fanen **Debitor** i handlingsruden på siden **Alle debitorer**. Dialogboksen **Søgning efter SE-nummer**, der vises, viser SE-numre, debitor-id, debitornavn og den juridiske enhed, hvor SE-id'et bruges. Du kan kun kopiere en debitor, hvis den er i en juridisk enhed, der ikke er den aktuelle juridiske enhed. Følg disse trin, når du har valgt en debitor, der opfylder dette kriterie.

1. Indstillingen **Kopiér debitor** vises. Denne indstilling er som standard angivet til **Nej**. Hvis du vil kopiere debitoren til den aktuelle juridiske enhed, skal du angive indstillingen til **Ja**. 
2. Vælg **Vælg**. Den nye debitor oprettes.
