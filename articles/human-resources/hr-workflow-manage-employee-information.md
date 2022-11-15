---
title: Bruge arbejdsprocesser til at administrere medarbejderoplysninger
description: Denne artikel forklarer, hvordan du kan bruge arbejdsgange til at administrere medarbejderoplysninger.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750728"
---
# <a name="use-workflows-to-manage-employee-information"></a>Bruge arbejdsprocesser til at administrere medarbejderoplysninger

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives, hvordan du kan bruge arbejdsgangsfunktionen i Human Resources til at administrere medarbejderoplysninger. Du kan f.eks. knytte en arbejdsgang til en stilling og konfigurere et godkendelsesforløb, der startes, når medarbejderne ændrer deres post.

Arbejdsgangsfunktionen til Human Resources indeholder adskillige arbejdsganger til administration af personaleaktiviteter. Desuden er der adgang til talrige indstillinger, så du kan ændre bestemte arbejdsgange og knytte dem til et rapporteringshierarki. Arbejdsgange er tilgængelige som en hjælp til at styre ændringer af flere standardtyper af medarbejderoplysninger. Du kan knytte en arbejdsgang til en stilling. Hvis medarbejderne derefter ændrer deres medarbejderpost, starter en arbejdsproces, der kræver godkendelse, før de nye oplysninger gemmes. Arbejdsgange er foruddefineret for følgende typer oplysninger for at hjælpe dig med effektivt at administrere ændringer og holde dine medarbejderdata nøjagtige:

-   Identifikationsnumre
-   Kurser
-   Uddannelser
-   Billede
-   Udlånte emner
-   Erhvervserfaring
-   Projekterfaring
-   Færdigheder
-   Tillidsposter
-   Handlinger for Human Resources
-   Kursustilmelding

Når medarbejdere ansættes, overføres eller fratræder, kan arbejdsgangen omfatter en revisionsproces. På denne måde kan et dokument blive evalueret, eller vilkårene for en handling kan defineres som en del af arbejdsgangen. Når evalueringsprocessen er fuldført, fuldføres dokumentet eller handlingen, og arbejdsgangen flyttes til et trin til endelig godkendelse.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Knyt en arbejdsgang til et stillingshierarki

Du kan knytte en arbejdsgang til ethvert stillingshierarki, du konfigurerer. Der bruges to hierarkityper til ruteplanlægning af arbejdsgange: **Ledelse** og **Konfigurerbar**.

