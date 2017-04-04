---
title: Oprette variable kompensationsstrukturer
description: "Variabel løn udgør en medarbejders uregelmæssige løn såsom bonus eller aktiebonusser. Dette emne beskriver de komponenter, der skal konfigureres, før du kan bruge variabel kompensation og melde en medarbejder til en variabel lønstruktur."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Oprette variable kompensationsstrukturer

Variabel løn udgør en medarbejders uregelmæssige løn såsom bonus eller aktiebonusser. I denne artikel beskrives de komponenter, der skal konfigureres, før du kan bruge variabel kompensation og tilmelde en medarbejder til en variabel lønstruktur.

Beregning af beløb i variabel kompensation for dine medarbejdere kan være baseret på flere faktorer, f.eks. medarbejderens præstation, medarbejderens kompensationsniveau og afdelingens ydeevne.

## <a name="variable-compensation-components"></a>Komponenter i variabel kompensation
### <a name="create-compensation-types"></a>Oprette kompensationstyper

**Variable kompensationstyper **er en nødvendig komponent. Variable kompensationstyper giver dig mulighed for at de former for variabel kompensation, som organisationen giver. Desuden kan du angive, om kompensationen er i rede penge eller i en ikke-pengemæssige form, f.eks. aktier.

### <a name="describe-vesting-rules"></a>Beskrive fordelingsregler

Virksomheder kan selv vælge, om de vil konfigurere **fordelingsregler**. Fordelingsregler beskriver, hvordan den variable bonus skal fordeles over tid. En fordelingsregel kan for eksempel angive, at medarbejderen får 25 % af sin samlede bonus hvert år for de næste fire år. Fordelingsregler er kun til orientering.

## <a name="variable-compensation-plans"></a>Variabel løn-strukturer
Den **variable lønstruktur** indeholder regler, beregningsmetoder og standardværdier for beregningen af variabel kompensation for tilmeldte medarbejdere. Når du opretter en variabel lønstruktur, skal du angive variable kompensationstype. Variable kompensationstype bestemmer, om systemet beregner et valutabeløb eller et antal enheder som tildeling. Du skal også angive beregningsmetoden:

-   **Tidspunkt** – beregning af den variable bonus er baseret på den faste løn, medarbejderen havde på en bestemt dato. Denne dato angives under proceshændelsen, når nye kompensationsbeløb behandles.
-   **Sammensat** – Et bonusbeløb beregnes for hver entydig fast løn-lønsats, som medarbejderen havde mellem cyklussens startdato og cyklussens slutdato på proceshændelsen. Derefter tilsættes satserne sammen for at bestemme den endelige bonus. For eksempel under cyklussen overføres en medarbejder til en anden placering, der havde en anden lønsats. I dette tilfælde reguleres den variable bonus for det tidsrum, hvor medarbejderen havde hver enkelt lønsats.

Størrelsen af den variable bonus kan være baseret på enten en procentdel af medarbejderens almindelige grundlæggende indtjening eller et angivet antal enheder.

-   Vælg indstillingen **Procent af basis** for at indtaste en standardprocent, og angiv, om grundlaget skal være medarbejderens faste lønsats eller kontrolpunktet for medarbejderens kompensationsniveau. Kompensationsniveau er angivet på medarbejderens job. En af referencepunkterne i kompensationsstrukturen kan angives som referencepunktet på den faste kompensationsplan. Systemet bruger kompensationsniveau fra medarbejderens job og oprette krydshenvisninger til det med det referencepunkt, der er angivet på medarbejderens faste lønstruktur finde kontrol punkt beløbet til medarbejderens kompensationsniveau. Control point beløb kan derefter bruges i stedet for medarbejderens faste lønsats som grundlag for tildeling.
-   Vælg indstillingen** Antal enheder** for at angive et standardantal enheder, værdien af hver enkelt enhed og valutaen for enhedsværdien, hvis kompensationsplanen gælder for en ikke-kontant bonus (eksempelvis 200 aktieenheder, som værdiansættes til 40 USD) eller kun antallet af enheder, hvis kompensationsplanen er for en kontantbonus. For en kontantbonus modtager medarbejderen det angivne antal enheder af den valuta, der bruges til hans eller hendes fast løn-struktur (eksempelvis 500 enheder 1 USD). Kontrolelementet ansættelsesdato kan bruges til at angive, om der er en direkte én til én-tilknytning mellem antallet af enheder og enhedsværdien. Når du opretter en variabel lønstruktur for en kontant-baseret plan ved hjælp af antallet enheder, denne indstilling skal være låst til **Ja**, og enhedsværdien er **1,0000**.

