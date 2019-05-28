---
title: Ofte stillede spørgsmål om adressekartoteker
description: Dette emne indeholder svar på ofte stillede spørgsmål, der er relateret til adressekartoteker i Microsoft Dynamics 365 for Finance and Operations.
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb0239fd9bd80ae15bd2cca08d5a5f5258aef638
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545711"
---
# <a name="address-books-faq"></a>Ofte stillede spørgsmål om adressekartoteker

[!include [banner](../includes/banner.md)]

## <a name="how-do-i-check-for-duplicate-records"></a>Hvordan kontrollerer jeg, om der er ens poster?

Du kan søge efter dublerede poster direkte fra listesiden **Globalt adressekartotek**. På handlingsruden skal du på fanen **Part** i gruppen **Vedligehold** klikke på **Kontrollér, om der er dubletter**. Vælg derefter de værdier, der skal indgå i kontrollen efter dubletter.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Kan jeg tilføje eller slette flere partposter fra et adressekartotek?

Ja, du kan tilføje flere partposter til et adressekartotek og også fjerne flere partposter.

- Hvis du vil tilføje flere partposter til et adressekartotek, skal du på listesiden **Globalt adressekartotek** vælge parterne på listen. Derefter skal du på handlingspanelet på fanen **Part** i gruppen **Vedligehold** klikke på **Tildel parter**. Vælg de adressekartoteker, du vil tilføje de valgte partposter i, og klik derefter på **OK**. Alle de valgte partposter føjes til de adressekartoteker, du har valgt.
- Hvis du vil fjerne flere partposter fra et adressekartotek, skal du på listesiden **Globalt adressekartotek** vælge parterne på listen. Derefter skal du på handlingspanelet på fanen **Part** i gruppen **Vedligehold** klikke på **Fjern parter**. Vælg de adressekartoteker, du vil fjerne parter fra, og klik derefter på **OK**. Alle de valgte partposter fjernes fra de adressekartoteker, du har valgt.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Kan jeg ændre parttypen for en post, eller er det nødvendigt at slette den gamle post og oprette en ny?

Nogle gange skal du muligvis ændre parttypen for en post fra person til organisation eller fra organisation til person. Nancy er f.eks. medlem af salgsteamet for Fabrikam, Storbritannien. På en handelsmesse i London møder hun seks nye kundeemner. Nancy opretter en partpost for kundeemne for hver enkelt kundeemne. Når Nancy gemmer posterne, bliver hver enkelt post også oprette i det globale adressekartotek. Fabrikam har angivet standardparttypen til organisation, men to af de nye kundeemner bør have en post af typen person. Når Nancy vender tilbage fra handelsmessen, skal hun derfor ændre parttypen for to kundeemneposter. Hvis du vil ændre en partpost fra én parttype til en anden, skal du først oprette en ny partpost med den korrekte type i det globale adressekartotek. Du kan derefter knytte den gamle partpost med denne nye post. Når du har foretaget den nye parttilknytning, skal du slette den oprindelige partpost, der har den forkerte posttype.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Hvordan kan jeg ændre navnet eller adressen på en partpost?

Du kan opdatere navnet på en partpost og de adresser, der er knyttet til den pågældende post, når som helst.

- Hvis du vil opdatere navnet på en partpost, skal du åbne partposten og derefter klikke på **Rediger** i handlingsruden. På oversigtspanelet **Generelt** skal du skrive det nye navn for parten og derefter gemme posten.
- Hvis du vil opdatere en adresse til en partpost, skal du åbne partposten og derefter klikke på oversigtspanelet **Adresser**, vælge adressen, der skal opdateres. Klik på **Rediger**, og klik derefter på siden **Rediger adresse**, foretag de nødvendige ændringer af adressen eller parametrene.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Er det muligt at flette to eller flere partposter til én post?

Sommetider har du måske brug for at flette to eller flere partposter til én enkelt post. Det kan ske, hvis du opretter en eller flere identiske partposter, enten med vilje eller utilsigtet. Når du fletter partposter, vælger du at beholde én post. Oplysningerne fra de andre poster flettes derefter ind i denne post. Du opdager for eksempel, at der er gemt oplysninger om Fabrikam i tre partposter: A, B og C. Du beslutter at beholde partpost A. De oplysninger, der er gemt i partposterne B og C, bliver derfor flettet ind i partpost A. Der er situationer, hvor du ikke kan flette partposter:

- Du kan ikke flette partposter, der er knyttet til samme partrolle, f.eks. som kunde eller kreditor, i samme juridiske enhed. Eksempel: Part A er tilknyttet en kunde i den juridiske enhed 123, og part B er tilknyttet en anden kunde i samme juridiske enhed 123. Disse partposter kan ikke flettes, fordi den flettede partpost ville være tilknyttet flere kunder i samme juridiske enhed, hvilket ikke er tilladt. Posterne kan dog flettes, hvis part B er knyttet til en kreditor i den juridiske enhed 123 eller til en kunde i en anden juridisk enhed.
- Du kan ikke flette interne organisationspartposter i samme juridiske enhed, team eller driftsenhed.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Skal jeg oprette en partpost i det globale adressekartotek eller et andet sted, som siden Kunde eller Kreditor?

I det globale adressekartotek eller på den relevante enhedsside kan du angive partposter. Når du tilføjer en post på ét sted, tilføjes den samme post altid på den anden placering. Hvis du f.eks. tilføjer en partpost for en kunde i det globale adressekartotek, bliver posten også tilføjet på siden **Kunde**. Hvis du på samme måde tilføjer en partpost for en kunde på siden **Kunde**, tilføjes posten også i det globale adressekartotek. Brug følgende retningslinjer til at afgøre, hvor du skal indtaste nye partposter:

- **Oprettelse af en partpost, hvis du ikke kender enhedstypen** – Hvis du skal oprette en partpost, men ikke kender enhedstypen (hvis du f.eks. ikke ved, om enheden er en kunde eller en salgsmulighed), skal du oprette posten i det globale adressekartotek. Du kan vælge enhedstypen senere.
- **Oprettelse af en partpost, hvis du kender enhedstypen** – Hvis du kender enhedstypen for parten, kan du oprette en post på den relevante side for den pågældende type. Du kan f.eks. oprette en post for en kunde på siden **Kunde**. Når du opretter og gemmer en post ved hjælp af den relevante enhedsside, oprettes posten automatisk i det globale adressekartotek.

## <a name="can-i-translate-address-information-for-party-records"></a>Kan jeg oversætte adresseoplysninger for partposter?

Du kan konfigurere oversættelser af adresseoplysninger, så oplysningerne vises på dit eget sprog (systemsprog) i Microsoft Dynamics 365 for Finance and Operations, men på et andet sprog i dokumenter, f.eks salgsordrer. Du kan angive oversættelser af lande-/områdenavne, adresseformål og navnerækkefølge. Dit systemsprog er f.eks. dansk, og du opretter en salgsordre for en kunde i Frankrig. I dette tilfælde kan du se kundeposten på dansk i programmet, men få vist adresseoplysningerne på fransk i den udskrevne salgsordre. Når du konfigurerer oversættelser, skal du indtaste en oversættelse for hver vare på listen. De varer, du ikke angiver en oversættelse for, vises på systemsproget. Dit systemsprog er f.eks. dansk, og du sender et dokument til en kunde i Spanien. Hvis du ikke har angivet spanske (ESP) oversættelser af adresseoplysningerne, vises disse oplysninger på dansk både i dit program og på det udskrevne materiale.
