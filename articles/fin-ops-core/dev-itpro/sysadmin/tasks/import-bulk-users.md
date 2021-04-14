---
title: Importere brugere fra Azure Active Directory
description: Systemadministratorer kan bruge denne procedure til at importere valgte brugere manuelt eller til at importere et stort antal brugere fra Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745783"
---
# <a name="import-users-from-azure-active-directory"></a>Importere brugere fra Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Importere valgte brugere

Systemadministratorer kan bruge denne procedure til at importere et valgte brugere fra Azure Active Directory (Azure AD).

1. Brugeren importeres med det aktuelle sessionsfirma som standardfirma. Du skal ændre det aktuelle firma, hvis det er relevant, før du importerer brugere.
2. Gå til **Systemadministration > Brugere > Brugere**.
3. Klik på **Importér brugere**.
4. Vælg de brugere, der skal importeres, og vælg **Importér brugere**.

Når importen er fuldført, skal du tildele roller til brugere.

## <a name="import-users-in-bulk"></a>Masseimportere brugere

Systemadministratorer kan bruge denne procedure til at importere et stort antal brugere fra Azure Active Directory.
Bemærk, at det ikke er muligt at vælge brugere, når du bruger indstillingen Batchimport.

## <a name="run-the-import-as-a-batch-job"></a>Køre importen som et batchjob
1. Brugeren importeres med det aktuelle sessionsfirma som standardfirma. Du skal ændre det aktuelle firma, hvis det er relevant, før du importerer brugere.
2. Gå til **Systemadministration > Brugere > Brugere**.
3. Klik på **Batchimport**.
4. Udvid sektionen **Kør i baggrunden**.
4. Vælg **Ja** i feltet **Batchbehandling**.
6. Indtast eller vælg en værdi i feltet **Batchgruppe**. Dette trin er valgfrit.  
7. Vælg **Ja** i feltet **Privat**. Dette trin er valgfrit.  
8. Vælg **Ja** i feltet **Kritisk job**. Dette trin er valgfrit.  
9. Vælg en indstilling i feltet **Overvågningskategori**.
10. Klik på **OK**.

Når importen er fuldført, skal du tildele roller til brugere.

## <a name="run-in-a-sandbox-environment"></a>Køre i et sandkassemiljø
1. Vælg **Batchimport**.
2. Vælg **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]