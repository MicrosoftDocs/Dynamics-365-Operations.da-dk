---
title: Arbejdslinjedetaljer
description: Dette emne indeholder oplysninger om siden Oplysninger om arbejdslinje, der viser en omfattende, sorterbar og filtrerbar liste over de individuelle arbejdslinjer i systemet.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 07dbfa301e4b242f50a9c2758b11b5ad2c31b261
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998347"
---
# <a name="work-line-details"></a>Arbejdslinjedetaljer

[!include [banner](../includes/banner.md)]

Siden **Oplysninger om arbejdslinje** viser en omfattende, sorterbar og filtrerbar liste over de individuelle arbejdslinjer i systemet. Den indeholder en komplet oversigt over arbejde, der planlægges og udføres på lagerstedet. Du kan nemt skifte mellem at få vist alle arbejdslinjer og kun få vist åbne arbejdslinjer. De detaljer, der er angivet for hver linje, omfatter arbejdsstatus, varenummer, lokation, arbejdsmængde, last-id og forsendelses-id.

## <a name="turn-on-the-work-line-details-feature"></a>Aktivér funktionen Oplysninger om arbejdslinje

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Oplysninger om arbejdslinje*

## <a name="open-and-use-the-work-line-details-page"></a>Åbne og bruge siden Oplysninger om arbejdslinje

Hvis du vil have vist listen over oplysninger om arbejdslinjer, skal du gå til **Lokationsstyring \> Arbejde \> Oplysninger om arbejdslinje**. Herfra kan du udføre følgende opgaver:

- Brug feltet **Filtrer** til at søge efter linjer, der har en bestemt værdi, for alle tilgængelige parametre. (Tilgængelige parametre omfatter mange parametre, der ikke vises som kolonner i gitteret).
- Brug afkrydsningsfeltet **Vis lukket** for at få vist eller skjule lukkede linjer.
- Vælg **Vis dimensioner** for at åbne dialogboksen **Dimensionsvisning**, hvor du kan vælge at få vist eller skjule forskellige dimensionskolonner i gitteret.
- Vælg en kolonneoverskrift for at åbne en menu, hvor du kan vælge at sortere eller filtrere listen efter værdier i den pågældende kolonne.
- Vælg en arbejdslinje, og vælg derefter **Skift lokation** for at åbne en dialogboks, hvor du kan ændre placeringen for den pågældende arbejdslinje. Den lokation, du angiver, tilsidesætter opsætningen af lokationsvejledningen.
- Vælg en arbejdslinje, og vælg derefter **Annuller arbejdslinje** for at åbne en dialogboks, hvor du helt eller delvist kan reducere antallet på den pågældende arbejdslinje.
- Juster antal.
- Få vist posteringerne bag en vilkårlig arbejdslinje.

## <a name="try-out-the-feature"></a>Prøv funktionen

Dette afsnit indeholder en demoversion i tre dele, der viser, hvordan du kan arbejde med oplysninger om arbejdslinjer.

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem denne demo ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge denne demonstration som vejledning, når du arbejder i et produktionssystem. Du skal dog erstatte dine egne værdier, og du mangler muligvis nogle typer påkrævede poster, som standarddemodataene giver.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Kontroller, at scenarieopsætningen indeholder en tilstrækkelig disponibel lagerbeholdning

Hvis du arbejder med **USMF**-demodataene, skal du først sikre dig, at systemet er konfigureret, så der er en tilstrækkelig lagerbeholdning på hver af de relevante pluklokationer. I denne demo er der en forventning om, at du har den følgende tilgængelige lagerbeholdning:

- **Vare M9200:** 45 ea. (eller mere)
- **Vare M9202:** 10 ea. (eller mere)

Udfør følgende trin for at kontrollere, om der er tilstrækkelig lager til rådighed, og om det er nødvendigt at foretage justeringer.

1. Gå til **Lokationsstyring \> Konfiguration \> Lokationsvejledninger**, og bestem, hvilke pluklokationer der bruges til plukning af salgsordre på lagersted 51. (Få flere oplysninger under [Styre lagerarbejde ved hjælp af arbejdsskabeloner og lokalitetsdirektiver](control-warehouse-location-directives.md).)
1. Kontrollér lagerniveauerne på de relevante lokationer.
1. Regulere lagerbeholdning efter behov. Du kan oprette manuelle bevægelser, bruge genopfyldning eller anvende et andet flow til at regulere lagerbeholdningen.

