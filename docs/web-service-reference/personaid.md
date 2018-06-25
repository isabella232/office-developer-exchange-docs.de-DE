---
title: PersonaId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eec3a468-afd5-4d72-a61e-cd1964fb686c
description: Das PersonaId-Element gibt den Persona-Bezeichner für den zugeordneten Rolle.
ms.openlocfilehash: 77668a1b32a97eef08b3316c7d4d7c8e6494c7bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830738"
---
# <a name="personaid"></a><span data-ttu-id="ab72b-103">PersonaId</span><span class="sxs-lookup"><span data-stu-id="ab72b-103">PersonaId</span></span>

<span data-ttu-id="ab72b-104">Das **PersonaId** -Element gibt den Persona-Bezeichner für den zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="ab72b-104">The **PersonaId** element specifies the persona identifier for the associated persona.</span></span> 
  
```XML
<PersonaId Id="" ChangeKey=""/>
```

 <span data-ttu-id="ab72b-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="ab72b-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab72b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ab72b-106">Attributes and elements</span></span>

<span data-ttu-id="ab72b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ab72b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab72b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab72b-108">Attributes</span></span>

|<span data-ttu-id="ab72b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ab72b-109">**Attribute**</span></span>|<span data-ttu-id="ab72b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab72b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab72b-111">Id</span><span class="sxs-lookup"><span data-stu-id="ab72b-111">Id</span></span>  <br/> |<span data-ttu-id="ab72b-112">Der Textwert des **Id** -Attributs ist der Bezeichner der Rolle.</span><span class="sxs-lookup"><span data-stu-id="ab72b-112">The text value of the **Id** attribute is the identifier of the persona.</span></span>  <br/> |
|<span data-ttu-id="ab72b-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="ab72b-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="ab72b-114">Der Textwert des **ChangeKey** -Attributs ist der Key Ändern der Rolle.</span><span class="sxs-lookup"><span data-stu-id="ab72b-114">The text value of the **ChangeKey** attribute is the change key of the persona.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ab72b-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab72b-115">Child elements</span></span>

<span data-ttu-id="ab72b-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="ab72b-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ab72b-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab72b-117">Parent elements</span></span>

<span data-ttu-id="ab72b-118">[GetPersona](getpersona.md) | [Persona](persona.md)</span><span class="sxs-lookup"><span data-stu-id="ab72b-118">[GetPersona](getpersona.md) | [Persona](persona.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab72b-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab72b-119">Remarks</span></span>

<span data-ttu-id="ab72b-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ab72b-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ab72b-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ab72b-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab72b-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ab72b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab72b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab72b-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ab72b-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ab72b-124">Schema name</span></span>  <br/> |<span data-ttu-id="ab72b-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ab72b-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ab72b-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ab72b-126">Validation file</span></span>  <br/> |<span data-ttu-id="ab72b-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ab72b-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ab72b-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ab72b-128">Can be empty</span></span>  <br/> ||
   

