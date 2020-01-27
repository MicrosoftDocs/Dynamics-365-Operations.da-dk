---
title: Afbrudt forbindelse til Talent-klient
description: I dette emne beskrives, hvad du skal gøre, hvis kundens forbindelse til det lokale miljø afbrydes, og kunden ikke kender årsagen.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 02df31b56c0e960a16ec2aadd8b1e817e0b6ec65
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898451"
---
# <a name="talent-client-disconnects"></a>Afbrudt forbindelse til Talent-klient

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

Microsoft Dynamics 365 Talent afbryder brugerne, når to forskellige sessioner er åbne på samme tid for den samme bruger, og den samme browsertype. (F.eks. har bruger A åbnet både miljø 1 og miljø 2 i Chrome). Det er ligegyldigt, om brugerne åbner andre browservinduer eller andre faner. Hvis de samme brugerlegitimationsoplysninger bruges til at logge på både miljø 1 og miljø 2 på samme tid og i samme browsertype, så afbryder Talent forbindelsen til en af sessionerne.

**Løsning**

Kontroller, at det kun ét miljø er åbent ad gangen for en bestemt browsertype. Brugerne kan åbne flere sessioner til det samme miljø (dvs. flere faner i den samme browser).

Brugere, som vil springe mellem to miljøer på samme tid, skal åbne de enkelte miljøer i hver sin browsertyper. (F.eks. kan bruger A få vist miljø 1 i Chrome og miljø 2 i Microsoft Edge).
