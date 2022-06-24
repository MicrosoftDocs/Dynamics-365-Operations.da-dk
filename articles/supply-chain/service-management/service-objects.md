---
title: Oversigt over serviceobjekter
description: Denne artikel giver et overblik over, hvordan du kan arbejde med serviceobjekter.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8150a94677fe38f4caa6f3e0b5fb5d1be5972eaf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862405"
---
# <a name="service-objects-overview"></a>Oversigt over serviceobjekter

[!include [banner](../includes/banner.md)]

Serviceobjekter er en kundes aktiver og produkter, som du kan udføre en service på. Afhængigt af, hvilken form for service og ydelser du kan tilbyde, kan objekterne være materielle eller immaterielle:

-  Materielle objekter er ting, f.eks. maskiner eller en bygning, som du kan udføre en fysisk serviceopgave på.

    Et materielt serviceobjekt kan også være en lagervare, som du opretter i formularen Frigivne produktdetaljer. Afhængigt af den lagerdimensionsgruppe, som du knytter til varen, kan du oprette et serviceobjekt til et detaljeniveau, som omfatter vareserienummeret. Det er en fordel, når du skal kunne følge netop den vare, som serviceobjektet repræsenterer.

    Et materielt serviceobjekt kan også være en vare, der ikke er direkte relateret til et firmas direkte produktion eller forsyningskæde. En værktøjskasse, der anvendes til reparation i en serviceordre, kan for eksempel være et serviceobjekt, der ikke findes på lageret. I så fald skal du ikke registrere det som en lagervare.

-  Immaterielle objekter er ikke-fysiske ting, f.eks. en række konti eller et juridisk dokument, som du kan udføre en serviceopgave på.

## <a name="example-of-an-intangible-service-object"></a>Eksempel på et immaterielt serviceobjekt

Firma A fører finansielle poster for flere små virksomheder. En af virksomhed A's kunder er det lokale fodboldhold, for hvem virksomhed A har den ugentlige bogføring og den årlige revision af klubbens konti. Klubbens konti er oprettet i formularen Serviceobjekter og angives som objektet i serviceaftalen. Der er to linjer i serviceaftalen for objektet. Linje 1 er den ugentlige bogføring med et ugentligt interval, der er knyttet til linjen, og linje 2 er den årlige revision med et årligt interval tilknyttet.

## <a name="related-articles"></a>Relaterede artikler

[Oprette serviceobjekter](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]