---
title: Administrere ændringer i formler og deres stoffer
description: I dette emne beskrives, hvordan du udfører formelstyring og administrerer ændringer i behandling af produktionsmasterdata.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d25ddfc992d49c9a3c24d03cb0c71d68f7aa21fa
ms.sourcegitcommit: 908a85987b604a7782407da70fb70ef75c07989f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/19/2021
ms.locfileid: "6641098"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Administrere ændringer i formler og deres stoffer

[!include [banner](../includes/banner.md)]

Hvis du bruger funktionerne til procesproduktion i Microsoft Dynamics 365 Supply Chain Management, kan du også bruge de relaterede funktioner til formelstyring til at administrere følgende ændringer:

- **Formel- og planlægningsvarer:** Administrer ændringer af stoffer i formler og deres samprodukter og biprodukter.
- **Samprodukter og biprodukter:** Rediger mængder og andre oplysninger om samprodukter og biprodukter i en formel.
- **Fastvægtvarer:** Administrer ændringer af fastvægtvarer.

## <a name="turn-on-this-feature-in-your-system"></a>Aktivere denne funktion i systemet

Når du skal bruge denne funktion, skal du udføre følgende opgaver:

1. Aktivér funktionen *Styring af tekniske ændringer* og dens konfigurationsnøgle, som beskrevet i [Oversigt over styring af tekniske ændringer](product-engineering-overview.md). Som nævnt i dette emne skal du sørge for, at du også aktiverer licensnøglen til **Ændringsstyring for procesproduktion**, som er indlejret under licensnøglen til **Teknisk ændringsstyring**.
1. Slå funktionen *Administrere ændringer i formler og deres stoffer* til i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="feature-naming-conventions"></a>Navngivningskonventioner for funktioner

I brugergrænsefladen og dokumentationen til Supply Chain Management kaldes ændringsstyringsfunktionalitet typisk *teknisk ændringsstyring*, og de produkter, der skal administreres, kaldes typisk *tekniske produkter*. Selvom denne terminologi normalt ikke er forbundet med styring af formler til procesproduktion, bør du tænke på teknisk ændringsstyring som blot ændringsstyring, og du bør tænke på tekniske produkter som versionerede produkter.

## <a name="work-with-formula-change-management-features"></a>Arbejde med funktioner til administration af formelændringer

På følgende liste opsummeres, hvordan funktioner til teknisk ændringsstyring gælder for formelstyring. Den indeholder også links til flere oplysninger. Da styring af formelændringer udnytter funktionerne til styring af tekniske ændringer, bør du lære, hvordan teknisk ændringsstyring generelt fungerer, så du kan bruge det til at administrere dine formler og deres stoffer.

- **Centraliseret produktdataadministration** – Konfigurer en organisation, der gennem en administreret frigivelsesproces sikrer, at nøjagtige og relevante produktdata er tilgængelige for brugere i hele virksomheden. Yderligere oplysninger finder du i [Tekniske virksomheder og regler for ejerskab af data](engineering-org-data-ownership-rules.md).
- **Produktversioner** – Registrer ændringer af produkter via produktversioner, og styr produktet i alle faser af forsyningskæden. På denne måde kan du spore ændringerne i dine formuleringer. Du kan finde flere oplysninger under [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).
- **Administration af produktlivscyklus** – Administrer synligheden af produktdata i hele organisationen, og kontrollér tilgængeligheden af produktversioner i hver fase i forsyningskæden. Du har detaljeret kontrol over, hvornår en produktversion kan bruges i bestemte forretningsprocesser, og du kan oprette din egen livscyklus, så den passer til dine forretningsbehov. Du kan finde flere oplysninger i [Produktlivscyklustilstand og transaktioner](product-lifecycle-state-transactions.md).
- **Administration af formelændringer** – Brugere i hele organisationen kan anmode om ændringer af formler. Du kan bruge ændringsordrer til at vurdere og dokumentere virkningen af foreslåede ændringer. Tilføj arbejdsgange for at administrere ændringsprocessen og frigivelsen af nye versioner af produktet og dets formel. Yderligere oplysninger finder du i [Administrere ændringer af tekniske produkter](engineering-change-management.md).
- **Parathedskontrol** – Brug systemkontroller og brugervejledninger (spørgeskemaer og tjeklister) til at sikre, at alle nødvendige produktdata er angivet fuldt ud, før produktet frigives. Du kan finde flere oplysninger under [Produktparathed](product-readiness.md).
- **Udvidede funktioner til produktfrigivelse** – Frigiv fuldt definerede versioner af et produkt og dets formel fra en organisation (juridisk enhed) til andre juridiske enheder. Du kan også beslutte, om produktoplysningerne skal gennemses eller redigeres, før de frigives. Yderligere oplysninger finder du under [Frigive produktstrukturer](release-product-structure.md).

Bemærk, at de fleste af de emner, der linkes til på den foregående liste, indeholder eksempler, der er baseret på styklister. Formler fungerer dog på samme måde. Her er nogle yderligere begreber, som er nyttige at kende, når du bruger ændringsstyring (eller kun formelændringsstyring) til at administrere formler og styklister:

- For hver [tekniske produktkategori](engineering-versions-product-category.md) kan du angive produktionstypen (stykliste, formel eller planlægningsvare). Du kan også angive, om fangstvægtsupport er påkrævet for produkter, der bruger den pågældende kategori.
- Samprodukter og biprodukter er ikke tekniske produkter. De er derfor ikke versionerede. Hvis du skal ændre dem, skal du blot oprette et nyt produkt. Denne tilgang gør vedligeholdelse nemmere.
- Du kan administrere slutprodukter, der er styklister, og som har underordnede formelvarer. Funktionaliteten fungerer, når der anvendes en hvilken som helst kombination af styklister, som indeholder formler, og/eller formler, som indeholder styklister.
