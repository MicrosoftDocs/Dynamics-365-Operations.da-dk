---
title: Foretage fejlfinding af problemer ved opsætning og installation af Store Commerce
description: Denne artikel forklarer, hvordan du kan fejlfinde konfigurations- og installationsproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 92d4a9d78485b681b4e802f695d54f44ecd7c5de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870460"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Foretage fejlfinding af problemer ved opsætning og installation af Store Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikel forklarer, hvordan du kan fejlfinde konfigurations- og installationsproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Jeg kan ikke aktivere appen, og jeg modtager en fejlmeddelelse for forbindelse

Når du har indtastet den gyldige CPOS-URL-adresse (Sky Point of Sale), kan du få vist en fejlmeddelelse for forbindelse, der ligner følgende eksempel:

> Der er opstået en forbindelsesfejl, og enheden kan ikke oprette forbindelse til CPOS. Der kan være problemer med den URL-adresse, der er skrevet til CPOS.

I dette tilfælde skal du gennemse URL-adressen for numeriske fejl eller finde ud af, om CPOS ikke kan nås, fordi den er offline.

Kontrollér desuden, at CSU-versionen (Sky Scale Unit) 10.0.25 (9.35.\*.\*) eller senere. CPOS version 10.0.25 eller senere skal bruges Store Commerce.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Jeg kan ikke installere appen, fordi Modern POS allerede er installeret

Du kan få vist følgende fejlmeddelelse under installationen:

> Der er tidligere blevet installeret en version (9.\*.\*.\*) af dette produkt (Modern POS) via det tidligere installationsprogram.

For at rette fejlen skal du afinstallere MPOS-appen (Modern Point of Sale) for alle brugere på maskinen og derefter prøve igen. Du kan bekræfte, om MPOS er blevet fjernet for alle brugere ved at køre følgende PowerShell-kommando.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Jeg kan ikke aktivere appen på grund af en ugyldig URL-adresse eller en fejltilstand

Hvis den CPOS-URL-adresse, du har angivet, ikke er gyldig, og du vil ændre den, eller hvis Store Commerce-appen er i fejltilstand under aktiveringen, kan du genstarte processen ved at nulstille appen. I Store Commerce gemmes kun en gyldig URL-adresse til CPOS.

Hvis du vil nulstille Store Commerce-appen, skal du følge disse trin.

1. I Windows-menuen **Start** skal du markere og holde (eller højreklikke) på appen og derefter vælge **Mere \> App-indstillinger**.
2. Rul ned siden med appindstillinger, indtil du finder knappen **Nulstil**.
3. Vælg **Nulstil**. Når du bliver bedt om at bekræfte, at du vil nulstille appen, skal du vælge OK.
