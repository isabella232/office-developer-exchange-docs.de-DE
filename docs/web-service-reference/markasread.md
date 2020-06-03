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
description: Das MarkAsRead-Element gibt an, ob Nachrichten als gelesen markiert werden sollen.
ms.openlocfilehash: 691409a4eace8885d36f4b30b8eef1aca8c332a6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461765"
---
# <a name="markasread"></a><span data-ttu-id="8a1dc-103">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="8a1dc-103">MarkAsRead</span></span>

<span data-ttu-id="8a1dc-104">Das **MarkAsRead** -Element gibt an, ob Nachrichten als gelesen markiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a1dc-104">The **MarkAsRead** element indicates whether messages are to be marked as read.</span></span> 
  
```XML
<MarkAsRead>true | false</MarkAsRead>
```

 <span data-ttu-id="8a1dc-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="8a1dc-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a1dc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8a1dc-106">Attributes and elements</span></span>

<span data-ttu-id="8a1dc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8a1dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a1dc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8a1dc-108">Attributes</span></span>

<span data-ttu-id="8a1dc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a1dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a1dc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a1dc-110">Child elements</span></span>

<span data-ttu-id="8a1dc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a1dc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a1dc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a1dc-112">Parent elements</span></span>

|<span data-ttu-id="8a1dc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a1dc-113">**Element**</span></span>|<span data-ttu-id="8a1dc-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a1dc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a1dc-115">Aktionen</span><span class="sxs-lookup"><span data-stu-id="8a1dc-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="8a1dc-116">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="8a1dc-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8a1dc-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="8a1dc-117">Text value</span></span>

<span data-ttu-id="8a1dc-118">Der Textwert **true** gibt an, dass die Nachricht als gelesen markiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8a1dc-118">A text value of **true** indicates that the message must be marked as read.</span></span> <span data-ttu-id="8a1dc-119">Der Wert **false** gibt an, dass Nachrichten nicht als gelesen markiert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="8a1dc-119">A value of **false** indicates that messages must not be marked as read.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8a1dc-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a1dc-120">Remarks</span></span>

<span data-ttu-id="8a1dc-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8a1dc-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a1dc-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8a1dc-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a1dc-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a1dc-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a1dc-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8a1dc-124">Schema Name</span></span>  <br/> |<span data-ttu-id="8a1dc-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8a1dc-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8a1dc-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8a1dc-126">Validation File</span></span>  <br/> |<span data-ttu-id="8a1dc-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8a1dc-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a1dc-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8a1dc-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="8a1dc-129">True</span><span class="sxs-lookup"><span data-stu-id="8a1dc-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a1dc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a1dc-130">See also</span></span>



- [<span data-ttu-id="8a1dc-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8a1dc-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

