---
title: "Ændre ejerskabet til konsignationslager ud fra produktionsbehov"
description: "Denne fremgangsmåde viser, hvordan du ændrer ejeren af konsignationslageret fra leverandøren til din juridiske enhed, når der er behov for lageret i produktionen."
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5925f5423d596adc4326dfff4734de2afd80b5a8
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Ændre ejerskabet til konsignationslager ud fra produktionsbehov

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du ændrer ejeren af konsignationslageret fra leverandøren til din juridiske enhed, når der er behov for lageret i produktionen. Denne ændring af ejerskabet sker ved at oprette og bogføre en ændringskladde for lagerejerskab. Ændringskladdelinjer for ejerskab kan oprettes manuelt, eller som vist i denne registrering, baseret på eksisterende produktionsbehov. Typisk udfører en tilsynsførende denne opgave. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data. Hvis du bruger dine egne data, skal du kontrollere, at du har følgende forudsætninger: navnet på en lagerbeholdning, der er blevet oprettet til ændring af lagerejerskab, fysisk registrerede kreditorejede disponible varer og en eller flere produktionsordrelinjer for materialet. Denne procedure er til en funktion, der blev tilføjet i Dynamics 365 for Operations, version 1611.


## <a name="create-an-inventory-ownership-journal"></a>Opret en lagerejerskabskladde
1. Gå til Lagerstyring > Kladdeposteringer > Elementer > Ændring af lagerejerskab.
2. Klik på Ny.
    * Kladden for ændring af beholdningsejerskab bruges til at ændre ejeren af konsignationslager fra leverandøren til den aktuelle juridiske enhed. Denne ændring af ejerskabet sker ved at frigive den disponible lagerbeholdning, der ejes af leverandøren, og derefter modtage dette lager i den aktuelle juridiske enhed.  
3. Indtast eller vælg en værdi i feltet Navn.
    * Du kan kun vælge lagerkladdenavne, der har kladdetypen Ændring af ejerskab.  
4. Klik på OK.
5. Klik på Funktioner.
6. Klik på Opret kladdelinjer ud fra produktionsordrer.
    * Du kan starte processen til ændring af ejerskab ved at forespørge alle produktionslinjer, der er behov for forbrug af råvarer.  
7. I Statusser, der skal medtages for lagerafgang skal du vælge en indstilling.
    * Brug denne indstilling til at filtrere efter afgangsstatus for lagerposteringer. Du kan for eksempel oprette kladdelinjer for lager, der har statusserne Plukket og Reserveret fysisk.  
8. Udvid posterne for at inkludere sektion.
    * I dette afsnit kan du anvende yderligere filtrering. Du kan for eksempel vælge en dato for en bestemt råvare.  
9. Klik på OK.

## <a name="post-the-inventory-ownership-change-journal"></a>Bogfør ændringskladden for beholdningsejerskab
1. Klik på Bogfør.
    * Når kladden er bogført, frigives det lager, der ejes af leverandøren, ved hjælp af henvisningen "Ændring af ejerskab". Lagerbeholdningen modtages derefter som disponibel ved hjælp af den lagertransaktion, der opdateres på produktkvitteringen for indkøbsordre. Bemærk, at det kun er transaktioner, der vedrører den bogførte kladde, der oprettes. Der oprettes ingen forventede lagertransaktioner.  
2. Klik på OK.
3. Luk siden.

