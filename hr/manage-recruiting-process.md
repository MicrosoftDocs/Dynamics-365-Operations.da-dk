---
title: Administrere en rekrutteringsproces
description: "I denne artikel beskrives et koncept, som rekrutteringsmedarbejdere kan bruge til at spore trinnene i en rekrutteringsproces, herunder arbejdet med at annoncere ledige stillinger og rekruttere ansøgere, spore oplysninger om ansøgeren og ansøgningen, interviewe ansøgere og vælge en eller flere kandidater til at udfylde de ledige stillinger i organisationen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 551e15ed31953d6e5fc99a1177c1310194ea95d0
ms.lasthandoff: 03/31/2017


---

# <a name="manage-a-recruiting-process"></a>Administrere en rekrutteringsproces

Dette emne beskriver et koncept, som jobagenter kan bruge til at spore trinnene i en proces, rekruttering, herunder bestræbelser på at annoncere ledige stillinger og rekruttering af ansøgere, sporing af oplysninger om ansøgeren og ansøgningen, interviewing ansøgere og vælge en eller flere kandidater til at udfylde de ledige stillinger i organisationen.

<a name="overview"></a>Overblik
--------

Rekrutteringsprojekter kan hjælpe dig med at organisere de trin, du skal udføre under udfyldning af ledige stillinger i en juridisk enhed. En ansøger er en person, der gælder for ansættelse til din virksomhed.  Et program er en ansøger udtryk for interesse i at blive ansat af en virksomhed og kan være bundet til et rekrutteringsprojekt til udtrykkelige interesse i en bestemt åbning.  En enkelt ansøger kan have flere programmer inden for samme juridiske enhed eller på tværs af flere firmaer i organisationen.

<a name="recruitment-projects"></a>Rekrutteringsprojekter
--------------------

Rekrutteringsprojekter gør det muligt for jobagenter at spore status i forhold til udfyldning af en eller flere ledige stillinger.  Rekrutteringsprojektet identificerer afdeling og det job, som en eller flere stillinger er åbne. Rekrutteringsprojekter kan også registrere følgende oplysninger om ledige stillinger:
-   Antallet af ledige stillinger
-   Den ansvarlige for ansættelsen og en alternativ kontakt for stillingen
-   Den dato, da rekvisitionen blev godkendt
-   Ansøgningsfristen
-   Den anslåede startdato

Rekrutteringsprojektet indeholder den **jobannonce**, der blev brugt på **Medarbejderselvbetjeningen** for at annoncere for stillingen. For at vise stillingen til medarbejdere, skal rekrutteringsprojektet have en **jobannonce**, feltet** Vis på medarbejderselvbetjening** skal være angivet til Ja, **ansøgningsfristen** skal angives til en fremtidig dato, og rekrutteringsprojektet skal have en **projektstatus**, der er igangsat. I følgende tabel vises de mulige ansættelse projektstatusser og deres beskrivelse.

| **Status**    | **Indicates that…**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Planlagt | Rekruttering indsats fremstilles.  Rekruttering er endnu ikke startet for dette projekt. |
| Startet   | Ansøgninger accepteres nu for stillinger i dette projekt.                    |
| Udført  | Alle stillinger i dette projekt er blevet udfyldt.                                          |
| Annulleret  | Rekruttering er blevet annulleret for dette projekt.                                           |

Rekrutteringsmedarbejdere kan også registrere det **medie**, der bruges til at annoncere stillingen via eksterne medier samt holde styr på **udviklingen** i forhold til projektet eller ansøgninger.

<a name="applicants"></a>Ansøgere
----------

En ansøger er en person, der ansøger om et job i virksomheden.  Ansøgere deles mellem alle juridiske enheder i organisationen, hvilket giver dig en stor pulje af talent for at søge fra. Du kan angive kvalifikationer, referencer, tilpasningsanmodninger og personlige oplysninger for ansøgere. Når du opretter en ansøgningspost, oprettes en personpost for ansøgeren i det globale adressekartotek. Du kan bruge siden **Ansøger** til at opdatere følgende globale adressekartoteksoplysninger for personer, der er ansøgere:
-   Adresseoplysninger
-   Kontaktoplysninger
-   Identifikationsoplysninger
-   Navnedetaljer
-   Personlige oplysninger

## <a name="applications"></a>Applikationer
Du kan registrere oplysninger fra modtagne jobansøgninger på siden **Ansøgning**. Programmet er ansøgerens udtryk for interesse i en sag, der er åbne i din organisation.  Hvis du vil oprette et program, skal ansøgeren allerede findes som en ansøger eller en person i dit system.
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

En **ansøgnings** korrespondanceaktion afgør, hvilken dokument- eller e-mailskabelon, der bruges til at kommunikere med den ansøger, der har sendt ansøgningen. Du kan knytte **ansøgningsbogmærker** med korrespondanceaktioner, så du kan bruge værdier fra programmet, ansøgeren, samtale og ansættelse projekt sider i din kommunikation med ansøgerne.  **Skabeloner til ansøgnings** kan oprettes for korrespondancetype handlinger, så du hurtigt vil sende e-mails til ansøgere, der har et program med en bestemt status og korrespondance handling kombination. For eksempel kan du sende en bekræftelse via e-mail til alle programmer med en **Status** modtaget og en **korrespondance handling** modtaget.  Når du sender e-mailen, har du mulighed for automatisk at opdatere status for programmerne.

## <a name="application-routing"></a>Ansøgningsproces

Hvis en ansøgning skal gennemses af flere arbejdere, kan du bruge siden **Ansøgningsrute** til at oprette en arbejdercirkulationsliste for at administrere processen.

## <a name="interviews"></a>Samtaler

**Ansøgersamtaler** kan planlægges fra den **programmer** side.  Brug af **sende mødeoplysninger** knap til at sende en kalenderfil med planlægningsoplysninger samtalen til ansøgeren og interviewer.

## <a name="skill-mapping"></a>Kompetencesøgning

**Kompetencesøgning** og **kompetencesøgning - profiler** kan bruges til at identificere kandidater, der kan være velegnet til en stilling.

## <a name="hiring-applicants"></a>Ansætte ansøgere

Brug siden **Ansøgninger** til at ansætte en ansøger. Når du ansætter en ansøger, får ansøgerposten statussen **Ansat**, og ansøgerens personpost i det globale adressekartotek knyttes til den nye medarbejderpost. Ændringerne i oplysningerne i det globale adressekartotek for den nye medarbejderpost, vises også i ansøgerposten. Dette kan hjælpe med at reducere indtastning af data, hvis den nye arbejder nogensinde gælder for et andet job i virksomheden.  For at ansætte en eksisterende arbejder til en ny placering, skal du klikke på **ændre placering** i den **Ansøgningsstatus** direkte til initiate overførslen.