Den **ansættelsesreglen** indstilling kan du angive, om alle medarbejdere skal have den samme stigning, uanset den dato, de blev hyret (**ansættelsesreglen** = **ingen**), eller om medarbejderne skal modtage en procentdel af den bonus, som er baseret på længden af deres ansættelse i cyklussen (**ansættelsesreglen** = **procent**). 

**Regulering** kan du justere en medarbejders bonus baseret på ydeevnen af medarbejderens afdeling. Performanceværdier kan indstilles for hver afdeling på den **afdelinger** side, under **relaterede formularer**&gt;**løn**&gt;**ydeevne**. Den bonus, som medarbejdere i den pågældende afdeling modtager, afhænger af værdien af den **procent for opnåelsen af målet** felt, der angiver den afdeling ydeevne:

-   Hvis afdelingens ydeevne er 100 procent, medtages bonussen for medarbejderen i den pågældende afdeling med den procentdel, der er angivet i feltet** Udbetaling ved 100 %**.
-   Hvis afdelingens ydeevne er mere end 100 procent, tilføjer systemet den procentdel, der er angivet i feltet **Pr. 1 % over målsætningen** til den procentdel, der er angivet i feltet **Udbetaling ved 100 %**, indtil den værdi, der er angivet i feltet **Højst tilladte udbetaling**, er nået.
-   Hvis afdelingens ydeevne er mere end 100 procent, trækker systemet den procentdel fra, der er angivet i feltet **Pr. 1 % under målsætningen** fra den procentdel, der er angivet i feltet **Udbetaling ved 100 %**, indtil den værdi, der er angivet i feltet **Lavest tilladte udbetaling**, er nået.

Du kan angive** toleranceniveauer** for grænseværdier i procent, så der vises en advarsel, hvis reguleringen medfører, at procentdelen er uden for procentdelen for grænseværdien. 

Som standard søger systemet efter den afdeling, der er angivet på medarbejderens stilling. Men prisen for nogle medarbejdere kan afhænge af ydeevnen for flere afdelinger. De forskellige afdelinger og procentdelen af den bonus, der tildeles udførelsen af hver afdeling kan i så fald angives, for medarbejderens tilmelding til variabel kompensation. Du kan finde flere oplysninger i afsnittet "tilmelding til variabel kompensation", der følger efter. 

Regulering bruges kun, hvis **Præstationsløn** er markeret, når kompensationsprocessen køres. 

Den **niveauer, tilsidesætter** under fanen kan du tilsidesætte bonussen standardprocenten eller antal enheder, der er baseret på kompensationsniveau for medarbejderen. Hvis **Aktiver tilsidesætter for niveauer** er angivet til **Ja** for medarbejdere, der er tilmeldt variable lønstrukturen, tager systemet niveau fra en medarbejders job, og derefter søger efter den i niveauer tilsidesætter tabel til at bestemme den procentdel eller det antal enheder for det pågældende niveau. Hvis niveauet ikke blev fundet i niveauet tilsidesætter tabel, standardprocenten eller antallet af enheder fra den **generelle** fane anvendes. Procent og antal enheder kan også tilsidesættes i medarbejderens tilmelding i variable lønstrukturen.

## <a name="variable-compensation-enrollment"></a>Tilmelding til variabel kompensation
### <a name="determine-who-is-eligible-for-the-plan"></a>Bestem, hvem der er berettiget til planen

