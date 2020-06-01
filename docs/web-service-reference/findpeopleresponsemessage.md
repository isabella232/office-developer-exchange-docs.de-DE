---
title: FindPeopleResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba686738-e654-404d-ab54-83c71d030350
description: Das FindPeopleResponseMessage-Element gibt die Antwortnachricht für eine FindPeople-Anforderung an.
ms.openlocfilehash: 5a2ce7b8643fff9d4a93b62459638d3a99605c98
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466374"
---
# <a name="findpeopleresponsemessage"></a><span data-ttu-id="6fc6b-103">FindPeopleResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6fc6b-103">FindPeopleResponseMessage</span></span>

<span data-ttu-id="6fc6b-104">Das **FindPeopleResponseMessage** -Element gibt die Antwortnachricht für eine **FindPeople** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-104">The **FindPeopleResponseMessage** element specifies the response message for a **FindPeople** request.</span></span> 
  
```XML
<FindPeopleResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <People/>
   <TotalNumberOfPeopleInView/>
</FindPeopleResponseMessage>
```

 <span data-ttu-id="6fc6b-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6fc6b-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6fc6b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc6b-106">Attributes and elements</span></span>

<span data-ttu-id="6fc6b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fc6b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fc6b-108">Attributes</span></span>

<span data-ttu-id="6fc6b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6fc6b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc6b-110">Child elements</span></span>

<span data-ttu-id="6fc6b-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [Personen](people.md)  |  [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span><span class="sxs-lookup"><span data-stu-id="6fc6b-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [People](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6fc6b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc6b-112">Parent elements</span></span>

[<span data-ttu-id="6fc6b-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6fc6b-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="6fc6b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fc6b-114">Remarks</span></span>

<span data-ttu-id="6fc6b-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6fc6b-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6fc6b-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6fc6b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fc6b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fc6b-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6fc6b-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6fc6b-119">Schema name</span></span>  <br/> |<span data-ttu-id="6fc6b-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6fc6b-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6fc6b-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6fc6b-121">Validation file</span></span>  <br/> |<span data-ttu-id="6fc6b-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6fc6b-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6fc6b-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6fc6b-123">Can be empty</span></span>  <br/> |<span data-ttu-id="6fc6b-124">false</span><span class="sxs-lookup"><span data-stu-id="6fc6b-124">false</span></span>  <br/> |
   

