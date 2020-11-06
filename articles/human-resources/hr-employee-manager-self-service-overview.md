---
title: Oversigt over medarbejderes og lederes selvbetjening
description: Denne artikel giver et overblik over arbejdsområdet til selvbetjening for medarbejdere og ledere.
author: andreabichsel
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 116c85c53b0ec2fe1e1fd2d1fbc2738f5b6351fb
ms.sourcegitcommit: e100c1c7c8dcdacf066defc206dd2f44b8ce6100
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4057046"
---
# <a name="employee-and-manager-self-service-overview"></a>Oversigt over selvbetjening for medarbejdere og ledere

Denne artikel giver et overblik over arbejdsområdet til selvbetjening for medarbejdere og ledere.

## <a name="edit-personal-details"></a>Rediger personlige oplysninger

Hvis du vil tilføje eller ændre personlige oplysninger, skal du se under [Redigere personlige oplysninger](hr-employee-manager-self-service-edit-personal-information.md).

## <a name="user-not-assigned-to-a-worker-record"></a>Brugeren er ikke tildelt en arbejderpost

Hvis du ikke har knyttet din bruger til en **Arbejder** -post på siden **Brugere** , vises følgende meddelelse:

**Dit bruger-id er ikke tilknyttet til din medarbejderpost i systemet. Du kan ikke få vist eller opdatere dine oplysninger, før id'et er tilknyttet. Kontakt din chef eller dit supportteam for at få hjælp.**

Hvis du vil knytte en bruger til en **Arbejder** -post, skal du navigere til **Brugere** og vælge brugeren. Vælg **Rediger** , tilføj den tilsvarende arbejder i feltet **Person** i formularen, og vælg **Gem**. Nu skulle du have adgang til Medarbejderselvbetjening.

## <a name="security-requirements-for-employee-and-manager-self-service"></a>Sikkerhedskrav til medarbejder- og lederselvbetjeningstjeneste

Medarbejder- og lederselvbetjeningstjeneste kræver to sikkerhedsroller:

- Medarbejdere kræver medarbejderrollen.
- Ledere kræver både medarbejder- og lederrolle.

>[!NOTE]
>Du kan også bruge brugerdefinerede roller til at få adgang til Medarbejder- og lederselvbetjeningstjeneste, så længe de har fået adgang til medarbejder- og lederarbejdsområder.<br>
>Lederens adgang til medarbejderoplysninger er baseret på det aktuelle stillingslinjehierarki, der er defineret i Human Resources.

## <a name="employee-self-service"></a>Medarbejderselvbetjening

Fanen **Mine oplysninger** indeholder følgende oplysninger for Medarbejderselvbetjening.  

### <a name="summary"></a>Resumé

**Workflowopgaver, der er tildelt mig** viser alle de godkendelser og arbejdsgangselementer, der er tildelt medarbejderen. Du kan konfigurere elementer i arbejdsgangen til at sende mails til brugeren.

**Spørgeskemaer, der er tildelt til mig** viser alle planlagte spørgeskemaer, der er tildelt direkte til medarbejderen eller gruppen.

**Firmaadressekartotek** gør det muligt for medarbejdere at se oplysninger, der er relateret til enkeltpersoner i organisationen. Offentlige kontaktpersoners oplysninger er tilgængelige for alle medarbejdere. Firmaadressekartoteket er begrænset til det firma, som medarbejderen har logget på.

**Teamkalender** indeholder dit teams kalenderoplysninger. Du kan finde flere oplysninger i [Vise team- og firmakalendere](hr-employee-self-service-calendar.md).

### <a name="my-career-information"></a>Mine karriereoplysninger

Sektionen **Mine karriereoplysninger** i Medarbejderselvbetjening indeholder kort, der er relateret til orlov og fravær, performancestyring, kompetencer, frynsegoder, opgaver og vedhæftede filer.

Kortet **Fritidssaldi** viser saldiene for alle tilmeldte planer. Dette kort viser din forventede saldo baseret på periodiseringsmetoden. Du kan angive og sende anmodninger om fritid, som derefter gennemgår en arbejdsgangsproces for godkendelse. Du kan finde flere oplysninger om orlov og fravær under [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md).

På **Opgave** -kortet vises de opgaver, der er tildelt til dig, og du kan få dem vist og administrere dem.

