---
title: Foretage fejlfinding af produktoplysninger
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med produktoplysninger.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 87b04998889b86a79fd8dabde422147c5494b003
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516753"
---
# <a name="troubleshoot-product-information"></a>Foretage fejlfinding af produktoplysninger

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med produktoplysninger.

## <a name="i-cant-delete-a-released-product"></a>Jeg kan ikke slette et frigivet produkt.

### <a name="issue-description"></a>Problembeskrivelse

Du kan kun slette et frigivet produkt og alle dets varianter, hvis der ikke er relaterede transaktioner for det frigivne produkt.

### <a name="issue-resolution"></a>Problemløsning

Udfør følgende trin for at slette en frigivet produkt eller produktmaster.

1. Luk alle åbne transaktioner for varerne.
1. Reducer lagerbeholdningen til 0 (nul).
1. Udfør lagerlukning.
1. Slet alle produktvarianter for den produktmaster, du vil slette.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Kan jeg ændre varenummeret for et frigivet produkt?

I de fleste tilfælde kan du ikke redigere varenumre for frigivne produkter, fordi ændringen vil medføre, at dataene bliver beskadiget. Du kan kun redigere varenummeret, hvis du skal reparere databeskadigelse, som blev forårsaget af en tidligere omdøbning af den primære nøgle for det frigivne produkt, som angivet på listen over [fjernede eller udfasede funktioner til Finance and Operations 10.0.0 med Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).

