---
title: Nyheder eller ændringer i Dynamics 365 Human Resources fra den 9. august 2021
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 9. august 2021.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 58926e5a6c1476db84fa41945dc92196eb24f4bf
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068448"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources fra den 9. august 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives funktioner, der enten er nye, ændrede eller kommer snart i Microsoft Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4393.

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis denne artikel til at omfatte fejlrettelser, som blev udført i buildet, efter at denne artikel blev udgivet.

| Fejlnummer | Problem | Beskrivende tekst |
| --- | --- | --- |
| 558385 | Når indstillingen **Vælg automatisk udvalgte modtagere** er aktiveret for standardudpegede, vælges den standardudpegede ikke. | Dette problem er nu løst. Der vælges automatisk flere standardudpegede i berettigede planer, når indstillingen **Vælg automatisk udpegede modtagere** på siden **Delte Human Resources-parametre** er aktiveret. |
| 589617 | På siden **Fridag** er saldi for **Tilgængelig for køb** og **Tilgængelig for salg** tomme, når adgangen er begrænset til et bestemt firma. | Dette problem er nu løst. På siden **Fridag** vises de rette saldi for **Tilgængelig for køb** og **Tilgængelig for salg**, når brugeren er begrænset til et bestemt firma. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering eller deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md)|
| Give en fraværsadministrator mulighed for at administrere orlov | [Give en fraværsadministrator mulighed for at administrere orlov](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | I denne version opdaterer vi visningen af arbejdsområdet for fraværsadministrator. Du kan finde flere oplysninger under [Konfigurere fraværschefrolle](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Konfigurere krav om vedhæftet fil pr. orlovstype | [Konfigurere krav om vedhæftet fil pr. orlovstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurere orlovs- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Konfigurer orlovsenheder pr. orlovstype | [Konfigurer orlovsenheder pr. orlovstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurere orlovs- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt | [Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til at betale](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Kommer snart

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Detaljer |
| --- | --- |
| Platform update 10.0.21 (45) | Udrulning af platformsopdatering 10.0.21 er planlagt til at starte med servicefrigivelse den 4. oktober 2021. Du kan få mere at vide i [Platformsopdateringer til version 10.0.21 af programmer til finans og drift (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

