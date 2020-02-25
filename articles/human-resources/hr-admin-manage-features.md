---
title: Administrere funktioner
description: Få mere at vide om, hvordan du slår nye funktioner til eller fra i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008457"
---
# <a name="manage-features"></a>Administrere funktioner

Som en del af vores fortløbende implementering af nye funktioner til Microsoft Dynamics 365 Human Resources, vil vi give kunderne mulighed for at udnytte nye funktioner, så hurtigt som muligt. Vi leverer prøveversionsfunktioner, som næsten er generelt tilgængelige og har gennemgået omfattende test. Vi mangler kun en sidste runde af kundefeedback og validering, før vi gør dem almindeligt tilgængelige.

Yderligere oplysninger om nye funktioner i Personale finder du i [Nyheder i Personale](hr-admin-whats-new.md) og [Dynamics 365 og Power Platform Frigivelsesplan](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Arbejdsområdet **Administration af funktioner** indeholder en oversigt over de funktioner, der er leveret i hver udgave. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem. Du kan finde flere oplysninger om Administration af funktioner under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funktioner vises i forhåndsvisning i mindst 30 dage og typisk 30-60 dage. De vigtigste funktioner er normalt tilgængelige i oktober og april hvert år efter forhåndsvisningsperioden. Så snart du ser nye egenskaber i arbejdsområdet **Administration af funktioner**, kan du slå dem til. Nogle funktioner er muligvis som slået til som standard.

Når en funktion er generelt tilgængelig, kan den slås til eller fra i produktionsmiljøer. Arbejdsområdet **Administration af funktioner** angiver, hvornår en visningsfunktion skal være obligatorisk. Denne dato er som regel den 1. oktober eller 1. april for at tilpasse det med de halvårlige frigivelsesplaner. Du kan ikke slå de obligatoriske funktioner fra. Indtil den bliver obligatorisk, kan du slå en funktion til og fra i alle miljøer.

## <a name="enable-or-disable-preview-features"></a>Aktivere eller deaktivere funktioner i prøveversion

Hvis du vil have adgang til visningsfunktionerne, skal du først aktivere dem i dit miljø. Aktivering eller deaktivering af funktioner til visning er specifik for miljøet.

> [!IMPORTANT]
> Prøveversionsfunktioner er kun tilgængelige i **Sandkasse**-miljøer. Når du slår en prøveversionsfunktion til, aktiverer du den for alle brugere i organisationen, der arbejder i det pågældende miljø. Når du slår prøveversionsfunktionen fra, deaktiverer du den og gør den utilgængelig for brugerne. Visningsfunktioner understøttes kun i begrænset omfang i Personal. Der er en mindre grad af beskyttelse af personlige oplysninger og færre sikkerhedsfunktioner, og de medtages ikke i Personale-serviceniveauaftalen (SLA). Du bør ikke bruge visningsfunktioner til behandling af personoplysninger (dvs. alle oplysninger, der kan identificere dig) eller til at behandle andre data, der er omfattet af lovbestemte overholdelseskrav.

1. I Personale skal du vælge **Systemadministration**.

2. Vælg felter **Funktionsstyring**.

3. Hvis du vil aktivere en prøveversionsfunktion, skal du vælge den på listen og derefter vælge **Aktivér**. Hvis du vil deaktivere en prøveversionsfunktion, skal du vælge den på listen og derefter vælge **Deaktiver**.

## <a name="preview-feature-benefits-management"></a>Prøveversionsfunktion: Administration af frynsegoder

Med administration af frynsegoder får du en fleksibel løsning, der understøtter en lang række frynsegodeindstillinger, sammen med en brugervenlig medarbejderoplevelse, der fremviser dine tilbud. Du kan finde flere oplysninger om konfiguration af administration af frynsegoder og brug i [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).

Administration af frynsegoder erstatter funktionaliteten i arbejdsområdet **Frynsegoder**. Når du aktiverer prøveversionsfunktionen Administration af frynsegoder, kan du ikke længere få adgang til følgende formularer i arbejdsområdet **Frynsegoder**:

- **Frynsegoder**
- **Frynsegodeelementer**
- **Bidragsberegningssatser**
- **Resultater af tilmelding til frynsegoder**
- **Resultater af frynsegodeudløb og -forlængelse**
- **Regeltyper for frynsegodeberettigelse**
- **Politikker for berettigelse til frynsegoder**
- **Berettigelseshændelser**

Du kan få vist oplysningerne i disse formularer i skrivebeskyttet tilstand. Hvis du vil redigere oplysningerne, skal du først deaktivere prøveversionsfunktionen Administration af frynsegoder.

### <a name="benefits-management-known-issues"></a>Kendte problemer i forbindelse med Administration af frynsegoder

#### <a name="life-events"></a>Livshændelser

Når der behandles livshændelser, modtager brugeren en fejlmeddelelse:

Startdato for dækning skal være mellem *begyndelsen af planperioden* og *slutningen af planperioden*. 

Livshændelsen fortsætter med at blive behandlet som forventet.

#### <a name="eligibility-processing"></a>Berettigelsesbehandling

Når du kører frynsegodeberettigelse, der bruger en 1-5X løn, % af løn og dækningsbeløb med fladt beløb, skal datoen for frynsegodedetaljer angives til startdatoen for medarbejder i **Ansættelseshistorik**, med antal arbejdstimer, betalingsfrekvens og årligt beløb for frynsegodeløn. Hvis der findes fast løn for arbejderen, skal du angive antal arbejdstimer sammen med betalingsfrekvensen, og det årlige lønbeløb beregnes. Hvis medarbejderen er fastansat, er der ikke behov for antal arbejdstimer. Det anbefales, at du angiver fast løn først, når du opretter nye arbejdere. Sådan opdateres posten med frynsegodedetaljer: Naviger til **Arbejder > Historik for arbejder > Detaljer om ansættelse**. Juster datoen efter arbejderens startdato.

#### <a name="employee-self-service"></a>Medarbejderselvbetjening

Medarbejderne kan vælge en plan, som de ikke er kvalificerede til, og tjekke ud. For eksempel: En arbejder har ingen afhængige, men har tilladelse til at vælge en medicinsk plan med en familiedækningsindstilling.

Medarbejderbeløb beregnes ikke ved opdatering af dækningsbeløbet for livsforsikring. Når en medarbejder f.eks. tilbydes en livsforsikringsplan, kan de vælge dækning på op til $50.000 til en pris af $,36 pr. dækning på $1.000.  Når medarbejderen opdaterer dækningsbeløbet, forbliver medarbejderens tilknyttede omkostninger nul.

For en frynsegodeplan, der kun tillader en enkelt markering af denne plantype, modtager brugeren en fejlmeddelelse, hvis de forsøger at frafalde en plan, efter at der er valgt en plan. En bruger vælger f.eks. en medicinsk plan og anbringer den i sin indkøbsvogn. Brugeren vælger derefter **Frafald** for en anden medicinsk plan. Brugeren vil modtage en fejlmeddelelse.

## <a name="preview-features-in-leave-and-absence"></a>Prøveversionsfunktioner for orlov og fravær

Prøveversionsfunktioner for orlov og fravær omfatter:

- **Orlovs- og fraværskalender** – Orlovs- og fraværsparametre flyttes fra **Personaleparametre** til en ny skærm kaldet **Orlovs- og fraværsparametre**. Den nye skærm indeholder en ny fane **Kalender**. Denne forhåndsvisning aktiverer kun et undersæt af parametrene. Du kan få adgang til den nye skærm fra fanen **Links** i arbejdsområdet **Orlov og fravær**. Kalenderne omfatter:
  - **Firmakalender** – viser alle anmodninger om medarbejderfridage. Personer med rollen **Personale** kan få adgang til denne kalender fra fanen **Links** i arbejdsområdet **Orlov og fravær**.
  - **Kalender for lederteam** – viser alle anmodninger om fridage i direkte rapporter. Ledere kan få adgang til kalenderen fra fanen **Mit team** i Medarbejderselvbetjening under **Orlov og fravær**. 

- **Feriekalendere for orlov og fravær** – Orlovstyper omfatter en ny indstilling, **Ferie**, der bruges sammen med arbejdstidskalenderen. Dage, der er defineret af helligdage og lukninger, er nu angivet som **Ferie**, når der genereres arbejdsdage. Når periodiseringer behandles, foretages der reguleringer af medarbejdere, der er tildelt til kalenderen, for at tage højde for helligdage, der ligger på en arbejdsdag.

- **Revision af orlovsperiodisering** – En ny skærm giver dig mulighed for at se, hvornår periodiseringer er behandlet og slettet, både af alle medarbejdere og individuelle medarbejdere. Du kan få adgang til denne nye skærm fra fanen **Links** i arbejdsområdet **Orlov og fravær**.

- **Sletning af orlovsperiodisering** – Du kan nu slette periodiseringsposter for bestemte orlovsplaner. Du kan få adgang til denne nye indstilling fra fanen **Links** i arbejdsområdet **Orlov og fravær**. For de enkelte medarbejdere vises denne indstilling i **Orlov og fravær**-grupperingen i medarbejderprofilen. 

- **Afrunding af orlovsperiodisering** – Nye indstillinger for **Orlovstype** definerer, hvilken type afrundingsperiodisering der skal bruges, plus decimalpræcisionen i afrunding under periodiseringsprocessen. Når periodiseringer behandles, anvendes afrundingen og præcisionen til periodiseringsposterne. 

- **Konfigurer flere orlovstyper i en enkelt orlovsplan** – En ny kolonne i orlovsperiodiseringtidsplanen for orlovstyper giver dig mulighed for at definere flere orlovstyper i en orlovs- og fraværsplan med forskellige periodiseringstidsplaner. Det tidligere felt **Orlovstype** er fjernet. I medarbejderens tilmelding vises saldi for orlovstyperne nu i en tabel i stedet for øverst på skærmen.

  > [!IMPORTANT]
  > Du kan ikke deaktivere denne funktion, når du har aktiveret den.

- **Brug en medarbejders fuldtidsækvivalent for periodisering**– En ny kolonne i orlovsperiodiseringtidsplanen gør det muligt at bruge fuldtidsækvivalent til periodisering. Når periodiseringer behandles, bruger programmet medarbejderens primære stilling og den angivne fuldtidsækvivalent til at fastlægge det forholdsmæssige periodiseringsbeløb.

  > [!NOTE]
  > Denne funktion er kun tilgængelig, hvis du aktiverer **Konfigurer flere orlovstyper i en enkelt orlovsplan**. 

## <a name="feedback"></a>Tilbagemelding

Vi vil gerne høre fra dig om din oplevelse med disse funktioner i prøveversion. Vi opfordrer dig til jævnligt at opslå din feedback på følgende websteder, når du bruger disse eller andre funktioner:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Dette websted er en nyttig ressource, hvor brugere kan diskutere eksempler på brug, stille spørgsmål og få hjælp fra community'et.
- Fortæl os om de funktioner, som du gerne vil have i produktet, eller gør os opmærksom på eventuelle ændringer, som du synes, vi skal foretage af eksisterende funktioner. Foreslå produktideer til [Personale-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    
Medtag ikke personlige oplysninger (oplysninger, der kan identificere dig) i din feedback eller indsendelser af produktanmeldelser. Indsamlede oplysninger kan blive analyseret yderligere, men de bruges ikke til at besvare spørgsmål i henhold til gældende love om beskyttelse af personlige oplysninger. Personlige data, der indsamles særskilt i henhold til disse programmer, er underlagt [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Se også

- [Nyheder i Personale](hr-admin-whats-new.md)
- [Dynamics 365 og Power Platform Frigivelsesplan](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)