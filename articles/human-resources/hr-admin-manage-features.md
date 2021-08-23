---
title: Administrere funktioner i Human Resources
description: Få mere at vide om, hvordan du slår nye funktioner til eller fra i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a9c459b2b34164a9be3ed609a99deb4c5b710d340ef560e6f991e760375d6146
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738361"
---
# <a name="manage-features-in-human-resources"></a>Administrere funktioner i Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Som en del af vores fortløbende implementering af nye funktioner til Microsoft Dynamics 365 Human Resources, vil vi give kunderne mulighed for at udnytte nye funktioner, så hurtigt som muligt. Vi leverer prøveversionsfunktioner, som næsten er generelt tilgængelige og har gennemgået omfattende test. Vi mangler kun en sidste runde af kundefeedback og validering, før vi gør dem almindeligt tilgængelige.

Yderligere oplysninger om nye funktioner i Human Resources finder du i [Nyheder i Human Resources](hr-admin-whats-new.md) og [Dynamics 365 og Power Platform Frigivelsesplan](/dynamics365/release-plans/?panel=products1#pivot=products).

Arbejdsområdet **Administration af funktioner** indeholder en oversigt over de funktioner, der er leveret i hver udgave. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem. Du kan finde flere oplysninger om Administration af funktioner under [Oversigt over funktionsstyring](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Alle nye funktioner vises i forhåndsvisning i mindst 30 dage og typisk 30-60 dage. De vigtigste funktioner er normalt tilgængelige i oktober og april hvert år efter forhåndsvisningsperioden. Så snart du ser nye egenskaber i arbejdsområdet **Administration af funktioner**, kan du slå dem til. Nogle funktioner er muligvis som slået til som standard.

Når en funktion er generelt tilgængelig, kan den slås til eller fra i produktionsmiljøer. Arbejdsområdet **Administration af funktioner** angiver, hvornår en visningsfunktion skal være obligatorisk. Denne dato er som regel den 1. oktober eller 1. april for at tilpasse det med de halvårlige frigivelsesplaner. Du kan ikke slå de obligatoriske funktioner fra. Indtil den bliver obligatorisk, kan du slå en funktion til og fra i alle miljøer.

## <a name="enable-or-disable-preview-features"></a>Aktivere eller deaktivere funktioner i prøveversion

Hvis du vil have adgang til visningsfunktionerne, skal du først aktivere dem i dit miljø. Aktivering eller deaktivering af funktioner til visning er specifik for miljøet.

> [!IMPORTANT]
> Prøveversionsfunktioner er kun tilgængelige i **Sandkasse**-miljøer. Når du slår en prøveversionsfunktion til, aktiverer du den for alle brugere i organisationen, der arbejder i det pågældende miljø. Når du slår prøveversionsfunktionen fra, deaktiverer du den og gør den utilgængelig for brugerne. Visningsfunktioner understøttes kun i begrænset omfang i Personal. Der er en mindre grad af beskyttelse af personlige oplysninger og færre sikkerhedsfunktioner, og de medtages ikke i Human Resources-serviceniveauaftalen (SLA). Du bør ikke bruge visningsfunktioner til behandling af personoplysninger (dvs. alle oplysninger, der kan identificere dig) eller til at behandle andre data, der er omfattet af lovbestemte overholdelseskrav.

1. I Human Resources skal du vælge **Systemadministration**.

2. Vælg felter **Funktionsstyring**.

3. Hvis du vil aktivere en prøveversionsfunktion, skal du vælge den på listen og derefter vælge **Aktivér**. Hvis du vil deaktivere en prøveversionsfunktion, skal du vælge den på listen og derefter vælge **Deaktiver**.

## <a name="enable-or-disable-benefits-management"></a>Aktivere eller deaktivere Administration af frynsegoder

Hvis du vil aktivere administration af frynsegoder, skal du bruge samme fremgangsmåde som i [Aktivere eller deaktivere funktioner i prøveversion](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Du kan ikke deaktivere administration af frynsegoder i et **produktionsmiljø**, når du har aktiveret det. Du kan dog deaktivere administration af frynsegoder i **sandkassemiljøer**.

Du kan finde flere oplysninger om konfiguration af administration af frynsegoder og brug i [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).

Administration af frynsegoder erstatter funktionaliteten i arbejdsområdet **Frynsegoder**. Når du aktiverer prøveversionsfunktionen Administration af frynsegoder, kan du ikke længere få adgang til følgende formularer i arbejdsområdet **Frynsegoder**:

- **Frynsegoder**
- **Frynsegodeelementer**
- **Bidragsberegningssatser**
- **Resultater af tilmelding til frynsegoder**
- **Resultater af frynsegodeudløb og -forlængelse**
- **Regeltyper for frynsegodeberettigelse**
- **Politikker for berettigelse til frynsegoder**
- **Berettigelseshændelser**

Du kan få vist oplysningerne i disse formularer i skrivebeskyttet tilstand. Hvis du vil redigere oplysningerne, skal du først deaktivere Administration af frynsegoder (gælder kun for **sandkassemiljøer**).

## <a name="enable-or-disable-leave-and-absence"></a>Aktivere eller deaktivere orlov og fravær

Hvis du vil aktivere orlov og fravær, skal du bruge samme fremgangsmåde som i [Aktivere eller deaktivere funktioner i prøveversion](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Du kan ikke deaktivere funktionen **Flere orlovstyper** i orlov og fravær, når du har aktiveret den. Det gælder både i **sandkasse-** og i **produktionsmiljøer**.

Du kan få flere oplysninger om visningsfunktioner for orlov og fravær i [Visningsfunktioner for orlov og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Send os feedback

Vi vil gerne høre fra dig om din oplevelse med disse funktioner i prøveversion. Vi opfordrer dig til jævnligt at opslå din feedback på følgende websteder, når du bruger disse eller andre funktioner:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Dette websted er en nyttig ressource, hvor brugere kan diskutere eksempler på brug, stille spørgsmål og få hjælp fra community'et.
- Fortæl os om de funktioner, som du gerne vil have i produktet, eller gør os opmærksom på eventuelle ændringer, som du synes, vi skal foretage af eksisterende funktioner. Foreslå produktideer til [Human Resources-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Medtag ikke personlige oplysninger (oplysninger, der kan identificere dig) i din feedback eller indsendelser af produktanmeldelser. Indsamlede oplysninger kan blive analyseret yderligere, men de bruges ikke til at besvare spørgsmål i henhold til gældende love om beskyttelse af personlige oplysninger. Personlige data, der indsamles særskilt i henhold til disse programmer, er underlagt [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Se også

- [Nyheder i Human Resources](hr-admin-whats-new.md)
- [Dynamics 365 og Power Platform Frigivelsesplan](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]