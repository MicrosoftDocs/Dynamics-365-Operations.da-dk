---
title: Batch-udgivelse af delvist reserverede flytteordrer
description: "I dette emne beskrives, hvordan du kan konfigurere og anvende batchudlevering af delvist reserverede overførselsordrer fra en mobilenhed."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: 4477749c721cf8c8bd244f551d9eca7ec9449fd1
ms.contentlocale: da-dk
ms.lasthandoff: 02/08/2018

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Batch-udgivelse af delvist reserverede flytteordrer

[!include[banner](../includes/banner.md)]

Funktionen til batchfrigivelse af delvist reserveret overførselsordrer giver dig mulighed for delvist at frigive overførselsordrer til et lagersted ved hjælp af et batchjob.
Da du har mulighed for at frigive en delmængde, behøver du ikke vente på, at hele ordreantallet er tilgængeligt på lageret, før du frigiver en ordre.

Frigivelsen af ordrer til et lagersted er en proces til avanceret lagerstyring. Denne proces omfatter aktiviteter, f.eks. plukning, pakning og levering, som en lagermedarbejder kan udføre ved hjælp af en mobil enhed.

## <a name="where-it-applies"></a>Hvor det er relevant

I denne funktion frigives overførselsordrer til et lagersted ved hjælp af et batchjob. Denne funktion er nyttig, når du ikke har tilstrækkelig lagerbeholdning på lagerstedet, men du stadig ønsker at overføre varer fra ét lagersted til en anden.

## <a name="how-it-is-set-up"></a>Sådan konfigureres den

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Angive opfyldelseskriterier for overførsels- og salgsordrer

Inden en ordre kan frigives delvist til et lagersted i en batch, skal opfyldelseskriterierne være opfyldt. Disse opfyldelseskriterier bestemmes af opfyldelsespolitikken

Opfyldelsespolitikker for overførselsordrer og salgsordrer angives på firmaniveau. Afhængigt af konfigurationen af opfyldelsespolitikken kan frigivelse af ordrer i en batch accepteres eller afvises. Ordrerne behandles derefter i overensstemmelse hermed.

-   Hvis du vil oprette opfyldelsespolitikker for overførsels- og salgsordrer, skal du klikke på **Lokationsstyring** \> **Konfiguration** \> **Frigiv til lagersted** \> **Opfyldelsespolitik** og derefter oprette en opfyldelsespolitik ved at angive et navn og en beskrivelse.

-   Hvis du vil angive en opfyldelsessats, en værditype og den meddelelse, der vises, hvis opfyldelsespolitikken overtrædes, skal du klikke på **Lokationsstyring** \> **Konfiguration** \> **Frigiv til lagersted** \> **Opfyldelsespolitik** og derefter angive felterne **Opfyldelsessats**, **Værditype** og **Meddelelser om opfyldelsesovertrædelse**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Angive opfyldelsespolitikker for overførsels- og salgsordrer

-   Hvis du vil angive opfyldelsespolitikkerne for overførselsordrer, skal du klikke på **Lagerstyring** \> **Konfiguration** \> **arametre til lager- og lokationsstyring** \> **Flytteordrer** \> **Lokationsstyring** og derefter vælge en opfyldelsespolitik for flytteordrer.

-   Hvis du vil angive opfyldelsespolitikker for salgsordrer, skal du klikke på **Debitor** \> **Konfiguration** \> **Debitorparametre** \> **Lokationsstyring** og derefter vælge en opfyldelsespolitik for salgsordrer.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Tillade frigivelse i en batch og angive det antal, der skal frigives i en batch

Et batchjob bruges til at frigive ordrer til et lagersted i en batch. De parametre, som adskiller de ordrer, der skal køres i et batchjob, angives i selve batchjobbet.

Parameteren **Antal** angiver, om hele antallet skal frigives, eller om det fysisk reserverede antal skal frigives i en batch. Parameteren **Tillad frigivelse af delvis frigivne ordrer** bestemmer, om ordrer i batchen skal godkendes eller afvises, hvis de tidligere er frigivet delvist.

-   Hvis du vil angive parametrene **Antal** og **Tillad frigivelse af delvis frigivne ordrer** for flytteordrer, skal du klikke på **Lokationsstyring** \> **Frigiv til lagersted** \> **Frigiv flytteordrer automatisk**.

-   Hvis du vil angive parametrene **Antal** og **Tillad frigivelse af delvis frigivne ordrer** for salgsordrer, skal du klikke på **Lokationsstyring** \> **Frigiv til lagersted** \> **Frigiv salgsordrer automatisk**.

