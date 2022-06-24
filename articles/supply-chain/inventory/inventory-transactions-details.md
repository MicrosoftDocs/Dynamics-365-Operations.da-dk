---
title: Detaljer om lagertransaktion
description: Denne artikel indeholder en oversigt over siden Transaktionsdetaljer, der indeholder detaljer om en valgt lagertransaktion.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 55e29d5804f57cd86fb5ddac5d6c5576b7ea5f61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859381"
---
# <a name="inventory-transaction-details"></a>Detaljer om lagertransaktion

Du kan bruge siden **Transaktionsdetaljer** til at få vist detaljer om enhver valgt lagertransaktion.

## <a name="open-the-transaction-details-page"></a>Åbne siden Transaktionsdetaljer

Benyt følgende fremgangsmåde for at åbne siden **Transaktionsdetaljer**.

1. Gå til **Lagerstyring \> Forespørgsler og rapporter \> Transaktioner**.
1. Vælg den transaktion, du vil undersøge.
1. Vælg **Transaktionsoplysninger** i handlingsruden.

## <a name="fasttabs-overview"></a>Oversigt over oversigtspaneler

Siden **Transaktionsoplysninger** er opdelt i flere oversigtspaneler. Formålet med hvert oversigtspanel beskrives i følgende tabel.

| Oversigtspanel | Beskrivende tekst |
|---|---|
| Almindelig | I dette oversigtspanel vises grundlæggende oplysninger om den valgte lagertransaktion. Ud over de felter, der vises på siden **Lagertransaktioner**, indeholder det de yderligere felter, der beskrives senere i denne artikel. |
| Opdateringer | I dette oversigtspanel vises der oplysninger, der vedrører de fysiske, økonomiske og udligningsmæssige aspekter af den valgte lagertransaktion. Visse felter er måske tomme, afhængigt af transaktionens aktuelle status. Disse felter angives dog automatisk, når transaktioner bogføres. Ud over de felter, der vises på siden **Lagertransaktioner**, indeholder dette oversigtspanel yderligere felter, der beskrives senere i denne artikel. |
| Finanskonteringer | I dette oversigtspanel vises den bogføringstype og finanskonto, der bruges til den fysiske opdatering, den økonomiske opdatering, den fysiske omsætning, de fysiske gebyrer, de økonomiske indtægter og de økonomiske gebyrer, der er knyttet til den valgte lagertransaktion. |
| Referencer | I dette oversigtspanel vises yderligere oplysninger om den kildetransaktion, der har oprettet den valgte lagertransaktion. Disse oplysninger kan f.eks. omfatte detaljer fra indkøbsordren eller salgsordren. |
| Relaterede oplysninger | I dette oversigtspanel vises flere oplysninger om den valgte lagertransaktion. Disse felter er muligvis ikke angivet, hvis du ikke bruger visse funktioner som f.eks. indkøbskategorier eller projekter. |
| Økonomiske dimensioner - fysisk | I dette oversigtspanel vises de økonomiske dimensionsværdier, der blev brugt, da den fysiske opdatering blev bogført. Hvis den fysiske opdatering ikke er bogført, er felterne tomme. |
| Økonomiske dimensioner - økonomisk | I dette oversigtspanel vises de økonomiske dimensionsværdier, der blev brugt, da den økonomiske opdatering blev bogført. Hvis den økonomiske opdatering ikke er bogført, er felterne tomme. |
| Lagerdimensioner | I dette oversigtspanel vises de lagerdimensionsværdier, der er knyttet til den valgte lagertransaktion. Disse værdier omfatter websted, lagersted, størrelse, farve, konfiguration, lokation, batchnummer, serienummer lagerstatus, nummerplade og ejer. |

## <a name="fields-on-the-general-fasttab"></a>Felter i oversigtspanelet Generelt

Følgende tabel beskriver de felter i oversigtspanelet **Generelt**, der ikke også vises på siden **Lagertransaktioner**.

