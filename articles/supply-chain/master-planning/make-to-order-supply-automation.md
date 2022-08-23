---
title: Automatisering af forsyning af levering til ordre
description: I denne artikel beskrives, hvordan du kan konfigurere og bruge de forskellige forbedringer, der er tilføjet af funktionen Automatisering af forsyning af levering til ordre.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9044acb472548a797ed387b08ca6892459785793
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220556"
---
# <a name="make-to-order-supply-automation"></a>Automatisering af forsyning af levering til ordre

[!include [banner](../includes/banner.md)]

Funktionen *Automatisering af forsyning af levering til ordre* tilføjer flere forbedringer i Microsoft Dynamics 365 Supply Chain Management. Du kan bruge dem til at udføre følgende opgaver:

- Se ressourcekapacitetsbelastningen for en brugerdefineret periode og aktivere en langsigtet evaluering af kapacitetsbelastningen.
- Opnå større fleksibilitet ved at styre forsinkelsestolerancen (negative dage) for hver behovsplan.
- Holde produkter tilgængelige for sidste minuts-ordrer og optimere brugen af eksisterende forsyning via udligning af den senest mulige forsyning til en efterspørgsel i stedet for at bruge den første mulige forsyning.
- Holde komponenttildelingen fleksibel for produktionsordrer efter autorisation, så systemet kan optimere for sidste minuts efterspørgselsændringer. Med andre ord begrænse markering til ét niveau.
- Kontroller opfyldelsespolitikken for hver enkelt salgsordre. Standardindstillingerne tages fra kundeopsætningen.
- Få bedre flow af interne oplysninger. Indkøbsordrer opdateres, så de indeholder felter for leveringsmåde, leveringsbetingelser og eksternt varenummer. Denne ændring sikrer, at der kan opnås detaljerede efterspørgselsoplysninger til leverandørfirmaet.

Denne artikel beskriver, hvordan du konfigurerer og bruger hver enkelt forbedring.

> [!NOTE]
> Alle de forbedringer, der er beskrevet i denne artikel, gælder for systemer, der bruger indbygget varedisponering. Følgende to forbedringer understøttes også af tilføjelsesprogrammet Planlægningsoptimering til Microsoft Dynamics 365 Supply Chain Management:
>
> - Forsinkelsestolerance på behovsplaner
> - Styre den udligningsrækkefølge, der bruges under varedisponering

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Aktivere funktionen Automatisering af forsyning af levering til ordre

Før du kan bruge den funktion, der er beskrevet i denne artikel, skal du aktivere den i systemet. Administratorer kan bruge arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), der viser funktionen på følgende måde:

- **Modul:** *Varedisponering*
- **Funktionsnavn:** *Automatisering af forsyning af levering til ordre*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Angiv det antal dage, der skal vises på siden Kapacitetsbelastning

På siden **Kapacitetsbelastning** kan du gennemse en ressources tilgængelige kapacitet. Funktionen *Automatisering af forsyning af levering til ordre* forbedrer siden **Kapacitetsbelastning** ved at tilføje et felt for **Antal dage**. Du kan bruge dette felt til at begrænse det antal dage, som gitteret **Oversigt** viser. Den værdi, du angiver, gemmes i hukommelsen. Hvis du forlader siden og efterfølgende vender tilbage senere, viser gitteret **Oversigt** derfor stadig det antal dage, du senest har angivet.

Hvis du vil åbne siden **Kapacitetsbelastning**, så du kan gennemse den tilgængelige kapacitet for en enkelt ressource, skal du følge disse trin.

1. Gå til **Organisationsadministration \> Ressourcer \> Ressourcer**.
1. Vælg en ressource, der skal inspiceres
1. Vælg **Kapacitetsbelastning** i gruppen **Vis** under fanen **Ressource** i handlingsruden.
1. Brug filteret **Antal dage** til at begrænse det antal dage, som gitteret **Oversigt** viser.

Hvis du vil åbne siden **Kapacitetsbelastning**, så du kan gennemse den tilgængelige kapacitet for en ressourcegruppe, skal du følge disse trin.

1. Gå til **Virksomhedsadministration \> Ressourcer \> Ressourcegrupper**.
1. Vælg en ressourcegruppe, der skal inspiceres
1. Vælg **Kapacitetsbelastning** i gruppen **Vis** under fanen **Ressourcegruppe** i handlingsruden.
1. Brug filteret **Antal dage** til at begrænse det antal dage, som gitteret **Oversigt** viser.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Anvende et enkelt markeringsniveau, når du autoriserer ordreforslag

