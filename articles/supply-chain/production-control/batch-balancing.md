---
title: Batchtilpasning
description: Denne artikel beskriver batchtilpasningsprocessen.
author: johanhoffmann
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 50392e8aa0deb568a57e1df59ced70625a4f8a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856042"
---
# <a name="batch-balancing"></a>Batchtilpasning

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan batchtilpasningsprocessen understøttes.

Hvis du ønsker flere oplysninger, kan du se en [video om batchtilpasning](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

I batchtilpasningsprocessen beregnes mængden af stoffer, der skal bruges i et produktionsbatch, ud fra koncentrationen af aktive stoffer i de valgte produktbatchnumre.

## <a name="products-that-have-an-active-ingredient"></a>Produkter, der har et aktivt stof

Et produkt kan defineres ud fra dets koncentration af et aktivt stof. Det aktive stof i et produkt modelleres ved hjælp af en produktspecifik batchattribut, der har en minimumværdi, en maksimumværdi og et målniveau.

En batchattributs målniveau repræsenterer den anslåede procentdel af et aktivt stof i et produkt. Minimum- og maksimumværdierne repræsenterer den accepterede afvigelse fra målniveauet. De kan bruges f.eks. som en accepteret tolerance for batchnumre ved produktkvittering.

Et produkt kan kun have ét aktivt stof. Når du vil angive det aktive stof for et produkt, skal du først definere en produktspecifik batchattribut. Du kan derefter tilknytte attributten som en basisattribut for produktet.

På produktniveau skal du også angive, hvordan niveauet af det aktive stof for en batch af produktet skal registreres: som en del af indkøbstilgangsprocessen eller som en del af en kvalitetsordreprocessen.

Hvis du vil knytte en basisattribut til et produkt, kræves følgende opsætning:

- Produktet skal være batchstyret. Du kan gøre et produkt batchstyret ved at tildele en sporingsdimensionsgruppe til det produkt, der har en aktiv batchdimension.

- Den attribut, der angiver stofniveauerne, skal være defineret som en produktspecifik batchattribut for produktet.

Sådan søger du efter og redigerer den faktiske værdi af det aktive stof til en batch:
1. Gå til **Lagerstyring \> Forespørgsler og rapporter \> Sporingsdimensioner \> Batches**.
1. Vælg et batchnummer i gitteret.
1. Åbn fanen **Vis** i handlingsruden, og vælg derefter **Lagerbatchattributter**.

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Typer af stoffer, og hvordan de indgår i batchtilpasningsprocessen

En formellinje, der oprettes, kan have en af disse stoftyper:

- None
- Aktive
- Kompenserer
- Fyld

Resten af dette afsnit indeholder eksempler på, hvordan hver stoftype fungerer. Eksemplerne er baseret på følgende formel, der har en samlet batchstørrelse på 100 liter.

| Stoftype | varenummer | Formellinjeantal | Enhed |
|---|---|---|---|
| None | T | 20 | Liter |
| Aktive | B | 30 | Liter |
| Kompenserer | K | 10 | Liter |
| Fyld | N | 40 | Liter |

Følgende tabel indeholder en oversigt over resultaterne af hvert eksempel.

| varenummer | Ingredienstype | Estimeret antal | Afstemt antal | Aktivt antal | Enhed | Basisværdi |
|---|---|---|---|---|---|---|
| T | None | 20 | 20 | | Liter | |
| L | Aktive | 30 | 25,71 | 9,00 | Liter | 30.00 |
| K | Kompenserer | 10 | 14.72 | | Liter | |
| N | Fyld | 40 | 39.57 | | Liter | |

### <a name="active-ingredients"></a>Aktive stoffer

Når et produkt, der har en basisattribut, føjes til en formellinje, kaldes det et *aktivt stof* i formlen. Batchordrer, der har formler, som indeholder aktive stoffer, kan bruges til batchtilpasningsprocessen. For hvert stof i formlen beregner batchtilpasningsprocessen den mængde, der kræves for at fremstille produktet. Beregning af mængderne er baseret på koncentrationen af aktive stoffer i de valgte batchnumre.

#### <a name="active-ingredient-example"></a>Eksempel på aktivt stof

Stof B har basisattributten X og et målniveau på 30, og det medtages i en formel, der kræver 30 liter af stof B for hver 100 liter af produktet. Der oprettes en batchordre, der har en batchstørrelse på 100 liter. Batchordren startes, og under batchtilpasningsprocessen vælger brugeren en batch af stof B, der har et styrkeniveau på 35. Da styrkeniveauet for 35 ligger over målniveauet på 30, reduceres den tilpassede mængde af stof B ved hjælp af forholdet mellem styrkeværdien og målniveauet for batchen, ganget med den forkalkulerede mængde. Beregningen af den tilpassede mængde ser sådan ud:

(30 ÷ 35) × 30 liter = 25,71 liter

### <a name="none-ingredients"></a>Ingen stoffer

Når du anvender batchtilpasningsprocessen, og **stoftypen** er *Ingen*, er den forkalkulerede mængde og den tilpassede mængde på formellinjen i batchordren ens.

#### <a name="none-ingredient-example"></a>Eksempel på intet stof

Stof A tildeles til e stof af typen *None* og føjes til en formel for et færdigt produkt. Formlen kræver 10 liter af stof A for hver 100 liter af det færdige produkt. Når en batchordre kræver 200 liter, beregnes både den forkalkulerede mængde og den tilpassede mængde af stof A som 20 liter.

### <a name="compensating-ingredients"></a>Kompenserende stoffer

Et kompenserende stof kan enten forskyde eller supplere effekten af det aktive stof i et produkt. Derfor afhænger mængden af det kompenserende stof, der forbruges, af styrken af produktet:

- **Modsatrettet effekt** – Hvis mængden af det aktive stof er større end forventet, skal du tilføje mindre af det kompenserende stof.

- **Supplerende effekt** – Hvis mængden af det aktive stof er mindre end forventet, skal du tilføje mere af det kompenserende stof.

Relationen mellem et aktivt stof og et supplerende stof konfigureres på siden **Kompensationsprincip**.

Benyt følgende fremgangsmåde for at konfigurere forhold mellem stoffer.

1. Vælg **Administration af produktionsoplysninger \> Styklister og formler \> Formler**.
1. Åbn en formellinje, og vælg derefter **Stoffer** for at åbne siden **Kompensationsprincip**.
1. Vælg den linje, der repræsenterer et kompensationsprincip, og vælg derefter det aktive stof, der skal kompenseres.

Du kan også angive en positiv eller negativ kompensationsfaktor i kompensationsprincippet for at angive, hvor meget der skal kompenseres for, og om princippet skal være modsatrettet eller supplerende. En positiv faktor angiver en supplerende effekt, og en negativ faktor angiver en modsatrettet effekt.

#### <a name="compensating-ingredient-example"></a>Eksempel på kompenserende stof

Stof B er et aktivt stof, der har basisattribut X og et målniveau 30. Det indgår i en formel, der kræver 30 liter af stof B for hver 100 liter af produktet. Stof C er et kompenserende stof, og en mængde på 10 er inkluderet i den samme formel. En kompenserende faktor på 1,10 er angivet for kompensationsprincippet. Derfor reduceres den tilpassede mængde af det kompenserende stof med differencen mellem det aktive stofs tilpassede mængde og den anslåede krævede mængde ganget med 1,10.

I eksemplet for stoftypen *Aktiv* blev den tilpassede mængde af det aktive stof, der krævedes, beregnet til 25,71, og det anslåede krævede mængde blev beregnet til 30. I dette tilfælde beregnes den tilpassede mængde af det kompenserende stof som følger:

1. Forskellen mellem den beregnede og den tilpassede mængde bestemmes:  
    25,71 - 30 = - 4,29

1. Resultatet ganges derefter med kompensationsfaktoren:  
    4,29 × 1.10 = - 4,72

1. Den forkalkulerede kompensationsmængde reduceres med - 4,72 for at bestemme den tilpassede kompensationsmængde:  
    10 - (- 4,72) = 14,72

Da 1,10 er en positiv kompensationsfaktor, har dette kompensationsprincip en supplerende effekt. I dette tilfælde er det aktive stof mere effektivt end forventet. Derfor er mere af det kompenserende stof påkrævet.

### <a name="filler-ingredients"></a>Fyldstoffer

Et *fyldstof* er et neutralt stof, der bruges til at nå den ønskede afgangsmængde for det færdige produkt. Reguleringer af mængden af fyldstoffet beregnes ud fra variationer i det aktive stof og det kompenserende stof sammenlignet med standardmængden.

#### <a name="filler-ingredient-example"></a>Eksempel på fyldstof

Du har udarbejdet et produkt, som indeholder ingredienser A, B, C og D for en formelstørrelse på 100 liter. Du har beregnet den tilpassede mængde af alle stoftyper undtagen stoftypen *Fyld*, som bruges på én linje.
Den tilpassede mængde af fyldstoffet beregnes som forskellen mellem batchstørrelsen på 100 liter, og summen af stofferne A, B og C:

100 - (20 + 25,71 + 14,72) = 39,57

## <a name="the-batch-balancing-process"></a>Batchtilpasningsprocessen

Batchtilpasningsprocessen udføres fra siden **Batchtilpasning**.
Vælg **Omkostningsstyring \> Batchordrer**, og vælg derefter **Batchtilpasning** under fanen **Proces**. Batchtilpasning er tilgængelig for batchordrer, der har status **Startet**.

Generelt kan batchtilpasning anvendes på batchordrer, hvis formlen har mindst én formellinje, hvor **Stoftype** er *Aktiv*. (Du kan se en undtagelse fra denne regel i afsnittet "Batch ordrer, der ikke kan anvendes til batchtilpasning" senere i denne artikel).

Batchtilpasningsprocessen kan opdeles i to underprocesser:

1. Afstem batchstoffer
1. Bekræft og frigiv formlen

### <a name="balance-batch-ingredients"></a>Afstem batchstoffer

I underprocesserne til afstemning af batchstofferne beregnes mængden af stoffer, der skal bruges til et produktionsbatch, ud fra de valgte batchnumre, der har aktive stoffer. Som hovedregel kan beregningen kun fuldføres, hvis der er fuld dækning for alle stoffer. Du kan ikke kun tilpasse en del af det batch, som batchordren er konfigureret til at producere.

> [!NOTE]
> Du kan ikke gemme en beregning og derefter fuldføre kørslen af batchtilpasningsprocessen senere. Hvis du lukker siden **Batchtilpasning**, skal du gentage beregningen for at fuldføre processen.

### <a name="confirm-and-release-the-formula"></a>Bekræft og frigiv formlen

Når stofmængderne er beregnet, kan du bekræfte og frigive formlen. Frigivelsesprocessen varierer, afhængigt af om produkterne er aktiveret til lokationsstyringsprocesserne:

- Hvis et produkt er aktiveret til lokationsstyringsprocesserne, frigives formellinjen til lagerstedet i overensstemmelse med principperne for lokationsstyringsprocesserne. Formellinjen frigives i mængder, der svarer til de mængder, der er afstemt, og den er frigives for bestemte batchkørsler, der er valgt for de aktive stoffer.

    > [!NOTE]
    > Formellinjer kan kun frigives til lagerstedet som del af batchtilpasningsprocessen. Selvom der er andre muligheder for frigivelse af produktionsmaterialer til lagerstedet, kan de ikke bruges til formellinjerne.

- Hvis et produkt ikke er aktiveret til lokationsstyringsprocesserne, oprettes en plukliste til produktion for produktet, når du bekræfter og frigiver formlen.

I en enkelt formel kan du kombinere produkter, der er aktiveret til lokationsstyringsprocesser, og produkter, der ikke er aktiveret til lokationsstyringsprocesser. Når de to typer produkter medtages i én formel, frigives de produkter, der er aktiveret til lokationsstyringsprocesser, til lagerstedet. For de produkter, der ikke er aktiveret til lokationsstyringsprocesserne, oprettes en plukliste, når formlen er bekræftet og frigivet.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Batchordrer, der ikke kan anvendes til batchtilpasning

Der er to undtagelser til reglen om, at batchordrer kan anvendes til batchtilpasning, hvis formlen har mindst én formellinje, hvor **Stoftype** er *Aktiv*.

1. Hvis en formel indeholder et aktivt stof for et produkt, der er aktiveret til lokationsstyringsprocesser, men batchnummeret er under lokation i reservationshierarkiet, kan batchtilpasning ikke bruges på batchordren.
1. Hvis formelmåleenheden er forskellig fra det aktive stofs lagermåleenhed, kan batchordren ikke anvendes til batchjustering.

En batchordre, der ikke er tilgængelig for batchtilpasning, gennemgår den almindelige procescyklus for batchordrer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]