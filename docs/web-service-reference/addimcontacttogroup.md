---
title: AddImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65554e4c-c0d9-485e-9f01-ed1baa8280ab
description: Das AddImContactToGroup-Element definiert eine Anforderung an einen vorhandenen instant messaging-Kontakt zu einer instant messaging-Gruppe hinzufügen.
ms.openlocfilehash: 71c841ce6df2ed7dcbbf77597b26f3e3e742a7fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757304"
---
# <a name="addimcontacttogroup"></a><span data-ttu-id="eeb16-103">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="eeb16-103">AddImContactToGroup</span></span>

<span data-ttu-id="eeb16-104">Das **AddImContactToGroup** -Element definiert eine Anforderung an einen vorhandenen instant messaging-Kontakt zu einer instant messaging-Gruppe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eeb16-104">The **AddImContactToGroup** element defines a request to add an existing instant messaging contact to an instant messaging group.</span></span> 
  
```XML
<AddImContactToGroup>
   <ContactId/>
   <GroupId/>
</AddImContactToGroup>
```

 <span data-ttu-id="eeb16-105">**AddImContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="eeb16-105">**AddImContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eeb16-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eeb16-106">Attributes and elements</span></span>

<span data-ttu-id="eeb16-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eeb16-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eeb16-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="eeb16-108">Attributes</span></span>

<span data-ttu-id="eeb16-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="eeb16-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eeb16-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eeb16-110">Child elements</span></span>

<span data-ttu-id="eeb16-111">[ContactId](contactid.md) | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="eeb16-111">[ContactId](contactid.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eeb16-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eeb16-112">Parent elements</span></span>

<span data-ttu-id="eeb16-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="eeb16-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eeb16-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eeb16-114">Remarks</span></span>

<span data-ttu-id="eeb16-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eeb16-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eeb16-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="eeb16-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eeb16-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eeb16-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eeb16-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="eeb16-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eeb16-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eeb16-119">Schema name</span></span>  <br/> |<span data-ttu-id="eeb16-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="eeb16-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eeb16-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eeb16-121">Validation file</span></span>  <br/> |<span data-ttu-id="eeb16-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eeb16-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eeb16-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="eeb16-123">Can be empty</span></span>  <br/> |<span data-ttu-id="eeb16-124">false</span><span class="sxs-lookup"><span data-stu-id="eeb16-124">false</span></span>  <br/> |
   

