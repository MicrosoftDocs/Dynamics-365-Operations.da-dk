---
title: Produktlivscyklustilstande og transaktioner
description: I dette emne forklares det, hvordan du kan styre, hvilke transaktioner der er tilladt for hver enkelt livscyklustilstand, når et teknisk produkt går gennem dets livscyklus.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 69ee39479424c1b629388c18e8bfefd023036d22
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425080"
---
# <a name="product-lifecycle-states-and-transactions"></a>Produktlivscyklustilstande og transaktioner

[!include [banner](../includes/banner.md)]

Når et teknisk produkt går gennem dets livscyklus, er det vigtigt, at du kan styre, hvilke transaktioner der er tilladt for hver enkelt livscyklustilstand. Produkter, der endnu ikke er i en moden tilstand, bør f.eks. ikke sættes på en salgsordre. Hvis et produkt når frem til afslutning af dets levetid, kan det også være en god ide at kontrollere det pågældende produkts indstrømning.

I forbindelse med et teknisk produkt er ændringer af livscyklustilstanden forbundet med produktets tekniske versioner. Produktets livscyklustilstand kan derfor også være forbundet med dets tekniske version. Når produktets livscyklustilstand er tilknyttet en teknisk version, kan du bruge livscyklustilstanden til at styre, hvilke transaktioner der er tilladt for den tekniske version.

## <a name="create-and-manage-product-lifecycle-states"></a>Oprette og styre produkters livscyklustilstande

Hvis du vil arbejde med produkters livscyklustilstande, skal du gå til **Styring af tekniske ændringer \> Konfiguration \> Tilstand for produktlivscyklus**. Udfør derefter ét af følgende trin.

- Hvis du vil oprette en ny livscyklustilstand, skal du vælge **Ny** i handlingsruden og derefter angive felterne som beskrevet i følgende underafsnit.
- Hvis du vil redigere en eksisterende livscyklustilstand, skal du vælge den i listeruden, vælge **Rediger** i handlingsruden og derefter angive felterne som beskrevet i følgende underafsnit.
- Hvis du vil slette en eksisterende livscyklustilstand, skal du vælge den i listeruden og derefter vælge **Slet** i handlingsruden.

> [!NOTE]
> Tekniske produkter bruger samme produktlivscyklustilstande som standardprodukter (ikke-tekniske). Du kan også åbne siden **Tilstand for produktlivscyklus**, der er beskrevet i dette emne, ved at gå til **Administration af produktoplysninger \> Konfiguration \> Tilstand for produktlivscyklus**. Du kan finde flere oplysninger om produkters livscyklustilstande for både tekniske produkter og standardprodukter under [Oversigt for produkters livscyklustilstande](../pim/product-lifecycle.md).

### <a name="header"></a>Overskrift

Angiv følgende felter i overskriften på et produkts livscyklustilstand.

| Felt | Beskrivelse |
|---|---|
| Status | Angiv et navn til produktets livscyklustilstand. |
| Beskrivelse | Angiv en beskrivelse af produktets livscyklustilstand. |

### <a name="general-fasttab"></a>Oversigtspanelet Generelt

I oversigtspanelet **Generelt** skal du indstille følgende felter.

| Felt | Beskrivelse |
|---|---|
| Standard, når det frigives til en juridisk enhed | For standardprodukter skal du angive denne indstilling til *Ja*, hvis denne livscyklustilstand skal anvendes på alle produkter, når de frigives første gang. Angiv indstillingen til *Nej*, hvis livscyklustilstanden skal anvendes manuelt senere.<p>Denne indstilling kan ikke anvendes til tekniske produkter. Livscyklustilstanden for en teknisk produktversion, efter at den er oprettet i det tekniske firma, er angivet i den tekniske ændringskategori. Når produktet frigives til et driftsselskab, kopieres produktets livscyklustilstand. Det vil med andre ord sige, at når et teknisk produkt frigives til et driftsselskab, har det samme livscyklustilstand som den, det havde i den tekniske virksomhed. Livscyklustilstanden kan overskrives i driftsselskabet.</p> |
| Er aktiv for planlægning | Angiv denne indstilling til *Ja* for at medtage produkter, der findes i denne livscyklustilstand, i beregninger på styklisteniveauerne for varedisponering. Angiv den til *Nej* for at udelukke produkter, der er i denne livscyklustilstand, fra beregningerne. |

### <a name="enabled-business-processes-fasttab"></a>Oversigtspanelet Aktiverede forretningsprocesser

Brug oversigtspanelet **Aktiverede forretningsprocesser** til at styre, hvilke af de tilgængelige forretningsprocesser der kan bruges sammen med produkter i den nuværende livscyklustilstand. De processer, der er angivet i dette oversigtspanel, findes automatisk på følgende måde:

- Første gang du gemmer en ny livscyklustilstand, indlæser siden de forretningsprocesser, der aktuelt er tilgængelige.
- Hvis du føjer nye forretningsprocesser til systemet, kan du opdatere listen i oversigtspanelet **Aktiverede forretningsprocesser** for en eksisterende livscyklustilstand ved at vælge **Søg efter opdateringer** i handlingsruden.

Følgende felter er tilgængelige for hver proces, der vises i oversigtspanelet **Aktiverede forretningsprocesser**.

| Felt | Beskrivelse |
|---|---|
| Behandling | Dette skrivebeskyttede felt viser navnet på en eksisterende forretningsproces. |
| Procesområde | Dette skrivebeskyttede felt viser navnet på et eksisterende procesområde. |
| Police | Vælg en af følgende værdier for at kontrollere, om og hvordan den aktuelle proces tillades for produkter, der er i denne livscyklustilstand:<ul><li>**Aktiveret** – Forretningsprocessen er tilladt.</li><li>**Blokeret** – Processen er ikke tilladt. Hvis en bruger forsøger at bruge processen på et produkt, der er i denne livscyklustilstand, vil systemet blokere forsøget og vise en fejl i stedet. Du kan f.eks. blokere for, at produkter bliver købt efter afslutning af deres levetid.</li><li>**Aktiveret med advarsel** – Processen er tilladt, men der vises en advarsel. Du kan f.eks. vælge, at et prototypeprodukt skal lægges på en produktionsordre, der er oprettet af afdelingen for forskning og udvikling. Andre afdelinger skal dog være opmærksomme på, at de ikke bør producere produktet endnu.</li></ul> |

Hvis du tilføjer flere regler for livscyklustilstand som en tilpasning, kan du få vist disse regler i brugergrænsefladen ved at vælge **Opdater processer** i den øverste rude. Knappen **Opdater processer** er kun tilgængelig for administratorer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]