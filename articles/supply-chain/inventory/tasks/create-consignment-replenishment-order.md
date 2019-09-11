---
title: Oprette en genopfyldningsordre til konsignation
description: Dette emne forklarer, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager.
author: mkirknel
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f426dbf00eace23da2f26eb50dd9675fe22ed445
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914763"
---
# <a name="create-a-consignment-replenishment-order"></a>Oprette en genopfyldningsordre til konsignation

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emne forklarer, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager. Det viser også, hvordan du registrerer modtagelse af produkter, så konsignationslageret registreres som disponibel lagerbeholdning, der ejes af leverandøren. Denne procedure vil normalt ske via en indkøber. Du kan bruge denne guide i USMF-demodatafirmaet. Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

## <a name="create-a-consignment-replenishment-order"></a>Oprette en genopfyldningsordre til konsignation
1. Gå i navigationsruden til **Moduler > Indkøb og forsyning > Konsignation > Genopfyldningsordrer til konsignation**.
2. Vælg **Ny**.
3. I feltet **Kreditorkonto** skal du vælge kreditor **US-104** (du skal vælge en kreditor, der er registreret som ejer på siden **lagerejere**). 
4. Vælg **OK**.
5. Vælg **Tilføj linje**.
6. I feltet **varenummer** skal du skrive `M9211CI` (du skal vælge en vare, der er oprettet til konsignationslager).
7. Angiv et tal i feltet **Antal**.
8. Angiv en dato i feltet **Ønsket leveringsdato**. De ønskede og bekræftede datoer, der bruges af MRP-programmet for den forventede ankomst af varer.  
9. Angiv en dato i feltet **Bekræftet leveringsdato**.
10. Vis eller skjul sektionen **Linjedetaljer**.
11. Vælg fanen **Lagerdimensioner**.
12. Opdater siden for at få vist ejeren i feltet **Ejer af lagerdimensioner**. Leverandør US-104 er nu anført som ejer.  

## <a name="check-the-inventory-transaction-status"></a>Kontroller lagerposteringsstatussen
1. Vælg **Lager**.
2. Vælg **Transaktioner**.
3. Bemærk, at feltet **Modtagelse** er indstillet til **Bestilt** i den ønskede række.  
4. Luk siden.

## <a name="receive-items"></a>Modtag varer
1. Vælg **Produktkvittering**.
2. Skriv en værdi i feltet **Ekstern produktkvittering**.
3. Skriv et tal i feltet **Antal**, der er lavere end det tal, der vises der. 
4. Vælg **OK**.

## <a name="check-the-on-hand-inventory"></a>Kontroller lagerbeholdningen
1. Vælg **Lager**.
2. Vælg **Disponibelt lager**.
3. Vælg **Oversigt**. De varer, der er modtaget som konsignationslager, der ejes af leverandøren, er disponible. Det resterende antal på genopfyldningsordren til konsignation vises i feltet **Bestilt i alt**.  
4. Luk siden.

