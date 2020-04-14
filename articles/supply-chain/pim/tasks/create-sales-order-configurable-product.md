---
title: Oprette en salgsordre for et konfigurerbart produkt
description: Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cafd6e01800b55f316179c481aaa110b2cbcbc80
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150027"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Oprette en salgsordre for et konfigurerbart produkt

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre. I dette eksempel bruges modellen D0006-højttaler i demodatafirmaet USMF. En salgsordrebehandler bruger normalt denne procedure.


## <a name="create-a-sales-order"></a>Oprette en salgsordre
1. Klik på Salgsordrebehandling og -forespørgsel.
2. Klik på Ny.
3. Klik på Salgsordre.
4. Vælg US-001 i feltet Debitorkonto. 
5. Klik på OK.
6. I feltet Varenummer skal du vælge D0006.
    * Til denne opgave skal du vælge et produkt, der kan konfigureres.  
7. Klik på Produkt og forsyning.
8. Klik på Konfigurer linje.
    * Bemærk, at prisen er ændret, baseret på den konfiguration, der blev valgt, og at feltet Medtag kabel nu er angivet til Sand.  
    * Bemærk standardprisen og de indstillinger, der er valgt til kablet.  
9. Klik på Indlæs skabelon..
    * Dette eksempel viser, hvordan du kan bruge en skabelon til at vælge en foruddefineret konfiguration. Hvis du bruger denne procedure som en opgaveguide, og du ønsker at se de andre attributværdier, der er tilgængelige, skal du klikke på knappen Lås op.  
10. Klik på OK.
11. Klik på OK.
12. Vis eller skjul sektionen Linjedetaljer.
13. Klik på fanen Produkt.
    * Konfigurationen af varen vises nu under produktdimensionerne.  
14. Luk siden.

## <a name="select-the-product-configuration"></a>Vælg produktkonfigurationen.

