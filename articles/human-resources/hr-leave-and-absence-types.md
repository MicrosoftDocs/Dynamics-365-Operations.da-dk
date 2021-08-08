---
title: Konfigurere orlovs- og fraværstyper
description: Konfigurer de orlovstyper, medarbejderne kan tage i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63970f69a437864675eada975c54446325fb60e2
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639576"
---
# <a name="configure-leave-and-absence-types"></a>Konfigurere orlovs- og fraværstyper

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Orlovstyper i Dynamics 365 Human Resources bruges til at definere de forskellige typer fravær, som medarbejdere kan rapportere. Du kan skræddersy orlovstyper i henhold til organisationens behov. Eksempler på orlovstyper omfatter:

- Betalt fravær (PTO)
- Orlov uden løn
- Ferie med løn
- Sygeorlov
- Sygeorlov
- Forældreorlov
- Kortvarigt handicap
- Tjenestefrihed ved dødsfald

## <a name="add-a-leave-type"></a>Tilføje en orlovstype

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Orlovs- og fraværstyper** under **Konfiguration**.

3. Vælg **Ny**.

4. Angiv et navn til orlovstypen under **Type**, vælg en arbejdsgang fra **Arbejdsgangs-id**, og indtast en **Beskrivelse**.

5. I **Generelt** skal du vælge **Ingen**, **Planlagt** eller **Ikke planlagt** på rullelisten **Kategori**.

6. Vælg en lønkode på rullelisten **Lønkode**.

7. Under **Årsagskode skal angives** skal du vælge, om du vil kræve en årsagskode. Hvis du vil kræve årsagskoder, skal du muligvis tilføje dem. Under **Årsagskoder** skal du vælge **Tilføj**, vælge en årsagskode og derefter markere afkrydsningsfeltet **Aktiveret** ved siden af.

8. Under **Begræns adgangen til valgte roller** skal du vælge, om du vil begrænse adgangen. Vælg derefter sikkerhedsrollerne under **Sikkerhedsroller for denne orlovstype**. Sikkerhedsrollerne defineres i den arbejdsgang, du valgte under **Arbejdsgangs-id** tidligere i denne procedure.

9. Vælg den farve, der skal vises på orlovs- og fraværskalendere for denne orlovstype, under **Kalenderfarve**. 

10. Under **Suspensionsforhold** skal du vælge, om du ønsker, at denne orlovstype enten skal suspendere en anden orlovstype, eller den skal suspenderes af en anden orlovstype. Når der sendes en orlovsanmodning for den suspenderende orlovstype, oprettes der automatisk en orlovssuspendering for den suspenderede orlovstype. 

10. Vælg **Gem**.

## <a name="configure-leave-type-rules"></a>Konfigurere regler for orlovstype

1. Angiv afrundingsindstillinger for orlovstypen. Indstillingerne omfatter **Ingen**, **Op**, **Ned** og **Nærmeste**. Du kan også angive afrundingspræcision for orlovstypen.

2. Angiv **Helligdagskorrektion** for orlovstypen. Når du vælger denne indstilling, bruger Human Resources det antal helligdage, der falder på en arbejdsdag, til at bestemme, hvordan der skal periodiseres tid for orlovstypen. Hvis juledag f.eks. falder på en mandag, trækker Human Resources én dag fra orlovstypen ved behandling af periodiseringer.

   Du kan angive helligdage i arbejdstidskalenderen. Du kan finde flere oplysninger under [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)
   
 3. Angiv **Overført orlovstype** for orlovstypen. Når du vælger denne indstilling, overføres eventuelle overførte saldi til den angivne orlovstype. Type overført orlov skal også medtages i orlovs- og fraværsplanen. 
 