Hvis du vil have mulighed for at redigere varenumre for frigivne produkter, skal du [stemme for denne ide i portalen Ideer](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Standardrydningsprincippet fra produktet angives ikke på styklistelinjen.

### <a name="issue-description"></a>Problembeskrivelse

Når du føjer en vare til en styklistelinje, bruger systemet ikke de standardoplysninger om rydningsprincippet, der er konfigureret for varen. Det vil sige, at rydningsprincippet fra varen ikke vises på siden **Styklistelinje**.

### <a name="issue-resolution"></a>Problemløsning

Hvis du angiver et rydningsprincip på en styklistelinje, vil det gælde for den pågældende styklistelinje. Men hvis træk rydningsprincippet er tomt, eller hvis det ikke er angivet på en styklistelinje, gælder det rydningsprincip, der er angivet for varen, stadig for den pågældende styklistelinje, selvom den ikke vises på styklistelinjen.

Standardlogikken for andre funktioner i Microsoft Dynamics 365 Supply Chain Management fungerer normalt ikke på denne måde. Men den aktuelle funktionalitet kan ikke ændres. Ellers vil nogle af de eksisterende tilpasninger, der er afhængige af den, være brudte.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Du kan bruge systemet til at gemme dublerede stregkoder for forskellige varer eller for den samme vare, der har forskellige dimensioner.

Systemet gennemtvinger ikke entydige stregkoder i øjeblikket, og tilføjelsen af denne begrænsning vil være en nyskabende ændring. Microsoft har faktisk bevis på, at nogle eksisterende kundeinstallationer vil blive beskadiget af denne ændring. Vi vil dog overveje en bredere designændring for at aktivere denne funktion i fremtiden.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Jeg modtager følgende fejlmeddelelse, når jeg redigerer varepostskabeloner: "Lagerlokationen kan ikke oprettes, fordi varen ikke er på lager. Til lagervarer skal indstillingen Lagerført produkt på den tilknyttede varemodelgruppe vælges".

### <a name="issue-description"></a>Problembeskrivelse

Dette problem opstår, hvis du følger disse trin i et forsøg på at oprette en skabelon for en vare, der ikke er på lager.

1. Åbn et frigivet produkt, der ikke er på lager.
1. I handlingsruden skal du under fanen **Indstillinger** vælge **Postoplysninger**.
1. Vælg **Regnskabsskabelon** i dialogboksen **Postoplysninger**.

I dette tilfælde får du vist følgende fejlmeddelelse:

> Lagerlokationen kan ikke oprettes, da varen ikke er på lager. Til lagervarer skal indstillingen Lagerført produkt på den tilknyttede varemodelgruppe vælges.

### <a name="issue-resolution"></a>Problemløsning

Processen med at oprette produktskabeloner kræver en ekstra produktspecifik logik. Du kan derfor ikke bruge standardknappen **Regnskabsskabelon** til dette formål. Ellers skal du udføre disse trin.

1. Åbn et frigivet produkt.
1. I gruppen **Ny** under fanen **Produkt** i handlingsruden skal du vælge **Skabelon \> Opret delt skabelon**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Hjælp-standardtekst, der tilføjes i produktattributter, angives ikke i et frigivet produkt.

En beskrivelse og hjælp-tekst, der tilføjes i produktattributterne, kan ikke ses eller angives som standard i de frigivne produkter. Denne funktionsmåde er tilsigtet.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Det standardantal, der angives, er forskelligt, når det registreres fra en stykliste, og når det registreres fra en styklisteversion.

### <a name="issue-description"></a>Problembeskrivelse

Når du føjer en vare til en stykliste, angives antallet som standard til 1 i stedet for det antal, der er defineret i feltet **Min. ordreantal** på siden **Standardindstillinger for ordre** for et valgt produkt. Men når du tilføjer en vare fra en styklisteversion, og varen og varianten vælges, tager det antal, der angives som standard, det minimumantal, der er angivet i standardordreindstillingerne for de specifikke dimensioner, i betragtning.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde forventes. Men det faktum, at logikken er forskellig i styklisten og styklisteversionen, er et kendt problem. Denne funktionsmåde ændres dog ikke, fordi en ændring kan påvirke mange forskellige kundescenarier.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>Jeg kan ikke ændre de vedhæftede billeder, der er overført fra dataobjektet for vedhæftede filer i produktdokumentet, i de frigivne produktoplysninger.

### <a name="issue-description"></a>Problembeskrivelse

Dette problem kan opstå, når du knytter et billede til en vare ved hjælp af dataobjektet *Vedhæftede filer i produktdokument*. I dette tilfælde vises varebilledet for varen. Men hvis du vælger **Skift billede**, vises intet på listen over overførte billeder. Der vises desuden ingen vedhæftede filer for varen.

### <a name="issue-resolution"></a>Problemløsning

Enheden *EcoResProductDocumentAttachmentEntity* (*Vedhæftede filer i produktdokument*) importerer vedhæftede dokumenter for *produkter*, men ikke for *frigivne produkter*. (Frigivne produkter kaldes også *varer*). Hvis du vil have vist vedhæftede filer for en vare på siden **Frigivne produktdetaljer**, skal du bruge enheden *EcoResReleasedProductDocumentAttachmentEntity* (*Vedhæftede frigivne produktdokumenter*) i stedet.

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Microsoft Flow-connectoren viser følgende fejlmeddelelse: "Opdatering ikke tilladt for feltet 'ProductNumber'".

### <a name="issue-description"></a>Problembeskrivelse

Dette problem opstår, hvis du forsøger at opdatere feltet **Produktnummer** ved hjælp af *Frigivne produkter*-enhed V2 og Microsoft Flow.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde forventes. Muligheden for at redigere produktnummeret for et frigivet produkt er fjernet i Dynamics 365 Finance and Operations 10.0.0 med Platform Update 24 for at hjælpe med at forhindre databeskadigelse. I undtagelsestilfælde, hvor du har brug for at reparere databeskadigelse forårsaget af en tidligere omdøbning af primærnøglen for et frigivet produkt, kan du kontakte Microsoft Support for at anmode om midlertidig fjernelse af denne begrænsning.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Jeg kan ikke oprette en frigivet produktvariant i en anden juridisk enhed.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du forsøger at frigive en produktmaster uden varianter og derefter opretter varianterne i de enkelte juridiske enheder (firma), efterhånden som de er påkrævede, kan du ikke frigive varianterne ved hjælp af variantforslag. Du kan heller ikke oprette varianterne manuelt.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet. Relationen mellem en produktmaster og de dimensioner, masteren kan tage, opbevares på et delt niveau. Derfor kan du ikke oprette de tilgængelige dimensioner for en delt produktmaster i den specifikke juridiske enhed, hvor disse dimensioner frigives, og derefter replikere processen i hver juridiske enhed, hvor dimensionerne er påkrævet. Du skal i stedet ændre din frigivelsesproces for at kunne tilpasse den designede proces.

Her er processen for frigivelse af produkter.

1. Opret den delte produktmaster og de dimensioner, der kan frigives til de juridiske enheder.
1. Frigiv produkterne til de juridiske enheder ved enten at bruge variantforslag eller ved manuelt at tilføje de kombinationer, der skal frigives.

Du kan også oprette et frigivet produkt direkte.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Når jeg frigiver en variant i et andet firma, får jeg vist følgende fejlmeddelelse: "Der er allerede oprettet en produktvariant med de angivne dimensioner".

### <a name="issue-description"></a>Problembeskrivelse

Hvis en produktvariant allerede er frigivet i firma A, og du forsøger at frigive den i firma B ved hjælp af knappen **Ny** på siden **Frigivne produktvarianter**, får du vist følgende fejlmeddelelse:

> Produktvariant med angivne dimensioner er allerede oprettet.

### <a name="issue-resolution"></a>Problemløsning

Knappen **Ny** på siden **Frigivne produktvarianter** opretter varianten og frigiver den i firmaets kontekst. Hvis varianten allerede er oprettet, kan du ikke bruge knappen **Ny** til at frigive den i et andet firma.

Du kan løse problemet ved at åbne **Produktmaster**-siden og vælge **Frigiv produkt** for at frigive den eksisterende variant i det ønskede firma.
