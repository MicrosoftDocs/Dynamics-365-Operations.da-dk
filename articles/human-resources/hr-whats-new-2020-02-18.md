---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (18. februar 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 18. februar 2020.
author: andreabichsel
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec7d8dbc73dce57d3968c4d239a51d27673a2493
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066277"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (18. februar 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.2903. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="platform-update-32"></a>Platform update 32 

Platformsopdatering 32 er nu tilgængelig. Du kan finde flere oplysninger i [Nyheder eller ændringer i Platform update 32 til programmer til finans og drift (februar 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Søgeværdier huskes, når der ændres visningsindstillinger i den strømlinede medarbejderformular (383833)

Den nye formular **Arbejder** husker nu søgeværdier, når du ændrer visningsindstillingerne og anvender ændringer.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Oversigtsfelter for kompensationsstyring i visningsfunktionen omdirigeres til forkert formular (401861)

I de faste og variable kompensationsstyringsfelter vises nu de korrekte poster i den nye **Arbejder**-formular. Gælder kun for eksempelfunktionen i den strømlinede medarbejderformular. Du kan aktivere denne visningsfunktion i **Funktionsstyring**. Du kan finde flere oplysninger under [Administrere funktioner](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>Tomt Status-felt for nogle orlovsanmodningsposter i Dataverse (414915)

Denne ændring løser et problem i Dataverse, når feltet **Status** i en orlovsanmodning er indstillet til **Gennemsyn**. Dataverse afspejler nu statussen.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Analyse af kompetencekløft er kun mulig for tildelt job (411390)

Du kan nu foretage en analyse af kompetencekløft på et job, der er defineret i Human Resources.

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>Systemvaluta synkroniseres ikke fra Dataverse til Human Resources i nye miljøer (418011)

Systemvalutaen i Dataverse kan nu synkroniseres til Human Resources.

## <a name="in-preview"></a>Som eksempel

- [Visningsfunktioner for orlov og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Prøveversionsfunktion til Administration af frynsegoder](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Kommer snart

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