Kortet **Næste registrerede kursus** viser det næste kursus, du er tilmeldt. Du kan se og tilmelde dig alle åbne kurser. Alle kurser, der er åbne for tilmelding, har status **Startet** , og der er muligt for medarbejderne selv at tilmelde sig på dette kort. Afhængigt af organisationens indstillinger skal din tilmelding til et kursus evt. gennemgå en godkendelsesproces.

På kortet **Certifikat** vises certifikatet og udløbsdatoen for det certifikat, der udløber tættest på dags dato. Du kan opdatere, tilføje eller fjerne certifikater. Afhængigt af organisationens indstillinger skal certifikatopdateringer evt. gennemgå en godkendelsesproces.

Kortet **Næste planlagte gennemsyn** viser din næste performancegennemgang. Du kan starte en ny gennemgang fra dette kort. Din chef eller HR-medarbejder kan også starte gennemgang. Afhængigt af organisationens indstillinger kan du evt. også se, opdatere og sende afslutningsgennemgange fra dette kort.

Du kan administrere dine mål med kortet **Performancemål**. Dette kort viser det antal mål, du har i hver status ( **Ikke startet** , **Holder tidsplanen** og **Skal forbedres** ). Du kan oprette, opdatere og fjerne mål, afhængigt af den tildelte rollebaserede sikkerhed. Hvis du vil, kan du tilføje nye mål fra grupper eller skabeloner. Ledere og HR-medarbejdere kan også oprette mål på vegne af medarbejdere og bestemme, hvor detaljerede de enkelte mål skal være. Ledere og medarbejdere kan samarbejde om mål og opdatere aktiviteter, målinger og status. Du kan også medtage vedhæftede filer.

Du kan få vist dine eksisterende færdigheder på kortet **Færdigheder**. Du kan opdatere færdigheder, tilføje nye eller fjerne dem, der ikke længere er relevante. Afhængigt af organisationens indstillinger skal ændringer af dine færdigheder evt. gennemgå en godkendelsesproces.

Du kan få vist den aktuelle kompensation på kortet **Kompensation**. Vælg **Vis** for at få vist din årlige løn og beløbet for den seneste stigning. Hvis du er ansat i mere end ét firma, vises hvert årlige beløb på kortet. Hvis du vil have vist dine detaljerede kompensationshistorik, skal du vælge det årlige lønbeløb for at åbne formularen **Historik for fast og variabel kompensation**. Fremtidig kompensation vises ikke i denne formular. Hvis du har mere end én ansættelse, kan du skifte mellem firmaer i denne formular for at få vist din kompensationshistorik uden at skulle logge på de enkelte firmaer.

Få vist og administrere dokumenter ved hjælp af kortet **Vedhæftede filer**. Du kan administrere alle **Eksterne** vedhæftede filer. Både HR- og andre medarbejdere kan tilføje vedhæftede filer via Medarbejderselvbetjening eller formularen **Arbejder**. Vedhæftede filer er som standard indstillet til **Ekstern**.

### <a name="additional-information"></a>Yderligere oplysninger

Dette afsnit indeholder links til andre Medarbejderselvbetjenings-områder som områderne i afsnittet **Mine karriereoplysninger**.

Du kan tilmelde dig frynsegoder via linket **Frynsegoder**. Du kan finde flere oplysninger om administration af frynsegoder under [Oversigt over frynsegoder](hr-benefits-management-overview.md)

Under **Performance** kan du vælge **Performancekladder** for at oprette performancekladdeposter, der kan bruges til både performancemål og -gennemgange. Du kan vælge **Send tilbagemelding** for at give andre medarbejdere i organisationen en tilbagemelding. Afhængigt af organisationens indstillinger kan e-mails sendes til modtager, afsender og ledere. Du kan sende tilbagemeldinger til alle medarbejdere i organisationen. Afsendelse af tilbagemeldinger er ikke begrænset til firmaet.

Under **Kompetencer** kan du foretage ændringer af **Kurser** , **Uddannelse** , **Tillidsposter** og **Erhvervserfaring**. Afhængigt af organisationens indstillinger skal opdateringer af disse kompetencer evt. gennemgå en godkendelsesproces.

Du kan se jobdetaljer under **Organisation**. Jobdetaljer omfatter færdigheder, certifikater og ansvarsområder for din primære stilling. Du kan også se et udlånt udstyr, der er tjekket ud til dig. Afhængigt af organisationens indstillinger skal ændringer af lånt udstyr evt. gennemgå en godkendelsesproces.

