---
title: Administrere rekrutteringsprocesser
description: I denne artikel beskrives et koncept, som rekrutteringsmedarbejdere kan bruge til at spore trinnene i en rekrutteringsproces, herunder arbejdet med at annoncere ledige stillinger og rekruttere ansøgere, spore oplysninger om ansøgeren og ansøgningen, interviewe ansøgere og vælge en eller flere kandidater til at udfylde de ledige stillinger i organisationen.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfdc1295e0b82672576acdf8e2756dbb36612f8b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510722"
---
# <a name="manage-recruiting-processes"></a>Administrere rekrutteringsprocesser

[!include [banner](../includes/banner.md)]

I dette emne beskrives et koncept, som rekrutteringsmedarbejdere kan bruge til at spore trinnene i en rekrutteringsproces, herunder arbejdet med at annoncere ledige stillinger og rekruttere ansøgere, spore oplysninger om ansøgeren og ansøgningen, interviewe ansøgere og vælge en eller flere kandidater til at udfylde de ledige stillinger i organisationen.

## <a name="overview"></a>Overblik

Rekrutteringsprojekter kan hjælpe dig med at organisere de trin, du skal udføre under udfyldning af ledige stillinger i en juridisk enhed. En ansøger er en person, der ansøger om ansættelse i din virksomhed. En ansøgning er en ansøgers udtryk for interesse i at blive ansat af en virksomhed og kan være knyttet til et rekrutteringsprojekt for at udtrykke interesse i en bestemt stilling. En enkelt ansøger kan have flere ansøgninger inden for samme juridiske enhed eller på tværs af flere firmaer i organisationen.

## <a name="recruitment-projects"></a>Rekrutteringsprojekter

Rekrutteringsprojekter gør det muligt for rekrutteringsmedarbejdere at spore status i forhold til at udfylde en eller flere ledige stillinger. Rekrutteringsprojektet identificerer afdeling og det job, som en eller flere stillinger er åbne for. Rekrutteringsprojekter kan også registrere følgende oplysninger om ledige stillinger:

- Antallet af ledige stillinger
- Den ansvarlige for ansættelsen og en alternativ kontakt for stillingen
- Den dato, da rekvisitionen blev godkendt
- Ansøgningsfristen
- Den anslåede startdato

Rekrutteringsprojektet indeholder den **jobannonce**, der blev brugt på **Medarbejderselvbetjeningen** for at annoncere for stillingen. For at vise stillingen til medarbejdere, skal rekrutteringsprojektet have en **jobannonce**, feltet **Vis på medarbejderselvbetjening** skal være angivet til Ja, **ansøgningsfristen** skal angives til en fremtidig dato, og rekrutteringsprojektet skal have en **projektstatus**, der er igangsat. Følgende tabel viser de forskellige rekrutteringsprojektstatusser og en beskrivelse af dem.

| Status    | Angiver, at...                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Planlagt | Rekrutteringsindsatsen er ved at blive klargjort. Rekruttering er endnu ikke startet for dette projekt. |
| Startet   | Ansøgninger accepteres nu for stillinger i dette projekt.                   |
| Udført  | Alle stillinger i dette projekt er blevet udfyldt.                                         |
| Annulleret  | Rekruttering er blevet annulleret for dette projekt.                                          |

Rekrutteringsmedarbejdere kan også registrere det **medie**, der bruges til at annoncere stillingen via eksterne medier samt holde styr på **udviklingen** i forhold til projektet eller ansøgninger.

## <a name="applicants"></a>Ansøgere

En ansøger er en person, der ansøger om et job i din virksomhed. Ansøgere deles mellem alle juridiske enheder i organisationen, hvilket giver dig en stor pulje af talent for at søge fra. Du kan angive kvalifikationer, referencer, tilpasningsanmodninger og personlige oplysninger for ansøgere. Når du opretter en ansøgningspost, oprettes en personpost for ansøgeren i det globale adressekartotek. Du kan bruge siden **Ansøger** til at opdatere følgende globale adressekartoteksoplysninger for personer, der er ansøgere:

- Adresseoplysninger
- Kontaktoplysninger
- Identifikationsoplysninger
- Navnedetaljer
- Personlige oplysninger

