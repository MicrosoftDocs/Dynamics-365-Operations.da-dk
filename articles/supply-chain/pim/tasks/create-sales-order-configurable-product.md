---
title: Oprette en salgsordre for et konfigurerbart produkt
description: Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570579"
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