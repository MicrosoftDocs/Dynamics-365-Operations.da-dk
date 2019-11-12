---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (6. december 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bb43745b5a52c10b2d54480005d9d4e5ca6dc5bf
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550245"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-6-2018"></a>Nyheder eller ændringer i Dynamics 365 Talent - Core HR (6. december 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2071**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.


## <a name="platform-update-22-for-finance-and-operations"></a>Platform update 22 til Finance and Operations

### <a name="export-up-to-1-million-rows-to-excel"></a>Eksportere op til 1 million rækker til Excel

Funktionen Eksporter til Excel kan nu konfigureres, så brugerne kan eksportere op til 1 million rækker fra et gitter i Talent, en betydelig udvidelse fra den tidligere grænse på 10.000 rækker. 

### <a name="restyled-personalization-toolbar"></a>Ændret udseende af tilpasningsværktøjslinjen

Tilpasningsværktøjslinjen har fået nyt udseende i Platform update 22 til Finance and Operations, så brugerne lettere kan skræddersy deres egne oplevelser i Talent. Der er foretaget følgende ændringer: 

-  Navnet på hver tilpasningsværktøjslinje vises nu sammen med et ikon, som hjælper brugerne med hurtigt at genkende det værktøj, de er interesserede i at bruge.
-  Beskrivelsen af, hvordan det aktuelle værktøj bruges, vises nu også og hjælper brugerne med at forstå, hvordan de kan oprette de nødvendige tilpasninger.  
-  Hele tilpasningsværktøjslinjen kan flyttes på skærmen ved at trække og slippe på et bestemt område længst til venstre på værktøjslinjen. Dette gør det muligt for brugerne at tilpasse elementer, der er tidligere blev dækket af værktøjslinjen.   

### <a name="optimized-is-one-of-filtering-experience"></a>Optimeret "er en af" filtreringsoplevelserne

"Er en af"-filtreringsoperatoren er tilgængelig for de fleste felter, når filterruden og gitteroverskrifternes rullelister bruges. Med denne operator kan en bruger filtrere et felt, baseret på flere værdier. Der findes en ny og forbedret brugeroplevelse af operatoren "er en af" i Platform update 22 til Finance and Operations. Du kan finde flere oplysninger i [Den optimerede filtreringsoplevelse "er en af"](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering).

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>Indsætte lister fra Excel i filterfelterne med operatoren "er en af"

Brugere kan have en liste over værdier i Excel, som de vil bruge til at filtrere data i Talent, for bestemte opgaver. F.eks. kan en bruger i Personale have fundet en gruppe medarbejdere fra en rapport, der kræver yderligere undersøgelser i systemet, og det ville være ideelt for denne bruger at kunne kopiere listen direkte fra Excel til et filterfelt i Talent.

Fra og med Platform update 22 til Finance and Operations genkender operatoren "er en af" i filterruden og gitterkolonnefiltreringen nu lister, der er kopieret fra Excel, så de kan indsættes direkte i et filtreringsfelt. Dette omfatter en samling af værdier, der er kopieret fra forskellige rækker og kolonner i Excel. Du kan finde flere oplysninger om denne funktion i [Indsætte lister fra Excel i filterfelterne med operatoren "er en af"](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel).

## <a name="in-preview"></a>Som eksempel

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>Konfigurere britisk lønintegrationen mellem Talent og Dayforce

Integration mellem Talent og Ceridian Dayforce er tilgængelig som prøveversion for Storbritannien. Du kan finde flere oplysninger i følgende emne [Konfigurere lønintegration mellem Talent og Dayforce](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration).

## <a name="coming-soon"></a>Kommer snart

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Orlov og fravær: fremtidig orlov og budgettering af orlovssaldi

Med de ændringer, der foretages, så medarbejderne kan budgettere fritid og anmode om fremtidig fritid, uden at det påvirker deres aktuelle fritidssaldi, ændres den måde, som fritidssaldi vises på, også. 

Den disponible saldo, der aktuelt vises, er mængden af fritid, der er tilgængelig for anmodninger, herunder periodiseringer, til og med i dag og alle godkendte orlovsanmodninger og i al fremtid. 

Når der gives mulighed for budgettering, ændres den viste saldo til den aktuelle fritidssaldo, herunder periodiseringer til og med i dag og anmodninger til og med dags dato. Medarbejdere og ledere kan se disse opdaterede saldi i medarbejdernes og ledernes selvbetjeningsportal på kortet **Fridage** og i vinduet **Saldi for fritid**. Personalechefer kan se disse opdaterede saldi i arbejdsområdet **Personer** og i medarbejderens vindue **Tildelte orlovsplaner**.

## <a name="other-changes"></a>Andre ændringer 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>Fratrædelseskode udfyldes ikke til posten for tildeling af arbejderstilling

Der er implementeret en ændring, der udfylder årsagskoden i stillingstildelingsposten under fratrædelsesprocessen.

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>Validering af personalenummer, som er i brug, kræver yderligere oplysninger

Der vises yderligere oplysninger, når nummerserier er i brug, for bedre at forstå problemer, når et nyt nummer ikke kan oprettes.
 
### <a name="attachments-buttons-not-available-for-workers"></a>Knapper til vedhæftede filer er ikke tilgængelige for arbejdere

Der er foretaget ændringer til rettelse af vedhæftede filer. Når du føjer en ny vedhæftet fil til en arbejder, er knapperne **Ny** og **Rediger** nu tilgængelige, når der er åbne faktabokse i arbejdervinduet. 

## <a name="known-issues"></a>Kendte problemer

### <a name="mapping-errors-in-the-integration-with-finance"></a>Tilknytningsfejl i integrationen med Finance

Følgende problemer er identificeret i den aktuelle skabelon til integration af Talent med Finance. En ny skabelon offentliggøres snart og anvendes på alle nye integrationsprojekter, der oprettes. For eksisterende integrationsprojekter kan opgavetilknytningerne opdateres. Du kan finde opdaterede tilknytninger i følgende tabel. 

>[!NOTE]
> Den overordnede tildelingsopgave Jobstillinger til stillinger kan ikke integrere data. Dette er et problem, der er i øjeblikket undersøges. Der findes ingen løsning i den aktuelle tilknytning. 

I opgaven Afdelinger til driftsenhed skal følgende tilknytninger opdateres.

| Eksisterende kildefelt          | Nyt kildefelt |
| -------------------------------|------------------|
| cdm_description (beskrivelse)  | cdm_name (navn)  |

En yderligere tilknytning skal også tilføjes. Vælg det sidste **Ingen**-felt for at tilføje følgende tilknytning.

| Kildefelt                   | Destinationsfelt    |
| -------------------------------|----------------------|
| cdm_description (beskrivelse)  | NAMEALIAS (NAMEALIAS)|

De opdaterede tilknytninger skal se ud som dette.

![Opgaven Afdelinger til driftsenheder](./media/DepartmentMapping.png)


I opgaven Job til stillingsdetaljer skal følgende tilknytninger opdateres.

| Eksisterende kildefelt          | Nyt kildefelt                   |
| -------------------------------|------------------------------------|
| cdm_name (navn)                | cdm_description (beskrivelse)      |
| cdm_name (beskrivelse)         | cdm_jobdescription (stillingsbeskrivelse)|


De opdaterede tilknytninger skal se ud som dette.

![Opgaven Job til stillingsdetaljer](./media/JobMapping.png)

I opgaven Arbejdere til arbejde skal følgende tilknytninger opdateres.

| Eksisterende kildefelt                 | Nyt kildefelt                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-mailadresse 1)   | cdm_primaryemailaddress (primær e-mailadresse) |
| cdm_telephone1 (telefon 1)          | cdm_primarytelephone (primær telefon)       |

Transformeringen af feltet Køn skal også opdateres. Vælg tilknytningstypen **fn** (funktion) for Køn, og opdater følgende værditilknytninger.

| Common Data Service-værdi | Finance and Operations-værdi | | ------------|------------------ -----------| | 75440000    | Mand                         | | 75440001    | Kvinde                       | | 75440002    | Ingen                         | | 75440003    | Ikke-specifik                  |

De opdaterede tilknytninger skal se ud som dette.

![Opgaven Arbejdere til arbejde](./media/WorkerMapping.png)

![Transformering af feltet Køn](./media/WorkerTransform.png)

