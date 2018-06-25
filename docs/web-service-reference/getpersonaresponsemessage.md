---
title: GetPersonaResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a5bf44c6-c46b-442d-98d4-8b49fdf14b30
description: Die GetPersonaResponseMessage enthält die Antwortdaten, die eine Anforderung GetPersona entsteht.
ms.openlocfilehash: 7d38daac9c7c3a74ba9d9670c2bd16dcf2cd47e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758775"
---
# <a name="getpersonaresponsemessage"></a><span data-ttu-id="b2ee4-103">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b2ee4-103">GetPersonaResponseMessage</span></span>

<span data-ttu-id="b2ee4-104">Die **GetPersonaResponseMessage** enthält die Antwortdaten, die eine Anforderung **GetPersona** entsteht.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-104">The **GetPersonaResponseMessage** contains the response data resulting from a **GetPersona** request.</span></span> 
  
```XML
<GetPersonaResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Persona/>
</GetPersonaResponseMessage>
```

 <span data-ttu-id="b2ee4-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b2ee4-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b2ee4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b2ee4-106">Attributes and elements</span></span>

<span data-ttu-id="b2ee4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2ee4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b2ee4-108">Attributes</span></span>

<span data-ttu-id="b2ee4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b2ee4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2ee4-110">Child elements</span></span>

<span data-ttu-id="b2ee4-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Persona](persona.md)</span><span class="sxs-lookup"><span data-stu-id="b2ee4-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Persona](persona.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b2ee4-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2ee4-112">Parent elements</span></span>

[<span data-ttu-id="b2ee4-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b2ee4-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="b2ee4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b2ee4-114">Remarks</span></span>

<span data-ttu-id="b2ee4-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b2ee4-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2ee4-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b2ee4-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2ee4-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2ee4-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b2ee4-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b2ee4-119">Schema name</span></span>  <br/> |<span data-ttu-id="b2ee4-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b2ee4-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b2ee4-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b2ee4-121">Validation file</span></span>  <br/> |<span data-ttu-id="b2ee4-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b2ee4-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b2ee4-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b2ee4-123">Can be empty</span></span>  <br/> ||
   

