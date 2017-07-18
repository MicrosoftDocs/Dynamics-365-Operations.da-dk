---
title: Oversigt over produktoplysninger
description: "Dette emne indeholder oplysninger om administration af produktoplysninger. Administration af produktoplysninger fungerer sammen med en fælles produktdefinition, kategorisering og identifikatorer på tværs af alle juridiske enheder, og også med bestemte konfigurationer af et produkt, så det passer til forretningsprocesserne."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: db8a9666518b58b6b32bb4a14933095dd9416aa0
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="product-information-overview"></a>Oversigt over produktoplysninger

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Dette emne indeholder oplysninger om administration af produktoplysninger. Administration af produktoplysninger fungerer sammen med en fælles produktdefinition, kategorisering og identifikatorer på tværs af alle juridiske enheder, og også med bestemte konfigurationer af et produkt, så det passer til forretningsprocesserne. 

Produktoplysninger er udgangspunkt for supply chain- og detailprogrammer på tværs af alle brancher. Det refererer til processer og teknologier, der har fokus på central administration af oplysninger om produkter (f.eks. på tværs af supply chains). Det er vigtigt, at der bruges delte produktdefinitioner, dokumentation, attributter og identifikatorer. I de forskellige moduler i en virksomhedsløsning, kræves der produktspecifikke oplysninger og konfigurationer for at administrere de forretningsprocesser, der er relateret til bestemte produkter, produktfamilier eller produktkategorier.

## <a name="product-definition"></a>Produktdefinition

Et produkt defineres primært af produktnummer, navn og beskrivelse. Andre data er dog også nødvendige for at beskrive en vare eller tjenesteydelse:

- Produkttype: Vare eller tjenesteydelse
- Produktundertype: Specifikke produkter eller produktmastere
- Definition af produktvariantmodellen:

     - Produktdimensioner og dimensionsgrupper
     - Produktnomenklatur
     - Produktkonfigurationsmodeller

- Tilknytning af produktet til en eller flere kategorier
- Definition af produkt- og kategoriattributterne
- Produktbilleder
- Vedhæftede filer
- Måleenheder og relaterede konverteringer
- Oversættelser af alle navne og beskrivelser

## <a name="distribution-export-and-import-of-product-data"></a>Distribution, eksport og import af produktdata

Produktdefinitionen kan oprettes i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Den kan også importeres fra styring af systemer til produktlivscyklus (PLM), produktdatastyring (PDM) eller administration af produktoplysninger (PIM). Når der bruges mere end én forekomst af Finance and Operations, bruges der som regel én forekomst som produktdatamaster for alle andre forekomster. Denne fremgangsmåde understøttes af en stor mængde dataenheder, der aktiverer eksport og import af produktdefinitionsdata fra én forekomst til en anden.

For at understøtte distributionen af produktdata til mange forekomster kan du bruge tjenesten Common Data Service i Finance and Operations. Produktdefinitionerne kan eksporteres fra en forekomst af Finance and Operations til Common Data Service. Produktdefinitionerne kan derefter bruges til at klargøre andre forretningsprogrammer, f.eks. Microsoft Dynamics 365 for Sales, med produktdata.

Bemærk, at i dynamiske og fleksible organisationer ændres produktoplysningsdata hver dag. Vedligeholdelse af nøjagtige og faktiske produktdata er derfor en forretningsproces, der er vigtig i sig selv.

## <a name="product-masters-and-product-variants"></a>Produktmastere og produktvarianter

I en fleksibel verden, hvor produkter hurtigt skal kunne tilpasses kundebehov, angiver produktdefinitioner et sæt produkter i stedet for specifikke produkter. I Microsoft Dynamics 365 for Finans and Operations kaldes disse generiske produkter for *produktmastere*. Produktmastere indeholder definitioner og regler, der angiver, hvordan specifikke produkter beskrives og fungerer i forretningsprocesser. Baseret på disse definitioner, kan der genereres specifikke produkter. Disse specifikke produkter kaldes for *produktvarianter*.

I Finance and Operations er en produktmaster knyttet til en produktdimensionsgruppe og en konfigurationsteknologi for at angive forretningsreglerne. Produktdimensionerne (farve, størrelse, type og konfiguration) er et bestemt sæt attributter, der kan bruges i hele programmet til at definere og spore specifikke funktionsmåder for relaterede produkter. Disse dimensioner kan også hjælpe brugerne med at søge efter og identificere produkterne.

