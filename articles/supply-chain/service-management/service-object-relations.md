---
title: Serviceobjektrelationer
description: Du kan oprette serviceobjektrelationer mellem et serviceobjekt og en serviceaftale eller en serviceordre.
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
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
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: 0e54a0dc9b643077d45fe76e073772e81f99ea44
ms.contentlocale: da-dk
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-relations"></a>Serviceobjektrelationer 

[!include[banner](../includes/banner.md)]



Du kan oprette serviceobjektrelationer mellem et serviceobjekt og en serviceaftale eller en serviceordre. Når du opretter en relation, knyttes serviceobjektet til serviceaftalen eller serviceordren.

Når relationen er oprettet, kan du knytte serviceobjektet til alle linjer i serviceaftalen eller serviceordren.

## <a name="template-boms"></a>Styklisteskabeloner

Du kan også angive en styklisteskabelon til objektrelationen. Styklisteskabelonen er en stykliste til det objekt, service udføres for. Hvis du erstatter en komponentgruppe i serviceobjektet under et servicebesøg, kan du registrere denne ændring i servicestyklisten ved at bruge formen Serviceobjekter.

## <a name="example"></a>Eksempel

Du opretter en serviceaftale for servicering af to elevatorer hos en kunde.
Serviceaftalen her id'et ID SAL-001.

Elevatorerne er i formen Serviceobjekter angivet som objekter, EL-S/1000 og EL-L/1000.

Du knytter serviceobjekterne, EL-S/1000 og EL-L/1000, til serviceaftalen.

Du ønsker at registrere ændringer i styklisten for serviceobjektet, mens du erstatter komponentdelene i objektet, og derfor knytter du en servicestykliste til serviceobjektrelationen som beskrevet i følgende tabel.

| serviceobjekt | Relation – serviceaftale | Servicestykliste   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | Stykliste-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | Stykliste-EL-L/1000 |

Da der findes serviceobjektrelationer til aftalen, kan du nu oprette serviceaftalelinjer med disse objekter som vist i følgende tabel.

| Konteringstype | Kategori           | serviceobjekt |
|------------------|--------------------|----------------|
| Time             | Inspektion         | EL-S/1000      |
| Time             | Rensning af gearkasse  | EL-S/1000      |
| Vare             | Materialer til rensning | EL-S/1000      |
| Time             | Inspektion         | EL-L/1000      |
| Time             | Rensning af gearkasse   | EL-L/1000      |
| Vare             | Materialer til rensning | EL-L/1000      |

Under et servicebesøg er du nødt til at udskift gearkassen til elevator EL-S/1000. Når en komponentdel i objektet skal udskiftes, kan du få adgang til styklistedesigneren ved at bruge den serviceobjektrelation, du har angivet for den aktuelle serviceaftale.

Få adgang til styklistedesigneren ved brug af en serviceobjektrelation

1. Serviceaftaler
2. Dobbeltklik på en serviceaftale, eller klik på Serviceaftale for at oprette en ny serviceaftale.
3. Klik på fanen Opsætning.
4. Hvis du vil knytte en styklisteskabelon til serviceaftalen, skal du klikke på Serviceobjekter.
5. Klik på Designer for at åbne formen Designer og redigere styklisteskabelonen, i formen Serviceobjekter.

## <a name="automatically-created-service-orders"></a>Automatisk oprettede serviceordrer

Hvis serviceordrer oprettes automatisk for en serviceaftale, oprettes serviceobjektrelationerne i aftalen også i serviceordrerne.


