---
title: FindPeopleResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba686738-e654-404d-ab54-83c71d030350
description: Das FindPeopleResponseMessage-Element gibt die Antwortnachricht für eine Anforderung FindPeople.
ms.openlocfilehash: 205f20b26b5097d24de45c5a5f9681f3557a6f87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758481"
---
# <a name="findpeopleresponsemessage"></a><span data-ttu-id="d154f-103">FindPeopleResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d154f-103">FindPeopleResponseMessage</span></span>

<span data-ttu-id="d154f-104">Das **FindPeopleResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="d154f-104">The **FindPeopleResponseMessage** element specifies the response message for a **FindPeople** request.</span></span> 
  
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

 <span data-ttu-id="d154f-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d154f-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d154f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d154f-106">Attributes and elements</span></span>

<span data-ttu-id="d154f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d154f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d154f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d154f-108">Attributes</span></span>

<span data-ttu-id="d154f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d154f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d154f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d154f-110">Child elements</span></span>

<span data-ttu-id="d154f-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Personen](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span><span class="sxs-lookup"><span data-stu-id="d154f-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [People](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d154f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d154f-112">Parent elements</span></span>

[<span data-ttu-id="d154f-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d154f-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="d154f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d154f-114">Remarks</span></span>

<span data-ttu-id="d154f-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d154f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d154f-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d154f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d154f-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d154f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d154f-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="d154f-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d154f-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d154f-119">Schema name</span></span>  <br/> |<span data-ttu-id="d154f-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d154f-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d154f-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d154f-121">Validation file</span></span>  <br/> |<span data-ttu-id="d154f-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d154f-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d154f-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d154f-123">Can be empty</span></span>  <br/> |<span data-ttu-id="d154f-124">false</span><span class="sxs-lookup"><span data-stu-id="d154f-124">false</span></span>  <br/> |
   

