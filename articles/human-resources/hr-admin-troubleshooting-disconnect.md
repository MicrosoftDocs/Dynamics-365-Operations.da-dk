---
title: Klient afbryder forbindelsen
description: I denne artikel beskrives det, hvad du skal gøre, hvis kundens forbindelse til det lokale miljø afbrydes, og kunden ikke kender årsagen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.article: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73f0c31d5153a82651ed77aa37bc10966ce7c9b1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008458"
---
# <a name="client-disconnects"></a>Klient afbryder forbindelsen

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

Microsoft Dynamics 365 Human Resources afbryder brugerne, når to forskellige sessioner er åbne på samme tid for den samme bruger, og den samme browsertype. (F.eks. har bruger A åbnet både miljø 1 og miljø 2 i Chrome). Det er ligegyldigt, om brugerne åbner andre browservinduer eller andre faner. Hvis de samme brugerlegitimationsoplysninger bruges til at logge på både miljø 1 og miljø 2 på samme tid og i samme browsertype, så afbryder Personale forbindelsen til en af sessionerne.

**Løsning**

Kontroller, at det kun ét miljø er åbent ad gangen for en bestemt browsertype. Brugerne kan åbne flere sessioner til det samme miljø (dvs. flere faner i den samme browser).

Brugere, som vil springe mellem to miljøer på samme tid, skal åbne de enkelte miljøer i hver sin browsertyper. (F.eks. kan bruger A få vist miljø 1 i Chrome og miljø 2 i Microsoft Edge).
