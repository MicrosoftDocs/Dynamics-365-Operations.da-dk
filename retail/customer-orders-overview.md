---
title: Oversigt over kundeordrer
description: "Dette emne indeholder oplysninger om kundeordrer i Retail Modern POS (MPOS). Kundeordrer kaldes også specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Oversigt over kundeordrer

[!include[banner](includes/banner.md)]


Dette emne indeholder oplysninger om kundeordrer i Retail Modern POS (MPOS). Kundeordrer kaldes også specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.

Med et hav af tilgængelige kanaler i detailverdenen giver mange detailhandlere mulighed for kundeordrer eller specialordrer for at opfylde forskellige produkt- og opfyldelseskrav. Her er nogle typiske scenarier:

-   En kunde ønsker, at produkter skal leveres til en bestemt adresse på en bestemt dato.
-   En kunde ønsker at afhente varer fra en butik eller et sted, der er forskelligt fra butikken eller det sted, hvor kunden købte varerne.
-   En kunde ønsker, at en anden afhenter de produkter, kunden har købt.

Detailhandlere kan også bruge kundeordrer til at minimere manglende salg, som ellers kan skyldes, at en vare midlertidigt ikke kan leveres, da varerne kan leveres eller afhentes på et andet tidspunkt eller sted.

## <a name="set-up-customer-orders"></a>Konfigurere kundeordrer
Her er nogle af de parametre, der kan indstilles på siden **Detailparametre**, for at definere, hvordan kundeordrer opfyldes:

-   **Standard indbetalingsprocent** – Angiv det beløb, som kunden skal betale som et depositum, før en ordre kan bekræftes. Standardindbetalingsbeløbet beregnes som en procentdel af ordreværdien. Afhængigt af rettigheder kan en tilknyttet butik muligvis overstyre beløbet ved hjælp af **Tilsidesæt depositum**.
-   **Annulleringsgebyrprocent** – Hvis et gebyr vil blive anvendt, når en kundeordre annulleres, skal du angive beløbet på dette gebyr.
-   **Kode for annulleringsgebyr** – Hvis et gebyr vil blive anvendt ved annullering af en kundeordre, afspejles dette gebyr under en gebyrkode på salgsordren i Microsoft Dynamics AX. Brug denne parameter til at definere annulleringen af gebyrkoden.
-   **Kode for leveringsgebyr** – Detailhandlere kan opkræve et ekstra gebyr for levering af varer til en kunde. Beløbet for dette leveringsgebyr afspejles under en gebyrkode på salgsordren i Dynamics AX. Brug denne parameter til at knytte leveringsgebyrkoden til forsendelsesgebyrer på kundeordren.
-   **Refunder forsendelsesgebyrer** – Angiv, om forsendelsesgebyrer, der er tilknyttet en kundeordre, kan refunderes.
-   **Maksimalt beløb uden godkendelse** – Hvis forsendelsesgebyrer kan tilbagebetales, skal du angive det maksimale forsendelsesgebyrbeløb, der kan tilbagebetales på tværs af returordrer. Hvis dette beløb overskrides, kræves ledertilsidesættelse for at fortsætte med refusionen. For at tage højde for følgende scenarier kan en tilbagebetaling af forsendelsesgebyrer overstige det beløb, der oprindeligt blev betalt:
    -   Gebyrer anvendes på niveauet for salgsordrehovedet, og når et antal af en produktlinje returneres, kan den maksimale refusion af forsendelsesgebyrer, der er tilladt for produkterne og antallet, ikke bestemmes på måde, der fungerer for alle detailkunder.
    -   Forsendelsesgebyrer påløber for hver leveringsforekomst. Hvis en kunde returnerer varer flere gange, og forhandlerens politik angiver, at forhandleren skal bære omkostningerne ved returforsendelsesgebyrer, bliver returforsendelsesgebyrerne højere end de faktiske forsendelsesgebyrer.

## <a name="transaction-flow-for-customer-orders"></a>Transaktionsflow for kundeordrer
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Oprette en kundeordre i Retail Modern POS

1.  Føj en kunde til transaktionen.
2.  Føj produkter til indkøbsvognen.
3.  Klik på **Opret kundeordre**, og vælg derefter ordretypen. Ordretypen kan enten være **Kundeordre** eller **Tilbud**.
4.  Klik på **Afsendelse valgt** eller **Send alle** for at levere produkterne til en adresse på debitorkontoen, angive den ønskede afsendelsesdato og forsendelsesgebyrer.
5.  Klik på **Afhent valgte** eller **Afhent alle** for at vælge produkter, der vil blive afhentet fra det aktuelle lager eller et andet lager på en bestemt dato.
6.  Opkræv indbetalingsbeløbet, hvis der kræves et depositum.

### <a name="edit-an-existing-customer-order"></a>Rediger en eksisterende kundeordre

1.  Klik på **Find en ordre** på startsiden.
2.  Find og vælg den ordre, der skal redigeres. Klik på **Rediger** nederst på siden.

### <a name="pick-up-an-order"></a>Afhente en ordre

1.  Klik på **Find en ordre** på startsiden.
2.  Vælg den ordre, der skal afhentes. Klik på **Pluk og pakning** nederst på siden.
3.  Klik på **Afhent**.

### <a name="cancel-an-order"></a>Annullere en ordre

1.  Klik på **Find en ordre** på startsiden.
2.  Vælg den ordre, der skal annulleres. Klik på **Annuller** nederst på siden.

#### <a name="create-a-return-order"></a>Oprette en returordre

1.  Klik på **Find en ordre** på startsiden.
2.  Vælg den ordre, der skal returneres, vælg fakturaen for ordren, og vælg derefter produktlinjen for den vare, der skal returneres.
3.  Klik på **Returordre** nederst på siden.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynkront transaktionsflow for kundeordrer
Kundeordrer kan oprettes fra POS-klienten i enten synkron eller asynkron tilstand.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktivere kundeordrer, der skal oprettes i asynkron tilstand

1.  In Dynamics AX skal du klikke på **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Funktionalitetsprofiler**.
2.  I oversigtspanelet **Generelt** skal du vælge **Ja** for **Opret kundeordre i asynkron tilstand**.

Når indstillingen **Opret kundeordre i asynkron tilstand** er indstillet til **Ja**, oprettes kundeordrer altid i asynkron tilstand, også selvom Retail Transaction Service (RTS) er tilgængelig. Hvis du vælger **Nej** for denne indstilling, oprettes kundeordrer altid i synkron tilstand ved hjælp af RTS. Når kundeordrer oprettes i asynkron tilstand, hentes de og indsættes i Dynamics AX af Pull-job (P). De tilsvarende salgsordrer oprettes i Dynamics AX, når **Synkroniser ordrer** køres enten manuelt eller via en batchproces.

<a name="see-also"></a>Se også
--------

[Hybride kundeordrer](hybrid-customer-orders.md)