## <a name="applications"></a>Applikationer

Du kan registrere oplysninger fra modtagne jobansøgninger på siden **Ansøgning**. Ansøgningen er ansøgerens udtryk for interesse i et job, der er ledigt i din organisation. For at oprette en ansøgning, skal ansøgeren allerede findes som en ansøger eller en person i dit system.

Jobansøgninger, der sendes af ansøgere via internettet, er enten opfordrede ansøgninger, der er indsendt som svar på en stillingsannonce, eller uopfordrede ansøgninger. Opfordrede ansøgninger knyttes automatisk til det rekrutteringsprojekt, stillingsannoncen er oprettet fra. Uopfordrede ansøgninger knyttes til det rekrutteringsprojekt, der er angivet i området **Rekruttering** på siden **Personaleparametre**.

### <a name="application-status"></a>Ansøgningsstatus

Ansøgningsstatus angiver, hvor langt ansøgningen er nået i rekrutteringsforløbet. Følgende tabel viser de forskellige ansøgningsstatusser og en beskrivelse deraf.

| Status    | Angiver, at...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Modtaget  | Ansøgningen er modtaget.                                                             |
| Bekræftet | Der kan sendes en besked til ansøgeren om, at ansøgningen er modtaget.            |
| Samtale | Der kan sendes en invitation om en jobsamtale til ansøgeren.                                     |
| Afslag | Der kan sendes et afslag til ansøgeren.                                          |
| Annulleret  | Der kan sendes en bekræftelse på tilbagetrækning til ansøgeren. Denne status tildeles manuelt. |
| Ansat  | Der kan sendes et ansættelsestilbud til ansøgeren.                                         |

### <a name="correspondence-actions"></a>Korrespondanceaktioner

En **ansøgnings** korrespondanceaktion afgør, hvilken dokument- eller e-mailskabelon der bruges til at kommunikere med den ansøger, der har sendt ansøgningen. Du kan knytte **Ansøgningsbogmærker**, så du kan bruge værdier fra siderne Ansøgning, Ansøger, Jobsamtale og Rekrutteringsprojekt i din kommunikation med ansøgerne. **Skabeloner til ansøgnings-e-mail** kan oprettes for korrespondanceaktioner, så du hurtigt kan sende e-mails til ansøgere, der har en ansøgning med en bestemt kombination af status og korrespondanceaktion. Du kan f.eks. sende en bekræftelse via e-mail til alle ansøgninger med **Status** Modtaget og **korrespondanceaktionen** Modtaget. Når du sender e-mailen, har du mulighed for automatisk at opdatere status for ansøgningerne.

## <a name="application-routing"></a>Ansøgningsproces

Hvis en ansøgning skal gennemses af flere arbejdere, kan du bruge siden **Ansøgningsrute** til at oprette en arbejdercirkulationsliste for at administrere processen.

## <a name="interviews"></a>Samtaler

**Jobsamtaler med ansøger** kan planlægges fra siden **Ansøgninger**. Brug knappen **Send oplysninger om møde** til at sende en kalenderfil med planlægningsoplysninger om samtalen til ansøgeren og interviewer.

## <a name="skill-mapping"></a>Kompetencesøgning

**Kompetencesøgning** og **kompetencesøgning - profiler** kan bruges til at identificere kandidater, der kan være velegnet til en stilling.

## <a name="hiring-applicants"></a>Ansætte ansøgere

Brug siden **Ansøgninger** til at ansætte en ansøger. Når du ansætter en ansøger, får ansøgerposten statussen **Ansat**, og ansøgerens personpost i det globale adressekartotek knyttes til den nye medarbejderpost. Ændringerne i oplysningerne i det globale adressekartotek for den nye medarbejderpost, vises også i ansøgerposten. Dette kan hjælpe med at reducere indtastning af data, hvis den nye medarbejder på et tidspunkt søger et andet job i din virksomhed. Hvis du vil ansætte en eksisterende arbejder til en ny stilling, skal du klikke på **Skift stilling** i rullemenuen **Ansøgningsstatus** for at starte overførslen.
