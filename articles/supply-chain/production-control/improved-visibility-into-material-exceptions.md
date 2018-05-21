---
title: Synlighed i materialeundtagelser
description: "I dette emne beskrives, hvordan du kan få bedre indsigt i undtagelser for råmaterialer til produktionsordrer og batchordrer."
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: eca3141fc48aea24411524e5fc84686d9e4bfaa7
ms.contentlocale: da-dk
ms.lasthandoff: 03/07/2018

---
# <a name="visibility-into-material-exceptions"></a>Synlighed i materialeundtagelser

[!include [banner](../includes/banner.md)]

I arbejdsområdet **Administration af produktion** findes tre felter, som giver dig bedre indblik i undtagelser for råmaterialer til produktionsordrer og batchordrer:

- Ikke-frigivne materialelinjer, der kræver opmærksomhed
- Ubehandlede bølger, der kræver opmærksomhed
- Åbent lagerstedsarbejde, der kræver opmærksomhed

For alle tre felter sammenlignes råvaredatoen for styklistelinjerne og formellinjerne med datoen i arbejdsområdet og også med filtrene for **Produktionsenhed**, **Ressourcegruppe** og **Ressource**, der indstilles i menuen **Konfigurere mit arbejdsområde**. Som standard er datoen for arbejdsområdet indstillet til dags dato, men du kan ændre den.

En ikke-frigivet styklistelinje eller formellinje kræver opmærksomhed, hvis råvaredatoen på linjen er den samme som eller tidligere end datoen i arbejdsområdet, og hvis den opfylder de kriterier, der er defineret af filtrene i arbejdsområdet.

I følgende figur repræsenterer den blå linje et produktionsjob, der er planlagt for en ressource. Jobbet er planlagt til at starte d. 1. maj 2017 (01-05-2017). Datoen er råvaredatoen. Med andre ord skal de råvarer, der er tildelt til jobbet på stykliste- og formellinjerne være klar på denne dato. Den anden dato i figuren, den 6. maj 2017 (06-05-2017), repræsenterer datoen i arbejdsområde. I dette eksempel er råvaredatodatoen tidligere end datoen i arbejdsområdet. Derfor er den dato, hvor forbrug af råvarer skulle starte, overskredet, og stykliste- og formellinjerne opfylder for kriterierne for, hvornår de kræver opmærksomhed.

![Eksempel på et produktionsjob, hvor råvaredatodatoen er før datoen i arbejdsområdet.](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Ikke-frigivne materialelinjer, der kræver opmærksomhed

En stykliste- eller formellinje kan frigives til lageret på tre måder:

- Som en del af en produktionsordre- eller batchordrefrigivelse
- Som en manuel frigivelse
- Automatisk via et batchjob

Du kan finde flere oplysninger under [Frigive stykliste- og formellinjer til lageret](releasing-bom-and-formula-lines-to-warehouse.md). 

Hvis en stykliste- eller formellinje ikke er blevet frigivet, eller kun delvist er blevet frigivet, og hvis dato- og filterkriterierne i arbejdsområdet er opfyldt, indgår linjen i beregningen af det antal, der vises i feltet **Ikke-frigivne materialelinjer, der kræver opmærksomhed**.

Når du vælger feltet, åbnes siden **Frigiv til lagersted**. Denne side viser antallet af ikke-frigivne stykliste- og formellinjer, som er angivet af tallet i feltet. De ikke-frigivne linjer vises i øverste gitter. Dette gitter viser det antal, der oprindeligt blev anslået for linjen, det antal, der allerede er frigivet, og det resterende antal, der stadig skal frigives. Du kan tilføje linjer fra det øverste gitter i det nederste gitter. Du kan derefter frigive de valgte linjer fra det nederste gitter til lageret. Du kan også justere det antal, der skal frigives fra det nederste gitter, så kun en delmængde frigives.

## <a name="unprocessed-waves-needing-attention"></a>Ubehandlede bølger, der kræver opmærksomhed

Når en stykliste- eller formellinje er frigivet, føjes den til en ny produktionsbølge eller en eksisterende åben bølge, afhængigt af konfigurationen af produktionsbølgeskabelonen. Via konfigurationen af bølgeskabelonen kan du også angive en bølge, så den automatisk behandles, når en stykliste- eller formellinje frigives. Når bølgen er behandlet, oprettes lagerstedsarbejde for råvarepluk. Hvis bølgeskabelonen er konfigureret, så bølger ikke behandles på tidspunktet for frigivelsen, forbliver bølgen i ubehandlet-tilstand. Feltet **Ubehandlede bølger, der kræver opmærksomhed** viser det antal stykliste- og formellinjer, der er frigivet til lageret i ubehandlede bølger, og som har en råvaredato, der er tidligere end eller lig med datoen i arbejdsområdet. Linjerne skal også forbruges af en operationsressource, der gælder for filteret i arbejdsområdet.

Når feltet er markeret, åbnes siden **Alle produktionsbølger**. Denne side filtreres efter antallet af åbne bølger, der indeholder bølgelinjer fra frigivne stykliste- og formellinjer, der opfylder kriterierne for feltet. Fra siden **Alle produktionsbølger** kan du behandle bølgen manuelt.

## <a name="open-warehouse-work-needing-attention"></a>Åbent lagerstedsarbejde, der kræver opmærksomhed

Feltet **Åbent lagerstedsarbejde, der kræver opmærksomhed** viser det antal stykliste- og formellinjer, der er frigivet til lageret i ubehandlede bølger, og som har ubehandlet arbejde, der er tidligere end eller lig med datoen i arbejdsområdet. Linjerne skal også forbruges af en operationsressource, der gælder for filteret i arbejdsområdet.

Når feltet er markeret, åbnes siden **Alt arbejde**. Denne side filtreres efter antallet af åbne arbejdsoverskrifter, der indeholder arbejdslinjer fra frigivne stykliste- og formellinjer, der opfylder kriterierne for feltet. Fra siden **Alt arbejde** kan du behandle arbejdet manuelt.

