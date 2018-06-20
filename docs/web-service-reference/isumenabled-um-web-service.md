---
title: IsUMEnabled (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: 33810bbd-837f-4a71-9ed9-cb4b8c52186d
description: Das IsUMEnabled-Element gibt an, ob ein Postfach für Unified Messaging aktiviert ist.
ms.openlocfilehash: 5f4d59c5497158e5afbc8bb5db4900bd129df50b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830113"
---
# <a name="isumenabled-um-web-service"></a><span data-ttu-id="eda7a-103">IsUMEnabled (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="eda7a-103">IsUMEnabled (UM web service)</span></span>

<span data-ttu-id="eda7a-104">Das **IsUMEnabled** -Element gibt an, ob ein Postfach für Unified Messaging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eda7a-104">The **IsUMEnabled** element indicates whether a mailbox is enabled for Unified Messaging.</span></span> 
  
```xml
<IsUMEnabled/>
```

 <span data-ttu-id="eda7a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="eda7a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eda7a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eda7a-106">Attributes and elements</span></span>

<span data-ttu-id="eda7a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eda7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eda7a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="eda7a-108">Attributes</span></span>

<span data-ttu-id="eda7a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="eda7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eda7a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eda7a-110">Child elements</span></span>

<span data-ttu-id="eda7a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="eda7a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eda7a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eda7a-112">Parent elements</span></span>

<span data-ttu-id="eda7a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="eda7a-113">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="eda7a-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="eda7a-114">Text value</span></span>

<span data-ttu-id="eda7a-115">Ein Textwert, der einen booleschen Wert darstellt ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="eda7a-115">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="eda7a-116">Der Wert **true** gibt an, dass das Postfach für Unified Messaging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eda7a-116">A value of **true** indicates that the mailbox is enabled for Unified Messaging.</span></span> <span data-ttu-id="eda7a-117">Der Wert **false** bedeutet, dass das Postfach nicht für Unified Messaging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eda7a-117">A value of **false** means that the mailbox is not enabled for Unified Messaging.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eda7a-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eda7a-118">Remarks</span></span>

<span data-ttu-id="eda7a-119">Um zu bestimmen, ob ein Postfach für Unified Messaging aktiviert ist, verwenden Sie die [IsUMEnabled-Vorgang (UM-Webdienst)](isumenabled-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="eda7a-119">To determine whether a mailbox is enabled for Unified Messaging, use the [IsUMEnabled operation (UM web service)](isumenabled-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eda7a-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eda7a-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eda7a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="eda7a-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eda7a-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eda7a-122">Schema Name</span></span>  <br/> |<span data-ttu-id="eda7a-123">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="eda7a-123">Messages</span></span>  <br/> |
|<span data-ttu-id="eda7a-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eda7a-124">Validation File</span></span>  <br/> |<span data-ttu-id="eda7a-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eda7a-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eda7a-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="eda7a-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="eda7a-127">False</span><span class="sxs-lookup"><span data-stu-id="eda7a-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eda7a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eda7a-128">See also</span></span>



[<span data-ttu-id="eda7a-129">IsUMEnabled-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="eda7a-129">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)


[<span data-ttu-id="eda7a-130">Unified Messaging Web Service XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="eda7a-130">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)

