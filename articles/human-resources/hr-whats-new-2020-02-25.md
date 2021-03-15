---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (25. februar 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 25. februar 2020.
author: andreabichsel
manager: tfehr
ms.date: 02/25/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4faecb83518f3ef8af825872abc2a6ffb94162fc
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128016"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (25. februar 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.2927. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Aktivér navigation i Sagsstyring og datastyringsobjektenhed (DMF) (414754)

Denne eksempelfunktion aktiverer yderligere navigation til sager i Sagsstyring. Du kan aktivere denne visningsfunktion i arbejdsområdet **Funktionsstyring**. Disse menupunkter vises i arbejdsområdet **Overholdelse** i Dynamics 365 Human Resources. Med denne ændring har HR adgang til:

- Alle sager
- Mine sager
- Mine åbne sager
- Mine forsinkede sager
- Sager, der er tildelt mig via arbejdsgangen

Sammen med disse nye visninger i sager er DMF-enheden **Sagsoplysninger** også tilgængelig.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Aktivér Relationsdefinitioner i det globale adressekartotek (414762)

Relationer er nu aktiveret i det globale adressekartotek. Før denne uges udgivelse viste faktafeltet **Relationer** alle systemdefinerede relationer. Nu kan du definere disse relationer på siden med det globale adressekartotek.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>En stilling kan fjernes, når der findes aktive kompensationsposter for stillingen (414568)

Med denne ændring vises en advarsel, når du forsøger at slette en stilling, og en arbejder har en aktiv kompensationspost for samme stilling. Når det sker, skal du opdatere medarbejderens faste løn-post, før stillingen fjernes.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Arbejdsprocessen for gennemgang af ydeevne tilføjer indimellem godkendelser fra personer, der ikke er en del af processen (414171)

Denne ændring retter et problem, hvor yderligere godkendelsesdeltagere føjes til gennemsynet af ydeevnen.

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>Tildelingen af arbejderstilling, der ikke er oprettet i Dataverse, da den blev valgt i dialogboksen Ny arbejder (413479)

Denne ændring retter en fejl, når du ansætter en ny arbejder og tildeler den nye ansættelse til en stilling via dialogboksen **Ny medarbejder**. Nu afspejles stillingstildelingen i Dataverse.

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

I løbet af de næste par uger vil disse enhedsændringer være tilgængelige i alle miljøer. Sådan installeres den nyeste Dataverse-løsning til HR manuelt:

1.  Gå til [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2.  Vælg **Miljøer**.

3.  Find det miljø, du vil opgradere. Det skal svare til **Miljønavn** i sektionen **Common Data Service-oplysninger** i formularen **Om** i HR.

4.  Vælg miljøet for at få vist miljødetaljerne.

5.  Vælg **Administrer løsninger** på handlingslinjen i toppen. Der åbnes et nyt browservindue, hvor du kan navigere til **Dynamics 365 Administration** i konteksten af dit miljø.

6.  Vælg **Dynamics 365 Human Resources Anchor** i listen **Løsning**.

7.  Vælg **Opgrader** for at anvende den seneste løsning.

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