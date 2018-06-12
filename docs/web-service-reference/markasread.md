---
title: MarkAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MarkAsRead
api_type:
- schema
ms.assetid: 404842e1-fbdb-480d-a1d8-ba1ab2c9fb1e
description: Das MarkAsRead-Element gibt an, ob Nachrichten sind, als gelesen markiert werden soll.
ms.openlocfilehash: b453ad73912e99b6fd3aed84b03a7d2fc2b6a294
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830355"
---
# <a name="markasread"></a><span data-ttu-id="d3de6-103">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="d3de6-103">MarkAsRead</span></span>

<span data-ttu-id="d3de6-104">Das **MarkAsRead** -Element gibt an, ob Nachrichten sind, als gelesen markiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3de6-104">The **MarkAsRead** element indicates whether messages are to be marked as read.</span></span> 
  
```XML
<MarkAsRead>true | false</MarkAsRead>
```

 <span data-ttu-id="d3de6-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d3de6-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3de6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d3de6-106">Attributes and elements</span></span>

<span data-ttu-id="d3de6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3de6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3de6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3de6-108">Attributes</span></span>

<span data-ttu-id="d3de6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3de6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3de6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3de6-110">Child elements</span></span>

<span data-ttu-id="d3de6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3de6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d3de6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3de6-112">Parent elements</span></span>

|<span data-ttu-id="d3de6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3de6-113">**Element**</span></span>|<span data-ttu-id="d3de6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3de6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3de6-115">Aktionen</span><span class="sxs-lookup"><span data-stu-id="d3de6-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="d3de6-116">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="d3de6-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d3de6-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="d3de6-117">Text value</span></span>

<span data-ttu-id="d3de6-118">Der Textwert **true** gibt an, dass die Nachricht als gelesen markiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d3de6-118">A text value of **true** indicates that the message must be marked as read.</span></span> <span data-ttu-id="d3de6-119">Der Wert **false** gibt an, dass Nachrichten nicht als gelesen markiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d3de6-119">A value of **false** indicates that messages must not be marked as read.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d3de6-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3de6-120">Remarks</span></span>

<span data-ttu-id="d3de6-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d3de6-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3de6-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d3de6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3de6-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3de6-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d3de6-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d3de6-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d3de6-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d3de6-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d3de6-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d3de6-126">Validation File</span></span>  <br/> |<span data-ttu-id="d3de6-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d3de6-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d3de6-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d3de6-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3de6-129">True</span><span class="sxs-lookup"><span data-stu-id="d3de6-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3de6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3de6-130">See also</span></span>



- [<span data-ttu-id="d3de6-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d3de6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

