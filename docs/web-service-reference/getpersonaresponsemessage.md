---
title: GetPersonaResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a5bf44c6-c46b-442d-98d4-8b49fdf14b30
description: Das GetPersonaResponseMessage enthält die Antwortdaten, die aus einer getpersona-Anforderung resultieren.
ms.openlocfilehash: 6391e1b6682180e292d03c5db651e8edc6f46b52
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458327"
---
# <a name="getpersonaresponsemessage"></a><span data-ttu-id="097f1-103">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="097f1-103">GetPersonaResponseMessage</span></span>

<span data-ttu-id="097f1-104">Das **GetPersonaResponseMessage** enthält die Antwortdaten, die aus einer **getpersona** -Anforderung resultieren.</span><span class="sxs-lookup"><span data-stu-id="097f1-104">The **GetPersonaResponseMessage** contains the response data resulting from a **GetPersona** request.</span></span> 
  
```XML
<GetPersonaResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Persona/>
</GetPersonaResponseMessage>
```

 <span data-ttu-id="097f1-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="097f1-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="097f1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="097f1-106">Attributes and elements</span></span>

<span data-ttu-id="097f1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="097f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="097f1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="097f1-108">Attributes</span></span>

<span data-ttu-id="097f1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="097f1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="097f1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="097f1-110">Child elements</span></span>

<span data-ttu-id="097f1-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [Persona](persona.md)</span><span class="sxs-lookup"><span data-stu-id="097f1-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Persona](persona.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="097f1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="097f1-112">Parent elements</span></span>

[<span data-ttu-id="097f1-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="097f1-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="097f1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="097f1-114">Remarks</span></span>

<span data-ttu-id="097f1-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="097f1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="097f1-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="097f1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="097f1-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="097f1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="097f1-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="097f1-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="097f1-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="097f1-119">Schema name</span></span>  <br/> |<span data-ttu-id="097f1-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="097f1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="097f1-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="097f1-121">Validation file</span></span>  <br/> |<span data-ttu-id="097f1-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="097f1-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="097f1-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="097f1-123">Can be empty</span></span>  <br/> ||
   