| Felt | Beskrivende tekst |
|---|---|
| Part | Navnet på den relevante part for den valgte lagertransaktion. En indkøbsordretransaktion viser f.eks. navnet på leverandøren på indkøbsordren, og navnet på kunden vises i en salgsordretransaktion. Dette felt er ikke tilgængeligt for alle typer lagertransaktioner. |
| Lagerreference | Hvis en anden lagertransaktion er relateret til den valgte lagertransaktion, er det typen af den anden transaktion. Hvis en købsordre er mærket i forhold til en salgsordre, vil feltet **Lagerreference** til indkøbsordretransaktionen være angivet til *Salgsordre*. Afmærkning foretages automatisk for ordrer i direkte levering og interne ordrer. Når du bruger afmærkning med andre efterkalkulationsmetoder end *standardomkostning* og *glidende gennemsnit*, opretter systemet udligninger og reguleringer af de nøjagtige transaktioner, der er afmærket. På denne måde kan du opnå "faktisk" efterkalkulation, der tilsidesætter logikken i FIFO-metoden (First In, First Out), LIFO (Last in, First out) eller vægtet gennemsnit. |
| Lagernummer | Den specifikke transaktion, der er relateret til den valgte lagertransaktion. Hvis en købsordre f.eks. er mærket i forhold til en salgsordre, vil feltet **Lagernummer** til indkøbsordretransaktionen være angivet til salgsordrenummeret. |
| Projekt-id | Hvis den valgte lagertransaktion er relateret til et projekt, angives dette felt til projektnummeret. |
| Parti-id | Det entydige parti-id, som systemet har tildelt den valgte lagertransaktion. |
| Referenceparti | Hvis en anden lagertransaktion er relateret til den valgte lagertransaktion, er parti-id'et til den anden transaktion. Hvis en købsordre f.eks. er mærket i forhold til en salgsordre, vil feltet **Referenceparti** til indkøbsordretransaktionen være værdien af **Parti-id** for salgsordrelinjens lagertransaktion. |
| Dimensionsnummer | Et entydigt id, der repræsenterer kombinationen af alle de lagerdimensionsværdier, der er tildelt den valgte lagertransaktion. |
| Værdi åben | En værdi, der angiver, om den valgte lagertransaktion er blevet udlignet af lagerlukningsprocessen. Hvis feltet er angivet til *Ja*, er transaktionen ikke udlignet. |
| Forventet dato | For tilgangstransaktioner er det den dato, hvor lagertilgang forventes at finde sted. Feltet kan f.eks. vise den forventede tilgangsdato i en lagerblokeringsordre eller leveringsdatoen på en indkøbsordrelinje. |
| Lagerdato | Dette felt angives, når der er udført en registreringstransaktion på tilgangsordren, før der er bogført en fysisk tilgang. |
| Ikke-økonomisk overførsel | En værdi, der angiver, om den valgte lagertransaktion er en ikke-økonomisk overførsel. En ikke-økonomisk overførsel finder sted, når en ændring i lagerdimensionerne ikke registreres økonomisk på siden **Varemodelgruppe**. |
| Overførselsparti-id | Hvis den valgte lagertransaktion er en ikke-økonomisk overførsel, angives dette felt til værdien af **Parti-id** for den anden lagertransaktion, som den valgte transaktion udlignes mod. |

## <a name="fields-on-the-updates-fasttab"></a>Felter i oversigtspanelet Opdateringer

Følgende tabel beskriver de felter i oversigtspanelet **Opdateringer**, der ikke også vises på siden **Lagertransaktioner**.

| Felt | Beskrivende tekst |
|---|---|
| Fysisk bilag | Bilagsnummeret fra finans, hvor den fysiske bogføring for den valgte lagertransaktion blev genereret. |
| Rute | Den rute, der er relateret til den valgte lagertransaktion. Dette felt er kun angivet for produktionspluklistetransaktioner, hvor styklisten eller formellinjen er relateret til en bestemt vare. |
| Følgeseddel | Det følgeseddelnummer, der blev angivet for en produktkvitteringstransaktion i en indkøbsordre. |
| Fysisk kostbeløb | Det beløb, der blev bogført i finans for den fysiske opdatering. For et standardomkostningsprodukt repræsenterer dette beløb standardomkostningen. I forbindelse med andre efterkalkulationsmetoder repræsenterer det det vægtede gennemsnit for produktet på bogføringstidspunktet. |
| Fysisk omsætning | Det beløb i udskudt indtægt, der blev bogført i finans for den fysiske opdatering. |
| Last-id | Hvis den aktuelle transaktion er relateret til en last i Transportstyring, viser dette felt det entydige nummer på den last, der inkluderede varen. |
| Fysisk bogført | En værdi, der angiver, om den valgte lagertransaktion er fysisk bogført. Hvis den aktuelle transaktion er bogført i Finans, er der også et fysisk bilag. |
| Økonomisk bogført | En værdi, der angiver, om den valgte lagertransaktion er økonomisk bogført. Hvis den aktuelle transaktion er bogført i Finans, er der også et økonomisk bilag. |
| Bogført fysisk omkostning | En værdi, der angiver, om de fysiske gebyrer, der er knyttet til den valgte lagertransaktion, er blevet bogført. |
| Bogført økonomisk omkostning | En værdi, der angiver, om de økonomisk gebyrer, der er knyttet til den valgte lagertransaktion, er blevet bogført. |
| Økonomisk bilag | Bilagsnummeret i finansmodulet, hvor den økonomiske bogføring blev genereret. |
| Faktura | Det fakturanummer, der blev genereret i forbindelse med f.eks. en indkøbsordre eller salgsordre. |
| Tilpasning | Det beløb, der blev reguleret i den valgte lagertransaktion fra lagerluknings- og reguleringsprocessen. |
| Drift, bogført beløb | Det beløb af den valgte lagertransaktion, der blev bogført i driftsopgørelsen. |
| Ikke-bogført faktura | Fakturanummeret på en relateret indkøbsordre, der vises på siden **Ventende kreditorfaktura**. |
| Økonomisk lukket | Den dato, hvor transaktionen blev fuldt udlignet. |
| Dækket fastvægtantal | Den fastvægt, der dækkes af udligningen. |
| Udlignet antal | Det antal, der er udlignet for den valgte lagertransaktion. |
| Udlignet beløb | Den værdi, der er udlignet for den valgte lagertransaktion. |
