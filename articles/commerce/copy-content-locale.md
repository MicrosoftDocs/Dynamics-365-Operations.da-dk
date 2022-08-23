---
title: Kopiere indhold til en anden landestandard
description: Denne artikel beskriver, hvordan du kopierer eksisterende indhold til en anden landestandard i et websted i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269255"
---
# <a name="copy-content-to-another-locale"></a>Kopiere indhold til en anden landestandard

[!include[banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kopierer eksisterende indhold til en anden landestandard i et websted i Microsoft Dynamics 365 Commerce-webstedsgenerator.

Når du opretter indhold i Commerce-webstedsgenerator, er det altid knyttet til id for landestandard, f.eks. "en-us". Du kan kopiere individuelle sider og aktiver til en anden landekode inden for samme e-handelswebsted ved at skifte landekode, når du redigerer en indholdsvare og derefter opretter en ny variant for varen. I nogle tilfælde kan det være en god ide at duplikere alle indholdselementer i en eksisterende landekode til den nye landekode i nogle tilfælde, f.eks. når du starter en helt ny landekode. Hvis den nye landekode har samme basissprog som en af de eksisterende landekode, kan du bruge den eksisterende landekode som kildekode til kopieringshandlingen for landekode. (Landekoderne "en-us" og "en-au" bruger begge det engelske sprog). På denne måde kan du hjælpe dig med at reducere den tid, der kræves for at lokalisere indholdet i den nye landekode.

I følgende procedurer forklares det, hvordan du kan føje en ny landekode til en eksisterende kanal, kopiere alle indholdselementer fra en eksisterende landekode til en ny landekode og overvåge statussen for en kopieringshandling for landekode.

## <a name="add-a-new-locale"></a>Tilføj en ny landekode

Udfør følgende trin for at tilføje en landekode i Commerce-webstedsgenerator.

1. Naviger til dit websted i webstedsgeneratoren.
1. I venstre navigationsrude skal du vælge **Webstedsindstillinger** og derefter **Kanaler**.
1. Vælg den **Kanal**, vælg den kanal for at tilføje den nye landekode.
1. Vælg **Tilføj landekode** i den kanaldialogboks, der vises til højre.
1. Vælg en landekode i feltet **Landekode, der skal understøttes** i dialogboksen **Tilføj landekode**.
1. Bekræft, at **domæneværdien** er korrekt.
1. Angiv en entydig URL-sti under **Sti** (f.eks. **en-us** eller **engelsk-us**).
1. Vælg **OK**.
1. Luk derefter kanaldialogboksen.
1. Under **Kanal** skal du bekræfte, at den nye landekode vises ved siden af den korrekte kanal.
1. Vælg **Gem og udgiv**.

> [!NOTE]
> Før den nye landekode kan konfigureres i Site Builder, skal den føjes til den tilknyttede online-butikskanal i Commerce Headquarters.

## <a name="copy-all-content-items-to-a-new-locale"></a>Kopiere alle indholdselementer til en ny landekode

Udfør følgende trin for at kopiere indholdselementer til en ny landekode i Commerce-webstedsgenerator.

1. Naviger til dit websted i webstedsgeneratoren.
1. I venstre navigationsrude skal du vælge **Webstedsindstillinger** og derefter **Kanaler**.
1. Vælg **Opret landekopi fra** på kommandolinjen.
1. I dialogboksen **Opret landekopi**, der vises til højre, skal du under **Kildewebsted** bekræfte, at den korrekte lokation er valgt.
1. Vælg kildekanalen i feltet **Kildekanal**.
1. Vælg samme kildekanal i feltet **Destinationskanal**.
1. Vælg kildelandestandard i feltet **Kildelandestandard**.
1. Vælg den nye landestandard i feltet **Destinationsstandard**.
1. Vælg **Kopier landestandard**. En besked bekræfter, at kopieringshandlingen for landestandarden er startet.

> [!NOTE]
> Du kan også kopiere indhold mellem forskellige kanaler.

## <a name="monitor-the-status-of-the-locale-copy"></a>Overvåge status for landestandarden

Hvis du vil overvåge status for landestanden, skal du følge disse trin.

1. Naviger til dit websted i webstedsgeneratoren.
1. I venstre navigationsrude skal du vælge **Websteds-indstillinger** og derefter **Jobs**.
1. Vælg det job, der skal overvåges, under **Aktuelle jobs**. Jobdetaljer vises i den dialogboks, der vises til højre.
