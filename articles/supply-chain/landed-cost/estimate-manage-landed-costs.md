---
title: Estimere og administrere landingsomkostninger
description: Systemet bruger din automatiske omkostningsopsætning til at fastlægge et estimat for dine landingsomkostninger. Denne artikel forklarer, hvordan du kan definere forskellige scenarier for at få et mere præcist estimat.
author: Weijiesa
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2e7cdd7c7439a24ec75a59bcee1e8f42f37bb2cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854435"
---
# <a name="estimate-and-manage-landed-costs"></a>Estimere og administrere landingsomkostninger

[!include [banner](../../includes/banner.md)]

Systemet bruger din [automatiske omkostningsopsætning](auto-cost-setup.md) til at fastlægge et estimat for dine landingsomkostninger. Du kan også definere forskellige scenarier for at få et mere præcist estimat. Disse scenarier gemmes. Du kan derfor gennemgå dem senere og sammenligne dem med faktiske data i en rapport. Du kan også opdatere varens pris.

## <a name="set-up-cost-estimates"></a>Konfigurere omkostningsestimater

### <a name="set-up-cost-templates"></a>Konfigurer omkostningsskabeloner

Omkostningsskabeloner opretter standardindstillinger, som de brugere, der får estimatet, ikke nødvendigvis kender til. Skabeloner kan være med til at reducere kompleksiteten i estimeringsprocessen ved at minimere de valg, brugerne skal angive for at opnå et præcist estimat. Hvis du bruger standardomkostningsmodellen, kan du bruge omkostningsskabeloner, mens du konfigurerer vareomkostningerne.

Du kan konfigurere dine omkostningsskabeloner ved at gå til **Landingsomkostninger \> Opsætning af efterkalkulation \> Omkostningsskabeloner**. På siden **Omkostningsskabeloner** viser listeruden til venstre alle aktuelle omkostningsskabeloner. Du kan oprette, fjerne og redigere skabeloner ved at bruge knapperne i handlingsruden.

I følgende tabel forklares de felter, der er tilgængelige for hver skabelon.

| Felt | Beskrivelse |
|---|---|
| Omkostningsskabelon | Angiv et entydigt navn til omkostningsskabelonen. Navnet beskriver typisk faktoren eller omkostningsmultiplikatoren for skabelonen. |
| Beskrivelse | Angiv en beskrivelse af omkostningsskabelonen. |
| Fragtfirma | Vælg det fragtfirma, der skal anvendes, når skabelonen bruges. |
| Leveringsmåde | Vælg den leveringsmåde, f.eks. skibs- eller luftfragt, der skal anvendes, når skabelonen bruges. Dette felt hjælper med at bestemme de automatiske omkostninger, der er knyttet til varerne i et omkostningsestimat. |
| Forsendelsescontainertype | Vælg den type af forsendelsescontainer, der skal anvendes, når skabelonen bruges. Dette felt hjælper med at bestemme de automatiske omkostninger, der er knyttet til varerne i et omkostningsestimat. |
| Toldmægler | Toldmægleren (leverandøren), der skal anvendes, når skabelonen bruges. Dette felt hjælper med at bestemme de automatiske omkostninger, der er knyttet til omkostningsestimatet. |
| Faktor | Angiv den multiplikator (procent), der automatisk skal anvendes for omkostningsestimatet, når skabelonen anvendes. Hvis du f.eks. vil lægge 10 procent til det beregnede omkostningsestimat, skal du angive *1,10*. |

### <a name="create-a-cost-estimate"></a>Oprette en omkostningsestimat

Brug dialogboksen **Omkostningsestimat** til at generere et nyt omkostningsestimat, der er baseret på en valgt omkostningsskabelon, et valgt sæt af varer og andre detaljer om en rejse. Disse indstillinger bruges derefter til at bestemme de estimerede landingsomkostninger for varer. Disse omkostningsestimater bruges primært til at arbejde med varer med standardomkostninger. Hvis du lægger de forkalkulerede landingsomkostninger til standardomkostningerne for varer på lageret, skulle du opleve mindre afvigelsestransaktioner, når varerne føjes til en fragt, da standardomkostningen afspejler estimaterne for disse landingsomkostninger.