Når du er klar til at tilmelde medarbejdere i en variabel lønstruktur, er det første trin at bestemme, hvem der er berettiget til den kompensation, der er specificeret i strukturen. Du kan ikke tildele strukturen til nogen medarbejdere, medmindre du fastlægger berettigelse. Hvis du vil konfigurere berettigelse, skal du åbne siden **Berettigelsesregler** for at oprette en ny berettigelsesregel til din struktur og derefter definere de kriterier, som en medarbejder skal opfylde, for at være berettiget til kompensationsplanen. Du kan begrænse berettigelse efter afdeling, fagforening, kompensationsområde (lokation), job, jobfunktion, jobtype og/eller kompensationsniveau. Medarbejdere kan kun være tilmeldt en kompensationsstruktur, hvis de opfylder **alle** de kriterier, der er angivet for berettigelsesreglen. 

**Bemærk!** Berettigelsesregler bruges til at fastlægge berettigelse for både fast løn-strukturer og variable lønstrukturer. Berettigelsesreglerne bruger følgende feltet i posterne job, stilling og medarbejder til at afgøre, om en medarbejder er berettiget til en kompensationsplan:

-   På siden **Job**:
    -   Feltet **Job**
    -   Felterne **Funktion** og **Jobtype** under fanen **Jobklassificering**
    -   Feltet **Niveau** under fanen **Kompensation**
-   På siden **Stillinger**: Felterne **Afdeling** og **Kompensationsområde**.
-   På den **medarbejdere** side: oplysninger om fagforeninger, som er knyttet til medarbejderen under **personlige oplysninger**&gt;**fagforeninger** på den *** arbejder *** fane

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Aktivér tilmelding for den variable lønstruktur

På siden **Variable lønstrukturer** skal du angive indstillingen **Aktivér tilmelding** til **Ja** for at tillade, at berettigede medarbejdere bliver tilmeldt planen.

### <a name="enroll-the-employee"></a>Tilmelde medarbejderen.

Du kan nu tilmelde medarbejder til den variabel lønstruktur. Hvis du vil registrere en medarbejder, skal du gå til siden **Medarbejdere** og vælge medarbejderen. Klik på ruden handling **løn**&gt;**tilmelding til variabel plan**. 

**Bemærk!** **Tilmelding** skal være indstillet til **Ja** for den variable lønstruktur. Den **Plan** viser kun de planer, som medarbejderen er berettiget til, baseret på de regler for støtteberettigelse, der er konfigureret for disse planer. Hvis en berettigelsesregel ikke er angivet for en plan, vil ingen medarbejdere være berettiget til denne plan. 

Sørg for, at den **ikrafttrædelsesdato** er angivet korrekt. Hvis variable lønstrukturen bruger den **sammensat** beregningsmetoden ikrafttrædelsesdatoen for tilmelding kan betragtes under beregning af medarbejderens bonus. 

Du kan bruge den **tilsidesætter** tab for at tilsidesætte bestemte værdier for medarbejderen. For eksempel hvis **ansættelsesreglen** er indstillet til **procent** på planen, og en anden ansættelsesdato, der skal bruges under beregning af medarbejderens leje procent, kan du angive ansættelsesdatoen den **ansætte dato** felt. Du kan også tilsidesætte enten den **bonusprocent** værdi eller den **antal enheder** værdi for en bestemt medarbejder, afhængigt af indstillingerne for planen. Disse værdier vil stadig indregnes ved ansættelsesreglen præstationsfaktorer og andre indstillinger på planen. 

**Tilsidesættelser af organisatoriske** bruges til at basere en medarbejders bonus på ydeevnen for en eller flere afdelinger. Den procentdel, der er fordelt på tværs af afdelinger skal give 100 %. Medarbejderens enkelte medarbejders præstation tages også i betragtning. Disse indstillinger bruges kun, hvis **præstationsløn** er markeret, når der køres kompensationsprocessen.

<a name="see-also"></a>Se også
--------

[Kompensationsplaner](compensation-plans.md)


