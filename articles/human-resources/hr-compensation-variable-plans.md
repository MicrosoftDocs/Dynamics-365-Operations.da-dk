---
title: Oprette planer for variabel kompensation
description: I denne artikel beskrives de komponenter, der skal konfigureres, før du kan bruge variabel kompensation og tilmelde en medarbejder til en variabel lønstruktur.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f2f51a095a23b651dca645b14e652519f20037e2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070552"
---
# <a name="create-variable-compensation-plans"></a>Oprette variable kompensationsstrukturer


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Variabel løn udgør en medarbejders uregelmæssige løn såsom bonus eller aktiebonusser. Denne artikel beskriver, hvordan komponenter konfigureres, før du kan bruge variabel kompensation og tilmelde en medarbejder til en variabel lønstruktur.

Beregning af beløb i variabel kompensation for dine medarbejdere kan være baseret på flere faktorer, f.eks. medarbejderens præstation, medarbejderens kompensationsniveau og afdelingens ydeevne.

## <a name="variable-compensation-components"></a>Komponenter i variabel kompensation
### <a name="create-compensation-types"></a>Oprette kompensationstyper

**Variable kompensationstyper** er en nødvendig komponent. **Variable kompensationstyper** beskriver de former for variabel kompensation, som din organisation giver. Desuden kan du angive, om kompensationen er i rede penge eller i en ikke-pengemæssige form, f.eks. aktier.

### <a name="describe-vesting-rules"></a>Beskrive fordelingsregler

Virksomheder kan vælge at konfigurere **Fordelingsregler**. **Fordelingsregler** beskriver, hvordan den variable bonus skal fordeles over tid. En fordelingsregel kan for eksempel angive, at medarbejderen får 25 % af den samlede bonus hvert år i de næste fire år. Fordelingsregler er kun til orientering.

## <a name="variable-compensation-plans"></a>Variabel løn-strukturer
Den **variable lønstruktur** indeholder regler, beregningsmetoder og standardværdier for beregningen af variabel kompensation for tilmeldte medarbejdere. Når du opretter en variabel lønstruktur, skal du angive den variable kompensationstype. Den variable kompensationstype bestemmer, om systemet beregner bonussen som et valutabeløb eller et antal enheder. 

**Begrænsningen af adgangen til valgte roller**-parameter begrænser adgangen til kompensationsplanen til de valgte sikkerhedsroller, der er tildelt den pågældende plan i Personale. Når du f.eks. opretter lønstrukturer, der er for ledere og ikke bør være synlige for alle hr-specifikke roller, kan du bruge denne parameter til at begrænse adgangen til de pågældende lønstrukturer. 

Du skal også angive beregningsmetoden:

-   **Tidspunkt** – Beregningen af den variable bonus er baseret på den faste løn, medarbejderen havde på en bestemt dato. Denne dato angives i proceshændelsen, når nye kompensationsbeløb behandles.
-   **Sammensat** – Et bonusbeløb beregnes for hver entydig fast løn-lønsats, som medarbejderen havde mellem cyklussens startdato og cyklussens slutdato på proceshændelsen. Derefter lægges satserne sammen for at bestemme den endelige bonus. For eksempel blev en medarbejder under cyklussen overført til en anden placering, der havde en anden lønsats. I dette tilfælde reguleres den variable bonus for det tidsrum, hvor medarbejderen havde hver enkelt lønsats.

Størrelsen af den variable bonus kan være baseret på enten en procentdel af medarbejderens almindelige grundlæggende indtjening eller et angivet antal enheder.

