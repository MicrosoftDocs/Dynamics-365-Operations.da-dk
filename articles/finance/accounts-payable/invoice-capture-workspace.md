---
title: Arbejdsområde for løsningen Invoice Capture
description: Denne artikel indeholder oplysninger om arbejdsområdet i løsningen Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691134"
---
# <a name="invoice-capture-solution-workspace"></a>Arbejdsområde for løsningen Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Side om side-fremviseren til løsningen Invoice Capture

Det har normalt været en tidskrævende proces med fejlrisiko at indtaste fakturaer i systemet, fordi kontorassistenter skal navigere i flere vedhæftede filer og vinduer for at indsamle de korrekte oplysninger. Ved hjælp af dokumentfremviseren side om side kan du forbedre oplevelsen af at arbejde med fakturaer ved at gøre processen lettere, mere effektiv og mere præcis.

Med dokumentfremviseren side om side kan brugere have det oprindelige dokument og fakturaen åbnet side om side i samme vindue. Fakturasiden er udfyldt med oplysninger, der kommer fra det oprindelige fakturadokument. Fremviseren bygger forbindelsen mellem felterne på fakturasiden og det oprindelige fakturadokument. Fremviseren hjælper også brugerne med at finde eventuelle fejl, der findes på fakturasiden.

### <a name="open-the-side-by-side-viewer"></a>Åbne side om side-fremviser

I Microsoft Dynamics 365 Finance kan du åbne side om side-fremviseren fra listen på oversigtssiden eller fra fakturalistesiden. Du kan også åbne den ved at dobbeltrykke (eller dobbeltklikke) på en post eller ved at vælge fakturanummeret.

### <a name="using-the-side-by-side-viewer"></a>Brug af side om side-fremviseren

#### <a name="manually-review-an-invoice"></a>Gennemgå en faktura manuelt

Et fakturadokument, der er importeret, kræver måske manuelt gennemsyn pga. fejl eller advarsler. Ved side om side-fremviseren viser dokumentoverskriften statussen **Importeret**, og den aktuelle version vil være **Oprindelig version**.

Hvis du vil starte gennemgangen af fakturaen, skal du vælge **Start gennemgang**. Alle felter kan redigeres. Feltet **Status** opdateres til **Til gennemgang**, og feltet **Aktuel version** opdateres til **Ændret version**.

#### <a name="view-and-work-with-messages"></a>Se og arbejde med meddelelser

Brugerne bør starte gennemsynsprocessen fra meddelelsesruden. Fejlmeddelelser angives med et rødt X, advarselsmeddelelser angives ved hjælp af en trekant, og oplysningsmeddelelser angives ved en cirkel. Meddelelser, der er relateret til konfidensscore, kan klassificeres som enten advarsler eller fejl, afhængigt af den grænse, der angives af variantgruppen. Du kan finde flere oplysninger i [Variantgrupper til løsningen Invoice Capture](invoice-capture-config-group.md).

Advarsler og fejlmeddelelser kan ignoreres fra meddelelsesruden, fakturahovedet eller fakturalinjerne. Når en meddelelse ignoreres, vises den ikke længere som en fejl eller en advarsel, og fakturaen mislykkes ikke i valideringen.

- Hvis du vil ignorere meddelelser fra meddelelsesruden, skal du vælge **Ignorer**. Hvis du vil nulstille en meddelelse, der er blevet ignoreret, skal du vælge **Ignorer** igen. Dens type ændres derefter fra fejl eller advarsel til oplysninger.
- Hvis du vil ignorere meddelelser fra fakturahovedet eller fakturalinjen, skal du vælge **Ignorer** i feltet. Meddelelsessymbolet forsvinder. Det vises dog igen, hvis meddelelsen nulstilles fra meddelelsesruden.

I forbindelse med meddelelser, der er knyttet til felter i fakturahovedet, flyttes markøren til det tilsvarende felt i hovedsektionen, når du vælger meddelelsen i meddelelsesruden.

#### <a name="proofread-and-edit-fields"></a>Læse og redigere felter

Hvis værdien af et felt læses fra den oprindelige faktura via OCR (Optical Character Recognition), vises der et symbol i feltet. Hvis du vælger symbolet, vil dokumentfremviseren zoome ind og fremhæve det sted, som feltværdien læses fra, for at hjælpe dig med at kontrollere fakturadataene.

Hvis du vil nulstille dokumentfremviseren til den oprindelige forstørrelse, skal du følge et af disse trin:

