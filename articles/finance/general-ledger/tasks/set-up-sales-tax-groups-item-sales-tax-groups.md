---
title: Konfigurere momsgrupper og varemomsgrupper
description: Denne opgaveregistrering fører dig gennem konfigurationen af moms- og varemomsgrupper.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e97766be1207fb66b38f25b1e423fb21cec9e726
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222161"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]