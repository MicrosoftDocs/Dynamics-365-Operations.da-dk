---
title: "Konfigurer parametre for personale på tværs af juridiske enheder"
description: "Du skal konfigurere delte parametre for poster, der deles på tværs af virksomheder, herunder stillingsposter. I denne artikel beskrives det, hvordan du kan bruge personaleparametre på tværs af juridiske enheder."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7f856946c90be5d21a822fdefc119ce61e3f411c
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a>Konfigurer parametre for personale på tværs af juridiske enheder

[!include[banner](includes/banner.md)]


Du skal konfigurere delte parametre for poster, der deles på tværs af virksomheder, herunder stillingsposter. I denne artikel beskrives det, hvordan du kan bruge personaleparametre på tværs af juridiske enheder.

Visse typer poster, f.eks. stillingsposter, deles på tværs af firmaer. Du skal konfigurere delte parametre for disse poster. Du kan f.eks. bruge siden **Delte parametre for personale** for at konfigurere personaleparametre på tværs af juridiske enheder. 

På siden **Delte parametre for personale** er parametrene grupperet i områder, baseret på deres funktionalitet. 

På fanen **Identifikation** skal du vælge de identifikationstyper, der repræsenterer de identifikationsnumre, der er angivet på siden. Før du kan angive identifikationsoplysninger om arbejderne, skal du konfigurere identifikationstyper. Oplysninger om CPR-nummer, nationalt id-nummer, ID for udlænding og personlige id-kode vedligeholdes på siden **Identifikationstype**. Hvis du vil definere en ny identifikationstype, eller gennemse listen over eksisterende typer, skal du klikke på **Personale** &gt; **Opsætning** &gt; **Identifikationstyper**. Du kan indtaste en simpel kode og beskrivelse. 

På fanen **Nummerserier** kan du vælge den nummerserie, der bruges til følgende poster: personalenummer, stilling, Id for brugeranmodning, I-9-dokument, ansøger, diskussion, Frynsegode-id og personalehandling (hvis denne posttype er aktiveret). Brug listesiden **Nummerserier**, hvis du vil vedligeholde nummerseriereferencer og -koder. Brug sidesøgefunktionen for at finde denne side. 

På fanen **Stillinger** skal du angive, om nye stillinger er tilgængelige for tildeling som standard:

-   **Altid** – Du kan tildele arbejdere til nye stillinger, når stillingerne oprettes. Når der oprettes stillinger, angives dato og klokkeslæt for **Tilgængelig for tildeling** under fanen **Generelt** på siden **Stilling** automatisk til oprettelsesdatoen og -klokkeslættet.
-   **Aldrig** – Du kan ikke tildele arbejdere til nye stillinger, når stillingerne oprettes. Hvis du vælger denne indstilling, skal du åbne siden **Stilling** for hver ny stilling, når den bliver tilgængelig, og derefter, på fanen **Generelt**, angive datoen **Tilgængelig for tildeling**for at aktivere arbejdertildeling.


<a name="see-also"></a>Se også
--------

[Oprette firmaspecifikke parametre for personale](set-up-company-specific-hr-parameters.md)




