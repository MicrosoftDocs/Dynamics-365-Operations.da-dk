---
title: Kreditoreksempelchecks til elektronisk rapportering
description: Dette emne indeholder generelle oplysninger om brug af eksempelcheckformater i elektronisk rapportering.
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ae42c9012a430aeeed6adb78b33776c727e4a3f8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551143"
---
[!include [banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-vendor-checks"></a>Kreditoreksempelchecks til elektronisk rapportering

Du kan bruge elektronisk rapportering (ER) til at formatere kreditorchecks. Der findes mange checkformater, som er specifikke for bank- og checkudbyderen, på markedet. Der er medtaget eksempelcheckformater i betalingscheckmodellen i værktøjslageret i elektronisk rapportering. Disse eksempelchecks kaldes **Check i midten (USA)** og **Check på øverste talon nedenfor (USA)**.

## <a name="what-check-formats-are-currently-supported"></a>Hvilke checkformater understøttes i øjeblikket?

Du bør altid gå til biblioteket med delte aktiver i Microsoft Dynamics Lifecycle Services (LCS) og få vist den aktuelle liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**. Næste afsnit, "Hvad skal jeg bruge for at komme i gang?", indeholder et link til et emne, der forklarer, hvordan du opretter et LCS-lager, så du kan se tilgængelige konfigurationer og importere valgte konfigurationer.

Microsoft Dynamics 365 Finance omfatter også et eksempelformat, hvor checken er foroven efterfulgt af to remitteringsafsnit. Det omfatter også et eksempelformat, hvor checken er i midten mellem to remitteringsafsnit. Disse eksempelformater svarer til Deluxe-forretningscheckformater.

## <a name="what-do-i-have-to-set-up"></a>Hvad skal jeg bruge for at komme i gang?

- Før du kan udskrive checks ved hjælp af ER, skal mindst én aktiv checkkonfiguration importeres til dine ER-konfigurationer. Du kan finde vejledning i [Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Når du konfigurerer check i Kontant- og bankstyring for bankkontoen, skal du markere afkrydsningsfeltet **Generisk elektronisk eksportformat** og derefter vælge det relevante checkformat som en eksportformatkonfiguration.
- Du skal også angive antallet af bilagslinjer, der skal udskrives på remitteringen. Husk at medtage overskriftsrækker, når du beregner dette tal. For de to eksempelformater er det anbefalede antal følgeseddellinjer 17. Men dette nummer varierer afhængigt af din checkbeholdning og printerdriverne.
- Det anbefales at udskrive en prøvecheck for at validere checklayoutet. For at udskrive en prøvecheck skal du vælge indstillingen **Udskriv prøve**. Eksempelcheckformaterne fungerer bedst, når **Margener** er indstillet til **Ingen** i de avancerede printeregenskaber for Microsoft Excel. Når prøvechecken er oprettet, skal du aktivere redigering af Excel-outputtet og konfigurere sidelayoutet, så alle margener er indstillet til **0** (nul). Sammenlign testkopien af checkene med din checkbeholdning, og juster indstillingerne, indtil du er tilfreds med justeringen.
- Når du genererer betalinger for den konfigurerede bankkonto i betalingskladden, udskrives checks ved hjælp af det angivne format.

Du kan finde flere oplysninger under [Redigere et elektronisk rapporteringsformat](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).