---
title: Oprette ER-konfigurationer i RCS og overføre dem til det globale lager
description: Dette emne forklarer, hvordan du opretter en ER-konfiguration (Electronic reporting) i Microsoft Regulatory Configuration Services (RCS) og uploader den til det globale lager.
author: JaneA07
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: eb04362d6d7261af56d2940b085fbc8d43c9d662
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965083"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Oprette ER-konfigurationer i RCS (Regulatory Configuration Services) og overføre dem til det globale lager

[!include [banner](../includes/banner.md)]

Du kan bruge Microsoft RCS (Regulatory Configuration Services) til at designe ER-konfigurationer (Electronic reporting) og udgive dem, så de kan bruges i organisationen.

Følgende procedurer forklarer, hvordan en bruger med rollen systemadministrator eller udvikler af elektronisk rapportering kan oprette en afledt version af en ER-konfiguration, der er konfigureret i en RCS-forekomst, og derefter overføre den afledte konfiguration til det globale lager. 

Før du kan fuldføre disse procedurer, skal du fuldføre følgende forudsætninger:

- Få adgang til et RCS-miljø for din organisation.
- Opret en aktiv konfigurationsudbyder, og markér den som aktiv. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Du skal også sikre dig, at der er klargjort et RCS-miljø til din organisation. Hvis du ikke har klargjort en RCS-forekomst til din organisation, kan du gøre dette ved at bruge følgende trin:

1. I en Finans- og driftsapp skal du gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. I **Relaterede links / Eksterne links** skal du vælge **Regulatory services – konfiguration** og derefter følge instruktionerne for **tilmelding** til klargøring af ét.

Hvis der allerede er klargjort et RCS-miljø til din organisation, kan du bruge side-URL-adressen til at få adgang til det og vælge indstillingen til **logon**.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Oprette en afledt version af en konfiguration i RCS

> [!NOTE]
> Hvis det er første gang, du bruger RCS, har du ikke nogen tilgængelig konfiguration, som du kan udlede af. Du skal importere en konfiguration fra det globale lager. Du kan finde flere oplysninger under [Downloade ER-konfigurationer fra det globale lager i konfigurationstjeneste](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Log på** RCS, og vælg arbejdsområdet **Elektronisk rapportering**.
2. Få bekræftet, at du har en aktiv konfigurationsudbyder til din organisation, som er angivet til aktiv (se forudsætninger). 
3. Vælg **Rapporteringskonfigurationer**.
4. Vælg den konfiguration, som du vil aflede en ny version af. Du kan bruge filterfeltet oven over træet til at indsnævre søgningen.
5. Vælg **Opret konfiguration** \> **Afledt fra navn**.
6. Angiv et navn og en beskrivelse, og vælg derefter **Opret konfiguration** for at oprette en ny afledt version med status af "kladde".
7. Vælg den nyafledte konfiguration, og foretag yderligere ændringer af konfigurationsformatet, hvis det er nødvendigt. 
8. Når ændringerne er fuldført, skal du angive **Ændringsstatus** for konfigurationen til **Fuldført**, så den kan publiceres til lageret. Vælg **OK**.

![Ny konfigurationsversion i RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Når konfigurationsstatussen ændres, kan du få vist en meddelelse om valideringsfejl, der er relateret til de tilknyttede programmer. Hvis du vil deaktivere valideringen, skal du vælge bruger parametre i handlingsruden under fanen **Konfigurationer**, vælge **Brugerparametre** og derefter angive indstillingen **Spring validering ved skift og rebasering af konfigurationsstatus** til **Ja**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Uploade en konfiguration til det globale lager

Hvis du vil dele en ny eller afledt konfiguration i din organisation, kan du uploade den til det globale lager med disse trin:

1. Vælg den fuldførte version af konfigurationen, og vælg derefter **Upload til lager**.
2. Vælg indstillingen **Global (Microsoft)**, og vælg derefter **Send**.

    ![Uploade til lagerindstillingerne.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Vælg **Ja** i bekræftelsesmeddelelsesboksen. 
4. Opdater beskrivelsen af versionen efter behov, og vælg derefter **OK**. Du kan også vælge at uploade versionen til et tilknyttet program eller til et GIT-lager.  

Status for konfigurationen opdateres til **Delt**, og konfigurationen overføres til det globale lager. Der oprettes også en kladdeversion af den konfiguration, du har uploadet, som kan bruges, hvis efterfølgende ændringer er nødvendige.

Når konfigurationen er uploadet til det globale lager, kan du arbejde med den der på følgende måder:

- Importere den til Dynamics 365-forekomsten. Du kan finde flere oplysninger under [(ER) Importér konfigurationer fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Del det med en tredjepart eller en ekstern organisation. Se [RCS ER-konfigurationer (Electronic reporting) med eksterne organisationer](rcs-global-repo-share-configuration.md)

    ![Den afledte Intrastat Contoso-konfigurationsversion i det globale lager.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Slette en konfiguration fra det globale lager
Fuldfør følgende trin for at slette en konfiguration, som din organisation har oprettet.

1. I arbejdsområdet **Elektronisk rapportering** skal du bekræfte, at din konfigurationsudbyder er **Aktiv**. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Vælg **lager** på din aktive konfigurationsudbyder.
3. Vælg den globale lagertype **Global**, og vælg **Åbn**.
4. Find den konfiguration, du vil slette, ved hjælp af funktionen **Filter** i oversigtspanelet **Filter**.
5. I oversigtspanelet **Version** skal du vælge den version af konfigurationen, du vil slette, og derefter vælge **Slet**:

    ![Slette en konfiguration fra det globale lager.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Vælg **Ja** i bekræftelsesmeddelelsesboksen.

    ![Slette meddelelse om bekræftelse af konfigurationsversion.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Konfigurationsversionen slettes, og der vises en bekræftelsesmeddelelse. 

> [!NOTE]
> Der kan kun slettes konfigurationer af den konfigurationsudbyder, der har oprettet dem. Hvis konfigurationen er delt med en anden organisation, skal du fjerne delingen af konfigurationen, før du sletter den.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
