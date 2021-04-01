---
title: Livscyklustilstande for arbejdsordre
description: Dette emne beskriver livscyklustilstande for arbejdsordrer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e72c56765ad51a4f43fb01d842f5940a4d1a025e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248833"
---
# <a name="work-order-lifecycle-states"></a>Livscyklustilstande for arbejdsordre


[!include [banner](../../includes/banner.md)]

 

Arbejdsordrens livscyklus angiver de tilstande, som en arbejdsordre kan gennemgå. Som eksempel kan nævnes **Oprettet**, **Planlagt**, **I gang** og **Afsluttet**. Livscyklustilstande for arbejdsordrer kan opdateres manuelt på en arbejdsordre, eller de kan opdateres automatisk (f.eks. under planlægning af arbejdsordrer).

De livscyklustilstande for arbejdsordrer, der skal være angivet for dine arbejdsordrer, skal være knyttet til tilsvarende projektstadier på siden **Parametre for projektstyring og regnskab** (**Projektstyring og regnskab** \> **Parametre for projektstyring og regnskab**). Du skal først konfigurere projektstadier i Projektstyring og regnskab. Derefter konfigurerer du arbejdsordrens livscyklustilstande og livscyklusmodeller i Styring af aktiver.

I følgende tabel beskrives indstillingerne i sektionerne **Arbejdsordre** og **Tidsplan** i oversigtspanelet **Generelt** på siden **Livscyklustilstande for arbejdsordre** (**Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Livscyklustilstande**).

![Siden Livscyklustilstand for arbejdsordre](media/09-setup-for-work-orders.png)

