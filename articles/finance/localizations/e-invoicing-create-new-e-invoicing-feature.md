---
title: Oprette en ny funktion til elektronisk fakturering
description: Dette emne forklarer, hvordan du opretter en ny funktion til elektronisk fakturering, når der ikke er indbygget nogen konfigurerbar funktion for dit land eller område.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744929"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Oprette en ny funktion til elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du opretter en ny funktion til elektronisk fakturering, når der ikke er indbygget nogen konfigurerbar funktion for dit land eller område.

Følg nedenstående trin for at oprette en ny funktion til elektronisk fakturering:

1. Opret en ny filformatkonfiguration ved hjælp af den konfiguration af fakturamodellen, der medfølger, og få fordel af den eksisterende fakturatilknytning for den funktion, du vil oprette.
2. Føj konfigurationerne af filformat til konfigurationerne af elektronisk fakturering.
3. Konfigurer funktionen til elektronisk fakturering.
4. Fuldfør den nye funktion til elektronisk fakturering, og publicer den til din organisations globale lager.
5. Installer den nye funktion til elektronisk fakturering i servicemiljøet.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Oprette nye filformatkonfigurationer, der er afledt af den eksisterende fakturamodel

I denne procedure kan du oprette de filformatkonfigurationer, der kræves til den nye funktion til elektronisk fakturering, som du vil oprette. Du kan oprette konfigurationen af det elektroniske fakturafilformat og alle andre filformatkonfigurationer, som din nye funktion til elektronisk fakturering kræver.

Før du starter denne procedure, skal du logge på din RCS-konto (Regulatory Configuration Service).

1. I Microsoft Dynamics 365 Finance skal du i arbejdsområdet **Elektronisk rapportering** vælge **Lagre** for **Microsoft**-konfigurationsudbyderen.
2. Vælg **Global**, vælg **Åbn**, og vælg derefter konfigurationen **Fakturamodel** i venstre rude.

    > [!IMPORTANT]
    > Vælg modelkonfigurationen **Regnskabsdokumenter** for Brasilien.

3. Vælg **Importér** under fanen **Konfigurationer**.
4. Luk siden.
5. Luk siden.
6. Vælg feltet **Rapporteringskonfigurationer**, og vælg derefter den fakturamodel, du har importeret.
7. Vælg **Opret konfiguration**, og vælg derefter **Format baseret på fakturakontekstmodel**.
8. Angiv et navn på og en beskrivelse af formatkonfigurationen.
9. I feltet **Formattype** skal du vælge filtypenavnet.
10. Vælg **Opret konfiguration**, og vælg den formatkonfiguration, du lige har oprettet.
11. Vælg **Designer**, og brug værktøjet Formatdesigner til at konfigurere fillayoutet, så det opfylder filformatspecifikationerne.
12. Luk siden.
13. Under fanen **Versioner** skal du vælge **Skift status** \> **Fuldført**.
14. Vælg **Skift status** \> **Del** for at publicere formatkonfigurationen til det globale lager.

Den nye filformatkonfiguration skal deles med Microsoft-domænet, før konfigurationen kan forbruges af den elektroniske faktureringstjeneste.

1. Vælg den formatkonfiguration, du arbejder på. Status for konfigurationen skal være **Delt**.
2. Under fanen **Versioner** skal du vælge **Adanceret deling** \> **Globalt lager**.
3. I oversigtspanelet **Delt med** skal du vælge **Organisation**.
4. I feltet **Parametre** skal du angive **Microsoft.com** for at dele formatkonfigurationen med Microsoft-domænet.
5. Vælg **OK**.

## <a name="create-the-new-electronic-invoicing-feature"></a>Oprette den nye funktion til elektronisk fakturering

1. I RCS skal du i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** vælge feltet **Elektronisk fakturering**.
2. Vælg **Tilføj**, og vælg derefter **Ny funktion**.
3. Angiv et navn og en beskrivelse for funktionen til elektronisk fakturering.
4. Vælg **Opret funktion**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Tilføje konfigurationer af funktionen til elektronisk fakturering

1. Vælg den funktion til elektronisk fakturering, du arbejder med.
2. Vælg **Tilføj** under fanen **Konfigurationer**.
3. I gitteret **Konfigurationer** skal du navigere til og vælge de filformatkonfigurationer, som din funktion til elektronisk fakturering kræver for at generere den elektroniske fakturafil.
4. Vælg **OK**.

## <a name="add-electronic-invoicing-feature-setups"></a>Tilføje funktionsopsætninger for elektronisk fakturering

1. Under fanen **Opsætninger** skal du vælge **Tilføj** og derefter vælge **Brugerdefineret opsætning**.
2. Angiv et navn til og en beskrivelse af funktionsopsætningen.
3. Vælg **Behandlingspipeline** i feltet **Opsætningstype**.
4. Vælg **Opret**.
5. Vælg den opsætning, du arbejder med, og vælg derefter **Rediger**.
6. Vælg **Ny** under fanen **Behandlingspipeline** for at tilføje en pipeline-handling. Yderligere oplysninger om pipeline finder du i [Handlinger](e-invoicing-configuration-rcs.md#actions).
7. Under fanen **Anvendelighedsregler** skal du vælge **Ny** for at tilføje klausuler for anvendelighedsregler. Du kan finde flere oplysninger om anvendelighedsregler under [Anvendelighedsregler](e-invoicing-configuration-rcs.md#applicability-rules).
8. Vælg **Ny** for at tilføje variabler efter behov under fanen **Variabler**.
9. Vælg **Gem**, og vælg derefter **Valider** for at kontrollere konfigurationskonsistensen.
10. Luk siden.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Installere funktionen til elektronisk fakturering i servicemiljøet

Du kan finde oplysninger om, hvordan du fuldfører denne opgave, under [Implementere funktionen Elektronisk fakturering i servicemiljøet](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Implementere funktionen Elektronisk fakturering i et tilknyttet program

Du kan finde oplysninger om, hvordan du fuldfører denne opgave, under [Konfigurere programopsætning](e-invoicing-get-started.md#configure-the-application-setup) og [Implementere funktionen Elektronisk fakturering i tilknyttet program](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
