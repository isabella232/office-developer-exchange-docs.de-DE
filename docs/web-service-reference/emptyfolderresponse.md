---
title: EmptyFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c900be49-3c90-41aa-aba5-bcf1116ec2aa
description: Das EmptyFolderResponse-Element definiert eine Antwort auf eine EmptyFolder-Vorgangsanforderung.
ms.openlocfilehash: 9b20df8c0b095870185aab14dbd1f7ff4fc47def
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530677"
---
# <a name="emptyfolderresponse"></a><span data-ttu-id="745c8-103">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="745c8-103">EmptyFolderResponse</span></span>

<span data-ttu-id="745c8-104">Das **EmptyFolderResponse** -Element definiert eine Antwort auf eine [EmptyFolder-Vorgangs](emptyfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="745c8-104">The **EmptyFolderResponse** element defines a response to an [EmptyFolder operation](emptyfolder-operation.md) request.</span></span> 
  
```XML
<EmptyFolderResponse>
   <ResponseMessages/>
</EmptyFolderResponse>
```

 <span data-ttu-id="745c8-105">**EmptyFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="745c8-105">**EmptyFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="745c8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="745c8-106">Attributes and elements</span></span>

<span data-ttu-id="745c8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="745c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="745c8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="745c8-108">Attributes</span></span>

<span data-ttu-id="745c8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="745c8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="745c8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="745c8-110">Child elements</span></span>

|<span data-ttu-id="745c8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="745c8-111">**Element**</span></span>|<span data-ttu-id="745c8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="745c8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="745c8-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="745c8-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="745c8-114">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="745c8-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="745c8-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="745c8-115">Parent elements</span></span>

<span data-ttu-id="745c8-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="745c8-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="745c8-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="745c8-117">Remarks</span></span>

<span data-ttu-id="745c8-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="745c8-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="745c8-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="745c8-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="745c8-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="745c8-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="745c8-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="745c8-121">Schema name</span></span>  <br/> |<span data-ttu-id="745c8-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="745c8-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="745c8-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="745c8-123">Validation file</span></span>  <br/> |<span data-ttu-id="745c8-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="745c8-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="745c8-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="745c8-125">Can be empty</span></span>  <br/> |<span data-ttu-id="745c8-126">False</span><span class="sxs-lookup"><span data-stu-id="745c8-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="745c8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="745c8-127">See also</span></span>



[<span data-ttu-id="745c8-128">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="745c8-128">EmptyFolder operation</span></span>](emptyfolder-operation.md)
  
[<span data-ttu-id="745c8-129">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="745c8-129">EmptyFolder</span></span>](emptyfolder.md)


- [<span data-ttu-id="745c8-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="745c8-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

