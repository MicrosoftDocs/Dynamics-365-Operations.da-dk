---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (3. marts 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 3. marts 2020.
author: Darinkramer
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d6f6f4a32e4bf85908f51eb1eed858b704c814dc
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526835"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (3. marts 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.2955. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service-løsning er nu tilgængelig med følgende ændringer:

Der vil snart være en ny Common Data Service-løsning med følgende ændringer:

| Beskrivelse | Forskydning |
| ----------------------------------------- | --- |
| Ændringer i objektet **Job/Stilling** | **Kompensationsområde** er tilføjet</br>**Økonomiske dimensioner** er tilføjet |
| Ændringer i objektet **Arbejder** | **Navnerækkefølge** er tilføjet</br>**Arbejder hjemmefra** er tilføjet</br>**Sprog** er tilføjet</br>**Anciennitetsdato** er tilføjet</br>**Jubilæumsdato** er tilføjet</br>**Oprindelig ansættelsesdato** er tilføjet |
| Ændringer af objektet **Ansættelse** | **Økonomiske dimensioner** er tilføjet</br>**Årsag til fratrædelse** er tilføjet</br>**Fratrædelsesdato** er omdøbt fra **Overførselsdato**</br>**Datoer for prøvetid** er tilføjet |
| Ændringer i objektet **Arbejders adresse** | **Gadenavn** er tilføjet</br>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** er markeret til udfasning |
| Nye konfigurationsobjekter til variabel kompensation | **Type af variabel kompensationsplan**</br>**Kompensation - variabel struktur**</br>**Fordelingsregler**</br>**Niveau i variabel kompensationsplan** |
| Nyt objekt **Arbejderkalender for ansættelse** | **Arbejdskalenderobjekt** er tilføjet |
| Nyt objekt **Lønoplysninger for stillinger** | **Lønoplysninger for stillinger** er tilføjet |
| Nyt objekt **Titel** | **Titel** er tilføjet. Den nye enhed **Titel** vil blive medtaget i synkroniseringsprocessen mellem Human Resources og Common Data Service. Der henvises ikke til den først i enhederne **Stilling** eller **Job**. |

I løbet af de næste par uger vil disse enhedsændringer være tilgængelige i alle miljøer. Sådan installeres den nyeste Common Data Service-løsning til HR manuelt:

1.  Gå til [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2.  Vælg **Miljøer**.

3.  Find det miljø, du vil opgradere. Miljøet skal svare til **Miljønavn** i sektionen **Common Data Service-oplysninger** i formularen **Om** i HR.

4.  Vælg miljøet for at få vist miljødetaljerne.

5.  Vælg **Administrer løsninger** på handlingslinjen i toppen. Der åbnes et nyt browservindue, hvor du kan navigere til **Dynamics 365 Administration** i konteksten af dit miljø.

6.  Vælg **Dynamics 365 Human Resources Anchor** i listen **Løsning**.

7.  Vælg **Opgrader** for at anvende den seneste løsning.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Importér problemer med enheden Forlad registreringsdata (406082)

Du kan nu tilmelde en medarbejder til en ny orlovsplan af samme type, hvis den nye tilmeldingsdato er senere end den udløbne registreringsdato for den forrige plan.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Problem med eksport af bidragssatser i 401k payrollWorkerEnrolledBenefitDetail-enhed i DMF (420700)

Denne ændring retter eksportfunktionen for **payrollWorkerEnrolledBenefitDetail**-enheden, så den afspejler de aktuelle værdier for arbejdsgiverens bidrag.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Når du søger i den strømlinede arbejderformular, vises en meddelelse om, at feltet Person skal udfyldes (402525)

Når du søger efter en medarbejder, vises en meddelelse om, at du skal udfylde feltet **Person**, ikke længere.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Værdien i feltet Note gengives ikke i formularen Tilføj flere færdigheder (380134)

Denne ændring retter et problem, når du tilpasser formularen **Tilføj flere færdigheder** i Medarbejderselvbetjening.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Flere fast løn-strukturer udløber ikke ved overførsel af medarbejdere (389466)

Med denne ændring udløber alle aktive fast løn-poster for den gamle stilling på overførselsdatoen.

## <a name="in-preview"></a>Som eksempel

Følgende prøvefunktioner blev tilgængelige d. 3. februar 2020:

- **Visningsfunktioner for orlov og fravær** - Du kan finde flere oplysninger under [Visningsfunktioner for orlov og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Prøveversionsfunktion: Administration af frynsegoder** – Der er flere oplysninger, herunder kendte problemer, under [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]