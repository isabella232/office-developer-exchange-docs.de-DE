---
title: ConvertIdResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertIdResponse
api_type:
- schema
ms.assetid: ac1f044f-04a4-42ef-b762-cac5cd37894d
description: Das ConvertIdResponse-Element enthält eine Antwort auf eine ConvertId an. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 80299afebcebf15546b0fdbe14f0b08960527a47
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757712"
---
# <a name="convertidresponse"></a><span data-ttu-id="69e73-104">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="69e73-104">ConvertIdResponse</span></span>

<span data-ttu-id="69e73-105">Das **ConvertIdResponse** -Element enthält eine Antwort auf eine ConvertId an.</span><span class="sxs-lookup"><span data-stu-id="69e73-105">The **ConvertIdResponse** element contains a response to a ConvertId request.</span></span> <span data-ttu-id="69e73-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="69e73-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertIdResponse>
   <ResponseMessages/>
</ConvertIdResponse>
```

 <span data-ttu-id="69e73-107">**ConvertIdResponseType**</span><span class="sxs-lookup"><span data-stu-id="69e73-107">**ConvertIdResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69e73-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="69e73-108">Attributes and elements</span></span>

<span data-ttu-id="69e73-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="69e73-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69e73-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="69e73-110">Attributes</span></span>

<span data-ttu-id="69e73-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="69e73-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69e73-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69e73-112">Child elements</span></span>

|<span data-ttu-id="69e73-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="69e73-113">**Element**</span></span>|<span data-ttu-id="69e73-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69e73-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69e73-115">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="69e73-115">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="69e73-116">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="69e73-116">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69e73-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69e73-117">Parent elements</span></span>

<span data-ttu-id="69e73-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="69e73-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69e73-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69e73-119">Remarks</span></span>

<span data-ttu-id="69e73-120">Antwortnachrichten, die innerhalb des [ResponseMessages](responsemessages.md) -Elements enthalten sind, werden Instanzen des Objekts ConvertIdResponseMessageType.</span><span class="sxs-lookup"><span data-stu-id="69e73-120">The response messages that are contained within the [ResponseMessages](responsemessages.md) element will be instances of ConvertIdResponseMessageType.</span></span> 
  
<span data-ttu-id="69e73-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="69e73-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69e73-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="69e73-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69e73-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="69e73-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="69e73-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="69e73-124">Schema Name</span></span>  <br/> |<span data-ttu-id="69e73-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="69e73-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="69e73-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="69e73-126">Validation File</span></span>  <br/> |<span data-ttu-id="69e73-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="69e73-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="69e73-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="69e73-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="69e73-129">False</span><span class="sxs-lookup"><span data-stu-id="69e73-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69e73-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69e73-130">See also</span></span>



[<span data-ttu-id="69e73-131">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="69e73-131">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="69e73-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="69e73-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="69e73-133">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="69e73-133">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

