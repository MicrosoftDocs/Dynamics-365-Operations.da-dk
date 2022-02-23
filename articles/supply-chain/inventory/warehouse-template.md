---
title: Konfigurere et lagersted ved hjælp af en skabelon til konfiguration af lagersted
description: I dette emne beskrives, hvordan du konfigurerer et lagersted ved hjælp af en skabelon til konfiguration af lagersted.
author: perlynne
manager: tfehr
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d533eed984c188c5b6520232f2b875bddd1f57bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967124"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Konfigurere et lagersted ved hjælp af en skabelon til konfiguration af lagersted

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer et lagersted ved hjælp af en skabelon til konfiguration af lagersted. Der findes flere foruddefinerede konfigurationsskabeloner, som du kan bruge. Du kan finde oplysninger om, hvordan du kan bruge disse skabeloner, i [Konfigurationsdataskabeloner](../../dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Scenarier, hvor konfigurationsskabeloner kan være nyttige

Konfigurationsskabeloner kan være nyttige i mange scenarier. Her er nogle eksempler:

- Du har fuldført og testet en konfigurationsopsætning i et testmiljø, og nu skal du kopiere opsætningen til et produktionsmiljø.
- Du vil rulle lagerstedsopsætningen ud til flere juridiske enheder eller oprette et nyt lagersted i den samme juridiske enhed.
- Du vil hurtigt forberede en demo af lagerstedsfunktionerne.
- Du vil have, at eksisterende varer og lagersteder kan bruge funktionerne i Lokationsstyring i stedet for funktionerne i Lagerstyring.

I dette emne beskrives det første af disse scenarier. Den viser, hvordan du kan bruge en konfigurationsskabelon til at kopiere en konfigurationsopsætning fra et testmiljø til et produktionsmiljø.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Kopiere en konfigurationsopsætning fra et testmiljø til et produktionsmiljø

I dette scenarie findes konfigurationsopsætningen for et lagersted og nogle transaktionsprocesser allerede i et testmiljø. Du vil nu kopiere konfigurationsopsætningen for lagerstedet fra testmiljøet til et produktionsmiljø.

> [!NOTE]
> Det er vigtigt, at du medtager andre relaterede opsætningsdata, når du kopierer en konfigurationsopsætning. Du vil for eksempel konfigurere produkter ved at kopiere opsætningen fra et testmiljø. Du kan dog ikke konfigurere en fast plukplads for et produkt, før produktet er oprettet. Selvom individuelle konfigurationsskabeloner ikke understøtter denne type afhængighed, findes der standarddataskabeloner, der understøtter funktionen. Du kan nemt medtage disse standardskabeloner i en konfigurationsproces.

### <a name="export-a-default-warehouse-template"></a>Eksportere en standardlagerstedsskabelon 

1. Åbn arbejdsområdet **Datastyring**.

    > [!NOTE]
    > Hvis du bruger dette arbejdsområde for første gang, skal du indlæse alle dataenheder, før du fortsætter.

2. Vælg feltet **Skabeloner**, og vælg derefter **Indlæs standardskabeloner** for at indlæse standardskabelonerne.

    > [!NOTE]
    > **Indlæs standardskabeloner** er kun tilgængelig i visningen **Udvidet**. Vælg **Rammeparametre** og vælg derefter **Vis standarder** i feltet **Udvidet visning** .

3. Når standardskabelonerne er indlæst, kan du ændre dem, så de opfylder dine forretningsbehov.

    > [!NOTE]
    > For at indlæse standardskabeloner og importere skabeloner skal du have administratoradgang. Dette krav hjælper med at sikre, at alle enheder er korrekt indlæst i skabelonen.

4. Kontroller, at du er i den juridiske enhed, som du vil eksportere de firmaspecifikke data fra.
5. I arbejdsområdet skal du vælge **Eksportér**.
6. Opret et nyt eksportprojekt.
7. Vælg **+ Tilføj skabelon**, og find **400 - WMS** standardskabelonen for lagerstedet. Denne skabelon tilføjer dataenheder til konfiguration af lagersted.

    > [!NOTE]
    > Hvis de data, du eksporterer, skal filtreres (f.eks. hvis du kun vil eksportere de data, der er relateret til et bestemt lagersted), skal du evaluere hver dataenhed og tilføje filtrering via en forespørgsel. Du kan også eksportere alle data og derefter slette de poster, der ikke er behov for i destinationsfilerne.

8. Vælg **Eksportér**. Data, der er knyttet til alle dataenhederne i projektet, eksporteres.

Du kan hente en zip-fil til datapakken. Denne fil indeholder alle data i det valgte format (f.eks. Excel-format). Som nævnt skal nogle poster i filerne i datapakken muligvis opdateres, før du kan importere dem til produktionsmiljøet. Hvis du opdaterer en post, skal du sørge for ikke at ændre filnavnet.

### <a name="import-a-warehouse-configuration-setup"></a>Importere en opsætning af en lagerstedskonfiguration

1. Sørg for, at du er i det firma, du vil importere lagerstedsdataene til, i destinationsmiljøet.

    > [!NOTE]
    > Før du foretager importen, skal du identificere eventuelle dataafhængigheder. For eksempel omfatter skabelonen **Lokationsstyring** en dataenhed, der hedder **Dispositionskoder for lagerstedet**. Denne enhed indeholder data, der er relateret til opsætningssiden **Dispositionskoder** (**Lokationsstyring** > **Opsætning** > **Mobilenhed** > **Dispositionskoder**). Hvis en eksisterende opsætning allerede håndterer returvareprocessen for salgsordrer, indeholder feltet **Returdispositionskode** en værdi. Dispositionskoden i dette felt er relateret til dataenheden **Dispositionskode**, som er en del af skabelonen **Salg og marketing**. Hvis dataene fra dataenheden **Dispositionskode** ikke blev importeret, før dataene fra feltet **Dispositionskoder for lagerstedet**, mislykkes importen.

2. I arbejdsområdet **Datastyring** skal du vælge **Importér**.
3. Opret et nyt importprojekt.
4. Vælg **+ Tilføj fil**, og overfør zip-filen til datapakken.
5. Vælg **Importér**. I visningen **Udvidet** visning kan du bruge indstillingen **Filter** til at få hurtigt overblik over de problemer, der kan opstå under importen.

Loggen **Vis udførelseslog** indeholder detaljerede oplysninger om hver dataenhed, der importeres. Du kan bruge den midlertidige datavisning til hurtigt at komme til måldataene. På denne måde kan du se, hvordan de importerede data ser ud på de relaterede sider i programmet. Når du bruger standarddataskabelonerne, fungerer importrækkefølgen for hver dataenhed på den foruddefinerede måde for at sikre, at alle afhængige data importeres først. Hvis brugerdefinerede dataenheder er del af projektet, skal du sikre dig, at den korrekte rækkefølge er defineret. Du kan finde flere oplysninger i [Konfigurere dataskabeloner](../../dev-itpro/data-entities/configuration-data-templates.md).

Hvis du vil vide mere om, hvordan du kan bruge lagerstedsskabelon til at kopiere konfigurationen af et lagersted fra ét firma til et nyt firma i den samme forekomst, kan du se denne 3 minutters video på YouTube om [hvordan du bruger lagerstedsskabelon til at kopiere konfigurationen til Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-topic"></a>Relateret emne

[Konfigurationsdataskabeloner](../../dev-itpro/data-entities/configuration-data-templates.md)
