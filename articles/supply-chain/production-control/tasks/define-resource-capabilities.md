---
title: Definere ressourceegenskaber
description: Ressourceegenskaber beskriver, hvad operationsressourcer kan gøre.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42451da0bd465ce3a18ecf18570f3331847474c1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579106"
---
# <a name="define-resource-capabilities"></a>Definere ressourceegenskaber

[!include [banner](../../includes/banner.md)]

Ressourceegenskaber beskriver, hvad operationsressourcer kan gøre. Under planlægningen sammenlignes krav i hvert enkelt job og handling med egenskaberne hos de tilgængelige ressourcer. Denne opgaveguide hjælper dig med at oprette en ressourceegenskab og tildele den til en ressource. Det demodatafirma, der bruges til at oprette denne opgave, er USMF.


## <a name="create-a-resource-capability"></a>Opret en ny ressourceegenskab.
1. Gå til Ressourceegenskaber.
2. Klik på Ny.
3. Skriv id'et for ressourcens egenskab i feltet Egenskab.
    * For en given operation kan du bruge egenskabs-id'et til at angive, at ressourcerne skal have denne egenskab for at udføre handlingen.  
4. Skriv en beskrivelse af egenskaben i feltet Beskrivelse.

## <a name="assign-capability-to-a-resource"></a>Tildel egenskab til en ressource
1. Klik på Tilføj.
2. Skriv id'et for ressourcen i feltet Ressource.
    * En ressourceegenskab kan tildeles til en eller flere ressourcer.  
3. Angiv en dato i feltet Udløb.
    * Du kan bruge dette felt til at angive, at en ressource kun har egenskaben i et begrænset tidsrum.  
4. Angiv et tal i feltet Prioritet.
    * Når du planlægger opgaver og operationer, kan du angive, om du vil vælge ressourcer efter prioritet. Hvis du vælger at gøre dette, og mere end én ressource kan udføre jobbet eller handlingen inden den ønskede dato, vælges ressourcen med den laveste prioritet med hensyn til den nødvendige egenskab.  
5. Angiv et tal i feltet Niveau.
    * Når du angiver, at et job eller en handling kræver en bestemt egenskab, kan du også angive det krævede minimumsniveau. Brug egenskabsniveauet til at skelne mellem ressourcer, der kan udføre det samme job, men ved forskellige hastigheder, styrke, omfang og så videre.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]