### <a name="part-1-create-picking-work"></a>Del 1: Oprette plukarbejde

Før du begynder at oprette arbejdet, skal du kontrollere, at lagerstedet er konfigureret til at reagere på anmodninger på en bestemt måde.

Benyt følgende fremgangsmåde for at oprette noget plukarbejde.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at åbne dialogboksen **Opret salgsordre**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til _US-001_.
    - I oversigtspanelet **Generelt** skal du indstille **Lagersted** til _51_.

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Din nye indkøbsordre åbnes. Den omfatter en ny, tom række i gitteret **Salgsordrelinjer**. Angiv følgende værdier på denne ordrelinje:

    - **Varenummer:** _M9200_
    - **Antal:** _20_
    - **Enhed:** _Styk_

1. Vælg den nye ordrelinje, og vælg derefter **Reservation** i menuen **Lager** for at åbne siden **Reservation**.
1. På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden. Systemet opretter en forsendelse, føjer den til en ny last og opretter det nødvendige arbejde.
1. Opret endnu en salgsordre for den samme debitorkonto og det lagersted, som du brugte til den første ordre. Føj følgende to ordrelinjer til denne ordre:

    - **Linje 1:** Indstil feltet **Varenummer** til _M9200_, feltet **Antal** til _25_ og feltet **Enhed** til _EA_.
    - **Linje 2:** Indstil feltet **Varenummer** til _M9202_, feltet **Antal** til _10_ og feltet **Enhed** til _EA_.

1. Gentag trin 6 til 8 for at reservere lageret for hver ordrelinje (en ad gangen), og gentag derefter trin 9 for at frigive ordren til lagerstedet.

### <a name="part-2-change-the-location-for-a-work-line"></a>Del 2: Ændre lokationen for en arbejdslinje

1. Gå til **Lagerstedsstyring \> Arbejde \> Oplysninger om arbejdslinje**.
1. Find og vælg en af de arbejdslinjer, du har oprettet for denne demo.
1. Vælg **Skift lokation** for at åbne dialogboksen **Vælg ny lokation**.
1. Gå til dialogboksen **Vælg ny lokation** i feltet **Lokation**, og vælg en ny lokation for arbejdslinjen.
1. Vælg **OK** for at anvende din ændring, og luk dialogboksen.

> [!IMPORTANT]
> Du kan kun sende lokationsændringer, hvis den nye lokation har tilstrækkeligt lager til rådighed (til et pluk), eller hvis dens lokationstype kan valideres (til placer).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>Del 3: Ændre antallet på en arbejdslinje eller annullere en arbejdslinje

1. Gå til **Lagerstedsstyring \> Arbejde \> Oplysninger om arbejdslinje**.
1. Find og vælg en af de arbejdslinjer, du har oprettet for denne demo. Bemærk, at du kun kan annullere eller ændre antal for arbejdslinjer, hvis arbejdstypen er _pluk_.
1. Vælg **Annuller arbejdslinje** for at åbne dialogboksen **Antal, der skal annulleres**.
1. I dialogboksen **Antal, der skal annulleres** skal du ændre værdien i feltet **Antal** for at angive det antal, der skal *trækkes fra* det antal, der aktuelt er angivet for linjen. Feltet **Antal** viser som standard det samlede antal.

    - Hvis du annullerer det samlede antal, ændres værdien for **Arbejdsstatus** til _Annulleret_, men feltet **Arbejdsantal** vil stadig vise den oprindelige værdi.
    - Hvis du blot annuller en del af antallet, opdateres feltet **Arbejdsantal** for at vise den nye værdi, men værdien **Arbejdsstatus** ændres ikke.

1. Vælg **OK** for at anvende din ændring, og luk dialogboksen.

> [!IMPORTANT]
> Hvis du kun vil annullere en del af antallet for en arbejdslinje, skal du også fjerne det forældede antal fra lastlinjen. Hvis ikke, medmindre underlevering er konfigureret korrekt, kan lastlinjen ikke leveres/bekræftes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]