Du kan åbne dialogboksen **Omkostningsestimat** ved at gå til **Landingsomkostninger \> Periodiske opgaver \> Omkostningsestimat**. Derefter skal du angive felterne som beskrevet i følgende underafsnit. Vælg til sidst **OK** for at oprette estimatet. Siden **Omkostningsestimat** (**Landingsomkostninger \> Forespørgsler \> Omkostningsestimater**) vises derefter med det nye estimat, som beskrevet senere i denne artikel.

### <a name="settings-on-the-parameters-tab"></a>Indstillinger under fanen Parametre

I følgende tabel beskrives de felter, der er tilgængelige under fanen **Parametre** i dialogboksen **Omkostningsestimat**.


| Felt | Beskrivelse |
|---|---|
| Omkostningsskabelon | Vælg en omkostningsskabelon. De indstillinger, der er knyttet til den valgte skabelon, bruges til at bestemme, hvilke automatiske omkostninger der anvendes. |
| Estimatdato | Dette felt er som standard angivet til dags dato, men du kan ændre værdien. Den angivne dato bruges til at vælge de relevante salgspriser, indkøbspriser, automatiske omkostninger og valutakursen, hvis der bruges en forsendelsessats. |
| Mål | Omkostninger kan afhænge af et mål. Ved brug af luftfragt kan der f.eks. anvendes volumenprissætning. Hvis omkostningen afhænger af et mål, skal du angive værdien af dette mål. Ellers anbefales du at angive dette felt til *1*, medmindre du er sikker på, at der ikke forekommer en fordeling ved hjælp af mål. Angiv en decimalværdi. Enheden er den, der er defineret i den relevante automatiske omkostningspost. |
| Rejseskabelon | Vælg en [rejseskabelon](multi-leg-journey-setup.md). Dette felt bruges til at bestemme de korrekte automatiske omkostninger, der skal anvendes. |
| Fra havn | Den havn, som varerne vil blive afsendt fra. Dette felt angives på baggrund af den valgte rejseskabelon. |
| Til havn | Den havn, som varerne vil blive afsendt til. Dette felt angives på baggrund af den valgte rejseskabelon. |
| Valuta | Vælg den valuta, som varerne købes i. |
| Containere | Hvis der typisk bruges flere containere, skal du angive antallet af containere. Systemet vil derefter bruge omkostninger for flere containere, når omkostningerne estimeres. |
| Specifikationer | Hvis der typisk bruges flere folioer, skal du angive antallet. (Antallet er normalt *1*). |
| Lokation | Angiv den lokation, hvor varerne skal leveres. |

### <a name="settings-on-the-items-tab"></a>Indstillinger under fanen Varer

Under fanen **Varer** kan du føje så mange varer til estimatet, som der er brug for. Brug værktøjslinjen til at føje varer til gitteret eller fjerne varer. Vælg **Lager \> Vis dimensioner** på værktøjslinjen for at åbne en dialogboks, hvor du kan føje dimensionskolonner til gitteret eller fjerne kolonner.

I følgende tabel forklares de felter, der er tilgængelige for hver vare.

| Felt | Beskrivelse |
|---|---|
| varenummer | Vælg den vare, prisen skal bestemmes for. (Hvis varen endnu ikke findes i systemet, skal du oprette en dummy-vare, eventuelt knytte den til en vareomkostningsgruppe for fragt og derefter enten lade prisen være tom eller oprette eller ændre prisen). |
| Kreditorkonto | Vælg den leverandør, der skal bruges til estimatet af denne vare. Hvis varen er tildelt en standardleverandør, udfyldes feltet automatisk. |
| Kvantitet | Vælg det antal, du vil indkøbe. |
| Kostpris | Systemet bruger dets prissætningsregler til at finde en indledende pris, men du kan tilsidesætte denne pris, hvis det er nødvendigt. |
| Salgspris | Angiv den forventede salgspris for varerne. |
| Mål | Angiv en decimalværdi for målingen af varerne. Enheden er den, der er konfigureret for det gældende frigivne produkt. |
| Opdater varevægt/-volumen | Markér dette afkrydsningsfelt for at opdatere vægt- eller volumenmål for det frigivne produkt, så det svarer til den værdi af **Mål**, der er angivet for denne række. |
| (Andre dimensioner) | Afhængigt af de dimensioner, du har valgt at få vist, kan du se flere kolonner med oplysninger om de enkelte varer. |

