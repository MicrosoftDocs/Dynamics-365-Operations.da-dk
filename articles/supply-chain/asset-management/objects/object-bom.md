---
title: Aktivstyklister
description: Denne artikel beskrives aktivstyklister i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 665c705e3ffb617fc159a1223cb3f776878d5cd2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016240"
---
# <a name="asset-boms"></a>Aktivstyklister

[!include [banner](../../includes/banner.md)]

 

Denne artikel beskrives aktivstyklister i Styring af aktiver. På siden **Aktivstykliste** vises en oversigt over alle varer (reservedele og andre varer), der bruges på et aktiv i hele dets levetid. Når du opretter et nyt aktiv, bør du overveje at oprette en aktivstykliste som en del af opsætningsproceduren. På denne måde kan du spore varehistorikken for aktivet fra oprettelsesdatoen.

Når du har fuldført et vedligeholdelsesjob, og vareforbruget er registreret på en arbejdsordre, kan du spore forbruget af reservedele og andre varer, der bruges på aktivet. Denne funktion giver dig mulighed for at beholde en komplet vareforbrugspost for alle dine aktiver. Du kan for eksempel bruge posten til at overvåge, om en bestemt reservedel ofte udskiftes, eller til at holde styr på de reservedele eller andre elementer, der i øjeblikket bruges på et aktiv.

> [!NOTE]
> På en arbejdsordre kan vareforbruget omfatte både reservedele og andre ekstra varer, såsom smøremidler, bolte og pakninger.

En aktivstykliste kan opdateres automatisk på grundlag af opsætningen i Styring af aktiver. Hvis der er oprettet en livscyklustilstand for arbejdsordren med henblik på at håndtere afsluttede eller fuldførte arbejdsordrer, og hvis indstillingen **Opdater aktivstykliste** for den pågældende arbejdsordres livscyklustilstand er angivet til **Ja** på siden **Arbejdsordrers livscyklustilstande**, vil alle varer, der anvendes til arbejdsordren, automatisk blive opdateret på siden **Aktivstykliste**, når arbejdsordren opdateres til den pågældende livscyklustilstand. 


Du kan også opdatere en aktivstykliste manuelt ved at oprette nye varelinjer på siden **Aktivstykliste**.

På siden **Aktiv stykliste** kan du spore reservedelshistorikken for aktiver, når vareforbruget er blevet registreret på en arbejdsordre. Hvis du vil bruge denne funktion, skal du vælge de varegrupper, der skal bruges til reservedelsregistreringen på siden **Reservedelsvaregrupper**.

Hvis du vil bruge funktionen aktivstykliste, skal du først oprette de påkrævede reservedelsvaregrupper. Hvis du ønsker, at aktivstyklisten automatisk opdateres, når en arbejdsordre er fuldført, kan du dernæst oprette en livscyklustilstand for arbejdsordren for at håndtere den pågældende opdatering. 


## <a name="set-up-spare-parts-item-groups"></a>Konfigurer reservedelsvaregrupper

Opsætningen af reservedelshistorik er baseret på varegrupper, der er oprettet i modulet **Lager- og lokationsstyring**. I Styring af aktiver skal du oprette varegrupper, således at du kan spore reservedelshistorikken for varerne i de valgte varegrupper.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Reservedelsvaregrupper**.
2. Vælg **Ny** for at oprette en varegruppe.
3. I feltet **Varegruppe** vælges gruppen. Navnet på gruppen indtastes automatisk i feltet **Navn**.

## <a name="view-and-update-asset-boms"></a>Se og opdater aktivstyklister

Når du bogfører vareforbruget på en arbejdsordre, kan du få vist det registrerede vareforbrug på siden **aktivstykliste**.

1. Vælg **Styring af aktiver** \> **Aktiver** \> **Alle aktiver**. Vælg aktivet på listen, og vælg derefter **Aktivstykliste**.

    > [!NOTE]
    > Hvis du vil se alle registreringer af vareforbrug, skal du vælge **Styring af aktiver** \> **Forespørgsler** \> **Aktiver** \> **Aktivstykliste**.

2. Vælg **Opdater aktivstykliste**. Du kan føje aktiver, aktivtyper og ressourcer til opdateringen efter behov ved at vælge **Vælg.** Vælg **OK** for at starte opdateringen. Du kan også konfigurere funktionen Opdater som et batchjob.
3. Hvis du vil se flere oplysninger, der er relateret til varerne, kan du tilføje lagerdimensioner. Vælg **Lager** \> **Vis dimensioner**, og markér derefter kasserne ud for de dimensioner, du ønsker at se. Hvis du vil beholde denne opsætning for alle aktiver skal du på siden **Aktivstykliste** angive indstillingen **Gem opsætning** til **Ja**.
4. Hvis du vil have en oversigt over, hvor i Styring af aktiver varen på den valgte linje bruges, skal du i relation til aktiver, jobtypestandarder, reservedele og arbejdsordrer vælge **Vare, hvor det er brugt**. 
5. Hvis du kun vil se aktive varelinjer, skal du vælge **Se** \> **Nuværende**. Hvis du vil se alle varelinjer, herunder linjer, hvor udløbsdatoen er tidligere end den aktuelle dato, skal du vælge **Se** \> **Alle**.

> [!NOTE]
> Når du har fuldført en arbejdsordre, anbefaler vi, at du opdaterer aktivstyklisten i overensstemmelse hermed, hvis nogle af de varer eller reservedele, der er relateret til det relaterede aktiv, er udløbet eller er blevet erstattet af andre varer eller reservedele.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Opret en ny varelinje i en aktivstykliste

Du kan oprette varelinjer for aktiver manuelt.

1. På siden **Aktivstykliste** skal du vælge **Ny**.
2. Vælg det **Aktiv**, du vil tilføje en varelinje for, i feltet aktiv.
3. Indtast et fortløbende linjenummer i feltet **Linjenummer**.
4. Indtast en ny startdato for varen i feltet **Gyldig**.
5. Hvis varen udløber, skal du angive en udløbsdato i feltet **Udløb**.
6. Vælg varen i feltet **Varenummer**. Navnet indtastes automatisk i feltet **Produktnavn**.
7. Angiv det forbrugte antal i feltet **Antal**. Feltet **Enhed** opdateres automatisk.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]