Under **Spørgeskema** kan du se udfyldte spørgeskemaer. Du kan også se spørgeskemaer, der ikke er udfyldt, for hele firmaet. Du kan vælge at udfylde et spørgeskema på et hvilket som helst tidspunkt. Forfatteren af spørgeskemaet kan bestemme tidsrammen, og hvem spørgeskemaet gælder for.

Du kan konfigurere brugerdefinerede links i **Personaleparametre**. Du kan f.eks. definere links til lønopgørelser, årsafslutningsdokumentation eller eksterne løsninger. Disse links vises nederst i denne sektion, men du kan flytte dem ved hjælp af tilpasning.

Du kan også oprette yderligere faner ved at integrere Power Apps i arbejdsområdet Medarbejderselvbetjening. Brug menuen **Indstillinger** til at tilpasse siden med en hvilken som helst Power Apps. I menuen **Indstillinger** kan du vælge at tilføje en Power App, angive detaljerne og indsætte appen. Power Apps vises som standard som den første fane i rækkefølgen. Du kan ændre rækkefølgen ved hjælp af standardtilpasning.

## <a name="my-team"></a>Mit team

Fanen **Mit team** indeholder følgende oplysninger for Chefselvbetjening. Kun ledere har adgang til fanen **Mit team**.

### <a name="personnel-actions"></a>Personalehandlinger

Personalehandlinger vises på basis af konfigurationsindstillinger i **Delte parametre for personale** og **Personaleparametre**. Når personalehandlinger er aktiveret for **Arbejdere** , aktiveres nye menuindstillinger, herunder:

- **Anmod om ny medarbejder**
- **Anmod om ny kontrahent**
- **Anmod om arbejderdelegering**
- **Anmod om opsigelse**
- **Anmod om ændring af løn**

Du kan konfigurere disse indstillinger, så der udføres en valgfri gennemgangs- og godkendelsesarbejdsgang.

Hvis du aktiverer **Stillingshandlinger** , aktiveres følgende indstillinger:

- **Anmod om ny stilling**
- **Anmod om ændring af stillingsdetaljer**

Du kan også konfigurere disse indstillinger, så der udføres en valgfri gennemgangs- og godkendelsesarbejdsgang.

### <a name="summary"></a>Resumé

Oplysningerne i sektionen **Resume** afhænger af de indstillinger, der er valgt i **Personaleparametre**. Under fanen **Chefselvbetjening** på siden **Personaleparametre** kan du konfigurere indstillinger for visning af poster, der er ved at udløbe, og åbne stillinger. Aktivering af disse indstillinger bestemmer, hvad ledere kan se i sektionen **Resume**.

Du kan konfigurere følgende felter for ledere:

- **Certifikater, som udløber for mit team**
- **Identifikationsnumre, der udløber for mit team**
- **Prøvetider, der udløber for mit team**
- **Screeninger, der udløber for mit team**
- **Test, der udløber for mit team**
- **Åbne stillinger til direkte og/eller udvidede rapporter**
- **Afventer anmodninger om fridage for mit team**
- **Vurdering af færdigheder i team**
- **Analyse af kompetencekløft**
- **Performancekladder for team**
- **Mål for teamperformance**
- **Evalueringer af teamperformance**
- **Eksisterende arbejdere**

Du kan konfigurere følgende indstillinger for ledere til at foretage ændringer eller tilføje anmodninger om orlov på vegne af deres direkte rapporter:

- Certifikater
- Kurser
- Udlånsemner
- Færdigheder
- Orlovs- og fraværsanmodninger

### <a name="my-team-information"></a>Mine teamoplysninger

Mine teamoplysninger giver ledere mulighed for at få vist og opdatere direkte underordnede og underordnede med udvidelser. Hvis du vil have adgang til underordnede med udvidelser, skal du vælge den medarbejder, der har direkte underordnede, og derefter vælge **Vis team** på kortet. Der gælder samme indstillinger for underordnede med udvidelser som for direkte underordnede. 

#### <a name="summary-tab"></a>Fanen Resume

Fanen **Resume** giver en hurtig visning af dine direkte underordnede. Hvis arbejdere rapporterer til en direkte underordnet, viser kortet antallet af direkte underordnede i den øverste sektion sammen med knappen **Vis team**. Indstillingerne over de enkelte kort gælder for den valgte medarbejder. Hvis du f.eks. vil angive en orlovsanmodning på vegne af en medarbejder, skal du vælge medarbejderen og derefter vælge **Anmod om fravær** over kortene. 

