---
title: Varen kan ikke have en stykliste eller formel
description: Når du forsøger at autorisere en ordre, modtager du en fejlmeddelelse under varevalidering. Den angiver, at varen ikke kan have en stykliste eller formel.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730100"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Varen kan ikke have en stykliste eller formel

Fejlkode: PRO2614

## <a name="symptoms"></a>Symptomer

Når du forsøger at autorisere en ordre, modtager du følgende fejlmeddelelse under varevalidering:

> Varen kan ikke have en stykliste eller formel

## <a name="resolution"></a>Løsning

Varer, der har en stykliste eller formel, skal være af typen *Planlægningsvare*, *Stykliste* eller *Formel*. Benyt følgende fremgangsmåde for at ændre typen af vare.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Åbn det relevante produkt.
1. I oversigtspanelet **Opret** skal du angive feltet **Produktionstype** til *Planlægsningsvare*, *Stykliste* eller *Formel*.
