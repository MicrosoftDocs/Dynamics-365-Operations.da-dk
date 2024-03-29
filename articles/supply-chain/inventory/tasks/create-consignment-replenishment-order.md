---
title: Opret en genopfyldningsordre til konsignation
description: Denne artikel forklarer, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager.
author: yufeihuang
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a1d0a7d322b17d3d80dd9fade2b037dd148d9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859367"
---
# <a name="create-a-consignment-replenishment-order"></a>Opret en genopfyldningsordre til konsignation

[!include [banner](../../includes/banner.md)]

Denne artikel forklarer, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager. Det viser også, hvordan du registrerer modtagelse af produkter, så konsignationslageret registreres som disponibel lagerbeholdning, der ejes af leverandøren. Denne procedure vil normalt ske via en indkøber. Du kan bruge denne guide i USMF-demodatafirmaet. Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]