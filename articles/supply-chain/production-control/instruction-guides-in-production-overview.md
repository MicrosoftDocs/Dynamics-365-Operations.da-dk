---
title: Levere Mixed-Reality-vejledninger til arbejdere i produktion
description: Dette emne forklarer, hvordan du kan integrere modulet til produktionsstyring i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides.
author: johanhoffmann
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "61943"
- intro-internal
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 703f2cb9a1ea8691420765a8598d59f3e6cc6488
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062946"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Levere Mixed-Reality-vejledninger til arbejdere i produktion

[!include [banner](../includes/banner.md)]


Arbejdere i produktionsprocesser vil nyde godt af relevante instruktioner, der er tilgængelige på det rette tidspunkt i forbindelse med deres arbejde. *Instruktioner* gælder i flere arbejdsdomæner, herunder: montage, service, drift, certificering og sikkerhed. Løbende uddannelsesinstruktioner kan gøre det lettere for medarbejderne at udrette mere og arbejde bedre på tværs af alle disse kernefunktioner i virksomheden.

## <a name="introduction"></a>Introduktion

Du kan levere instruktioner på forskellige måder. Et effektivt standardsystem, der bruger [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guides kan hjælpe medarbejderne med praktisk læring. Du kan definere standardiserede processer med trinvise instruktioner, der fører medarbejderne til de værktøjer og dele, de har brug for, og viser medarbejderne, hvordan disse værktøjer bruges i ægte arbejdssituationer.

Du kan knytte guider til forskellige aspekter af produktionsstyring, herunder:

- [Ressourcer](#resources)
- [Ressourcegrupper](#resource-groups)
- [Frigivne produkter](#released-products)
- [Formler](#formulas)
- [Formelversioner](#formula-versions)
- [Styklister](#bom)
- [Styklisteversioner](#bom-versions)
- [Ruter](#routes)
- [Ruteversioner](#route-versions)
- [Ruteoperationsrelationer](#route-operation-relations)

> [!NOTE]
> Du kan også tilknytte guider med Aktivstyring. Du kan finde flere oplysninger under [Integrere Dynamics 365 Supply Chain Management (Aktivstyring) med Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).

Når en medarbejder i forreste linje vælger et job i produktionen via Supply Chain Management, kan arbejderen se [de relevante guider](#logic) på jobkortet. Når arbejderen vælger en specifik vejledning, vises en QR-kode for den pågældende vejledning på skærmen. Arbejderen bruger derefter sin HoloLens til at scanne QR-koden, der starter vejledninger og viser de nødvendige instruktioner.

Følgende underafsnit beskriver et par udvalgte scenarier, hvor firmaer på tværs af brancher kan se den største værdi, når der bruges vejledninger til at præsentere instruktioner til produktion.

### <a name="assembly"></a>Assembly

![Bruge guider i assembly-opgaver.](media/instruction-guides-hero-assembly.png "Bruge guider i serviceopgaver")

Instruktionerne i assembly-drift viser arbejdere de værktøjer og dele, de har brug for, og hvordan de bruges i reelle arbejdssituationer.

Produktionschefer kan oprette og tildele guider, f.eks. til [produktionsruter](routes-operations.md), [operationsrelationer](routes-operations.md#operation-relations) eller [styklister](bill-of-material-bom.md). Arbejdere kan finde de relevante instruktioner om den pågældende operationsoplevelse i produktionen.

### <a name="service"></a>Ydelse

![Bruge guider i serviceopgaver.](media/instruction-guides-hero-service.png "Bruge guider i serviceopgaver")

Udstyr teknikere med instruktioner på arbejdspladsen, hvilket eliminerer behovet for at planlægge yderligere besøg.

Servicechefer kan f.eks. tildele guider til bestemte [produkter](../../commerce/product.md), der gennemgår rutinerne for kvalitetsvurdering.

### <a name="quality"></a>Kvalitet

![Bruge guider i kvalitetssikringsopgaver.](media/instruction-guides-hero-quality.png "Bruge guider i kvalitetssikringsopgaver")

Udrul nye processer for at sikre øget konsistens ved at omdanne medarbejdernes viden til et rutineværktøj.

Kvalitetssikringschefer kan f.eks. tildele guider til [produkter](../../commerce/product.md), der gennemgår rutinerne for kvalitetsvurdering.

### <a name="certifications"></a>Certificeringer

![Bruge guider til certificeringsrelaterede opgaver.](media/instruction-guides-hero-certification.png "Bruge guider til certificeringsrelaterede opgaver")

Sørg for, at hver medarbejder overholder høje standarder, ved hurtigt at identificere, hvem der har brug for hjælp og hvor.

### <a name="safety"></a>Sikkerhed

![Bruge guider til instruktionerne for arbejdssikkerhed.](media/instruction-guides-hero-safety.png "Bruge guider til instruktionerne for arbejdssikkerhed")

Udlevér vejledninger, der gennemgår de farlige procedurer virtuelt inden forsøg på at udføre dem i det fysiske miljø. Med en Mixed Reality-tilgang kan arbejderne opleve farlige procedurer virtuelt.

Produktionschefer kan levere dedikerede håndteringsinstruktioner for farligt materiale eller delikate håndteringsprocedurer ved at tildele instruktioner til [produktvarer](../../commerce/product.md), [ruter](routes-operations.md) og [operationer](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Introduktion til vejledninger og Guides

Hvis du vil aktivere instruktioner i produktionsprocesser, giver Supply Chain Management en standardintegration med Dynamics 365 Guides. Der kræves en licenseret og installeret programforekomst af Guides for at opbygge, vedligeholde og tildele Mixed Reality-instruktioner til produktionsaktiver og arbejde.

### <a name="prerequisites"></a>Forudsætninger

Hvis du vil bruge denne funktion, skal systemet indeholde følgende:

- Dynamics 365 Supply Chain Management version 10.0.15 eller nyere
- [Dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md) til Supply Chain Management-apps.
- [Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 eller nyere

### <a name="turn-on-the-feature"></a>Slå funktionen til

Hvis du vil gøre funktionen tilgængelig på systemet, skal du aktivere dens konfigurationsnøgler. Du behøver kun at gøre dette én gang. For at kunne gøre dette skal en administrator udføre følgende:

1. Sæt systemet i vedligeholdelsestilstand som beskrevet i [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.
1. Udvid afsnittet **Mixed Reality**, og markér derefter afkrydsningsfeltet **Mixed Reality-guide**.
1. Udvid afsnittet **Administration af produktion**, og markér derefter afkrydsningsfeltet **Produktionsinstruktioner**.
1. Slå vedligeholdelsestilstand fra som beskrevet i [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Konfigurere, hvordan guider vises i produktionen

Hvis du vil konfigurere, hvordan guider vises i produktionen, skal du gå til **Mixed Reality \> Dynamics 365 Guides \> Konfigurer guideintegration**.

![Konfigurere guideintegration i produktion.](media/instruction-guides-configure-integration.png "Konfigurere guideintegration i produktion")

Angiv følgende felter:

- **Microsoft Dataverse-URL-adresse** - Angiv URL-adressen til det Microsoft Dataverse-miljø, hvor du opretter din Guides. Formatet er "contoso.crm4.dynamics.com", hvor den første del af URL-adressen typisk er navngivet efter din organisation (f.eks. "contoso."), den anden del er specifik for dit miljøs dataområde (som f.eks. "crm4"), og den sidste del er domænet (f.eks. "dynamics.com"). En måde at finde den rigtige URL-adresse på er at gå til [home.dynamics.com](https://home.dynamics.com/) og derefter åbne din Guides-app. Når Guides åbnes, kan du se URL-adressen på adresselinjen i din browser (tag kun basis-URL-adressen, som ligner det foregående eksempel). Denne værdi bruges til at oprette adresser til dine guider og vil blive kodet i QR-koderne."
- **QR-kodestørrelse** - Angiv størrelsen på den gengivne QR-kode. Det anbefales, at du vælger en størrelse, der vil udfylde det meste af din skærm, men ikke mere. *15* er typisk en god værdi.
- **Rettelsesniveau for QR-kodefejl** - Angiv QR-kodens granularitet. En højere granularitet kan hjælpe med at øge kodens pålidelighed, men **størrelsen på QR-koden** skal være stor nok til at understøtte det detaljeringsniveau, der kræves af det valgte rettelsesniveau.

> [!TIP]
> - QR-kodestørrelser, der er for store til skærmen, tager lidt længere tid at gengive og skal derefter skaleres ned, så de passer til skærmen. Disse giver ikke nogen fordel.
> - QR-kodestørrelser, der er for små, kan reducere muligheden for HoloLens at læse koden korrekt i visse miljøer.
> - Det anbefales, at du tester indstillingerne for de enkelte enheder, der skal vise QR-koder for HoloLens-brugere. Vælg indstillinger, der giver tilstrækkelig læsbarhed i produktionsmiljøet.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Få vist en oversigt over alle guidetildelinger

Du kan bruge siden **Alle guider** til at få vist listen over alle tilgængelige guider i organisationen og alle tildelinger til dine produktionsprocesser og ressourcer. Hvis du vil åbne den, skal du gå til **Mixed Reality \> Guider \> Alle guider**. Oversigten øverst viser alle tilgængelige guider, og du kan bruge feltet her til at filtrere listen. På listen nederst vises alle guidetildelinger, og der findes en værktøjslinje til styring af dem.

![Administrere guider.](media/instruction-guides-allguides.png "Administrere guider")

I følgende afsnit beskrives de objekttyper, du kan tildele guider. Hver enkelt tildelte guide indeholder instruktioner, der automatisk knyttes til de enkelte produktionsjob og vil være tilgængelige i produktionen.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Knytte en guide til en ressource

Føj en guide til en [ressource](operations-resources.md) for at tilbyde guiden i forbindelse med de relevante produktionsjob.

### <a name="typical-scenario-using-resources"></a>Typisk scenarie, der bruger ressourcer

Du kan f.eks. knytte en guide med generel maskinsikkerhed eller håndteringsoplysninger til en ressource af typen maskine. Derefter vil guiden være tilgængelig på alle de job, der udføres på maskinen.

### <a name="add-a-guide-to-a-resource"></a>Føje en guide til en ressource

Sådan føjer du en guide til en ressource:

1. Gå til **Produktionsstyring \> Opsætning \> Ressourcer \> Ressourcer**.
1. Vælg den ressource, du vil tildele en guide, i listeruden.
1. Udvid oversigtspanelet **Tilknyttede guider**.
1. Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**. Der føjes en ny linje til gitteret.
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele. Hvis du har et stort antal guider, kan du filtrere listen for at finde den, du søger efter.
    ![Administrere guider.](media/instruction-guides-allguides.png "Administrere guider")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Knytte en guide til en ressourcegruppe

Du kan føje en guide til [ressourcegrupper](tasks/define-discrete-manufacturing-resource-group.md), hvis du bruger dem til at administrere grupper af maskiner, produktionslinjer eller arbejdsceller.

### <a name="typical-scenarios-using-resource-groups"></a>Typiske scenarier, der bruger ressourcegrupper

**Eksempel 1:** Du har defineret en ressourcegruppe til flere maskiner af samme model. I stedet for at tildele den relevante vejledning til håndtering af maskinmodellen til alle relevante ressourcer, kan du i stedet tildele guiden til den ressourcegruppe, der afspejler maskinmodellen.

**Eksempel 2:** Du har defineret en ressourcegruppe for en arbejdscelle, der indeholder forskellige maskiner, og du har en guide, der giver generelle instruktioner til, hvordan arbejdscellen vedligeholdes. Guiden gælder for alle produktionsaktiviteter i denne arbejdscelle.

### <a name="add-a-guide-to-a-resource-group"></a>Føje en guide til en ressourcegruppe

Sådan føjer du en guide til en ressourcegruppe:

1. Gå til **Produktionsstyring \> Opsætning \> Ressourcer \> Ressourcegrupper**.
1. Vælg den ressourcegruppe, du vil tildele en guide, i listeruden.
1. Udvid oversigtspanelet **Tilknyttede guider**.
1. Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**. Der føjes en ny linje til gitteret.
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele. Hvis du har et stort antal guider, kan du filtrere listen for at finde den, du søger efter.
    ![Føje en guide til en ressourcegruppe.](media/instruction-guides-resourcegroup.png "Føje en guide til en ressourcegruppe")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Knytte en guide til et frigivet produkt

Du kan føje en guide til et hvilket som helst [frigivet produkt](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>Typisk scenarie, der bruger frigivne produkter

Guider på produktniveau hjælper produktionsarbejdere med instruktioner, der er relevante for driften eller håndteringen af et bestemt frigivet produkt eller en vare.

### <a name="add-a-guide-to-a-released-product"></a>Føje en guide til et frigivet produkt

Sådan føjer du en guide til et frigivet produkt:

1. Gå til **Administration af produktionsoplysninger \> Produkter \> Frigivne produkter**.
1. Åbn det produkt, du vil tildele en guide.
1. Åbn fanen **Tekniker** i handlingsruden, og vælg **Tilknyttede guider** i gruppen **Vis**.
1. Siden **Tilknyttede guider** åbnes for det valgte produkt.
1. Vælg **Tilføj** i handlingsruden for at føje en ny linje til gitteret. 
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.
    ![Føje en guide til et frigivet produkt.](media/instruction-guides-ReleasedProduct-AddGuides.png "Føje en guide til et frigivet produkt")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Knytte en guide til en formel

Du kan føje en guide til enhver [formel](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>Typisk scenarie, der bruger formler
  
Guider på formelniveau giver produktionsarbejdere instruktioner i konteksten af en formel eller opskrift. Guider kan også tildeles versioner af en formel.

> [!NOTE]
> Du kan tildele vejledning, der er relevant for produktionsprocesser, ud fra en formel til en rute-, ruteversions- eller ruteoperationsrelation.  

> Guider kan i øjeblikket ikke knyttes til individuelle formellinjer.

### <a name="add-a-guide-to-a-formula"></a>Føje en guide til en formel

Sådan føjer du en guide til en formel:

1. Gå til **Administration af produktionsoplysninger \> Styklister og formler \> Formler**.
1. Åbn den formel, du vil tildele en guide.
1. Åbn fanen **Overskrift** over det øverste oversigtspanel.
1. Udvid oversigtspanelet **Tilknyttede guider**.
1. Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**. Der føjes en ny linje til gitteret.
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.
    ![Føje en guide til en formel.](media/instruction-guides-Formula.png "Føje en guide til en formel")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Knytte en guide til en formelversion

Du kan føje en guide til enhver [formelversion](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Typisk scenarie, der bruger formelversioner

Guider, der er tilknyttet en enkelt version af en formel, giver produktionsarbejdere vejledning, som gennemgår produktionen af den pågældende version af formelopskriften.

> [!TIP]
> Du kan tildele vejledning, der er relevant for produktionsprocesser, ud fra denne formelversion til en rute-, ruteversions- eller ruteoperationsrelation.  

> [!NOTE]
> Guider kan i øjeblikket ikke knyttes til individuelle formellinjer.

### <a name="add-a-guide-to-a-formula-version"></a>Føje en guide til en formelversion

Sådan føjer du en guide til en formelversion:

1. Gå til **Administration af produktionsoplysninger \> Styklister og formler \> Formler**.
1. Åbn den formel, der indeholder en version, som du vil tildele en guide.
1. Åbn fanen **Overskrift** over det øverste oversigtspanel.
1. Vælg den version, du vil tildele en guide, i oversigtspanelet **Formelversioner**.
1. Vælg **Tilknyttede guider** på værktøjslinjen **Formelversioner**.
    ![Åbne de guider, der er tilknyttet en valgt formelversion.](media/instruction-guides-FormulaVersion.png "Åbne de guider, der er tilknyttet en valgt formelversion")
1. Siden **Tilknyttede guider** åbnes for din formelversion.
1. Vælg **Tilføj** i handlingsruden for at føje en ny linje til gitteret. 
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.
    ![Føje en guide til en formelversion.](media/instruction-guides-FormulaVersionAddGuide.png "Føje en guide til en formelversion")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Knytte en guide til en stykliste

Du kan føje en guide til enhver [stykliste](bill-of-material-bom.md).

### <a name="typical-scenario-using-bills-of-materials"></a>Typisk scenarie, der bruger styklister

Guider, der er tilknyttet en stykliste, giver produktionsarbejdere en vejledning, der forklarer, hvordan materiale forberedes og håndteres fra en stykliste. Guider kan også tildeles versioner af en stykliste.

> [!NOTE]
> Guider kan i øjeblikket ikke knyttes til individuelle styklistelinjer.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Føje en guide til en stykliste

Sådan føjer du en guide til en stykliste:

1. Gå til **Administration af produktionsoplysninger \> Styklister og formler \> Styklister**.
1. Åbn den stykliste, du vil tildele en guide.
1. Åbn fanen **Overskrift** over det øverste oversigtspanel.
1. Udvid oversigtspanelet **Tilknyttede guider**.
1. Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**. Der føjes en ny linje til gitteret.
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.
    ![Føje en guide til en stykliste.](media/instruction-guides-BOM.png "Føje en guide til en stykliste")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Knytte en guide til en styklisteversion

Du kan føje en guide til enhver [styklisteversion](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Typisk scenarie, der bruger styklisteversioner

Guider, der er tilknyttet en individuel styklisteversion, giver produktionsarbejdere en vejledning, der forklarer, hvordan materiale forberedes og håndteres til en version af en stykliste, der er forskellig fra den almindelige stykliste eller andre versioner af den.

> [!NOTE]
> Guider kan i øjeblikket ikke knyttes til individuelle styklistelinjer.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Føje en guide til en styklisteversion

Sådan føjer du en guide til en styklisteversion:

1. Gå til **Administration af produktionsoplysninger \> Styklister og formler \> Styklister**.
1. Åbn den stykliste, der indeholder en version, som du vil tildele en guide.
1. Åbn fanen **Overskrift** over det øverste oversigtspanel.
1. Vælg den version, du vil tildele en guide, i oversigtspanelet **Styklisteversioner**.
1. Vælg **Tilknyttede guider** på værktøjslinjen **Styklisteversioner**.
    ![Åbn de guider, der er tilknyttet en valgt styklisteversion.](media/instruction-guides-BOMVersion.png "Åbne de guider, der er tilknyttet en valgt styklisteversion")
1. Siden **Tilknyttede guider** åbnes for din styklisteversion.
1. Vælg **Tilføj** i handlingsruden for at føje en ny linje til gitteret.
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.
    ![Føje en guide til en styklisteversion.](media/instruction-guides-BOMVersionAddGuide.png "Føje en guide til en styklisteversion")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Knytte en guide til en rute

Du kan føje en guide til enhver [rute](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>Typisk scenarie, der bruger ruter

Ruter bruges typisk til at angive, hvordan et bestemt frigiveret produkt skal produceres på basis af en stykliste eller styklisteversion og med et sæt ressourcer eller ressourcegrupper.

Tildel en guide en rute for at få trinvise instruktioner til den pågældende produktionsproces.

### <a name="add-a-guide-to-a-route"></a>Føje en guide til en rute

Sådan føjer du en guide til en rute:

1. Gå til **Produktionsstyring \> Alle ruter**.
1. Åbn den rute, du vil tildele en guide.
1. Udvid oversigtspanelet **Tilknyttede guider**.
1. Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**. Der føjes en ny linje til gitteret.
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.
    ![Føje en guide til en rute.](media/instruction-guides-Route.png "Føje en guide til en rute")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Knytte en guide til en ruteversion

Du kan føje en guide til enhver [ruteversion](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>Typisk scenarie, der bruger ruteversioner

Ruteversioner bruges typisk til at angive varianter af produktionsprocesser baseret på en eksisterende rute. Du kan tildele forskellige guider til hver ruteversion.

### <a name="add-a-guide-to-a-route-version"></a>Føje en guide til en ruteversion

Sådan føjer du en guide til en ruteversion:

1. Gå til **Produktionsstyring \> Alle ruter**.
1. Åbn den rute, du vil tildele en guide.
1. Vælg den version, du vil tildele en guide, i oversigtspanelet **Versioner**.
1. Vælg **Tilknyttede guider** på værktøjslinjen **Versioner**.
    ![Åbne de guider, der er tilknyttet en valgt ruteversion.](media/instruction-guides-RouteVersion.png "Åbne de guider, der er tilknyttet en valgt ruteversion")
1. Siden **Tilknyttede guider** åbnes for din styklisteversion.
1. Vælg **Tilføj** i handlingsruden for at føje en ny linje til gitteret.
1. For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.
    ![Føje en guide til en ruteversion.](media/instruction-guides-RouteVersionAddGuide.png "Føje en guide til en ruteversion")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Knytte en guide til en ruteoperationsrelation

Du kan føje en guide til enhver [ruteoperationsrelation](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>Typisk scenarie, der bruger ruteoperationsrelationer

Operationsrelationer er den mest specifikke måde at føje guider til en produktproces og dens relaterede operationer. Du kan angive retningslinjer for hver operation i en rute og angive en anden vejledning for alle typer relationskontekster, der er angivet for en rute, f.eks. for bestemte varer, konfigurationer og meget mere. Du kan også angive, hvilke faser i operationen retningslinjerne skal gælde for (f.eks. opsætning, kø, proces eller transport).

> [!NOTE]
> Hvis du angiver guider for flere operationsrelationer for en rute, vil der blandt disse guider kun blive vist guiden fra den mest specifikke relation i produktionen for det oprettede job.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Føje en guide til en ruteoperationsrelation

Sådan føjer du en guide til en ruteoperationsrelation:

1. Gå til **Produktionsstyring \> Alle ruter**.
1. Åbn den rute, du vil tildele en guide.
1. Åbn fanen **Rute** i handlingsruden, og vælg **Rutedetaljer** i gruppen **Vedligehold**.
1. Siden **Rutedetaljer** åbnes for den valgte rute.
1. Vælg den handling, du vil give vejledning til, i det øverste gitter.
1. Vælg en specifik relation (eller den generiske **All**-relation) i nederste gitter.
    ![Vælge en operation og derefter en relation.](media/instruction-guides-RouteOperationRelation.png "Vælge en operation og derefter en relation")
1. Åbn fanen **Tilknyttede guider** oven over det nederste gitter. ![Fanen Tilknyttede guider.](media/instruction-guides-RouteOperationRelation-AddGuide.png "Fanen Tilknyttede guider")
1. Vælg **Tilføj** på værktøjslinjen øverst i det nederste gitter for at føje en ny linje til gitteret.
1. For den nye række skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele. I resten af rækken skal du markere afkrydsningsfeltet for hver kontekst, hvor den valgte guide skal være tilgængelig.

> [!NOTE]
> Du kan tilføje en eller flere guider for hver fase i hver handling.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Valgte guider fra produktionens udførelsesgrænseflade

Når en arbejder åbner en jobliste i produktionens udførelsesgrænseflade finder Supply Chain Management de relevante guider for de viste job. Du kan bruge knappen **Guider** til at få vist de relevante guider.

![Knappen Guider i produktionens udførelsesgrænseflade.](media/instruction-guides-Shopfloor1.png "Knappen Guider i produktionens udførelsesgrænseflade")

Tag derefter en HoloLens på, og få adgang til den tilhørende guide ved at studere QR-koden og aktivere den respektive guide.

![QR-kode for adgang til guider ved hjælp af en HoloLens.](media/instruction-guides-Shopfloor2.png "QR-kode for adgang til guider ved hjælp af en HoloLens")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Fortolkning af logikken for valg af guider

Du kan føje guider til følgende produktionsdata:

- [Ressourcer](#resources)
- [Ressourcegrupper](#resource-groups)
- [Frigivne produkter](#released-products)
- [Formler](#formulas)
- [Formelversioner](#formula-versions)
- [Styklister](#bom)
- [Styklisteversioner](#bom-versions)
- [Ruter](#routes)
- [Ruteversioner](#route-versions)
- [Ruteoperationsrelationer](#route-operation-relations)

Når Supply Chain Management genererer jobbene til produktionen, vil det indsamle de relevante guider fra disse kilder. Bemærk følgende vigtige regler.

- Hvis du knytter en styklisteversion eller en formelversion til en rute eller produktionsordre, vises alle de guider, der er tilknyttet denne version, samt de guider, der er knyttet til den overordnede stykliste eller formel af denne version, i jobbet.
- Hvis du knytter en ruteversion til en produktionsordre, vises alle de guider, der er tilknyttet denne version, samt de guider, der er knyttet til den overordnede rute af denne version, i jobbet.
- Hvis du definerer flere ruteoperationsrelationer, der omfatter *Alle*-relationen, og tildeler dem guider, vises kun guiderne fra den mest specifikke relation for jobbet.  

![Diagram til fortolkning af relevante guider.](media/instruction-guides-Resolve.png "Diagram til fortolkning af relevante guider")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]