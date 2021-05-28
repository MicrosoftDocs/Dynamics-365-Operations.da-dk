---
title: Kategorianmodninger fra kreditorer
description: Dette emne beskriver, hvordan kreditorer kan anmode om indkøbskategorier for deres konto. Det beskriver også den godkendelsesproces, der fuldføres af indkøbsagenter.
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1951f85f84c3b8b2d42f49d5f464d90d410ebfa2
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015945"
---
# <a name="category-requests-from-vendors"></a>Kategorianmodninger fra kreditorer

[!include [banner](../includes/banner.md)]

Med kategorianmodningsprocessen kan kreditorer anmode om, at der knyttes nye indkøbskategorier til deres konto. Disse indkøbskategorier kan derefter bruges af de relaterede indkøbs- og forsyningsprocesser. (Du kan finde flere oplysninger under [Oversigt over indkøbskataloger](procurement-catalogs.md).)

Kategorianmodninger startes af kreditorer i arbejdsområdet **Kreditoroplysninger**. De sendes derefter til gennemsyn og godkendelse hos din godkenderenhed. Godkendte kategorier føjes til listen over indkøbskategorier for kreditorens konto.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funktionen i systemet

Hvis systemet ikke allerede indeholder den funktion, der er beskrevet i dette emne, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Tillad kreditorer at ansøge om indkøbskategorier via leverandørsamarbejde*.