| Navn på indstilling                   | Beskrivelse |
|-------------------------------|-------------|
| Aktive                        | Vælg **Ja** i denne indstilling, hvis arbejdsordren skal være aktiv, mens den er i denne livscyklustilstand. |
| Tilføj linje                      | Vælg **Ja** i denne indstilling, hvis der kan føjes arbejdsordrejob til en arbejdsordre, der er i denne livscyklustilstand. |
| Slet                        | Vælg **Ja** i denne indstilling, hvis en arbejdsordre kan slettes, mens den er i denne livscyklustilstand. |
| Slet linje                   | Vælg **Ja** i denne indstilling, hvis arbejdsordrejob kan slettes i en arbejdsordre, der er i denne livscyklustilstand. |
| Tillad planlægning              | Vælg **Ja** i denne indstilling, hvis en arbejdsordre kan planlægges, mens den er i denne livscyklustilstand. |
| Angiv faktisk start              | Vælg **Ja** i denne indstilling, hvis brugeren skal bedes om at vælge en faktisk startdato og -klokkeslæt for en arbejdsordre, når den opdateres til denne livscyklustilstand. |
| Angiv faktisk slutning                | Vælg **Ja** i denne indstilling, hvis brugeren skal bedes om at vælge en faktisk slutdato og -klokkeslæt for en arbejdsordre, når den opdateres til denne livscyklustilstand. |
| Bogfør kladder                 | Vælg **Ja** i denne indstilling, hvis arbejdsordrekladder automatisk skal bogføres, når en arbejdsordre opdateres til denne livscyklustilstand. Hvis der opstår en fejl under kladdebogføringen, vises en meddelelse, og opdateringen af arbejdsordrens livscyklustilstand annulleres. Hvis du vil have vist kladdelinjerne for en arbejdsordre, skal du vælge **Styring af aktiver** \> **Almindeligt** \> **Arbejdsordrer** \> **Alle arbejdsordrer**, **Aktive arbejdsordrer** eller **Mine aktive arbejdsordrer**, vælge arbejdsordren på listen og derefter vælge **Kladder**. Denne opsætning af automatisk bogføring af arbejdsordrekladder i en bestemt livscyklustilstand er den samme, som når du vælger **Bogfør kladder** på siden **Arbejdsordrekladder**.<p>**Bemærk!** Hvis du vælger **ja** i denne indstilling, bogføres kladderne automatisk, hvis der ikke er oprettet en godkendelsesarbejdsgang. Hvis dit firma bruger den kladdegodkendelsesopsætning, der er konfigureret på siden **Kladdegodkendelse** (**Projektstyring og regnskab** \> **Opsætning** \> **Kladder** \> **Kladdegodkendelse**), skal en chef eller medarbejder validere og bogføre forbrugsregistreringer.</p> |
| Behandl vedligeholdelsestjekliste | Vælg **Ja** i denne indstilling, hvis alle tilknyttede vedligeholdelsestjeklister skal behandles, når en arbejdsordre opdateres til denne livscyklustilstand. Som en del af denne behandling bogføres alle de tællerregistreringer, der er foretaget på en vedligeholdelsestjekliste, og resultatet af hele vedligeholdelsestjeklisten evalueres. Vedligeholdelsestjeklistelinjer, der har resultaterne **Bestået** og **Mislykket**, evalueres, og hvis mindst en linje mislykkes, markeres hele vedligeholdelsestjeklisten som **Mislykket** i Styring af aktiver. |
| Udført                         | Vælg **ja** i denne indstilling, hvis tidsplanstatus for arbejdsordrejobbet for alle de arbejdsordrejob, der oprettes i en arbejdsordre, automatisk skal opdateres til **Klar**, når arbejdsordren opdateres til denne livscyklustilstand. |
| Igangsætning                         | Vælg **ja** i denne indstilling, hvis tidsplanstatus for arbejdsordrejobbet for alle de arbejdsordrejob, der oprettes i en arbejdsordre, automatisk skal opdateres til **Påbegyndt**, når arbejdsordren opdateres til denne livscyklustilstand. |
| Afslutning                           | Vælg **ja** i denne indstilling, hvis tidsplanstatus for arbejdsordrejobbet for alle de arbejdsordrejob, der oprettes i en arbejdsordre, automatisk skal opdateres til **Afsluttet**, når arbejdsordren opdateres til denne livscyklustilstand. |
| Slet tidsplanslinjer         | Vælg **Ja** i denne indstilling, hvis tidsplanen for alle arbejdsordrejob, der er oprettet i en arbejdsordre, som allerede er planlagt, skal slettes, når arbejdsordren opdateres til denne livscyklustilstand. Det vil sige, at kapacitetsreservationer på aktivet, den relaterede vedligeholdelsesarbejder og relaterede værktøjer slettes. Du kan f.eks. vælge **Ja** i denne indstilling i en arbejdsordres livscyklustilstand med navnet **Forkalkuleret**. Når en arbejdsordre derefter føres tilbage til denne livscyklustilstand, fordi omplanlægning er påkrævet, kan planlægningen slettes på den pågældende arbejdsordre. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Konfigurere projektstadier og livscyklustilstande for arbejdsordrer

1. Vælg **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.
2. Under fanen **Projektstadie** skal du for hvert af de stadier, du vil bruge, markere afkrydsningsfeltet for hver projekttype, der skal bruges til dine arbejdsordrer. Projekttyperne definerer de regler, der er tilladt for de økonomiske opgaver. Eksempler på økonomiske opgaver omfatter oprettelse af et budget, oprettelse af estimater og oprettelse af primosaldi.

    > [!IMPORTANT]
    > Hvis der ikke er valgt et projektstadie for en projekttype, men projektstadiet bruges til en livscyklustilstand for en arbejdsordre, opdateres arbejdsordreprojekterne ikke, som de skal.

3. Luk siden **Parametre for projektstyring og regnskab**.
4. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Livscyklustilstande**.
5. Vælg **Ny** for at oprette en livscyklustilstand for en arbejdsordre.
6. Angiv et ID for livscyklustilstand i feltet **Livscyklustilstand**.
7. Indtast et navn i feltet **Navn**.

    I oversigtspanelet **Detaljer** viser feltet **Livscyklusmodeller** antallet af livscyklusmodeller for arbejdsordrer, der bruger denne livscyklustilstand.

