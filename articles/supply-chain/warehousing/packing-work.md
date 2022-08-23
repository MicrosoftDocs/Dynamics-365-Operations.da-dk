---
title: Pakkearbejde til pakning af udgående containere og behandling af forsendelser
description: Denne artikel beskriver arbejdsordretypen "Pakning", som administrerer arbejdet for pakning af containere og understøtter delforsendelser af pakkede containere, der er relateret til laster, hvor lagervarer fortsat ikke er pakkede.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220547"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Pakkearbejde til pakning af udgående containere og behandling af forsendelser

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver arbejdsordretypen *Pakning*, som administrerer arbejdet for pakning af containere og understøtter delforsendelser af pakkede containere, der er relateret til laster, hvor lagervarer fortsat ikke er pakkede. Med pakkearbejde kan du bruge [Bekræft og flyt](confirm-and-transfer.md)-funktionalitet til at bekræfte udgående forsendelser, der er tilknyttet containere.

Pakkearbejde oprettes automatisk, når lager, der er relateret til kildedokumentarbejde, gemmes på lokationer af typen *Pakkelokation*. Arbejdet består af to linjer, én for *Pluk* og én for *Læg på lager* og vedligeholdes automatisk som en del af en containerlukkeproces/-genåbningsproces.

Yderligere oplysninger om, hvordan du opretter og bruger containerpakkeprocessen, finder du i [Pakke containere til forsendelse](packing-containers.md).

## <a name="turn-on-the-feature"></a>Slå funktionen til

Hvis systemet ikke allerede indeholder de funktioner, der er beskrevet i denne artikel, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funktioner i denne rækkefølge. Begge funktioner er del af modulet **Lagerstedsstyring**.

1. *Bekræft og flyt*
1. *Pakkearbejde for pakkestationer*

## <a name="set-up-a-location-for-packing-work"></a>Konfigurere en lokation til pakkearbejde

Benyt følgende fremgangsmåde til at definere pakkelokationer. For hver lokation kan du vælge, om systemet automatisk opretter pakkearbejde.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Pakning \> Konfiguration af pakkestation**.
1. I handlingsruden skal du vælge **Ny** for at tilføje en konfigurationspost til pakkestation.
1. Angiv følgende felter i den nye post:

    - **Lagersted** – Vælg eller indtast det lagersted, hvor pakkestationen er placeret.
    - **Lokation** – Vælg eller indtast pakkelokationen. Lokationen skal tilknyttes en lokationsprofil, der bruger den lokationstype, der er konfigureret som pakkelokationstype for dit firma, på siden **Parametre til lokationsstyring**. Du kan finde flere oplysninger i [Pakke containere til forsendelse](packing-containers.md).
    - **Opret pakkearbejde** – Markér dette afkrydsningsfelt for at oprette pakkearbejde, hver gang varer leveres til pakkelokationen. Arbejdet indeholder links til relaterede lastlinjer, så dellaster kan pakkes og leveres.

## <a name="example-scenario"></a>Eksempelscenario

I dette eksempelscenario vises, hvordan du kan behandle et udgående salgsordreflow ved at pakke en container og sende en dellast.

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge dette scenarie som vejledning i at bruge funktionen i et produktionssystem. I dette tilfælde skal du dog erstatte dine egne værdier for hver af de indstillinger, der beskrives her.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Konfigurere pakkearbejde for lagerstedets pakkelokation

Du kan kun komme i gang, hvis du konfigurerer arbejdsprocessen *Pakning* for et bestemt lagersted og en bestemt lokation.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Pakning \> Konfiguration af pakkestation**.
1. Vælg **Ny** i handlingsruden for at tilføje en ny konfigurationspost.
1. Angiv følgende værdier i den nye post:

    - **Lagersted:** *62*
    - **Lokation:** *Pakke*
    - **Opret pakkearbejde:** *Ja*

1. Luk siden **Konfiguration af pakkestation**.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Opret en lastskabelon, der tillader delvis levering.

Hvis du vil aktivere, at en last leveres via flere forsendelser, skal du knytte den til en lastskabelon, der giver mulighed for delvis forsendelse. Følg disse trin for at oprette den påkrævede skabelon.

1. Gå til **Lagerstedsstyring \> Opsætning \> Last \> Lastskabeloner**.
1. Vælg **Ny** i handlingsruden for at tilføje en ny konfigurationspost.
1. Angiv følgende værdier i den nye post:

    - **Id'et for lastskabelonen:** *Delvis*
    - **Tillad opdeling af lastlinje under afsendelsesbekræftelse:** *Ja*

1. Luk siden **Lastskabeloner**.

Yderligere oplysninger finder du under [Bekræfte og flytte](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Behandle en salgsordre

Benyt følgende fremgangsmåde for at behandle en salgsordre, så den leveres delvist.

1. Fuldfør [eksempelscenariet](packing-containers.md#scenario), der er angivet i [Pakke containere til forsendelse](packing-containers.md). I så fald skal du oprette en salgsordre på to styk af én vare. Derefter pakker du kun ét af styk i en container og lukker containeren. Du skal notere det forsendelses-id, du opretter, ned, sådan som det er vist i scenariet.
1. Gå til **Lagerstedsstyring \> Arbejde \> Alt arbejde**.
1. Markér afkrydsningsfeltet **Vis lukket arbejde** i filterområdet. Angiv derefter forsendelses-id'et i feltet **Filter**, og vælg at filtrere efter værdien **Forsendelses-id**. Du bør nu se tre arbejdsoverskrifter. Den ene er til salgsordreplukarbejdet og har statussen *Lukket*. To er til pakkeprocessen: Den ene er relateret til den lukkede container og har statussen *Lukket*, mens den anden vedrører den upakkede resterende vare og har statussen *Åben*.
1. Vælg værdien **Last-id** for enhver af arbejdsoverskrift for at åbne siden **Lastdetaljer** for lasten.
1. Skift til **overskriftsvisningen**.
1. Vælg knappen **Rediger** i feltet **Lastskabelon-id** i oversigtspanelet **Generelt**. Vælg derefter den lastskabelon for delvis levering, du har oprettet i dette scenario (*Delvis*).
1. I handlingsruden på fanen **Send og modtag** i gruppen **Bekræft** skal du vælge **Udgående forsendelse**.
1. Vælg indstillingen **Opdel antal til ny last** i dialogboksen **Bekræft afsendelse**.
1. Vælg **OK**.

Du har nu afsendt én container, der er relateret til den oprindelige last, og systemet har oprettet en ny last for de resterende varer, der stadig skal pakkes i containere.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
