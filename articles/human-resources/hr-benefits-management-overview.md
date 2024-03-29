---
title: Oversigt over administration af frynsegoder
description: Denne artikel indeholder en oversigt over funktionen Frynsegodeadministration i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/06/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e3fa839b6e0f3cbaea8d2225b5a42ee8a368272
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336936"
---
# <a name="benefits-management-overview"></a>Oversigt over administration af frynsegoder

Hvis du vil forblive konkurrencedygtig, skal du tilbyde en lang række frynsegoder for at tiltrække og holde på dine bedste medarbejdere. Ud over standardfrynsekoder som sundhedsforsikring og tandlægedækning kan det også være en god idé at tilbyde udvidede tjenester som hjælp til adoption, rekreative ordninger og beklædningsgodtgørelse. Frynsegodeadministration i Microsoft Dynamics 365 Human Resources er en fleksibel løsning, som understøtter en lang række frynsegodeindstillinger. Human Resources inkluderer også en brugervenlig medarbejderoplevelse, der viser det, du tilbyder.

- Forbedrede frynsegodeplaner giver dig mulighed for at oprette og administrere unikke frynsegodeplaner og understøtte komplekse satstabeller for frynsegoder og indlejrede niveauer. Du kan nemt oprette frynsegodeprogrammer, pakker og regler for automatisk registrering, der gør det nemmere for medarbejderne.
- Med flekskreditprogrammer kan du gøre det muligt at understøtte pension og andre levetidshændelser.
- Omfattende berettigelsesregler sikrer, at de rigtige fordele stilles til rådighed for de rette medarbejdere.
- Onlinetilmeldinger til frynsegoder giver medarbejderne en nem oplevelse.
- Den kvalificerede levetidshændelsesproces understøtter fremtidige levetidshændelser.

Hvis du vil have adgang til demodataene, skal du geninstallere dit sandkassemiljø.

