---
title: Angive kreditorkonti
description: "I dette emne beskrives, hvilke typer oplysninger du skal angive, når du opretter en ny kreditorkonto."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 0719a49bee069dc49be084a3fbc4ba5eb4883d03
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-vendor-accounts"></a>Angive kreditorkonti

I dette emne beskrives, hvilke typer oplysninger du skal angive, når du opretter en ny kreditorkonto.

Når du har oprettet en kreditorkonto, kan du angive oplysninger om kreditoren. Disse oplysninger bruges til automatisk at indsætte data i dokumenter og spore aktivitet, der involverer kreditoren. Du kan f.eks. konfigurere følgende oplysninger om en kreditor:

-   Tilknyt en kreditorgruppe. Alle kreditorer skal være knyttet til en kreditorgruppe. Kreditorerne i en kreditorgruppe har parametre, som de deler. De kan f.eks. have samme betalingsbetingelser.
-   Konfigurer kreditoren til katalogimport. Kreditorer kan levere en fil, der indeholder kataloget over deres varer og tjenester. Denne fil kan overføres, så dine medarbejdere kan bestille fra kreditoren.
-   Tildel kreditoren til indkøbskategorier.
-   Tillad en eksisterende kreditor at gøre forretninger med en anden juridisk enhed i organisationen.
-   Sæt en kreditor på hold for bestemte typer transaktioner.
-   Angiv bankoplysninger for kreditoren, så du kan sende betalinger elektronisk.
-   Konfigurer moms-, leverings-, faktura- og betalingsoplysningerne for kreditoren. Disse indstillinger kopieres som standard til nye dokumenter, du opretter for kreditoren.
-   Konfigurer standard økonomiske dimensioner, der bruges til automatisk bogføring af transaktioner med kreditoren til regnskaber.

Hvis du vil fremskynde oprettelsen af kreditorkonti, kan du oprette skabeloner. Du opretter en skabelon på den **leverandør** i handlingsruden, skal du klikke på **indstillinger**&gt;**registrere oplysninger om**. Klik derefter på **Regnskabsskabelon**. Regnskabsskabeloner deles med andre brugere.  

Du kan også oprette en brugerskabelon til eget brug. Du kan ikke slette en kreditor, der er tilknyttet andre poster, f.eks. kontakter og produkter.

## <a name="vendor-account-numbers"></a>Kreditorkontonumre
Kontonummeret er et entydigt id for en kreditor. Du kan konfigurere kontonumre, så de genereres automatisk, når du opretter en kreditor. Du kan også konfigurere nummerserien, så kontonumrene angives manuelt. Du kan f.eks. bruge kreditorens telefonnummer som id.

## <a name="vendor-organizations-and-individual-vendors"></a>Leverandørorganisationer og individuelle kreditorer
Når du opretter en ny kreditorkonto, skal du vælge, om kreditoren er en organisation eller en person. Dit valg påvirker de oplysninger, der skal udfyldes for kreditoren. Disse oplysninger omfatter fornavn, efternavn og titel for en person. For en organisation omfatter disse oplysninger organisationsnummeret og antallet af medarbejdere.

## <a name="addresses"></a>Adresser
For hver kreditor kan du angive flere adresser, som bruges til forskellige formål. Du kan f.eks. oprette en adresse, der er beregnet til **Faktura**. Hvis du betaler kreditoren med check, kan du også angive en adresse beregnet til **Remitter-til**. Hvis du skal angive en adresse, der skal bruges ved pengeoverførsler til udenlandske banker, bliver formålet **SWIFT**.

## <a name="vendor-contacts"></a>Kreditorkontakter
Du kan gemme kontakter for en kreditor. Disse kontakter kan derefter bruges på dokumenter som indkøbsordrer eller anmodninger om tilbud (tilbudsanmodninger).  

Føje kontaktpersoner til en kreditor på den **alle kreditorer** skal den **leverandør** under fanen den **opsætning af** skal du klikke på **kontakter**&gt;**Tilføj kontakter**.  

Du kan oprette kreditorkontakter fra bunden. Du kan også kopiere oplysninger fra en anden person, der allerede er registreret i Microsoft Dynamics 365 for Operations, og redigere oplysningerne, som du har brug for.  

**Bemærk:** Tilføjelse af en kontakt for en kreditor er ikke det samme som at tilføje kontaktoplysninger for den pågældende kreditor. Selvom du kan tilføje generelle kontaktoplysninger for en kreditor, kan du også have flere bestemte personer, der er kontakter i den pågældende virksomhed, og som alle har deres egne kontaktoplysninger.  

Du kan ikke slette en kontaktpersonpost, hvis der refereres til kontakten i et dokument. I stedet kan du deaktivere kontakten.  

