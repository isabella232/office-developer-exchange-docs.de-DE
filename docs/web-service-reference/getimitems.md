---
title: GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 455e5709-6c06-49fd-bfb2-403fc912287c
description: Das GetImItems Anforderung-Element definiert eine Anforderung zum Abrufen von Informationen zu den angegebenen instant messaging-Gruppen und Instant messaging-Kontakte Rollen.
ms.openlocfilehash: ff7d520dde44fac6e9278633c1ad46b07b38d6c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758697"
---
# <a name="getimitems"></a><span data-ttu-id="e0a6f-103">GetImItems</span><span class="sxs-lookup"><span data-stu-id="e0a6f-103">GetImItems</span></span>

<span data-ttu-id="e0a6f-104">Das **GetImItems** Anforderung-Element definiert eine Anforderung zum Abrufen von Informationen zu den angegebenen instant messaging-Gruppen und Instant messaging-Kontakte Rollen.</span><span class="sxs-lookup"><span data-stu-id="e0a6f-104">The **GetImItems** request element defines a request to get information about the specified instant messaging groups and instant messaging contact personas.</span></span> 
  
```XML
<GetImItems>
   <ContactIds/>
   <GroupIds/>
   <ExtendedProperties/>
</GetImItems>
```

 <span data-ttu-id="e0a6f-105">**GetImItemsType**</span><span class="sxs-lookup"><span data-stu-id="e0a6f-105">**GetImItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0a6f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e0a6f-106">Attributes and elements</span></span>

<span data-ttu-id="e0a6f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e0a6f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0a6f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e0a6f-108">Attributes</span></span>

<span data-ttu-id="e0a6f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e0a6f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0a6f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0a6f-110">Child elements</span></span>

<span data-ttu-id="e0a6f-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span><span class="sxs-lookup"><span data-stu-id="e0a6f-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e0a6f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0a6f-112">Parent elements</span></span>

<span data-ttu-id="e0a6f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e0a6f-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0a6f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0a6f-114">Remarks</span></span>

<span data-ttu-id="e0a6f-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e0a6f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e0a6f-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e0a6f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0a6f-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e0a6f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0a6f-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0a6f-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0a6f-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e0a6f-119">Schema name</span></span>  <br/> |<span data-ttu-id="e0a6f-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e0a6f-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0a6f-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e0a6f-121">Validation file</span></span>  <br/> |<span data-ttu-id="e0a6f-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e0a6f-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0a6f-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e0a6f-123">Can be empty</span></span>  <br/> ||
   

