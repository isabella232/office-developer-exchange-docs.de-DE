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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463300"
---
# <a name="getuserphotoresponsemessage"></a><span data-ttu-id="9d685-103">GetUserPhotoResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9d685-103">GetUserPhotoResponseMessage</span></span>

<span data-ttu-id="9d685-104">Das **GetUserPhotoResponseMessage** -Element enthält die Antwort auf eine GetUserPhoto-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9d685-104">The **GetUserPhotoResponseMessage** element contains the response to a GetUserPhoto request.</span></span> 
  
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

 <span data-ttu-id="9d685-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9d685-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d685-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d685-106">Attributes and elements</span></span>

<span data-ttu-id="9d685-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d685-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d685-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d685-108">Attributes</span></span>

<span data-ttu-id="9d685-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d685-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d685-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d685-110">Child elements</span></span>

<span data-ttu-id="9d685-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [HasChanged](haschanged.md)  |  [PictureData](picturedata.md)</span><span class="sxs-lookup"><span data-stu-id="9d685-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [HasChanged](haschanged.md) | [PictureData](picturedata.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9d685-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d685-112">Parent elements</span></span>

[<span data-ttu-id="9d685-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9d685-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="9d685-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d685-114">Remarks</span></span>

<span data-ttu-id="9d685-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9d685-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9d685-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9d685-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d685-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9d685-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d685-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d685-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9d685-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d685-119">Schema name</span></span>  <br/> |<span data-ttu-id="9d685-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9d685-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9d685-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d685-121">Validation file</span></span>  <br/> |<span data-ttu-id="9d685-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9d685-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d685-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9d685-123">Can be empty</span></span>  <br/> ||
   