*Afmærkning* bruges til at sammenkæde udbud og efterspørgsel. Det ligner *udligning*, som angiver, hvordan varedisponering forventer at dække behov. Markering er dog mere permanent end udligning. Funktionen *Automatisering af forsyning af levering til ordre* giver mulighed for at begrænse lagermarkering til et enkelt niveau, når ordreforslag autoriseres. Den tilføjer følgende nye indstillinger i feltet **Opdater markering** i dialogboksen **Autorisation**, når du autoriserer et ordreforslag:

- *Enkelt niveau, standard* – Der bruges markering på enkelt niveau. Markering på enkelt niveau markerer kun hovedvaren og ikke styklistekomponenterne. Du kan derfor sikre, at komponenttildelingen for produktionsordrer er fleksibel efter autorisation. Markering på enkelt niveau giver systemet mulighed for at optimere for sidste minuts efterspørgselsændringer. Ved *standard*-markering på et enkelt niveau markeres behovsordrer i forhold til deres opfyldningsordrer, men opfyldningsordrer markeres ikke, hvis de har et restantal.
- *Enkelt niveau, udvidet* – Der bruges markering på enkelt niveau. Ved *udvidet*-markering på et enkelt niveau markeres behovsordrer i forhold til deres opfyldningsordrer, og opfyldningsordrer markeres altid, uanset om de har et restantal.

Disse indstillinger er også tilgængelige i feltet **Opdater markering** under fanen **Standardopdatering** på siden **Varedisponeringsparametre**, hvor du definerer standardvalget i dialogboksen **Autorisation**.

