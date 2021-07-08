---
title: Containerisering
description: Dette emne beskriver, hvordan du automatiserer containeriseringen af laster. Automatiseret containerisering opretter containere og plukkearbejde til forsendelser, når en bølge behandles.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 88e38989e3d3e46d0c43779659bc6ea2e29f08e2
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292731"
---
# <a name="containerization"></a>Containerisering

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du automatiserer containeriseringen af laster. Automatiseret containerisering opretter containere og plukkearbejde til forsendelser, når en bølge behandles.

Hvis du vil konfigurere containerisering, skal du oprette følgende:

- **Containertype** – Definer de fysiske egenskaber ved containerne. Brug containertyper til at pakke lagervarer i en bestemt type og størrelse af emballage, f.eks. beholdere eller paller.
- **Containergrupper** – Opret grupper af containertyper, der ligner hinanden. En containergruppe kan f.eks. indeholde containertyper, der har samme størrelsesdimensioner. En containergruppe angiver den rækkefølge, hvori containerne pakkes, og hvor stor en procentdel af hver container der fyldes.
- **Skabelon til container-build** – Opret skabeloner, der definerer regler for containerisering. Det kan f.eks. være regler for blandingslager og andre pakkestrategier.
- **Bølgeskabeloner** – konfigurer en eller flere bølgeskabeloner til at oprette plukkearbejde for containerisering.

## <a name="create-wave-templates-for-containerization"></a>Oprette bølgeskabeloner til containerisering

Du skal konfigurere en eller flere forsendelsesbølgeskabeloner til containerisering. Bølgeskabeloner indeholder kriterier, der bestemmer følgende:

- Hvordan bølger behandles. Det kan være enten manuelt eller automatisk.
- Hvordan du opretter plukkearbejde. Dette bestemmes af bølgemetoderne. Bølgeskabelonen skal indeholde metoden **containerisering**.
- Hvordan varer eller fordelingslinjer matches med en bølge.

Du finder flere oplysninger under [Bølgeskabeloner](wave-templates.md).

## <a name="create-container-types"></a>Oprette containertyper

Brug containertyper til at oprette beskrivelser af containere, herunder maksimumværdier for fysiske størrelsesdimensioner og vægtkapaciteten. Når en containeriseret bølge behandles, oprettes containere, der er baseret på oplysningerne om containertypen.

Følg disse trin for at konfigurere en containertype:

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Containertype**.
1. Vælg **Ny** for at oprette en ny containertype.
1. Angiv et entydigt id og en beskrivelse af containertypen.
1. I feltet **Taravægt** skal du angive den faktiske eller anslåede vægt af containeren.
1. I feltet **Maksimal vægt** skal du angive den maksimumvægt, som containeren kan indeholde.
1. I felterne **Maksimumvolumen ved containerisering**, **Maksimumlængde ved containerisering**, **Maksimumbredde ved containerisering** og **Maksimumhøjde ved containerisering** skal du angive containerens fysiske dimensioner.

    > [!NOTE]
    > Værdierne for længde og bredde kan erstatte hinanden. Det betyder, at du kan rotere varer lateralt eller på x-aksen, hvis det er nødvendigt. Hvis f.eks. længden er 2 meter, og bredden er 1 m, kan du ændre længden til 1 m og bredden til 2 meter. Bemærk, at dette ikke gælder for højdedimensionen. Du kan ikke ændre højdeværdien for at rotere en vare lodret.

1. Vælg Brugerdefinerede attributværdier for containeren i attributfelterne. Attributter er brugerdefinerede værdier, der bruges til at filtrere eller sortere elementer baseret på en værdi, som ellers ikke er tilgængelig. Hvis du f.eks. vil pakke varerne til en bestemt kunde, kan du oprette en attribut for kundenavnet. Opret attributter på siden **Containerattributter**.

## <a name="create-container-groups"></a>Oprette containergrupper

Du kan konfigurere logiske grupper af containertyper. For hver gruppe kan du angive den rækkefølge, som containerne skal pakkes i, og hvor stor en procentdel af containerne der skal fyldes. Størrelsesdimensionerne for varen bestemmer, om den kan passe ind i en container. Den container, der er tættest på varens størrelsesdimension, bruges. Hvis du har flere containertyper i en gruppe, anbefaler vi, at du arrangerer rækkefølgen efter størrelse, så den største container er først, nummer 1 i rækkefølgen, og den mindste container er sidst.

Følg disse trin for at konfigurere en containergruppe:

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Containergrupper**.
1. Vælg **Ny** for at oprette en ny containergruppe.
1. Angiv et entydigt id, og beskriv containergruppen.
1. I oversigtspanelet **Detaljer** skal du vælge **Ny** for at føje en containertype til gruppen.
1. Vælg en containertype i feltet **Containertype**.
1. Vælg **Flyt op** eller **Flyt ned** for at angive den rækkefølge, som containertyperne er pakket i.

