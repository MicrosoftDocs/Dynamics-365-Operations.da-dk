---
title: Læg på lager-klynger
description: Læg på lager-klynger giver mulighed for at plukke flere id'er samtidigt og derefter tage dem til læg på lager forskellige steder. De kan være meget nyttige for detailforretninger, hvor id'erne typisk ikke er fulde lagerpaller.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c2b12798a6ef9c2d4aa022e0c270d8191b2cf4e7fc844042ed88c4eb9f5b98a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741902"
---
# <a name="putaway-clusters"></a>Læg på lager-klynger

[!include [banner](../includes/banner.md)]

Læg på lager-klynger giver mulighed for at plukke flere id'er samtidigt og derefter tage dem til læg på lager forskellige steder. Denne proces omtales ofte som en *leveringsrute*. Læg på lager-klynger kan være meget nyttige for detailforretninger, hvor id'erne typisk ikke er fulde lagerpaller. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Aktivere funktionen læg på lager-klynge

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Funktionen læg på lager-klynge*

## <a name="setup-for-the-example-scenario"></a>Konfiguration af eksempelscenariet

### <a name="cluster-profiles"></a>Klyngeprofiler

Læg på lager-klyngeprofilen bestemmer, hvor en vare placeres, på baggrund af den lokation, der er tildelt varen på modtagelsestidspunktet. Hvis der kræves forskellige klynger, skal der oprettes andre læg på lager-klynger, én for hvert menupunkt på mobilenheden.

1. Gå til **Lokationsstyring \> Opsætning \> Mobilenhed \> Klyngeprofiler**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i visningen **Overskrift**:

    - **Læg på lager-klyngeprofil-id:** *Læg på lager-klynge*
    - **Læg på lager-klyngeprofil-id-navn:** *Læg på lager-klynge*
    - **Klyngetype:** *Læg på lager*
    - **Løbenummer:** Accepter standardværdien.

1. Vælg **Gem** for at gøre de påkrævede felter i oversigtspanelet **Generelt** tilgængelige.
1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Tidsindstilling for klyngetildeling:** *Ved modtagelse*

        Dette felt definerer, om læg på lager-klyngen skal tildeles med det samme, når lageret modtages, eller om det skal gøres senere.

    - **Regel for klyngetildeling:** *Manuel*

        Dette felt definerer, om klyngetildelingen skal registreres automatisk af systemet eller manuelt af brugeren.

    - **Vejledningskode:** Lad feltet være tomt.
    - **Find Læg på lager-klynge:** *Modtagelse*

        Følgende værdier er tilgængelige:

        - **Modtagelse** – En lokation blev fundet umiddelbart under modtagelsen.
        - **Klyngelukning** – En lokation findes, når klyngen lukkes.
        - **Brugerstyret** – Der findes en lokation, når id'et plukkes fra klyngen for læg på lager. I dette tilfælde er der ikke angivet en lokation, når det læg på lager-arbejde oprettes. Under selve læg på lager skal brugeren scanne nummerpladen-id eller arbejds-id for at starte læg på lager-trinnet. Systemet finder derefter læg på lager-lokationen igen og fortæller brugeren, hvor det plukkede antal skal placeres.

    - **Læg på lager-klynge pr. bruger:** *Nej*

        Dette felt definerer, om de enkelte klynger skal være entydige pr. bruger, når klynger tildeles automatisk. Den er kun tilgængelig, når feltet **Klyngetildelingsregel** er angivet til *Automatisk*.

    - **Enhedsbegrænsning:** Lad feltet være tomt.

        I dette felt defineres den enhed, der skal være modtaget, for at profilen er gyldig. Hvis det er tomt, vil alle enheder være gyldige.

    - **Opdeling af arbejdsenhed:** *Individuel*

        Dette felt definerer, om al lagerbeholdning skal konsolideres (ved hjælp af klynge-id og nummerplade-) på én nummerplade, når en klynge lukkes, og om den skal lægges på lager som en enkelt nummerplade eller separat på de nummerplader, der er modtaget. Dette felt er ikke tilgængeligt, når feltet **Find Læg på lager-klynge** er angivet til *Modtagelse*.

    - **Klyngen fortsætter som overordnet id:** *Nej*

        Hvis denne indstilling er angivet til *Ja*, når læg på lager-trinnet udføres, bliver klynge-id'et til et overordnet nummerplade-id, og alle varer i klynge-id'et vil blive knyttet til dette id.

1. I oversigtspanelet **Klyngesortering** kan du definere sorteringskriterier for læg på lager. Vælg **Ny** på værktøjslinjen for at tilføje en linje, og angiv derefter følgende værdier:

    - **Løbenummer:** Accepter standardværdien.
    - **Feltnavn:** *WMSLocationId*

        Dette felt definerer det felt, som denne linje skal bruge som sorteringskriterium.

    - **Sortering:** *Stigende*

        Dette felt definerer, om sorteringen skal udføres i stigende eller faldende rækkefølge.