- Vælg det samme symbol, som du tidligere har valgt.
- Vælg knappen i øverste højre hjørne af dokumentfremviseren.

Rediger felterne efter behov. Redigeringer gemmes automatisk, når markøren forlader et felt. Et symbol til højre for et felt angiver, at feltet er blevet opdateret manuelt. Når siden er opdateret, fjernes symbolet.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Kontrollere en faktura for at hente opdaterede meddelelser

Når du redigerer et felt, opdateres feltværdien, men der genereres ikke nye valideringsmeddelelser. Du kan hente opdaterede valideringsmeddelelser ved at vælge **Tjek**. Meddelelserne i meddelelsesruden, i fakturahovedet og på fakturalinjerne opdateres.

#### <a name="complete-the-review"></a>Fuldføre gennemsynet

Hvis du vil fuldføre gennemsynet, skal du vælge **Fuldfør gennemsyn**. Fakturaerne valideres. Hvis der findes fejl, forbliver dokumentstatus **Til gennemgang**, og der vises en meddelelseslinje. Alle meddelelser i meddelelsesruden og på fakturahovedet og -linjerne opdateres automatisk, så de indeholder oplysninger om årsagerne til den mislykkede validering.

Når alle blokerende fejl er rettet, kan gennemsynet fuldføres. Dokumentstatus opdateres til **Gennemset**, og felterne kan ikke længere redigeres. Du kan genstarte gennemsynet ved at vælge **Start gennemgang** igen.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Generere en ventende kreditorfaktura i Finance

Hvis du vil sende fakturadokumentet til det tilknyttede Finance-miljø, skal du vælge **Generér**. Hvis generering af fakturaer mislykkes, vises der en fejlmeddelelse på en meddelelseslinje.

#### <a name="void-an-invoice"></a>Afvise en faktura

Hvis du vil afvise en faktura, skal du vælge **Afvist**. Afviste fakturaer kan ikke gennemses, og de vises ikke på listen **Fakturaer kræver manuelt gennemsyn**.

### <a name="validation-logic"></a>Valideringslogik

Visse nøglefelter i side om side-fremviseren findes ikke i de midlertidige fakturadata, men er obligatoriske for at generere ventende fakturaer i Finance. Disse felter er afledt af en kombination af de aktuelle midlertidige fakturadata og masterdata fra Finance.

De felter, der skal udledes, er **Juridisk enhed**, **Kreditorkonto** og **Varenummer**. De skal afledes i følgende rækkefølge. Hvis afledning af et felt mislykkes, stopper processen.

1. **Juridisk enhed** – Den juridiske enhed afledes først. Hvis der findes en aktiv tilknytningsregel for den juridiske enhed, afledes den juridiske enhed ud fra firmanavnet og firmaadressen.
2. **Kreditorkonto** – Derefter afledes kreditorkontoen på grundlag af en aktiv tilknytningsregel og en kombination af den afledte juridiske enhed og kreditorens navn og adresse.
3. **Varenummer** – Til sidst afledes varenavnet fra midlertidig lagring på grundlag af følgende tre typer oplysninger:

    - En konfigureret tilknytningsregel
    - Den afledte juridiske enhed
    - Den afledte kreditorkonto

Hvis du vil køre en validering, skal du vælge **Tjek** i side om side-fremviseren. Valideringen udfører i øjeblikket følgende kontroller:

- **Obligatorisk kontrol** – Denne kontrol validerer de obligatoriske felter for side om side-fremviseren. Brugere kan vælge, hvilke felter der skal være obligatoriske, på siden **Konfigurationsindstilling**.
- **Konfidensscore** – Brugerne kan angive advarselsgrænsen og fejlgrænsen for konfidensscoren. Denne kontrol fokuserer på konfidensscoren fra OCR, der ligger under disse grænser. Der vises fejl- eller advarselsmeddelelser på basis af valideringsresultatet.
- **Juridisk enhed** – Denne kontrol validerer, om en juridisk enhed er i Finance. Hvis den juridiske enhed ikke findes i Finance-miljøet, mislykkes valideringen.

Når side om side-fremviseren bruges første gang, og brugeren vælger **Tjek**, køres aflednings- og valideringsprocesserne. Hvis fakturaerne er nøjagtige, køres valideringsprocessen, når brugeren vælger **Fuldfør gennemsyn**. Den køres også, når brugeren vælger **Generér kreditorfaktura**.

Afledningsprocessen finder sted før valideringsprocessen, og alle advarsler eller fejl kommer fra valideringsprocessen. Advarslerne og fejlene logføres i Finance.
