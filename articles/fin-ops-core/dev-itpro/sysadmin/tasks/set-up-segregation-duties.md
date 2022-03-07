---
title: Konfigurer opdeling af opgaver
description: Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745735"
---
# <a name="set-up-segregation-of-duties"></a>Konfigurer opdeling af opgaver

[!include [banner](../../includes/banner.md)]

Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere. Dette begreb kaldes opdeling af opgaver. Du ønsker f.eks. ikke, at den samme person både skal bekræfte modtagelsen af varer og behandle betalingen til kreditoren. Opdeling af opgaver hjælper dig med at mindske risikoen for svig og også med at registrere fejl eller uregelmæssigheder. Du kan også bruge opdeling af opgaver til at gennemtvinge politikker for intern kontrol. Fuldfør følgende procedure for at oprette en regel. Du skal være systemadministrator for at kunne fuldføre proceduren.

1. Gå til **Systemadministration** > **Sikkerhed** > **Opdeling af opgaver** > **Regler for opdeling af opgaver**.
2. Klik på **Ny**.
3. Skriv en værdi for reglen i feltet **Navn**.
4. Klik på rullelisten i feltet **Første pligt** for at åbne opslaget.
5. Find og vælg den ønskede post på listen. Vælg den første programadgangsrettighed, der styres af reglen.
6. Klik på rullelisten i feltet **Anden pligt** for at åbne opslaget. 
7. Find og vælg den ønskede post på listen. Vælg den anden programadgangsrettighed, der styres af reglen.
10. Vælg en indstilling i feltet **Alvorsgrad**. Vælg alvorligheden af den risiko, der forekommer, når den samme bruger eller rolle udfører begge opgaver.  
11. Indtast en værdi i feltet **Sikkerhedsrisiko**. Angiv en beskrivelse af sikkerhedsrisikoen.  
12. Indtast en værdi i feltet **Sikkerhedsmitigering**. Angiv en beskrivelse af de handlinger, du udfører for at reducere sikkerhedsrisikoen. Du kan f.eks. mindske risikoen ved at foretage en mere detaljeret gennemgang af processen, ved at gennemføre en månedlig evaluering på lederniveau eller ved at dele ressourcer med andre afdelinger.     
13. Klik på **Gem**.

> [!IMPORTANT] 
> Overholdelse af reglerne for opdeling af opgaver kontrolleres ikke, når du opretter en regel. Du kan oprette en regel, der skaber en konflikt for eksisterende roller. Eksisterende brugerrolletildelinger kan også være i konflikt med den nye regel. Du skal validere overholdelsen af angivne standarder, når du har oprettet eller redigeret en regel. Yderligere oplysninger finder du i [Identificere og løse konflikter i opdeling af opgaver](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]