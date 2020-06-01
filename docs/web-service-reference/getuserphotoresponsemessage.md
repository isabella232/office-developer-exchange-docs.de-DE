---
title: GetUserPhotoResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54d43fe6-9f7b-4f84-920a-bd686c65b059
description: Das GetUserPhotoResponseMessage-Element enthält die Antwort auf eine GetUserPhoto-Anforderung.
ms.openlocfilehash: a6df1204d4ac3a976694afbca008852acef6a76e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463300"
---
# <a name="getuserphotoresponsemessage"></a><span data-ttu-id="cfb62-103">GetUserPhotoResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cfb62-103">GetUserPhotoResponseMessage</span></span>

<span data-ttu-id="cfb62-104">Das **GetUserPhotoResponseMessage** -Element enthält die Antwort auf eine GetUserPhoto-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cfb62-104">The **GetUserPhotoResponseMessage** element contains the response to a GetUserPhoto request.</span></span> 
  
```XML
<GetUserPhotoResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <HasChanged/>
   <PictureData/>
</GetUserPhotoResponseMessage>
```

 <span data-ttu-id="cfb62-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cfb62-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cfb62-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cfb62-106">Attributes and elements</span></span>

<span data-ttu-id="cfb62-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cfb62-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cfb62-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cfb62-108">Attributes</span></span>

<span data-ttu-id="cfb62-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cfb62-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cfb62-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cfb62-110">Child elements</span></span>

<span data-ttu-id="cfb62-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [HasChanged](haschanged.md)  |  [PictureData](picturedata.md)</span><span class="sxs-lookup"><span data-stu-id="cfb62-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [HasChanged](haschanged.md) | [PictureData](picturedata.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cfb62-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cfb62-112">Parent elements</span></span>

[<span data-ttu-id="cfb62-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cfb62-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="cfb62-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfb62-114">Remarks</span></span>

<span data-ttu-id="cfb62-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cfb62-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cfb62-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cfb62-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cfb62-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cfb62-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfb62-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfb62-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cfb62-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cfb62-119">Schema name</span></span>  <br/> |<span data-ttu-id="cfb62-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cfb62-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cfb62-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cfb62-121">Validation file</span></span>  <br/> |<span data-ttu-id="cfb62-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cfb62-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cfb62-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cfb62-123">Can be empty</span></span>  <br/> ||
   

