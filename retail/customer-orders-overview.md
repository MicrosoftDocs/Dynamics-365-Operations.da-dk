---
title: Oversigt over ordrer til kunden
description: "Dette emne indeholder oplysninger om kundeordrer i Retail moderne POS (MPOS). Kundeordrer er også kendt som specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og strømme af transaktionen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
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

# <a name="customer-orders-overview"></a>Oversigt over ordrer til kunden

Dette emne indeholder oplysninger om kundeordrer i Retail moderne POS (MPOS). Kundeordrer er også kendt som specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og strømme af transaktionen.

I en omni-kanal retail verden giver mange detailhandlere mulighed for kunden ordrer eller særlige ordrer for at opfylde forskellige krav til produktet og udførelse. Her er nogle typiske scenarier:

-   En kunde ønsker produkter skal leveres til en bestemt adresse på en bestemt dato.
-   En kunde ønsker at afhente varer fra en butik eller en placering, der er forskellig fra butikken eller sted, hvor kunden købte disse produkter.
-   En kunde ønsker en anden at afhente produkter, kunden har købt.

Detailhandlere kan du også bruge kundeordrer for at minimere tabt salg, lager udfald muligvis ellers, da varerne kan leveres eller afhentes på et andet tidspunkt eller sted.

## <a name="set-up-customer-orders"></a>Opsætning af kundeordrer
Her er nogle af de parametre, der kan indstilles på den **Retail parametre** side til at definere, hvordan kundeordrer er opfyldt:

-   **Standard depositum procent** – Angiv det beløb, som kunden skal betale som et depositum, før en ordre kan bekræftes. Standard indbetalingsbeløb beregnes som en procentdel af værdien af ordren. Afhængigt af rettigheder, Tilknyt en butik muligvis overskrive beløbet ved hjælp af **deponere tilsidesættelse af**.
-   **Annullering gebyr procent** – Hvis et gebyr vil blive anvendt, når en kundeordre annulleres, angive mængden af denne afgift.
-   **Annullering tillægskode** – Hvis et gebyr vil blive anvendt ved annullering af en kundeordre, gebyr, afspejles under en tillægskode for salgsordre i Microsoft Dynamics AX. Brug denne parameter til at definere tillægskode annullering.
-   **Forsendelsesgebyrkode** – detailhandlere kan opkræve et ekstra gebyr for levering af varer til en kunde. Mængden, forsendelsesgebyr afspejles under en tillægskode på salgsordren i Dynamics AX. Brug denne parameter til at knytte den forsendelsesgebyrkode til forsendelsesgebyrer på kundens ønske.
-   **Tilbagebetale forsendelsesgebyrer** – Angiv, om forsendelsesgebyrer, der er tilknyttet en kundeordre refunderes.
-   **Maksimumbeløb uden godkendelse** – Hvis forsendelsesgebyrer, der tilbagebetales, angiver den maksimale mængde levering gebyr restitutioner på tværs af returordrer. Hvis dette beløb overskrides, der manager tilsidesættelse kræves for at fortsætte med restitution. For at tage højde for følgende scenarier ved kan tilbagebetaling af forsendelsesomkostninger overstige det beløb, der oprindeligt er betalt:
    -   Gebyrer anvendes på niveauet for salgsordrehovedet, og når et antal af en produktserie returneres, den maksimale refusion af forsendelsesgebyrer, der er tilladt for produkterne og mængden, der ikke kan bestemmes på måde, der fungerer for alle detailkunder.
    -   Forsendelsesgebyrer, der påløber for hver forekomst af levering. Hvis en kunde returnerer varer flere gange, og den forhandler politik angiver, at forhandleren skal bære omkostningerne ved returnering forsendelsesgebyrer, bliver returnering forsendelsesgebyrerne til mere end de faktiske forsendelsesgebyrer.

## <a name="transaction-flow-for-customer-orders"></a>Transaktionsflow for kundeordrer
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Opret en kundeordre i moderne detail-POS

1.  Føj en kunde til transaktionen.
2.  Føje varer til indkøbsvognen.
3.  Klik på **Opret kundeordre**, og vælg derefter typen. Ordretypen kan enten være **kundeordre** eller **tilbud**.
4.  Klik på **skib, der er valgt** eller **leverer alle** for at levere produkter til en adresse på debitorkontoen, angive den ønskede afsendelsesdato og forsendelsesgebyrer.
5.  Klik på **afhentning af valgt** eller **afhentning af alle** til at vælge produkter, der vil blive plukket fra det aktuelle lager eller en anden butik, på en bestemt dato.
6.  Samle det indbetalingsbeløb, hvis der kræves et depositum.

### <a name="edit-an-existing-customer-order"></a>Rediger en eksisterende kundeordre

1.  Klik på hjemmesiden, **finde en ordre**.
2.  Find og Vælg ordren til at redigere. I bunden af siden, skal du klikke på den **Rediger**.

### <a name="pick-up-an-order"></a>Vælge en ordre

1.  Klik på hjemmesiden, **finde en ordre**.
2.  Du kan vælge at afhente ordren. I bunden af siden, skal du klikke på **pluk- og pakning af**.
3.  Klik på **afhente**.

### <a name="cancel-an-order"></a>Annullere en ordre

1.  Klik på hjemmesiden, **finde en ordre**.
2.  Vælg at annullere ordren. I bunden af siden, skal du klikke på **annullere**.

#### <a name="create-a-return-order"></a>Oprette en returordre

1.  Klik på hjemmesiden, **finde en ordre**.
2.  Vælg ordren til at vende tilbage, vælge fakturaen for ordren, og vælg derefter produktlinje at returnere varen.
3.  I bunden af siden, skal du klikke på den **returordre**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynkron transaktionsflow for kundeordrer
Kundeordrer kan oprettes fra sted, hvor salg (POS) klient i enten synkrone eller asynkrone tilstand.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktivere kundeordrer skal oprettes i asynkron tilstand

1.  I Dynamics AX, skal du klikke på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**POS profil**&gt;**funktionalitetsprofiler**.
2.  På den **generelle** Angiv i oversigtspanelet på **Opret kundeordre i asynkron tilstand** at **Ja**.

Når den **Opret kundeordre i asynkron tilstand** indstilling er angivet til **Ja**, oprettes der altid kundeordrer i asynkron tilstand, selv om Retail Transaction Service (RTS) er tilgængelig. Hvis du angiver denne indstilling til **ingen**, kundeordrer oprettes altid i synkron tilstand ved hjælp af RTS. Når kunden bestiller oprettes i asynkron tilstand, er de trukket og indsat i Dynamics AX, ved at trække (P) job. De tilsvarende salgsordrer oprettes i Dynamics AX når **synkronisere ordrer** køres enten manuelt eller via en batchproces.

<a name="see-also"></a>Se også
--------

[Hybrid kundeordrer](hybrid-customer-orders.md)