Hvis du vil se eller justere detaljer om volumen og/eller vægt for en vare, skal du vælge varen i gitteret og derefter bruge felterne nederst på siden.

## <a name="manage-estimated-costs"></a>Administrere forkalkulerede omkostninger

Hvis du vil se og redigere de omkostningsestimater, du har oprettet, skal du gå til **Landingsomkostninger \> Forespørgsler \> Omkostningsestimater**. På siden **Omkostningsestimater** viser listeruden til venstre alle aktuelle omkostningsestimater. Du kan bruge knapperne i handlingsruden til at arbejde med et udvalgt estimat. Bemærk, at du ikke kan oprette et nyt omkostningsestimat fra siden **Omkostningsestimater**. Brug i stedet dialogboksen **Omkostningsestimat** (**Landingsomkostninger \> Periodiske opgaver \> Omkostningsestimater**) som beskrevet tidligere i denne artikel.

På siden **Omkostningsestimater** vises, hvordan hver enkelt forkalkulerede omkostning er afledt. Den viser også de forkalkulerede landingsomkostninger for hver enkelt vare. Du kan redigere et omkostningsestimat ved at ændre kostprisen og/eller valutaen, der er tilknyttet de forskellige varer. Du kan også redigere de tilknyttede fragtomkostninger på både fragtniveau og containerniveau. Når du bruger denne side til at ændre omkostningerne, bliver du bedt om at genberegne de forkalkulerede omkostninger for varerne i omkostningsestimatet. Når du er klar, kan du bruge estimaterne til at opdatere kostprisen for varerne i omkostningsskabelonen.

### <a name="information-on-the-header"></a>Information i overskriften

Øverst på siden **Omkostningsestimater** vises de indstillinger, der blev brugt til at generere det valgte omkostningsestimat som beskrevet i forrige afsnit. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Indstillinger og knapper i oversigtspanelet Linjer

Oversigtspanelet **Linjer** indeholder hver vare, der indgår i det aktuelle estimat. I følgende tabel forklares de felter, der er tilgængelige for hver række.

| Felt | Beskrivelse |
|---|---|
| Kreditorkonto | Den kreditorkonto, der er tilknyttet varen. |
| varenummer | Varenummeret. |
| Kvantitet | Det antal varer, der bruges til at bestemme omkostningen. |
| Kostpris | Kostprisen i henhold til samhandelsaftalen. Værdien vises i den lokale valuta. |
| Mål | Det enkelte mål. Enheden er den, der er defineret for det gældende frigivne produkt. |
| Forkalkuleret landingsomkostning | Den forkalkulerede landingsomkostning for det samlede antal. |
| Pr. enhed | Den forkalkulerede landingsomkostning divideret med antallet. |
| (Andre dimensioner) | Afhængigt af de dimensioner, du har valgt at få vist, kan du se flere kolonner med oplysninger om de enkelte varer. |

I følgende tabel forklares de knapper, der er tilgængelige på værktøjslinjen i oversigtspanelet **Linjer**.

| Knap | Beskrivelse |
|---|---|
| Tilføj | Føj varer til omkostningsestimatet. Når du har tilføjet varer, skal du vælge **Genberegn** i handlingsruden. |
| Fjern | Fjern varer fra omkostningsestimatet. Når du har fjernet varer, skal du vælge **Genberegn** i handlingsruden. |
| Ruteomkostninger | Åbn en side, hvor du kan se og redigere forskellige typer fragtomkostninger for varen. |
| Lager \> Vis dimensioner | Åbn en dialogboks, hvor du kan føje dimensionskolonner til gitteret eller fjerne kolonner. |

