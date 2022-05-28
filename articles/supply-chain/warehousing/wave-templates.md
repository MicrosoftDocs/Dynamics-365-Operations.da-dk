---
title: Bølgeskabeloner
description: Dette emne beskriver, hvordan du konfigurerer de kriterier, der bestemmer, om bølger behandles manuelt eller automatisk, og det arbejde, der oprettes for et lagersted, når en bølge behandles.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 61fbcad572bbb69ab8a4eb2cd309cdf8a6328391
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686591"
---
# <a name="wave-templates"></a>Bølgeskabeloner

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer de kriterier, der bestemmer, om bølger behandles manuelt eller automatisk, og det arbejde, der oprettes for et lagersted, når en bølge behandles. Du angiver kriterierne ved at konfigurere bølgeskabeloner og forespørgsler, der svarer til en bølge med frigivne linjer i salgsordrer, produktionsordrer og kanbans.

## <a name="settings-for-wave-templates"></a>Indstillinger for bølgeskabeloner

Når du konfigurerer en bølgeskabelon, angiver du følgende:

- **Lokation** og **Lagersted**, som skabelonen opretter arbejde for.
- Den rækkefølge, som skabelonerne evalueres i. Den rækkefølge, hvori skabelonerne matches med frigivne linjer på salgsordrer, produktionsordrer og kanbans. Når en linje frigives, anvendes den første bølgeskabelon, som linjen opfylder kriterierne for. Jo bredere kriterierne er, jo mere sandsynligt er det, at en linje opfylder kriterierne, så du skal placere skabelonerne med de mest specifikke kriterier øverst på listen. Brug knapperne **Flyt op** og **Flyt ned** i handlingsruden til at arrangere skabelonerne på listen.
- De handlinger, der foretages af hver skabelon. De **bølgemetoder**, der udfører de handlinger, der oprettes af skabelonen, f.eks. oprette eller distribuere arbejde for hver type bølgeskabelon.
- De bølgeattributter (filtre), der skal anvendes til brug af bølgeskabelonen.

> [!NOTE]
> Hvis det er nødvendigt, kan en udvikler oprette yderligere metoder. Du kan få vist den fulde liste over metoder på siden **Bølgeprocesmetoder**.

Nogle indstillinger repræsenterer strategiske beslutninger i forhold til bølgebehandling på følgende måde:

- Hvis skabelonen bruges til levering af varer for salgsordrer og overførselsordrer eller bruges til at flytte produktsvarer til produktionsordrer eller kanbans.
- Hvis en bølge behandles manuelt eller automatisk:

  - **Manuel behandling** – Linjen føjes til en bølge, og lageret reserveres. Du skal dog vælge **Proces** på listesiden **Alle bølger** for at oprette plukarbejde til ordren.
  - **Automatisk behandling** – Du kan helt eller delvist automatisere bølgebehandling. Hvis du fuldautomatiserer bølgebehandlingen, oprettes en bølge, der indeholder linjen fra salgsordren, produktionsordre eller kanban, når en salgsordre, produktionsordre eller kanban oprettes. Varerne trækkes fra den disponible lagerbeholdning, og plukkearbejdet oprettes. Hvis du automatiserer bølgebehandlingen delvist, kan du angive værdier, der udløser bølgebehandlingen. Du kan f.eks. angive en maksimal vægt for forsendelser, der udløser bølgebehandling, når den samlede vægt af linjerne i bølgen når værdien.

- Hvis du tildeler forsendelser til en åben bølge. Hvis du f.eks. lover kunder, at der leveres en ordre, der er afgivet ved kl. 12.00 middag, inden for 24 timer, kan du konfigurere en bølgeskabelon, som automatisk tildeler ordrelinjer til en åben bølge indtil kl. 12.00 middag. Bølgen behandles automatisk på det pågældende tidspunkt.

Når en bølge er behandlet, vil det plukkearbejde, der er oprettet, blive baseret på den arbejdsskabelon og lokationsvejledning, der er angivet for lagerstedet. Arbejdsskabelonen angiver, hvordan plukkearbejdet oprettes, og lokationsvejledningen angiver placeringerne for pluk og læg på lager.

## <a name="create-a-wave-template"></a>Oprette en bølgeskabelon

Følg disse trin for at konfigurere en bølgeskabelon:

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Bølger** \> **Bølgeskabeloner**.
1. Vælg **Ny** for at oprette en ny bølgeskabelon.
1. Vælg en af følgende indstillinger i feltet **Bølgeskabelontype**:

    - *Forsendelse* - Bruge bølgeskabelonen til forsendelsesvarer til salgsordrer og flytteordrer.
    - *Produktionsordrer* - Brug bølgeskabelonen til at flytte varer til produktionsordrer.
    - *Kanban* - Brug bølgeskabelonen til at flytte varer til kanbanordrer.

1. Angiv et navn og en beskrivelse af bølgeskabelonen i felterne **Navn på bølgeskabelon** og **Beskrivelse af bølgeskabelon**.

    > [!NOTE]
    > Hvis der oprettes mere end én skabelon til lagerstedet, angiver tallet i feltet **Sekvens for bølgeskabelon** placeringen af skabelonen i den rækkefølge, hvori skabelonerne anvendes når skabelonens kriterier er opfyldt. Du kan vælge **Flyt op** eller **Flyt ned** for at ændre rækkefølgen af skabeloner.

