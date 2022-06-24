---
title: Overpluk for salgsordrer og flytteordrer
description: Denne artikel forklarer, hvordan du aktiverer overpluk af salgsordrer og flytteordrer.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b8bbc7d532f910edfb442831d6c906f253dee06c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897278"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Overpluk for salgsordrer og flytteordrer

[!include [banner](../includes/banner.md)]

Denne artikel viser et scenario for, hvordan du enten kan aktivere en bestemt arbejder eller alle arbejdere til overpluk. Overplukprocessen giver mulighed for kontrolleret overpluk under plukarbejdet.

Lagerstedsoverpluk er et simpelt begreb. Systemet giver arbejdere mulighed for at plukke flere varer, end der er angivet for en ordre. Det tager dog stadig højde for den overleveringsgrænse, der er angivet på linjeniveau for flytteordren eller salgsordren. Hvis denne grænse overskrides, får arbejderne via appen Warehouse Management besked om, at de overskrider overleveringsgrænsen.

Overpluk-funktionen er med til at minimere vedligeholdelsen og hjælper samtidig med, at opsætningen forbliver fleksibel. Du kan definere et eller flere menupunkter på en eller flere mobilenheder og kun aktivere overpluk for nogle af dem. Du kan også forhindre, at udvalgte arbejdere overplukker salgsordrer og/eller flytteordrer uden at skulle ændre menupunkterne. I stedet kan du deaktivere en eller begge egenskaber i de relevante arbejderopsætninger.

Funktionen til overpluk kan hjælpe arbejdere med at spare tid og kræfter, når de plukker og afsender varer. Funktionen giver f.eks. arbejdere mulighed for at udføre disse opgaver:

- Kompensere for svind under pluk eller forsendelse.
- Undgå at pakke noget emballage ud under plukprocessen.
- Kompensere for vareskade under transport.
- Afsende en afvigelse i antal eller måleenhed.
- Minimere opdelingen af antal på nummerplader.
- Undgå materialespild og mangel på kostbare materialer.
- Måle det plukkede antal efter plukning (f.eks. ved indvejning af fragtbil).

> [!IMPORTANT]
> Funktionen til overpluk gælder kun for salgsordrers og flytteordres pluk og behandling. Genopfyldning understøtter ikke overpluk. Når der køres genopfyldningsarbejde, vil brugerne ikke kunne overplukke.

Denne artikels scenarie viser, hvordan du kan konfigurere og bruge funktionen til overpluk.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Forudsætninger for scenario: Gøre demodata tilgængelige

Scenariet i denne artikel indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til *USMF*, før du går i gang.

## <a name="scenario-setup"></a>Konfigurere scenarie

Før du gennemgår eksempelscenariet, skal du aktivere overpluk for både den relevante arbejder og det relevante menupunkt.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Konfigurere en arbejder til at tillade overpluk

Her er den generelle procedure for konfiguration af en arbejder, så der aktiveres overpluk for salgsordrer og flytteordrer separat. Denne konfiguration bestemmer, hvilken plukarbejder der kan udføre overpluk, og om den pågældende arbejder kan udføre overpluk af både flytteordrer og salgsordrer.

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejder**.
1. Vælg **Julia Funderburk** i listeruden.
1. Vælg rækken med følgende værdier i oversigtspanelet **Brugere**. Hvis der ikke allerede findes en række med disse værdier, skal du oprette den.

    - **Bruger-id:** *24*
    - **Brugernavn:** *WH 24*
    - **Standardlagersted:** *24*
    - **Menunavn:** *Hoved*

1. Angiv følgende værdier for bruger *24* i oversigtspanelet **Arbejde**, hvis de ikke allerede er angivet:

    - **Tillad salg over pluk:** *Ja*
    - **Tillad flytteordre over pluk:** *Ja*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Konfigurere et menupunkt for mobilenheden for at tillade overpluk

Her er den generelle procedure for konfiguration af et menupunkt på en mobilenhed for at aktivere overpluk. Afhængigt af dine forretningskrav for tilladelsesniveauet for den arbejder, der skal bruge menuen på mobilenheden, kan nogle parametre være slået til eller fra.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg den post, der hedder *Salgspluk*, i listeruden. Hvis der ikke findes en eksisterende post med dette navn, skal du oprette den. Bekræft eller angiv følgende værdier for posten:

    - **Menupunktnavn:** *Salgspluk*
    - **Titel:** *Salgspluk*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Ja*
    - **Styret af:** *Brugerstyret*
    - **Tilsidesæt mål-id:** *Ja*
    - **Tilsidesæt nummerplade under læg på lager:** *Ja*
    - **Hold arbejde låst af bruger:** *Ja*
    - **Tillad overpluk:** *Ja*