### <a name="settings-on-the-general-fasttab"></a>Indstillinger i oversigtspanelet Generelt

I oversigtspanelet **Generelt** vises detaljer om den vare, der aktuelt er valgt i oversigtspanelet **Linjer**. Mange af disse oplysninger gentages fra oversigtspanelet **Linjer** og kan redigeres begge steder. Der er dog også flere oplysninger tilgængelige her. Værdierne i de ekstra felter er baseret på opsætningen af det relevante frigivne produkt.

### <a name="settings-on-the-dimension-fasttab"></a>Indstillinger i oversigtspanelet Dimension

I oversigtspanelet **Dimension** vises værdier for alle tilgængelige lagerdimensioner for den vare, der aktuelt er valgt i oversigtspanelet **Linjer**, uanset hvilke dimensioner du har valgt at få vist her. Alle de værdier, der vises her, kommer fra den relevante skabelon til omkostningsestimat. De er valgfrie i skabelonen til omkostningsestimat.

### <a name="buttons-on-the-action-pane"></a>Knapper i handlingsruden

Du kan bruge knapperne i handlingsruden på siden **Omkostningsestimater** til at arbejde med det valgte omkostningsestimat. I følgende tabel forklares de knapper, der er tilgængelige.

| Handling | Beskrivelse |
|---|---|
| Omkostningsforespørgsel | Se alle omkostninger for fragten. Du kan få vist omkostninger på niveauet for den enkelte vare efter behov. |
| Opdater standardomkostning | <p>Opdater standardomkostningen ved hjælp af den standardefterkalkulationsversion, der er defineret på siden **Parametre for landingsomkostninger**. Du kan tilsidesætte denne version.</p><p>**Bemærk:** Hvis en vare har flere varedimensioner (f.eks. forskellige størrelser, farver og varianter), men disse dimensioner ikke er valgt til estimatet, opretter systemet en ventende pris for hver kombination.</p><p>**Vigtigt:** Prisopdelingen oprettes og bruges til at bestemme standardomkostningsafvigelsen pr. landingsomkostning.</p> |
| Fragtomkostninger | Se og rediger fragtomkostninger for alle varer i forsendelsen. |
| Genberegn | Opdater de forkalkulerede landingsomkostninger, når fragtomkostninger er opdateret, tilføjet eller fjernet. |
| Lås | Lås omkostningsestimatposten, så der ikke kan foretages flere ændringer. |

## <a name="item-cost-price-update"></a>Opdatering af varekostpris

Den periodiske opgave **Opdatering af varens kostpris** opdaterer alle forkalkulerede omkostninger, der svarer til de filtre, du angiver, når du kører opgaven. Effekten minder om virkningen af at vælge **Opdater standardomkostninger** i handlingsruden for et enkelt estimat. I dette tilfælde gælder opdateringen dog for alle matchende estimater.

Følg disse trin for at køre den periodiske opgave.

1. Gå til **Landingsomkostninger \> Periodiske opgaver \> Opdatering af varens kostpris**.
1. I dialogboksen **Opdater kostpris fra estimat** skal du angive følgende felter efter behov for at begrænse omfanget af opdateringen:

    - **Version** – Opdater kun estimater, der bruger den angivne efterkalkulationsversion.
    - **Lokation** – Opdater kun estimater, der bruger den angivne lokation.
    - **Omkostningsskabelon** – Opdater kun estimater, der bruger den angivne skabelon.
    - **Til havn** – Opdater kun estimater, der bruger den angivne "til"-havn.
    - **Estimatdato** – Opdater kun estimater, der har den angivne dato.

1. Angiv indstillingerne i oversigtspanelet **Poster, der skal medtages** og **Kør i baggrunden** som normalt ved periodiske opgaver.
1. Vælg **OK** for at køre opgaven.

> [!NOTE]
> Denne periodiske opgave kan kun udføres korrekt, hvis følgende oplysninger er tilgængelige:
>
> - Hvert relevante produkt skal have defineret **Bruttodybde**, **Bruttobredde** og **Bruttohøjde**.
> - Hver relevante leverandør skal have defineret en **Fra-havn**.
