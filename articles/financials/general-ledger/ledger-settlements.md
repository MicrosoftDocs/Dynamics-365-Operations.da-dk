---
title: Finansudligninger
description: I dette emne beskrives, hvordan du kan bruge siden Finansudligninger til at udligne finansposteringer og tilbageføre udligninger.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b02a1a066913c9959e9a55e78789e5ff1a175c56
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "308477"
---
# <a name="ledger-settlements"></a>Finansudligninger

[!include [banner](../includes/banner.md)]

Med Finansudligninger kan du sammenholde debet- og kreditposteringer i finansmodulet og markere dem som udlignet. På denne måde kan du sikre dig, at relaterede posteringer er blevet afstemt. Du kan også tilbageføre udligninger, hvis de er foretaget ved en fejltagelse.

## <a name="enable-advanced-ledger-settlements"></a>Aktivere avancerede finansudligninger

Siden til avancerede finansudligninger indeholder flere funktioner til filtrering og udvælgelse af posteringer. Du kan aktivere siden for avancerede finansudligninger ved at følge disse trin.

1. Vælg **Finans** \> **Opsætning Finans** \> **Finansparametre**. 
2. Under fanen **Finansudligninger** skal du vælge **Ja** i indstillingen **Avanceret finansudligning** for at aktivere funktionen Avanceret finansudligning. Siden for avancerede **Finansudligninger** bruges, når du vælger **Finansudligninger** i **Periodiske opgaver**. 
3. Du skal angive listen over konti, der skal bruges til finansudligninger, for hver kontoplan. Denne liste bruges til at filtrere listen over transaktioner, der vises på siden **Finansudligninger**. På listen **Kontoplaner** skal du vælge en kontoplan og derefter vælge **Ny** for at føje nye konti til listen.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Udligne posteringer ved hjælp af siden Avancerede finansudligninger

Du kan udligne finanstransaktionerne ved at følge disse trin.

1. Vælg **Finans** \> **Periodiske opgaver** \> **Finansudligninger**.
2. Angiv filtrene øverst på siden:

    - Vælg et datointerval, eller vælg **Datointervalkode** for automatisk at fylde i datointervallet.
    - Rediger posteringslaget efter behov.
    - For at få vist finanskontoen og dimensionerne hver for sig, skal du vælge et økonomisk dimensionssæt.

3. Vælg **Vis posteringer** for at få vist alle de posteringer, der svarer til de filtre, du har angivet, og listen over konti, du angav, da du konfigurerede kontoplanen i det forrige afsnit. Hvis du ændrer nogen af filtrene eller dimensionssættene, skal du vælge **Vis posteringer** igen.
4. Vælg en eller flere linjer, som du overvejer til udligning. Værdien i feltet **Valgt beløb** øverst på siden forøges eller formindskes med det samlede beløb på de linjer, du har valgt.
5. Når du er færdig med at vælge posteringer, skal du vælge **Markér valgte**. Der vises en markering i kolonnen **Markeret** for hver postering, du har valgt. Værdien i feltet **Markeret beløb** over gitteret forøges eller formindskes desuden med det samlede beløb på de linjer, du har markeret.
6. Når værdien i **Markeret beløb** er **0** (nul), skal du vælge **Udlign markerede posteringer**. Status for de markerede posteringer opdateres til **Udlignet**.

## <a name="make-transactions-easier-to-find"></a>Gøre posteringer nemmere at finde

Siden **Finansudligninger** indeholder funktioner, der gør det nemmere at få vist de posteringer, du skal bruge til udligning.

- Knappen **Fjern markering af valgte** rydder feltet **Markeret** for alle linjer, der er valgt.
- Filteret **Markeret** kan du bruge til at filtrere posteringer afhængigt af, om feltet **Markeret** er valgt eller ryddet for dem.
- Med filteret **Status** kan du filtrere posteringer på baggrund af, om deres status er **Udlignet** eller **Ikke udlignet**.
- Med knappen **Sortér efter absolut beløb** kan du sortere beløbene efter absolut værdi, så du kan gruppere debiteringer og krediteringer, der har samme beløb.

## <a name="reverse-a-settlement"></a>Tilbageføre en udligning

Du kan tilbageføre en udligning, der er foretaget ved en fejl.

1. Følg trin 1 til 3 i afsnittet "Udligne posteringer ved hjælp af siden Avancerede finansudligninger" for at få vist de posteringer, du søger efter.
2. Vælg **Udlignet** i filteret **Status**.
3. Vælg en eller flere linjer, som du overvejer at tilbageføre. Værdien i feltet **Valgt beløb** øverst på siden forøges eller formindskes med det samlede beløb på de linjer, du har valgt.
4. Når du er færdig med at vælge posteringer, skal du vælge **Markér valgte**. Der vises en markering i kolonnen **Markeret** for hver postering, du har valgt. Værdien i feltet **Markeret beløb** øverst på siden forøges eller formindskes desuden med det samlede beløb på de linjer, du har markeret.
5. Når værdien i **Markeret beløb** er **0** (nul), skal du vælge **Tilbagefør markerede posteringer**. Status for de markerede posteringer opdateres til **Ikke udlignet**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Opdater listen over konti, der er medtaget på listen over posteringer

Vælg **Finansudligningskonti** for at åbne en dialogboks, hvor du kan redigere de konti, der er medtaget på listen over posteringer. Vælg **Ny** for at føje nye konti til listen. Denne liste bruges til at filtrere listen over transaktioner, der vises på siden **Finansudligninger**.
