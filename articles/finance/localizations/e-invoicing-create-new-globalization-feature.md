---
title: Oprette en globaliseringsfunktion
description: Dette emne forklarer, hvordan du kan oprette en globaliseringsfunktion.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 197a5b983b307758425b1acc1f354d0a8bfbf8a1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371581"
---
# <a name="create-a-globalization-feature"></a>Oprette en globaliseringsfunktion

[!include [banner](../includes/banner.md)]

Du kan oprette en funktion til elektronisk faktura fra bunden, eller du kan basere den på en eksisterende funktion. Når du opretter en funktion fra bunden, skal du manuelt tilføje ER-konfigurationer og andre komponenter som f.eks. funktionskonfigurationer og detaljer om programopsætning. Når du opretter en funktion, der er baseret på en eksisterende funktion, arver den nye funktion alle basisfunktionens konfigurationer og parametre. Du kan gennemse, hvad der er kopieret fra basisfunktionen til den nye funktion.

## <a name="create-a-feature-from-scratch"></a>Oprette en funktion fra bunden

Dette afsnit forklarer, hvordan du opretter en funktion til elektronisk fakturering, når der ikke er indbygget en tilgængelig globaliseringsfunktion i det globale lager til dine forretningsscenarier.

Følg nedenstående trin for at oprette en funktion til elektronisk fakturering.

1. Logge på din RCS-konto (Regulatory Configuration Service).
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.
3. Vælg **Tilføj**, og derefter skal du i rulledialogboksen vælge indstillingen **Ny funktion**.
4. Angiv et navn og en beskrivelse for funktionen til elektronisk fakturering.
5. Vælg **Opret funktion**. Den første version af den nye funktion vises i højre side af siden og har statussen **Kladde**.

    Derefter skal du tilføje ER-konfigurationer og funktionsopsætninger. Før du tilføjer nye eller eksisterende ER-formatkonfigurationer, skal du kontrollere, at de findes i dit lokale RCS-lager.

6. Vælg den funktion til elektronisk fakturering, du arbejder med.
7. Vælg **Tilføj** under fanen **Konfigurationer**.
8. I gitteret **Konfigurationer** skal du søge efter og vælge de formatkonfigurationer, der kræves til behandlingspipelinen (f.eks. for at generere elektroniske fakturafiler eller behandle svar fra eksterne webtjenester).
9. Vælg **OK**. Du kan nu bruge konfigurationerne i behandlingspipelinens handlinger. Du kan finde flere oplysninger i [Arbejde med konfigurationer](e-invoicing-work-configurations.md).
10. Hvis du vil tilføje en funktion til elektronisk fakturering, skal du oprette den under fanen **Konfigurationer** på siden **Ny funktion**. Du kan finde flere oplysninger i [Arbejde med funktionsopsætninger](e-invoicing-feature-setup.md).
11. Fuldfør opsætningen, og udrul funktionen til elektronisk fakturering i servicemiljøet. Du kan finde flere oplysninger i [Afslutte, publicere og udrulle en globaliseringsfunktion](e-invoicing-complete-publish-deploy-globalization-feature).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Oprette filformatkonfigurationer, der er afledt af den eksisterende fakturamodel

Du kan springe dette afsnit over, hvis du ikke behøver at oprette ER-konfigurationer, men kan genbruge eksisterende versioner som basis.

I denne procedure kan du se, hvordan du opretter de filformatkonfigurationer, der kræves til den nye funktion til elektronisk fakturering, som du vil oprette. Opret konfigurationen af det elektroniske fakturafilformat og alle andre filformatkonfigurationer, som din nye funktion til elektronisk fakturering kræver.

1. Log på din RCS-konto.
2. I arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.
3. Vælg **Fakturamodel**, eller vælg **Regnskabsmodel** for brasilianske scenarier.
4. Vælg **Opret konfiguration**, og vælg **Format, der er baseret på datamodellen Faktura** i rulledialogboksen.
5. Angiv et navn på og en beskrivelse af formatkonfigurationen.
6. I feltet **Formattype** skal du vælge filtypenavnet.
7. Vælg den rodstruktur, du vil knytte formatet til, i feltet **Datamodeldefinition**. F.eks. bruges **InvoiceCustomer** til formater for debitorfakturaer.
8. Vælg **Opret konfiguration**.
9. Vælg den nye formatkonfiguration.
10. Vælg **Designer**, og brug værktøjet Formatdesigner til at konfigurere fillayoutet, så det opfylder filformatspecifikationerne.
11. Luk siden.
12. Under fanen **Versioner** skal du vælge **Skift status** \> **Fuldført**.
13. Vælg **Skift status** \> **Del** for at publicere formatkonfigurationen til det globale lager.

De nye filformatkonfigurationer skal deles med Microsoft-domænet, før de kan forbruges af den elektroniske faktureringstjeneste.

1. Vælg den formatkonfiguration, du arbejder på. Status for konfigurationen skal være **Delt**.
2. Under fanen **Versioner** skal du vælge **Adanceret deling** \> **Globalt lager**.
3. I oversigtspanelet **Delt med** skal du vælge **Organisation**.
4. I feltet **Parametre** skal du angive **microsoft.com** for at dele formatkonfigurationen med Microsoft-domænet.
5. Vælg **OK**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Oprette en funktion, der er baseret på en eksisterende funktion

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.
3. Sørg for, at din aktive konfigurationsudbyder er valgt i feltet **Konfigurationsudbyder**. På denne måde vises den nye funktion til elektronisk fakturering på listen, når den er oprettet. Hvis den aktive konfigurationsudbyder ikke er valgt, filtreres den nye funktion ud af listen.
4. Vælg **Tilføj**, og derefter skal du i rulledialogboksen vælge indstillingen **Baseret på eksisterende version**.
5. Angiv et navn til og en beskrivelse af funktionen.
6. Vælg basisversionen af funktionen i feltet **Basisfunktion**.
7. Vælg **Opret funktion**. Funktionen oprettes og har statussen **Kladde**.
8. Gennemse funktionskomponenterne for at finde ud af, om der kræves opdateringer:

    - Gennemse konfigurationerne, hvis du skal tilpasse ER-formaterne og deres binding med formattilknytninger til funktionsversionen.
    - Gennemse opsætningen, hvis du skal tilpasse fanen **Handlinger**, fanen **Anvendelighedsregler** eller fanen **Variabler** for funktionsversionen.

9. Fuldfør opsætningen, og udrul funktionen til elektronisk fakturering i servicemiljøet. Du kan finde flere oplysninger i [Afslutte, publicere og udrulle en globaliseringsfunktion](e-invoicing-complete-publish-deploy-globalization-feature).
