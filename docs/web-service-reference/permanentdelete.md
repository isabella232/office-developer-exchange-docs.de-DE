---
title: PermanentDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermanentDelete
api_type:
- schema
ms.assetid: 1a0e0f46-1472-4eb7-bb54-f193a2603587
description: Das PermanentDelete-Element gibt an, ob Nachrichten endgültig gelöscht und nicht im Ordner "Gelöschte Elemente" gespeichert werden sollen.
ms.openlocfilehash: da7680eefca9ad359948af38eac49d18e9055988
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467767"
---
# <a name="permanentdelete"></a><span data-ttu-id="d3730-103">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="d3730-103">PermanentDelete</span></span>

<span data-ttu-id="d3730-104">Das **PermanentDelete** -Element gibt an, ob Nachrichten endgültig gelöscht und nicht im Ordner "Gelöschte Elemente" gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3730-104">The **PermanentDelete** element indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span> 
  
```XML
<PermanentDelete>true | false</PermanentDelete>
```

 <span data-ttu-id="d3730-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="d3730-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3730-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d3730-106">Attributes and elements</span></span>

<span data-ttu-id="d3730-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3730-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3730-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3730-108">Attributes</span></span>

<span data-ttu-id="d3730-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3730-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3730-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3730-110">Child elements</span></span>

<span data-ttu-id="d3730-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3730-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d3730-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3730-112">Parent elements</span></span>

|<span data-ttu-id="d3730-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3730-113">**Element**</span></span>|<span data-ttu-id="d3730-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3730-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3730-115">Aktionen</span><span class="sxs-lookup"><span data-stu-id="d3730-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="d3730-116">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="d3730-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d3730-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="d3730-117">Text value</span></span>

<span data-ttu-id="d3730-118">Der Textwert **true** gibt an, dass die Nachricht als dauerhaft gelöscht gekennzeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="d3730-118">A text value of **true** indicates that the message must be marked to be permanently deleted.</span></span> <span data-ttu-id="d3730-119">Der Wert **false** gibt an, dass die Nachricht nicht als dauerhaft gelöscht gekennzeichnet werden darf.</span><span class="sxs-lookup"><span data-stu-id="d3730-119">A value of **false** indicates that the message must not be marked to be permanently deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d3730-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3730-120">Remarks</span></span>

<span data-ttu-id="d3730-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d3730-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3730-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d3730-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3730-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3730-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d3730-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d3730-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d3730-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d3730-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d3730-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d3730-126">Validation File</span></span>  <br/> |<span data-ttu-id="d3730-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d3730-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d3730-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d3730-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3730-129">True</span><span class="sxs-lookup"><span data-stu-id="d3730-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3730-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3730-130">See also</span></span>



- [<span data-ttu-id="d3730-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d3730-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

