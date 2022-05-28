---
title: Eksempler og logik til rapport over lagerværdi
description: Dette emne indeholder nogle eksempler på resultater, der vises i hver type lagerværdirapport. Lagerværdirapporter indeholder oplysninger om fysiske og økonomiske lagerantal og -beløb.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d594fc18a104c434a334a5b6d1d249330a6be9a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675313"
---
# <a name="inventory-value-report-examples-and-logic"></a>Eksempler og logik til rapport over lagerværdi

[!include [banner](../includes/banner.md)]

Lagerværdirapporter indeholder oplysninger om fysiske og økonomiske lagerantal og -beløb. Dette emne indeholder nogle eksempler på resultater, der vises i hver type lagerværdirapport.

Yderligere oplysninger om, hvordan du genererer og bruger de enkelte typer lagerværdirapporter, finder du i [Rapporter over lagerværdier](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Eksempeldata, der bruges i disse eksempler

Eksemplerne i dette emne er baseret på de eksempeldata fra lagertransaktioner, der er beskrevet i dette afsnit.

### <a name="storage-dimension-setup"></a>Konfiguration af lagringsdimension

Systemeksemplet indeholder følgende opsætning af lagringsdimensioner.

| Navn | Aktivt | Fysisk lager | Økonomisk lager |
|---|---|---|---|
| Lokation | Ja | Ja | Ja |
| Lagersted | Ja | Ja | Nej |

### <a name="inventory-model"></a>Lagermodel

I forbindelse med eksempelsystemet er lagermodellen for de frigivne produkter *FIFO*, og feltet **Kostpris** for lagermodellen er *Medtag fysisk værdi*.

### <a name="inventory-transactions"></a>Lagerbevægelser

Eksempelsystemet indeholder følgende lagertransaktioner for et frigivet produkt, der har varenummeret *B0001*.

| Reference | Websted | Lagersted | Tilgang | Emne | Fysisk dato | Økonomisk dato | Kvantitet | Kostbeløb | Fysisk kostbeløb |
|---|---|---|---|---|---|---|---|---|---|
| Indkøbsordre | 1 | 11 | Købt | | 15. marts | 15. marts | 10 | 1.000 | 1.000 |
| Indkøbsordre | 2 | 21 | Købt | | 15. marts | 15. marts | 10 | 2,000 | 2,000 |
| Indkøbsordre | 1 | 11 | Modtaget | | 15. april | | 5 | | 375 |
| Overførselsordre | 1 | 11 | | Solgt | Maj 2 | Maj 2 | -5 | -458,33 | -458,33 |
| Overførselsordre | 1 | 12 | Købt | | Maj 2 | Maj 2 | 5 | 458.33 | 458.33 |
| Salgsordre | 1 | 12 | | Solgt | Maj 3 | Maj 3 | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Konfiguration af lagerværdirapport

Eksempelsystemet indeholder en konfiguration af en lagerværdirapport med følgende indstillinger:

- **Interval:** *Bogføringsdato*
- **Lager:** *Ja*
- **Beregn gennemsnitlig enhedsomkostning:** *Ja*
- **Samlet antal og værdi:** *Ja*
- **Lokation, Vis:** *Valgt*
- **Ressource-id, Vis:** *Ja*
- **Niveau:** *Totaler*

## <a name="inventory-value-report-example-1"></a>Eksempel 1 på lagerværdirapport

Resultaterne vises i følgende tabel og illustrationer, når du bruger eksempeldata og rapportkonfiguration, der er beskrevet tidligere i dette emne.

| Ressourcetype | Ressource | Websted | Reference | Lager: økonomisk antal | Lager: økonomisk beløb | Lager: bogført fysisk antal | Lager: bogført fysisk beløb | Lager: antal | Lager: beløb | Gennemsnitlig enhedskostpris |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiale | B0001 | 1 | Slutsaldo | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Materiale | B0001 | 2 | Slutsaldo | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standardrapporten Lagerværdi til eksempel 1

I følgende illustration vises standardrapporten **Lagerværdi** til eksempel 1. (Vælg illustrationen for at åbne en større version.)

[![Rapporten Lagerværdi til eksempel 1.](media/inventory-value-report-ex1-small.png "Rapporten Lagerværdi til eksempel 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Rapporten Lagerværdirapportlager til eksempel 1

I følgende illustration vises rapporten **Lagerværdirapportlager** til eksempel 1. (Vælg illustrationen for at åbne en større version.)

[![Rapporten Lagerværdirapportlager til eksempel 1.](media/inventory-value-report-storage-ex1-small.png "Rapporten Lagerværdirapportlager til eksempel 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Eksempel 2 på lagerværdirapport

I nedenstående tabel og illustrationer vises resultaterne, når du bruger de eksempeldata, der er beskrevet tidligere i dette emne, men du ændrer værdien i feltet **Niveau** til *Posteringer* i rapportkonfigurationen, og du angiver feltet **Fra dato** til *15. marts*, når du kører rapporten.

| Ressourcetype | Ressource | Websted | Dato | Tal | Reference | Lager: økonomisk antal | Lager: økonomisk beløb | Lager: bogført fysisk antal | Lager: bogført fysisk beløb | Lager: antal | Lager: beløb |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiale | B0001 | 1 | 3/15/2021 | 00000126 | Indkøbsordre | 0,00 | 0,00 | 10.00 | 1,000.00 | **10.00** | **1,000.00** |
| Materiale | B0001 | 1 | 3/15/2021 | 00000126 | Indkøbsordre | 10.00 | 1,000.00 | -10,00 | -1.000,00 | **0.00** | **0.00** |
| Materiale | B0001 | 1 | 4/15/2021 | 00000128 | Indkøbsordre | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Materiale | B0001 | 1 | 5/2/2021 | 000003 | Forsendelse af flytteordre | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Materiale | B0001 | 1 | 5/2/2021 | 000003 | Modtagelse af flytteordre | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiale | B0001 | 1 | 5/3/2021 | 000835 | Salgsordre | 0,00 | 0,00 | -1,00 | -91,67 | **-1.00** | **-91.67** |
| Materiale | B0001 | 1 | 5/3/2021 | 000835 | Salgsordre | -1,00 | -91,67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Materiale | B0001 | 2 | 3/15/2021 | 00000127 | Indkøbsordre | 0,00 | 0,00 | 10.00 | 2,000.00 | **10.00** | **2,000.00** |
| Materiale | B0001 | 2 | 3/15/2021 | 00000127 | Indkøbsordre | 10.00 | 2,000.00 | -10,00 | -2.000,00 | **0.00** | **0.00** |
| Materiale | B0001 | 2 | 5/2/2021 | 000003 | Forsendelse af flytteordre | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiale | B0001 | 2 | 5/2/2021 | 000003 | Modtagelse af flytteordre | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Standardrapporten Lagerværdi til eksempel 2

I følgende illustration vises standardrapporten **Lagerværdi** til eksempel 2. (Vælg illustrationen for at åbne en større version.)

[![Rapporten Lagerværdi til eksempel 2.](media/inventory-value-report-ex2-small.png "Rapporten Lagerværdi til eksempel 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Rapporten Lagerværdirapportlager til eksempel 2

I følgende illustration vises rapporten **Lagerværdirapportlager** til eksempel 2. (Vælg illustrationen for at åbne en større version.)

[![Rapporten Lagerværdirapportlager til eksempel 2.](media/inventory-value-report-storage-ex2-small.png "Rapporten Lagerværdirapportlager til eksempel 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Eksempel 3 på lagerværdirapport

Det anbefales, at du kører rapporter over lagerværdier efter genberegning eller lagerlukning, så du har de posteringer og beløb, der påvirkes af genberegningen eller lagerlukningen.

Følgende undersektioner viser de lagerværdirapporter, der genereres, efter at du har lukket lageret, indtil den 30. maj.

### <a name="example-3-when-the-totals-level-is-used"></a>Eksempel 3, når niveauet Totaler bruges

Resultaterne vises i følgende tabel, når du bruger eksempeldata og rapportkonfiguration, der er beskrevet tidligere i dette emne. (I denne rapportkonfiguration er feltet **Niveau** angivet til *Totaler*).

| Ressourcetype | Ressource | Websted | Reference | Lager: økonomisk antal | Lager: økonomisk beløb | Lager: bogført fysisk antal | Lager: bogført fysisk beløb | Lager: antal | Lager: beløb | Gennemsnitlig enhedskostpris |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiale | B0001 | 1 | Slutsaldo | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Materiale | B0001 | 2 | Slutsaldo | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Eksempel 3, når niveauet Transaktioner bruges

Følgende tabel viser resultaterne, når du bruger de eksempeldata, der er beskrevet tidligere i dette emne, men du ændrer værdien i feltet **Niveau** til *Transaktioner* i rapportkonfigurationen.

| Ressourcetype | Ressource | Websted | Dato | Tal | Reference | Lager: økonomisk antal | Lager: økonomisk beløb | Lager: bogført fysisk antal | Lager: bogført fysisk beløb | Lager: antal | Lager: beløb |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiale | B0001 | 1 | 3/15/2021 | 00000126 | Indkøbsordre | 0,00 | 0,00 | 10.00 | 1,000.00 | 10.00 | 1,000.00 |
| Materiale | B0001 | 1 | 3/15/2021 | 00000126 | Indkøbsordre | 10.00 | 1,000.00 | -10,00 | -1.000,00 | 0,00 | 0,00 |
| Materiale | B0001 | 1 | 4/15/2021 | 00000128 | Indkøbsordre | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Materiale | B0001 | 1 | 5/2/2021 | 000003 | Forsendelse af flytteordre | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiale | B0001 | 1 | 5/2/2021 | 000003 | Modtagelse af flytteordre | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiale | B0001 | 1 | 5/3/2021 | 000835 | Salgsordre | 0,00 | 0,00 | -1,00 | -91,67 | -1,00 | -91,67 |
| Materiale | B0001 | 1 | 5/3/2021 | 000835 | Salgsordre | -1,00 | -91,67 | 1.00 | 91.67 | 0,00 | 0,00 |
| Materiale | B0001 | 1 | 5/31/2021 | 000835 | Salgsordre | 0,00 | -8,33 | 0,00 | 0,00 | 0,00 | -8,33 |
| Materiale | B0001 | 1 | 5/31/2021 | 000003 | Forsendelse af flytteordre | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
| Materiale | B0001 | 1 | 5/31/2021 | 000003 | Modtagelse af flytteordre | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiale | B0001 | 2 | 3/15/2021 | 00000127 | Indkøbsordre | 0,00 | 0,00 | 10.00 | 2,000.00 | 10.00 | 2,000.00 |
| Materiale | B0001 | 2 | 3/15/2021 | 00000127 | Indkøbsordre | 10.00 | 2,000.00 | -10,00 | -2.000,00 | 0,00 | 0,00 |
| Materiale | B0001 | 2 | 5/2/2021 | 000003 | Forsendelse af flytteordre | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiale | B0001 | 2 | 5/2/2021 | 000003 | Modtagelse af flytteordre | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiale | B0001 | 2 | 5/31/2021 | 000003 | Forsendelse af flytteordre | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiale | B0001 | 2 | 5/31/2021 | 000003 | Modtagelse af flytteordre | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
