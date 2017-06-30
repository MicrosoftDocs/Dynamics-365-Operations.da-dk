---
title: Konfigurer konsignation
description: "Dette emne forklarer, hvordan du konfigurerer indgående konsignationslageroperationer."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b8692a3033cd665402721ea18ba8c28557c049de
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-consignment"></a>Konfigurer konsignation

[!include[banner](../includes/banner.md)]


Dette emne forklarer, hvordan du konfigurerer indgående konsignationslageroperationer. 

Konsignationslager er lager, der ejes af en leverandør, men lagret på dit sted. Når du er klar til at forbruge eller bruge af lageret, overtager du ejerskabet af lageret. I dette emne beskrives den opsætning, der er nødvendig for at aktivere konsignationsprocesser. Yderligere oplysninger om konsignationsprocesser findes under [Konsignation](consignment.md).

## <a name="inventory-owners"></a>Lagerejere
For at registrere fysisk indgående konsignationslager skal du definere en leverandørejer. Dette gøres på siden **Lagerejer**. Når du vælger en **kreditorkonto**, oprettes standardværdier for felterne **Navn** og **Ejer**. Værdien i feltet **Ejer** vil være synlig for leverandøren, så kan du ændre den, hvis dine kontonavne for kreditorer ikke er let for eksterne personer at genkende. Det er muligt at redigere feltet **Ejer**, men kun indtil tidspunktet, når du gemmer posten **Lagerejer**. Feltet **Navn** udfyldes med navnet på den part, der er tilknyttet kreditorkontoen, og dette kan ikke ændres. 

[![lagerejere](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Sporingsdimensionsgruppe
Varer, der skal bruges i konsignationsprocesser, skal være tilknyttet en **sporingsdimensionsgruppe**, hvor dimensionen **Ejer** er sat til **Aktiv**. Ejerdimensionen har altid **Fysisk lager** og **Økonomisk lager** som valgte indstillinger. **Disponer pr. dimension** er aldrig markeret. 

[![sporingsdimensionsgruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Ændringskladde for beholdningsejerskab
Kladden **Ændring af beholdningsejerskab**bruges til at registrere overdragelse af ejendomsretten til konsignationslager fra leverandøren til den juridiske enhed, der bruger den. Det skal være identificeret med et lagerkladdenavn som enhver lagerkladde. Disse navne oprettes på siden **Lagerkladdenavne**, og **Kladdetype** skal være indstillet til **Ændring af ejerskab**. 

[![ændringskladde for beholdningsejerskab](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Leverandørsamarbejde i konsignationsprocesser
Hvis dine kreditorer bruger leverandørsamarbejde som interface, kan de bruge dette til at overvåge forbruget af lageret på dit sted. Yderligere oplysninger om opsætning af leverandører til leverandørsamarbejde findes i [Konfiguration af sikkerhed for brugere af leverandørsamarbejde](../procurement/configure-security-vendor-portal-users.md).