Du kan finde flere oplysninger under [Lagermarkering med Planlægningsoptimering](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Angive forsinkelsestolerance (negative dage) på behovsplanniveau

Funktionen *Automatisering af forsyning af levering til ordre* tilføjer muligheden for at konfigurere forsinkelsestolerance (negative dage) på behovsplanniveau. Indstillingen er også tilgængelig på varedisponerings- og disponeringsgruppeniveauer. Hvis negative dage tildeles på mere end ét niveau, anvender systemet følgende hierarki til at bestemme, hvilken indstilling der skal bruges:

- Hvis negative dage er konfigureret på siden **Behovsplaner**, tilsidesætter denne indstilling alle andre indstillinger for negative dage, når planen kører.
- Hvis negative dage konfigureres på siden **Varedisponering**, tilsidesætter denne indstilling disponeringsgruppen.
- Negative dage, der er konfigureret på siden **Disponeringsgrupper**, gælder kun, hvis der ikke er konfigureret negative dage for en relevant vare eller behovsplan.

Hvis du vil angive negative dage for en behovsplan, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en behovsplan på listesiden, eller opret en ny.
1. Angiv indstillingen **Negative dage** til **Ja** i oversigtspanelet *Tidshorisonter i dage*.
1. Angiv det antal negative dage, der skal være tilladt, i det nærliggende felt.

Du kan finde flere oplysninger om brug af negative dage i [Forsinkelsestolerance (negative dage)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Styre den udligningsrækkefølge, der bruges under varedisponering

Ved behovsplanlægning anvendes en *udligningsrækkefølge* for at bestemme, hvilken forsyning der skal dække hvilket behov. Funktionen *Automatisering af forsyning af levering til ordre* tilføjer en ny indstilling **Brug seneste mulige forsyning**, som giver dig mere kontrol over udligningssekvensen. Med den nye indstilling kan du holde produkter tilgængelige for sidste minuts-ordrer og optimere brugen af eksisterende forsyning via udligning af den senest mulige forsyning til en efterspørgsel i stedet for at bruge den første mulige forsyning.

Du kan angive udligningsrækkefølgen på behovsplan, varedisponerings- eller disponeringsgruppeniveau. Hvis en udligningssekvens er konfigureret på mere end ét niveau, anvender systemet følgende hierarki til at bestemme, hvilken indstilling der skal bruges:

- Hvis der er konfigureret en udligningssekvens på siden **Behovsplaner**, tilsidesætter denne indstilling alle andre indstillinger for udligningssekvens, når planen køres.
- Hvis en udligningssekvens konfigureres på siden **Varedisponering**, tilsidesætter denne indstilling disponeringsgruppen.
- Den udligningsrækkefølge, der er oprettet på siden **Disponeringsgrupper**, gælder kun, hvis der ikke er konfigureret indstillinger for udligningssekvens for en relevant vare eller behovsplan.

Hvis du vil konfigurere udligning på disponeringsgruppeniveau, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Dækning \> Dækningsgrupper**.
1. Vælg en gruppe på listesiden, eller opret en ny.
1. I sektionen **Udligningssekvens** i oversigtspanelet **Generelt** skal du bruge felterne **Forbrug disponibel lagerbeholdning** og **Brug seneste mulige forsyning** til at konfigurere udligningssekvensen. Tabellen senere i dette afsnit viser, hvordan disse indstillinger kombineres for at definere udligningssekvensen.

Hvis du vil konfigurere udligning på varedisponeringsniveau, skal du følge disse trin.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg et produkt i gitteret, eller opret et nyt.
1. Vælg **Plan** i handlingsruden, og vælg derefter **Varedisponering**.
1. Siden **Varedisponering** indeholder rækker, hvor du kan definere disponeringsregler, der gælder for varen på hvert lagersted. Vælg en eksisterende række i gitteret, eller opret en ny.
1. Markér afkrydsningsfeltet **Tilsidesæt udligningssekvens** under fanen **Generelt**.
1. Brug felterne **Forbrug disponibel lagerbeholdning** og **Brug seneste mulige forsyning** til at konfigurere udligningssekvensen. Tabellen senere i dette afsnit viser, hvordan disse indstillinger kombineres for at definere udligningssekvensen.

Hvis du vil konfigurere udligning på behovsplanniveau, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en behovsplan på listesiden, eller opret en ny.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Tilsidesæt udligningssekvens** til *Ja*.
1. Brug felterne **Forbrug disponibel lagerbeholdning** og **Brug seneste mulige forsyning** til at konfigurere udligningssekvensen. Tabellen senere i dette afsnit viser, hvordan disse indstillinger kombineres for at definere udligningssekvensen.

I følgende tabel vises, hvordan indstillingerne **Forbrug disponibel lagerbeholdning** og **Brug seneste mulige forsyning** kombineres for at oprette udligningssekvensen.

| | Brug seneste mulige forsyning = Ja | Brug seneste mulige forsyning = Nej |
|---|---|---|
| **Forbrug disponibel lagerbeholdning** = *Før al anden levering* | <ol><li>Disponibel</li><li>Eksisterende forsyning, der kan opfylde behovsdatoen</li><li>Eksisterende forsyning, der ikke kan opfylde behovsdatoen, men stadig inden for negative dage</li><li>Oprette ny forsyning (ordreforslag)</li></ol> | <ol><li>Disponibel</li><li>Eksisterende forsyning, der kan opfylde behovsdatoen</li><li>Eksisterende forsyning, der ikke kan opfylde behovsdatoen, men stadig inden for negative dage</li><li>Oprette ny forsyning (ordreforslag)</li></ol> |
| **Forbrug disponibel lagerbeholdning** = *Efter al anden levering* | <ol><li>Eksisterende forsyning, der kan opfylde behovsdatoen</li><li>Disponibel</li><li>Eksisterende forsyning, der ikke kan opfylde behovsdatoen, men stadig inden for negative dage</li><li>Oprette ny forsyning (ordreforslag)</li></ol> | <ol><li>Eksisterende forsyning, der kan opfylde behovsdatoen</li><li>Eksisterende forsyning, der ikke kan opfylde behovsdatoen, men stadig inden for negative dage</li><li>Disponibel</li><li>Oprette ny forsyning (ordreforslag)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Gennemse og angive den opfyldelsespolitik, der gælder for hver salgsordre

Opfyldelsespolitikker kontrollerer procentdelen af den samlede ordrepris eller mængde, der skal være reserveret fysisk, før en salgsordre kan frigives til lagerstedet. Du kan angive en global standardopfyldelsespolitik og derefter tilsidesætte den for specifikke kunder efter behov. Funktionen *Automatisering af forsyning af levering til ordre* giver mulighed for at se, hvilken standardpolitik der faktisk anvendes til en hvilken som helst ordre, og anvende en ordrespecifik tilsidesættelse efter behov.

- Hvis du vil angive standarden for den globale opfyldelsespolitik for salgsordrer, skal du gå **Debitor \> Konfiguration \> Debitorparametre**. Angiv derefter feltet **Opfyldelsespolitik for salgsordre** til navnet på den politik, du vil bruge, under fanen **Lagerstedsstyring**. 
- Hvis du vil angive en kundespecifik opfyldelsespolitik for salgsordrer, skal du gå til **Debitor \> Kunder \> Alle kunder**. Angiv derefter feltet **Opfyldelsespolitik** til navnet på den politik, du vil bruge, under fanen **Lagersted**.

Hvis du vil se den standardpolitik, der gælder for alle ordrer, og anvende en ordrespecifik tilsidesættelse, skal du følge disse trin.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Åbn den salgsordre, som du vil inspicere eller redigere.
1. Vælg visningen **Overskrift**.
1. Gennemse og rediger følgende felter i oversigtspanelet **Lagersted** efter behov:

    - **Opfyldelsespolitik for ordre** – Vælg den opfyldelsespolitik, der skal bruges til den valgte ordre. Standardpolitikken tilsidesættes. Hvis du vil bruge den standardopfyldelsespolitik, der vises i feltet **Standardpolitik for opfyldelse**, skal du lade dette felt være tomt.
    - **Standardpolitik for opfyldelse** – Dette felt viser den standardopfyldelsespolitik, der gælder, hvis feltet **Opfyldelsespolitik for ordre** er tomt. Feltet er skrivebeskyttet. Hvis feltet ikke er udfyldt, defineres der ingen kundespecifik eller global standardopfyldelsespolitik.

    Hvis både feltet **Standardpolitik for opfyldelse** og feltet **Opfyldelsespolitik for ordre** er tomt, anvendes ingen opfyldelsespolitik. Der kan dog være andre begrænsninger, der kan kræve, at reservationer eller andre betingelser skal være opfyldt, før salgsordren kan frigives.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Angive leveringsmåde og -betingelser på de enkelte indkøbsordrelinjer

Alle indkøbsordrer inkluderer **Leveringsbetingelser** og indstillinger for **Leveringsmåde** i ordreoverskriften. Funktionen *Automatisering af forsyning af levering til ordre* føjer disse indstillinger til hver ordrelinje. Du kan derfor definere tilsidesættelser af **Leveringsbetingelse** og/eller **Leveringsmåde** for en hvilken som helst ordrelinje efter behov. I forbindelse med linjer, hvor der ikke er defineret nogen tilsidesættelse, bruges værdien fra overskriften. Du kan angive, om en ændring af værdien i et eller begge disse felter i ordreoverskriften også skal opdatere alle linjer.

Hvis du vil angive, hvad der skal ske med linjeindstillinger, hvis en bruger ændrer værdien af **Leveringsbetingelse** og/eller **Leveringsmåde** i ordreoverskriften, skal du følge disse trin.

1. Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsparametre**.
1. Vælg linket **Opdater ordrelinjer** i oversigtspanelet **Standardværdier og parametre** under fanen **Generelt**.
1. Vælg en af følgende værdier i dialogboksen **Opdater ordrelinjer** i felterne **Opdater leveringsbetingelser** og **Opdater leveringsmåde**:

    - *Aldrig* – Opdater aldrig ordrelinjerne, når indstillingerne er ændret i ordreoverskriften.
    - *Altid* – Opdater altid alle ordrelinjer, når indstillingerne er ændret i ordreoverskriften.
    - *Spørg* – Hvis en bruger ændrer en eller begge indstillinger i ordreoverskriften, skal du åbne en dialogboks, hvor brugeren bliver spurgt, om brugeren vil opdatere alle linjer, så de stemmer overens med ændringen i en eller begge indstillinger.

Hvis du vil angive leveringsoplysninger i et indkøbsordrehoved, skal du følge disse trin.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Åbn den indkøbsordre, som du vil inspicere eller redigere.
1. Vælg visningen **Overskrift**.
1. Angiv felterne **Leveringsmåde** og **Leveringsbetingelser** i oversigtspanelet **Levering** efter behov.
1. Afhængigt af indstillingerne på siden **Indkøbs - og forsyningsparametre** kan du blive spurgt, om du vil anvende ændringerne på alle ordrelinjer.

Hvis du vil angive tilsidesættelser af leveringsoplysninger for en indkøbsordrelinje, skal du følge disse trin.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Åbn den indkøbsordre, som du vil inspicere eller redigere.
1. Vælg visningen **Linjer**.
1. På oversigtspanelet **Indkøbsordrelinjer** skal du vælge den linje, du vil redigere.
1. Angiv felterne **Leveringsmåde** og **Leveringsbetingelser** under fanen **Levering** i oversigtspanelet **Linjedetaljer**. Fjern markeringen i et eller begge felter for at bruge de tilsvarende indstillinger i overskriften.

For interne ordrer synkroniseres værdierne for felterne **Leveringsmåde** og **Leveringsbetingelser** på hver indkøbsordrelinje mellem indkøbsordren og den relaterede salgsordre.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Synkronisere eksterne vare-id'er og beskrivelser for interne ordrer

I forbindelse med interne ordrer giver funktionen *Automatisering af forsyning af levering til ordre* mulighed for at synkronisere eksterne vare-id'er og tekstbeskrivelser på indkøbsordrelinjer med de relaterede interne salgsordrelinjer, uanset om indkøbsordren er til direkte levering. Denne funktion giver dig også mulighed for at angive den endelige eksterne kundekonto på en intern indkøbsordre. Systemet tager derefter automatisk eksterne vare-id'er og tekstbeskrivelser fra den eksterne kundepost i stedet for den interne leverandørpost.

Hvis du vil konfigurere en intern leverandør til at synkronisere eksterne vare-id'er og varenavne mellem interne indkøbsordrer og deres relaterede interne salgsordrer, skal du følge disse trin.

1. Gå til **Indkøb og forsyning \> Kreditorer \> Alle kreditorer**.
1. Vælg den interne leverandør, der skal konfigureres.
1. I handlingsruden under fanen **Generelt** i gruppen **Konfigurer** skal du vælge **Internt**.
1. På siden **Intern handel** under fanen **Politikker for oprettelse af indkøbsordre** i sektionen **Intern indkøbsordre -\> Intern salgsordre** skal du markere afkrydsningsfeltet **Eksternt vare-id og varenavn**.

Følg disse trin for at angive den endelige eksterne kundekonto til en intern indkøbsordre. Feltet **Debitorkonto** gælder kun for interne indkøbsordrer. Brug det til at angive kontonummeret på den kunde, der skal modtage varerne i sidste ende. Når dette felt er angivet, tager indkøbsordrelinjer eksterne varebeskrivelser og -numre fra den angivne debitorkonto i stedet for den interne leverandør, der er angivet på indkøbsordren. Hvis du ændrer debitorkontoen senere, opdateres eksterne varebeskrivelser og id'er, så de svarer til værdierne i den nye konto. Eksterne varebeskrivelser og -id'er for hver linje synkroniseres også med den tilsvarende interne salgsordre.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Åbn den indkøbsordre, du vil konfigurere, eller opret en ny.
1. Vælg visningen **Overskrift**.
1. I **Reference**-sektionen skal du angive **Debitorkonto**-feltet til den relevante eksterne debitorkonto.

Hvis du vil angive eksterne vare-id'er og tekstbeskrivelser til en indkøbsordrelinje til en intern ordre, skal du følge disse trin. De værdier, du angiver, synkroniseres med de relaterede interne salgsordrelinjer, uanset om indkøbsordren er til direkte levering.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Åbn den indkøbsordre, du vil konfigurere, eller opret en ny.
1. Vælg visningen **Linjer**.
1. På oversigtspanelet **Indkøbsordrelinjer** skal du vælge den linje, du vil redigere.
1. Angiv en ekstern beskrivelse af den vare, der er angivet på den valgte ordrelinje, i feltet **Tekst** i sektionen **Ordrelinje** i oversigtspanelet **Linjedetaljer** under fanen **Generelt**. Denne værdi synkroniseres med den relaterede interne salgsordrelinje.
1. I afsnittet **Reference** skal du i feltet **Ekstern** angive et eksternt vare-id for den vare, der er angivet på den valgte ordrelinje. Denne værdi synkroniseres med den relaterede interne salgsordrelinje.

Du kan få flere oplysninger i [Oprette og fakturere en intern salgsordre til en ekstern kunde](../sales-marketing/intercompany-sales-order-for-external-customer.md).
