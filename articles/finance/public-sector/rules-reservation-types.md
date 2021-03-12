---
title: Konfigurere regler for generel budgetreservation og reservationstyper
description: I dette emne beskrives, hvordan du kan konfigurere og redigere regler for generelle budgetreservationer og reservationstyper til den offentlige sektor.
author: AlexRenney
manager: AnnBe
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetReservation_PSN, BudgetReservationType_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: ec41dc28e9f833896e26f07f807c59f2423710ed
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978193"
---
# <a name="set-up-general-budget-reservation-rules-and-reservation-types"></a>Konfigurere regler for generel budgetreservation og reservationstyper

[!include [banner](../includes/banner.md)]

Offentlige institutioner bruger ofte generelle budgetreservationer til at sætte budgetterede midler til side eller øremærke dem, så de ikke er tilgængelige til andre formål. Hvis du vil bruge generelle budgetreservationer, skal du angive budgetregler, og du skal oprette mindst én generel budgetreservationstype.

> [!NOTE]
> Hvis din organisation er i Frankrig, bruger du forpligtelser i stedet for generelle budgetreservationer.

Følgende illustration viser, hvordan du konfigurerer systemet til at bruge generelle budgetreservationer. Hvert nummereret trin svarer til et afsnit i dette emne.

![Opsætning af generel budgetreservation](media/gbr-rules-reservations-process.jpg "Opsætning af generel budgetreservation")

## <a name="prerequisites"></a>Forudsætninger

Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.

<table>
<thead>
<tr>
<th>Kategori</th>
<th>Forudsætning</th>
</tr>
</thead>
<tbody>
<tr>
<td>Relaterede konfigurationsopgaver</td>
<td>
<ul>
<li>Du skal bruge bogføringsdefinitioner, medmindre du ikke aktiverer rammeaftaler.</li>
<li>Konfiguration af budgetstyring skal være aktiveret, budgetstyring skal være slået til, og et oprindeligt budget skal være bekræftet.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-budgeting-parameters-for-regulatory-accounting"></a>Konfigurere budgetparametre for lovmæssig regnskabsførelse

Benyt følgende fremgangsmåde for at konfigurere budgetparametre for lovmæssig regnskabsførelse.

1. Gå til **Budgettering \> Opsætning \> Grundlæggende budgettering \> Budgetparametre**.
2. Under fanen **Budget** på oversigtspanelet **Lovpligtig** skal du vælge **Ja** i indstillingen **Generelle budgetreservationer**.
3. Valgfrit: I oversigtspanelet **Behæftelseskontrol** kan du vælge **Ja** i indstillingerne **Forhindre stigninger i overført behæftelse** og **Brug sessionsdato til GBR-regnskab**.
4. Valgfrit: Vælg **Ja** i indstillingen **Tillad rettelser i tidligere år** i oversigtspanelet **Rettelser i tidligere år af generel budgetreservation**.

## <a name="select-source-documents-for-budget-control"></a>Vælg kildedokumenter til budgetstyring

Du kan øremærke budgetmidler til denne indkøbsmetode ved at konfigurere den generelle budgetreservation som et kildedokument. 

Benyt følgende fremgangsmåde for at vælge kildedokumenter.

1. Gå til **Budgettering \> Opsætning \> Budgetstyring \> Konfiguration af budgetstyring**.
2. Vælg **Opret kladde**.
3. Under fanen **Dokumenter og kladder** skal du markere afkrydsningsfelterne **Generel budgetreservation** og **Kontroller på linjepost**.
4. Under fanen **Aktivér budgetstyring** skal du vælge **Aktivér**.

Når du opretter en generel budgetreservation, oprettes der også budgetkildesporingsposter og ledsagende budgetkontrolresultater, og der forekommer budgetkontrol, når du opretter en linje eller bogfører en reservation.

## <a name="set-up-general-ledger-information-for-general-budget-reservations"></a>Konfigurere finanskontioplysninger for generelle budgetreservationer

Som et led i at sikre, at finanskonti er angivet korrekt, skal du konfigurere, hvordan generelle budgetreservationer bruges til at registrere regnskabsmæssige forpligtelser.

Benyt følgende fremgangsmåde for at konfigurere finanskontioplysninger for generelle budgetreservationer.

1. Gå til **Finans \> Opsætning Finans \> Finansparametre**.
2. Under fanen **Finans** i oversigtspanelet **Konteringsregler** skal du vælge **Ja** i indstillingen **Brug bogføringsdefinitioner**. Vælg **Ja** i den bekræftelsesmeddelelsesboks, der vises.
3. Marker afkrydsningsfeltet **Generelle budgetreservationer**. Luk derefter beskeden.

    Når du markerer afkrydsningsfeltet **Generelle budgetreservationer**, markeres afkrydsningsfelterne **Aktiver behæftelse** og **Aktivér proces for budgetreservationer** automatisk og er ikke tilgængelige. Disse to processer skal bruges, når der anvendes generelle budgetreservationer.

## <a name="create-posting-definitions"></a>Oprette bogføringsdefinitioner

Du kan konfigurere posteringsbogføringsdefinitioner for at opdatere forskellige finanskonti for forskellige typer af generel budgetreservation.

Benyt følgende fremgangsmåde for at oprette bogføringsdefinitioner for generelle budgetreservationer.

