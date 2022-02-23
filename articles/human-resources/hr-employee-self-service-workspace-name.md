---
title: Skifte arbejdsområdenavn for medarbejderselvbetjening
description: Dette emne beskriver, hvor du ændrer visningsnavnet for arbejdsområde for medarbejderselvbetjening i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2ce008c44ba84c919f4538be4d8e4ff95be018e7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417877"
---
# <a name="change-employee-self-service-workspace-name"></a>Skifte arbejdsområdenavn for medarbejderselvbetjening

Hvis du har frivillige eller andre, der ikke er medarbejdere, kan det være en god ide at ændre navnet på arbejdsområdet **Medarbejderselvbetjening**. Du kan ændre dette arbejdsområde til **Selvbetjening** i stedet.

> [!NOTE]
> Hvis du ændrer navnet på arbejdsområdet **Medarbejderselvbetjening**, ændres også det menupunkt, der bruges internt af Dynamics 365 Human Resources. Hvis du tidligere har anvendt sikkerhedstilpasninger på menupunktet **HcmMedarbejderSelvbetjeningArbejdsområde**, anbefales det, at du anvender de samme ændringer i **HcmSelvbetjeningArbejdsområde** for at bevare pariteten.

1. I Human Resources skal du vælge **Personalestyring**, vælge **Links** og derefter vælge **Human Resources-parametre**.

2. Vælg fanen **Medarbejderselvbetjening**.

3. Under **Visningsnavn** skal du vælge **Selvbetjening**.

   ![Skift navnet på arbejdsområdet Medarbejderselvbetjening til Selvbetjening](./media/hr-employee-self-service-workspace-name.png)

4. Vælg **Gem**.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over medarbejderes og lederes selvbetjening](hr-employee-manager-self-service-overview.md)
