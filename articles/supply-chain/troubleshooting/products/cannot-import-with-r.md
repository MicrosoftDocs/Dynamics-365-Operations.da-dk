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
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026363"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Du kan ikke importere en vare ved hjælp af enheden Frigivne produkter V2

KB-nummer: 4611825

## <a name="symptoms"></a>Symptomer

Når du forsøger at importere en vare ved hjælp af enheden *Frigivne produkter V2*, modtager du en fejlmeddelelse, der svarer nogenlunde til følgende eksempel:

> Der kan ikke oprettes en post i Varer – sporingsdimensionsgrupper (EcoResTrackingDimensionGroupItem). Varenummer: 2040663, Batch. Posten findes allerede.

## <a name="resolution"></a>Løsning

Hvis du vil importere nye frigivne produkter, skal du bruge enheden *Frigivet produktoprettelse V2* i stedet for enheden *Frigivne produkter V2*.