1. I felterne **Lokation** og **Lagersted** skal du vælge stedet og lagerstedet, for hvilke bølgeskabelonen opretter bølger og plukkearbejde.
1. Hvis du vil automatisere bølgebehandling, skal du foretage følgende indstillinger efter behov:

    - **Automatiser bølgeoprettelse** - Angiv den til *Ja* for automatisk at oprette en bølge, når en salgsordre, produktionsordre eller kanban er frigivet til lagerstedet.
    - **Tildel til åbne bølger** - Angiv den til *Ja*, hvis der automatisk skal tildeles linjer til en åben bølge, når linjerne frigives. Linjerne tildeles bølger ud fra forespørgselsfiltret til bølgeskabelonen.
    - **Udfør behandling af bølgen ved frigivelse til lagerstedet** – Angiv dette til *Ja*, hvis du automatisk vil behandle bølgen og oprette arbejde, når en linje frigives til lagerstedet.
    - **Udfør automatisk behandling af bølge ved grænseværdi** - Angiv den til *Ja* for automatisk at behandle bølgen, når dens værdier når de grænser for vægt, levering, og linjer, der er angivet i feltgruppen **Grænser for bølge**. Denne indstilling er kun aktiv, hvis der er valgt *Forsendelse* i feltet **Bølgeskabelontype**.
    - **Automatiser bølgefrigivelse** – Angiv dette til *Ja*, så du automatisk frigiver bølgen. Plukkearbejdet oprettes og gøres tilgængeligt på mobilenheder.
    - **Automatiser frigivelse af genopfyldningsarbejde** - Angiv denne indstilling til *Ja* for at oprette behovsbaseret genopfyldningsarbejde og frigive det automatisk. Du skal føje genbestillingsbølgemetoden til bølgeskabelonen og oprette en genbestillingsskabelon med typen *Bølgebehov*. Konfigurer en genopfyldningsskabelon på siden **Genopfyldningsskabeloner**. Dette kræver, at du føjer genopfyldningsmetoden til bølgeskabelonen.
    - **Fortsæt bølgebehandling, når oprettelse af arbejde mislykkes** - Når den er angivet til *Ja*, vil systemet bruge en tom lokation, hvis det ikke kan reservere lager på den lokation, der foreslås af lokationsdirektivet (f. eks. fordi lageret ikke længere er tilgængeligt). Når den er angivet til *Nej*, mislykkes bølgen, hvis systemet ikke kan reservere lagerbeholdningen.

1. Angiv feltgruppen **Grænseværdi for bølge** efter behov:
    - **Vægtgrænsen for bølge** – Angiv den maksimale vægt, en bølge kan indeholde.
    - **Forsendelsesgrænse** – Angiv det maksimale antal forsendelser, der kan medtages i en bølge.
    - **Linjegrænse** – Angiv det maksimale antal linjer, der kan medtages i en bølge.

1. I feltgruppen **Standardværdier** skal du vælge de bølgeattributter, der skal bruges som yderligere kriterier for bølgeskabelonen. Bølgeattributter er nyttige til at tildele yderligere kriterier, f.eks. en bestemt kunde, til en bølgeskabelon. Opret disse attributter på siden **Bølgeattributter**. 

1. Indstil **Politik for bølgebesked** til den politik, du vil bruge til at generere beskeder, der er relateret til bølger, der bruger denne skabelon. Du kan se et eksempel på en politik for bølgebeskeder i [Beskeder om udførelse af bølge](wave-execution-notifications.md).

1. I oversigtspanelet **Metoder** viser ruden **Valgte metoder** metoderne for den valgte type bølgeskabelon. Bølgemetoderne udfører de handlinger, der oprettes af skabelonen, f.eks. oprette eller distribuere arbejde. Disse handlinger kaldes også bølgetrin. Bølgemetoder er foruddefinerede for hver type bølgeskabelon. Du kan ikke fjerne de foruddefinerede bølgemetoder, men du kan ændre rækkefølgen af metoderne og tilføje flere metoder. Hvis du f.eks. opretter en bølgeskabelon til forsendelse, kan du tilføje metoder til genopfyldning og containerbrug. Bølgecontainer kan føjes til en serie af bølgemetoder for at definere containerbrugen for de linjer, der behandles i bølgeskabelonen. Hvis du vil tilføje en ekstra metode, skal du gøre følgende:

    - Vælg en metode i ruden **Resterende metoder**, og vælg **Venstre** pil for at føje den til ruden **Valgte metoder**.
    - Hvis du vil ændre rækkefølgen, skal du vælge en metode og derefter klikke på pilene **Op** eller **Ned**.

    > [!NOTE]
    > Når du tilføjer en metode, vises den automatisk på den korrekte placering i trinrækkefølgen.

1. Hvis du vil konfigurere den forespørgsel, der svarer til de frigivne linjer, til en passende bølge, skal du vælge **Rediger forespørgsel** i handlingsruden.
1. Vælg **Valider skabelon** for at bekræfte, at indstillingerne for bølgeskabelonen er gyldige.
