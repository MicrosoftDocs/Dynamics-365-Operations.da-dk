---
title: Opret en genopfyldningsordre til konsignation
description: "Denne procedure viser, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Opret en genopfyldningsordre til konsignation

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager. Det viser også, hvordan du registrerer modtagelse af produkter, så konsignationslageret registreres som disponibel lagerbeholdning, der ejes af leverandøren. Denne procedure vil normalt ske via en indkøber. Du kan bruge denne guide i USMF-demodatafirmaet. Denne procedure er til en funktion, der blev tilføjet i Dynamics 365 for Operations, version 1611.




## <a name="create-a-consignment-replenishment-order"></a>Opret en genopfyldningsordre til konsignation
1. Gå til Indkøb og forsyning > Konsignation > Genopfyldningsordrer til konsignation.
2. Klik på Ny.
3. Vælg leverandøren US-104 i feltet Kreditorkonto.
    * Du skal vælge en leverandør, der er registreret som ejer på siden Lagerejere.  
4. Klik på OK.
5. Klik på Tilføj linje.
6. I feltet Varenummer skal du skrive M9211CI.
    * Du skal vælge en vare, der er oprettet til konsignationslageret.  
7. Angiv et tal i feltet Antal.
8. Angiv en dato i feltet Ønsket leveringsdato.
    * De ønskede og bekræftede datoer, der bruges af MRP-programmet for den forventede ankomst af varer.  
9. Angiv en dato i feltet Bekræftet leveringsdato.
10. Vis eller skjul sektionen Linjedetaljer.
11. Klik på fanen Lagerdimensioner.
12. Opdater siden for at få vist ejeren i feltet Ejer af lagerdimensioner.
    * Leverandør US-104 er nu anført som ejer.  

## <a name="check-the-inventory-transaction-status"></a>Kontroller lagerposteringsstatussen
1. Klik på lager.
2. Klik på Transaktioner.
3. Markér den valgte række på listen.
    * Bemærk, at feltet Modtagelse er indstillet til Bestilt.  
4. Luk siden.

## <a name="receive-items"></a>Modtag varer
1. Klik på Produktkvittering.
2. Skriv en værdi i feltet Ekstern produktkvittering.
3. Skriv et tal i feltet Antal, der er lavere end det tal, der vises.
4. Klik på OK.

## <a name="check-the-on-hand-inventory"></a>Kontroller lagerbeholdningen
1. Klik på lager.
2. Klik på Beholdning.
3. Klik på Oversigt.
    * De varer, der er modtaget som konsignationslager, der ejes af leverandøren, er disponible. Det resterende antal på genopfyldningsordren til konsignation vises i feltet Bestilt i alt.  
4. Luk siden.
5. Klik på Luk.