Når funktionen er aktiveret, kan du stadig føje indkøbskategorier til kreditorkonti manuelt. Du kan finde flere oplysnigner i [Godkende kreditorer til specifikke indkøbskategorier](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Krav til kreditorsamarbejde

Før en kreditor kan udstede kategorianmodninger, skal kreditoren være konfigureret til kreditorsamarbejde.

Kreditoren skal mindst have én bruger for leverandørsamarbejdet. Kun kreditorbrugere med sikkerhedsrollen *Kreditoradministrator (ekstern)* kan oprette og sende kategorianmodninger.

Du kan finde flere oplysninger under [Konfigurere og vedligeholde kreditorsamarbejde](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Konfigurere arbejdsgangen for kreditors kategorianmodning

Arbejdsgangen *Kreditors kategorianmodning* skal være konfigureret i arbejdsgangene for indkøb og forsyning. Kreditorerr sender nye kategorianmodninger, som du kan gennemse og godkende. De indkøbskategorier, der er anmodet om, føjes til en kreditorkonto, når kategorianmodningen er godkendt.

I følgende eksempel kan du se, hvordan du kan konfigurere en simpel arbejdsgang for *Kreditors kategorianmodning* med en enkelt godkender. Du skal gennemse de interne processer for at fastlægge opsætningen af den relevante arbejdsgang for din godkenderenhed.

1. Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsarbejdsgange**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg **Arbejdsgang for anmodning om kreditorkategor** i dialogboksen for at åbne arbejdsgangseditoren.
1. Logge på arbejdsgangseditoren.
1. Gå til handlingsruden, og vælg **Egenskaber**.
1. På siden **Egenskaber** for arbejdsgangen skal du angive en instruktionstekst i feltet **Indsendelsesinstruktioner**. Instruktionerne kan ses af kreditorer, når de sender en kategorianmodning.
1. Luk siden **Egenskaber**.
1. Træk arbejdsgangselementet **Godkend ny kategorianmodning** over på lærredet.
1. Træk et link fra arbejdsgangelementet **Start** til arbejdsgangelementet **Godkend ny kategorianmodning**.
1. Træk et link fra arbejdsgangelementet **Godkend ny kategorianmodning** til arbejdsgangelementet **Afslut**.
1. Dobbeltklik på (eller dobbeltklik på) arbejdsgangelementet **Godkend ny kategorianmodning**.
1. Vælg og hold (eller højreklik på) arbejdsgangelementet **Trin 1**, og vælg derefter **Egenskaber**.
1. Indtast emneteksten for arbejdsgangelementet i feltet **Emne for workflowopgave** på siden **Egenskaber** . Denne tekst vises som værdien i feltet **Emne** på siden **Arbejdselementer, der er tildelt mig**.
1. I feltet **Emne for workflowopgave** skal du indtaste instruktionsteksten. Instruktionerne er synlige for godkendere, når de vælger **Arbejdsgang** i handlingsruden for en kategorianmodning.
1. Vælg **Tildeling** i venstre rude.
1. Angiv **Tildel brugere til dette arbejdsgangselement** til **Bruger** under fanen *Tildelingstype*.
1. Vælg en godkender på listen **Tilgængelige brugere** under fanen **Bruger**. Vælg f.eks. en bruger i indkøbsafdelingen.
1. Vælg højre pileknap (**\>**) for at flytte godkenderen til listen **Valgte brugere**.
1. Luk siden **Egenskaber**.
1. Vælg **Gem og luk**.
1. Skriv noter om arbejdsgangen i feltet **Versionsnotater**.
1. Vælg **OK** for at gemme arbejdsgangen.
1. Hvis du er klar til at starte testen af arbejdsgangen, skal du vælge **Aktivér den nye version**. Ellers skal du vælge **Aktivér ikke den nye version**.
1. Vælg **OK** for at fuldføre opsætningen af arbejdsgangen.

> [!TIP]
> Hvis din godkenderenhed ikke kræver godkendelse af kategorianmodninger, skal du konfigurere arbejdsgangen til automatisk godkendelse.

Yderligere oplysninger om opsætning af arbejdsgange finder du i [Oversigt over arbejdsgangsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Oprette og sende en kategorianmodning

I dette afsnit beskrives det, hvordan kreditorerr kan bruge arbejdsområdet **Kreditoroplysninger** til at oprette, redigere, få vist og sende kategorianmodninger.

### <a name="start-a-new-request"></a>Starte en ny anmodning

Benyt følgende fremgangsmåde for at starte en ny kategorianmodning.

1. Vælg feltet **Kategorianmodninger** i arbejdsområdet **Kreditoroplysninger**.
1. Vælg **Ny kategorianmodning** i handlingsruden på siden **Kategorianmodninger**.
1. I dialogboksen **Ny kategorianmodning** kan du finde den kategori, du vil ansøge om, ved at gå til træet og/eller ved at bruge filteret øverst på listen. Marker afkrydsningsfeltet for hver relevant kategori.

    Vær opmærksom på følgende punkter:

    - Kategorier, der aktuelt er aktive på din kreditorkonto, vises som valgte og kan ikke fjernes.
    - Du kan anmode om flere indkøbskategorier i en enkelt kategorianmodning.

1. Vælg **OK** for at oprette en anmodningskladde.

    Den nye anmodningskladde vises nu på siden **Kategorianmodninger**.

1. Åbn den nye kladdeanmodning for at gennemse og redigere den efter behov.

    - Hvis du vil have vist listen over kategorier, der aktuelt er inkluderet i anmodningen, skal du vælge oversigtspanelet **Anmodede kategorier**.
    - Hvis du vil se de aktive kategorier, skal du åbne faktaboksen **Aktive kategorier** til højre på siden.
    - Hvis du vil føje en kategori til anmodningen, skal du vælge **Tilføj** på værktøjslinjen i oversigtspanelet **Anmodede kategorier**.
    - Hvis du vil fjerne en kategori fra anmodningen, skal du vælge kategorien i oversigtspanelet **Anmodede kategorier** og derefter vælge **Fjern** på værktøjslinjen.
    - Hvis du vil knytte et dokument til anmodningen, skal du vælge **Vedhæftede filer** i handlingsruden. Vedhæftede dokumenter vil være tilgængelige for godkendere, når de gennemgår kategorianmodningen.
    - Hvis du vil fjerne et vedhæftet dokument fra anmodningen, skal du vælge **Vedhæftede filer** i handlingsruden. Vælg det dokument, du vil fjerne, og vælg derefter **Slet** i handlingsruden.

1. Hvis du er klar til at sende anmodningen, skal du vælge **Send** i handlingsruden. Ellers skal du blot lukke siden og springe de øvrige trin over i denne procedure. Du kan vende tilbage til anmodningen på et senere tidspunkt.
1. Læs de indsendelsesinstruktioner, der vises, og vælg derefter **Send**.
1. Angiv de supplerende oplysninger, der kræves, i feltet **Kommentar**. Vælg derefter **Send** for at fuldføre anmodningen.

### <a name="edit-a-draft-or-recalled-request"></a>Redigere en kladde eller tilbagekaldt anmodning

Hvis du vil redigere en kladde eller en tilbagekaldt kategorianmodning, skal du benytte følgende fremgangsmåde.

1. Vælg feltet **Kategorianmodninger** i arbejdsområdet **Kreditoroplysninger**.
1. Vælg kladden eller den tilbagekaldte anmodning for at åbne den.
1. Rediger anmodningen efter behov, og derefter kan du enten lukke den eller sende den som beskrevet i forrige procedure.

### <a name="submit-a-draft-or-recalled-request"></a>Sende en kladde eller tilbagekaldt anmodning

Hvis du vil sende en kladde eller en tilbagekaldt kategorianmodning, skal du benytte følgende fremgangsmåde.

1. Vælg feltet **Kategorianmodninger** i arbejdsområdet **Kreditoroplysninger**.
1. Vælg den kladde eller tilbagekaldte anmodning, du vil sende.
1. Vælg **Send** i handlingsruden.
1. Læs de indsendelsesinstruktioner, der vises, og vælg derefter **Send**.
1. Angiv de supplerende oplysninger, der kræves, i feltet **Kommentar**. Vælg derefter **Send** for at fuldføre anmodningen.

    Statussen for kategorianmodningen ændres til en af følgende værdier:

    - _Afventer gennemgang_ – Anmodningen er i arbejdsgangen.
    - _Afventer godkendelse_ – Godkendelse er påkrævet.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Tilbagekalde en sendt anmodning, der endnu ikke er godkendt

Hvis du vil tilbagekalde en kategorianmodning, der er sendt, men endnu ikke er godkendt, skal du benytte følgende fremgangsmåde.

1. Vælg feltet **Kategorianmodninger** i arbejdsområdet **Kreditoroplysninger**.
1. Vælg den ventende anmodning, du vil tilbagekalde.
1. Vælg **Tilbagekald** i handlingsruden.
1. Angiv de supplerende oplysninger, der kræves, i feltet **Skriv en kommentar**. Vælg derefter **Send** for at fuldføre anmodningen.

    Statussen for kategorianmodningen ændres til _Annulleret_. Anmodningen bevarer denne status, indtil du sletter den eller sender den igen.

### <a name="delete-a-draft-or-recalled-request"></a>Slette en kladde eller tilbagekaldt anmodning

Hvis du vil slette en kladde eller en tilbagekaldt kategorianmodning, skal du benytte følgende fremgangsmåde.

1. Vælg feltet **Kategorianmodninger** i arbejdsområdet **Kreditoroplysninger**.
1. Vælg den kladde eller tilbagekaldte anmodning, du vil slette.
1. Vælg **Slet** i handlingsruden.
1. Vælg **Ja** for at bekræfte sletningen.

### <a name="view-completed-requests"></a>Få vist fuldførte anmodninger

Du kan få vist fuldførte anmodninger ved at åbne arbejdsområdet **Kreditoroplysninger** og vælge feltet **Kategorianmodninger**. Kategorianmodninger, der er fuldført, får en af følgende statusser:

- _Godkendt_ – Anmodningen er godkendt. Hvis du vil have vist de kategorier, der netop er blevet tilføjet, skal du gå tilbage til arbejdsområdet **Kreditoroplysninger**, åbne rullelisten **Flere detaljer** i venstre rude og derefter vælge **Kategorier**.
- _Afvist_ – Anmodningen er blevet afvist. Du kan oprette en ny kategorianmodning efter behov.

## <a name="review-category-requests"></a>Gennemgå kategorianmodninger

Dette afsnit forklarer, hvordan du godkender, afviser og uddelegerer kategorianmodninger, som kreditorer har sendt, og hvordan du får vist fuldførte anmodninger. Disse handlinger i arbejdsgangen omfatter hele kategorianmodningen.

### <a name="view-category-requests"></a>Få vist kategorianmodninger

Benyt følgende fremgangsmåde for at få vist kategorianmodninger.

1. Gå til **Indkøb og forsyning \> Kreditorer \> Anmodninger om kreditorsamarbejde \> Kategorianmodninger**.

    Siden **Kategorianmodninger** vises. Standardsidevisningen viser kategorianmodninger med statussen *Ventende handling*.

1. Hvis du vil have vist alle anmodninger, skal du vælge *Alle* i feltet **Vis anmodninger**.
1. Åbn en anmodning for at gennemse og redigere den efter behov.

    - Hvis du vil have vist listen over kategorier, der aktuelt er inkluderet i anmodningen, skal du vælge oversigtspanelet **Anmodede kategorier**.
    - Hvis du vil se de aktive kategorier, skal du åbne faktaboksen **Aktive kategorier** til højre på siden.
    - Hvis der er sendt dokumenter, viser knappen **Vedhæftede filer** (papirklips) i handlingsruden en optælling af de tilknyttede dokumenter. Klik på knappen **Vedhæftede filer** for at få vist vedhæftede dokumenter. Vælg derefter det dokument, der skal vises, og vælg **Åbn** for at få det vist.
    - Hvis du vil knytte et dokument til anmodningen, skal du vælge **Vedhæftede filer** i handlingsruden. Vedhæftede dokumenter vil være tilgængelige for godkendere, når de gennemgår kategorianmodningen.
    - Hvis du vil fjerne et vedhæftet dokument fra anmodningen, skal du vælge **Vedhæftede filer** i handlingsruden. Vælg det dokument, du vil fjerne, og vælg derefter **Slet** i handlingsruden.
    - I handlingsruden skal du vælge **Arbejdgang** for at få vist arbejdsganghistorikken. Vælg **Mere** og derefter **Arbejdsgangshistorik** i indstillingerne for arbejdsgangen. Siden **Arbejdsgangshistorik** vises.

### <a name="approve-a-pending-category-request"></a>Godkende en ventende kategorianmodning

Hvis du vil godkende en ventende kategorianmodning, skal du benytte følgende fremgangsmåde.

1. Gå til **Indkøb og forsyning \> Kreditorer \> Anmodninger om kreditorsamarbejde \> Kategorianmodninger**.
1. Vælg den ventende anmodning, du vil godkende.
1. Gennemgå kategorianmodningen.
1. Valgfrit: Vælg en årsagskode i feltet **Årsagskode** i oversigtspanelet **Generelt**. Skriv derefter en kommentar om årsagskoden i feltet **Årsagskommentar**.
1. Vælg **Arbejdsgang** i handlingsruden.
1. Vælg **Godkend** i indstillingerne for arbejdsgangen.
1. Angiv de supplerende oplysninger, der kræves, i feltet **Kommentar**. Vælg derefter **Godkend** for at fuldføre anmodningen.

    Status for kategorianmodningen ændres til _Godkendt_, og indkøbskategorierne føjes til kreditorkontoen.

### <a name="reject-a-pending-category-request"></a>Afvise en ventende kategorianmodning

Hvis du vil afvise en ventende kategorianmodning, skal du benytte følgende fremgangsmåde.

1. Gå til **Indkøb og forsyning \> Kreditorer \> Anmodninger om kreditorsamarbejde \> Kategorianmodninger**.
1. Vælg den ventende anmodning, du vil afvise.
1. Gennemgå kategorianmodningen.
1. Vælg **Rediger** i handlingsruden.
1. Vælg en årsagskode i feltet **Årsagskode** i oversigtspanelet **Generelt**. Skriv derefter en kommentar om årsagskoden i feltet **Årsagskommentar**.
1. Vælg **Gem** i handlingsruden.
1. Vælg **Arbejdsgang** i handlingsruden.
1. Vælg **Mere** og derefter **Afvis** i indstillingerne for arbejdsgangen.
1. Angiv de supplerende oplysninger, der kræves, i feltet **Kommentar**. Vælg derefter **Afvis** for at fuldføre anmodningen.

    Statussen for kategorianmodningen ændres til _Afvist_. På dette tidspunkt kan kreditoren oprette en ny kategorianmodning efter behov.

### <a name="delegate-a-pending-category-request"></a>Uddelegere en ventende kategorianmodning

Hvis du vil uddelegere en ventende kategorianmodning til en anden bruger, skal du benytte følgende fremgangsmåde.

1. Gå til **Indkøb og forsyning \> Kreditorer \> Anmodninger om kreditorsamarbejde \> Kategorianmodninger**.
1. Vælg den ventende anmodning, du vil godkende.
1. Vælg **Arbejdsgang** i handlingsruden.
1. Vælg **Mere** og derefter **Uddeleger** i indstillingerne for arbejdsgangen.
1. Vælg den bruger i feltet **Bruger**, som skal tildeles den kategorianmodning, der skal gennemgås.
1. Angiv de supplerende oplysninger, der kræves, i feltet **Kommentar**.
1. Vælg **Uddeleger** for at fuldføre uddelegeringen. Den valgte bruger kan nu gennemgå kategorianmodningen.

### <a name="view-procurement-categories-for-a-vendor"></a>Få vist indkøbskategorier for en kreditor

Hvis du vil se indkøbskategorier for en kreditor, efter kategorianmodningen er godkendt, skal du benytte følgende fremgangsmåde.

1. Gå til **Indkøb og forsyning \> Kreditorer \> Alle kreditorer**.
1. Vælg den leverandør, du vil have vist indkøbskategorier for, på siden **Alle leverandører**.
1. Åbn fanen **Generelt** i handlingsruden, og vælg **Kategorier** i gruppen **Konfigurer**.

    Siden **Kategorier** vises. Oversigtspanelet **Indkøb** viser de indkøbskategorier, der er føjet til kategorianmodningen.

1. Du kan foretage ændringer i oversigtspanelet **Indkøb**, hvis det er nødvendigt. Du kan f.eks. angive feltet **Kreditokategoristatus** til _Foretrukket_.
