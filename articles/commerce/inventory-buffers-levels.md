---
title: Konfigurere lagerbuffere og lagerniveauer
description: Dette emne forklarer, hvordan du kan konfigurere lagerbuffere og lagerniveauer, der bestemmer beskeder om lagertilgængelighed på Microsoft Dynamics 365 Commerce-websteder.
author: boycezhu
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 842389811169f785235de7ac7d9a49ab903f99ddf7d43f139aba0873a2577d72
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727527"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Konfigurere lagerbuffere og lagerniveauer

[!include [banner](includes/banner.md)]

Dette emne forklarer, hvordan du kan konfigurere lagerbuffere og lagerniveauer, der bestemmer beskeder om lagertilgængelighed på Microsoft Dynamics 365 Commerce-websteder.

Dynamics 365 Commerce Headquarters indeholder lagerdata og forskellige kanaler som f.eks. POS-programmer, e-handelsudstillingsvinduer og andre brugerdefinerede integrerede programmer, der flytter lagerbeholdningen rundt på en asynkron måde. Derfor er de tilgængelige lagerværdier, der er hentet via siden disponibel lagerbeholdning i Commerce Headquarters, via POS-brugergrænsefladen (UI) og via e-Commerce-lagertilgængeligheds-API'erne, ikke altid 100-procent nøjagtige i realtid.

I stedet for at vise faktiske lagerværdier i e-handelsudstillingsvinduer foretrækker mange detailhandlere at vise meddelelser om status for lagertilgængelighed (f.eks. "Tilgængelig" eller "Udsolgt") for at informere kunderne om, hvorvidt en vare er disponibel til køb eller potentielt udsolgt. I denne tilgang skal lagerbuffere og lagerniveauer, der bestemmer meddelelserne om lagertilgængelighed, gøres tilgængelige og konfigureres.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Krav: Aktivér funktionen lagerbuffere og lagerniveauer

Funktionen for lagerbuffere og lagerniveauer styres via funktionsstyring i Commerce Headquarters. Udfør følgende trin for at aktivere funktionen.

1. Gå til **Systemadministration** \> **Arbejdsområder** \> **Funktionsstyring**.
1. Søg efter funktionen **Aktivér lagerbuffere og lagerniveauer**, vælg dens række og derefter **Aktivér nu**.

Når funktionen er aktiveret, kan du finde lagerniveauer i **Detail og handel \> Lagerstyring**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Oprette og konfigurere en lagerniveauprofil

En *lagerbeholdningsprofil* bestemmer, om status for en bestemt produktmængde skal være på lager, udsolgt eller have en anden brugerdefineret status. Du kan oprette og konfigurere flere lagerniveauprofiler pr. juridisk enhed. Hver profil består af et sæt lagerniveauer, og hvert niveau defineres af et *interval*, en *kode* og en *label*.

- **Interval** – Hvert interval defineres ud fra et *startantal* og et *slutantal*. En antalsværdi falder i et interval, hvis den er større end startantallet for det pågældende interval og ikke overstiger slutantallet.
- **Kode** – En kode er en intern forkortelse, der repræsenterer niveauet. Kunder, der direkte kan integreres med lager-API'er, kan bruge koder til at opbygge yderligere logik for et bestemt lagerniveau. De kan f.eks. deaktivere indkøbsfunktionen for et produkt, når dets lagerniveaukode er **OOS** ("out of stock – udsolgt").
- **Label** – En label er en meningsfuld kundehenvendt meddelelse, der videregiver et lagerniveau til kunderne på et e-handelswebsted.

### <a name="create-an-inventory-level-profile"></a>Oprette en lagerniveauprofil

Benyt følgende fremgangsmåde for at oprette en lagerniveauprofil.

