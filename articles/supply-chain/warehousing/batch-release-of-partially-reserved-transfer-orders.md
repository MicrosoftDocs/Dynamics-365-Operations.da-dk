---
title: Batch-udgivelse af delvist reserverede flytteordrer
description: Denne artikel beskriver, hvordan du kan konfigurere og anvende batchudlevering af delvist reserverede overførselsordrer fra en mobilenhed.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218676"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Batch-udgivelse af delvist reserverede flytteordrer

[!include [banner](../includes/banner.md)]

Funktionen til batchfrigivelse af delvist reserveret overførselsordrer giver dig mulighed for delvist at frigive overførselsordrer til et lagersted ved hjælp af et batchjob.
Da du har mulighed for at frigive en delmængde, behøver du ikke vente på, at hele ordreantallet er tilgængeligt på lageret, før du frigiver en ordre.

Frigivelsen af ordrer til et lagersted er en proces til lagerstyring (WMS). Denne proces omfatter aktiviteter, f.eks. plukning, pakning og levering, som en lagermedarbejder kan udføre ved hjælp af en mobil enhed.

## <a name="where-it-applies"></a>Hvor det er relevant

I denne funktion frigives overførselsordrer til et lagersted ved hjælp af et batchjob. Denne funktion er nyttig, når du ikke har tilstrækkelig lagerbeholdning på lagerstedet, men du stadig ønsker at overføre varer fra ét lagersted til en anden.

## <a name="how-it-is-set-up"></a>Sådan konfigureres den

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Angive opfyldelseskriterier for overførsels- og salgsordrer

Inden en ordre kan frigives delvist til et lagersted i en batch, skal opfyldelseskriterierne være opfyldt. Disse opfyldelseskriterier bestemmes af opfyldelsespolitikken

Opfyldelsespolitikker for overførselsordrer og salgsordrer angives på firmaniveau. Afhængigt af konfigurationen af opfyldelsespolitikken kan frigivelse af ordrer i en batch accepteres eller afvises. Ordrerne behandles derefter i overensstemmelse hermed.

- Hvis du vil oprette opfyldelsespolitikker for overførsels- og salgsordrer, skal du gå til **Lokationsstyring \> Konfiguration \> Frigiv til lagersted \> Opfyldelsespolitik** og derefter oprette en opfyldelsespolitik ved at angive et navn og en beskrivelse.
- Hvis du vil angive en opfyldelsessats, en værditype og den meddelelse, der vises, hvis opfyldelsespolitikken overtrædes, skal du gå til **Lokationsstyring \> Konfiguration \> Frigiv til lagersted \> Opfyldelsespolitikker** og derefter angive felterne **Opfyldelsessats**, **Værditype** og **Meddelelser om opfyldelsesovertrædelse**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Angive opfyldelsespolitikker for overførsels- og salgsordrer

- Hvis du vil angive opfyldelsespolitikkerne for overførselsordrer, skal du gå til **Lagerstyring \> Konfiguration \> Parametre til lager- og lokationsstyring** fanen **Flytteordrer** i sektionen **Lokationsstyring** og derefter vælge en opfyldelsespolitik for flytteordrer.
- Hvis du vil angive opfyldelsespolitikker for salgsordrer, skal du gå til **Debitor \> Konfiguration \> Debitorparametre** fanen **Lokationsstyring** og derefter vælge en opfyldelsespolitik for salgsordrer.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Tillade frigivelse i en batch og angive det antal, der skal frigives i en batch

Et batchjob bruges til at frigive ordrer til et lagersted i en batch. De parametre, som adskiller de ordrer, der skal køres i et batchjob, angives i selve batchjobbet.

Parameteren **Antal** angiver, om hele antallet skal frigives, eller om det fysisk reserverede antal skal frigives i en batch. Parameteren **Tillad frigivelse af delvis frigivne ordrer** bestemmer, om ordrer i batchen skal godkendes eller afvises, hvis de tidligere er frigivet delvist.

- Hvis du vil angive parametrene **Antal** og **Tillad frigivelse af delvis frigivne ordrer** for flytteordrer, skal du gå til **Lokationsstyring \> Frigiv til lagersted \> Frigiv flytteordrer automatisk**.
- Hvis du vil angive parametrene **Antal** og **Tillad frigivelse af delvis frigivne ordrer** for salgsordrer, skal du klikke gå til **Lokationsstyring \> Frigiv til lagersted \> Frigiv salgsordrer automatisk**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
