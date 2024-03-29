---
title: Starte en produktionsordre
description: Denne procedure viser, hvordan du starter en produktionsordre i produktionen.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa47510d84e5ee156d4f38a076ce17fad8359d147997349de023b64483d66160
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735129"
---
# <a name="start-a-production-order"></a>Starte en produktionsordre

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du starter en produktionsordre i produktionen. Tids- og materialeforbrug rapporteres i denne proces. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Dette er den femte procedure ud af syv, der beskriver produktionsordrelivscyklussen.


## <a name="start-a-production-order"></a>Starte en produktionsordre
1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
    * Vælg en produktionsordre, som har statussen Frigivet.  
2. Klik på Produktionsordre i handlingsruden.
3. Klik på Start.
    * På denne side kan du bekræfte start af produktionsordren.  
4. Klik på fanen Generelt.
5. I feltet Fra opr.nr. Nr. skal du skrive "10".
6. Vælg "Altid" i feltet Automatisk ruteforbrug.
7. Klik på afkrydsningsfeltet Bogfør rutekort nu.
8. Vælg "Altid" i feltet Automatisk styklisteforbrug.
9. Klik på afkrydsningsfeltet Bogfør plukliste nu.
10. Klik på afkrydsningsfeltet Udskriv plukliste nu.
11. Klik på OK.
    * Dette er den udskrevne plukliste, som viser de materialer, der er brugt til produktionsordren.  
12. Luk siden.

## <a name="validate-the-picking-list"></a>Valider pluklisten
1. Klik på Vis i handlingsruden.
2. Klik på Plukliste.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Klik på Rediger.
6. Angiv et nummer i feltet Forbrug.
7. Klik på Bogfør.
8. Klik på OK.
    * I pluklistejournalen bogføres de materialer, der forbruges af produktionsordren. Før du bogfører journalen, kan du foretage justeringer, hvis der er en forskel mellem den forkalkulerede mængde og den faktiske forbrugte mængde.  
9. Klik på fanen GridPanel.
10. Luk siden.

## <a name="verify-the-route-card-journal"></a>Bekræft rutekortjournalen
1. Klik på Vis i handlingsruden.
2. Klik på Rutekort.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Klik på Rediger.
6. Angiv et tal i feltet Timer.
7. Klik på Bogfør.
8. Klik på OK.
    * I rutekortkladden registreres den tid, der er brugt på de enkelte operationer. Antal gode og fejl kan også rapporteres.  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]