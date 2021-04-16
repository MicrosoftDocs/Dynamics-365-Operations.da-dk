---
title: Placering af lokations-id
description: Med placering af nummerplader kan du se, hvor en nummerplade er placeret på en lokation med flere paller, f.eks. en lokation, der bruger en pallereol med dobbeltdybde.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: e5fd7a9a9703f9ab6802def0aac096e29aa04f1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831379"
---
# <a name="location-license-plate-positioning"></a>Placering af lokations-id

[!include [banner](../includes/banner.md)]

Med placering af nummerplader kan du se, hvor en nummerplade er placeret på en lokation med flere paller, f.eks. en lokation, der bruger en pallereol med dobbeltdybde.

Funktionen tilføjer et løbenummer til hver nummerplade, der anbringes på en lagerplacering. Dette løbenummer bruges til at bestille nummerpladerne på lagerstedet. Derfor understøtter funktionen intelligente scenarier, hvor kunder anvender et reolsystem og skal vide, hvilken nummerplade der er på forsiden af det af hensyn til plukning.

Dette emne indeholder et scenarie, der viser, hvordan du kan konfigurere og bruge funktionen.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>Aktivér funktionen til placering af nummerplade på lokation

Før du kan bruge funktionen til placering af nummerplads på lokation, skal den være aktiveret i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Placering af nummerplade på lokation*

## <a name="example-scenario"></a>Eksempelscenario

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem dette scenarie ved hjælp af de værdier, der er foreslået, skal du arbejde på et system, hvor eksempeldata er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

### <a name="set-up-the-feature-for-this-scenario"></a>Konfigurer funktionen til dette scenarie

Udfør følgende procedurer for at konfigurere funktionen til *placering af nummerplader på lokation* for det scenarie, der vises i dette emne.

#### <a name="location-profiles"></a>Lokationsprofiler

Funktionen skal være aktiveret i lokationsprofilen for hver lokation, hvor den vil blive brugt.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Vælg **MASSE-06** på listen over lokationsprofiler i ruden til venstre.
1. I oversigtspanelet **Generelt** er der to nye muligheder, der er blevet tilføjet af funktionen. Angiv følgende værdier:

    - **Aktiver nummerpladeplacering:** *Ja*

        Når denne indstilling er angivet til *Ja*, bevares nummerpladeplaceringen for nummerplader på lokationen.

    - **Vis NP-position på mobilenhed:** *Ja*

        Når denne indstilling er angivet til *Ja*, vises nummerpladens placering for brugere af mobilenheder under justering og optælling. Du kan kun ændre indstillingen af denne valgmulighed, når funktionen er slået til.

1. Vælg **Gem**.

#### <a name="location-directives"></a>Lokationsvejledninger

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I venstre rude skal du kontrollere, at feltet **Arbejdsordretype** er angivet til *Salgsordrer*.
1. På listen over lokationsvejledninger skal du vælge **61 SO Plukliste**.
1. Vælg **Rediger** i handlingsruden.
1. I oversigtspanelet **Linjer** skal du vælge den linje, hvor et **løbenummer** har værdien *2*.
1. I oversigtspanelet **Handlinger i lokationsvejledning** skal du vælge den linje, der har en værdi for **Navn** med *Vælg for mindre end palle* (den skal være den eneste linje) og ændre værdien for **løbenummer** til *2*.
1. Vælg **Ny** over gitteret for at tilføje en linje til en ny handling i lokationsvejledning.
1. Angiv følgende værdier på den nye linje:

    - **Løbenummer:** *1*
    - **Navn:** *Plukposition 1*

1. Mens den nye linje stadig er markeret, skal du vælge **Rediger forespørgsel** over gitteret.
1. Vælg forespørgselseditoren skal du vælge fanen **Joinforbindelser**.
1. Udvid tabeljoinet **lokationer** for at få vist joinet med tabellen **Lagerdimensioner**.
1. Udvid tabeljoinet **Lagerdimensioner** for at få vist joinet med tabellen **Disponibel lagerbeholdning**.
1. Vælg **Lagerdimensioner**, og vælg derefter **Tilføj tabeljoin**.
1. På listen over tabeller, der vises, skal du i kolonnen **Relation** vælge **Nummerplade (nummerplade)**. Vælg derefter **Vælg** for at føje en **Nummerplade** til tabeljoinet **Lagerdimensioner**.
1. Mens **Nummerplade** stadig er valgt, skal du vælge **Tilføj tabeljoin**.
1. På listen over tabeller, der vises, skal du i kolonnen **Relation** vælge **Placering af nummerplade på lokation (nummerplade)**. Vælg derefter **Vælg** for at føje **Placering af nummerplads på lokation** til tabeljoinet **Lagerdimensioner**.

    ![Tabeljoinforbindelser](media/LpTableJoin.png "Tabeljoinforbindelser")

