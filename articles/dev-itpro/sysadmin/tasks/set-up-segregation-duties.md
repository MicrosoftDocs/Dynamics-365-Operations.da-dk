--- 
title: Konfigurer opdeling af opgaver
description: "Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-segregation-of-duties"></a>Konfigurer opdeling af opgaver

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere. Dette begreb kaldes opdeling af opgaver. Du ønsker f.eks. ikke, at den samme person både skal bekræfte modtagelsen af varer og behandle betalingen til kreditoren. Opdeling af opgaver hjælper dig med at mindske risikoen for svig og også med at registrere fejl eller uregelmæssigheder. Du kan også bruge opdeling af opgaver til at gennemtvinge politikker for intern kontrol. Fuldfør følgende procedure for at oprette en regel. Du skal være systemadministrator for at kunne fuldføre proceduren. Det demodatafirma, der bruges til at oprette denne procedure, er DAT. 

1. Gå til Systemadministration > Sikkerhed > Opdeling af opgaver > Regler for opdeling af opgaver.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
    * Angiv et navn til reglen.  
4. Klik på rullelisten i feltet Første opgave for at åbne opslaget.
5. Find og vælg den ønskede post på listen.
    * Vælg den første programadgangsrettighed, der styres af reglen.  
6. Klik op linket i den valgte række på listen.
7. Klik på rullelisten i feltet Anden opgave for at åbne opslaget.
8. Find og vælg den ønskede post på listen.
    * Vælg den anden programadgangsrettighed, der styres af reglen.  
9. Klik op linket i den valgte række på listen.
10. Vælg en indstilling i feltet Alvorsgrad.
    * Vælg alvorligheden af den risiko, der forekommer, når den samme bruger eller rolle udfører begge opgaver.  
11. Indtast en værdi i feltet Sikkerhedsrisiko.
    * Angiv en beskrivelse af sikkerhedsrisikoen.  
12. Indtast en værdi i feltet Sikkerhedsmitigering.
    * Angiv en beskrivelse af de handlinger, du udfører for at reducere sikkerhedsrisikoen. Du kan f.eks. mindske risikoen ved at foretage en mere detaljeret gennemgang af processen, ved at gennemføre en månedlig evaluering på lederniveau eller ved at dele ressourcer med andre afdelinger.  
13. Klik på Gem.


