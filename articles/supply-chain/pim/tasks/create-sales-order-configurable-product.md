---
title: Oprette en salgsordre for et konfigurerbart produkt
description: Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921283"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Oprette en salgsordre for et konfigurerbart produkt

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre. I dette eksempel bruges modellen D0006-højttaler i demodatafirmaet USMF. En salgsordrebehandler bruger normalt denne procedure.

## <a name="create-a-sales-order"></a>Oprette en salgsordre

1. Gå til **Salg og marketing \> Arbejdsområder \> Salgsordrebehandling og -forespørgsel**.
1. Vælg **Ny**.
1. Vælg **Salgsordre**.
1. Vælg **US-001** i feltet *Debitorkonto*. 
1. Vælg **OK**.
1. Vælg **D0006** i feltet *Varenummer*.
    * Til denne opgave skal du vælge et produkt, der kan konfigureres.  
1. Vælg **Produkt og forsyning**.
1. Vælg **Konfigurer linje**.
    * Bemærk, at prisen er ændret, baseret på den valgte konfiguration, og at feltet **Medtag kabel** nu er angivet til *Sand*.  
    * Bemærk standardprisen og de indstillinger, der er valgt til kablet.  
1. Vælg **Indlæs skabelon**.
    * Dette eksempel viser, hvordan du kan bruge en skabelon til at vælge en foruddefineret konfiguration. Hvis du bruger denne procedure som en opgaveguide, og du ønsker at se de andre attributværdier, der er tilgængelige, skal du vælge knappen **Lås op**.  
1. Vælg **OK**.
1. Vælg **OK**.
1. Vis eller skjul sektionen **Linjedetaljer**.
1. Vælg fanen **Produkt**.
    * Konfigurationen af varen vises nu under produktdimensionerne.  
1. Luk siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]