## <a name="configuration-technologies"></a>Konfigurationsteknologier

Du kan vælge mellem tre konfigurationsteknologier:

- De foruddefinerede varianter er defineret af foruddefinerede produktdimensioner. Variantdefinitionen omfatter definitionen af en bestemt, gyldig kombination af dimensioner, f.eks. farve, type og størrelse. Hver kombination resulterer i en specifik produktvariant.
- Den dimensionsbaserede konfiguration bruges typisk i produktionsscenarier, og du kan bruge konfigurationsdimensionen i definitionen af styklister. Når du har valgt en bestemt konfiguration, bruges det undersæt af styklistelinjer, der gælder for konfigurationen, til planlægning og produktion. Dette begreb kaldes også for *global stykliste*, fordi der bruges én fælles stykliste til alle konfigurationer af et produkt.
- Begrænsningsbaseret konfiguration bruger en produktkonfigurationsmodel til at beskrive alle mulige attributter og komponenter, der kræves for at beskrive alle mulige varianter af et produkt i en enkelt model. Begrænsningerne af attributkombinationer kan beskrives med regulære udtryk eller tabelbaserede begrænsninger. Produktkonfigurationsmodeller og -styringer bliver stadig vigtigere i administration af produktoplysninger og bruges på tværs af alle brancher.

Når du planlægger implementeringen af Finance and Operations, er det meget vigtigt, at du vælger den korrekte konfigurationsteknologi for en forretningsproces. Et produkt kan ikke konverteres fra én model til en anden efter implementeringen.

## <a name="product-variant-model-definition-workspace"></a>Arbejdsområdet Definition af produktvariantmodel

Arbejdsområdet **Definition af produktvariantmodel** giver et overblik over produktmasterne. Det viser også status for udgivelse af mastere og relaterede varianter til specifikke juridiske enheder.

## <a name="released-products"></a>Frigivne produkter

De produkter, der frigives til en bestemt juridisk enhed, kaldes *frigivne produkter*. Produkter kan frigives samlet i én juridisk enhed eller mange juridiske enheder ad gangen. Da der evt. skal tilføjes forskellige egenskaber og attributter for produkterne pr. juridisk enhed, kan du i arbejdsområdet **Vedligeholdelse af frigivet produkt** overvåge og fuldføre de nyligt frigivne produkter i hver juridisk enhed eller i underorganisationerne i en juridisk enhed.

### <a name="released-product-maintenance-workspace"></a>Arbejdsområdet Vedligeholdelse af frigivet produkt

Du kan konfigurere arbejdsområdet **Vedligeholdelse af frigivet produkt** i menupunktet **Konfigurer mit arbejdsområde**. Vælg et kategorihierarki og en kategori, som du vil filtrere arbejdsområdet efter. Hvis du vil justere de relevante produktoplysninger i arbejdsområdet, du kan også definere, i dage, tidshorisonter for **Produkter, der er frigivet for nylig** og **Stoppede frigivne produkter**.

Arbejdsområdet består af en oversigt over felter og to lister. Listen **Åbne sager** viser produktændringssager, der har produkter i det valgte produktkategorihierarki, som ikke er afsluttet og lukket. Listen **Frigivet for nylig** viser de produkter, der er udgivet inden for den tidshorisont, der er angivet i konfigurationen af arbejdsområdet. Valideringen udføres for hvert element på listen, og der vises en valideringsstatus. Denne status kan indikere, at den nødvendige konfiguration for den juridiske enhed ikke er fuldført. På listen har du direkte adgang til siderne **Frigivne produktdetaljer**, **Vedligeholdelse af produktattribut**, **Vedligeholdelse af produktkategori**, **Standardindstillinger for ordre** og **Oversættelser af tekst** for at fuldføre den påkrævede konfiguration af produktet.

### <a name="manually-creating-a-new-released-product"></a>Manuel oprettelse af et nyt frigivet produkt

Du kan manuelt oprette et frigivet produkt i en enkelt kørsel afhængigt af organisationens forretningsprocesser og eventuelle regler om, hvorvidt denne funktion skal bruges. Denne funktion opretter et nyt produkt, og frigør det automatisk til den aktuelle juridiske enhed. Hvis du vil oprette et nyt produkt, skal du klikke på listesiden **Frigivne produkter** i arbejdsområdet **Vedligeholdelse af frigivet produkt** eller på listesiden **Frigivet produkt**.
