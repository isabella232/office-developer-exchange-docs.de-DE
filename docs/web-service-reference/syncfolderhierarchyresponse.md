---
title: SyncFolderHierarchyResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchyResponse
api_type:
- schema
ms.assetid: 7e6061d2-bbce-4864-a7bb-a6457628cb7c
description: Das SyncFolderHierarchyResponse-Element definiert eine Antwort auf eine SyncFolderHierarchy an.
ms.openlocfilehash: aee70603b84dfdf5f7f580fd2566f7ebfbbce383
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839148"
---
# <a name="syncfolderhierarchyresponse"></a><span data-ttu-id="b5903-103">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="b5903-103">SyncFolderHierarchyResponse</span></span>

<span data-ttu-id="b5903-104">Das **SyncFolderHierarchyResponse** -Element definiert eine Antwort auf eine SyncFolderHierarchy an.</span><span class="sxs-lookup"><span data-stu-id="b5903-104">The **SyncFolderHierarchyResponse** element defines a response to a SyncFolderHierarchy request.</span></span> 
  
```xml
<SyncFolderHierarchyResponse>
   <ResponseMessages/>
</SyncFolderHierarchyResponse>
```

 <span data-ttu-id="b5903-105">**SyncFolderHierarchyResponseType**</span><span class="sxs-lookup"><span data-stu-id="b5903-105">**SyncFolderHierarchyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5903-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b5903-106">Attributes and elements</span></span>

<span data-ttu-id="b5903-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5903-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5903-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5903-108">Attributes</span></span>

<span data-ttu-id="b5903-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5903-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5903-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5903-110">Child elements</span></span>

|<span data-ttu-id="b5903-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5903-111">**Element**</span></span>|<span data-ttu-id="b5903-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5903-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5903-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b5903-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b5903-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b5903-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b5903-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5903-115">Parent elements</span></span>

<span data-ttu-id="b5903-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5903-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5903-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5903-117">Remarks</span></span>

<span data-ttu-id="b5903-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b5903-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5903-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b5903-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5903-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5903-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b5903-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b5903-121">Schema name</span></span>  <br/> |<span data-ttu-id="b5903-122">Nachrichten-schema</span><span class="sxs-lookup"><span data-stu-id="b5903-122">messages schema</span></span>  <br/> |
|<span data-ttu-id="b5903-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b5903-123">Validation file</span></span>  <br/> |<span data-ttu-id="b5903-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b5903-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b5903-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b5903-125">Can be empty</span></span>  <br/> |<span data-ttu-id="b5903-126">False</span><span class="sxs-lookup"><span data-stu-id="b5903-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5903-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5903-127">See also</span></span>



[<span data-ttu-id="b5903-128">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b5903-128">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="b5903-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b5903-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

