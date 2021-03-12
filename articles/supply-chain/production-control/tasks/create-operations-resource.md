---
title: Oprette en operationsressource
description: En operationsressource udfører aktiviteterne i et projekt eller en produktionsproces.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b91d5ea7618010ab9d4006d643c59a7f995eb0c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981225"
---
# <a name="create-an-operations-resource"></a>Oprette en operationsressource

[!include [banner](../../includes/banner.md)]

En operationsressource udfører aktiviteterne i et projekt eller en produktionsproces. Denne procedure viser, hvordan du definerer en operationsressource. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.

1. Gå til ressourcer.
2. Klik på Ny.
3. Skriv en værdi i feltet Ressource.
4. Skriv en værdi i feltet Beskrivelse.

## <a name="define-capacity-and-consumption-parameters"></a>Definere kapacitets- og forbrugsparametre
1. Udvid sektionen Handling.
2. Angiv et tal i feltet Spildprocent.
3. Indtast eller vælg en værdi i feltet Opstillingsart.
    * Angiv den omkostningsart, der definerer, hvordan der tages højde for omkostning til opstilling.  
4. Indtast eller vælg en værdi i feltet procestidsart.
    * Angiv den omkostningsart, der definerer, hvordan der tages højde for omkostning til procestid.  
5. Indtast eller vælg en værdi i feltet Antalsart.
    * Angiv omkostningsarten, der definerer, hvordan der tages højde for ressourceomkostninger baseret på output-antal.  
6. Vælg en indstilling i feltet Kapacitetsenhed.
    * Angiv den enhed, som kapaciteten af operationsressourcen udtrykkes i.  
7. Indtast et tal i feltet Kapacitet.
8. Indtast et tal i feltet Effektivitetsprocent.
    * Angiv den effektivitet, du forventer af operationsressourcen. Effektivitetsprocenten justerer operationsressourcens gennemløb og påvirker den tid, der er afsat til ressourcen.  
9. Angiv et tal i feltet Grovplanlægningsprocent.
    * Angiv den maksimale procent af kapaciteten af den operationsressource, som du vil bruge til grovplanlægning.  
10. Vælg Ja i feltet Kapacitetsbegrænsning.
    * Angiv denne indstilling til Ja, hvis operationsressourcen skal planlægges ud fra den faktiske kapacitet, der er tilgængelig, og om der skal tages hensyn til eksisterende kapacitetsreservationer. Hvis denne indstilling er angivet til Nej, antages operationsressourcen at have ubegrænset kapacitet, og ressourcen kan være overbooket.  
11. Vælg Ja i feltet Flaskehalsressource.

## <a name="define-working-times"></a>Definere arbejdstider
1. Udvid sektionen Kalendere.
2. Klik på Tilføj.
3. Indtast eller vælg en værdi i feltet Kalender.
    * Angiv den arbejdstidskalender, der definerer ressourcens kapacitet (i timer).  
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.

## <a name="define-resource-capabilities"></a>Definere ressourceegenskaber
1. Udvid sektionen Egenskaber.
2. Klik på Tilføj.
    * En funktion er en operationsressource evne til at udføre en bestemt aktivitet. Planlægningsprogrammet allokerer ressourcer ved at sammenligne ressourcekravene for hver enkelt aktivitet med funktionerne i de tilgængelige operationsressourcer.  
3. Indtast eller vælg en værdi i feltet Egenskab.
4. Angiv et tal i feltet Niveau.
    * Angiv det færdighedsniveau, som ressourcen behandler egenskaben med.  
5. Angiv et tal i feltet Prioritet.
    * Angiv prioriteten af operationsressourcen med hensyn til egenskaben. Når der planlægges efter prioritet, vælges operationsressourcen med den højeste prioritet (laveste numeriske værdi) først.  

## <a name="assign-resource-to-resource-group"></a>Tildele ressource til ressourcegruppe
1. Udvid sektionen Ressourcegrupper.
2. Klik på Tilføj.
    * Ressourcegruppen definerer rammerne for stedet, produktionsenheden og lagerstedet for operationsressourcer. Operationsressourcen kan kun planlægges, når den tildeles til en ressourcegruppe og kun på det sted, hvor ressourcegruppen er placeret.  
3. Indtast eller vælg en værdi i feltet Ressourcegruppe.
4. Indtast eller vælg en værdi i feltet Indlagringslokalitet.
    * Angive lagerstedslokationen, som operationsressourcen forbruger materialer fra.  

