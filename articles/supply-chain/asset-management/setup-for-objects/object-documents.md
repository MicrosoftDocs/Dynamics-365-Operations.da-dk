---
title: Aktivdokumenter
description: I dette emne beskrives aktivdokumenter i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b830d835d99122a8c0572481f4c229c37d97d0c
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653245"
---
# <a name="asset-documents"></a>Aktivdokumenter

[!include [banner](../../includes/banner.md)]

 

I dette emne beskrives aktivdokumenter i Styring af aktiver.

I Styring af aktiver kan du oprette dokumenter, så de automatisk relateres til f.eks. jobtyper, aktivproducenter, aktivtyper eller aktiver. Denne funktion er nyttig, når opdaterede dokumentversioner udgives. I så fald skal du bare placere det opdaterede dokument på den standardplacering, du bruger til dine Supply Chain Management-dokumenter, og knytte dokumentet til den aktivdokumentpost, du har oprettet. Du kan derefter få adgang til det opdaterede dokument fra menupunkterne **Alle aktiver**, **Aktive aktiver**, **Mine aktive aktiver**, **Alle arbejdsordrer** og **Aktive arbejdsordrejobs**. Processen til tilknytning af dokumenter til en aktivdokumentpost bruger det dokumenthåndteringssystem, der er angivet som standard.

**Eksempel 1:** et dokument, der er relateret til en jobtype, kan beskrive en procedure for den pågældende jobtype.

**Eksempel 2:** et dokument, der er relateret til en kombination af en aktivtype, en producent og en model, kan være standardmanualen for den valgte aktivproducentmodel.

## <a name="create-asset-document-relation"></a>Opret aktivdokumentrelation

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktivdokumenter**.
2. Vælg **Ny** for at oprette en aktivdokumentpost.
3. Afhængigt af det hvor detaljeret, du ønsker, at dokumentrelationen skal være, skal du foretage relevante valg i et eller flere af følgende felter: **Aktivtype**, **Producent**, **Model**, **Aktiv**, **Jobtypekategori**, **Jobtype**, **Jobtypevariant** og **Jobkrav**. De indstillinger, der er tilgængelige i felterne **Jobtypevariant** og **Jobkrav**, afhænger af dit valg i feltet **Jobtype**.

    > [!NOTE]
    > Når systemet søger efter dokumenter, der skal relateres til et aktiv eller en arbejdsordre, gennemgår Styring af aktiver alle aktivdokumentposter for at søge efter et potentielt match. Den kontrollerer altid den mest specifikke kombination først. Med andre ord kontrollerer Styring af aktiver først, om der er et match for feltet **Jobkrav**. Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Jobtypevariant**. Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Jobtype** osv. Som du kan se i layoutet for siden **Styring af aktiver**, betyder denne adfærd, at Styring af aktiver kontrollerer hver enkelt post fra højre mod venstre for et match for at finde den mest specifikke kombination. Flere dokumenter kan være relateret til et aktiv eller en arbejdsordre. Du kan redigere serviceniveauet på en reparationsanmodning eller en arbejdsordre efter behov.

4. Vælg **Vedhæftede filer**. Standardsiden **Dokumentoversigt** vises.
5. Konfigurer de dokumenter eller notater, der skal knyttes til aktivets dokumentpost. Når du har vedhæftet dokumenter, viser feltet **Vedhæftede filer** det antal dokumenter, der er relateret til posten.