8. I oversigtspanelet **Generelt** i sektionen **Arbejdsordre** skal du vælge de funktioner, der skal være tilgængelige for denne livscyklustilstand, ved at vælge **Ja** i de relevante indstillinger. Se beskrivelser af disse indstillinger i tabellen senere i dette emne.
9. Vælg det projektstadie, der skal knyttes til denne livscyklustilstand, i feltet **Stadie** i sektionen **Projekt**.
10. I sektionen **Projekt** skal du vælge **Ja** i indstillingen **Luk aktiviteter**, hvis projektaktiviteter, der er relateret til hvert arbejdsordrejob, skal lukkes automatisk, når arbejdsordren er i denne levetidstilstand.

    > [!NOTE]
    > Hvis du vil finde nummeret på den projektaktivitet, der er relateret til et arbejdsordrejob, skal du vælge **Styring af aktiver** \> **Almindelig** \> **Arbejdsordrer** \> **Alle arbejdsordrer**, **Aktive arbejdsordrer** eller **Mine aktive arbejdsordrer**. Åbn arbejdsordren, og vælg derefter arbejdsordrejobbet. Aktivitetsnummeret vises i feltet **Aktivitetsnummer** i sektionen **Projekt** under fanen **Generelt** i oversigtspanelet **Linjedetaljer**.

11. I sektionen **Budget** skal du vælge **ja** i indstillingen **Kopiér timebudget**, **Kopier varebudget** og/eller **Kopier udgiftsbudget**, hvis projektprognoser for arbejdsordrer automatisk skal kopieres til arbejdsordrekladder, når arbejdsordren er i denne livscyklustilstand.
12. I sektionen **Tidsplan** skal du vælge **Ja** i en af indstillingerne, hvis planlægningsstatus for arbejdsordrejob skal opdateres, når arbejdsordren er i denne livscyklustilstand. Beskrivelser af indstillingerne **Klar**, **Start**, **Slut** og **Slet tidsplanlinjer** finder du i tabellen tidligere i dette emne.

    > [!NOTE]
    > Hvis du vil se tidsplanlinjer, der er relateret til arbejdsordrejob, skal du vælge **Styring af aktiver** \> **Almindelig** \> **Arbejdsordrer** \> **Alle arbejdsordrer**, **Aktive arbejdsordrer** eller **Mine aktive arbejdsordrer**. Åbn arbejdsordren, vælg jobbet for arbejdsordren i oversigtspanelet **Arbejdsordrejob**, og se relaterede oplysninger i oversigtspanelet **Linjedetaljer**. Feltet **Status** under fanen **Tidsplan** viser status for arbejdsordrejobbet. Feltet **Status** kan indstilles til følgende værdier: **Planlagt**, **Klar**, **Startet**, **Stoppet** og **Afsluttet**.

