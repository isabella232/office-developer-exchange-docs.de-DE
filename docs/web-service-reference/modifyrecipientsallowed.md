---
title: ModifyRecipientsAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f25e673-0df0-4285-bf03-a083a395cdab
description: Das ModifyRecipientsAllowed-Element gibt an, ob die Änderung der Empfänger aktiviert ist.
ms.openlocfilehash: 2b07c7fa8e6b5872621c8b019b60584abbf98e3c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830473"
---
# <a name="modifyrecipientsallowed"></a><span data-ttu-id="2a5db-103">ModifyRecipientsAllowed</span><span class="sxs-lookup"><span data-stu-id="2a5db-103">ModifyRecipientsAllowed</span></span>

<span data-ttu-id="2a5db-104">Das **ModifyRecipientsAllowed** -Element gibt an, ob die Änderung der Empfänger aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2a5db-104">The **ModifyRecipientsAllowed** element specifies whether modification of the recipients is enabled.</span></span> 
  
```XML
<ModifyRecipientsAllowed> true | false </ModifyRecipientsAllowed>
```

 <span data-ttu-id="2a5db-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="2a5db-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a5db-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2a5db-106">Attributes and elements</span></span>

<span data-ttu-id="2a5db-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a5db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a5db-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2a5db-108">Attributes</span></span>

<span data-ttu-id="2a5db-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a5db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a5db-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a5db-110">Child elements</span></span>

<span data-ttu-id="2a5db-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a5db-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2a5db-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a5db-112">Parent elements</span></span>

[<span data-ttu-id="2a5db-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="2a5db-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="2a5db-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="2a5db-114">Text value</span></span>

<span data-ttu-id="2a5db-115">Der Textwert **true** für das **ModifyRecipientsAllowed** -Element gibt an, dass die Empfängerliste Element mit der Verwaltung von Informationsrechten aktiviert für ein Element geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a5db-115">A text value of **true** for the **ModifyRecipientsAllowed** element indicates that the item recipient list is modifiable for an item with rights management enabled on it.</span></span> <span data-ttu-id="2a5db-116">Der Wert **false** gibt an, dass die Empfängerliste nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a5db-116">A value of **false** indicates that the recipient list is not modifiable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2a5db-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2a5db-117">Remarks</span></span>

<span data-ttu-id="2a5db-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2a5db-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2a5db-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2a5db-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a5db-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2a5db-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a5db-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a5db-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a5db-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2a5db-122">Schema name</span></span>  <br/> |<span data-ttu-id="2a5db-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2a5db-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="2a5db-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2a5db-124">Validation file</span></span>  <br/> |<span data-ttu-id="2a5db-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2a5db-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a5db-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2a5db-126">Can be empty</span></span>  <br/> ||
   

