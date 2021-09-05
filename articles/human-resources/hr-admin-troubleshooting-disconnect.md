---
title: Klient afbryder forbindelsen
description: Dette emne beskriver, hvad du skal gøre, hvis kundens forbindelse til det lokale miljø afbrydes.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f99731d4d0658ed6f06b9e6915237532601a0a1d
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413505"
---
# <a name="client-disconnects"></a>Klient afbryder forbindelsen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Miljøoplysninger** 

Dette problem kan opstå i alle miljøer.
 
**Symptom** 

Kundens forbindelse til det lokale miljø afbrydes, og kunden kender ikke årsagen. Kunden modtager en af følgende fejlmeddelelser:

- Din forbindelse er blevet afbrudt. Klik på Luk for at fortsætte med at arbejde.
- Du ser ud til at have mistet netværksforbindelsen. Klik på Prøv igen.

**Rødt flag**

Dette problem opstår ofte, når brugerne er i implementeringsstadiet, sammenligner oplysninger på tværs af produktions- og testmiljøer og glemmer, at de skifter fra den ene session til den anden. Hvis brugerne er på dette stadie, vil de højst sandsynligt opleve dette problem.

**Udsted** 

**Browsertyper:** Google Chrome, Internet Explorer og Microsoft Edge

Microsoft Dynamics 365 Human Resources afbryder brugerne, når to forskellige sessioner er åbne på samme tid for den samme bruger, og den samme browsertype. (F.eks. har bruger A åbnet både miljø 1 og miljø 2 i Chrome). Det er ligegyldigt, om brugerne åbner andre browservinduer eller andre faner. Hvis de samme brugerlegitimationsoplysninger bruges til at logge på både miljø 1 og miljø 2 på samme tid og i samme browsertype, så afbryder Human Resources forbindelsen til en af sessionerne.

**Løsning**

Kontroller, at det kun ét miljø er åbent ad gangen for en bestemt browsertype. Brugerne kan åbne flere sessioner til det samme miljø (dvs. flere faner i den samme browser).

Brugere, som vil springe mellem to miljøer på samme tid, skal åbne de enkelte miljøer i hver sin browsertyper. (F.eks. kan bruger A få vist miljø 1 i Chrome og miljø 2 i Microsoft Edge).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
