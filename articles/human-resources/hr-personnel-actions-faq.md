---
title: Ofte stillede spørgsmål om personalehandlinger
description: Denne artikel indeholder svar på spørgsmål, som du kan have, hvis din organisation bruger personalehandlinger.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 8882fd00c68dc3cafcb4ecf1b2fe351a9e7f5741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874301"
---
# <a name="personnel-actions-faq"></a>Ofte stillede spørgsmål om personalehandlinger


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel indeholder svar på spørgsmål, som du kan have, hvis din organisation bruger personalehandlinger. Human Resourceshandlinger er yderligere trin, du skal udføre, når du udfører bestemte opgaver i forbindelse med personale. 

Eksempler på opgaver, der kan kræve personalehandlinger, er:
 - Når du opretter nye stillinger. 
 - Redigerer eksisterende stillingsværdier. 
 - Ansætter nye arbejdere. 
 - Overfører arbejdere. 
 - Skifter arbejderkompensation. 
 - Ændrer tildeling af stillinger. 
 - Opsiger arbejdere.

> [!NOTE]
> Personalehandlinger er kun tilgængelige, hvis felterne **Aktivér arbejderhandlinger** og **Aktivér stillingshandlinger** er angivet til **Ja** under fanen **Personalehandlinger** på siden **Delte parametre for personale**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Hvordan kan jeg se, om min organisation kræver personalehandlinger?
Human Resourceshandlinger kræves af organisationen, hvis du bliver bedt om at vælge en personalehandling, når du opretter nye stillinger, ændrer eksisterende stillinger, ansætter nye medarbejdere, overflytter arbejdere, ændrer arbejderes løn, ændrer stillingsopgaver, opsiger arbejdere eller angiver orlov for arbejdere. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Hvad er forskellen mellem en stillingshandling og en arbejderhandling?
Der findes to typer personalehandlinger:

- **Stilling**-handling – En stillingshandling udføres på eksisterende stillinger eller nye stillinger. En stillingshandling kan f.eks. kræves, hvis du ændrer en værdi for en eksisterende stilling, eller hvis du opretter en ny sæsonbestemt stilling. 

- **Arbejder**-handling – En arbejderhandling udføres for eksisterende arbejdere eller nye arbejdere. En arbejderhandling kan f.eks. kræves, når du ansætter en ny arbejder, eller når en eksisterende arbejder bliver forfremmet. 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Hvad betyder statusserne for personalehandlingerne?
Human Resourceshandlinger kan have følgende statusser:

- **Kladde** – Hvis der bruges en arbejdsgang, er handlingen ikke sendt. Hvis der ikke bruges en arbejdsgang, er handlingen ikke fuldført.
- **Til gennemsyn** – Human Resourceshandlingen er sendt til arbejdsgangen, men arbejdsgangen er ikke fuldført.
- **Godkendt afventen** – Arbejdsgangen er fuldført, men ændringerne er stadig i gang. **Annulleret** – Arbejdsprocessen er annulleret, eller personalehandlingen er tilbagekaldt. **Afvist** – Handlingsanmodningen er afvist af godkenderen.
- **Behandler handling** – Handlingsanmodningen er godkendt, og ændringerne behandles.
- **Arbejdsgang er fuldført** – Arbejdsgangen er fuldført, og ændringerne er behandlet. **Ikke udført** – Arbejdsgangen mislykkedes, fordi oplysningerne er forældede. Klik på **Genaktiver** for at få vist de seneste oplysninger og fortsætte.
- **Afsluttede** – Stillingen er oprettet eller ændret, eller medarbejderen er blevet ansat, overflyttet eller afsluttet, eller kompensationen blev ændret. **Fejl** – Der opstod et problem, som ikke skyldes, at oplysningerne er forældet. Åbn **Meddelelseslogfil for personalehandlinger** for at finde årsagen til fejlen.
- **Afvist** – Handlingsanmodningen blev afvist af godkenderen.

## <a name="can-i-delete-a-personnel-action"></a>Kan jeg slette en personalehandling?
Ja, kan du slette personalehandlinger, der har status **Kladde**, **Fejl**, **Lykkedes ikke** eller **Annulleret**. Du kan kun slette personalehandlinger, der har statussen **Fuldført**, hvis du har angivet indstillingen **Tillad sletning af fuldførte arbejderhandlinger** til **Ja** på siden **Delte Human Resources-parametre**.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Hvordan kan jeg hurtigst se status for en anmodning om personalehandling?
Åbn en listeside for **Personalehandling**, og vælg en personalehandling.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Hvad skal jeg gøre, hvis en anmodning om personalehandling mislykkes?
Hvis en anmodning om personalehandling mislykkes, skal du følge disse trin for at løse fejlen og sende anmodningen igen:

> 1. I **Handlingsrude** skal du klikke på knappen **Fejltekst** for at få vist den meddelelsestekst, der beskriver problemet.
> 
> 2. I **Handlingsrude** skal du klikke på **Genaktiver** for at indlæse de seneste oplysninger og igen indstille **Kladde** som status for personalehandlingen.
> 
> 3. Ret fejlen, og klik derefter på **Fuldfør** eller **Send**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Hvad sker der med en personalehandling, der bruger en arbejdsgang, når den endelige godkendelse er fuldført?
Hvis der ikke er fejl, bliver personalehandlingen skrivebeskyttet. (Du kan få vist historikken for listesiden **Alle arbejderhandlinger**, men du kan ikke ændre personalehandlingen). Når status for en personalehandling er **Fuldført**, er stillings- eller arbejderposten allerede blevet opdateret. Hvis du vil have vist de ændringer, der er udført, kan du åbne listesiden **Stillinger** eller **Arbejdere**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Hvorfor får jeg vist følgende fejl, når jeg indtaster en værdi, der er forskellig fra nul, i feltet med lønsats? "Værdien ligger uden for det gyldige interval – den skal være mellem 0,00 og 0,00"
Du modtager denne meddelelse, fordi feltet **Niveau** i formularen **Job** er tomt for det job, der er knyttet til den valgte stilling.

Du kan løse denne fejl ved at udføre disse trin:

> 1. Klik på feltet **Stilling** på siden **Tildeling af arbejderstillinger**.  
> 2. Klik på værdien i feltet **Job** for at åbne siden **Job**.
> 3. Klik på **Rediger** i handlingsruden.
> 4. Klik på fanen **Kompensation**.
> 5. Vælg et niveau i feltet **Niveau**.
> 6. Luk siden **Job**.
> 7. Luk siden **Stilling**.
> 8. Vend tilbage til fanen **Kompensation** på siden **Arbejder**, og vælg **Fast løn**.  Vælg **Ny**, og angiv medarbejderens stilling i feltet **Stilling**.  Angiv en værdi i feltet **Plan**, og angiv derefter medarbejderens kompensation i feltet **Lønsats**.

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>Hvorfor kan jeg ikke ændre ikrafttrædelsesdatoen i overskriften på siden Arbejderhandling?
Du kan ikke ændre ikrafttrædelsesdatoen, fordi feltet er udfyldt med den mest logiske dato for handlingstypen.

skriv URL-adressen til siderne på administrationsporten, f.eks.:

- Ikrafttrædelsesdatoen i hovedet til en handling af typen **Opsig en medarbejder** er den dato, du har angivet i feltet **Fratrædelsesdato**.
- Ikrafttrædelsesdatoen i en handling af typen **Ansæt en arbejder** er den dato, du angav i feltet **Startdato for ansættelse**.
- Ikrafttrædelsesdatoen i en handling af typen **Overfør en arbejder** er den dato, du angav i feltet **Startdato for tildeling** for arbejderen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
