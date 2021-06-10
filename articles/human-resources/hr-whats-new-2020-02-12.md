---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (12. februar 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 12. februar 2020.
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6cae0d3f59b1b0d01f3b2f6cf3469520e35d2f91
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051206"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (12. februar 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.2867. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Eksisterende enheder CompFixedEmpls og HcmPersonImage skal være tilgængelige fra OData (414178)

Med denne uges udgivelse er enhederne **CompFixedEmpls** og **HcmPersonImage** offentlige og tilgængelige via ODAta.

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>Slet ansættelse fra Dataverse virker ikke, når oplysninger om ansættelse ikke er aktive (403193)

Denne ændring giver dig nu mulighed for at slette ansættelser via Dataverse, når der ikke findes nogen aktive ansættelsesoplysninger.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Arbejdsgang for kursusregistrering ændrer status til fuldført og fejl efter anden godkendelse (409749)

Arbejdsgangen for kursusregistrering er blevet opdateret, så der er mulighed for flere godkendere.

## <a name="in-preview"></a>Som eksempel

Følgende prøvefunktioner er tilgængelige den 3. februar 2020:

- **Visningsfunktioner for orlov og fravær** - Du kan finde flere oplysninger under [Visningsfunktioner for orlov og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Prøveversionsfunktion: Administration af frynsegoder** – Der er flere oplysninger, herunder kendte problemer, under [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Kommer snart

### <a name="platform-update-32"></a>Platform update 32 

Platform update 32 vil snart være tilgængelig. [Få flere oplysninger om Platform update 32 her](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

### <a name="updated-dataverse-solution"></a>Opdateret Dataverse-løsning

Der vil snart være en ny Dataverse-løsning med følgende ændringer:

| Beskrivelse | Forskydning |
| ----------------------------------------- | --- |
| Ændringer i objektet **Job/Stilling** | **Kompensationsområde** er tilføjet</br>**Økonomiske dimensioner** er tilføjet |
| Ændringer i objektet **Arbejder** | **Navnerækkefølge** er tilføjet</br>**Arbejder hjemmefra** er tilføjet</br>**Sprog** er tilføjet</br>**Anciennitetsdato** er tilføjet</br>**Jubilæumsdato** er tilføjet</br>**Oprindelig ansættelsesdato** er tilføjet |
| Ændringer af objektet **Ansættelse** | **Økonomiske dimensioner** er tilføjet</br>**Årsag til fratrædelse** er tilføjet</br>**Fratrædelsesdato** er omdøbt fra **Overførselsdato**</br>**Datoer for prøvetid** er tilføjet |
| Ændringer i objektet **Arbejders adresse** | **Gadenavn** er tilføjet</br>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** er markeret til udfasning |
| Nye konfigurationsobjekter til variabel kompensation | **Type af variabel kompensationsplan**</br>**Kompensation - variabel struktur**</br>**Fordelingsregler**</br>**Niveau i variabel kompensationsplan** |
| Nyt objekt **Arbejderkalender for ansættelse** | **Arbejdskalenderobjekt** er tilføjet |
| Nyt objekt **Lønoplysninger for stillinger** | **Lønoplysninger for stillinger** er tilføjet |
| Nyt objekt **Titel** | **Titel** er tilføjet. Den nye enhed **Titel** vil blive medtaget i synkroniseringsprocessen mellem Human Resources og Dataverse. Der henvises ikke til den først i enhederne **Stilling** eller **Job**. |

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]