-   Vælg indstillingen **Procent af basis** for at indtaste en standardprocent, og angiv, om grundlaget skal være medarbejderens faste lønsats eller kontrolpunktet for medarbejderens kompensationsniveau. Kompensationsniveauet er angivet på medarbejderens job. Et af referencepunkterne i kompensationsstrukturen kan angives som referencepunktet på den faste kompensationsplan. Systemet bruger kompensationsniveauet fra medarbejderens job og opretter krydshenvisninger til det med det referencepunkt, der er angivet på medarbejderens faste lønstruktur for at finde referencepunktbeløbet for medarbejderens kompensationsniveau. Referencepunkbeløbet kan derefter bruges i stedet for medarbejderens faste lønsats som grundlag for bonussen.
-   Vælg indstillingen **Antal enheder** for at angive et standardantal enheder, værdien af hver enkelt enhed og valutaen for enhedsværdien, hvis kompensationsplanen gælder for en ikke-kontant bonus (eksempelvis 200 aktieenheder, som værdiansættes til 40 USD) eller kun antallet af enheder, hvis kompensationsplanen er for en kontantbonus. For en kontantbonus modtager medarbejderen det angivne antal enheder af den valuta, der bruges til fast løn-strukturen (eksempelvis 500 enheder af 1 USD). Kontrolelementet for en til en-relationen kan bruges til at angive, om der er en direkte én til én-tilknytning mellem antallet af enheder og enhedsværdien. Når du opretter en variabel lønstruktur for en kontantbaseret plan ved hjælp af antallet enheder, er denne indstilling automatisk låst til **Ja**, og enhedsværdien er **1.0000**.

Indstillingen **Ansættelsesregel** angiver, om alle medarbejdere skal have den samme stigning uanset datoen for deres ansættelse (**Ansættelsesregel** = **Ingen**), eller om medarbejderne skal modtage en procentdel af bonussen, der er baseret på længden af deres ansættelse i løbet af cyklussen (**Ansættelsesregel** = **Procent**). 

**Regulering** justerer en medarbejders bonus baseret på ydeevnen (performance) af medarbejderens afdeling. Performanceværdier kan indstilles for hver afdeling på siden **Afdelinger** under **Relaterede formularer** &gt; **Kompensation** &gt; **Ydeevne**. Den bonus, som medarbejdere i den pågældende afdeling modtager, afhænger af værdien i feltet **Opnået procent af mål**, der angiver afdelingens ydeevne:

-   Hvis afdelingens ydeevne er 100 procent, medtages bonussen for medarbejderen i den pågældende afdeling med den procentdel, der er angivet i feltet **Udbetaling ved 100 %**.
-   Hvis afdelingens ydeevne er mere end 100 procent, tilføjer systemet den procentdel, der er angivet i feltet **Pr. 1 % over målsætningen** til den procentdel, der er angivet i feltet **Udbetaling ved 100 %**, indtil den værdi, der er angivet i feltet **Højst tilladte udbetaling**, er nået.
-   Hvis afdelingens ydeevne er mere end 100 procent, trækker systemet den procentdel fra, der er angivet i feltet **Pr. 1 % under målsætningen** fra den procentdel, der er angivet i feltet **Udbetaling ved 100 %**, indtil den værdi, der er angivet i feltet **Lavest tilladte udbetaling**, er nået.

**Ttoleranceniveauer** kan angives for grænseværdier i procent, så der vises en advarsel, hvis reguleringen medfører, at procentdelen er uden for procentdelen for grænseværdien. 

Som standard bruger systemet den afdeling, der er angivet for medarbejderens stilling, til medarbejderbonus. Men prisen for nogle medarbejdere kan afhænge af ydeevnen for flere afdelinger. I dette tilfælde kan de forskellige afdelinger og procentdelen af den bonus, der tildeles ydeevnen for hver afdeling, angives ved medarbejderens tilmelding til variabel kompensation. Du kan finde flere oplysninger i afsnittet "Tilmelding til variabel kompensation", der følger nedenfor. 

Regulering bruges kun, hvis **Præstationsløn** er markeret, når kompensationsprocessen køres. 

Under fanen **Niveautilsidesættelser** kan du tilsidesætte bonussens standardprocent eller antal enheder, der er baseret på kompensationsniveauet for medarbejderen. Hvis **Aktiver tilsidesætter for niveauer** er indstillet til **Ja** for medarbejdere, der er tilmeldt den variable lønstruktur, bliver niveauet fra en medarbejders job sammenlignet med niveautilsidesættelser for at bestemme procentdelen eller antallet af enheder for det pågældende niveau. Hvis niveauet ikke findes i tabellen med niveautilsidesættelser, bruges standardprocenten eller antallet af enheder fra fanen **Generelt**. Procent og antal enheder kan også tilsidesættes ved medarbejderens tilmelding til den variable lønstruktur.

