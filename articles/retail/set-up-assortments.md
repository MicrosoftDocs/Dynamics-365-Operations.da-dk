---
title: "Opsætning af sortimenter"
description: I denne artikel beskrives det, hvad et sortiment er, og det forklares, hvordan du konfigurerer sortimenter i Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fc0aced939fd02ddf59295b8ba592ca78ca4f290
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-assortments"></a>Konfigurere udvalg

[!include[banner](includes/banner.md)]


I denne artikel beskrives det, hvad et sortiment er, og det forklares, hvordan du konfigurerer sortimenter i Microsoft Dynamics 365 for Retail.

Et sortiment er en samling af relaterede produkter, som du tildeler til en detailkanal, f.eks. en fysisk butik eller en onlinebutik. Du kan bruge udvalgt til at identificere de produkter, der er tilgængelige i hver butik. Et udvalg kan omfatte varekategorier. Alle de produkter, der er tildelt en bestemt kategori, er derfor inkluderet i sortimentet. Et udvalg kan også omfatte specifikke produkter og bestemte varianter af produkter. Ved at oprette et udvalg kan du tildele tusindvis af produkter til dine detailkanaler på det samme tidspunkt i enhver kombination, som din butikker kræver. Du kan oprette så mange produktudvalg, som du har brug for. Hvert produkt kan medtages i et eller flere udvalg, og hvert udvalg kan tildeles til en eller flere detailkanaler. Du kan f.eks. definere et sortiment der omfatter et grundlæggende sæt af produkter. Alle butikker modtager dette sortiment. Du kan derefter definere et andet sortiment, der kun indeholder stort sportsudstyr. Kun dine større butikker modtager dette sortiment. Følgende diagram viser, hvordan produkter kan tildeles til sortimenter, og hvordan disse sortimenter kan tildeles til detailkanaler. ![Produktsortimentrelationer](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Forudsætninger
Før du kan oprette et udvalg og tildele det til en detailkanal, skal du udføre følgende opgaver.

| Opgave                              | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurer en detailkanal.          | Detailkanaler repræsenterer en fysisk butik, en onlinebutik eller en onlinemarkedsplads. Du skal oprette mindst én detailkanal og konfigurere indstillingerne for butikken. Udvalg tildeles butikker for at identificere de produkter, der føres i en bestemt butik.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Opret et organisationshierarki. | Når du har oprettet detailkanaler til organisationen, skal du konfigurere et detailorganisationshierarkiet, der repræsenterer organisationsstrukturen i detailkanalerne. Et organisationshierarki kan bruges til udvalg, genbestilling og rapportering. Ved at føje dine detailkanaler til et organisationshierarki kan du tildele udvalg til grupper af butikker. I stedet for at tildele udvalg individuelt til hver butik kan du tildele udvalgene til organisationsnoden på højeste niveau. Hver gang der derefter føjes en ny detailkanal føjes til organisationsnoden på højeste niveau, arver denne detailkanal automatisk eventuelle udvalg, som blev tildelt til organisationsnoden på højeste niveau. Du kan kun tildele sortimenter til detailkanaler, der indgår i et organisationshierarki, der er tildelt formålet **Detailsortiment**. |
| Definer produkter.                  | Før du kan føje produkter til et sortiment, skal du tilføje dem i Microsoft Dynamics 365 for Retail. Du kan manuelt tilføje produkter, eller du kan importere dem fra en leverandør. Når du føjer produkter, skal du frigive dem til en juridisk enhed. Det er kun produkter, der er frigivet til en juridisk enhed, som kan gøres tilgængelige for detailkanaler. Produkter, der endnu ikke er frigivet til en juridisk enhed, kan føjes til et sortiment, og sortimentet kan godkendes. Det er dog først, når produkterne er frigivet til en juridisk enhed, at de kan gøres tilgængelige for detailkanalerne.                                                                                                                                                                                                                                                                                     |
| Konfigurer et kategorihierarki.      | Når du opretter dine detailprodukter, kan du gruppere og kategorisere dem ved hjælp af funktionen til kategorihierarkier. Du kan oprette ét kernehierarki for at gruppere og kategorisere alle de produkter, du distribuerer via dine detailkanaler. Du kan også oprette separate, supplerende kategorihierarkier for at gruppere eller kategorisere produkterne til særlige formål, såsom kampagner eller udvalg. Ved hjælp af kategorihierarkier kan du tildele alle produkter i en bestemt kategori til et sortiment. Produkter, der føjes til den kategori, der er inkluderet i udvalget, medtages automatisk i det pågældende udvalg. Næste gang detailsortimentsplanlægger køres derefter, bliver disse produkter tilgængelige for de detailkanaler, som udvalget er tildelt.                                            |

## <a name="setting-up-an-assortment"></a>Konfigurere et sortiment
Når du har fuldført forudsætningerne, kan du oprette et udvalg og tildele den til dine detailkanaler. Hvis du vil konfigurere et sortiment, skal du fuldføre følgende opgaver.

1.  Opret et nyt udvalg, eller kopiér et eksisterende udvalg.
2.  Vælg de detailkanaler eller grupper af detailkanaler på højeste niveau, som udvalgene gælder for.
3.  Føj produktkategorier, individuelle produkter eller produktvarianter til udvalget. Du kan inkludere alle produkter i en bestemt kategori, eller du kan udelukke markerede produkter fra en kategori, der er inkluderet i sortimentet.
4.  Udgiv udvalget. Detailsortimentsplanlæggeren kører automatisk, når du udgiver et udvalg. Denne proces opretter listen over produkter. Når denne proces er fuldført, bliver produkterne tilgængelige for de detailkanaler, som produktudvalget er tildelt. Hvis der foretages ændringer af et udvalg, der er udgivet, eller af detailkanaler, som udvalget er tildelt til, skal udvalget opdateres. Hvis du vil opdatere udvalg, når der er foretaget ændringer, kan du køre detailsortimentsplanlæggeren som et batchjob.





