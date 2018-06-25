---
title: GetMailTipsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTipsResponse
api_type:
- schema
ms.assetid: fe270e34-566e-4f9e-9e73-fbf38e06436d
description: Das GetMailTipsResponse-Element darstellt, die Antwortnachricht für einen Vorgang GetMailTips.
ms.openlocfilehash: e7a18e8818761af931d32b26aeaf58a2853fa684
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758729"
---
# <a name="getmailtipsresponse"></a><span data-ttu-id="39a84-103">GetMailTipsResponse</span><span class="sxs-lookup"><span data-stu-id="39a84-103">GetMailTipsResponse</span></span>

<span data-ttu-id="39a84-104">Das **GetMailTipsResponse** -Element stellt die Antwortnachricht für einen [Vorgang GetMailTips](getmailtips-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="39a84-104">The **GetMailTipsResponse** element represents the response message for a [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<GetMailTipsResponse>
   <ResponseMessages/>
</GetMailTipsResponse>
```

 <span data-ttu-id="39a84-105">**GetMailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="39a84-105">**GetMailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39a84-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="39a84-106">Attributes and elements</span></span>

<span data-ttu-id="39a84-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="39a84-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39a84-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="39a84-108">Attributes</span></span>

<span data-ttu-id="39a84-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="39a84-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39a84-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39a84-110">Child elements</span></span>

|<span data-ttu-id="39a84-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="39a84-111">**Element**</span></span>|<span data-ttu-id="39a84-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39a84-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39a84-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="39a84-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="39a84-114">Stellt eine Liste der e-Mail-Tipps Antwortnachrichten dar.</span><span class="sxs-lookup"><span data-stu-id="39a84-114">Represents a list of mail tips response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39a84-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39a84-115">Parent elements</span></span>

<span data-ttu-id="39a84-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="39a84-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="39a84-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="39a84-117">Text value</span></span>

<span data-ttu-id="39a84-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="39a84-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39a84-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39a84-119">Remarks</span></span>

<span data-ttu-id="39a84-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="39a84-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39a84-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="39a84-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39a84-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="39a84-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="39a84-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="39a84-123">Schema Name</span></span>  <br/> |<span data-ttu-id="39a84-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="39a84-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="39a84-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="39a84-125">Validation File</span></span>  <br/> |<span data-ttu-id="39a84-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="39a84-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="39a84-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="39a84-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="39a84-128">False</span><span class="sxs-lookup"><span data-stu-id="39a84-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39a84-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39a84-129">See also</span></span>



[<span data-ttu-id="39a84-130">GetMailTips-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39a84-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="39a84-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="39a84-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