1. I oversigtspanelet **Arbejdsskabelon for klynge** skal du vælge **Ny** på værktøjslinjen for at tilføje en linje og derefter angive følgende værdier:

    - **Arbejdsordretype:** *Indkøbsordrer*
    - **Arbejdsskabelon:** *61 PO Direct*

1. Vælg **Gem** i handlingsruden, og vælg derefter **Rediger forespørgsel**.
1. I dialogboksen **Læg på lager-klynge** skal du under fanen **Interval** vælge **Tilføj** for at tilføje endnu en linje i forespørgslen. Opdater derefter forespørgselslinjerne som vist i følgende tabel.

    | Tabellen | Afledt tabel | Felt | Afgrænsning |
    |---|---|---|---|
    | Arbejde | Arbejde | Lagersted | *61* |
    | Arbejde | Arbejde | Arbejds-id | Lad feltet være tomt. |

1. Vælg **OK** for at gemme forespørgslen og lukke dialogboksen.
1. Vælg **Gem** i handlingsruden, og luk siden.

> [!IMPORTANT]
> De felter i klyngeprofilen, der vises nedtonet, når **Generér klynge-id** er angivet til *Ja*, er ikke tilgængelige og tages ikke med i betragtning, når denne funktion bruges.

### <a name="mobile-device-menu-items"></a>Menupunkter i mobilenhed

Der findes to nye menupunkter for mobilenheder til denne funktion. Menupunktet **Modtag og sortér klynge** bruges til at sortere den modtagne lagerbeholdning til en læg på lager-klynge ved modtagelse. Menupunktet **Læg på lager-klynge** bruges til at lægge klyngen på lager, efter at den er tildelt.

#### <a name="receive-and-sort-cluster"></a>Modtage og sortere klynge

Opret et nyt menupunkt til mobilenheder til modtagelse af lager og sortering i en klynge. Dette menupunkt opretter indgående arbejde, efter at der er modtaget en lagerbeholdning, hvilket angiver, at det modtagende menupunkt bruges til læg på lager-klynger.

> [!NOTE]
> Menupunktet **Modtag og sortér klynge** kan bruges sammen med følgende elementer til modtagelse af menupunkter:
>
> - Indkøbsordrelinje til modtagelse
> - Indkøbsordrevare til modtagelse
> - Modtagelse af varelast

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i visningen **Overskrift**:

    - **Navn på menupunkt:** *Modtag og sortér klynge*
    - **Titel:** *Modtag og sortér klynge*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Nej*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Arbejdsoprettelsesproces:** *Indkøbsordrevare til modtagelse*
    - **Generer nummerplade:** *Ja*
    - **Tildel læg på lager-klynge:** *Ja*

        > [!NOTE]
        > Indstillingen **Tildel læg på lager-klynge** er kun tilgængelig i forbindelse med aktiviteten *Arbejdsoprettelsesproces* for modtagelse.

    Acceptér standardværdierne for alle de andre felter.

1. Vælg **Gem** i handlingsruden.

#### <a name="cluster-putaway"></a>Klynge for Læg på lager

Opret et nyt menupunkt til mobilenheder til at lægge klyngen på lager, efter at den er tildelt.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i visningen **Overskrift**:

    - **Menupunktnavn:** *Læg på lager-klynge*
    - **Titel:** *Læg på lager-klynge*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Ja*

1. I oversigtspanelet **Generelt** skal du indstille feltet **Styret af** til *Læg på lager-klynge*. Acceptér standardværdierne for alle de andre felter.
1. Konfigurer den gyldige arbejdsklasse for dette menupunkt i mobilenheden i oversigtspanelet **Arbejdsklasser**:

    - **Arbejdsklasse-id:** *Indkøb*
    - **Arbejdsordretype:** *Indkøbsordrer*

1. Vælg **Gem** i handlingsruden.

### <a name="mobile-device-menu"></a>Menu i mobilenhed

Tilføj de menupunkter, du netop har oprettet, i menuen Indgående i mobilappen.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg **Rediger** i handlingsruden.
1. Vælg **Indgående** på menulisten.
1. På listen **Tilgængelige menuer og menupunkter** skal du finde og vælge **Modtag og sortér klynge**.
1. Vælg den højre pileknap for at flytte menupunktet til listen **Menustruktur**.
1. Brug knappen Pil op eller Pil ned til at flytte menupunktet til den ønskede placering i menuen.
1. Vælg **Gem** i handlingsruden.
1. Gentag trin 4-7 for at tilføje de resterende menupunkter.

    - Tildel klynge
    - Klynge for Læg på lager

## <a name="example-scenario"></a>Eksempelscenario

Dette scenario simulerer behandling af læg på lager-klyngen.

### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Kreditor \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:

    - **Kreditorkonto:** *1001*
    - **Lagersted:** *61*

1. Vælg **OK**.

    Siden **Alle indkøbsordrer** vises.

