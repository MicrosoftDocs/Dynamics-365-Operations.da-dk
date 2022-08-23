---
title: ER-funktionen NUMSEQVALUE
description: Denne artikel indeholder oplysninger om, hvordan funktionen NUMSEQVALUE til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 62255f0a47d3c67468cf2cf3922a1886c29c03d6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271547"
---
# <a name="numseqvalue-er-function"></a>ER-funktionen NUMSEQVALUE

[!include [banner](../includes/banner.md)]

Funktionen `NUMSEQVALUE` returnerer en *Streng*-værdi, som repræsenterer den nye genererede værdi for en nummerserie, der er baseret på den angivne nummerserie, omfang og område-ID. Område-ID'et er lig med den firmakode, der leveres af den kontekst, som det elektroniske rapporteringsformat (ER-format) køres under.

## <a name="syntax-1"></a>Syntaks 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Syntaks 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumenter

`number sequence code`: *Streng*

En tekstværdi, der repræsenterer koden for den nummerserie, som en ny værdi kræves i.

`number sequence record ID`: *Int64*

En *Int64*-værdi, der repræsenterer post-ID'et for en post i tabellen NumberSequenceTable, som indeholder definitionen af den nummerserie, som en ny værdi kræves i.

`scope type`: *Fasttekstværdi*

En fasttekstværdi for fastteksten **ERExpressionNumberSequenceScopeType**, der definerer omfanget af den nummerserie, som en ny værdi kræves i. De tilgængelige områdetyper er **Delte**, **Juridiske enheder** og **Firma**.

`scope ID`: *Streng*

En *Streng*-værdi, der identificerer området baseret på den angivne områdetype.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

For områdetypen **Delt** skal du angive en tom streng som område-ID'et.

For områdetyperne **Firma** og **Juridisk enhed** skal du angive firmakoden som område-ID. Hvis du angiver en tom streng som område-ID for disse områdetyper, bruges den aktuelle firmakode.

Når der bruges syntaks 1, anmodes nummerserien om områdetypen **Firma**, og firmakoden leveres af den kontekst, som ER-formatet køres under.

## <a name="example-1"></a>Eksempel 1

I dit ER-format definerer du datakilden **AskNumSeq** af typen *Brugerinputparameter*. Denne datakilde refererer til den udvidede datatype (EDT) **Beskrivelse**. Derefter skal du definere datakilden **NumSeq** af typen *Beregnet felt*. Denne datakilde indeholder udtrykket `NUMSEQVALUE (AskNumSeq)`. Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi for den nummerserie, der blev angivet ved kørslen, ved at indtaste dens kode i dialogboksen. Der anmodes om nummerserien for områdetypen **Firma**. Firmakoden leveres af den kontekst, som ER-formatet køres under.

## <a name="example-2"></a>Eksempel 2

De følgende datakilder er defineret i din modeltilknytning:

- Datakilden **LedgerParms** for typen *Tabel*. Denne datakilde refererer til tabellen LedgerParameters.
- Datakilden **NumSeq** for typen *Beregnet felt*. Denne datakilde indeholder udtrykket `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi af den nummerserie, der er konfigureret i Finans-parametrene for det firma, der leverer den kontekst, som ER-formatet køres under. Denne nummerserie identificerer entydigt kladder og fungerer som et batchnummer, der knytter posteringerne sammen.

## <a name="example-3"></a>Eksempel 3

De følgende datakilder er defineret i din modeltilknytning:

- Datakilden **enumScope** for Microsoft Dynamics 365 Finance *fasttekst*-typen. Denne datakilde refererer til fastteksten **ERExpressionNumberSequenceScopeType**.
- Datakilden **NumSeq** for typen *Beregnet felt*. Denne datakilde indeholder udtrykket `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi af den **Gene\_1**-nummerserie, der er konfigureret for det firma, der leverer den kontekst, som ER-formatet køres under.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
