---
title: Oprette serviceaftaler
description: I dette emne beskrives det, hvordan du kan bruge funktionerne i modulerne Servicestyring og Projektstyring og regnskab til at oprette serviceaftaler.
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
ms.openlocfilehash: 4daf023cb65cad39eab9e1560a0093e78cada0fbfb993b8db2d182c26f476397
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759401"
---
# <a name="create-service-agreements"></a>Oprette serviceaftaler

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du kan bruge funktionerne i modulerne Servicestyring og Projektstyring og regnskab til at oprette serviceaftaler.

## <a name="create-a-service-agreement-from-service-management"></a>Oprette en serviceaftale fra Service

1. Gå til **Servicestyring**.
2. Vælg **Serviceaftaler** for at oprette en ny serviceaftalelinje i sidehovedet. 
3. Vælg **Ny**. Indtast en beskrivelse, vælg en reference til et projekt i feltet **Projekt-id**, og udfyld resten af felterne og linjerne til serviceaftalen. Vælg **Gem**.
4. Under fanen **Relationer** skal du vælge **Serviceobjekter** eller **Serviceopgaver** for at oprette serviceobjektrelationer eller serviceopgaverelationer for serviceaftalen. De serviceobjekter og -opgaver, du har oprettet relationer for, kan tilknyttes på serviceaftalelinjerne.
5. På den nederste halvdel af siden kan du oprette serviceaftalelinjer ved at kopiere linjer fra en serviceskabelon eller en anden serviceaftale eller ved at oprette serviceaftalelinjerne manuelt.

> [!NOTE]
> Hvis du kopierer linjer til serviceaftalen fra en anden serviceaftale, kan du angive, om du også vil kopiere serviceobjektrelationer og serviceaftalerelationer. Hvis du kopierer disse relationer, føjes de til eventuelle eksisterende relationer på serviceaftalen. Hvis du kopierer serviceaftalelinjer fra en serviceskabelon, kopieres serviceobjektrelationerne og serviceopgaverelationerne automatisk som serviceobjektrelationer og serviceopgaverelationer på de nye serviceaftalelinjer.

## <a name="create-service-agreement-lines-manually"></a>Oprette serviceaftalelinjer manuelt

1. På siden **Serviceaftaler** skal du tilføje en serviceaftalelinje i linjegitteret. 
2. Angiv de relevante oplysninger for serviceaftalelinjen. 
3. Vælg **Gem** for at gemme linjen, og luk derefter siden.

## <a name="create-a-service-agreement-from-project"></a>Oprette en serviceaftale fra Projekt

1. Vælg **Projektstyring og regnskab**.
2. Vælg **Alle projekter**.
3. Vælg projektet på listen.
4. Vælg **Administrer** i **handlingsruden**. I **Ny**-aktionsgruppen skal du vælge **Service** og vælge **Serviceaftale**.
5. Følg trinnene i sektionen med titlen **Oprette en serviceaftale** som beskrevet tidligere i dette emne for at angive projektreferencen.


## <a name="related-topics"></a>Relaterede emner

[Oversigt over udvikling og udfyldelse af serviceaftaler](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]