---
title: Oprette foruddefinerede produktvarianter
description: Denne procedure fører dig gennem oprettelsen af produktvarianter for en produktmaster ved hjælp af kombinationer af produktdimensioner.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f78441445baecba279f96eb3935d9ebbb4ff03f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021878"
---
# <a name="predefined-product-variants"></a>Foruddefinerede produktvarianter

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Eksempelscenarie: Oprette foruddefinerede produktvarianter

Dette eksempelscenarie viser, hvordan du opretter produktvarianter for en produktmaster ved hjælp af kombinationer af produktdimensioner.

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Hvis du vil følge dette scenarie ved hjælp af de foreslåede værdier, skal du have installeret demodata, og du skal bruge den juridiske enhed *USMF*.

### <a name="step-1-create-a-product-master"></a>Trin 1: Opret en produktmaster

Sådan oprettes en produktmaster:

1. Gå til **Administration af produktoplysninger > Produkter > Produktmastere**.
1. Vælg **Ny**.
1. Hvis feltet **Produktnummer** ikke allerede viser et tal, skal du angive en værdi. Dette trin er kun påkrævet, hvis der ikke er oprettet nogen nummerserie for dette felt.
1. Indtast en navn i feltet **Produktnavn**.
1. I feltet **Produktdimensionsgruppe** skal du vælge produktdimensionsgruppen *SizeCol* (Størrelse og Farve).
1. Vælg **OK** for at oprette og åbne den nye produktmaster.

### <a name="step-2-add-product-dimensions"></a>Trin 2: Tilføj produktdimensioner

Dette eksempel viser, hvordan du manuelt angiver produktdimensioner. Du kan også vælge en størrelses-, farve- eller typografigruppe, der indeholder de produktdimensionsværdier, du vil bruge.

Sådan tilføjes produktdimensioner:

1. Når den nye produktmaster stadig er åben, skal du vælge **Produktdimensioner** i handlingsruden.
1. Åbn fanen **Størrelse**, og vælg **Ny** på værktøjslinjen for at føje en række til gitteret. Angiv følgende indstillinger for den nye række:
    - **Størrelse:** Vælg en størrelsesværdi.
    - **Navn:** Angiv et navn til størrelsen.
1. Vælg **Ny** på værktøjslinjen, og føj endnu en størrelse til gitteret med en ny **Størrelse** og et nyt **Navn**.
1. Åbn fanen **Farver**, og vælg **Ny** på værktøjslinjen for at føje en række til gitteret. Angiv følgende indstillinger for den nye række:
    - **Farve:** Vælg en farveværdi.
    - **Navn:** Angiv et navn til farven.
1. Vælg **Ny** på værktøjslinjen, og føj endnu en farve til gitteret med en ny **Farve** og et nyt **Navn**.
1. Vælg **Gem**.
1. Luk siden for at vende tilbage til den nye produktmaster.

### <a name="step-3-generate-product-variants"></a>Trin 3: Generer produktvarianter

> [!NOTE]
> I dette afsnit beskrives, hvordan du kan generere produktvarianter, når funktionen *Forbedringer af sider med variantforslag* ikke er aktiveret. Se næste afsnit for at få oplysninger om, hvordan du kan generere produktvarianter, når funktionen er tilgængelig.

Sådan genereres produktvarianter:

1. Når den nye produktmaster stadig er åben, skal du vælge **Produktvarianter** i handlingsruden.
1. Vælg **Variantforslag** i handlingsruden.
1. Systemet genererer en liste over alle de mulige kombinationer af de størrelser og farver, du har defineret for produktet. Vælg **Vælg alle** på værktøjslinjen.
    - I dette eksempel skal du vælge alle mulige varianter. Hvis du kun vil bruge et undersæt af de mulige kombinationer af produktdimensioner, skal du kun markere de nødvendige afkrydsningsfelter efter behov.  
1. Vælg **Opret**.
1. Vælg **Gem**.

## <a name="improved-variant-suggestions"></a>Forbedrede variantforslag

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

Funktionen *Forbedringer af sider med variantforslag* forbedrer siden **Variantforslag** med henblik på at løse problemer med ydeevne og anvendelighed for virksomheder, der har et stort antal kombinationer af produktdimensioner. Den forbedrede proces for valg af produktdimensionsværdier, hvor der kan genereres variantforslag, gør det hurtigere og nemmere at identificere og frigive de relevante sæt produktvarianter.

Følgende forbedringer tilføjes af denne funktion:

- **Udskudt generering af variantforslag:** Siden **Variantforslag** viser ikke længere forslag, når du åbner det første gang. I stedet skal du udtrykkeligt vælge, hvilke værdier du skal bruge, og derefter vælge knappen **Foreslå** for at generere kombinationerne. Dette gør processen mere synlig og interaktiv.
- **Valg af dimensionsværdier:** Når du har mange dimensionsværdier, er du typisk interesseret i at generere variantforslag, der kun indeholder nogle få af dem (f.eks. når du introducerer et nyt sæt farver eller typografier). Med det forbedrede design kan du vælge de dimensionsværdier, du vil generere produktvariantforslag for. Dette øger relevansen af de foreslåede varianter markant og forbedrer både systemets ydeevne og brugerens produktivitet.

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a>Aktivere funktionen Forbedringer på side med variantforslag

Før du kan bruge funktionen *Forbedringer af side med variantforslag*, skal den være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Administration af produktoplysninger*
- **Funktionsnavn:** *Forbedringer af side med variantforslag*

### <a name="work-with-the-improved-variant-suggestions"></a>Arbejde med de forbedrede variantforslag

Sådan genereres forslag til produktvarianter, når funktionen *Forbedringer af side med variantforslag* er aktiveret:

1. Åbn eller opret en produktmaster, og tilføj de nødvendige produktdimensioner som beskrevet i forrige afsnit.
1. Når produktmasteren er åben, skal du vælge **Produktvarianter** i handlingsruden.
1. Vælg **Variantforslag** i handlingsruden.
1. Vælg de værdier, du vil bruge til de enkelte dimensioner.
1. Vælg **Foreslå** på den øverste værktøjslinje.
1. Systemet genererer en liste over alle de mulige kombinationer af de størrelser og farver, du har valgt. I oversigtspanelet **Foreslåede varianter** skal du markere afkrydsningsfeltet for hver kombination af produktdimensioner, du vil bruge, eller vælg **Vælg alle** på værktøjslinjen for at vælge dem alle.  
1. Vælg **Opret** for at føje varianter til den aktuelle produktmaster.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
