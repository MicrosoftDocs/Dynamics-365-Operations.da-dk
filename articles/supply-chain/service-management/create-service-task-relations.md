---
title: Oprette serviceopgaverelationer
description: Du kan knytte serviceopgaver til serviceaftaler eller serviceordrer for at beskrive den serviceopgave, der skal udføres for aftalen eller ordren.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea5952376fe30f489d385c8f8295fbf86f2af085
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470724"
---
# <a name="create-service-task-relations"></a>Oprette serviceopgaverelationer    

[!include [banner](../includes/banner.md)]

Du kan knytte serviceopgaver til serviceaftaler eller serviceordrer for at beskrive den serviceopgave, der skal udføres for aftalen eller ordren. Disse oplysninger er tilgængelige for serviceteknikere og kunder.

## <a name="create-a-relation-with-a-service-agreement"></a>Oprette en relation med en serviceaftale

1.  Gå til **Servicestyring** \> **Fælles** \> **Serviceaftaler** \> **Serviceaftaler**.

2.  Vælg en eksisterende serviceaftale, eller opret en ny.

3.  Vælg knappen **Serviceopgaver** i handlingsruden.

4.  Vælg **Ny** i formularen **Serviceopgaver** for at oprette en ny linje, og vælg derefter en serviceopgave på listen **Serviceopgave** for at knytte serviceopgaven til serviceaftalen.

5.  Angiv beskrivelser af evt. interne eller eksterne noter i fritekstfelterne under fanen **Beskrivelse**.

6.  Luk formen for at gemme posten.

Gentag denne procedure, indtil du har oprettet alle nødvendige serviceopgaverelationer for serviceaftalen. Du kan nu angive disse serviceaftaler for alle tilknyttede aftalelinjer.

En serviceopgaverelation, der oprettes til en serviceaftale, kan vælges fra alle de serviceordrer, der er tilknyttet serviceaftalen.

## <a name="create-a-relation-with-a-service-order"></a>Oprette en relation med en serviceordre

1.  Gå til **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.

2.  Vælg en eksisterende serviceordre, eller opret en ny.

3.  Vælg knappen **Serviceopgaver** i handlingsruden.

4.  Vælg **Ny** i formularen **Serviceopgaver** for at oprette en ny linje, og vælg derefter en serviceopgave på listen **Serviceopgave** for at knytte serviceopgaverne til serviceordren.

5.  Angiv beskrivelser af evt. interne eller eksterne noter i fritekstfelterne under fanen **Beskrivelse**.

6.  Luk formen for at gemme posten.

Gentag denne procedure, indtil du har oprettet alle nødvendige serviceopgaverelationer for serviceordren. Du kan nu vælge den serviceopgave, du har oprettet relationen for, når du opretter serviceordrelinjer.

Serviceopgaverelationer, der oprettes til en serviceordre, kan vælges i den specifikke serviceordre.

## <a name="see-also"></a>Se også

[Oversigt over serviceopgaver](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]