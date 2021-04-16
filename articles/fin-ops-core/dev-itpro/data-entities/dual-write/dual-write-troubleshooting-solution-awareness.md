---
title: Foretage fejlfinding af problemer i forbindelse med løsningsbevidsthed
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 86dd8803f7560ea337f2452e9722fe0151466daf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748867"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Foretage fejlfinding af problemer i forbindelse med løsningsbevidsthed

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="error-on-the-dual-write-page"></a>Fejl på siden Dobbeltskrivning

På siden **Dobbeltskrivning** kan du få vist en fejlmeddelelse, der ligner følgende eksempel:

*Enheden med navnet 'msdyn\_dualwriteentitymap' med namemapping='Logical' blev ikke fundet i MetadataCache*.

Hvis du vil løse problemet, skal du sørge for, at Dobbeltskrivning-kerneløsningen er installeret i Dataverse. Dobbeltskrivning-kerneløsningen er en forudsætning for løsningsbevidsthed.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]