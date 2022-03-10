---
title: Foretage fejlfinding af problemer i forbindelse med løsningsbevidsthed
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f83a064bfc8896bdf76bcd38f9187ed0e1ea56cf
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062307"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Foretage fejlfinding af problemer i forbindelse med løsningsbevidsthed

[!include [banner](../../includes/banner.md)]





Dette emne indeholder fejlfindingsoplysninger for dobbeltskrivning mellem Finans- og driftsapps og Dataverse. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="error-on-the-dual-write-page"></a>Fejl på siden Dobbeltskrivning

På siden **Dobbeltskrivning** kan du få vist en fejlmeddelelse, der ligner følgende eksempel:

*Enheden med navnet 'msdyn\_dualwriteentitymap' med namemapping='Logical' blev ikke fundet i MetadataCache*.

Hvis du vil løse problemet, skal du sørge for, at Dobbeltskrivning-kerneløsningen er installeret i Dataverse. Dobbeltskrivning-kerneløsningen er en forudsætning for løsningsbevidsthed.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]