---
title: Placeringsstatus for lagersted
description: Dette emne indeholder en oversigt over funktionen til lagerstedsstatus.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 7b17df2afee22dde1af5c44de31c585069daa349
ms.sourcegitcommit: d03f301633175b15d46690fc97067820bf21579f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2020
ms.locfileid: "3775168"
---
# <a name="warehouse-location-status"></a>Placeringsstatus for lagersted

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management indeholder flere lokationsfelter, der giver dig fleksibilitet, når du arbejder med og vedligeholder lokationer. Du kan medtage lokationsstatusser i lokationsvejledningen for at give bedre kontrol over lagerstedsforløbet.

Følgende fire felter på siden **Lokationer** sporer oplysninger om den aktuelle status for en lokation. Disse felter giver lagerchefer mulighed for at få et overblik over statussen på lagerstederne. De giver også mulighed for avanceret rapportering og filtrering.

- **Varenummer** – den vare, der i øjeblikket findes på lokationen. Hvis lokationen indeholder flere varer, er feltet tomt.
- **Dato og klokkeslæt for seneste aktivitet** – tidsstemplet for den sidste lagertransaktion, der blev udført i forhold til lokationen.
- **Forældelsesdato** – den dato, hvor lagerbeholdingen på lokationen blev bragt ind på lagerstedet. Denne værdi beregnes på basis af den aldersfordelte dato for nummerpladen. Den er nøjagtig for steder, hvor nummerpladen bruges til sporing, men er muligvis ikke nøjagtig for lokationer, hvor nummpladen ikke bruges til sporing.
- **Lokationsstatus** – statussen for lokationen. Der er fire mulige værdier:

    - **Ikke fastlagt** – lokationsprofilen kan ikke spore status. Derfor er den aktuelle status ukendt.
    - **Tom** – der er i øjeblikket ingen lagerbeholdning på lokationen.
    - **Pluk** – der er udført udgående transaktioner i forhold til lokationen, siden den sidst var tom.
    - **Lager** – der er kun udført indgående transaktioner i forhold til lokationen, siden den sidst var tom.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Aktivér funktionen til status for lagersted

Før du kan bruge funktionen *Status for lagersted*, skal den være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Status for lagersted*

## <a name="set-up-warehouse-location-status"></a>Konfigurere status for lagersted

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Forbered de eksempeldata, der kræves i eksempelscenariet

Før du går i gang med at arbejde med scenariet, skal du aktivere eksempeldata og konfigurere funktionen som beskrevet i dette afsnit. Hvis du vil fuldføre eksempelscenariet, skal du enten bruge lagerstedsappen eller den browserbaserede emulator. De trin, der angives her, bruger lagerstedsappen. Fremgangsmåden for den browserbaserede emulator er den samme.

#### <a name="use-the-usmf-legal-entity"></a>Brug den juridiske enhed USMF

Hvis du vil arbejde dig gennem eksempelscenariet ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

#### <a name="set-up-location-profiles"></a>Konfigurer lokationsprofiler

Eksempelscenariet kræver, at du forbereder to lokationsprofiler.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Vælg **Rediger** for at sætte siden i redigeringstilstand.
1. Vælg profilen **MASSE-06**.
1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Aktivér vare på lokation:** – angiv denne indstilling til _Ja_.
    - **Aktiver dato og klokkeslæt for lokalitetsaktivitet:** – angiv denne indstilling til _Ja_.
    - **Aktivér lokationsstatus:** – angiv denne indstilling til _Ja_.

    Disse indstillinger styrer, om referencefelterne på lokationerne er aktive.

1. Gentag trin 3 ti 4 for profilen **PLUK-06**.

> [!NOTE]
> Når parametrene på lokationsprofilen (**Aktivér vare på lokation**, **Aktivér lokationsaktivitet**, **Aktivér lokationsstatus**) er angivet til *Ja*, vil systemet omgående opdatere de relevante lokationer ved at udføre jobbet *Konsistenskontrol af lagersteds placeringsstatus*.

