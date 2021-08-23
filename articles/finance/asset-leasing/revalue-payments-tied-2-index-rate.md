---
title: Revaluere leasingbetalinger, der er knyttet til en indekssats
description: Dette emne beskriver den justering, der er foretaget for at lease passivet for et ROU-aktiv, når de variable leasede betalinger ændres på grund af en ændring af indekssatsen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1b3eed28ba6fc5af02c1bbf430cc9779426084f0eaf4e027141bbdd18a70dde4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734580"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Revaluere leasingbetalinger, der er knyttet til en indekssats

[!include [banner](../includes/banner.md)]

Dette emne beskriver den justering, der er foretaget i leasingforpligtelsen brugsretsaktiv (ROU)-aktiv, når de variable leasingbetalinger ændres på grund af en ændring af indekssatsen. Leasingforpligtelsen og ROU-aktiverne reguleres for at afstemme de nye betalinger. Under Accounting Standards Codification Topic 842 (ASC 842), som er standarden i almindeligt anerkendte regnskabsprincipper i USA (US GAAP), er det kun de variable betalinger, der ændres, når betalinger øges eller mindskes på grund af en ændring af indekseringshastigheden, medmindre der er flere ændringer i pengestrømme. Disse yderligere ændringer kan omfatte en ændring af de leasingbetingelser, der er knyttet til rentesatser. Yderligere oplysninger finder du under ASC 842-10-55-225 og stk. 42, litra b, i International Financial Reporting Standard 16 (IFRS 16).

## <a name="adjust-lease-payments"></a>Justere leasingbetalinger

Følg disse trin for at revaluere leasingbetalinger, der er knyttet til en indekssats.

1. Hvis du vil køre en værdireguleringsproces for rettighedsindeks, skal du gå til **Aktivleasing \> Periodisk \> Indeksrateregulering**.

    Siden **indeksregulering** vises og viser alle tidligere processer til leasingindeksregulering, der er blevet kørt. Oplysningerne på denne side indeholder det proces-ID, der blev oprettet ud fra nummerserieopsætningen, den juridiske enhed, antallet af leasingkartoteker, der blev justeret, den samlede regulering af forpligtelser for IFRS 16-leasingaftaler og de samlede variable betalinger, der er reguleret for ASC 842-leasingaftaler.

2. Hvis du vil køre værdireguleringen, skal du vælge **Leasingindeksregulering** i handlingsruden.

    Dialogboksen **Parametre til værdiregulering af indeks** vises. Her kan du filtrere og vælge, hvilke rettigheder, leasinggrupper eller andre kriterier, der skal bruges, når du vælger leasingaftaler til værdiregulering. Derudover kan du i fanen **Kør i baggrunden** angive indeksværdireguleringsprocessen, så den kører i en batch.

4. Vælg de filtre til valg af rettigheder, der skal medtages i baggrundsbehandlingen, og vælg derefter **OK**.

    Dialogboksen **Forhåndsversion af Vis indeksregulering** vises, og den viser de rettigheder, der vil blive værdiregulerede. Den indeholder også reguleringer af aktiver og passiver eller de variable betalingsjusteringer.
    
5. Hvis du vil forhindre, at leasingaftaler værdireguleres, skal du vælge de leasingaftaler, der **skal** værdireguleres. Hvis du ikke vælger nogen rettigheder, vil alle rettigheder blive værdireguleret. Når du er færdig, skal du vælge **OK** for at regulere leasingbetalinger.
6. Hvis du vil have vist de transaktioner, der er oprettet for en bestemt værdireguleringsproces, skal du vælge proces-id og derefter vælge **Transaktioner**.

    Der vises en dialogboks med oplysninger om de transaktioner, der blev oprettet under behandlingen.

> [!NOTE]
> Det er kun leasingaftaler, der har en værdireguleringsdato, der ligger på eller før systemdatoen, der kan reguleres. Systemet ignorerer automatisk alle de leasingaftaler, der har en værdireguleringsdato, der ligger senere end systemdatoen.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842-leasingaftaler – indeksregulering

Hvis du vil have vist effekterne af værdireguleringsprocessen af leasingaftalen til ASC 842, skal du åbne betalingsplanen for en leasingaftale. På siden vises kun de variable betalinger, der er foretaget på eller efter, at værdireguleringsdatoen er ændret pga. indeksværdireguleringen. Afskrivningsplanen for amortisering og afskrivning forbliver uændrede. Når du opretter en faktura, der har en variabel betaling, debiteres den variable betaling på kontoen for variabel betalingsbogføring. Desuden føjes det variable betalingsbeløb til den kreditpost, der bogføres direkte til kreditoren, eller bogføres på kontoen til forfaldsbetaling, afhængigt af opsætningen af leasingprofilen.

Betalingsskemalinjerne på siden oplysninger om leasingaftalen opdateres automatisk med en ny linje, der angiver den nye indekshastighed. Desuden viser en kolonne, om at linjen er oprettet manuelt eller ved hjælp af indeksværdireguleringsprocessen.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16-leasingaftaler – indeksregulering

Hvis du vil have vist effekterne af værdireguleringsprocessen af leasingaftalen til IFRS 16, skal du åbne leasingaftaler for en justeret leasingaftale. Felterne **Leasingbetingelse** og **Aktivets levetid** er blevet opdateret, så de afspejler tidspunktet fra startdatoen eller ændringsdatoen til dato reguleringsdatoen. Desuden er betalingsskemalinjerne opdateret til at afspejle de nye betalinger for leasingaftaler, den nye indekshastighed, og hvordan linjen blev oprettet.

Du kan få vist den nyligt genererede betalingsplan, der starter på værdireguleringsdatoen, og få vist det samlede opdaterede betalingsbeløb. Der er også oprettet en ny plan for betaling af ansvarsforsikring og en plan for aktivafskrivning for at afspejle den justerede betalingsplan.

Kladdeposten har automatisk bogført reguleringskladdeposten på kontoen for ændringen i de leasingbetalinger, der er relateret til indeksværdireguleringen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