- Et **ledelseshierarki** repræsenterer firmaets eller organisationens rapporteringsstruktur. Yderligere oplysninger om denne hierarkitype finder du i [Rapporterer til-stilling](hr-personnel-positions.md#reports-to-position).
- Et **Konfigurerbart** hierarki repræsenterer en matrix eller et brugerdefineret hierarki. Yderligere oplysninger om denne hierarkitype finder du i [Relationer](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Eksempel på ledelseshierarki

Du kan konfigurere en arbejdsgang, så når en medarbejder sender en indkøbsanmodning om en ny computer, dirigeres anmodningen til medarbejderens chef og souschef. Når du konfigurerer arbejdsgangstrinnet, skal du angive feltet **Tildelingstype** til **Hierarki**. Fanen **Hierarkitype** bliver derefter tilgængelig. I dette eksempel skal du vælge **Ledelseshierarki**.

### <a name="configurable-hierarchy-example"></a>Eksempel på konfigurerbart hierarki

Hvis en stilling er tilknyttet et matrixrapporteringshierarki, kan du konfigurere en arbejdsgang, der dirigerer udgifter for et bestemt projekt til projektlederen i stedet for medarbejderens chef. I dette tilfælde skal du angive feltet **Tildelingstype** til **Hierarki**. Under fanen **Hierarkitype** skal du vælge **Konfigurerbart hierarki**. Når arbejdsgangen er konfigureret, skal du vælge hierarkiet **Tilknyt** på siden **Opsætning af arbejdsgang** for at vælge det hierarki, der skal bruges til ruteplanlægning af arbejdsgangen.

> [!IMPORTANT]
> Når et dokument, en transaktion eller en masterpost sendes til arbejdsgangsgodkendelse, bruges afsenderens primære stilling til at bestemme, hvem dokumentet skal sendes til dernæst.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Hierarkiindstilling i arbejdsgangsparametre

1. Gå til **Ruteplanlægning i hierarki** på siden **Arbejdsgangsparametre**.
2. Som standard er indstillingen **Brug stillingshierarki** angivet til **Nej**. I dette tilfælde bruger arbejdsgangen arbejderens primære stilling, når der navigeres i hierarkiet. Angiv indstillingen til **Ja** for at få arbejdsgangen til at bruge stillingens overordnede, når der navigeres i hierarkiet.

### <a name="additional-example"></a>Ekstra eksempel 

Medarbejderen Grace Sturman har to stillinger: konsulent og underviser. Graces primære stilling er underviser. Når hun ikke underviser nye medarbejdere, er hun klar til konsulentarbejde. Via sin primære stilling rapporterer Grace til Claire, der er HR-direktør. Claire rapporterer til Charlie. I sin konsulentstilling har Grace flere overordnede relationer afhængigt af projektet.

Graces firma opretter ruteregler for arbejdsgange, der er baseret på et **Konfigurerbart** hierarki (matrix-/projektbaserede hierarkier). Dette hierarki bruger Graces konsulentstilling. Hvis indstillingen **Brug stillingshierarki** er angivet til **Nej**, når et dokument dirigeres til godkendelse hos Grace, vil arbejdsgangen se på hendes primære stilling (underviser) for at finde ud af, hvor dokumentet skal hen næste gang. I dette tilfælde vil det først blive distribueret til Claire og derefter til Charlie. Hvis indstillingen er angivet til **Ja**, og arbejdsgangen bruger et **Konfigurerbart** hierarki, vil arbejdsgangen se på Graces konsulentstilling og rapporteringsrelationen for at finde ud af, hvor dokumentet skal hen næste gang.

### <a name="configure-a-human-resources-workflow"></a>Konfigurer en arbejdsgang for Human Resources
Følg disse trin for at konfigurere en grundlæggende arbejdsgang, der startes, når medarbejdere anmoder om ændringer i deres personlige id.

1.  På siden **Arbejdsgange for Human Resources** skal du klikke på **ny**.
2.  På listen over tilgængelige arbejdsgange skal du vælge **Identifikationsnumre**.
3.  Vælg **Kør** for at starte arbejdsgangsdesigneren, og indtast derefter dit brugernavn og din adgangskode.
4.  Flyt elementet **Godkend identifikationsnummer** fra listen over arbejdsgangselementer til designerlærredet.
5.  Tilslut godkendelseselementet til **Start** og **Afslut**.
6.  Dobbeltklik på (eller dobbeltklik) **Godkend element**, vælg og hold nede (eller højreklik), og vælg derefter **Egenskaber**.
7.  Følg disse trin for at tilføje arbejdsgangsinstruktioner:

    1.  Vælg **Tildeling**, og vælg derefter **Hierarki** under tildelingstypen.
    2.  Under valget **Hierarki** skal du vælge **Konfigurerbart hierarki**.
    3.  Tilføj en stopbetingelse, og luk siden.

8.  Udfør eventuelle yderligere instruktioner.
9.  Vælg **Gem og luk**. Aktivér den nye arbejdsproces, når dialogboksen åbnes, og vælg **Gør den aktiv**.
10. Gå til **Human Resources** &gt; **Stillinger** &gt; **Stillingshierarkityper**.
11. Vælg **Matrix**.
12. Tilføj arbejdsgangen **Identifikationsnummer på arbejder** til listen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Få vist og administrer adresseændringer](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
