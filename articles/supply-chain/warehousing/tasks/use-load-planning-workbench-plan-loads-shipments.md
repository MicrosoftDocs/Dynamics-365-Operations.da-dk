---
title: Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet
description: Dette emne beskriver, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5e20eef8aa748bb64c6c14dd7e1d92ccf6592e0
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/10/2019
ms.locfileid: "1739059"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emne beskriver, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre. Som en forudsætning skal vi skal oprette salgsordren. Denne procedure er en del af det daglige arbejde for transportkoordinatoren. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-sales-order"></a>Oprette en salgsordre
1. Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Alle salgsordrer**.
2. Vælg **Ny**.
3. Vælg rullelisten i feltet **Kundekonto** for at åbne opslaget.
4. Vælg konto **US-004**.
5. Vælg **OK**.
6. Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.
7. Vælg vare **A0001**. **A0001** er aktiveret for transportstyring.  
8. Klik på rullelisten i feltet **Sted** for at åbne opslaget, og vælg derefter en vare.
9. Angiv et tal i feltet **Antal**.
10. Skriv i dette eksempel "24" i feltet **Lagerlokation**. Dette lagersted er aktiveret for transportstyring og avanceret lagerstedsstyring.  
11. Vælg **Gem**.
12. Luk siden.

## <a name="create-a-new-load"></a>Opret en ny belastning
1. Gå til **Navigationsrude > Moduler > Transportstyring > Planlægning > lastplanlægningspanelet**.
2. Vælg fanen **Salgslinjer**. Nu kan du opbygge belastningen for den salgsordre, som du lige har oprettet. Belastninger kan bygges baseret på udbud og efterspørgsel fra købsordrer, flytteordrer og salgsordrer.  
3. Klik på fanen **Udbud og efterspørgsel** i handlingsruden.
4. Vælg **Til ny last**.
5. Vælg feltet **Lastskabelons-Id** i rullelisten for at åbne opslaget. Lastskabelonen definerer det maksimale mål for vægt og volumen af den samlede belastning. For eksempel kan lastskabelonen repræsentere størrelsen af en container eller lastbil. Vælg en vare.
6. Vælg **OK**.

## <a name="rate-and-route-the-load"></a>Vurder og ruteplanlæg belastningen
1. Vælg **Bedømmelse og ruteplanlægning**.
2. Vælg **Panelet bedøm rute**.
3. Vælg **Bedøm butik**.
4. Find og vælg den ønskede post på listen.
5. Vælg **Tildel**.
6. Luk siden.

