---
title: Oprette salgsordrefakturaer
description: Denne artikel beskriver, hvordan du kan fakturere en salgsordre, herunder fletning af fakturaer og batchbehandling.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ff76eac54da6621d999d9b629fac920ba8de294
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778378"
---
# <a name="create-sales-order-invoices"></a>Oprette salgsordrefakturaer

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du kan fakturere en salgsordre, herunder fletning af fakturaer og batchbehandling. Denne procedure bruger demofirmaet USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Opret en faktura fra en salgsordre.
1. Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Salgsordrer, der er afsendt men ikke faktureret**.
2. Vælg en salgsordre på listen. 
3. Klik på **Faktura > Generér > Faktura** i **handlingsruden**. Bemærk, at denne salgsordre har flere tilknyttede følgesedler. Den viser kun ordet *flere* i stedet for nummeret på følgesedlen.  
4. Udvid sektionen **Parametre**.
    - Bogføring skal være angivet til **Ja** for at bogføre fakturaen. Du kan også deaktivere bogføring og bare udskrive fakturaen. Du kan dog opnå det samme resultat ved at oprette en proformafaktura i stedet for en faktura.  
    - Denne indstilling anvendes til batchjob. Forespørgslen køres, når batchjobbet køres.
5. Vælg **Efter** i feltet **Udskriv**.
6. Vælg **Ja** for **Udskriv faktura**. Udskriftsstyring kan udskrive flere kopier af fakturaen og også sende fakturaen via email som en PDF-fil.  
7. Vælg **Opsummer** i feltet **Udskriv gebyrer**.
8. Vælg **Saldo** i feltet **Kontrollér kreditmaks**.
9. Klik på **Annuller**.

## <a name="combine-orders-into-a-single-invoice"></a>Kombinere ordrer i én enkelt faktura
1. Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Alle salgsordrer**.
2. Find en debitor, der har flere fakturaer, der er åbne.
3. Vælg flere åbne salgsordrer fra samme kunde.
4. Klik på **Faktura > Generér > Faktura** i **handlingsruden**.
5. Udvid sektionen **Parametre**.
6. Vælg **Alle**" i feltet **Antal**. Bemærk, at der er vist to fakturaer oversigtsafsnittet. Nu vi flette dem til en enkelt faktura.  
7. Vælg **Fakturakonto** i feltet **Samleopdatering for**.
8. Klik på **Arranger** for at flette salgsordrerne til en enkelt faktura. De to salgsordrer er nu flettet i én faktura.   
9. Klik på **Annuller**.
10. Klik på **Ja**.

## <a name="post-invoices-in-a-batch"></a>Bogføre fakturaer i et batch
1. Gå til **Navigationsrude > Moduler > Debitor > Fakturaer > Batchfakturering > Faktura**.
2. Klik på **Vælg**.
3. Klik på **OK**.
4. Klik på **Batch**.
5. Vælg **Ja** for **Batchbehandling**.
6. Klik på **Gentagelse**.
7. Vælg **Dage**.
8. Klik på **OK**.
9. Klik på **OK**.
10. Klik på **Annuller**.
11. Klik på **Ja**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