### <a name="scenario"></a>Scenarie

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Vælg **Ny**.
1. Gå til dialogboksen **Opret indkøbsordre**, og gå til feltet **Kreditorkonto** i oversigtspanelet **Kreditor**, og vælg *104*.
1. I oversigtspanelet **Generelt** skal du i feltet **Lagersted** vælge *61*.
1. Vælg **OK**.
1. Den nye indkøbsordre (PO) åbnes. Den indeholder en tom linje i gitteret **Indkøbsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** _A0002_
    - **Antal:** _5_

1. Gå til handlingsruden, og vælg **Bekræft** i gruppen **Handlinger** under fanen **Køb** for at bekræfte indkøbsordren.
1. På mobilenheden skal du gå til **Indgående \> Købsmodtagelse**.
1. Vælg feltet **IO-num**, angiv indkøbsordrenummeret, og bekræft.
1. Vælg feltet **VARE**, angiv *A0002* som varenummeret, og bekræft.
1. Gå til siden **Antal**, og angiv *5* som antallet, og bekræft.

    Du kan angive antallet på en af følgende måder:

    - Vælg knappen plustegn (**+**) eller minustegn (**–**) for at tilføje eller fratrække en numerisk værdi.
    - Vælg det tomme felt mellem knapperne plustegn (**+**) og minustegn (**–**) for at åbne det numeriske tastatur.

1. Bekræft dit valg af varenummer *A0002* og et antal på *5*. Meddelelsen "Arbejde fuldført" vises nederst på siden.
1. Vælg menuknappen (kaldes også hamburger eller hamburgerknappen) i øverste højre hjørne, og vælg derefter **Annuller** for at afslutte **Købsmodtagelse** og vende tilbage til menuen **Indgående**.
1. Gå til indkøbsordresiden, og vælg **Arbejdsdetaljer** over gitteret **Indkøbsordrelinjer**.
1. Under fanen **Generelt** kan du se de oprettede værdier for **Arbejds-id** og **Målnummerplade-id**.
1. I sektionen **Linjer** kan du **lokationsværdierne** for arbejdstyperne *Pluk* og *Læg på lager*.
1. På mobilenheden skal du gå til **Indgående \> Læg indkøb på lager**.
1. Vælg feltet **Id**, angiv arbejds-id'et, og bekræft.
1. Bekræft en gang til for at fuldføre *Pluk*-posten.
1. Vælg menuknappen i øverste højre hjørne, og vælg derefter **Udfør** for at fuldføre *plukkearbejdet*.
1. Læg mærke til læg på lager-lokationen, og bekræft. Meddelelsen "Arbejde fuldført" vises nederst på siden.
1. Vælg menuknappen i øverste højre hjørne, og vælg derefter **Annuller** for at afslutte **Læg køb på lager**, og vend tilbage til menuen **Indgående**.
1. Vælg **Tilbage** for at vende tilbage til hovedmenuen.
1. I Dynamics 365 Supply Chain Management skal du gå til **Lokationsstyring \> Konfiguration \> Lager \> Lokationer**.
1. Filtrer efter **Lokation**, og angiv læg på lager-lokationen ud fra indkøbsordrearbejdet. Du bør se følgende resultater:

    - Kolonnen **Lokationsstatus** viser værdien *Lager*, fordi den sidste transaktion i forhold til denne lokation var læg på lager.
    - Kolonnen **Varenummer** viser en værdi for *A0002*, fordi den pågældende vare blev modtaget og lagt på lager på lokationen.
    - Kolonnen **Dato og klokkeslæt for seneste aktivitet** viser tidsstemplet for den dato og det tidspunkt, hvor arbejdet blev fuldført på lokationen.