## <a name="variable-compensation-enrollment"></a>Tilmelding til variabel kompensation
### <a name="determine-who-is-eligible-for-the-plan"></a>Bestem, hvem der er berettiget til planen

Når du er klar til at tilmelde medarbejdere i en variabel lønstruktur, er det første trin at bestemme, hvem der er berettiget til den kompensation, der er specificeret i strukturen. Du kan ikke tildele strukturen til nogen medarbejdere, medmindre du fastlægger berettigelse. Hvis du vil konfigurere berettigelse, skal du åbne siden **Berettigelsesregler** for at oprette en ny berettigelsesregel til din struktur og derefter definere de kriterier, som en medarbejder skal opfylde, for at være berettiget til kompensationsplanen. Du kan begrænse berettigelse efter afdeling, fagforening, kompensationsområde (lokation), job, jobfunktion, jobtype og/eller kompensationsniveau. Medarbejdere kan kun være tilmeldt en kompensationsstruktur, hvis de opfylder **alle** de kriterier, der er angivet for berettigelsesreglen. 

**Bemærk!** Berettigelsesregler bruges til at fastlægge berettigelse for både fast løn-strukturer og variable lønstrukturer. Berettigelsesreglerne bruger følgende feltet i posterne job, stilling og medarbejder til at afgøre, om en medarbejder er berettiget til en kompensationsplan:

- På siden **Job**:
  -   Feltet **Job**
  -   Felterne **Funktion** og **Jobtype** under fanen **Jobklassificering**
  -   Feltet **Niveau** under fanen **Kompensation**
- På siden **Stillinger**: Felterne **Afdeling** og **Kompensationsområde**.
- På siden <strong>Medarbejdere</strong>: De oplysninger om fagforeninger, som er forbundet med medarbejderen, under <strong>Personlige oplysninger</strong> &gt; <strong>Fagforeninger</strong> på fanen *<strong><em>Arbejder</em></strong>*

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Aktivér tilmelding for den variable lønstruktur

På siden **Variable lønstrukturer** skal du angive indstillingen **Aktivér tilmelding** til **Ja** for at tillade, at berettigede medarbejdere bliver tilmeldt planen.

### <a name="enroll-the-employee"></a>Tilmelde medarbejderen.

Du kan nu tilmelde medarbejder til den variabel lønstruktur. Hvis du vil registrere en medarbejder, skal du gå til siden **Medarbejdere** og vælge medarbejderen. I Handlingsrude skal du derefter klikke på **Kompensation** &gt; **Tilmelding til variabel plan**. 

**Bemærk!** **Tilmelding** skal være indstillet til **Ja** for den variable lønstruktur. Feltet **Plan** viser kun de strukturer, som medarbejderen er berettiget til baseret på de berettigelsesregler, der er konfigureret for disse strukturer. Hvis der ikke er konfigureret en berettigelsesregel for en struktur, vil ingen medarbejdere være berettiget til denne struktur. 

Sørg for, at feltet **Ikrafttrædelsesdato** er indstillet korrekt. Hvis den variable lønstruktur bruger beregningsmetoden **Sammensat**, kan ikrafttrædelsesdatoen for tilmelding blive vurderet under beregning af medarbejderens bonus. 

Du kan bruge fanen **Tilsidesættelser** til at tilsidesætte bestemte værdier for medarbejderen. For eksempel hvis **Ansættelsesregel** er indstillet til **Procent** for planen, og der skal bruges en anden ansættelsesdato under beregning af medarbejderens ansættelsesprocent, kan du angive ansættelsesdatoen i feltet **Dato for ansættelsesregel**. Du kan også tilsidesætte enten værdien **Bonusprocentdel** eller **Antal enheder** for en bestemt medarbejder, afhængigt af indstillingerne for planen. Disse værdier vil stadig blive indregnet af ansættelsesreglen, præstationsfaktorer og andre indstillinger for planen. 

**Organisationsmæssige overstyringer** bruges til at basere en medarbejders bonus på ydeevnen for en eller flere afdelinger. Den procentdel, der er fordelt på tværs af afdelinger, skal give 100 %. Den enkelte medarbejders præstation tages også i betragtning. Disse indstillinger bruges kun, hvis **Præstationsløn** er markeret, når kompensationsprocessen køres.





[!INCLUDE[footer-include](../includes/footer-banner.md)]
