---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 12. juli 2021
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 12. juli 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4ebe5a6ae19d00b94247381c700ff21d31910fcac1968ab4f8a673f89ddd2f0f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782629"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 12. juli 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4353.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
|  Slå visning af Antal års tjeneste til/fra | |Denne funktion giver mulighed for at bruge forskellige datoer til at beregne antallet af leveår, som vises på siden **Strømlinet medarbejderindtastning** og siden **Personer**.  Det vil være tilgængeligt i [Human Resources-parametre](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Emne |  Betegnelse |
| --- | --- | --- |
| 595871 | Ruden Om i Human Resources har en ugyldig Dataverse-terminologi | Med omdøbning af Common Data Service til Dataverse er terminologien blevet opdateret på informationssiden for Microsoft Dynamics 365 Human Resources (**Hjælp & Support > Om**). |
| 598676 | Den strømlinede medarbejderindtastningsformular, der tilsidesætter opgave, kan give en fejl, når den bruges med Gemt visning| Hvis funktionen 'Strømlinet medarbejderpost' er aktiveret på siden **Arbejder**, kan programmet mislykkes, hvis det er angivet i den gemte visning til **Altid åben for redigering**. |
| 592344 |Sektionen for arbejderkompensation ifølge stilling skal være skrivebeskyttet, når styring af frynsegoder er aktiveret | Oplysninger om arbejderkompensation oprettes ved hjælp af tidligere funktioner for frynsegoder.  Når styring af frynsegoder er aktiveret, er felterne skrivebeskyttede. Når styring af frynsegoder er aktiveret, og **Skjul tidligere frynsegodeformularer** er angivet til **Ja** i delte personaleparametre, skjules fanen **Arbejderkompensation**. |
| 598617 | Aktiveringsfanen for formularen **HcmDiscuuan** giver en ubegrænset løkke, når tilpasningerne anvendes | Når **Altid åben for redigering** er aktiveret for visning af både gitter og detaljer, er den kode, der aktiverer fanen i den tilsidesatte opgavemetode, i strid med tilpasning af den styring, der skal have fokus, og der oprettes en ubegrænset løkke. |
| 593553 | Feltet Kladdedato i kladden Ydeevne vises i UTC-tid | Feltet **Kladdedato** for ydeevnekladder vises i UTC-tidszonen og ikke i den tidszone, der er defineret i systemdatoopsætningen, og dette medfører, at datoen er ugyldig for visse tidszoner. |
| 586930 | Åbningsaktiviteter for ydeevnemål åbner en helt anden post | Når funktionen 'Udvidet rapportvisning for ydeevnekladder' er aktiveret i Funktionsstyring, vil valg af ydeevnemålene for udvidede rapporter på fanen **Mit team** i **Medarbejderselvbetjening** åbne målene for en medarbejder i stedet for den valgte medarbejder. |
| 569959 |  Enheden HcmPositionWorkerAssignmentV2 tildeler ikke en arbejder til en stilling | Brugerne modtger en fejl, når der tilføjes en stillingstildelingspost via enheden, og udgivelse mislykkedes. |
| 582259 | VETS 4212-rapporten bruger formularen 2017 i stedet for 2020-formularen | Opdateret til 2020-format.  Hvis du vil indlæse det nye format, skal du gå til **Rapportkonfigurationer** og slette VETS-4212 i venstre kolonne. Gå til **Elektronisk rapportering – Lager – HR-ressourcer**, og vælg **Åben**.  Vælg **VETS-4212 PDF-udskrift**, og vælg derefter **Importér**.|


## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md)|
|  Give en fraværsadministrator mulighed for at administrere orlov | [Give en fraværsadministrator mulighed for at administrere orlov](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Konfigurere fraværsadministratorrolle](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Konfigurere krav om vedhæftet fil pr. orlovstype | [Konfigurere krav om vedhæftet fil pr. orlovstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurere orlovs- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Konfigurer orlovsenheder pr. orlovstype | [Konfigurer orlovsenheder pr. orlovstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurere orlovs- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt | [Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til at betale](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
| Platform update 10.0.20 (44) | Platformsopdatering 10.0.20 er planlagt til at starte udrulning med servicefrigivelse den 26. juli 2021. Få flere oplysninger under [Platformsopdateringer for version 10.0.20 af Finance and Operations-apps (august 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
