---
title: Ofte stillede spørgsmål om integration af Dynamics 365 Talent med Dynamics 365 Finance
description: I dette emne beskrives, hvilke data der synkroniseres i en integration af Talent og Finance.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251008"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a>Ofte stillede spørgsmål om integration af Dynamics 365 Talent med Dynamics 365 Finance

[!include [banner](includes/banner.md)]

Dette emne indeholder svar på almindelige spørgsmål om, hvilke data der synkroniseres, når Dynamics 365 Talent integreres med Dynamics 365 Finance.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Synkroniseres alle data eller bare nogle dataenheder?

Med Core HR synkroniseres et undersæt af dataene. Du kan finde en liste over alle enheder i [Integration fra Dynamics 365 Talent til Dynamics 365 Finance](talent-financeandoperations-integration.md).

I Attract og Onboard er alle data indbygget i Common Data Service.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Kan jeg oprette en ny tilknytning uden at bruge skabelonerne?

Skabeloner bruges som udgangspunkt. Du kan oprette din egen skabelon, men der skal altid bruges en skabelon ved oprettelse af et integrationsprojekt. Du kan finde flere oplysninger om dataintegrator (DI), skabeloner og projekter under [Integrer data i Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a>Kan jeg tilknytte økonomiske dimensioner for at overføre mellem Talent og Finance?

Økonomiske dimensioner findes ikke på nuværende tidspunkt i Common Data Service og er derfor ikke del af standardskabelonen. Denne enhed er planlagt, men i øjeblikket er der ingen versionstidslinje.

For data i Finance, som ikke findes i Talent, kan du sammenkæde de to systemer ved hjælp af **Konfigurer links** i Talent. Du kan finde flere oplysninger om, hvordan du konfigurerer links mellem Talent og Finance, i [Nyheder eller ændringer i Dynamics 365 Talent: Core HR (31. oktober 2018)](whats-new-talent-october-31.md).

![Tilknyt økonomiske dimensioner](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Når jeg importerer medarbejdere, bliver de sommetider placeret blandt inaktive arbejdere i Finance. Hvorfor?

Denne fejl kan opstå, hvis medarbejderne ikke har en aktiv post med ansættelsesoplysninger. Du kan løse dette ved at gå til **Personalestyring \> Medarbejdere \> Ansættelseshistorik \> Datoadministrator** og kontrollere, at der findes en aktiv post med ansættelsesoplysninger.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Hvis jeg vælger kun at tilknytte et undersæt af felter, udløser ændringer af ikke-tilknyttede felter så en synkronisering?

Synkronisering af data følger tidsplanen for udførelse. Integrationen henter en post, hvis et felt i posten ændres, uanset om feltet er en del af integrationstilknytningen.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Hvordan kan jeg nøjes med at sende ændringer, der kun gælder en aktiv arbejder og ikke de afsluttede poster?

Ved hjælp af "Avanceret forespørgsel" kan du filtrere og omforme kildedata, før du overfører dem til destinationen.

![Avanceret forespørgsel for aktive arbejdere](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Kan jeg angive, hvilke felter der skal sendes til Finance for en bestemt enhed?

Felter kan tilføjes eller fjernes fra integrationsopgaven. Ikke alle datafelter, der findes på Common Data Service-enheden, udfyldes fra Core HR.
Yderligere data kan udfyldes via PowerApps.

![Tilføje eller fjerne felter i en integrationsopgave](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Jeg konfigurerede integration som et batchjob, men så mistede Talent forbindelsen til destinationssystemet. Hvordan kan jeg sende det samme sæt ændringer til destinationssystemet?

Der kræves ingen speciel opsætning for undtagelseshåndtering. Dataintegrator registrerer og rapporterer automatisk fejl, der finder sted på kilde og destination og giver mulighed for nye manuelle forsøg. Men det tillader ikke manuel rettelse af data. Hvis det er nødvendigt at opdatere data, skal det foregå ved kilden eller destinationen.

## <a name="can-i-set-up-bi-directional-integration"></a>Kan jeg konfigurere tovejsintegration?

Nej, integration går i øjeblikket kun fra Talent til Finance and Operations. Der er dog en tilgængelig standardskabelon, som kan bruges til at sende data fra Talent til Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Kan jeg tillade sletning af poster som en del af integrationen?

Nej, Dataintegrator henter ikke slettede poster til dataoverførsel. Kun oprettelse og opdateringer af data (UPSERT) er inkluderet i øjeblikket.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Kan jeg foretage den kørsel, der mislykkedes, igen? Vil den i så fald sende en komplet fil eller kun ændringerne?

Den første kørsel af Dataintegrator er altid en fuld kørsel. Efterfølgende kørsler er baseret på registrering af ændringer. Når der er foretaget en fejlkørsel, udpakkes de poster, der er medtaget i kørslen, og de seneste ændringer fra Common Data Service udsendes.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Når jeg gemmer projektet, får jeg fejlmeddelelsen: "Projektet har tilknytningsfejl". Hvad skal jeg gøre?

Kontroller konfiguration af integrationsnøglerne, foretag eventuelle nødvendige ændringer i opsætningen, og opdater derefter objekterne i projektet.

Når standardskabelonen bruges, importeres integrationsnøglerne automatisk. Dette problem kan opstå, når der føjes nye opgaver til den eksisterende skabelon.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Hvis jeg har N antal juridiske enheder, hvor arbejdere har ansættelse, skal jeg så oprette en tilknytning for hver af dem?

Ja, du skal bruge et separat integrationsprojekt i dataintegrationen for hver juridiske enhed i Finance.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Jeg har brug at overføre data, ikke der er en del af den standardskabelon, der leveres af Microsoft. Kan jeg gøre det?

Ja, du kan tilføje felter i eller fjerne dem fra den eksisterende skabelon. Skabelonen kan ændres, så der medtages yderligere data fra andre Common Data Service-enheder. Enheden skal være i Common Data Service, hvis den skal medtages i skabelonen. 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Jeg har netop oprettet nye Finance- og Talent-miljøer, og jeg får fejlmeddelelsen "Dataværdien overtræder integritetsbegrænsningerne". Hvorfor?

Årsager til denne fejl kan omfatte:

- Dataoverførslen resulterede i, at der blev udtrukket dubletposter ved kilden (Common Data Service).

- Dataoverførslen har null-værdier for felter, der kræves i Finance and Operations. Kontroller de data, der er i Common Data Service, og at de opfylder kravene i Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Hvis der er kørselsfejl, og medarbejder-id'et ikke synkroniseres, hvordan finder jeg så historikjobbet med den mislykkede medarbejderpost?

Dataintegrator opretter flere projekter i Finance. Forholdet mellem Dataintegrator-opgaven og Finance-projektet er 1 til 1.

Spor tiden fra historikken for Dataintegrator-udførelse, og se efter indeks -1-projektet i Finance. Hvis opgavenummeret er 9 i Dataintegrator, er indekset i Finance 8.

1. Hent opgaveindekset fra Dataintegrator (i dette eksempel er det "9").

![Hent opgaveindeks fra Dataintegrator](media/CaptureTaskIndex.png)

2. Spor projektets kørselstidspunkt.

![Spor projektets kørselstidspunkt](media/CaptureTimeOfExecution.png)

3. I Finance skal du identificere indeks - 1. I dette eksempel matcher projektet med suffikset "8" og kørselstidspunkt for indeks "0" udførelsestidspunktet i trin 2.

![Identifikation af indeks](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a>Jeg kan ikke se dataene i Finance efter at have integreret Talent og Finance. Hvad skal jeg gøre?

Integrationen i Finance er en totrinsproces. Kontroller først, at Talent-dataene er opdaterede og tilgængelige i Common Data Service. Dette er en synkronisering i nær-realtid, som du kan kontrollere i PowerApps ved at se på dataene i dataenhederne.

![Data i Common Data Service](media/DataInCDS.png)

Hvis dataene ikke vises som forventet i Common Data Service, skal du kontrollere, om enheden understøttes i integrationen. For at medtage flere data i Common Data Service kræver det en ændring fra Microsofts side.

Hvis enheden understøttes, og dataene er tilgængelige i Common Data Service, skal du kontrollere, at tilknytningen i dataintegrator er korrekt. Hvis integratortilknytningen ser ud til at være i orden, skal du kontrollere, at datastyringsjobbet er kørt korrekt. Fejl kan opstå under kørsel af batchjob. Du kan finde flere oplysninger om datastyring i [Datastyring](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Adresserne for mine medarbejdere er forkerte, når jeg har importeret dem i Finance. Hvad skal jeg gøre?

Nummerserien for **Lokations-id** bruger det samme mønster i Finance og Talent. Nummerserien skal være unik på begge sider, så der ikke opstår adressekollisioner under integrationen af data fra Common Data Service til Finance and Operations.

Ved implementering af Talent skal du kontrollere, at nummerserierne ikke er de samme i Talent og Finance. Kontroller, at alle nummerserier ikke er ens, hvor data kan vedligeholdes i begge systemer.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Når jeg opretter mit forbindelsessæt, kan jeg ikke se forbindelsen i rullelisten Forbindelse. Hvad skal jeg gøre?

Sørg for, når du opretter forbindelser, at vælge Dynamics 365 Finance og Common Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Når jeg synkroniserer ansættelser, vises fejlmeddelelserne "CompanyInfo_FK findes ikke", eller "Værdien '31/12/2154 23:59:59' i feltet 'Slutdato for ansættelse' bliver ikke fundet i den relaterede tabel 'Ansættelse'". Hvad skal jeg gøre?

Kontroller, at det er de korrekte juridiske enheder, du opretter tilknytning til. Synkroniseringen af en juridisk enhed er ikke en del af standardskabelonen, så det forventes, at de enkelte juridiske enheder, der findes i Talent og Common Data Service, også findes i Finance.
Kontroller også, at det er de korrekte juridiske enheder for det tilknyttede forbindelsessæt, du vælger.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Når jeg har oprettet projektet, ser felttilknytningen for Finance ud til at være tom. Hvad skal jeg gøre?

Opdater dataenhederne i Finance ved at gå til **Datastyring \> Rammeparametre \> Indstillinger for enhed \> Opdater liste over enheder.** Dette tager et par minutter, og derefter bør du kunne se disse tilknytninger. Dette problem opstår, når der oprettes nye projekter.

![Manglende felttilknytning](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Yderligere ressourcer

- Dataintegrator (DI): 

  - [Integrer data i Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [Dataintegrator-fejlstyring og fejlfinding](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [Svar på DSR-anmodninger om systemgenererede logfiler i PowerApps, Microsoft Flow og Common Data Service](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Datastyring:

  - [Datastyring](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
