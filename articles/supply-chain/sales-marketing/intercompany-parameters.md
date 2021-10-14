---
title: Interne parametre
description: Dette emne forklarer interne parametre
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 705efee84b255105ba39c603d23d2509e77b331a
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548172"
---
# <a name="intercompany-parameters"></a>Interne parametre

[!include [banner](../../includes/banner.md)]

I en intern organisation kan du oprette parametre, der bestemmer den måde, der handles mellem de forskellige juridiske enheder på. Disse parametre bestemmes ud fra de felter, du markerer. Du kan vælge mellem forskellige kombinationer med forskellige samhandelsmuligheder.

Følgende eksempler viser to eksempler, der beskriver scenarier for en interne organisationer, en med to niveauer og én med tre niveauer.

## <a name="example-1-two-level-intercompany-chain"></a>Eksempel 1: Intern kæde med to niveauer

Den interne organisation omfatter følgende juridiske enheder:

- Juridisk enhed A - Sælger til eksterne kunder, men har intet lager. Denne juridiske enhed køber fra Juridisk enhed B.
- Juridisk enhed B - Sælger udelukkende til Juridisk enhed A.

Begge juridiske enheder kan sælge og købe indbyrdes.

I dette eksempel er prisfastsættelsen for den oprindelige salgsordre, der sendes til den eksterne kunde, altid baseret på salgsprisen. Prisfastsættelsen for den interne salgsordre og den interne indkøbsordre styres af den interne salgs/overførselspris for den interne salgsordre i Juridisk enhed B.

Oplysningerne i ordrehovedet styres fra den oprindelige salgsordre til den eksterne kunde. Eventuelle ændringer i den interne salgsordre synkroniseres ikke til den oprindelige salgsordre.

Vælg **politikker for indkøbsordrer** på siden **Intern handel** for kreditorer i Juridisk enhed A. Marker følgende felter i feltgruppen **Oprindelig salgsordre (direkte levering)**:

- **Udskriv følgeseddel automatisk**
- **Bogfør faktura automatisk**
- **Udskriv faktura automatisk**

Marker følgende felter i feltgruppen **Intern købsordre (direkte levering)**:

- **Bogfør faktura automatisk**

Marker følgende felter i feltgruppen **Oprindelige salgsordrer <-> Intern købsordre**:

- **Kundeoplysninger**
- **RMA-nummer**

Marker følgende felter i feltgruppen **Intern købsordre <-> Intern salgsordre**:

- **Kundeoplysninger**
- **RMA-nummer**
- **Batchnummer**
- **Serienummer**

Vælg **politikker for salgsordrer** på siden **Intern handel** for kunder i Juridisk enhed B. Marker følgende felter i feltgruppen **Intern salgsordre (oprettelse)**:

- **Salgsordrenummerering** : **Firma + oprindeligt nummer**
- **Tillad samleopdatering af dokumenter for oprindelig kunde**

Marker følgende felter i feltgruppen **Intern salgsordrepriser**:

- **Pris- og rabatsøgning**
- **Tillad redigering af pris**
- **Tillad redigering af rabat**

Marker følgende felter i feltgruppen **Intern salgsordre \> Intern købsordre**:

- **Batchnummer**
- **Serienummer**

## <a name="example-2-three-level-intercompany-chain"></a>Eksempel 2: Intern kæde med tre niveauer

Den interne organisation omfatter følgende juridiske enheder:

- Juridisk enhed A – En juridisk salgsenhed, som sælger til eksterne kunder, og som køber fra Juridisk enhed B.
- Juridisk enhed B – En juridisk produktions- eller distributionsenhed, som ikke kan levere produkter, og som køber fra Juridisk enhed C.
- Juridisk enhed C – En juridisk produktions- eller distributionsenhed, som leverer produkter til Juridisk enhed B.

