---
title: ER-overflytningsoprydning
description: Dette emne forklarer, hvordan du kan bruge funktionen til ER-overflytningsoprydning til at løse problemer med ER-skabeloner.
author: NickSelin
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8b6e81e47cd781bbe856676b1cecb50b8ee1adfc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351043"
---
# <a name="er-migration-cleanup"></a>ER-overflytningsoprydning 

[!include[banner](../includes/banner.md)]

Når du administrerer dine Finance-forekomster, kan du vælge at flytte din aktuelle forekomst til en anden lokation. Du kan f.eks. flytte produktionsforekomsten til et nyt sandkassemiljø. Hvis du har konfigureret den elektroniske rapporteringsstruktur (ER) til at gemme skabeloner i Microsoft Azure Blob-lageret, henviser **DocuValue**-tabellen i det nye sandkassemiljø til forekomsten af blob-lager i produktionsmiljøet. Men der er ikke adgang til denne forekomst fra sandkassemiljøet, fordi overflytningsprocessen ikke understøtter overflytning af artefakter i blob-lageret. Det forventes derimod i det nye sandkassemiljø, at du henviser til forekomsten af blob-lageret i det sandkassemiljø, der endnu ikke modtager ER-skabelonerne.

Hvis du forsøger at køre et ER-format, der bruger en skabelon til at generere forretningsdokumenter, indtræffer der en undtagelse, og du får besked om den manglende skabelon. Du bliver også guidet til at bruge indstillingen til ER-overflytningoprydning til at slette og derefter importere den ER-formatkonfiguration, der indeholder skabelonen, igen.

[![Køre et ER-format.](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Du modtager en lignende fejl, hvis du navigerer til siden **Konfigurationer** (**Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**) og forsøger at slette en ER- formatkonfiguration, der bruger en skabelon, i konfigurationstræet.

[![Slette et ER-format.](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Gennemfør følgende trin for at løse problemer med ER-skabeloner, som du ikke kan få adgang til.

1.  Gå til siden **Organisationsadministration** \> **Periodisk** \> **Overflytningsoprydning**.
2.  Vælg en ER-formatkonfiguration, der ikke kan køres eller slettes.
3.  Vælg **Slet**.
4.  Bekræft sletningen af den valgte ER-formatkonfiguration.
5.  [Importér](download-electronic-reporting-configuration-lcs.md) den slettede ER-formatkonfiguration til den aktuelle overflytningsoprydning.

## <a name="applicability"></a>Anvendelighed

> (Vigtigt) Indstillingen **Overflytningsoprydning** er kun målrettet for ER-formatkonfigurationer, der indeholder ikke-tilgængelige ER-skabeloner. Når du sletter en ER-formatkonfiguration via indstillingen **Overflytningsoprydning**, sletter ER de skabeloner, der er relateret til konfigurationsartefakterne i den eneste programdatabase. Eksistensen af de relevante fysiske filer i blob-lageret kan ikke valideres. Det antages i stedet, at der ikke er nogen. Brug derfor ikke indstillingen **Overflytningsoprydning** som et alternativ til indstillingen for ER-konfigurationssletning på siden **Konfigurationer**. Brug kun indstillingen **Overflytningsoprydning**, når indstillingen for ER-konfigurationssletning på siden **Konfigurationer** mislykkedes.
>
> Hvis du bruger indstillingen **Overflytningsoprydning** til at slette en ER-formatkonfiguration, når skabelonen, der refereres til, er tilgængelig i blob-lageret, sletter du kun relaterede konfigurationsartefakter i programdatabasen. Den fysiske fil i skabelonen i blob-lageret slettes ikke. Filoverskrivning i blob-lageret er ikke længere tilladt. Du kan finde flere oplysninger i [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Derudover kan du ikke længere genimportere de konfigurationer, der er slettet, ved hjælp af overflytningsoprydningen i dette miljø. Du kan dette problem ved at finde den tilsvarende fil i blob-lageret og slette den manuelt.

[![Importere et ER-format.](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Der kan opstå et lignende problem, hvis du overflytter din programforekomst til en anden placering, der er brugt som overflytningsdestination mere end én gang, og hvor blob-lageret allerede indeholder ER-skabelonfiler.

Da du kan have flere ER-formatkonfigurationer, kan denne proces være tidskrævende. Det anbefales derfor at bruge funktionen [Sikkerhedskopilager til ER-skabeloner](er-backup-storage-templates.md) for automatisk at gendanne skabeloner med brudte referencer.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]