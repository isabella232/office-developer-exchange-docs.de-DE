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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457242"
---
# <a name="personaid"></a><span data-ttu-id="b225e-103">PersonaId</span><span class="sxs-lookup"><span data-stu-id="b225e-103">PersonaId</span></span>

<span data-ttu-id="b225e-104">Das **Persona** -ID-Element gibt den Persona-Bezeichner für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="b225e-104">The **PersonaId** element specifies the persona identifier for the associated persona.</span></span> 
  
```XML
<PersonaId Id="" ChangeKey=""/>
```

 <span data-ttu-id="b225e-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="b225e-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b225e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b225e-106">Attributes and elements</span></span>

<span data-ttu-id="b225e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b225e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b225e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b225e-108">Attributes</span></span>

|<span data-ttu-id="b225e-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b225e-109">**Attribute**</span></span>|<span data-ttu-id="b225e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b225e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b225e-111">Id</span><span class="sxs-lookup"><span data-stu-id="b225e-111">Id</span></span>  <br/> |<span data-ttu-id="b225e-112">Der Textwert des **ID-** Attributs ist der Bezeichner der Rolle.</span><span class="sxs-lookup"><span data-stu-id="b225e-112">The text value of the **Id** attribute is the identifier of the persona.</span></span>  <br/> |
|<span data-ttu-id="b225e-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="b225e-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="b225e-114">Der Textwert des **ChangeKey** -Attributs ist der Änderungsschlüssel der Rolle.</span><span class="sxs-lookup"><span data-stu-id="b225e-114">The text value of the **ChangeKey** attribute is the change key of the persona.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b225e-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b225e-115">Child elements</span></span>

<span data-ttu-id="b225e-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="b225e-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b225e-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b225e-117">Parent elements</span></span>

<span data-ttu-id="b225e-118">[Getpersona](getpersona.md)  |  [Persona](persona.md)</span><span class="sxs-lookup"><span data-stu-id="b225e-118">[GetPersona](getpersona.md) | [Persona](persona.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b225e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b225e-119">Remarks</span></span>

<span data-ttu-id="b225e-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b225e-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b225e-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b225e-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b225e-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b225e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b225e-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b225e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b225e-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b225e-124">Schema name</span></span>  <br/> |<span data-ttu-id="b225e-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b225e-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b225e-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b225e-126">Validation file</span></span>  <br/> |<span data-ttu-id="b225e-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b225e-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b225e-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b225e-128">Can be empty</span></span>  <br/> ||
   

