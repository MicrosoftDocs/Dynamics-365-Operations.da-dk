---
title: Oprette ER-konfigurationer i RCS og overføre dem til det globale lager
description: Dette emne forklarer, hvordan du opretter en ER-konfiguration (Electronic reporting) i Microsoft Regulatory Configuration Services (RCS) og uploader den til det globale lager.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441619"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Oprette ER-konfigurationer i RCS (Regulatory Configuration Services) og overføre dem til det globale lager

[!include [banner](../includes/banner.md)]

Du kan bruge Microsoft RCS (Regulatory Configuration Services) til at designe ER-konfigurationer (Electronic reporting) og udgive dem, så de kan bruges i organisationen.

Følgende procedurer forklarer, hvordan en bruger med rollen systemadministrator eller udvikler af elektronisk rapportering kan oprette en afledt version af en ER-konfiguration, der er konfigureret i en RCS-forekomst, og derefter overføre den afledte konfiguration til det globale lager. 

Før du kan fuldføre disse procedurer, skal du fuldføre følgende forudsætninger:

- Gå til en forekomst.
- Oprette en aktiv konfigurationsudbyder. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Du skal også sikre dig, at der er klargjort et RCS-miljø til dit firma.

1. I en Finance and Operations-app skal du gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Hvis der ikke er klargjort noget RCS-miljø til dit firma, skal du vælge **Regulatory services – ekstern konfiguration** og derefter følge instruktionerne for at klargøre et.

Hvis der allerede er klargjort et RCS-miljø til dit firma, kan du bruge side-URL-adressen til at få adgang til det ved at vælge indstillingen til logon.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Oprette en afledt version af en konfiguration i RCS

1. I arbejdsområdet **Elektronisk rapportering** skal du kontrollere, at du har en aktiv konfigurationsprovider til din organisation. 
2. Vælg **Rapporteringskonfigurationer**.
3. Vælg den konfiguration, som du vil aflede en ny version af. Du kan bruge filterfeltet oven over træet til at indsnævre søgningen.
4. Vælg **Opret konfiguration** \> **Afledt fra navn**.
5. Angiv et navn og en beskrivelse, og vælg derefter **Opret konfiguration** for at oprette en ny afledt version.
6. Vælg den netop afledte konfiguration, tilføj en beskrivelse af versionen, og vælg derefter **OK**. Statussen for konfigurationen er ændret til **Fuldført**.

![Ny konfigurationsversion i RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Når konfigurationsstatussen ændres, kan du få vist en meddelelse om valideringsfejl, der er relateret til de tilknyttede programmer. Hvis du vil deaktivere valideringen, skal du vælge bruger parametre i handlingsruden under fanen **Konfigurationer**, vælge **Brugerparametre** og derefter angive indstillingen **Spring validering ved skift og rebasering af konfigurationsstatus** til **Ja**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Uploade en konfiguration til det globale lager

Hvis du vil dele en ny eller afledt konfiguration i din organisation, kan du uploade den til det globale lager.

1. Vælg den fuldførte version af konfigurationen, og vælg derefter **Upload til lager**.
2. Vælg indstillingen **Global (Microsoft)**, og vælg derefter **Send**.

    ![Uploade til lagerindstillingerne](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Vælg **Ja** i bekræftelsesmeddelelsesboksen. 
4. Opdater beskrivelsen af versionen efter behov, og vælg derefter **OK**. 

Status for konfigurationen opdateres til **Del**, og konfigurationen overføres til det globale lager. Derfra kan du arbejd med den på følgende måder:

- Importere den til Dynamics 365-forekomsten. Du kan finde flere oplysninger under [(ER) Importér konfigurationer fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Del det med en tredjepart eller en ekstern organisation. Se [RCS ER-konfigurationer (Electronic reporting) med eksterne organisationer](rcs-global-repo-share-configuration.md)

    ![Den afledte Intrastat Contoso-konfigurationsversion i det globale lager](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Slette en konfiguration fra det globale lager
Fuldfør følgende trin for at slette en konfiguration, som din organisation har oprettet.

1. I arbejdsområdet **Elektronisk rapportering** skal du bekræfte, at din konfigurationsudbyder er **Aktiv**. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Vælg **lager** på din aktive konfigurationsudbyder.
3. Vælg den globale lagertype **Global**, og vælg **Åbn**.
4. Find den konfiguration, du vil slette, ved hjælp af funktionen **Filter** i oversigtspanelet **Filter**.
5. I oversigtspanelet **Version** skal du vælge den version af konfigurationen, du vil slette, og derefter vælge **Slet**:

    ![Slette en konfiguration fra det globale lager](media/RCS_Delete_from_GlobalRepo.JPG)

6. Vælg **Ja** i bekræftelsesmeddelelsesboksen.

    ![Slette meddelelse om bekræftelse af konfigurationsversion](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Konfigurationsversionen slettes, og der vises en bekræftelsesmeddelelse. 

> [!NOTE]
> Der kan kun slettes konfigurationer af den konfigurationsudbyder, der har oprettet dem. Hvis konfigurationen er delt med en anden organisation, skal du fjerne delingen af konfigurationen, før du sletter den.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]