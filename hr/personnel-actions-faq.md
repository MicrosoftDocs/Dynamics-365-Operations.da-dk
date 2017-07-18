---
title: "Personalehandlinger [Ofte stillede spørgsmål]"
description: "Dette emne indeholder svar på spørgsmål, som du kan have, hvis din organisation bruger personalehandlinger. Personalehandlinger er yderligere trin, du skal udføre, når du udfører bestemte opgaver i forbindelse med personale."
author: shielas
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 4c17441b70a75f032c900c9360da6c0730cf89ba
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="personnel-actions-faq"></a>Personalehandlinger [Ofte stillede spørgsmål]
Dette emne indeholder svar på spørgsmål, som du kan have, hvis din organisation bruger personalehandlinger. Personalehandlinger er yderligere trin, du skal udføre, når du udfører bestemte opgaver i forbindelse med personale. Eksempler på opgaver, der kan kræve personalehandlinger, er, når du opretter nye stillinger, ændrer eksisterende stillingsværdier, ansætter nye medarbejdere, overflytter arbejdere, ændrer arbejderes løn, ændrer stillingsopgaver eller opsiger arbejdere.

**Bemærk!** Personalehandlinger er kun tilgængelige, hvis konfigurationsnøglen for Personalehandlinger er valgt. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Hvordan kan jeg se, om min organisation kræver personalehandlinger?
Personalehandlinger kræves af organisationen, hvis du bliver bedt om at vælge en personalehandling, når du opretter nye stillinger, ændrer eksisterende stillinger, ansætter nye medarbejdere, overflytter arbejdere, ændrer arbejderes løn, ændrer stillingsopgaver, opsiger arbejdere eller angiver orlov for arbejdere. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Hvad er forskellen mellem en stillingshandling og en arbejderhandling?
Der findes to typer personalehandlinger:

- Stillingshandling – En stillingshandling udføres på eksisterende stillinger eller nye stillinger. En stillingshandling kan f.eks. kræves, hvis du ændrer en værdi for en eksisterende stilling, eller hvis du opretter en ny sæsonbestemt stilling. Yderligere oplysninger om, hvordan du bruger stillingshandlinger, finder du under Hovedopgaver: Eksisterende arbejderstillinger eller Hovedopgaver: Nye arbejderstillinger.

- Arbejderhandling – En arbejderhandling udføres for eksisterende arbejdere eller nye arbejdere. En arbejderhandling kan f.eks. kræves, når du ansætter en ny arbejder, eller når en eksisterende arbejder bliver forfremmet. Du kan finde detaljerede oplysninger om, hvordan du bruger arbejderhandlinger, under Tildele personalehandlinger til arbejdere.

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Hvad betyder statusserne for personalehandlingerne?
Personalehandlinger kan have følgende statusser:

- **Kladde** – Hvis der bruges en arbejdsgang, er handlingen ikke sendt. Hvis der ikke bruges en arbejdsgang, er handlingen ikke fuldført.
- **Til gennemsyn** – Personalehandlingen er sendt til arbejdsgangen, men arbejdsgangen er ikke fuldført.
- **Godkendt afventen** – Arbejdsgangen er fuldført, men ændringerne er stadig i gang. Annulleret – Arbejdsgangen er annulleret, eller personalehandlingen er tilbagekaldt. Afvist – Handlingsanmodningen er afvist af godkenderen.
- **Behandler handling** – Handlingsanmodningen er godkendt, og ændringerne behandles.
- **Arbejdsgang er fuldført** – Arbejdsgangen er fuldført, og ændringerne er behandlet. Lykkedes ikke – Arbejdsgangen mislykkedes, fordi oplysningerne er forældede. Klik på Genaktiver for at få vist de seneste oplysninger og fortsætte.
- **Afsluttede** – Stillingen er oprettet eller ændret, eller medarbejderen er blevet ansat, overflyttet eller afsluttet, eller kompensationen blev ændret. Fejl – Der opstod et problem opstod, som ikke skyldes, at oplysningerne er forældet. Åbn Meddelelseslogfil for personalehandlinger for at finde årsagen til fejlen.
- **Afvist** – Handlingsanmodningen blev afvist af godkenderen.

