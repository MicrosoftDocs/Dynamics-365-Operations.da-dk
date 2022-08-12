---
title: Fejlfinde fejl i forbindelse med løsningsforståelse
description: Denne artikel indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6866956efcc76a7da6c3aa5fb36058de78d5472e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111292"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Fejlfinde fejl i forbindelse med løsningsforståelse

[!include [banner](../../includes/banner.md)]





Denne artikel indeholder fejlfindingsoplysninger for dobbeltskrivning mellem programmer til finans og drift og Dataverse. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.

> [!IMPORTANT]
> Nogle af de problemer, som denne artikel vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="error-on-the-dual-write-page"></a>Fejl på siden Dobbeltskrivning

På siden **Dobbeltskrivning** kan du få vist en fejlmeddelelse, der ligner følgende eksempel:

*Enheden med navnet 'msdyn\_dualwriteentitymap' med namemapping='Logical' blev ikke fundet i MetadataCache*.

Hvis du vil løse problemet, skal du sørge for, at Dobbeltskrivning-kerneløsningen er installeret i Dataverse. Dobbeltskrivning-kerneløsningen er en forudsætning for løsningsbevidsthed.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