1. Gå til **Kvalitet \> Flytning** på mobilenheden.
1. Vælg feltet **LOK/NP**, og angiv den lokation, du har noteret i forrige trin.
1. Bekræft de oplysninger, der vises. Noter det nummerpladenummer, der genereres.
1. På skærmbilledet **Til/oplysninger** skal du vælge feltet **LOK/NP** og angive *06A07R2S1B* som den lokation, varen skal flyttes til.
1. På skærmbilledet **Til-oplysninger** skal du bekræfte **NP**-værdien (id'et for målnummerpladen), som genereres automatisk. Meddelelsen "Arbejde fuldført" vises nederst på siden.
1. Vælg menuknappen i øverste højre hjørne, og vælg derefter **Annuller** for at afslutte **Flytning**, og vend tilbage til menuen **Kvalitet**.
1. Vælg **Tilbage** for at vende tilbage til hovedmenuen.
1. I Dynamics 365 Supply Chain Management skal du gå til **Lokationsstyring \> Konfiguration \> Lager \> Lokationer**.
1. Opdater siden **Lokationer**, og få vist den oprindelige læg på lager-lokation igen. Bemærk, at feltet **Lokationsstatus** nu er angivet til *Tom*, og kolonnen **Varenummer** er tom.
1. Få vist posten for lokationen *06A07R2S1B*, og bemærk, at værdien for **Status** er ændret til *Lager*, og at felterne for **Varenummer** og **Dato og klokkeslæt for seneste aktivitet** er blevet opdateret.
1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny**.
1. Gå til dialogboksen **Opret salgsordre**, og vælg **US-002** i feltet *Debitorkonto*.
1. Vælg *61* i feltet **Lagersted**.
1. Vælg **OK**.
1. Din nye indkøbsordre åbnes. Den indeholder en tom linje i gitteret **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** _A0002_
    - **Antal:** _1_

1. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Reservation** i menuen **Lager**.
1. På siden **Reservation** skal du vælge **Reserver parti** for at reservere ordrelinjen. Vælg derefter knappen **Luk** (**X**) i øverste højre hjørne for at lukke siden.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.
1. Gå til sektionen **Salgsordrelinjer**, og vælg **Arbejdsoplysninger** i menuen **Lagersted**.
1. Kopiér værdien **Arbejds-id**, der blev oprettet.
1. På mobilenheden skal du gå til **Udgående \> Salgsplukning**.
1. Vælg feltet **Id**, angiv det arbejds-id, du kopierede tidligere, og bekræft.
1. På siden **Salgsordrer: Pluk** foreslår feltet **LOK** pluklokationen som den læg på lager-lokation, der blev oprettet tidligere. Noter lokationen.
1. Vælg feltet **LOK**, angiv lokationen, og bekræft.
1. Vælg feltet **NP**, angiv nummerpladenummeret, du noterede under flytteaktiviteten, og bekræft.
1. Vælg feltet **Vare**, angiv *A0002* som varenummeret, og bekræft.
1. Gå til siden **Antal**, og angiv *1* som antallet, og bekræft.

    Du kan angive antallet på en af følgende måder:

    - Vælg knappen plustegn (**+**) eller minustegn (**–**) for at tilføje eller fratrække en numerisk værdi.
    - Vælg det tomme felt mellem knapperne plustegn (**+**) og minustegn (**–**) for at åbne det numeriske tastatur.

1. Vælg feltet **MÅL-NP**, angiv et brugerdefineret målnummerplade-id, og bekræft.
1. Bekræft en gang til for at fuldføre plukarbejdet. Meddelelsen "Arbejde fuldført" vises nederst på siden.
1. Vælg menuknappen i øverste højre hjørne, og vælg derefter **Annuller** for at afslutte plukaktiviteten og gå tilbage til menuen **Udgående**.
1. I Dynamics 365 Supply Chain Management skal du gå til **Lokationsstyring \> Konfiguration \> Lager \> Lokationer**.
1. Filtrer efter **Lokation**, og angiv pluklokationen ud fra salgsordrearbejdet.
1. Bemærk, at feltet **Lokationsstatus** for den lokation, som salgsordrearbejdet er plukket fra, nu er indstillet til *Pluk*, og at feltet **Dato og klokkeslæt for seneste aktivitet** er opdateret.

> [!NOTE]
> Lokationsfelterne opdateres kun ved lagertransaktioner. Hvis du flytter lager ved hjælp af en kladde eller andre ikke-WHS-processer, opdateres felterne ikke.
