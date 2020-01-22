---
title: Nyheder eller ændringer i Dynamics 365 Talent (27. februar 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d0fdc9f056ea494cf52e8483b901070dae0bcd29
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897666"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-27-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (27. februar 2019)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>Føje menupunktet Brugerdefinerede felter til Systemadministration

Navigation til menuen **Brugerdefinerede felter** er tilføjet i **Systemadministration**-arbejdsområdet.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>Skjule import- og oprettelsesindstillinger for nye mobilprogrammer

På nuværende tidspunkt kan der ikke oprettes nye mobilapps i Talent. Muligheden for at oprette nye mobiloplevelser er blevet fjernet fra menuen **Mobilapp**.

### <a name="variable-compensation-award-dmf-entity"></a>Variabel kompensationsbonus (DMF-enhed)

I denne version kan **Variabel kompensationsbonus** Data Management Framework (DMF)-enheden nu eksporteres.

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>UK-adresser vises på siden med analyser for personalestyring som schweiziske adresser

I denne udgave vises adresser efter by. I denne version er problemer med visualiseringer, der viser en forkert placering for en medarbejder, løst.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>Power BI-personalerapporten viser en fejl, når en arbejders anciennitetsdato er på en skuddag

Der er foretaget en rettelse i Microsoft Power BI af hensyn til anciennitetsdatoer, der falder den 29. februar

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>Fast løn til medarbejder, variable bonusser for medarbejderen, variable lønstrukturer til medarbejder (tilmeldinger) giver mulighed for brugerdefinerede felter

Der kan nu tilføjes brugerdefinerede felter for fast løn til medarbejder, variable bonusser for medarbejderen og variable lønstrukturer for medarbejdere (tilmeldinger). Du kan nu spore yderligere oplysninger om medarbejderens faste og variable lønstrukturer ud over de oplysninger, der som standard er tilgængelige. Brugerdefinerede felter kan angives og opdateres via enten brugergrænsefladen eller de enheder, der findes.

### <a name="other-miscellaneous-bug-fixes"></a>Diverse andre fejlrettelser

Denne version indeholder andre mindre fejlrettelser.

## <a name="coming-soon"></a>Kommer snart

### <a name="advanced-compensation-security-fixed-and-variable"></a>Avanceret lønsikkerhed (fast og variabel)

I mange organisationer har chefer for løn og frynsegoder kun har adgang til bestemte lønposter. Disse poster kan være beregnet til ledere eller medarbejdere i bestemte områder. Med denne ændring kan HR-medarbejdere administrere og vedligeholde lønstrukturer for forskellige medarbejdergrupper i organisationen. Sikkerhedsroller, der kan tildeles til faste og variable lønstrukturer, bestemmer adgangen til disse strukturer og de medarbejderdata, der er knyttet til dem (f.eks. lønoplysninger og bonusposter). Kun de roller, der har den angivne adgang, vil kunne behandle løn for medarbejderne.

### <a name="platform-update-24-for-finance-and-operations"></a>Platform update 24 til Finance and Operations

Yderligere oplysninger om Platform update 24 til Microsoft Dynamics 365 Finance and Operations (marts 2019) finder du under [Funktioner i prøveversion af Finance and Operations Platform update 24 (marts 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>Gøre fast medarbejderløn tilgængelig for fremtidige stillingstildelinger

Det er almindeligt, at personer, der får ansættelse i en organisation, har en fremtidig startdato. Med denne ændring kan fast løn defineres for kommende medarbejdere, der har fremtidige stillingstildelinger.

## <a name="known-issues"></a>Kendte problemer

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance"></a>Ændringer af Core HR-integrationsskabelonen (Talent Common Data Service til Finance)
Core HR-skabelonen er blevet opdateret til en "avanceret forespørgselsskabelon". Derfor er den avancerede forespørgsel som standard tilgængelig for projekter, der er oprettet ved hjælp af denne skabelon. Desuden bliver enhver standardtilknytningsfunktion kun vist i den avancerede forespørgselseditor. (Standardtilknytningsfunktioner vises som "FN" i tilknytningerne).

Du kan finde flere oplysninger om tilknytningsfejl under [Nyheder eller ændringer i Dynamics 365 Talent: Core HR (14. december 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

For at bruge den nye skabelon skal du oprette et nyt projekt og vælge den nye Talent-integrationsskabelon.

Du kan opdatere den eksisterende skabelon ved at følge disse trin.

1. Opdater følgende tilknytninger:

    - **Jobstillinger til stillinger:** Fjern denne tilknytning.
    - **Den overordnede tildelingsopgave Jobstillinger til stillinger:** Fjern denne tilknytning.
    - **Jobstillinger til basisstilling:** Tilføj en ny tilknytning fra Common Data Service-enheden **Jobstillinger** til Finance and Operations-enheden **Basisstilling**. Flyt den til position 7 i rækkefølgen.

        [![Tilknytningen Jobstillinger til grundlæggende stilling](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **Jobstillinger til stillingens detaljer:** Tilføj en ny tilknytning fra Common Data Service-enheden **Jobstillinger** til Finance and Operations-enheden **Stillingens detaljer**. Flyt den til position 8 i rækkefølgen.

        [![Tilknytningen Jobstillinger til stillingsoplysninger](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **Jobstillinger til stillingens varighed:** Tilføj en ny tilknytning fra Common Data Service-enheden **Jobstillinger** til Finance and Operations-enheden **Stillingens varighed**.

        [![Tilknytningen Jobstillinger til Stillingsvarighed](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **Jobstillinger til stillingshierarkier:** Tilføj en ny tilknytning fra Common Data Service-enheden **Jobstillinger** til Finance and Operations-enheden **Stillingshierarkier**. Vælg **Avanceret forespørgsel** at gøre din avancerede forespørgsel tilgængelig for projektet.

       [![Knappen Avanceret forespørgsel](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. Tilføj følgende tilknytninger.
    
    [![Overførsel](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. Vælg linket **Avanceret forespørgsel og filtrering** ud for feltet **Søg**.  

    3. Find kolonnen **cdm_parentjobpositionid.cdm_jobpositionnumber**, og vælg pil ned-knappen ned i højre side af den.

    4. Vælg **Fjern tom** i dialogboksen, der vises.

    5. Vælg **Tilføj kolonne \> Tilføj betinget kolonne** for at tilføje en standardværditransformering af HIERARCHYTYPENAME.

        [![Kommandoen Tilføj betinget kolonne](./media/Add-column.png)](./media/Add-column.png)

    6. I dialogboksen **Tilføj betinget kolonne** skal du angive **HIERARCHYTYPENAME** som navn på den nye kolonne.
    7. I **Hvis**-delen af betingelsen skal du vælge et felt, bruge **lig med** som relationen og angive en værdi. I ***Så**- og **Ellers**-delen af betingelsen skal du angive, hvad standardværdien skal være. I dette tilfælde skal du angive **Linje** i begge dele.

        [![Dialogboksen Tilføj betinget kolonne](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. Vælg **OK** for at lukke dialogboksen **Avanceret forespørgsel og filtrering**.
    9. På siden **Tilknytningsopgave** skal du vælge den nye kolonne som kilde for at oprette en anden tilknytning til HIERARCHYTYPENAME.

        [![Overførsel](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