13. Vælg den levetidstilstand for vedligeholdelsesanmodningen, som relaterede vedligeholdelsesanmodninger skal opdateres til, i feltet **Livscyklustilstand** i sektionen **Vedligeholdelsesanmodninger**. Denne opdatering sker automatisk. Den kan kun udføres, hvis livscyklustilstanden for vedligeholdelsesanmodningen er valgt i den livscyklusmodel for vedligeholdelsesanmodninger, der bruges til vedligeholdelsesanmodningen.
14. I sektionen **Aktiver** skal du vælge **Ja** i indstillingen **Opdater aktivstykliste**, hvis alle varer, der bruges i en arbejdsordre, automatisk skal opdateres på siden **Aktivstykliste**, når arbejdsordren opdateres til denne livscyklustilstand. Denne indstilling kan være relevant, hvis f.eks. livscyklustilstanden for arbejdsordren definerer arbejdsordren som fuldført eller afsluttet.
15. I sektionen **Arbejdsordrepulje** kan du vælge **Ja** i indstillingen **Slet puljereference**, hvis de arbejdsordrer, der er i denne livscyklustilstand, automatisk skal slettes fra arbejdsordrepuljer.
16. I oversigtspanelet **Valider** skal du vælge de valideringstyper, der skal aktiveres i denne livscyklustilstand, ved at vælge **Ja** i de relevante indstillinger. Derefter skal du i feltet **Type** for hver af de valideringstyper, du vælger, vælge den type meddelelse, der skal vises, hvis obligatoriske felter, der er relateret til valideringstypen, ikke er blevet valideret. Hvis du vælger **Fejl**, annulleres opdateringen af arbejdsordrens livscyklustilstand, indtil de relaterede obligatoriske felter er opdateret på arbejdsordren.

    - Indstillingerne **Vedligeholdelsesnedetid**, **Vedligeholdelsestjekliste**, **Fejlsymptom**, **Fejlårsag** og **Fejlafhjælpning** er knyttet til indstillingerne i sektionen **Obligatorisk** på siden **Arbejdsordretyper** (**Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Arbejdsordretyper**). Hvis du vil aktivere disse valideringer, skal de relaterede indstillinger også indstilles til **Ja** i den arbejdsordretype, der bruges til arbejdsordren.
    - Hvis der er valgt **Ja** i indstillingen **Vedligeholdelsestjekliste** for den livscyklustilstand, som en arbejdsordre opdateres til, udføres valideringen for at kontrollere, at vedligeholdelsestjeklistelinjer, der er markeret som **Obligatorisk**, er registreret som enten **Kontrolleret** eller **Ikke-tilgængelig**. Hvis ingen af disse registreringer er foretaget på de obligatoriske linjer, vises der en oplysnings-, en fejl- eller en advarselsmeddelelse, når arbejdsordren opdateres til denne livscyklustilstand.
    - Hvis der er valgt **ja** i indstillingen **Bindende omkostning** for den livscyklustilstand, som en arbejdsordre opdateres til, beregnes det samlede beløb for bindende omkostninger (dvs. det samlede beløb for de udgifter, som den juridiske enhed har forpligtet sig til at betale), for hvert job i en arbejdsordre. Der vises en meddelelse, hvis det bindende omkostningsbeløb er større end 0 (nul). Du vælger de typer omkostningsforpligtelse, der er medtaget i oversigtspanelet **Udgiftsforpligtelse** under fanen **Omkostningsstyring** på siden **Parametre for projektstyring og regnskab** (**Parametre for projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**).
    - Hvis der er valgt **Ja** i indstillingen **Vedligeholdelsesnedetid** for den livscyklustilstand, som en arbejdsordre opdateres til, udføres der validering af vedligeholdelsesnedetid på det aktiv, der er knyttet til arbejdsordren. Hvis der er foretaget en registrering af vedligeholdelsesnedetid, men der ikke er en **Afsluttet** registrering, vises der en meddelelse, når arbejdsordren opdateres til denne livscyklustilstand.
    - Hvis standardprojektopsætningen ikke omfatter alle de stadier, du har brug for i opsætningen af Styring af aktiver, kan du oprette brugerdefinerede projektstadier under fanen **Projektstadie** på siden **Parametre for projektstyring og regnskab**. I følgende illustration vises fanen **Projektstadie** på siden **Parametre for projektstyring og regnskab**.

    ![Siden Konfigurer projektstadier for forskellige projekttyper](media/10-setup-for-work-orders.png)

> [!NOTE]
> Hvis den livscyklustilstand, du opdaterer en arbejdsordre til, er inaktiv, slettes kladder, der er relateret til arbejdsordren, men som endnu ikke er bogført, automatisk. Denne funktionsmåde hjælper med at sikre automatisk oprydning i ubrugte data. (En livscyklustilstand er inaktiv, hvis indstillingen **Aktiv** for den er **Nej** i oversigtspanelet **Generelt** på siden **Livscyklustilstande for arbejdsordre**).
>
> Hvis du manuelt konfigurerer arbejdsordren, så den ikke er inaktiv, slettes kladder, der er relateret til arbejdsordren, men som endnu ikke er bogført, dog **ikke** automatisk. (Hvis du vil inaktivere en arbejdsordre manuelt, skal du vælge **Styring af aktiver** \> **Almindeligt** \> **Arbejdsordrer** \> **Alle arbejdsordrer** eller **Aktive arbejdsordrer**. Åbn arbejdsordren, og skift til visningen **Hoved**. I oversigtspanelet **Generelt** skal du vælge **Rediger** og derefter vælge **Nej** i indstillingen **Aktiv**).

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Relationer mellem livscyklusmodeller for arbejdsordrer, arbejdsordretyper og livscyklustilstande for arbejdsordrer