## <a name="create-container-build-templates"></a>Oprette skabeloner til container-build

Du kan konfigurere regler for containerprocessen, som f.eks regler for lagerblanding og andre emballagestrategier. Du kan for eksempel konfigurere en regel, så arbejdere ikke kan pakke fordelingslinjer, der repræsenterer salgsordrer fra forskellige kunder i samme container.

Følg disse trin for at definere en containerbuildskabelon:

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Skabelon til container-build**.
1. Opret en ny containerbuildskabelon.
1. Angiv navnet på den containerskabelon og den ordrer, der er afstemt med fordelingslinjerne, i felterne **Containeriseringsnavn** og **Løbenummer**.

    > [!NOTE]
    > Systemet anvender den første skabelon, for hvilken fordelingslinjen opfylder forespørgselskriterierne. Placer derefter skabelonen med de mest specifikke kriterier øverst på listen. Jo bredere kriterier, desto mere sandsynligt er det, at en fordelingslinje opfylder kriterierne. Dette kan føre til linjer, der tildeles den forkerte container. Du kan om nødvendigt vælge **Flyt op** eller **Flyt ned** for at ændre rækkefølgen af skabeloner.

1. I feltet **Containergruppe-ID** skal du vælge den containergruppe, ud fra hvilken der skal oprettes containere.
1. I **Basisforespørgselstyper** skal du vælge den forespørgselstype, der bestemmer, hvad der skal pakkes, og hvad filterforespørgslen skal baseres på. Der findes følgende indstillinger:

      - **Salgsfordelingslinje** – Pakkefordelingslinjer, der oprettes til salgsordrer.
      - **Flyttefordelingslinje** – Pakkefordelingslinjer, der oprettes til flytteordrer.
      - **Container** – Pak en container, der allerede er blevet oprettet af containeriseringsprocessen. Dette bruges f.eks. til indlejring af containere.

        > [!NOTE]
        > Hvis du vil bruge indlejrede containere, skal du gøre det muligt at gentage containeriseringsmetoden. Du finder flere oplysninger under [Bølgeskabeloner](wave-templates.md).

1. I oversigtspanelet **Generelt** skal du i feltet **Kode for bølgetrin** angive det entydige id for den bølgeprocesmetode, der knytter containerbuildskabelonen sammen med trinnene i en bølgeskabelon.
1. Markér afkrydsningsfeltet **Tillad opdeling af plukninger** for at give arbejdere mulighed for at pakke arbejdsordrer i separate containere. Dette kræver, at hele antallet passer i containeren. Den største måleenhed i fordelingslinjen bruges altid.
1. Vælg **Pak efter enhed**, og vælg den måleenhed, der repræsenterer containeren. Du kan f.eks. angive, at en kasse er en container. Hvis du pakker efter måleenheden, kan du ikke samtidig angive en containergruppe, fordi måleenheden er containeren.
1. Vælg den pakkestrategi, der skal bruges, i feltet **Strategi for containerpakning**. Der findes følgende indstillinger:

    > [!NOTE]
    > Strategien gælder kun for salgsfordelingslinjer og flyttefordelingslinjer.

      - **Pak i alle åbne containere** – Systemet evaluerer, om fordelingslinjen passer ind i en container, der blev oprettet under containeriseringscyklussen.
      - **Pak kun i aktuel container** – Systemet evaluerer kun, om fordelingslinjen passer ind i den senest oprettede container.

    Du kan finde flere oplysninger og eksempler, der viser, hvordan du kan arbejde med pakningsstrategier for containere, i [Pakningsstrategier for containere](container-packing-strategy-overview.md).

1. Hvis du vil konfigurere regler for fordelingslinjer for pakning i containere, skal du vælge **Pauser i blandingsregler**. Du kan f.eks. oprette en regel, der tillader arbejdere at pakke fordelingslinjer for to forskellige varer i den samme container. Følg disse trin for at definere en blandingsregel:

    1. Vælg **Ny** på siden **Pauser i blandingsregler**.
    1. I feltet **Tabel** skal du vælge den tabel, der indeholder det felt, der skal bruges som kriterie for pause i blandingsreglen.
    1. I feltet **Feltvalg** skal du vælge det felt, der skal bruges som kriterie for pause i blandingsreglen.
    1. Gentag disse trin, indtil du har alle kriterier for pause i blandingsreglen.

    > [!NOTE]
    > Hvis du bruger blandingsregler, anbefaler vi, at du sorterer efter de samme felter i forespørgslens filterkriterier. Dette reducerer antallet af containere, der oprettes.