1. Vælg **OK** for at bekræfte de opdaterede joinforbundne tabeller og lukke forespørgselseditoren.
1. I oversigtspanelet **Handlinger i lokationsvejledning** skal du vælge **Rediger forespørgsel** igen for at åbne forespørgselseditoren.
1. Gå til fanen **Interval**, og vælg **Tilføj** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Tabel:** *Placering af nummerplade på lokation*
    - **Afledt tabel:** *Placering af nummerplade på lokation*
    - **Felt:** *NP-position*
    - **Afgrænsning:** *1*

    ![Nyt område](media/LpPositionCriteria.png "Nyt område")

1. Vælg **OK** for at bekræfte dine ændringer og lukke forespørgselseditoren.

### <a name="set-up-sample-data-for-this-scenario"></a>Konfigurer eksempeldata til dette scenarie

I dette scenarie skal brugeren logge på den Warehouse Mobile App ved hjælp af en arbejder, der er konfigureret til lagersted *61*, for at udføre arbejde. Brugeren skal også fuldføre transaktioner.

Da funktionen *Placering af nummerplade på lokation* tilføjer et nyt id for nummerpladepositioner på en placering, skal du først oprette nogle data for at kunne understøtte scenariet.

#### <a name="spot-count-the-first-location"></a>Lav spotoptælling på den første lokation

1. Åbn Warehouse Mobile App, og log på lagersted *61*.
1. Gå til **Lager \> Spotoptælling**.
1. På siden **Spotoptælling** skal du angive feltet **Lokation** til *01A01R1S1B*.
1. Vælg **OK**.

    På siden vises den lokation, du har angivet. Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"

1. Vælg **Opdater** for at tilføje en optælling på lokationen.
1. På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **Vare** og derefter angive værdien *A0001*.
1. Vælg **OK**.
1. På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **NP** og derefter angive værdien *LP1001* (eller andre nummerplader efter eget valg).

    Siden **Cyklusoptælling: Tilføj ny NP eller vare** viser **Nummerpladeposition 1**.

1. Vælg **OK**.

    Du skal nu angive antallet for den vare, der er optalt på nummerpladen.

1. Angiv feltet **Antal** til *10*.
1. Vælg **OK**.

    På siden vises den lokation, du har angivet. Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"

1. Vælg **Opdater** for at tilføje en anden optælling på lokationen.
1. På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **Vare** og derefter angive værdien *A0002*.
1. Vælg **OK**.
1. På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **NP** og derefter angive værdien *LP1002* (eller andre nummerpladenumre, du vælger, hvis det er forskelligt fra det nummer, du har angivet tidligere).
1. Skift nummerpladens placering ved at indstille feltet **NP-position** til *2*.
1. Vælg **OK**.
1. Angiv det antal af varen, der er optalt på nummerpladen, ved at angive feltet **Antal** til *10*.
1. Vælg **OK**.

    På siden vises den lokation, du har angivet. Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"

1. Vælg **OK**.

Arbejde er nu fuldført.

#### <a name="spot-count-the-second-location"></a>Lav spotoptælling på den anden lokation

1. På siden **Spotoptælling** skal du angive feltet **Lokation** til *01A01R1S2B*.
1. Vælg **OK**.

    På siden vises den lokation, du har angivet. Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"

1. Vælg **Opdater** for at tilføje en optælling på lokationen.
1. På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **Vare** og derefter angive værdien *A0002*.
1. Vælg **OK**.
1. På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **NP** og derefter angive værdien *LP1003* (eller andre nummerpladenumre, du vælger, hvis det er forskelligt fra begge de nummerpladenumre, du har angivet i den forrige procedure).

    Siden **Cyklusoptælling: Tilføj ny NP eller vare** viser **Nummerpladeposition 1**.

1. Vælg **OK**.
1. Angiv det antal af varen, der er optalt på nummerpladen, ved at angive feltet **Antal** til *10*.
1. Vælg **OK**.

    På siden vises den lokation, du har angivet. Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"

1. Vælg **OK**.

Arbejde er nu fuldført.

#### <a name="work-details"></a>Arbejdsdetaljer

> [!NOTE]
> Lav spotoptælling via cyklusoptælling af arbejde i mobilappen i Microsoft Dynamics 365. Arbejdet kræver, at optællingerne accepteres, før de bogføres til lageret.

1. Log på Dynamics 365 Supply Chain Management.
1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. På fanen **Oversigt** skal du se efter de linjer, der har følgende værdier:

    - **Arbejdsordretype:** *Cyklusoptælling*
    - **Lagersted:** *61*
    - **Arbejdsstatus:** *Afventer gennemsyn*

    Der skal være oprettet to arbejds-id'er for disse linjer. Optællingerne for begge disse arbejds-id'er skal accepteres.

