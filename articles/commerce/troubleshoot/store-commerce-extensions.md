---
title: Foretage fejlfinding af udvidelsesproblemer ved Store Commerce
description: Denne artikel forklarer, hvordan du kan foretage fejlfinding af udvidelsesproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269775"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Foretage fejlfinding af udvidelsesproblemer ved Store Commerce

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan foretage fejlfinding af udvidelsesproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.

## <a name="extensions-packages-arent-loaded"></a>Extensions-pakker er ikke indlæst

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Extensions-pakker vises ikke på siden POS \> Indstillinger

Commerce runtime (CRT) udløsere er muligvis ikke opdateret, så de indeholder udvidelsespakken, eller de implementeres ikke. Yderligere oplysninger finder du i [Commerce runtime (CRT) extensibility og triggere](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Extensions-pakker vises på siden POS \> Indstillinger, men de indlæste oplysninger er ikke indlæst

Bekræft, at udvidelserne findes i mappen **C:\\Programfiler\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Udvidelser**. Hvis pakkerne findes, skal der være en **POS**-mappe, der indeholder manifestet.

Hvis der ikke findes en **POS**-mappe, skal du bekræfte, at Store Commerce-projektet refererer korrekt til POS-udvidelsesprojektet. Valider stien til projektreferencen, og kontroller, at den findes. 

I følgende eksempelillustration har installationsprogrammet problemer med det udvidelsesprojekt, der refereres til.

![Projektreferencen til Store Commerce installer er ikke gyldigt.](media/ReferenceNotValid.png)

Hvis referencen til udvidelsesprojektet tilføjes korrekt, vil der ikke være nogen advarsels- eller afhængighedsforhold i installationsprojektet, som vist i følgende illustration af eksemplet nedenfor.

![Projektreferencen til Store Commerce installer er gyldigt.](media/ReferenceValid.png)