Livscyklusmodeller refererer til arbejdsgange, og livscyklustilstande vælges i en livscyklusmodel i rækkefølge. Livscyklusmodeller konfigureres i arbejdsordretyper. Arbejdsordretyper bestemmer størrelsen eller omfanget af arbejdsgange og arbejdsprocesser. **Vedligeholdelse**, som er en standardtype for arbejdsordrer, kan f.eks. være relateret til en livscyklusmodel for en arbejdsordre, hvor der er flere livscyklustilstande. På den anden side kan du have en **Korrigerende** arbejdsordretype, der bruges til arbejdsordrer, der ikke er planlagt, eller til arbejdsordrer, hvor jobbet er fuldført, før arbejdsordren er udført, på grund af en hastesituation. Denne arbejdsordretype kan være knyttet til en livscyklusmodel for en arbejdsordre, der kun har nogle få livscyklustilstande.

Årsagen til brugen af typer er, at når en type er defineret på f.eks. en arbejdsordre eller et aktiv, defineres de relaterede arbejdsprocesser (livscyklusser) automatisk. Du kan finde flere oplysninger om, hvordan du konfigurerer arbejdsordretyper, i [Arbejdsordretyper](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> Livscyklustilstande, livscyklusmodeller og typer anvendes på arbejdssteder, aktiver og vedligeholdelsesanmodninger, ud over arbejdsordrer.

I følgende illustration vises relationen mellem arbejdsordretyper, livscyklusmodeller og livscyklustilstande.

![Siden Arbejdsordretype sammenlignet med siden Livscyklusmodeller for arbejdsordre](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Livscyklusmodeller for arbejdsordre

Når du har oprettet de livscyklustilstande for arbejdsordrer, der kræves til dine arbejdsordrer, kan de opdeles i livscyklusmodeller for arbejdsordrer. Du skal som minimum oprette én standardlivscyklusmodel.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Livscyklusmodeller**.
2. Vælg **Ny** for at oprette en livscyklusmodel for en arbejdsordre.
3. Angiv et ID for livscyklusmodellen i feltet **Livscyklusmodel**.
4. Indtast et navn i feltet **Navn**.

    I oversigtspanelet **Detaljer** viser feltet **Livscyklustilstande** antallet af livscyklustilstande, der er valgt i denne livscyklusmodel. Feltet **Arbejdsordretyper** viser antallet af antallet af arbejdsordretyper, der bruger denne livscyklusmodel.

5. I oversigts panelet **Livscyklustilstande** skal du vælge de livscyklustilstande, der bør inkluderes i livscyklusmodellen:

    - Hvis du vil inkludere en livscyklustilstand i livscyklusmodellen, skal du vælge den i sektionen **Resterende livscyklustilstande** og derefter vælge knappen med højre pil ![Højre pil](media/12-setup-for-work-orders.png) for at flytte den til sektionen med **Valgte livscyklustilstande**.
    - Hvis du vil inkludere alle de tilgængelige livscyklustilstande i livscyklusmodellen, skal du vælge knappen **Vælg alle tilgængelige stadier** ![Vælg alle tilgængelige stadier](media/13-setup-for-work-orders.png). Alle livscyklustilstande flyttes til sektionen **Valgte livscyklustilstande**.
    - Hvis du vil fjerne en livscyklustilstand fra livscyklusmodellen, skal du vælge den i sektionen **Valgte livscyklustilstande** og derefter vælge knappen med venstre pil ![Venstre pil](media/14-setup-for-work-orders.png) for at flytte den til sektionen med **Resterende livscyklustilstande**.

6. Vælg **Opdateringer til livscyklustilstande** for at definere de livscyklustilstande, der kan følge en valgt livscyklustilstand.
7. I oversigtspanelet **Opdateringer** i feltet **Planlagt tilstand** skal du vælge den livscyklustilstand, der altid skal være valgt for en arbejdsordre, som du har fuldført arbejdsordreplanlægning for, uanset den tidligere livscyklustilstand for arbejdsordren.
8. Vælg den livscyklustilstand, der altid skal være valgt for en arbejdsordre, hvis arbejdsordreplanlægning slettes, i feltet **Ikke-planlagt livscyklustilstand**.
9. Gem livscyklusmodellen for arbejdsordren.

![Siden Livscyklusmodeller for arbejdsordre](media/15-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]