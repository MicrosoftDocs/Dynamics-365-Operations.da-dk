---
title: Integration for serviceaftaler og -projekter
description: Når du arbejder med serviceaftaler og serviceaftalelinjer, bruger du de data, der er konfigureret i følgende områder i Projektstyring og regnskab.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77b61c0b9d48557e25ec5aec43dd6546605d35b6fa2ac810d55b3333a8f00289
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720151"
---
# <a name="integration-for-service-agreements-and-projects"></a>Integration for serviceaftaler og -projekter 

[!include [banner](../includes/banner.md)]


Når du arbejder med serviceaftaler og serviceaftalelinjer, bruger du de data, der er konfigureret i følgende områder i **Projektstyring og regnskab**.

## <a name="project-prices"></a>Projektpriser

Kost- og salgsprisen for en serviceaftalepostering er afledt af den opsætning af kostpriser, der gælder for det projekt, som er knyttet til serviceaftalen. Kost- og salgspriser kan oprettes efter projekt, medarbejder og kategori. 

## <a name="project-validation"></a>Validering - projekter

De projekter, medarbejdere og kategorier, der kan vælges til en serviceaftalelinje, kan begrænses af opsætningen af validering i **Projektstyring og regnskab**. Ved hjælp af opsætning af validering kan du kombinere projekter, medarbejdere og kategorier for at kontrollere adgangen. 

## <a name="project-line-properties"></a>Projektlinjeegenskaber

En linjeegenskab angives automatisk for en serviceaftalelinje.

Linjeegenskaber oprettes i formularen **Linjeegenskaber** i **Projektstyring og regnskab**. Den linjeegenskab, der indsættes i en serviceaftale, knyttes til det projekt, der er valgt for serviceaftalen, og overføres efterfølgende til serviceaftalelinjen. 

## <a name="default-offset-accounts"></a>Standardmodkonti

Hvis du angiver en udgiftspostering, vælges der automatisk en standardmodkonto for denne postering. Standardudgiftskontoen konfigureres for det projekt, der er knyttet til den aktuelle serviceaftale.

## <a name="project-categories"></a>Projektkategorier

De kategorier, der er tilgængelige for serviceaftalelinjer, er konfigureret i formularen **Projektkategori** i afsnittet **Projektstyring og regnskab**. 

> [!NOTE]
> <P>Kategorier, hvor afkrydsningsfeltet <STRONG>Aktiv i kladder</STRONG> er markeret under fanen <STRONG>Projekt</STRONG> i formularen <STRONG>Projektkategorier</STRONG>, kan vælges. Hvis afkrydsningsfeltet <STRONG>Inaktive kategorier</STRONG> er markeret under fanen <STRONG>Kladder</STRONG> i formularen <STRONG>Parametre for projektstyring og regnskab</STRONG>, kan alle kategorier vælges.</P>

## <a name="project-parameters"></a>Projektparametre

Hvis feltet **Fratrådte arbejdere** under fanen **Kladder** i formularen **Parametre for projektstyring og regnskab** er markeret, kan du vælge inaktive medarbejdere og aktive medarbejdere i formularerne **Serviceaftaler** og **Serviceordrer**.

Du kan også aktivere felterne **Starttidspunkt** og **Sluttidspunkt** under fanen **Projekt** i formularen **Serviceordrer** for at angive start- og sluttidspunkter på serviceordrelinjer.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Aktivere funktionen for start- og sluttidspunkter på serviceordrer

1.  Klik på **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.

2.  Klik på fanen **Kladder**, og marker afkrydsningsfeltet **Vis start-/ sluttidspunkt**.

3.  Klik på **Projektstyring og regnskab** \> **Opsætning** \> **Kladder** \> **Kladdenavne**.

4.  Markér det kladdenavn, der er knyttet til serviceordren.

5.  Klik på fanen **Generelt**, og marker afkrydsningsfeltet **Vis start-/ sluttidspunkt**.


> [!NOTE]
> <P>Vælg det kladdenavn for serviceordren i feltet <STRONG>Time</STRONG> under fanen <STRONG>Kladder</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG>.</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]