1. På siden **Alle indkøbsordrer** i oversigtspanelet **Indkøbsordrelinjer** skal du bruge knappen **Tilføj linje** for at tilføje følgende linjer:

    - Indkøbsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antal:** *10*

    - Indkøbsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antal:** *20*

    - Indkøbsordrelinje 3:

        - **Varenummer:** *M9215*
        - **Antal:** *30*

1. Vælg **Gem** i handlingsruden.
1. Notér dig købsordrenummeret.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Modtage lagerbeholdning og lægge det på lager fra mobilenheden

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Modtage og sortere lageret i en klynge

1. Log på mobilappen Lokationsstyring som en bruger, der er konfigureret til lagersted *61*.
1. I hovedmenuen skal du vælge **Indgående**.
1. Vælg **Modtag og sortér klynge** i menuen **Indgående**.
1. Angiv indkøbsordrenummeret i feltet **IO-num**.
1. Vælg knappen **OK** (markeringssymbol).
1. Vælg feltet **Vare**, angiv *A0001* som varenummeret, og vælg **OK**.
1. Vælg feltet **Antal**, indtast *10* på det numeriske tastatur, og vælg derefter knappen med markeringen.
1. Vælg **OK** (knappen med markeringen) på siden **Antal** for at bekræfte det antal, du har angivet.
1. Vælg **OK** på opgavesiden **Vare** for at bekræfte, at varen *A0001* blev angivet.
1. Vælg feltet **Klynge-id**, og angiv en værdi, der tildeles et id for den klynge, du opretter.

    Det id, du angiver her, bruges, når de to resterende varer på indkøbsordren modtages.

1. Vælg **OK**.

    Opgavesiden **IO-num** vises med meddelelsen "Arbejde fuldført".

    Vare *A0001* er nu modtaget på lokationen *RECV* og tildelt det klynge-id, du angav i trin 10.

1. Gentag trin 4 til 11 for at få de resterende to varer fra indkøbsordren tildele dem klynge-id'et:

    - Antallet *20* for vare *A0002*
    - Antallet *30* for vare *M9215*

#### <a name="close-the-cluster"></a>Luk klyngen

Før varerne i klyngen kan lægges på lager, skal klyngen lukkes.

1. I Supply Chain Management skal du gå til **Lokationsstyring \> Arbejde \> Udgående \> Arbejdsklynger**.
1. Søg efter feltet **Klynge-id** for det klynge-id, du har angivet tidligere, i sektionen **Arbejdsklynge** på siden **Arbejdsklynger**.
1. Hvis klyngen ikke vises, er den muligvis allerede lukket. Hvis du vil finde ud af, om klyngen blev lukket, skal du markere afkrydsningsfeltet **Vis lukket arbejde** og søge efter det klynge-id, du har angivet tidligere. Udfør derefter ét af følgende trin:

    - Hvis klyngen er lukket, kan du springe de resterende trin i denne procedure over og gå videre til den næste procedure, [Lægge klyngen på lager](#put-the-cluster-away).
    - Hvis klyngen ikke er lukket, skal du følge de resterende trin i denne procedure for at lukke klyngen manuelt. Gå derefter videre til næste procedure.

1. Vælg det klynge-id, du har angivet tidligere, i sektionen **Arbejdsklynge**.
1. I handlingsruden skal du vælge **Luk klynge**.

    Når klyngen er lukket, vises den ikke længere i sektionen **Arbejdsklynger** (medmindre afkrydsningsfeltet **Vis lukket arbejde** er markeret).

#### <a name="put-the-cluster-away"></a>Lægge klyngen på lager

1. Log på mobilappen Lokationsstyring som en bruger, der er konfigureret til lagersted *61*.
1. I hovedmenuen skal du vælge **Indgående**.
1. Vælg **Læg på lager-klynge** i menuen **Indgående**.
1. Vælg **Klynge-id**, og angiv det klynge-id, du tidligere har angivet til den lukkede klynge.
1. Vælg **OK**.

    Siden **Læg på lager-klynge: Pluk** vises. Den viser klynge-id'et, plukpladsen, varerne (værdien *Flere* vil blive vist) og det samlede antal i klyngen, der skal plukkes.

1. Vælg **OK**.

    Siden **Læg på lager-klynge: Læg** vises. **Læg**-instruktionerne identificerer klynge-id'et, læg på lager-lokationen, varerne, det samlede antal og nummerplade-id'erne for de varer, der er modtaget i klyngen.

    Du har standardindstillingerne til at tilsidesætte eller ignorere dette trin.

    ![Siden Læg på lager-klynge: Læg.](media/Cluster_putaway-Put.png "Siden Læg på lager-klynge: Læg")

1. Vælg **OK** for at bekræfte læg på lager af klyngen.

    Meddelelsen "Klynge er fuldført" vises.

## <a name="notes-and-tips"></a>Noter og tip

For de tilfælde, hvor klynge-id'et bliver til det overordnede id for en indlejret Palle, angives positionen automatisk, når klynge-id'et scannes. Der skal ikke scannes flere id'er, selvom id-genereringen er angivet til manuel.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]