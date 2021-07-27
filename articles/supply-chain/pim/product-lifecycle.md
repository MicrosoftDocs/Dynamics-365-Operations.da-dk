---
title: Oversigt over status for produktlivscyklus
description: En status for produktlivscyklus dokumenter livscyklusstatus for et frigivet produkt eller en produktvariant.
author: cvocph
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 0ebd482ad7dfde5393f4c03541a2ae1bca76ca7c
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/03/2021
ms.locfileid: "6340036"
---
# <a name="product-lifecycle-state-overview"></a>Oversigt over status for produktlivscyklus

[!include [banner](../includes/banner.md)]

En status for produktlivscyklus dokumenter livscyklusstatus for et frigivet produkt eller en produktvariant. Status for produktlivscyklus defineres af brugeren, typisk en produktchef eller produktmasterdatachef. Bestemte virksomhedsprocesser, f.eks. ved varedisponering, kan blive påvirket af en bestemt livscyklusstatus.

Et frigivet produkt eller en produktvariant kan knyttes til en status for produktlivscyklus, der dokumenterer, hvilken livscyklusstatus et bestemt produkt eller en produktvariant har. Du kan definere et ubegrænset antal produktlivscyklusstatusser ved at tildele et tilstandsnavn og en beskrivelse. Du kan vælge én livscyklusstatus som standardstatus for nye frigivne produkter. Frigivne produktvarianter nedarver deres status for produktlivscyklus fra deres frigivne produktmaster ved oprettelse. Når du ændrer livscyklusstatussen for en frigivet produktmaster, kan du vælge at opdatere alle eksisterende varianter, der har samme oprindelige status.  

## <a name="create-a-new-product-lifecycle-state"></a>Oprette en ny status for produktlivscyklus

- Når du vil oprette en ny status for produktlivscyklus, skal du se [Opret en ny status for produktlivscyklus](tasks/new-product-lifecycle-state.md).

- Når du vil oprette en standardstatus for produktlivscyklus, skal du se [Oprette en standardstatus for produktlivscyklus](tasks/default-product-lifecycle-state.md).

## <a name="associate-product-lifecycle-states-to-released-products"></a>Knytte status for produktlivscyklus til frigivne produkter  

Der er flere måder til at knytte en status for produktlivscyklus til frigivne produkter eller produktvarianter.

- Ved oprettelse af et nyt frigivet produkt tildeles **Status for produktlivscyklus**-standarden automatisk.
- Ved frigivelse af et produkt til en juridisk enhed tildeles **Status for produktlivscyklus**-standarden automatisk.
- Ved frigivelse af en produktvariant til en juridisk enhed tildeles den **Status for produktlivscyklus**, der er knyttet til den frigivne produktmaster i denne juridiske enhed, automatisk til den nye variant.

Du kan opdatere status for produktlivscyklus manuelt ved hjælp af:

- Listesiden **Frigivne produkter** eller **Detaljevisning**.
- Listesiden **Frigivne produktvarianter** eller **Detaljevisning**.
- Finde forældede produkter eller produktvarianter baseret på behov og tilknytte en livscyklusstatus.  

Hvis du vil have flere oplysninger:

- Hvis du vil knytte en status for produktlivscyklus til en frigivet produktmaster, skal du se [Tildele en status for produktlivscyklus til en frigivet produktmaster](tasks/product-lifecycle-state-released-product-master.md).

- Hvis du vil knytte en status for produktlivscyklus til et frigivet produkt, skal du se [Tildele en status for produktlivscyklus til et frigivet produkt](tasks/product-lifecycle-state-released-product.md).

## <a name="impact-on-master-planning"></a>Påvirkning af varedisponering

Statussen for produktlivscyklus har kun ét kontrolflag: **Er aktiv for planlægning**. Som standard er dette indstillet til **Ja** for alle oprettede statusser for produktlivscyklus, men det kan ændres til **Nej**. Når det er indstillet **Nej**, er de tilknyttede frigivne produkter eller frigivne produktvarianter:

- Udelukket fra varedisponering.
- Udelukket fra beregning af styklisteniveau.

