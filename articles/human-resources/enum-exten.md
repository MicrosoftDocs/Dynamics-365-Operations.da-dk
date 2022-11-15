---
title: Udvidelse af enum for kønsbasis
description: Denne artikel indeholder en oversigt over udvidelse af fastteksten til kønsbasis (enum).
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749310"
---
# <a name="gender-base-enum-extensibility"></a>Udvidelse af enum for kønsbasis

Fastteksten (enum) **Køn** kan nu udvides. Denne artikel beskriver de ændringer, du skal foretage i kodebasen, hvis du planlægger at udvide enum for **Køn**.

## <a name="gender-vs-hcmpersongender"></a>Køn vs. HcmPersonGender

Der er to enums for kønsværdierne:

- **Køn** (programplatform)
- **HcmPersonGender** (PersonnelManagement)

Enum **Køn** bruges i hele Microsoft Dynamics 365 Finance, hvorimod **HcmPersonGender** er specifik for funktionen til styring af menneskelig kapital (HCM). Hvis du bruger HCM-funktionalitet, og du foretager eventuelle ændringer af enum **Køn**, bør du overveje at foretage de samme ændringer af **HcmPersonGender**. Hvis du f.eks. føjer **Transkønnet** til **Køn** som enum, skal du også føje **Transkønnet** til **HcmPersonGender**-enum.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (klasse)

Der er oprettet en ny **HcmPersonGenderTranformUtil**-klasse, der gør det muligt at konvertere mellem de to basisfasttekster. I denne klasse er der to metoder: **convertGenderToHcmPersonGender** og **convertHcmPersonGenderToGender**. Du skal oprette en udvidelse ved at bruge klassen **Kommandokæde** eller **hændelseshandlere** og udvide begge metoder for at tilknytte nye værdier, der føjes til begge basis-enum.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (klasse)

**PayrollStateWageTaxPrepDP** er dataproviderklassen for **Payroll State Wage Tax Prep**-rapporten i SQL Server Reporting Services (SSRS). Der findes tre værdier for USA: **Mand**, **Kvinde** og **Uspecificeret**. I metoden **populatePayrollStateWageTaxPrepTmp** findes der en switch-sætning, der bruges til at tilknytte værdien af **HcmPersonGender**-enum til et af tre felter: **IsMale**, **IsFemale** eller **IsUnspecifiedGender**. Standardværdien for switch-sætningen er **IsUnspecifiedGender**. Hvis du føjer værdier til **HcmPersonGender**-enum for at tilknytte anderledes, skal du oprette en udvidelse ved at bruge klassen **Kommandokæde** over metoden **populatePayrollStateWageTaxPrepTmp** for at ændre værdien efter behov.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (klasse)

Integrationsklassen **smmOutlookSync_Contact** knytter værdier til og fra **Outlook** og **Kontaktpersoner**. **Outlook** understøtter tre værdier: **Mand**, **Kvinde** og **Uspecificeret**. Klassen har to metoder, du kan bruge til at knytte **Genders** til **OutlookGenders**. Standardmetoden er **NonSpecific/UnSpecified**. Hvis du opretter flere værdier for **Køn**-enum, skal du oprette en udvidelse ved at bruge klassen **Kommandokæde** på begge metoder for at tilknytte værdier efter behov.