1. I gitteret skal du vælge det første arbejds-id for arbejdsordretypen *Cyklusoptælling*.
1. Gå til handlingsrunde og vælg **Cyklusoptælling** i gruppen **Arbejde** under fanen **Arbejde**.

    Der vises to linjer, én for hver vare og nummerplade. Værdierne i felterne **Optalt antal**, **Lokation**, **Nummerplade** og **Vare** skal svare til de optællingsposter, du har oprettet på mobilenheden. Hvis et eller flere af disse felter ikke er synlige, skal du vælge **Vis dimensioner** i handlingsruden for at føje dem til gitteret.

1. Vælg begge linjer.
1. Vælg **Accepter antal** i handlingsruden.
1. Du får vist meddelelse om "kladdebogføring". Vælg **Meddelelsesdetaljer** for at få vist det bogførte kladdenummer.
1. Luk meddelelsesdetaljerne.
1. Opdater siden **Arbejde**.

    Det første arbejds-id er lukket og vises ikke længere.

    > [!TIP]
    > Hvis du vil have vist lukket arbejde, skal du markere afkrydsningsfeltet **Vis lukket** over gitteret.

    Du accepterer nu arbejdet for nummerpladen på lokationen *01A01R1S2B*.

1. På fanen **Oversigt** skal du vælge det andet arbejds-id for arbejdsordretypen *Cyklusoptælling*.
1. Gå til handlingsrunde og vælg **Cyklusoptælling** i gruppen **Arbejde** under fanen **Arbejde**.

    Der vises en linje for varen og nummerpladen. Værdierne i felterne **Optalt antal**, **Lokation**, **Nummerplade** og **Vare** skal svare til de optællingsposter, du har oprettet på mobilenheden.

1. Vælg linjen.
1. Vælg **Accepter antal** i handlingsruden.
1. Du får vist meddelelse om "kladdebogføring". Vælg **Meddelelsesdetaljer** for at få vist det bogførte kladdenummer.
1. Luk meddelelsesdetaljerne.
1. Opdater siden **Arbejde**.

    Det andet arbejds-id er lukket og vises ikke længere.

    > [!TIP]
    > Hvis du vil have vist lukket arbejde, skal du markere afkrydsningsfeltet **Vis lukket** over gitteret.

#### <a name="on-hand-by-location"></a>Disponibel efter lokation

1. Gå til **Lokationsstyring \> Forespørgsler og rapporter \> Disponibel efter lokation**.
1. Angiv følgende værdier:

    - **Lokation:** *6*
    - **Lagersted:** *61*
    - **Opdater på tværs af lokationer:** *Ja*

1. Bemærk, at lokationen *01A01R1S1B* har to nummerplader:

    - **A0001**, hvor feltet **NP-position** er indstillet til *1*
    - **A0002**, hvor feltet **NP-position** er indstillet til *2*

1. Bemærk, at lokationen *01A01R1S2B* har én nummerplade:

    - **A0002**, hvor feltet **NP-position** er indstillet til *1*

### <a name="sales-order-scenario"></a>Salgsordrescenarie

Nu, hvor funktionen *Placering af nummerplade på lokation* er oprettet, og lageret er blevet gemt, skal du oprette en salgsordre for at generere plukarbejde, der anviser, at lagermedarbejderen skal plukke varen *A0002* fra det lagersted, hvor palle-id'et er i position *1*.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-004*
    - **Lagersted:** *61*

1. Vælg **OK**.
1. Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier på den nye linje:

    - **Varenummer:** *A0002*
    - **Antal:** *1*

1. Vælg **reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret til ordrelinjen.
1. Luk siden **Reservation**.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.

    Du modtager en orienterende meddelelse, der angiver bølge-id'et og forsendelses-id'et, der blev oprettet for ordren.

1. I oversigtspanelet **Salgsordrelinjer** skal du i menuen **Lager** over gitteret vælge **Arbejdsdetaljer**.
1. Siden **Arbejde** vises og viser det arbejde, der er oprettet for salgslinjen. Noter det arbejds-id, der vises.

### <a name="sales-picking-scenario"></a>Salgsplukscenarie

1. Åbn mobilappen, og log på lagersted *61*.
1. Gå til **Udgående \> Salgsplukning**.
1. Vælg feltet **Id** på siden **Scan et arbejds-id/nummerplade-id**, og angiv derefter arbejds-id'et fra salgslinjen.
1. Bemærk, at plukarbejdet dirigerer dig til at plukke vare *A0002* fra lokation *01A01R1S2B*. Du modtager denne instruktion, fordi vare *A0002* er på en licensnummerplade i position *1* på den pågældende lokation.

    ![Placering 1-lokation](media/LocationLicensePlatePositioning.png "Placering 1-lokation")

1. Angiv det nummerplade-id, du har oprettet for lokationen, og følg derefter vejledningen for at plukke salgsordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]