---
title: Oprette og behandle en overensstemmelse
description: Dette emne forklarer, hvordan du udfører uoverensstemmelsesstyring baseret på en eksisterende kvalitetsordre.
author: perlynne
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4f7e61adf37e74bdb082270b689cf0375ccc7f7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833947"
---
# <a name="create-and-process-a-conformance"></a>Oprette og behandle en overensstemmelse

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du udfører uoverensstemmelsesstyring baseret på en eksisterende kvalitetsordre. Du kan køre denne registrering i demofirmaet USMF, og du kan bruge de foreslåede værdier. Denne procedure udføres typisk af en kvalitetsmedarbejder.  Som en forudsætning skal du følge instruktionerne i [Inspicere varers kvalitet](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md). For at behandle godkendelse af en uoverensstemmelse skal den bruger, der kører opgavregistreringen, have en "Navn"-værdi tildelt på siden Brugere. For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.


## <a name="select-a-quality-order"></a>Vælg en kvalitetsordre
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Periodiske opgaver > Kvalitetsstyring > Kvalitetsordrer.**
2. Vælg på listen den kvalitetsordre, der blev oprettet i [Inspicere varers kvalitet](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>Oprette en uoverensstemmelse
1. Gå til Handlingsrude, og vælg **Forespørgsler**.
2. Vælg **Uoverensstemmelser**.
3. Vælg **Ny**.
4. Vælg det problem, der blev fundet i inspektionsprocessen, i rullemenuen til feltet **Problemtype**.  
5. Vælg **OK**.

## <a name="approvereject-a-nonconformance"></a>Godkende/afvise en uoverensstemmelse
1. Vælg **Funktioner**.
2. Vælg **Godkend uoverensstemmelsen**. I dette eksempel skal du godkende uoverensstemmelsen. Godkendte uoverensstemmelser kan være tilknyttet relaterede operationer for at registrere arbejde, der udføres som en del af håndteringen af uoverensstemmelsen og, som i dette emne, behandlingen af korrektionshåndtering.  
3. Vælg **Ja**.

## <a name="create-a-correction-action"></a>Opret en korrektionshandling
1. Vælg **Rettelser**.
2. Vælg **Ny**.
3. Vælg den ønskede post fra rullemenuen i feltet **Personalenummer** i den nye række.
4. Klik på **Vælg**.
5. Vælg **Vedhæft**. Oprette en note om korrektionen. I dette eksempel er handlingen at kontakte leverandøren for at diskutere uoverensstemmelsen.  
6. Vælg **Ny**.
7. Vælg **Note**. Afhængigt af opsætningen af rapporten kan forskellige dokumenttyper udskrives på de rapporter, der er relateret til uoverensstemmelsesstyring.  
8. Indtast en værdi i feltet **Beskrivelse**.
9. Luk siden.

## <a name="maintain-a-correction"></a>Vedligehold en korrektion
1. Vælg **Markér som fuldført**.
2. Vælg **OK**.
3. Luk siden.

## <a name="close-a-nonconformance"></a>Luk en uoverensstemmelse
1. Vælg **Funktioner**.
2. Vælg **Luk uoverensstemmelsen**.
3. Vælg **Ja**.
4. Luk siderne.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]