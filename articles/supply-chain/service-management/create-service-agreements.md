---
title: Oprette serviceaftaler
description: I dette emne beskrives det, hvordan du kan bruge funktionerne i modulerne Servicestyring og Projektstyring og regnskab til at oprette serviceaftaler.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a1a47761869a4190eac6dc9e069a6b520bf7a1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424818"
---
# <a name="create-service-agreements"></a>Oprette serviceaftaler

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du kan bruge funktionerne i modulerne Servicestyring og Projektstyring og regnskab til at oprette serviceaftaler.

## <a name="create-a-service-agreement-from-service-management"></a>Oprette en serviceaftale fra Service

1. Gå til **Servicestyring**.
2. Klik på **Serviceaftaler** for at oprette en ny serviceaftalelinje i sidehovedet. 
3. Klik på **Ny**. Indtast en beskrivelse, vælg en reference til et projekt i feltet **Projekt-id**, og udfyld resten af felterne og linjerne til serviceaftalen. Klik på **Gem**.
4. Under fanen **Relationer** skal du vælge **Serviceobjekter** eller **Serviceopgaver** for at oprette serviceobjektrelationer eller serviceopgaverelationer for serviceaftalen. De serviceobjekter og -opgaver, du har oprettet relationer for, kan tilknyttes på serviceaftalelinjerne.
5. På den nederste halvdel af siden kan du oprette serviceaftalelinjer ved at kopiere linjer fra en serviceskabelon eller en anden serviceaftale eller ved at oprette serviceaftalelinjerne manuelt.

> [!NOTE]
> Hvis du kopierer linjer til serviceaftalen fra en anden serviceaftale, kan du angive, om du også vil kopiere serviceobjektrelationer og serviceaftalerelationer. Hvis du kopierer disse relationer, føjes de til eventuelle eksisterende relationer på serviceaftalen. Hvis du kopierer serviceaftalelinjer fra en serviceskabelon, kopieres serviceobjektrelationerne og serviceopgaverelationerne automatisk som serviceobjektrelationer og serviceopgaverelationer på de nye serviceaftalelinjer.

## <a name="create-service-agreement-lines-manually"></a>Oprette serviceaftalelinjer manuelt

1. På siden **Serviceaftaler** skal du tilføje en serviceaftalelinje i linjegitteret. 
2. Angiv de relevante oplysninger for serviceaftalelinjen. 
3. Tryk på **CTRL+S** for at gemme linjen, og luk derefter siden.

## <a name="create-a-service-agreement-from-project"></a>Oprette en serviceaftale fra Projekt

1. Klik på **Projektstyring og regnskab**.
2. Klik på **Alle projekter**.
3. Vælg projektet på listen.
4. Klik på **Administrer** i **Handlingsrude**. I den **Ny** aktionsgruppe skal du klikke på **Service** og vælge **Serviceaftale**.
5. Følg trinnene i sektionen med titlen **Oprette en serviceaftale** som beskrevet tidligere i dette emne for at angive projektreferencen.


## <a name="related-topics"></a>Relaterede emner

[Oversigt over udvikling og udfyldelse af serviceaftaler](service-agreements.md)