1. Gå til **Detail og handel** \> **Lagerstyring** \> **Lagerniveauer**.
1. I handlingsruden skal du vælge **Ny** og derefter angive værdier i felterne **Profil-id** og **Beskrivelse**.
1. I oversigtspanelet **Intervaller** skal du vælge **Tilføj** for at tilføje et nyt niveau og derefter angive værdier i kolonnerne **Startantal**, **Slutantal**, **Kode** og **Label** for dette niveau. Gentag dette trin for at tilføje flere niveauer. Efter behov kan du redigere værdierne i datagitteret, eller du kan vælge **Slet** for at fjerne et niveau.
1. Vælg **Gem** i handlingsruden.

Når der oprettes en ny profil, initialiseres to lagerniveauer automatisk:

- **OOS** – Niveauet "out of stock – udsolgt", hvor den nedre grænse for intervallet er negativt uendeligt. Startantallet og koden kan ikke redigeres for dette niveau.
- **TILG.** – Niveauet "tilgængelig", hvor den øvre grænse for intervallet er uendelig. Slutantallet og koden kan ikke redigeres for dette niveau.

> [!NOTE]
> Der må ikke være mellemrum eller overlapning mellem områder i profildefinitionen.

Du kan bruge knappen **Oversættelser** i handlingsruden til at konfigurere lokaliserede strenge for label-meddelelsen. Du skal derefter køre distributionsplanjobbet **1110** (**Global konfiguration**) for at synkronisere de lokaliserede strenge med kanaler.

### <a name="configure-an-inventory-level-profile"></a>Konfigurere en lagerniveauprofil

Du kan konfigurere en lagerniveauprofil enten på produktkategoriniveau eller på det enkelte produktniveau. Når der er konfigureret en lagerniveauprofil for et produkt, bestemmes lagerniveauet ud fra de områder, der er defineret i den tilknyttede profil. Ellers bestemmes lagerniveauet "disponibel" eller "udsolgt" ud fra, om produktet har et positivt disponibelt antal.

Benyt følgende fremgangsmåde for at konfigurere en lagerniveauprofil for en kategori.

1. Gå til **Detail og handel** \> **Produkter og kategorier** \> **Commerce-produkthierarki**.
1. Vælg den kategori, der skal konfigureres en lagerniveauprofil for.
1. I oversigtspanelet **Produktegenskaber for salg** skal du vælge en juridisk enhed.
1. I afsnittet **Commerce-lager** i niveauprofilen **Lagerniveauprofil** skal du vælge en af de foruddefinerede lagerniveauprofiler.

Du kan bruge knappen **Opdater produkter** i handlingsruden til at overføre værdien for kategoriniveauprofilen til kategoriens underliggende produkter. Du finder flere oplysninger i [Administrere produktkategorier og -produkter](category-management-product-creation.md).

Benyt følgende fremgangsmåde for at konfigurere en lagerniveauprofil for et frigivet produkt.

1. Gå til **Detail og handel** \> **Produkter og kategorier** \> **Frigivne produkter efter kategori**.
1. Vælg et produkt, og åbn derefter siden produktdetaljer.
1. I oversigtspanelet **Sælg** i afsnittet **Commerce-lager** i feltet **Lagerniveauprofil** skal du vælge en af de foruddefinerede lagerniveauprofiler.

Når der oprettes et nyt produkt, angives feltet **Lagerniveauprofil**, på samme måde som mange andre attributter på produktniveau, til den værdi, der er konfigureret for den kategori, som produktet er tilknyttet.

> [!NOTE]
> Lagerniveauprofilen er en juridisk enhedsspecifik attribut. For den samme kategori eller det samme produkt kan værdien for lagerniveauprofil variere på tværs af juridiske enheder.

Udfør følgende trin for at synkronisere konfigurationerne af lagerniveauprofiler med kanaler.

1. Gå til **Retail og Commerce** \> **Retail og Commerce IT** \> **Distributionsplan**.
1. Kør distributionsplanen **1040** (**Produkt**).

## <a name="configure-an-inventory-buffer"></a>Konfigurere en lagerbuffer