Den interne afregningspris mellem de juridiske enheder B og C stammer fra den sælgende juridiske enhed først i kæden. Den har også betydning for Juridisk enhed A, som sælger til eksterne kunder. Prisfastsættelsen på den oprindelige salgsordre til eksterne kunder er dog altid baseret på salgsprisen.

Prisfastsættelsen for alle interne salgsordrer og -købsordrer styres på den interne salgsordre. Det styres i starten af kæden. Derfor styrer Juridisk enhed C, som sælger til Juridisk enhed B, prisen. Prisfastsættelsen for den interne salgsordre er baseret på den interne salgs/overførselspris, der er angivet for Juridisk enhed C.

Oplysningerne i ordrehovedet styres fra den oprindelige salgsordre til den eksterne kunde. Eventuelle ændringer i de interne ordrer synkroniseres ikke til den oprindelige salgsordre.

Der skal vælges følgende parametre:

Vælg **politikker for indkøbsordrer** på siden **Intern handel** for kreditorer i Juridisk enhed A. Marker følgende felter i feltgruppen **Oprindelig salgsordre (direkte levering)**:

- **Udskriv følgeseddel automatisk**
- **Bogfør faktura automatisk**
- **Udskriv faktura automatisk**

Marker følgende felter i feltgruppen **Intern købsordre (direkte levering)**:

- **Bogfør faktura automatisk**

Marker følgende felter i feltgruppen **Oprindelige salgsordrer <-> Intern købsordre**:

- **Kundeoplysninger**
- **RMA-nummer**

Marker følgende felter i feltgruppen **Intern købsordre <-> Intern salgsordre**:

- **Kundeoplysninger**
- **RMA-nummer**
- **Batchnummer**
- **Serienummer**

Vælg **politikker for salgsordrer** på siden **Intern handel** for kunder i Juridisk enhed B. Marker følgende felter i feltgruppen **Intern salgsordre (oprettelse)**:

- **Salgsordrenummerering** : **Firma + oprindeligt nummer**
- **Tillad samleopdatering af dokumenter for oprindelig kunde**

Marker følgende felter i feltgruppen **Intern salgsordre \> Intern købsordre**:

- **Batchnummer**
- **Serienummer**

Marker følgende felter i feltgruppen **Intern kundefakturapostering**:

- **Enhedspris er lig med kostpris**
- **Start bogføring af oprindelig debitorfaktura**

Vælg **politikker for indkøbsordrer** på siden **Intern handel** for kreditorer i Juridisk enhed B. Marker følgende felter i feltgruppen **Oprindelig salgsordre (direkte levering)**:

- **Udskriv følgeseddel automatisk**
- **Bogfør faktura automatisk**
- **Udskriv faktura automatisk**

Marker følgende felter i feltgruppen **Intern købsordre (direkte levering)**:

- **Bogfør faktura automatisk**

Marker følgende felter i feltgruppen **Oprindelige salgsordrer <-> Intern købsordre**:

- **Kundeoplysninger**
- **RMA-nummer**
- **Pris og rabat**

Marker følgende felter i feltgruppen **Intern købsordre <-> Intern salgsordre**:

- **Kundeoplysninger**
- **RMA-nummer**
- **Batchnummer**
- **Serienummer**

Vælg **politikker for salgsordrer** på siden **Intern handel** for kunder i Juridisk enhed C. Marker følgende felter i feltgruppen **Intern salgsordre (oprettelse)**:

- **Salgsordrenummerering** : **Nummerseriekode**
- **Tillad samleopdatering af dokumenter for oprindelig kunde**

Marker følgende felter i feltgruppen **Intern salgsordrepriser**:

- **Pris- og rabatsøgning**

Marker følgende felter i feltgruppen **Intern kundefakturapostering**:

- **Enhedspris er lig med kostpris**
- **Start bogføring af oprindelig debitorfaktura**

Marker følgende felter i feltgruppen **Intern salgsordre <-> Intern købsordre**:

- **Batchnummer**
- **Serienummer**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
