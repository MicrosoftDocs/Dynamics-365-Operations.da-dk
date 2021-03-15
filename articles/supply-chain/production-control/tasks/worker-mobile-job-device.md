---
title: Konfigurere en arbejder ved hjælp af den mobile jobenhed
description: I dette emne beskrives, hvordan du tildeler de korrekte roller til brugerkontoen for en arbejder og derefter gør det muligt for arbejderen at foretage shop floor-registreringer.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89b75936ea9c0f25f82175a1871088da8fd74ad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980925"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigurere en arbejder ved hjælp af den mobile jobenhed

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du tildeler de korrekte roller til brugerkontoen for en arbejder og derefter gør det muligt for arbejderen at foretage shop floor-registreringer.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Kontroller, at en arbejder er tildelt en bestemt rolle

I dette eksempel skal du kontrollere, at brugeren "SHANNON" er tildelt rollen maskinoperatør, før du konfigurerer arbejderens konto.

1. Gå til **Navigationsrude > Moduler > Systemadministration > Brugere > Brugere**.
2. Søg efter en bruger i quick-filteret. Skriv eksempelvis `shannon`.
3. Vælg linket i kolonnen **Bruger-ID** for den brugerkonto, der vises.
4. Vælg træet **Brugerens roller** og dernæst **Roller > Maskinoperatør**.
5. Luk siderne **Brugeroplysninger** og **Brugere** for at vende tilbage til startsiden.

## <a name="configure-worker-account"></a>Konfigurer arbejderkonto
1. Gå til **Navigationsrude > Moduler > Personale > Arbejdere >** Arbejdere.
2. Søg efter en bruger i quick-filteret. Skriv eksempelvis `shannon`.
3. Vælg linket i kolonnen **Navn** for den brugerkonto, der vises.
4. Vælg fanen **Tidsregistrering**.
5. Vælg **Aktivér på registreringsterminaler**.
6. Indtast eller vælg værdier i følgende felter:  

    - **Beregningsgruppe**  
    - **Standardberegningsgruppe**  
    - **Godkendelsesgruppe**  
    - **Standardprofil**  
    - **Profilgruppe**  

7. Vælg **OK**.
8. Vælg **Rediger** for at angive et kortnummer for den nye tidsregistreringsarbejder. Indtast en værdi i feltet **Kort-ID**.
9. Vælg **Gem**.
10. Luk siderne **Detaljer om arbejder** og **Arbejdere**.

## <a name="assign-worker-to-device-group"></a>Tildel arbejder til enhedsgruppe
1. Gå til **Produktionsstyring > Opsætning > Produktionsudførelse > Konfigurer jobkort for enheder**.
2. Vælg **Tilføj**.
3. Vælg den ønskede arbejder på listen. Vælg i dette eksempel **SHANNON**.
4. Vælg **OK**.
5. Vælg **Rediger**.
6. Du kan angive standardfilteret for arbejderen i feltet **Produktionsenhed**. Dette sikrer, at kun produktionsjob for den valgte produktionsenhed vises, når arbejderen logger på enheden. Indtast den ønskede værdi.
7. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]