---
title: Generere Affordable Care Act-rapporter i Frynsegodeadministration
description: I dette emner beskrives, hvordan Frynsegodeadministration hjælper dig med at spore de oplysninger, der er rapporteret på blanket 1095-B og 1095-C for Affordable Care Act (ACA) Employer Mandate.
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: d681514f53dbaf4aafce33722d0c1837c3d270407c19d629c3383ff1a2472d67
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727059"
---
# <a name="generate-aca-reports-in-benefits-management"></a>Generere ACA-rapporter i Frynsegodeadministration

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Frynsegodeadministration hjælper dig med at spore de oplysninger, der er rapporteret på blanket 1095-B og 1095-C for Affordable Care Act (ACA) Employer Mandate. Ligesom ACA-rapporteringsfunktionen i det gamle arbejdsområde **Frynsegoder** gælder denne funktion kun for juridiske enheder i USA.

Hvis du vil bruge denne funktion, skal du først aktivere **avanceret administration af frynsegoder**. Yderligere oplysninger, herunder vigtige oplysninger om styring af goder, finder du i [Aktiver eller deaktiver administration af frynsegoder](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> Du kan kun bruge ACA-rapportering fra arbejdsområdet til **Frynsegodeadministration** eller det gamle arbejdsområde til **Frynsegoder**, ikke fra begge. Hvis du f.eks. har skiftet til Frynsegodeadministration, er ACA-rapportering kun tilgængelig fra arbejdsområdet **Frynsegodeadministration**, ikke fra det gamle arbejdsområde til **Frynsegoder**.
>
> Hvis du skifter til Frynsegodeadministration midt i et tilmeldingsår, skal du konfigurere medarbejderdata korrekt for hele året i Frynsegodeadministration. På denne måde sikrer du, at du modtager nøjagtige rapporteringsoplysninger for hele året.

## <a name="getting-started"></a>Kom godt i gang

Hvis du vil spore oplysninger for 1095-.blanketter, skal du første oprette en eller flere Affordable Care-dækningsgrupper. Disse grupper angiver følgende oplysninger:

- Det dækningstilbud, som er til rådighed for en medarbejder
- Medarbejderens andel af det laveste månedlige løntillæg, hvis omkostningen ligger over den føderale fattigdomsgrænse
- 'Safe Harbor', der bruges af arbejdsgiveren, hvis det er relevant

De Affordable Care-dækningsgrupper giver dig mulighed for at administrere disse oplysninger for flere medarbejderposter, der har samme betingelser. Det er nemt at tildele grupper til en eller flere medarbejdere.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Oprette eller redigere en Affordable Care-dækningsgruppe

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Affordable Care-dækningsgruppe**.

    ![Vælge Affordable Care-dækningsgruppe.](./media/hr-benefits-management-aca-coverage-group.png)

2. Vælg **Ny** for at oprette en ny Affordable Care-dækningsgruppe eller **Rediger** for at ændre en eksisterende gruppe.

    ![Vælge Ny eller Rediger.](./media/hr-benefits-management-aca-new.png)

3. Angiv følgende felter.

    | Felt | Betegnelse |
    |---|---|
    | Navn | Angiv et navn på gruppen. |
    | Beskrivelse | Angiv en beskrivelse af gruppen. |
    | Tilbud om dækning | Den dækning, der tilbydes medarbejderne, deres ægtefælle eller partner og deres afhængige. |
    | Medarbejderens andel af omkostningen | Det beløb, medarbejderen er ansvarlig for. |
    | Gældende afsnit i 4980H Safe Harbor | Safe harbor-koden for 4980H eller overførselshjælpekoden. |
    | Planlæg startmåned | Vælg den kalendermåned, hvor frynsegodeplanåret starter. |
    | Gruppen er gældende fra | Den første dato, denne post er gyldig. |
    | Gruppen er gældende til | Den sidste dato, hvor denne post er gyldig. Hvis der ikke er nogen udløbsdato, skal du angive **Aldrig**. |

    ![Oprette en dækningsgruppe.](./media/hr-benefits-management-aca-new-group.png)

4. Vælg **Gem**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Tilknytte flere medarbejdere til Affordable Care-dækningsgruppe

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Affordable Care-dækningsgruppe**.
2. Vælg den gruppe, der skal tildeles medarbejdere til.
3. Vælg **Massetildeling**.

    ![Vælge Massetildeling.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Vælg medarbejdere på listen, og vælg derefter **Tildel**.

    ![Tildele valgte medarbejdere til en gruppe.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Vedligeholde flere versioner af en dækningsmuligheder

Du kan vedligeholde flere versioner af en enhver dækningsgruppe. Når der sker ændringer i organisationen eller de frynsegoder, der tilbydes, kan du holde oplysningerne for gruppen opdateret uden at skulle oprette en ny gruppe og tildele medarbejdere til den igen.

Når du har oprettet Affordable Care-dækningsgrupper, kan du massetildele medarbejdere til dem. Du kan også tildele medarbejdere til grupper enkeltvist og angive, om ACA-oplysninger spores og rapporteres.

Hvis du ikke behøver at spore og rapportere ACA-oplysninger for en medarbejder, kan du angive indstillingen **Rapportdækning** til **Nej**. Du kan f.eks. have deltidsansatte, der ikke kræver ACA-rapportering.

### <a name="override-default-values-for-an-employee"></a>Tilsidesætte standardværdier for en medarbejder

For medarbejdere, der er knyttet til en Affordable Care-dækningsgruppe kan du ændre følgende indstillinger for alle måneder, der kræver forskellige værdier:

- Tilbud om dækning
- Medarbejderens andel af omkostningen
- Gældende afsnit i 4980H Safe Harbor

> [!NOTE]
> Ved 2020 ACA-rapporter skal du rapportere både arbejds- og privat postnumre på Blanket 1095-C. Værdierne angives automatisk på basis af aktuelt aktive lokationer. Hvis en af lokationerne har været forskellig i løbet af et år, skal du tilsidesætte værdien. Feltet **Postnummer** (linje 17) i 1095-C-rapporten udfyldes kun på følgende måde, hvis **Tilbud om dækning**-koden indeholder **1L** - **1Q**:
>
> - **1L, 1M eller 1N:** Det primære postnummer for bopæl
> - **1O, 1P, 1Q:** Det primære postnummer for arbejde

Benyt følgende fremgangsmåde for at angive undtagelser for værdier for en Affordable Care-dækningsgruppe.

1. Vælg **Links** i arbejdsområdet **Personalestyring**, og vælg derefter **Arbejdere**.
2. Vælg medarbejderen på listen.
3. Under fanen **Ansættelse** i afsnittet **Flere oplysninger** skal du vælge **Affordable Care-dækning**.

    ![Ændre indstillinger for én medarbejder.](./media/hr-benefits-management-aca-change-single-employee.png)

4. Vælg **Rediger**.
5. For hver måned, der kræver ændringer, skal du markere afkrydsningsfeltet **Tilsidesæt standard** og derefter ændre de andre værdier efter behov.

    ![Tilsidesætte standardværdier.](./media/hr-benefits-management-aca-override-default.png)

6. Vælg **Gem**.

## <a name="report-health-care-coverage"></a>Indberette dækning af sygeforsikring

Du skal spore alle medarbejder-sponsorerede, selv-forsikrede sundhedsforsikringer for fuldtids- og deltidsansatte. Medtag hver medarbejder sammen med deres afhængige i 1095-C-rapporten for de måneder, de var dækket.

Hvis du vil angive, om der skal rapporteres en frynsegodeplan, skal du følge disse trin.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner**.
2. Vælg den frynsegodeplan, der skal rapporteres.
3. Vælg **Rediger**.
4. Angiv indstillingen **Rapporteret i henhold til Affordable Care Act** til **Ja**.

    ![Indberetning af dækning af sygeforsikring.](./media/hr-benefits-management-aca-report-coverage.png)

5. Vælg **Gem**.

Hvis en medarbejder vælger sundhedsforsikring for en afhængig, bestemmes den afhængiges dækningsperiode på den dato, hvor den afhængige blev tilmeldt eller fjernet. Dækningsdatoer for afhængige beregnes automatisk på basis af den periode, hvor den afhængige var berettiget og aktiv i en plan i løbet af tilmeldingsåret.

## <a name="generate-1095-b-and-1095-c-forms"></a>Generere 1095-B- og 1095-C-blanketter

Du kan også generere ACA 1095-B- og 1095-C-blanketter og derefter distribuere dem til hver af dine medarbejdere. Du kan også elektronisk generere Blanket 1095-C og de tilsvarende 1094-C-overførselsfiler, der skal sendes til Internal Revenue Service (IRS).

1. Vælg **ACA 1095-B**- eller **ACA 1095-C**-blanketten i arbejdsområdet **Frynsegodeadministration**.
2. Rediger parametrene efter behov, og vælg derefter **OK**.

    > [!NOTE]
    > Hvis du udskriver 1095-C-blanketter for mere end 500 medarbejdere, modtager du mere end én PDF-fil. Det anbefales, at du øger værdien i feltet **Maksimal filstørrelse i megabyte** på siden **Dokumentadministrationsparametre** til **150**. (Hvis du hurtigt vil åbne siden, kan du bruge søgefeltet på navigationslinjen).
    >
    > ![Ændre den maksimale filstørrelse.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Hvis du vil kontrollere status for rapporterne og få dem vist, skal du bruge søgefeltet på navigationslinjen til at åbne siden **Elektroniske rapporteringsjobs**.

    ![Søge efter siden Job til elektronisk rapportering.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Marker den rapport, du vil have vist, og vælg derefter **Vis filer**.

    ![Vise filer.](./media/hr-benefits-management-aca-show-files.png)

5. Vælg **Åbn**.

    ![Åbne en fil.](./media/hr-benefits-management-aca-open-file.png)

6. Åbn zip-filen, og vælg derefter rapporten på den meddelelseslinje, der vises nederst i browservinduet. Du kan få vist eller udskrive PDF-filen.

    ![Eksempel på 1095-C-formular.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>Vise oplysninger om ACA-dækning

På siden **Arbejderens dækning under Affordable Care** vises følgende oplysninger:

- Medarbejdere, der er tilknyttet hver dækningsgruppe
- Medarbejdere, der ikke behøver at blive medtaget i en rapport
- Ikke-tildelt medarbejder

Benyt følgende trin for at se disse oplysninger.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Arbejderens dækning under Affordable Care**.
2. Vælg en gruppe i feltet **Gruppenavn**.

    ![Vise ACA-dækning.](./media/hr-benefits-management-aca-view-coverage.png)

Hvis nogen af standardværdier fra Affordable Care-dækningsgruppen er blevet tilsidesat, vises en stjerne ud for den værdi, der er ændret. Hvis værdierne for alle 12 måneder er de samme og ikke er blevet tilsidesat, vises værdien i kolonnen **Alle 12 måneder**.

Du kan få vist medarbejdere, som ikke er markeret som ACA-reportable, og som ikke behøver en Blanket 1095-C. Vælg **Ikke ACA-rapporterbar** i feltet **Filtrer efter**.

Du kan få vist medarbejdere, som ikke er knyttet til en gruppe, eller som er tildelt en udløbet gruppe. Vælg **ikke-tildelt eller udløbet gruppe** i feltet **Filtrer efter**.

### <a name="export-to-excel"></a>Eksportér til Excel

Hvis du vil eksportere en af Microsoft Excel-listerne, skal du benytte følgende fremgangsmåde.

1. Vælg knappen **Åbn i Microsoft Office**.
2. Vælg **HCM Human Resources-midlertidige tabel til intern brug**.
3. Vælg **Hent**.

### <a name="view-aca-reportable-dependents"></a>Vise afhængige ACA, der kan rapporteres

Hvis du skal rapportere dækkede personer, fordi du giver dig selv forsikret dækning, kan du få vist alle afhængige, der er dækket af frynsegodeplaner, der er markeret som **ACA-rapporterbare**. Vælg **Vis afhængig af dækning** i handlingsruden.

![Vise afhængig af dækning.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Der vises dækningsoplysninger for dem, der er afhængige af medarbejderen.

![Dækning for afhængig part.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Siden viser kun frynsegoder, der er markeret som **ACA-rapporterbare**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]