*Lagerbufferen* er en brugerdefineret værdi, der trækker det ekstra antal af en vare fra det oprindelige antal for at beregne det forkalkulerede antal. Dette forkalkulerede antal giver detailhandlerne en sikker buffer, så de ikke sælger mere af et produkt, så salget overskrider den faktiske disponible lagerbeholdning. Du kan konfigurere lagerbufferen enten på produktkategoriniveau eller på det enkelte produktniveau. Hvis der ikke er angivet en lagerbuffer, bruges standardværdien **0** (nul).

Benyt følgende fremgangsmåde for at konfigurere lagerbufferen for en kategori.

1. Gå til **Detail og handel** \> **Produkter og kategorier** \> **Commerce-produkthierarki**.
1. Vælg kategorien, der skal konfigureres lagerbuffer for.
1. I oversigtspanelet **Produktegenskaber for salg** skal du vælge en juridisk enhed.
1. I afsnittet **Commerce-lager** i feltet **Lagerbuffer** skal du angive en positiv værdi.

Du kan bruge knappen **Opdater produkter** i handlingsruden til at overføre værdien for kategoriniveaubufferen til kategoriens underliggende produkter. Du finder flere oplysninger i [Administrere produktkategorier og -produkter](category-management-product-creation.md).

Benyt følgende fremgangsmåde for at konfigurere lagerbufferen for et frigivet produkt.

1. Gå til **Detail og handel** \> **Produkter og kategorier** \> **Frigivne produkter efter kategori**.
1. Vælg et produkt, og åbn derefter siden produktdetaljer.
1. I oversigtspanelet **Sælg** i afsnittet **Commerce-lager** i feltet **Lagerbuffer** skal du angive en positiv værdi.

Når der oprettes et nyt produkt, angives feltet **Lagerbufferl**, til den værdi, der er konfigureret for den kategori, som produktet er tilknyttet.

> [!NOTE]
> Hvis både lagerbufferen og lagerniveauprofilerne er konfigureret for et produkt, vil produktets forkalkulerede antal (dvs. det oprindelige antal minus bufferværdien) blive brugt til intervalberegning for at bestemme lagerniveauet.

Udfør følgende trin for at synkronisere konfigurationerne af lagerbuffere med kanaler.

1. Gå til **Retail og Commerce** \> **Retail og Commerce IT** \> **Distributionsplan**.
1. Kør distributionsplanen **1040** (**Produkt**).

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Bruge lagerbuffere og lagerniveauer i e-handelsscenarie

Med Commerce Site Builder bruges egenskaberne for lagerbuffer og lagerbeholdning i Commerce Headquarters til at bestemme meddelelser om lagertilgængelighed på e-handelswebsteder. Du finder flere oplysninger under [Anvendelse af lagerindstillinger](inventory-settings.md).

Hvis du alternativt integrerer med en tredjeparts e-handelsløsning, kan du også bruge API'erne **GetEstimatedAvailability** og **GetEstimatedProductWarehouseAvailability** til at få vist lagertilgængeligheden for et produkt i dit e-handelsscenarie. Yderligere oplysninger om disse API'er finder du i [Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md).

Indførelsen af lagerbuffere og lagerniveauer sætter disse API'er i stand til at returnere lagerniveaukoder og labelmeddelelser, der bestemmes ud fra det samlede disponible antal og tilgængelige fysiske værdier. API'erne kan konfigureres yderligere til at bestemme, om lagerantallet returneres sammen med meddelelsen, og om det disponible antal reduceres med lagerbufferværdien.

Udfør følgende trin for at konfigurere svaret på produktilgængeligheds-API'erne.

1. Gå til **Detail og handel** \> **Konfiguration af hovedkontor** \> **Parametre** \> **Commerce-parametre**.
1. I afsnittet **Lagerbeholdning** på fanen **Lager** i feltet **Produkttilgængeligheds-API'er for e-handel** skal du vælge en værdi.
1. Kør distributionsplanjobbet **1110** (**Global konfiguration**) for at anvende indstillingerne på kanaler.

## <a name="additional-resources"></a>Yderligere ressourcer

[Administrere produktkategorier og -produkter](category-management-product-creation.md)

[Anvendelse af lagerindstillinger](inventory-settings.md)

[Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
