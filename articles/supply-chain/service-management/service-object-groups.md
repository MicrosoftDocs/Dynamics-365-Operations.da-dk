---
title: Serviceobjektgrupper
description: Objektgrupper kan bruges til at sortere og filtrere data om objekter til rapporter og statistikker.
author: YuyuScheller
manager: AnnBe
ms.date: 05/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2ab3ed8a8f36f980473b17b5dfed8cb3d0054253
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-groups"></a>Serviceobjektgrupper 

[!include [banner](../includes/banner.md)]

Objektgrupper kan bruges til at sortere og filtrere data om objekter til rapporter og statistikker. Du kan f.eks. gruppere objekter efter geografisk placering eller type.

## <a name="group-by-geographical-location"></a>Gruppere efter geografisk placering

Du kan bruge denne grupperingsmetode til at vise, hvor de forskellige objekter, som dit firma servicerer, er beliggende. Gruppering af objekter efter geografisk placering kan også være nyttigt, hvis du f.eks. har brug for at identificere objekter, som dit firma allerede leverer service til i et bestemt land eller område.

## <a name="example"></a>Eksempel

En kunde fra Belgien kontakter dit servicecenter og ønsker at indgå en serviceaftale vedrørende et objekt, ABC. Du har knyttet en objektgruppe for geografisk placering, Belgien, til alle objekter, der serviceres i Belgien. Ved at bruge denne gruppe som filter kan du hurtigt finde ud af, om ABC allerede findes som en post i programmet, eller du skal definere et nyt objekt. 

## <a name="group-by-type"></a>Gruppere efter type

Du kan bruge denne grupperingsmetode til at vise de typer af objekter, som dit firma servicerer. Gruppering af objekter efter type kan også være nyttigt, hvis du f.eks. vil oprette et nyt objekt ud fra lignende eksisterende objekter i programmet.

## <a name="example"></a>Eksempel

En kunde ringer for at indgå en serviceaftale vedrørende et klimaanlæg, HIJ. Du har ikke i forvejen nogen post til dette anlæg. Du har derimod oprettet en objektgruppe med navnet Klimaanlæg, og du har knyttet denne gruppe til alle klimaanlægsobjekter. Derfor kan du hurtigt søge efter og identificere alle andre klimaanlæg og bruge skabelonoplysningerne fra disse objekter som grundlag for serviceaftalelinjerne til HIJ. Ved at bruge objektgrupper på denne måde sparer du tid, når du skal oprette nye objekter og finde ud af, hvilke serviceopgaver der skal udføres på dem. 

## <a name="create-service-object-groups"></a>Oprette serviceobjektgrupper

Opret grupper, som du kan tildele serviceobjekter til. Serviceobjekter er lagervarer og andre produkter, der udføres serviceydelser for. Ved at gruppere serviceobjekter kan du oprette rapporter for lignende og relaterede serviceobjekter. For eksempel kan en serviceobjektgruppe bestå af to serviceobjekter: ét serviceobjekt er en pakke, og det andet serviceobjekt er tjenesten, der skal installere pakken.

Hvis du vil oprette serviceobjektgrupper, skal du følge disse trin:

1. Klik på **Servicestyring > Opsætning > Serviceobjekter > Serviceobjektgrupper**.

2. Klik på **Ny** for at oprette en ny serviceobjektgruppe.

3. Angiv et entydigt navn for serviceobjektgruppen og evt. en beskrivelse.

Du kan tildele serviceobjekter til gruppen ved hjælp af formularen **Serviceobjekter**. 

## <a name="see-also"></a>Se også

[Oprette serviceobjekter](create-service-objects.md)



