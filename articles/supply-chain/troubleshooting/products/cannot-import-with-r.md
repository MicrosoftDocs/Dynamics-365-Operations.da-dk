---
title: Du kan ikke importere en vare ved hjælp af enheden Frigivne produkter V2
description: Du kan ikke importere en vare ved hjælp af enheden Frigivne produkter V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764686"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Du kan ikke importere en vare ved hjælp af enheden Frigivne produkter V2

KB-nummer: 4611825

## <a name="symptoms"></a>Symptomer

Når du forsøger at importere en vare ved hjælp af enheden *Frigivne produkter V2*, modtager du en fejlmeddelelse, der svarer nogenlunde til følgende eksempel:

> Der kan ikke oprettes en post i Varer – sporingsdimensionsgrupper (EcoResTrackingDimensionGroupItem). Varenummer: 2040663, Batch. Posten findes allerede.

## <a name="resolution"></a>Løsning

Hvis du vil importere nye frigivne produkter, skal du bruge enheden *Frigivet produktoprettelse V2* i stedet for enheden *Frigivne produkter V2*.
