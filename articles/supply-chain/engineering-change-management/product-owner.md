---
title: Produktejere
description: Denne artikel indeholder oplysninger om produktejere. En produktejer er en gruppe af brugere, der er ansvarlig for bestemte produkter. Det er kun medlemmer af gruppen, der kan frigive disse produkter. Produktejeren kan også bruges i godkendelsesarbejdsprocessen.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5e09fdbbe14aa5a5ffbc5f07ae90b5d307a9e155
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907516"
---
# <a name="product-owners"></a>Produktejere

[!include [banner](../includes/banner.md)]

Produktejeren er en gruppe af brugere, der er ansvarlig for bestemte produkter. Når en produktejergruppe tildeles et produkt, er det kun medlemmerne af denne gruppe, der kan frigive produktet. Produktejeren kan også bruges i godkendelsesarbejdsprocessen i styring af tekniske ændringer.

Produktejere er globale indstillinger. Derfor er de tilgængelige for alle juridiske enheder.

## <a name="create-a-product-owner-group"></a>Oprette en produktejergruppe

Hvis du vil oprette en produktejergruppe og føje medlemmer til den, skal du følge disse trin.

1. Gå til **Teknisk ændringsstyring \> Konfiguration \> Produktejere**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv et sigende gruppenavn i feltet **Produktejer**.
4. Indtast en beskrivelse af gruppen i feltet **Navn**.
5. Tilføj de arbejdere, der skal være medlemmer af gruppen, i oversigtspanelet **Medlemmer**.

## <a name="assign-a-product-owner-to-a-product"></a>Tildele en produktejer til et produkt

Følg disse trin, hvis du vil tildele en produktejer til et produkt.

1. Åbn siden **Produktdetaljer** for det relevante produkt eller produktmasteren.
1. I oversigtspanelet **Generelt** skal du angive navnet på den relevante produktejergruppe i feltet **Produktejer**.

Mens en produktejer tildeles et produkt, kan kun medlemmerne af produktejergruppen redigere indstillingen for **Produktejer**.

Produktets ejer er også synlig på siden **Frigivne produkter**.

## <a name="product-owners-and-product-releases"></a>Produktejere og produktfrigivelser

Kun brugere fra et produkts produktejergruppe kan frigive produktet. Der er dog en undtagelse, når produktet er en underordnet vare, og dets overordnede er frigivet af ejeren af dets overordnede. Hvis produktet er en del af styklisten for et andet produkt, kontrollerer systemet ikke produktejeren af de enkelte varer på styklisten. Det kontrollerer kun produktejeren for den overordnede vare.

Produkt X tildeles f.eks. produktejergruppen *Design skabe*. Produkt X er også en del af styklisten for produkt Y, som er knyttet til produktejergruppen *Design højttalere*. Hvis en bruger fra *Design højttalere*-produktejergruppen frigiver produkt Y og dets stykliste, frigives produkt X sammen med produkt y.

## <a name="product-owners-and-approvals"></a>Produktejere og godkendelser

Da produktejere ved, om bestemte tekniske ændringer vil drage nytte af deres produkter, giver det ofte mening at inkludere dem som en del af godkendelsesprocessen i styring af tekniske ændringer. Du kan implementere denne fremgangsmåde ved at konfigurere produktejerne som deltagerudbydere i arbejdsprocesser, der bruges til styring af tekniske ændringer. Systemet tildeler derefter godkendelsesopgaver i arbejdsprocesserne baseret på produkterne i tekniske ændringsanmodninger og tekniske ændringsordrer. Yderligere oplysninger finder du i [Administrere ændringer af tekniske produkter](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]