## <a name="can-i-delete-a-personnel-action"></a>Kan jeg slette en personalehandling?
Ja, kan du slette personalehandlinger, der har status **Kladde**, **Fejl**, **Lykkedes ikke** eller **Annulleret**.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Hvordan kan jeg hurtigst se status for en anmodning om personalehandling?
Åbn en listeside for personalehandlinger, og vælg en personalehandling.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Hvad skal jeg gøre, hvis en anmodning om personalehandling mislykkes?
Hvis en anmodning om personalehandling mislykkes, skal du følge disse trin for at løse fejlen og sende anmodningen igen:

> 1. I **Handlingsrude** skal du klikke på knappen **Fejltekst** for at få vist den meddelelsestekst, der beskriver problemet.

> 2. I **Handlingsrude** skal du klikke på **Genaktiver** for at indlæse de seneste oplysninger og igen indstille **Kladde** som status for personalehandlingen.

> 3. Ret fejlen, og klik derefter på **Fuldfør** eller **Send**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Hvad sker der med en personalehandling, der bruger en arbejdsgang, når den endelige godkendelse er fuldført?
Hvis der ikke er fejl, bliver personalehandlingen skrivebeskyttet. (Du kan få vist historikken for listesiden **Alle arbejderhandlinger**, men du kan ikke ændre personalehandlingen). Når status for en personalehandling er **Afsluttede**, er placering eller arbejderposten allerede blevet opdateret. Hvis du vil have vist de ændringer, der er udført, kan du åbne listesiden **Stillinger** eller **Arbejdere**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Hvorfor får jeg vist følgende fejl, når jeg indtaster en værdi, der er forskellig fra nul, i feltet med lønsats? "Værdien ligger uden for det gyldige interval – den skal være mellem 0,00 og 0,00"
Du modtager denne meddelelse, fordi feltet Niveau i formularen Job er tomt for det job, der er knyttet til den valgte stilling.

Du kan løse denne fejl ved at udføre disse trin:

> 1. Klik på feltet Stilling i formularen Tildeling af arbejderstillinger.  
> 2. Klik på værdien i feltet Job for at åbne siden Job.
> 3. Klik på Rediger i handlingsruden.
> 4. Klik på fanen Kompensation.
> 5. Vælg et niveau i feltet Niveau.
> 6. Luk siden Job.
> 7. Luk siden Stilling.
> 8. Vend tilbage til fanen Kompensation på siden Arbejder, og vælge Fast løn.  Klik på Ny, og angiv medarbejderens stilling i feltet Stilling.  Angiv en værdi i feltet Plan, og angiv derefter medarbejderens kompensation i feltet Lønsats.

## <a name="why-cant-i-change-the-effective-date-in-the-header-of-the-worker-action-form"></a>Hvorfor kan jeg ikke ændre ikrafttrædelsesdatoen i overskriften i formen Arbejderhandling?
Du kan ikke ændre ikrafttrædelsesdatoen, fordi feltet er udfyldt med den mest logiske dato for handlingstypen.

skriv URL-adressen til siderne på administrationsporten, f.eks.:

- Ikrafttrædelsesdatoen i hovedet til en handling af typen **Opsig en medarbejder** er den dato, du har angivet i feltet **Fratrædelsesdato**.
- Ikrafttrædelsesdatoen i en handling af typen **Ansæt en arbejder** er den dato, du angav i feltet **Startdato for ansættelse**.
- Ikrafttrædelsesdatoen i en handling af typen **Overfør en arbejder** er den dato, du angav i feltet **Startdato for tildeling** for arbejderen.