Du kan finde detaljerede oplysninger om, hvordan du kan bruge statusser for produktlivscyklus til at udelukke produkter fra varedisponering og beregning af styklisteniveau, ved at se [Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering](tasks/exclude-products-master-planning.md)

> [!NOTE]
> Af hensyn til ydeevnen anbefales du at knytte alle forældede frigivne produkter eller produktvarianter, især når du arbejder med ikke-genanvendelige produktkonfigurationsvarianter, til en status for produktlivscyklus, der er deaktiveret for varedisponering.  

## <a name="default-migration-import-and-export"></a>Standardoverførsel, - import og -eksport

Statusser for produktlivscyklus understøttes af dataenheder, og livscyklusstatussen kan indstilles til en variabel status via enten den frigivne produktdataenhed eller den frigivne dataenhed.

## <a name="find-obsolete-products-and-products-variants"></a>Finde forældede produkter og produktvarianter

Du kan køre en simuleringsanalyse for at finde forældede frigivne produkter eller produktvarianter og derefter opdatere deres status for produktlivscyklus. For at finde forældede produkter skal du se [Finde forældede produktvarianter og tildele en status for produktlivscyklus](tasks/obsolete-product-variants.md). Dette emne viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter. Guiden viser også, hvordan du kan få vist resultaterne af simuleringen og vurdere, hvor mange produkter og produktvarianter der skal knyttes til en ny status for produktlivscyklus, når du kører opdateringen uden simulering.  

Hvis du kører analysen i en simuleringstilstand, vises de produkter og produktvarianter, der er identificeret som forældet, i en bestemt formular, hvor de nemt kan evalueres. Analysen søges efter posteringer og bestemte masterdata for at identificere produkter, der ikke er behov for i en variabel periode, og som ikke har nogen masterdata, der kan medføre behov. Nye frigivne produkter inden for en variabel periode kan udelukkes fra analysen. Når analysesimuleringen returnerer det forventede resultat, kan brugeren køre analysen og indstille en ny status for produktlivscyklus til alle produkter, der er angivet som forældede af analysen.  

> [!NOTE]
> Bemærk, at alle analyser og opdateringer skal udføre inden for den samme juridiske enhed.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Kriterier for valg og opdatering af frigivne produkter eller produktvarianter

Brug følgende kriterier til at vælge og opdatere frigivne produkter og produktvarianter:

- Statussen for produktlivscyklus for produktet eller produktvarianten skal være forskellig fra den nye ønskede status.
- Produktet eller produktvarianten blev oprettet for nogle dage siden baseret på antallet af dage, du angiver i valgdialogboksen.
- Der er ingen åbne produktionsordrer (= status < afsluttet) for produktet eller produktvarianten.
- Der er ingen åbne lagertransaktioner (= statusafgang ReservPhysical til QuotationIssue eller statustilgang Registreret til QuotationReceipt) for produktet eller produktvarianten.
- Der er ingen lagertransaktioner inden for de sidste dage for produktet eller produktvarianten.
- Der er ingen fremtidig behovs- eller forsyningsprognose for produktet eller produktvarianten.  
- Der er ikke angivet noget minimumlagerniveauet i varedisponering for produktet eller produktvarianten.
- Der er ingen aktiv kanban-regel for fast antal for produktet eller produktvarianten.  
- Der er ingen serviceordrelinje for produktet eller produktvarianten.
- Der er ingen aktive eller fremtidige salgs- eller købsaftalelinjer for produktet eller produktvarianten.
- Produktet eller produktvarianten bruges ikke i en stykliste, der er knyttet til en ikke-udløbet godkendt styklisteversion for et produkt eller variant, der er aktiv for planlægning.

## <a name="related-topics"></a>Relaterede emner

- [Oprette en ny status for produktlivscyklus](tasks/new-product-lifecycle-state.md)
- [Oprette en standardstatus for produktlivscyklus](tasks/default-product-lifecycle-state.md)
- [Tildele en produktlivscyklustilstand til en frigivet produktmaster](tasks/product-lifecycle-state-released-product-master.md)
- [Tildele en produktlivscyklustilstand til et frigivet produkt](tasks/product-lifecycle-state-released-product.md)
- [Find forældede produktvarianter og tildel en livscyklustilstand for et produkt](tasks/obsolete-product-variants.md)
- [Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]