Hvis du vælger knappen **Detaljer** , efter at du har valgt en medarbejder, vises følgende indstillinger:

- **Certifikater**
- **Kompensation**
- **Kurser**
- **Evalueringer**
- **Fridage**
- **Udlånte emner**
- **Performancemål**
- **Tilmeldte kurser**
- **Færdigheder**
- **Send tilbagemelding**

Afhængigt af organisationens indstillinger kan du enten foretage ændringer eller få vist oplysninger.

#### <a name="position-tab"></a>Fanen Stilling

Fanen **Stillinger** indeholder en oversigt over medarbejdere i deres primære stilling. Navn, felt og afdeling vises i overskriftsområdet på hvert kort. Dette kort omfatter:

- **Anciennitetsdato** – Vises fra sektionen Arbejderoversigt i formularen Arbejder
- **Antal års tjeneste** – Beregnet på baggrund af medarbejderens startdato
- **Antal tidligere stillinger** – Baseret på stillingshistorikken åbnes den detaljerede visning af alle medarbejderens tidligere stillinger, hvis du vælger denne indstilling
- **Fødselsdato** – Måned og dag for medarbejderens fødselsdato

Du kan få vist stillingsdata for både direkte underordnede og underordnede med udvidelser.

#### <a name="compensation-tab"></a>Fanen Kompensation

Fanen **Kompensation** viser medarbejderens årsløn. Der vises et firma-id under lønbeløbet. Hvis en medarbejder har mere end én ansættelse og får betaling fra flere juridiske enheder, har medarbejderen flere kompensationsplaner. Hvis du vil have vist alle kompensationsplan på tværs af juridiske enheder uden at skifte firma, skal du aktivere krydskompensation under **Human Resources > Delte parametre > Avanceret adgang > Aktivere kompensation på tværs af firmaer**.

Hvis du vil have vist kompensationshistorikken, skal du vælge lønbeløbet for at åbne formularen **Detaljer**. Der vises kun aktuelle og historiske poster for fast og variabel kompensation i formularen **Kompensation**. Hvis en medarbejder har mere end én ansættelse, kan du skifte mellem firmaer for at få vist kompensationshistorikken i de enkelte firmaer eller aktivere kompensation på tværs af firmaer i Delte parametre for Human Resources for at få vist alle kompensationsplaner.

Du kan få vist kompensation for både direkte underordnede og underordnede med udvidelser.

#### <a name="leave-and-absence-tab"></a>Fanen Orlov og fravær

Under fanen **Orlov og fravær** vises de største saldi for medarbejdere med aktivitet. Hvis du vil udføre en handling eller have vist en komplet liste over aktiviteter, skal du vælge **Detaljer** og derefter vælge **Fridage**. I formularen **Fridage** kan du få vist saldi, anmodninger, godkendte fridage og likviditetsbudget for at hjælpe medarbejderne med at administrere tiden bedre. Afhængigt af organisationens indstillinger kan du også anmode om fridage for dine direkte underordnede og underordnede med udvidelser.

#### <a name="performance-goals-tab"></a>Fanen præstationsmål

Under fanen **Performancemål** opsummeres performancemål efter status. Vælg et tal for en status, eller vælg performancemål fra **Detaljer** for at få vist alle mål for en medarbejder. Ledere og medarbejdere kan opdatere målene efter behov under målets varighed.

Ledere kan se alle mål for deres team via feltet **Mål for teamperformance** i sektionen **Resume** i **Mit team**.

#### <a name="reviews-tab"></a>Fanen Evalueringer

Fanen **Evalueringer** opsummerer de vurderinger, medarbejderen har i de enkelte tilstande: **I gang** , **Klar til evaluering** og **Slutevaluering**. Hvis du vil have adgang til en medarbejders evaluering, skal du vælge knappen **Detaljer** og derefter vælge evalueringer, der kan samarbejdes om. Afhængigt af, hvor en evaluering er i arbejdsgangsprocessen, kan du se, om evalueringen er tilgængelig for opdatering. 

Du kan se alle evalueringer for dit team via feltet **Evalueringer af teamperformance** i sektionen **Resume** i **Mit team**.