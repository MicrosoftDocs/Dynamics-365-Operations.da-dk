---
title: Angive forskellige dimensioner for pakning og lagring
description: I dette emne vises, hvordan du kan angive, hvilken proces (pakning, lagring eller indlejret emballage) hver enkelt dimension bruges til.
author: mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e8ce576f21f1f5ea5f3acb7d43bbe68826e6f39
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580066"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Angive forskellige dimensioner for pakning og lagring

[!include [banner](../../includes/banner.md)]

Nogle varer er pakket eller lagret på en sådan måde, at du kan få brug for at spore fysiske dimensioner forskelligt for hver af flere forskellige processer. Funktionen *Emballageproduktdimensioner* gør det muligt at konfigurere en eller flere typer dimensioner for hvert produkt. Hver dimensionstype indeholder et sæt fysiske målinger (vægt, bredde, dybde og højde) og fastlægger den proces, hvor disse fysiske målingsværdier gælder. Når denne funktion er aktiveret, understøtter systemet følgende dimensionstyper:

- *Lagring* – Lagringsdimensioner bruges sammen med lokationsmængder til at bestemme, hvor mange af hver vare der kan opbevares på forskellige lagersteder.
- *Emballage* – Pakkedimensioner bruges under containerisering og den manuelle pakningsproces til at bestemme, hvor mange af hver vare der kan være i forskellige containertyper.
- *Indlejret emballage* – Indlejrede emballagedimensioner bruges, når pakkeprocessen indeholder flere niveauer.

*Lagringsdimensioner* understøttes også, selvom funktionen *Emballageproduktdimensioner* ikke er aktiveret. Du kan konfigurere disse ved hjælp af siden **Fysisk dimension** i Supply Chain Management. Disse dimensioner bruges af alle processer, hvor dimensionerne for pakning og indlejret emballage ikke er angivet.

Dimensioner for *Emballage* og *indlejret emballage* konfigureres ved hjælp af siden **Fysiske produktdimensioner**, som tilføjes, når du aktiverer funktionen *Emballageproduktdimensioner*.
Dette emne indeholder et eksempel på, hvordan denne funktion bruges.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Aktivere funktionen Emballageproduktdimensioner

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Emballageproduktdimensioner*

## <a name="example-scenario"></a>Eksempelscenario

### <a name="set-up-the-scenario"></a>Konfigurere scenariet

Før du kan køre eksempelscenariet, skal du forberede systemet som beskrevet i dette afsnit.

#### <a name="enable-demo-data"></a>Aktivere demodata

Hvis du vil arbejde gennem dette scenarie ved hjælp af de demoposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed *USMF*, før du starter.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Føje en ny fysisk dimension til et produkt

Tilføj en ny fysisk dimension for et produkt på følgende måde:

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg produktet med **varenummeret** *A0001*.
1. I handlingsruden skal du åbne fanen **Styr lager** og vælge **Fysiske produktdimensioner** i gruppen **Lagersted**.
1. Siden **Fysiske produktdimensioner** åbnes. Gå til handlingsruden, og vælg **Ny** for at føje en ny dimension til gitteret med følgende indstillinger:
    - **Fysisk dimensionstype** - *Emballage*
    - **Fysisk enhed** - *stk.*
    - **Vægt** - *4*
    - **Vægtenhed** - *kg*
    - **Dybde** - *3*
    - **Højde** - *4*
    - **Bredde** - *3*
    - **Længde** - *cm*
    - **Volumenenhed** - *cm3*

Feltet **Volumen** beregnes automatisk ud fra indstillingerne for **Dybde**, **Højde** og **Bredde**.

#### <a name="create-a-new-container-type"></a>Oprette en ny containertype

Gå til **Lokationsstyring \> Opsætning \> Containere \> Containertyper**, og opret en ny post med følgende indstillinger:

- **Containertypekode** - *Lav kasse*
- **Beskrivelse** - *Lav kasse*
- **Maksimal nettovægt** - *50*
- **Volumen** - *144*
- **Længde** - *6*
- **Bredde** - *6*
- **Højde** - *4*

#### <a name="create-a-container-group"></a>Oprette en containergruppe

Gå til **Lokationsstyring \> Opsætning \> Containere \> Containergrupper**, og opret en ny post med følgende indstillinger:

- **Containergruppe-id** - *Lav kasse*
- **Beskrivelse** - *Lav kasse*

Føj en ny linje til sektionen **Detaljer**. Angiv **Containertype** til *Lav kasse*.

#### <a name="set-up-a-container-build-template"></a>Konfigurere en containerbuildskabelon

Gå til **Lokationsstyring \> Konfiguration \> Containere \> Skabeloner til containerbygning**, og vælg **Kasser**. Skift **Containergruppe-id** til *Lav kasse*.

### <a name="run-the-scenario"></a>Køre scenariet

Når du har forberedt systemet som beskrevet i forrige afsnit, er du klar til at køre scenariet som beskrevet i næste afsnit.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Oprette en salgsordre og oprette en forsendelse

I denne proces opretter du en forsendelse, der er baseret på varens *emballagedimensioner*, for hvilken højden er mindre end 3.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *63*

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Den skal omfatte en ny tom linje i gitteret i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** *A0001*
    - **Antal:** *5*

1. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.
1. Luk siden.
1. I handlingsruden skal du åbne fanen **Lagersted** og vælge **Frigiv til lagersted** for at oprette lagerstedet.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Lagersted \> Forsendelsesoplysninger**.
1. Åbn fanen **Transport** i handlingsruden, og vælg **Vis containere**. Bekræft, at varen blev pakket containere i de to *Lav kasse*-containere.

#### <a name="place-an-item-into-storage"></a>Anbringe en vare til lagring

1. Åbn mobilenheden, log på lagersted 63, og gå til **Lager \> Reguler ind**.
1. Angiv **Loc** = *SHORT-01*. Lav en ny nummerplade med **Vare** = *A0001* og **Antal** = *1 stk.*.
1. Vælg **OK**. Du modtager fejlen "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions." Det skyldes, at produktets *lagringstypedimensioner* er større end de dimensioner, der er angivet i lokationsprofilen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]