Du kan tilføje kreditorkontakter dine personlige kontaktpersoner i Microsoft Office 365. Men du skal først oprette synkronisering mellem Dynamics 365 for operationer og Office 365 i Microsoft Exchange Server-synkronisering, og installationsguiden af Microsoft Outlook.

## <a name="vendors-in-different-legal-entities"></a>Kreditorer i forskellige juridiske enheder
Hvis en kreditor kun er registreret for én juridisk enhed i organisationen, og andre juridiske enheder skal registrere den samme kreditor, kan du bruge siden **Føj kreditor til en anden juridisk enhed** for at konfigurere kreditoren til at kunne gøre forretninger med en anden juridisk enhed. Du skal vælge en kreditorgruppe, valuta og hold-status for kreditoren i den valgte juridiske enhed.  

Hvis flere juridiske enheder i organisationen handler med samme kreditor, og hver juridisk enhed har en separat kreditorkonto for kreditoren, kan du flette part-id'erne for kreditorkontiene. På denne måde kan oplysninger såsom adressen og antallet af medarbejdere deles, så du kun skal opdatere dem ét sted.  

Hvis du vil flette part-id'er, skal du følge disse trin.

1.  På siden **Globalt adressekartotek** skal du vælge de poster i adressebogen, der repræsenterer kreditoren i hver juridisk enhed, som skal medtages i fletningen.
2.  Klik på **Flet poster** i handlingsruden.

## <a name="agreements"></a>Aftaler
Når du har oprettet en kreditorkonto, vil du måske også registrere de aftaler, som du har med kreditoren. Du kan oprette pris-og rabataftaler ved hjælp af handlingerne i kreditorposten. Du kan også oprette en købsaftale på siden **Købsaftaler**.

## <a name="putting-a-vendor-on-hold"></a>Placering af en kreditor i venteposition
Du kan placere en kreditor i venteposition for forskellige posteringstyper. Følgende valgmuligheder er tilgængelige:

-   **Nej** – Der er ikke placeret nogen spærringer for kreditoren.
-   **Faktura** – Der kan ikke bogføres fakturaer for kreditoren.
-   **Alle** – Kreditoren er sat på hold for alle transaktionstyper. Disse transaktionsstyper omfatter indkøbsrekvisitioner, fakturaer og betalinger.
-   **Betaling** – Der kan ikke genereres betalinger for kreditoren.
-   **Rekvisition** – Der kan kun oprettes indkøbsrekvisitioner. Der kan ikke oprettes andre transaktioner.
-   **Aldrig** – Kreditoren bliver aldrig sat på hold på grund af inaktivitet.

Når du sætter en kreditor på hold, kan du også angive en årsag og en dato, hvor ventepositionen ophører. Hvis du ikke angiver en slutdato, opretholdes ventepositionen på ubestemt tid.

## <a name="vendor-invoice-account"></a>Kreditorfakturakonto
Hvis mere end én kreditor har samme faktureringsadresse, eller hvis eb kreditor faktureres gennem en tredjepart, kan du angive en faktureringskonto i kreditorregistreringen. Fakturakontoen er den konto, som fakturabeløbet krediteres, når du opretter en kreditorfaktura fra en indkøbsordre. Hvis du ikke angiver en fakturakonto i kreditorregistreringen, bruges kreditorkontoen som fakturakonto.

## <a name="vendor-bank-accounts"></a>Kreditorbankkonti
Hvis du skal foretage betalinger til en kreditorbankkonto, kan du angive oplysninger om kreditorens bank og bankkonti på siden **Kreditorbankkonti**. Du kan også angive oplysninger om validering og betalinger for bankkontoen. Du kan f.eks. tilføje adviseringer til kreditorbankkonti. Disse adviseringer kan bruges til at bekræfte nøjagtigheden af kontooplysninger, som f.eks. registreringsnumre og kontonumre. Du skal angive en standardkonto for betalinger til kreditoren. Når du foretager en faktisk betaling, du kan dog ændre denne konto til en af leverandørens andre konti.

## <a name="ledger-accounts"></a>Finanskonti
Du kan angive standardkonti, som automatisk vises i fakturakladderne for den angivne kreditor. Denne funktion kan være nyttig, hvis du ofte betaler for den samme slags varer eller tjenester fra samme kreditorer over tid. Når du angiver en standardkonto, kan du hurtigt og nemt angive kladdeposter i fakturakladden. De standardkonti, du angiver, bruges ikke til indkøbsordrer eller til kreditorfakturaer, der er angivet på siden **Kreditorfaktura**.  

Du vælger standardkontiene på siden **Standardkontoopsætning**, som du kan åbne fra fanen **Faktura** i kreditorregistreringen. De konti, du vælger her, vises på den filtrerede liste over konti for kreditorgruppen, når du angiver en kladdepost. Du kan angive en af kontiene som en standardkonto.

