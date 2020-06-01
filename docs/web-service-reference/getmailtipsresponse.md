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
description: Das GetMailTipsResponse-Element stellt die Antwortnachricht für einen GetMailTips-Vorgang dar.
ms.openlocfilehash: 2c0dcfe4e2deddcf9a6f4bb9d68d59115c171796
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458607"
---
# <a name="getmailtipsresponse"></a><span data-ttu-id="564b9-103">GetMailTipsResponse</span><span class="sxs-lookup"><span data-stu-id="564b9-103">GetMailTipsResponse</span></span>

<span data-ttu-id="564b9-104">Das **GetMailTipsResponse** -Element stellt die Antwortnachricht für einen [GetMailTips-Vorgang](getmailtips-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="564b9-104">The **GetMailTipsResponse** element represents the response message for a [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<GetMailTipsResponse>
   <ResponseMessages/>
</GetMailTipsResponse>
```

 <span data-ttu-id="564b9-105">**GetMailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="564b9-105">**GetMailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="564b9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="564b9-106">Attributes and elements</span></span>

<span data-ttu-id="564b9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="564b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="564b9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="564b9-108">Attributes</span></span>

<span data-ttu-id="564b9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="564b9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="564b9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="564b9-110">Child elements</span></span>

|<span data-ttu-id="564b9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="564b9-111">**Element**</span></span>|<span data-ttu-id="564b9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="564b9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="564b9-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="564b9-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="564b9-114">Stellt eine Liste der e-Mail-Tipps Antwortnachrichten dar.</span><span class="sxs-lookup"><span data-stu-id="564b9-114">Represents a list of mail tips response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="564b9-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="564b9-115">Parent elements</span></span>

<span data-ttu-id="564b9-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="564b9-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="564b9-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="564b9-117">Text value</span></span>

<span data-ttu-id="564b9-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="564b9-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="564b9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="564b9-119">Remarks</span></span>

<span data-ttu-id="564b9-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="564b9-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="564b9-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="564b9-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="564b9-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="564b9-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="564b9-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="564b9-123">Schema Name</span></span>  <br/> |<span data-ttu-id="564b9-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="564b9-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="564b9-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="564b9-125">Validation File</span></span>  <br/> |<span data-ttu-id="564b9-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="564b9-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="564b9-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="564b9-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="564b9-128">False</span><span class="sxs-lookup"><span data-stu-id="564b9-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="564b9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="564b9-129">See also</span></span>



[<span data-ttu-id="564b9-130">GetMailTips-Vorgang</span><span class="sxs-lookup"><span data-stu-id="564b9-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="564b9-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="564b9-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

