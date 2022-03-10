---
title: Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet
description: Dette emne beskriver, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre.
author: Mirzaab
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d641ece709d36d8f3ee29cde47918154835a5bb9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572931"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]