---
title: Tilføj eller Kopiér leasinger (prøveversion)
description: Denne artikel beskriver, hvordan du opretter en ny leasing ved at angive oplysninger om den i aktivleasing eller ved at kopiere oplysninger fra en eksisterende leasing.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880926"
---
# <a name="add-or-copy-leases-preview"></a>Tilføj eller Kopiér leasinger (prøveversion)

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan oprette en leasing fra bunden af aktivleasing, og hvordan du kan oprette en leasing ved at kopiere en eksisterende leasing. Processen til oprettelse af en leasing fra bunden omfatter angivelse af oplysninger til den nye leasing og oprettelse af en plan for leasing. Når der er konfigureret mindst én leasing, kan det være nemmere at kopiere oplysningerne fra en eksisterende leasing og derefter redigere disse oplysninger, når du har brug for at oprette en ny leasing.

## <a name="create-a-lease"></a>Oprette en leasing

Udfør følgende trin for at oprette en leasing i aktivleasing.

1. Gå til siden **Leasingoversigt**, og vælg **Ny** i handlingsruden.
2. Angiv oplysninger om leasing. De felter, der skal bruges, har røde kanter.

Startdatoen for leasingbetalingen må ikke være tidligere end startdatoen for leasing. Hvis du angiver en startdato for leasingbetalingen, der er før startdatoen for leasingen, får du vist en fejlmeddelelse.

Indstillingen **Opdeling af betalingsbeløb** i oversigtspanelet **Generelt** på siden **Leasingoplysninger** angives som standard til **Nej**, hvis indstillingen **Tillad opdeling af betaling** på siden **Parametre til aktivleasing** er angivet til **Ja**. 

Hvis indstillingen **Opdeling af betalingsbeløb** er angivet til **Ja**, låses feltet **Betalingsbeløb** i oversigtspanelet **Betalingsplanlinjer**. Det angives til summen af de betalingsbeløb, der angives senere i kataloget **Opdeling af betalingsbeløb**.

Vælg **Opdeling af betalingsbeløb** for at åbne en side, hvor du kan tilføje de specificerede betalingstyper. Knappen **Føj totaler til betalingsbeløb** flytter totalerne til feltet **Betalingsbeløb**.

> [!NOTE]
> Hvis du tilføjer et specificeret betalingsbeløb og derefter vælger **Esc**-tasten, føjes de angivne beløb ikke til feltet **Betalingsbeløb** i oversigtspanelet **Betalingsplanlinjer**. De gemmes i stedet i dialogboksen **Opdeling af betalingsbeløb**. Hvis du vil have vist totalbeløbet i dialogboksen, skal du vælge kolonnen **Beløb**, vælge og holde nede (eller højreklikke) og derefter vælge **Total for denne kolonne**. 

Knappen **Kopiér linje** kopierer den specificerede betalingsopdeling.

## <a name="create-a-lease-schedule"></a>Oprette en leasingplan

Når du er færdig med at angive oplysninger om en leasing, skal du udføre følgende trin for at oprette en leasingplan.

> [!NOTE]
> De økonomiske dimensioner kan ændres på baggrund af eventuelle brugerdefinerede økonomiske dimensioner.

1. Vælg **Opret planer** for at generere leasingkartotekerne. Leasingkartotekerne omfatter planerne for betaling, amortisering, afskrivning og repræsentationer.
2. Hvis du vil have adgang til leasingkartoteker og få vist de nyoprettede planer, skal du vælge fanen **Kartoteker**.

    På siden **Kartotekoplysninger** kan du se, hvordan rettigheden redegøres for de kartoteker, der er tildelt til den. Herfra kan du få vist planlægninger af leasingen.

    Betalingsplanen indeholder input fra fanen **Betalingsplanlinjer** på siden **Tilføj leasing**. Du kan stadig ændre hvert betalingsbeløb og variabel betaling. Leasingforpligtelsen beregnes på baggrund af den ændrede betalingsplan.

    > [!NOTE]
    > Startdatoen for leasingbetalingen skal være den samme som eller en senere dato end startdatoen for leasingen. Hvis startdatoen for leasingbetalingen er før startdatoen for leasingen, får du vist en fejlmeddelelse. 

4. Når du er færdig med at gennemse betalingsplanen, skal du vælge **Bekræft plan**. Når planen er bekræftet, er rettigheden ikke længere tilgængelig til redigering.

    > [!NOTE]
    > Systemet beregner automatisk leasingperioden fra betalingsplanlinjerne på siden **Tilføj leasing**.
    >
    > Hvis leasingperioden skal beregnes i måneder, finder systemet differencen mellem startdatoen og slutdatoen for en bestemt betalingsplanlinje. Der flyttes derefter til den næste betalingsplanlinje og finder differencen igen. Til sidst summerer systemet alle de beløb, der skal fastlægges for leasingperioden i måneder.

5. Hvis du vil have vist de beregnede perioders renteudgifter, skal du åbne siden **Amortiseringsplanen for leasingforpligtelse**. Hvis du vil have vist beregnede lineære afskrivninger, skal du åbne siden **Afskrivningsplan for aktiver**.
6. Når du er færdig med at gennemse det beregnede beløb, kan du oprette postering af den oprindelige genkendelseskladde på siden **Første indregning**. Du får vist en meddelelse om, at kladden er oprettet.

    > [!NOTE]
    > Kladdeposten bogføres ikke i Finans, før du bogfører posten manuelt.

7. Hvis du vil gennemse den foreslåede oprindelige genkendelsespost, før du bogfører den, skal du vælge **Aktivleasingkladde**.

    > [!NOTE]
    > Aktivleasingkladde kan ikke oprettes manuelt. Den oprettes automatisk, når der oprettes planlagte tidsplaner.

8. Når du er færdig med at gennemse journalposten for den oprindelige genkendelseskladde og er klar til at bogføre den, skal du vælge **Bogfør** for at genkende brugsretsaktivet (ROU) og rettighedspassiver i Finans.

## <a name="copy-a-lease"></a>Kopiere en leasing

Ved leasing af aktiver kan du kopiere oplysningerne til en leasing for at oprette en ny leasing, der har de samme oplysninger. Du kan derefter ændre leasingfelterne, før du opretter planerne for den kopierede leasing.

1. Vælg den leasing, der skal kopieres på siden **Leasingoversigt**, og vælg derefter **Kopiér leasing** i handlingsruden.

    > [!NOTE]
    > Hvis den **manuelle** parameter er slået fra for nummerserien for lease-id, oprettes det næste nummer i sekvensen automatisk som rettigheds-id for den kopierede leasing. Hvis parameteren **Manuel** er slået til, får du vist en meddelelse, hvor du bliver bedt om at angive et leasing-id, før du fortsætter med at kopiere leasingen.

2. Vælg **Kopiér**. Oplysningerne om leasingen for den valgte leasing kopieres til en ny leasing. Du kan derefter redigere oplysningerne om den nye leasing, før du gemmer den, og opretter planlægningen af leasing.

## <a name="asset-leasing-journal"></a>Aktivleasingkladde

Alle de kladdeposteringer, der er oprettet under Aktiv leasing, findes i Aktivleasingkladden. På siden **Aktivleasingkladde** (**Aktivleasing\> Kladdeposteringer \> Aktivleasingkladde**) kan du filtrere efter bogføringsstatus, få vist bestemte kladdeposteringer og bilag og bogføre ikke-bogførte kladdeposter.

> [!NOTE]
> Aktivleasingkladde kan ikke oprettes manuelt. Den oprettes automatisk, når der oprettes planlagte tidsplaner.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