4. Definer **Udløbsregler** for orlovstypen. Når du konfigurerer denne indstilling, kan du vælge enheden dage eller måneder og angive varigheden for udløbet. Ikrafttrædelsesdatoen for udløbsreglen bruges til at bestemme, hvornår du skal begynde at køre det batchjob, der behandler udløbet af orlov, eller den dato, hvor reglen træder i kraft. Selve udløbet finder altid sted på startdatoen for periodiseringsperioden. Hvis startdatoen for periodiseringsperioden f.eks. er 3. august 2021, og udløbsreglen er angivet til 6 måneder, behandles reglen på baggrund af udløbsforskydningen fra startdatoen for periodiseringsperioden, så den udføres den 3. februar 2022. De orlovssaldi, der findes på tidspunktet for udløbet, trækkes fra orlovstypen og afspejles i orloven.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Konfigurere den nødvendige vedhæftede fil pr. orlovstype

> [!NOTE]
> Hvis du vil bruge feltet **Vedhæftet fil påkrævet**, skal du først aktivere funktionen **(Forhåndsversion) Konfigurere påkrævet vedhæftet fil til orlovsanmodninger** i Funktionsstyring. Du kan få flere oplysninger om aktivering af prøveversionsfunktioner under [Administrere funktioner](hr-admin-manage-features.md).

1. Vælg **Orlovs- og fraværstyper** under **Opsætning** under fanen **Links** på siden **Orlov og fravær**.

2. Vælg en orlov- og fraværstype på listen. Brug derefter feltet **Vedhæftet fil påkrævet** i sektionen **Generelt** til at angive, om der skal overføres en vedhæftet fil, når en medarbejder sender en ny orlovsanmodning for den valgte orlovstype. 

Medarbejdere skal overføre en vedhæftet fil, når de sender en ny anmodning om orlov, som har en orlovstype, hvor feltet **Vedhæftet fil påkrævet** er aktiveret. Hvis du vil have vist den vedhæftede fil, der er overført som del af en orlovsanmodning, kan godkendere af orlov bruge indstillingen **Vedhæftede filer** til de arbejdselementer, der er tildelt dem. Hvis du får adgang til en anmodning om orlov via Human Resources-appen i Microsoft Teams, kan indstillingen **Vis detaljer** for orlovsanmodningen bruges til at få vist detaljer om den og eventuelle vedhæftede filer.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Konfigurere orlovsenheder (timer/dag) pr. orlovstype

> [!NOTE]
> Hvis du vil bruge funktionaliteten for orlovsenheder pr. orlovstype, skal du først aktivere funktionen **(Forhåndsvisning) Konfigurere orlovsenheder pr. orlovstype** i Funktionsstyring. Du kan få flere oplysninger om aktivering af prøveversionsfunktioner under [Administrere funktioner](hr-admin-manage-features.md).

> [!IMPORTANT]
> Orlovstyperne i en juridisk enhed bruger som standard orlovsenhederne fra konfigurationen af orlovsparametre på niveauet for den juridiske enhed.
> 
> Orlovsenheden for en orlovs- og fraværstype kan kun ændres, hvis der ikke er orlovstransaktioner for den pågældende orlovstype.
> 
> Funktionen kan ikke deaktiveres, efter den er blevet aktiveret.

1. Vælg **Orlovs- og fraværstyper** under **Opsætning** under fanen **Links** på siden **Orlov og fravær**.

2. Vælg en orlov- og fraværstype på listen. Vælg derefter orlovsenheden i feltet **Enhed** i sektionen **Generelt**. Du kan vælge **Timer** eller **Dage**.

3. Valgfrit: Hvis du har valgt **Timer** i feltet **Enhed**, kan du bruge feltet **Aktivér halvdagsdefinition** til at angive, om medarbejdere kan vælge den første eller anden halve fridag, hvis de anmoder om en halvdagsorlov.

Medarbejdere, der indsender en ny orlovsanmodning, kan vælge forskellige orlovstyper for at oprette deres orlovsanmodning. Alle orlovstyper, der vælges som del af en enkelt orlovsanmodning, skal dog have samme orlovsenhed. Medarbejdere kan få vist orlovsenheden for hver orlovstype i formularen **Anmodning om fridag**.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
- [Oprette en plan for orlov og fravær](hr-leave-and-absence-plans.md)
- [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)
- [Stop orlov midlertidigt](hr-leave-and-absence-suspend-leave.md)
- [Oprette en arbejdsproces for køb og salg af orlov](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