> [!NOTE]
> Du kan nu tilpasse siderne for Frynsegodeadministration. Brugerdefinerede felter, der vedrører dækningssatser, kan føjes til siden **Dækningsindstilling** for frynsegodeplaner. Du kan finde flere oplysninger om arbejde med brugerdefinerede felter i [Brugerdefinerede felter](hr-developer-custom-fields.md).
>
> ![Brugerdefinerede felter for administration af frynsegoder](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Aktivere Administration af frynsegoder

I disse artikler beskrives, hvordan du slår funktioner til i Human Resources. Det forklarer også, hvilke eksisterende funktioner i Human Resources der erstattes af Frynsegodeadministration, og hvilke funktioner der deaktiveres, når du aktiverer Frynsegodeadministration.

> [!IMPORTANT]
> Når du aktiverer Administration af frynsegoder i et **produktionsmiljø**, kan du ikke deaktivere det. Vi anbefaler, at du aktiverer og tester Administration af frynsegoder i et **sandkassemiljø**, før du aktiverer det i et **produktionsmiljø**. Der er betydelige forskelle mellem den gamle frynsegodefunktionalitet og de nye funktioner til administration af frynsegoder, der kræver yderligere opsætning, og som skal testes, før de bringes i produktion.

Du kan finde flere oplysninger under [Administrere funktioner](hr-admin-manage-features.md).

## <a name="process-overview"></a>Procesoversigt

Processen til konfiguration af frynsegoder omfatter følgende opgaver:

1.  Konfigurer de krævede oplysninger om frynsegoder.
2.  Konfigurer de valgfrie oplysninger om frynsegoder.
3.  Konfigurer frynsegodeplaner.
4.  Konfigurer flekskreditprogrammer (valgfrit).
5.  Konfigurer krævede medarbejderoplysninger.
6.  Konfigurer valgfrie medarbejderoplysninger.
7.  Behandl medarbejdere for at fastlægge berettigelse.
8.  Medarbejderne vælger planer via medarbejderselvbetjening (valgfrit).
9.  Bekræft valg af medarbejderplan.
10. Behandling af livshændelse (valgfrit).
11. Satsopdateringer (valgfrit).

## <a name="set-up-required-benefit-information"></a>Konfigurere krævede oplysninger om frynsegoder

Før medarbejdere kan tilmeldes planerne, skal der konfigureres flere komponenter:

- **Parametre for frynsegodeadministration** – Disse indstillinger deles på tværs af virksomheder. Du kan angive standardårsagskoder, aktivere indstillingen **Årsløn for frynsegoder**, angive en standardbetalingsfrekvens for nye ansættelser og aktivere livshændelser. Du kan finde flere oplysninger under [Angive parametre for frynsegodeadministration](hr-benefits-setup-parameters.md).
- **Indstillinger for berettigelse for personlig kontakt** – Personlige kontakter er personer, der skal være enten afhængige eller modtagere afde planer, der er konfigureret. De er typisk børn, ægtefæller eller betroede organisationer. Du kan finde flere oplysninger under [Konfigurere indstillinger for personlig kontaktberettigelse](hr-benefits-setup-contact-eligibility-options.md).
- **Dækningsindstillinger** – Konfigurer de dækningstyper, der er tilgængelige for en plan. Du skal definere specifikt, hvem der skal dækkes, eller hvor meget dækning der er til rådighed. Du kan finde flere oplysninger under [Opret dækningsindstillinger](hr-benefits-setup-coverage-options.md).
- **Plantyper** – Konfigurer de plantyper, der er tilgængelige, når du opretter en frynsegodeplan. Som eksempler på plantyper kan nævnes **Tandlæge**, **Optiker** og **Opsparing**. Nogle vigtige indstillinger for plantypen afgør, hvilke indstillinger der er tilgængelige i frynsegodeplanen. Yderligere oplysninger finder du i [Oprette plantyper](hr-benefits-setup-plan-types.md).
- **Berettigelsesregler** – Berettigelsesregler bruges til at bestemme, om en medarbejder er berettiget til en plan. Der skal knyttes mindst én berettigelsesregel til hver frynsegodeplan. Du kan finde flere oplysninger under [Konfigurere berettigelsesregler og -indstillinger](hr-benefits-setup-eligibility-rules.md).
- **Betalingsfrekvenser** – Betalingsfrekvenser skal bruges ved konfiguration af frynsegodesatser. Den betalingsfrekvens, der bruges på en sats, er med til at identificere det beløb, som medarbejderen og/eller arbejdsgiveren skylder hver uge, hver måned eller på årsbasis. Du kan finde flere oplysninger under [Konfigurere betalingsfrekvenser](hr-benefits-setup-payment-frequencies.md).
- **Satser** – Satser definerer, hvor meget et frynsegode vil koste medarbejderen eller arbejdsgiveren. Hvis der skal returneres penge til en medarbejder (f.eks. en kreditering af et medlemsskab af et fitnesscenter), angives en negativ sats. Du kan finde flere oplysninger i [Konfigurere satser](hr-benefits-setup-rates.md).
- **Niveausatser** – Niveausatser bruges, når en sats skal ændres på baggrund af visse kriterier. Den mest almindelige niveausats er et enkelt niveau baseret på alder. Der kan dog også konfigureres dobbelte niveausatser, hvor satsen kan ændre sig ud fra køn, alder eller andre kriterier.
- **Fradrag** – Fradragene er grundlæggende de hovedoplysninger eller -koder, som overføres til lønsystemet for at identificere fradraget for frynsegodet. Du skal konfigurere disse fradrag, fordi de skal angives i frynsegodeplanen. Du kan finde flere oplysninger i [Konfigurere fradrag](hr-benefits-setup-deductions.md).
- **Frynsegodeperioder** – En frynsegodeperiode er den periode, hvor medarbejderne skal have frynsegodedækning. Det kaldes også et planår. De åbne tilmeldingsperioder konfigureres også her.

## <a name="set-up-optional-benefit-information"></a>Konfigurere de valgfrie oplysninger om frynsegoder

Følgende komponenter behøver ikke at være konfigureret for at oprette en frynsegodeplan:

- **Programmer** – Et program er et sæt frynsegoder, der styres af de samme berettigelsesregler. Alle i salgsafdelingen kan f.eks. få en mobiltelefon.
- **Bundter** – Et bundt er en gruppe af frynsegoder, hvor der skal vælges én plan, før indstillingen kan vælges yderligere planer. En sundhedsforsikring, der kan trækkes fra, kan f.eks. være bundtet med en sundhedsopsparingskonto (HSA).
- **Livshændelsestyper** – Livshændelser er hændelser, der gør det muligt at ændre en medarbejders dækning. Livshændelsestyper er knyttet til en plantype. En sundhedsforsikrings plantype kan f.eks. tillade ændringer af planer som følge af en fødsel eller adoption eller på grund af en ændring af civilstand. Det er dog ikke muligt at foretage ændringer af en forsikrings plantype som følge af livshændelser. Du kan finde flere oplysninger under [Konfigurere livshændelsestyper](hr-benefits-setup-life-event-types.md).
- **Ventetider og venteperioder** – Der kan angives en venteperiode for dækningen i en frynsegodeplan. En nyansat medarbejder kan f.eks. først tilmelde sig en 401(k) efter tre måneders ansættelse. I dette tilfælde er ventetiden tre måneder. Ventedage bruges i venteperioden, hvis nye tilmeldinger kun kan behandles og sendes til udbyderen på en bestemt dag i måneden. Hvis f.eks. 401(k)-tilmeldinger kun kan behandles den 15. i måneden efter tre måneders ansættelse, er venteperioden, der er konfigureret til tre måneder, og ventetiden er den 15. i måneden. Du kan finde flere oplysninger i [Konfigurere ventedage](hr-benefits-setup-waiting-days.md) og [Konfigurere venteperioder](hr-benefits-setup-waiting-periods.md).
- **Årsagskoder** – Årsagskoder bruges til at forklare, hvorfor et frynsegode kan ændres for en medarbejder. Du kan finde flere oplysninger i [Konfigurere årsagskoder](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Konfigurere frynsegodeplaner

Når du konfigurerer en frynsegodeplan, skal du udføre følgende trin, før medarbejdere kan tilmeldes:

- Tildel en frynsegodeperiode.
- Tilknyt dækningsindstillinger.
- Angiv en gyldig fra- og gyldig til-dato under fanen **Generelt**.
- Tildel mindst én berettigelsesregel.
- Angiv feltet **Tillad/fortsæt tilmelding** under fanen **Opsætning**.

Du kan finde flere oplysninger om at konfigurere frynsegodeplaner under [Konfigurere frynsegodeplaner](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Konfigurere flekskreditprogrammer (valgfrit)

Du kan bruge flekskreditprogrammer til at tilmelde medarbejdere til frynsegoder ud fra et foruddefineret antal flekskreditter. Medarbejderne kan vælge, hvordan deres flekskreditter skal tildeles. Hvis medarbejdere f.eks. allerede er dækket af deres ægtefælles sundhedsforsikring, behøver de ikke bruge deres kredit til sundhedsdækning. Derfor kan de bruge dem til andre frynsegoder i stedet for. Du kan finde flere oplysninger om flekskreditprogrammer i [Konfigurere flekskreditprogrammer](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Konfigurere krævede medarbejderoplysninger

Før du kan tilmelde medarbejdere til frynsegoder, skal du angive de nødvendige oplysninger om dem. 

Medarbejderen skal være tildelt en **stilling**. Du kan tildele en **stilling** til medarbejderen på siden **Arbejder** eller **Stilling** ved at opdatere **Medarbejdertildeling**. 

Derefter skal medarbejdere tilmeldes en fast kompensationsplan på deres respektive startdatoer eller have et beløb for **Årlig frynsegodeløn**. Før der tildeles **Fast løn** til en medarbejder, skal der tildeles en **stilling**. 

> [!NOTE] 
> **Startdato for fast løn** kan ikke være før **Dato for stillingstildeling**.

Eller hvis du har en medarbejder, der modtager supplerende kompensation såsom provision, kan du tilføje et beløb for **Årlig frynsegodeløn** fra medarbejderposten. Human Resources skal bruge beløbet for **Årlig frynsegodeløn** til bestemmelse af dækningsbeløb i stedet for beløbet for **Fast årsløn**. **Årlig løn for frynsegoder** skal være gyldig pr. medarbejderens startdato eller starten af frynsegodeperioden, afhængigt af hvad der er den seneste. Der kræves dog ikke en stilling for at tildele **Årlig løn som personalegoder**. Hvis du vil aktivere funktionen **Årlig løn som personalegoder**, skal du gå til siden **Delte HR-parametre** under fanen **Personalegodeadministration**. Denne funktion er som standard deaktiveret.

> [!IMPORTANT]
> Hvis der både er angivet et beløb for **Fast løn** og **Årlig løn som personalegoder** for en medarbejder, bruges **Årlig løn som personalegoder** til at fastlægge dækningsbeløbene. I afsnittet **Detaljer om ansættelse** på siden **Arbejder** skal du vælge en værdi i feltet **Betalingsfrekvens for frynsegoder**.

## <a name="configure-optional-employee-information"></a>Konfigurere valgfrie medarbejderoplysninger
Når du opretter en frynsegodeplan, som bruger satser, der er baseret på køn eller alder, skal du angive medarbejderens fødselsdato og køn, som kan bruges til at beregne frynsegodeomkostningerne.

## <a name="process-employees-to-determine-eligibility"></a>Behandle medarbejdere for at fastlægge berettigelse
Før medarbejdere kan tilmeldes planer, køres berettigelsesbehandling for at bestemme, hvilke planer de er berettiget til. Du kan få vist resultaterne af berettigelsesprocessen i **resultatvisningen**. Du kan finde flere oplysninger under [Behandle tilmeldings berettigelse](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Medarbejderne vælger planer via **Medarbejderselvbetjening** (valgfrit)

Når der er en åben tilmelding, medarbejdere er nyansatte, eller der indtræffer en livshændelse, kan medarbejdere vælge eller opdatere deres fryensegoder via **Medarbejderselvbetjening**. Du kan finde flere oplysninger under [Konfigurere medarbejderselvbetjening](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Bekræfte valg af medarbejderplan

De frynsegoder, som medarbejderne vælger, skal bekræftes, før medarbejderne betragtes som tilmeldte. Frynsegoder kan også vælges på vegne af en medarbejder. Hvis du vil vælge eller bekræfte frynsegoder, skal du vælge **Arbejderens frynsegodeplaner** på siden **Medarbejder** under fanen **Frynsegoder**. Hvis du vil vælge eller bekræfte frynsegoder for flere medarbejdere, kan du bruge siden **Masseopdatering af medarbejderes frynsegoder**.

## <a name="life-event-processing-optional"></a>Behandling af livshændelse (valgfrit)

I løbet af medarbejderens livscyklus kan de enkelte medarbejdere opleve forskellige livshændelser, f.eks. ændringer i ansættelsen eller ændringer i afhængige eller modtagere. Hvis du vil bruge livshændelser, skal du aktivere dem på siden **Delte Human Resources-parametre**. Konfigurer typer og indstillinger for livshændelser for plantyper.

Før du kan behandle livshændelser, skal du allerede have kørt åben tilmelding mindst én gang i en ansættelsesperiode. I USA foregår åbne tilmeldinger typisk én gang om året. Uden for USA kan åben tilmelding forekomme på ansættelsestidspunktet. Behandling af livshændelser kræver ikke, at arbejderne vælger en frynsegodeplan. Arbejderne skal imidlertid være medtaget i åben tilmeldingsbehandling. Du kan finde flere oplysninger under følgende emner:

- [Behandle livshændelser](hr-benefits-process-life-events.md)
- [Behandle ændringer af livshændelser](hr-benefits-process-life-event-changes.md)
- [Behandle berettigelse til livshændelser](hr-benefits-process-life-event-eligibility.md)

Når behandlingen af livshændelser er fuldført, og så længe tilmeldingsperioden for livshændelser er åben, kan medarbejderne foretage ændringer i de planindstillinger, der påvirkes af livshændelsen. Administratorer kan foretage ændringerne på vegne af medarbejdere. Når tilmeldingsperioden er afsluttet, og der ikke er knyttet nogen ubekræftede plantyper til livshændelsestransaktionen, lukkes transaktionen.

Alle de planer, der påvirkes af livshændelsen, skal enten vælges eller frafaldes, og de skal derefter bekræftes. Hvis en plan ikke er valgt, ikke er frafaldet og derfor ikke er bekræftet, bliver livshændelsestransaktionen ikke lukket.

Administratorer kan lukke en livshændelsestransaktion manuelt efter behov ved at markere den og derefter vælge **Luk**. Hvis der er ikke-bekræftede planer i transaktionen, og en administrator vil lukke den, kan lukning af livshændelsen begrænse redigeringer af disse planer.

Lukkede livshændelser kan ikke slettes.

Administratorer kan genåbne en livshændelsestransaktion efter behov ved at markere den og derefter vælge **Åbn igen**.

## <a name="rate-updates-optional"></a>Satsopdateringer (valgfrit)

Nogle gange ændres satsen for et frynsegode i planlægningsperioden. Hvis du vil opdatere satserne for medarbejdere, der allerede er tilmeldt planen, skal du behandle satsændringerne. Du kan finde flere oplysninger under [Behandle satsændringer](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
