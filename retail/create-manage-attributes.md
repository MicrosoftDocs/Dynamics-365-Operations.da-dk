---
title: Oprette og administrere attributter
description: I denne artikel beskrives attributter i Microsoft Dynamics 365 for Operations. Med attributter kan du beskrive et produkt og dets egenskaber via brugerdefinerede felter.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Oprette og administrere attributter

I denne artikel beskrives attributter i Microsoft Dynamics 365 for Operations. Med attributter kan du beskrive et produkt og dets egenskaber via brugerdefinerede felter.

Med attributter kan du beskrive et produkt og dets egenskaber via brugerdefinerede felter. Du kan f.eks. angive produktets hukommelsesstørrelse og harddiskkapacitet og angive, om produktet er Energy star-kompatibel. Attributter kan være tilknyttet forskellige detailenheder, såsom produktkategorier og detailkanaler, og du kan angive standardværdier for dem. Produkter arver deres attributter og standardværdier for de attributter, når de er tilknyttet produktkategorier eller detailkanaler. Standardværdierne kan tilsidesættes på niveauet for hvert enkelt produkt i detailniveauet eller i et detailkataloget.

#### <a name="examples"></a>Eksempler

Kategori

Egenskab

Tilladte værdier

Standardværdi

Tv og video

Mærke

Alle gyldige værdier for **Mærke**

Ingen

Tv

Skærmstørrelse

**20"**-**80"**

Ingen

Lodret opløsning

**480i**, **720p**, **1080i** eller **1080p**

**1080p**

Skærmens opdateringshastighed

**60 Hz**, **120 Hz** eller **240 Hz**

**60 Hz**

HDMI-inputs

**0**-**10**

**3**

DVI-inputs

**0**-**10**

**1**

Sammensat inputs

**0**-**10**

**2**

Komponent-inputs

**0**-**10**

**1**

LCD

3D-klar

**Ja** eller **Nej**

**Ja**

3D-aktiveret

**Ja** eller **Nej**

**Nej**

Plasma

Driftstemperatur fra

**32**-**110** grader

**32**

Driftstemperatur til

**32**-**110** grader

**100**

Projection

Garanti på projektionsrør

**6**, **12** eller **18** måneder

**12**

\# på projektionsrør

**1**-**5**

**3**

## <a name="attribute-type"></a>Attributtype
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) Attributter er baseret på attributtyper. Attributtyper identificerer den type data, der kan angives for en bestemt attribut. Microsoft Dynamics 365 for Operations understøtter i øjeblikket følgende attributtyper:

-   **Valuta** – Denne attributtype understøtter valutaværdier. Den kan være afgrænset (dvs. den kan understøtte et interval), eller den kan være åben.
-   **DateTime** – Denne attributtype understøtter dato- og klokkeslætsværdier. Den kan være afgrænset (dvs. den kan understøtte et interval), eller den kan være åben.
-   **Decimal** – Denne attributtype understøtter numeriske værdier, der indeholder decimalpladser. Den understøtter også måleenheder. Den kan være afgrænset (dvs. den kan understøtte et interval), eller den kan være åben.
-   **Heltal** – Denne attributtype understøtter numeriske værdier. Den understøtter også måleenheder. Den kan være afgrænset (dvs. den kan understøtte et interval), eller den kan være åben.
-   **Tekst** – Denne attributtype understøtter tekstværdier. Den understøtter også et foruddefineret sæt af mulige værdier (fasttekst).
-   **Boolesk** – Denne attributtype understøtter binære værdier (**sandt**/**falsk**).
-   **Reference**.

## <a name="attribute"></a>Egenskab
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) Ud over navn, brugervenligt navn, beskrivelse og hjælpetekst kan en eller flere af følgende type oplysninger hentes for en attribut:

-   Standardværdi
-   Attribut-metadata, f.eks metadata, der angiver, om attributten kan søges, raffineres eller sorteres

## <a name="attribute-group"></a>Egenskabsgruppe
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Når attributter er blevet defineret, kan de grupperes i attributgrupper. Attributgrupper indeholder grupperinger af individuelle attributter og kan tildeles detailkategorier eller detailkanaler.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Tildele attributgrupper til detailkategorier
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) En eller flere attributgrupper kan knyttes til kategorinoder i detailproduktets kategorihierarki. Når produkter er kategoriseret, arver produkterne de attributter, der indgår i attributgrupper.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Tildele attributgrupper til detailbutikker
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) En eller flere attributgrupper kan knyttes til en eller flere detailbutikker i hierarkiet for detailbutikker. Når produkter er forbedret for specifikke detailbutikker, arver produkterne de attributter, der indgår i attributgrupper.

## <a name="overriding-attribute-values"></a>Tilsidesætte attributværdier
### <a name="at-the-product-level"></a>På produktniveau

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) Standardværdierne for attributter kan tilsidesættes på produktniveau (dvs. for individuelle produkter).

### <a name="in-a-retail-catalog"></a>I et detailkatalog

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) Standardværdierne for attributter kan tilsidesættes for individuelle produkter i specifikke kataloger, der er målrettet specifikke detailkanaler.

### <a name="at-the-retail-channel-level"></a>På detailkanalniveau

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) Standardværdierne for attributter kan tilsidesættes for individuelle produkter i specifikke kataloger, der er målrettet specifikke detailkanaler.


