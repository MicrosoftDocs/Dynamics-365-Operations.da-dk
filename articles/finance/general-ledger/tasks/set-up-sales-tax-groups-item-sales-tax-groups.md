---
title: Konfigurere momsgrupper og varemomsgrupper
description: Denne opgaveregistrering fører dig gennem konfigurationen af moms- og varemomsgrupper.
author: twheeloc
manager: AnnBe
ms.date: 07-01-2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b539129e62b9b0b10df1f505cbfec5c1143138
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141620"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>Konfigurere momsgrupper og varemomsgrupper

[!include [banner](../../includes/banner.md)]

Denne opgaveregistrering fører dig gennem konfigurationen af moms- og varemomsgrupper. Momsgrupper er grupper med momskoder, der er tilknyttet debitorer og kreditorer. De er også tilknyttet finanskonti for posteringer, der ikke er bogført for en bestemt kreditor eller debitor.  Varemomsgrupper er grupper af momskoder, der er knyttet til ressourcer som produkter.  Den momssats, der gælder for en bestemt postering, fastlægges af momskoden, som findes i momsgruppen og i varemomsgruppen for posteringen.  Der kan kun beregnes moms, hvis der er valgt en momsgruppe og en varemomsgruppe for hver postering, hvor der skal beregnes eller registreres moms.  

1. Gå til **Navigationsrude > Moduler > Skat > Indirekte skatter > Moms > Momsgrupper**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Momsgruppe**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Slå udvidelsen af sektionen **Opsætning** til/fra.
6. Klik på **Tilføj**.
7. Markér den valgte række på listen.
8. Klik på rullelisten i feltet **Momskode** for at åbne opslaget.
9. Klik op linket i den valgte række på listen.
10. Klik på **Gem**.
11. Luk siden.
12. Gå til **Moms > Indirekte skatter > Moms > Momsgrupper**.
13. Klik på **Ny**.
14. Skriv en værdi i feltet **Varemomsgruppe**.
15. Indtast en værdi i feltet **Beskrivelse**.
16. Klik på **Tilføj**.
17. Markér den valgte række på listen.
18. Klik på rullelisten i feltet **Momskode** for at åbne opslaget.
19. Klik op linket i den valgte række på listen.
20. Klik på **Gem**.

