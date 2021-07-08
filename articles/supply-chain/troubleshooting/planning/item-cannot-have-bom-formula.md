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
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294038"
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