> [!IMPORTANT]
> Når de relevante parametre for både arbejderen og menupunktet for mobilenheden er aktiveret, kan overpluk kun behandles via mobilenheden.

## <a name="example-scenario"></a>Eksempelscenario

Når forudsætningerne, opsætningen af arbejder og opsætningen af menupunkt er på plads, er du klar til at arbejde med funktionen.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Oprette en salgsordre, der giver mulighed for overlevering

1. Gå til **Sales and MArketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en ny salgsordre.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *24*

1. Vælg **OK**.
1. Den nye indkøbsordre åbnes. I oversigtspanelet **Salgsordrelinjer** skal du tilføje en linje, der har følgende indstillinger:

    - **Varenummer:** *A0001*
    - **Antal:** *10*

1. I oversigtspanelet **Linjedetaljer** under fanen **Levering** skal du angive feltet **Overlevering** til *10*.
1. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.
1. Luk siden **Reservation**.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

Når frigivelsen er fuldført, modtager du orienterende meddelelser, der viser bølgen og last-id'et, der blev oprettet.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Hent arbejds-id'et og id-nummeret til den nye ordre

Når du har frigivet salgsordren til lagerstedet, skal systemet have oprettet et nyt arbejds-id, der har én pluklinje. Udfør følgende trin for at finde arbejds-id'et og id-tildelingen.

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. Søg i gitteret **Oversigt** efter den salgsordre, du netop har oprettet, i kolonnen **Ordrenummer**. Notér dig arbejds-id'et for denne salgsordre.
1. Markér rækken for den nye salgsordre for at få vist relaterede oplysninger i **Linjer**-gitteret. Notér dig den lokation, som varen skal plukkes fra.
1. Gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**.
1. Vælg **Dimensioner** i handlingsruden.
1. I dialogboksen **Dimensionsvisning** skal du sørge for, at afkrydsningsfelterne **Id**, **Lagersted** og **Varenummer** er markeret, og vælg derefter **OK**.
1. I **Filter**-ruden skal du angive følgende filtre:

    - **Varenummer** – **er en af** – *A0001*
    - **Lagersted** – **begynder med** – *24*

1. Vælg **Anvend**.
1. Notér dit de viste værdier af **Id**.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Overplukke ordren ved hjælp af mobilappen Warehouse Management

1. Log på mobilappen Lokationsstyring som en bruger på lagersted *24*.
1. Gå til **Udgående \> Salgsplukning**.
1. Angiv det arbejds-id, der blev oprettet for salgsordren, i feltet **Scan arbejds-id eller nummerplade**.
1. Vælg **OK** (markeringssymbol).
1. Vælg **Overpluk**.
1. Angiv feltet **Plukantal** til *14*.
1. Vælg **OK** (markeringssymbol).

    På siden **Overpluk** modtager du følgende meddelelse: "Overlevering af linje er 40,00 procent, men den tilladte overlevering er kun 10,00 procent." Denne meddelelse angiver, at det plukantal, du har angivet, overskrider overleveringsgrænsen. Overleveringsgrænsen for salgsordrelinjen er 10 procent. For et angivet antal på 10 kan du derfor kun overplukke med 1 for et samlet plukantal på 11.

1. Angiv feltet **Plukantal** til *11*.
1. Vælg **OK** (markeringssymbol).
1. Angiv den nummerplade, du noterede i forrige afsnit, i feltet **Nummerplade**.
1. I feltet **Mål-id** skal du angive et målnummerplade-id. Bemærk, at pluklokationen (*FLOOR-001*), vare (*A0001*) og antal (*11 stk.*) vises.
1. Vælg **OK** (markeringssymbol).
1. Gennemse oplysningerne på siden **Salgsordrer – læg på lager**. Feltet **Lok** skal angive, at de plukkede varer skal placeres på lokationen *BAYDOOR*.
1. Vælg **OK** (markeringssymbol).

På siden **Scan et arbejds-id/nummerplade-id** modtager du en meddelelse om, at "Arbejde er fuldført". Denne meddelelse angiver, at arbejds-id'et for salgsordren er fuldført, og at det overplukkede antal ikke overskrider overleveringsgrænsen på 10 procent.
