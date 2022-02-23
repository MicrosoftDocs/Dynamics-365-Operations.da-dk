---
title: Konfigurere produkter, som kan være produceret eller indkøbt
description: 'Produkterne kan købes på forskellige måder: De kan produceres (fremstilles) eller fremskaffes (købes). Denne artikel beskriver nogle typiske punkter, du skal overveje, når du konfigurerer produkter til understøttelse af multiforsyning.'
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7acf4952c1dbb33f4ec615d1ecb9d508a9e7b980
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967502"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a>Konfigurere produkter, som kan være produceret eller indkøbt

[!include [banner](../includes/banner.md)]

Produkterne kan købes på forskellige måder: De kan produceres (fremstilles) eller fremskaffes (købes). Denne artikel beskriver nogle typiske punkter, du skal overveje, når du konfigurerer produkter til understøttelse af multiforsyning. 

Multiforsyning bruges typisk til en købt vare, der fremstilles fra tid til anden, eller når en vare, der var først og fremmest var en produceret vare, ændres, så den nu primært er en købt vare. Varen angives først som en produceret vare, så der kan defineres stykliste- og ruteoplysninger, og for at understøtte produktionsordrer for varen. Produktionstypen skal angives til **Stykliste** (eller til **Formel** eller **Samprodukt** i forbindelse med produktionsprocessen).

Når du bruger standardomkostning, kan vareomkostningsposten beregnes for den producerede vare. Men vareomkostningsposten kan måske ikke beregnes for den standardomkostning, du vil bruge ved indkøb. I dette tilfælde skal standardomkostningen angives og aktiveres manuelt for vareomkostningsposten. I forbindelse med omkostningsberegning kan du overveje at bruge en særlig stykliste og rute, der repræsenterer forsyningsblandingen af produktet i løbet af regnskabsperioden, for at minimere afvigelserne over tid. Derudover kan en produceret vare på ét sted overføres til et andet sted. Varens kostpris skal derfor angives manuelt og aktiveres for det sted, som varen overføres til. Når du bruger den producerede varen som en komponent i varer på højere niveau, skal komponentens omkostninger behandles som en købt vare. Disse retningslinjer gælder, uanset om komponentens omkostninger er beregnet eller angivet manuelt. Vareomkostningen i styklisteberegningen skal med andre ord behandles som en indkøbt komponent i stedet for at bruge varens stykliste og ruteoplysninger til at beregne omkostninger. 

Du kan forhindre beregningen i at finde sted ved at angive flaget **Stop udfoldning**, der er indlejret i den styklistekalkulationsgruppe, som er tilknyttet varen. Du kan forhindre, at der udfoldes behov gennem varen ved behovsplanlægningsberegninger, ved at angive udfoldningshorisonten til 0 (nul) dage i varedisponeringen eller i disponeringsgruppen. I behovsplanlægningsberegningen behandles varen derefter som en købt vare, og der udføres ikke yderligere beregninger for varens stykliste- og ruteoplysninger.





