---
title: PersonaId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eec3a468-afd5-4d72-a61e-cd1964fb686c
description: Das Persona-ID-Element gibt den Persona-Bezeichner für die zugeordnete persona an.
ms.openlocfilehash: 3d7315097a14fb1eed5f378422cba80414601675
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457242"
---
# <a name="personaid"></a><span data-ttu-id="21c63-103">PersonaId</span><span class="sxs-lookup"><span data-stu-id="21c63-103">PersonaId</span></span>

<span data-ttu-id="21c63-104">Das **Persona** -ID-Element gibt den Persona-Bezeichner für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="21c63-104">The **PersonaId** element specifies the persona identifier for the associated persona.</span></span> 
  
```XML
<PersonaId Id="" ChangeKey=""/>
```

 <span data-ttu-id="21c63-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="21c63-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21c63-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="21c63-106">Attributes and elements</span></span>

<span data-ttu-id="21c63-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="21c63-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21c63-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="21c63-108">Attributes</span></span>

|<span data-ttu-id="21c63-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="21c63-109">**Attribute**</span></span>|<span data-ttu-id="21c63-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21c63-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21c63-111">Id</span><span class="sxs-lookup"><span data-stu-id="21c63-111">Id</span></span>  <br/> |<span data-ttu-id="21c63-112">Der Textwert des **ID-** Attributs ist der Bezeichner der Rolle.</span><span class="sxs-lookup"><span data-stu-id="21c63-112">The text value of the **Id** attribute is the identifier of the persona.</span></span>  <br/> |
|<span data-ttu-id="21c63-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="21c63-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="21c63-114">Der Textwert des **ChangeKey** -Attributs ist der Änderungsschlüssel der Rolle.</span><span class="sxs-lookup"><span data-stu-id="21c63-114">The text value of the **ChangeKey** attribute is the change key of the persona.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="21c63-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21c63-115">Child elements</span></span>

<span data-ttu-id="21c63-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="21c63-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21c63-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21c63-117">Parent elements</span></span>

<span data-ttu-id="21c63-118">[Getpersona](getpersona.md)  |  [Persona](persona.md)</span><span class="sxs-lookup"><span data-stu-id="21c63-118">[GetPersona](getpersona.md) | [Persona](persona.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21c63-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21c63-119">Remarks</span></span>

<span data-ttu-id="21c63-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="21c63-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="21c63-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="21c63-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21c63-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="21c63-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21c63-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="21c63-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="21c63-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="21c63-124">Schema name</span></span>  <br/> |<span data-ttu-id="21c63-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="21c63-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="21c63-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="21c63-126">Validation file</span></span>  <br/> |<span data-ttu-id="21c63-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="21c63-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="21c63-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="21c63-128">Can be empty</span></span>  <br/> ||
   

