---
title: Serviceskabeloner
description: Du kan definere en serviceaftale som en skabelon og senere kopiere linjerne i skabelonen til en anden serviceaftale eller til en serviceordre.
author: ShylaThompson
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 409c15ae9c8f5f3c9c72adf3313f4594ba3c1764
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819010"
---
# <a name="service-templates"></a>Serviceskabeloner

[!include [banner](../includes/banner.md)]

Du kan definere en serviceaftale som en skabelon og senere kopiere linjerne i skabelonen til en anden serviceaftale eller til en serviceordre.

## <a name="example"></a>Eksempel

En kunde, som du yder service til, har identiske serviceelevatorer på fem forskellige lokationer.

Du vil definere fem serviceaftaler for kunden, én for hvert sted.
For at begrænse gentagelser i opsætningen og for at sikre, at opsætningsoplysninger i serviceaftalerne er identiske, opretter du en serviceaftale og specificerer den som en skabelon til servicearbejdet med elevatorerne.

Du kan nu kopiere skabelonlinjerne til de fem nye serviceaftaler, så hver serviceaftale udfyldes med linjerne fra skabelonen.

## <a name="create-a-template"></a>Opret en skabelon

Når du opretter en serviceskabelon, opretter du en serviceaftale, samtidig med at du opretter de nødvendige linjer i den, og derefter knytter du serviceaftalen til serviceskabelongruppen.

> [!NOTE]
> En serviceaftale kan kun defineres som en skabelon, hvis den ikke har tilknyttede serviceordrer. Der kan desuden ikke oprettes serviceordrer ud fra en serviceaftale, der er defineret som en skabelon.

## <a name="copy-template-lines"></a>Kopiér skabelonlinjer

Du kan kopiere skabelonlinjer fra en serviceskabelon til en anden serviceaftale eller til en serviceordre.

Når du kopierer skabelonlinjer til dine serviceordrer eller -aftaler, vises skabelongrupperne i en trævisning, hvor hver gruppe kan udvides. I denne visning kan du få vist hver skabelon og skabelonlinje.

Det er lettere at fastlægge, hvilke serviceskabelonlinjer du vil kopiere, hvis du har grupperet skabelonerne under navne, der afspejler brugen af skabelonerne.

## <a name="related-topics"></a>Relaterede emner

[Kopiere serviceskabelonlinjer](copy-service-template-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]