1. Gå til **Finans \> Opsætning af bogføring \> Bogføringsdefinitioner**.
2. Vælg **Ny**.
3. I feltet **Bogføringsdefinition** skal du angive en kort kode for definitionen (f.eks. **GBREnc**).
4. Indtast en beskrivelse (f.eks. **GBR-behæftelse**) i feltet **Beskrivelse**.
5. Vælg **Budgetreservation** i feltet **Modul**.
6. Angiv de resterende felter på siden efter behov.
7. Vælg **Definitioner af posteringsbogføring** i gruppen **Vis** under fanen **Bogføringsdefinition** i handlingsruden.
8. På siden **Definitioner af posteringsbogføring** under fanen **Budgetreservation** i feltgruppen **Vælg** er **Generel budgetreservation** valgt som standard. Vælg **Ultimo ved årsafslutning for generel budgetreservation**, hvis denne indstilling er relevant.
9. Vælg **Ny**.
10. Vælg en af følgende værdier i feltet **Reservationstype**.

    - Hvis du vil angive en ny posteringsbogføringsdefinition, der gælder for alle reservationstyper, skal du vælge **Alle**. I feltet **Bogføringsdefinition** skal du vælge den definition, som du oprettede tidligere i dette emne.
    - Hvis du vil angive en ny posteringsbogføringsdefinition, der gælder for en enkelt reservationstype, skal du vælge **Tabel**. Vælg derefter skal du vælge en reservationstype i feltet **Reservationstyperelation**. I feltet **Bogføringsdefinition** skal du derefter vælge den definition, som du oprettede tidligere i dette emne.

11. Gentag trin 2-10 for at oprette så mange andre bogføringsdefinitioner, som du har brug for, og vælg derefter **Luk**.

## <a name="set-up-the-reservation-number-sequence"></a>Konfigurere nummerserie for reservation

Benyt følgende fremgangsmåde, hvis du vil konfigurere den nummerserie, som generelle budgetreservationer bruger.

1. Gå til **Budgettering \> Opsætning \> Grundlæggende budgettering \> Budgetparametre**.
2. Vælg posten for generelle budgetreservationer i kolonnen **Reference** under fanen **Nummerserier**.
3. Vælg en kode i kolonnen **Nummerseriekode**.

    Du kan også tildele entydige nummerserier efter reservationstype.

## <a name="create-a-general-budget-reservation-type"></a>Oprette en generel budgetreservationstype

Reservationstypen bestemmer arten af en generel budgetreservation, f.eks. den type dokument, der eftergiver budgetreservation, den arbejdsgang, der bruges til at godkende reservationen, og den nummerserie, der bruges.

Benyt følgende fremgangsmåde, hvis du vil oprette en generel budgetreservationstype.

1. Gå til **Budgettering \> Opsætning \> Generelle budgetreservationer \> Reservationstype**.
2. Vælg **Ny**.
3. Angiv et navn til reservationstypen i feltet **Reservationstype**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. I feltet **Eftergivelsesdokument** er **Indkøbsrekvisition** valgt som standard. Vælg en anden værdi efter behov. I dette felt angives den type dokument, der skal eftergive den generelle budgetreservation.

    > [!NOTE]
    > Når du har oprettet en generel budgetreservation ved hjælp af reservationstypen, kan du ikke ændre reservationen til en anden type.

6. I oversigtspanelet **Overført budget** skal du vælge **Ja** i indstillingen **Reducer overført budget**, hvis resterende overførte budget, der er knyttet til en generel budgetreservation, skal reduceres til 0 (nul), når reservationen er færdig.
7. Valgfrit: Hvis der kræves en godkendelsesopgave eller en anden opgave, før reservationen kan bogføres, skal du vælge en arbejdsgang for generel budgetreservation i feltet **Arbejdsgang** i oversigtspanelet **Arbejdsgang**. Hvis du ikke udfylder dette felt, er en arbejdsgang ikke påkrævet for at kunne bogføre generelle budgetreservationer af denne type.
8. Valgfrit: Hvis der er flere reservationstyper med entydige nummerserier, skal du vælge den nummerseriekode, som denne reservationstype skal bruge, i oversigtspanelet **Nummerserie** i feltet **Nummerseriekode**.

    Hvis der ikke er konfigureret en nummerserie til en reservationstype, bruges nummerserien for budgetparametre.

9. Gentag trin 2-8 for at oprette evt. yderligere reservationstyper, du har brug for.

## <a name="next-step"></a>Næste trin

Når du har oprettet regler, kan du oprette generelle budgetreservationer. De generelle budgetreservationer gælder for de dokumenter, der er nødvendige for den indkøbsmetode, som du vælger (indkøbsrekvisition, indkøbsordre eller kreditorfaktura).

## <a name="technical-information-for-system-administrators"></a>Tekniske oplysninger til systemadministratorer

Hvis du ikke har adgang til de sider, der bruges til at fuldføre denne opgave, skal du kontakte din systemadministrator og angive de oplysninger, der vises i følgende tabel.

| Kategori                  | Forudsætning                                                  |
|---------------------------|---------------------------------------------------------------|
| Licenskonfigurationsnøgle | Offentlig sektor \> Generel budgetreservation                   |
| Sikkerhedsroller            | Du skal være medlem af sikkerhedsrollen **Budgetchef**. |
