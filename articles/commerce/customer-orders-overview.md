---
title: Kundeordrer i Modern POS (MPOS)
description: Dette emne indeholder oplysninger om kundeordrer i Modern POS (MPOS). Kundeordrer kaldes også specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a6fdc7b8d7ad65c9e4bf1d3b932b62918dea6e77
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710253"
---
# <a name="customer-orders-in-modern-pos-mpos"></a>Kundeordrer i Modern POS (MPOS)

[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om kundeordrer i Modern POS (MPOS). Kundeordrer kaldes også specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.

Med et hav af tilgængelige kanaler i handelsverdenen giver mange detailhandlere mulighed for kundeordrer eller specialordrer for at opfylde forskellige produkt- og opfyldelseskrav. Her er nogle typiske scenarier:

- En kunde ønsker, at produkter skal leveres til en bestemt adresse på en bestemt dato.
- En kunde ønsker at afhente varer fra en butik eller et sted, der er forskelligt fra butikken eller det sted, hvor kunden købte varerne.
- En kunde ønsker, at en anden afhenter de produkter, kunden har købt.

Detailhandlere kan også bruge kundeordrer til at minimere manglende salg, som ellers kan skyldes, at en vare midlertidigt ikke kan leveres, da varerne kan leveres eller afhentes på et andet tidspunkt eller sted.

## <a name="set-up-customer-orders"></a>Konfigurere kundeordrer

Her er nogle af de parametre, der kan indstilles på siden **Handelsparametre**, for at definere, hvordan kundeordrer opfyldes:

- **Standard indbetalingsprocent** – Angiv det beløb, som kunden skal betale som et depositum, før en ordre kan bekræftes. Standardindbetalingsbeløbet beregnes som en procentdel af ordreværdien. Afhængigt af rettigheder kan en tilknyttet butik muligvis overstyre beløbet ved hjælp af **Tilsidesæt depositum**.
- **Annulleringsgebyrprocent** – Hvis et gebyr vil blive anvendt, når en kundeordre annulleres, skal du angive beløbet på dette gebyr.
- **Kode for annulleringsgebyr** – Hvis et gebyr vil blive anvendt ved annullering af en kundeordre, afspejles dette gebyr under en gebyrkode på salgsordren. Brug denne parameter til at definere annulleringen af gebyrkoden.
- **Kode for leveringsgebyr** – Detailhandlere kan opkræve et ekstra gebyr for levering af varer til en kunde. Beløbet for dette leveringsgebyr afspejles under en gebyrkode på salgsordren. Brug denne parameter til at knytte leveringsgebyrkoden til forsendelsesgebyrer på kundeordren.
- **Refunder forsendelsesgebyrer** – Angiv, om forsendelsesgebyrer, der er tilknyttet en kundeordre, kan refunderes.
- **Maksimalt beløb uden godkendelse** – Hvis forsendelsesgebyrer kan tilbagebetales, skal du angive det maksimale forsendelsesgebyrbeløb, der kan tilbagebetales på tværs af returordrer. Hvis dette beløb overskrides, kræves ledertilsidesættelse for at fortsætte med refusionen. For at tage højde for følgende scenarier kan en tilbagebetaling af forsendelsesgebyrer overstige det beløb, der oprindeligt blev betalt:

    - Gebyrer anvendes på niveauet for salgsordrehovedet, og når et antal af en produktlinje returneres, kan den maksimale refusion af forsendelsesgebyrer, der er tilladt for produkterne og antallet, ikke bestemmes på måde, der fungerer for alle kunder.
    - Forsendelsesgebyrer påløber for hver leveringsforekomst. Hvis en kunde returnerer varer flere gange, og forhandlerens politik angiver, at forhandleren skal bære omkostningerne ved returforsendelsesgebyrer, bliver returforsendelsesgebyrerne højere end de faktiske forsendelsesgebyrer.
    

## <a name="disable-option-to-pay-later"></a>Deaktivere muligheden for at betale senere

I Commerce version 10.0.12 og nyere kan forhandlerne fjerne muligheden for at betale senere, når der oprettes en kundeordre i POS. Hvis du vil deaktivere indstillingen, skal du åbne **Funktionalitetsprofil** for den kanal, hvor betaling senere ikke er tilladt, og derefter vælge **Rediger**. Under fanen **Generelt** skal du vælge rullelisten for **Kræv betaling for opfyldelse**. Hvis betaling senere ikke skal være tilladt ved POS, skal du vælge **Kort påkrævet** og vælge **Gem**. Kør distributionsplanen **1070** for at synkronisere ændringen til kanalen. 

## <a name="transaction-flow-for-customer-orders"></a>Transaktionsflow for kundeordrer

### <a name="create-a-customer-order-in-modern-pos"></a>Oprette en kundeordre i Modern POS

1. Føj en kunde til transaktionen.
2. Føj produkter til indkøbsvognen.
3. Klik på **Opret kundeordre**, og vælg derefter ordretypen. Ordretypen kan enten være **Kundeordre** eller **Tilbud**.
4. Klik på **Afsendelse valgt** eller **Send alle** for at levere produkterne til en adresse på debitorkontoen, angive den ønskede afsendelsesdato og forsendelsesgebyrer.
5. Klik på **Afhent valgte** eller **Afhent alle** for at vælge produkter, der vil blive afhentet fra det aktuelle lager eller et andet lager på en bestemt dato.
6. Opkræv indbetalingsbeløbet, hvis der kræves et depositum.

### <a name="edit-an-existing-customer-order"></a>Rediger en eksisterende kundeordre

1. Klik på **Find en ordre** på startsiden.
2. Find og vælg den ordre, der skal redigeres. Klik på **Rediger** nederst på siden.

### <a name="pick-up-an-order"></a>Afhente en ordre

1. Klik på **Find en ordre** på startsiden.
2. Vælg den ordre, der skal afhentes. Klik på **Pluk og pakning** nederst på siden.
3. Klik på **Afhent**.

### <a name="cancel-an-order"></a>Annullere en ordre

1. Klik på **Find en ordre** på startsiden.
2. Vælg den ordre, der skal annulleres. Klik på **Annuller** nederst på siden.

### <a name="create-a-return-order"></a>Oprette en returordre

1. Klik på **Find en ordre** på startsiden.
2. Vælg den ordre, der skal returneres, vælg fakturaen for ordren, og vælg derefter produktlinjen for den vare, der skal returneres.
3. Klik på **Returordre** nederst på siden.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynkront transaktionsflow for kundeordrer

Kundeordrer kan oprettes fra POS-klienten i enten synkron eller asynkron tilstand.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktivere kundeordrer, der skal oprettes i asynkron tilstand

1. Klik på **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profil** &gt; **Funktionalitetsprofiler**.
2. I oversigtspanelet **Generelt** skal du vælge **Ja** for **Opret kundeordre i asynkron tilstand**.

Når indstillingen **Opret kundeordre i asynkron tilstand** er indstillet til **Ja**, oprettes kundeordrer altid i asynkron tilstand, også selvom Retail Transaction Service (RTS) er tilgængelig. Hvis du vælger **Nej** for denne indstilling, oprettes kundeordrer altid i synkron tilstand ved hjælp af RTS. Når kundeordrer oprettes i asynkron tilstand, hentes de og indsættes i Commerce af Pull-job (P). De tilsvarende salgsordrer oprettes, når **Synkroniser ordrer** køres enten manuelt eller via en batchproces.

## <a name="additional-resources"></a>Yderligere ressourcer

[Hybride kundeordrer](hybrid-customer-orders.md)
