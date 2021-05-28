---
title: Lokationsprofil tillader ikke negativt lager, men negativ disponeret lagerbeholdning tillades
description: Indstillingen Tillad negativ lagerbeholdning for lokationsprofilen er indstillet til Nej, men systemet tillader stadig negativ lagerbeholdning.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026369"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Lokationsprofil tillader ikke negativt lager, men negativ disponeret lagerbeholdning tillades

KB-nummer: 4613622

## <a name="symptoms"></a>Symptomer

Indstillingen **Tillad negativ lagerbeholdning** for lokationsprofilen er indstillet til *Nej*, men systemet tillader stadig negativ lagerbeholdning.

## <a name="example-scenario"></a>Eksempelscenario

For offentligt regulerede transaktioner skal systemet kunne registrere negativt lager for at kunne registrere tab. Du vil have, at en vare skal kunne vise negativ lagerbeholdning, men kun på angivne lokationer, f.eks. tankstationer. Hvis varemodelgruppen tillader negativt lager, opdager du dog, at det er ligegyldigt, om lokationen er indstillet til at tillade negativt lager. Hvis varen er konfigureret, så negativt lager ikke er tilladt, er det ligegyldigt, hvordan lokationsprofilen er konfigureret.

## <a name="resolution"></a>Løsning

Indstillingen **Tillad negativ lagerbeholdning** fra lokationsprofilen gælder kun for lagerprocesser som f.eks. plukning. Varemodelgrupper, der er indstillet til at tillade negativt lager, påvirker dog alle processer fra modulerne Lagerstyring og Lokationsstyring, og lokalitetsprofilen tilsidesætter ikke indstillingen.

Du kan styre, om et lagersted må have negativt lager. Indstil varemodelgrupperne til at forbyde negativt fysisk lager, og indstil kun det relevante lagersted til at tillade negativt lager.
