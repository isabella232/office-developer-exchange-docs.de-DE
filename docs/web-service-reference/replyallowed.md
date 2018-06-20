---
title: ReplyAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 880af57e-0fa1-473c-b87c-f02f1133ba5e
description: Das ReplyAllowed-Element gibt an, ob eine Antwort verwaltete Daten, die für die Verwaltung von Informationsrechten zulässig ist.
ms.openlocfilehash: c774836ac6e72648d6a6c017d41fcafdb64d116c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831107"
---
# <a name="replyallowed"></a><span data-ttu-id="b21d9-103">ReplyAllowed</span><span class="sxs-lookup"><span data-stu-id="b21d9-103">ReplyAllowed</span></span>

<span data-ttu-id="b21d9-104">Das **ReplyAllowed** -Element gibt an, ob eine Antwort verwaltete Daten, die für die Verwaltung von Informationsrechten zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="b21d9-104">The **ReplyAllowed** element specifies whether a reply is allowed for rights managed data.</span></span> 
  
```XML
<ReplyAllowed> true | false </ReplyAllowed>
```

 <span data-ttu-id="b21d9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b21d9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b21d9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b21d9-106">Attributes and elements</span></span>

<span data-ttu-id="b21d9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b21d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b21d9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b21d9-108">Attributes</span></span>

<span data-ttu-id="b21d9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b21d9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b21d9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b21d9-110">Child elements</span></span>

<span data-ttu-id="b21d9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b21d9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b21d9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b21d9-112">Parent elements</span></span>

[<span data-ttu-id="b21d9-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="b21d9-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="b21d9-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="b21d9-114">Text value</span></span>

<span data-ttu-id="b21d9-115">Der Textwert **true** für das **ReplyAllowed** -Element gibt an, dass Antworten für die Rechte verwaltete Daten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b21d9-115">A text value of **true** for the **ReplyAllowed** element indicates that replies are allowed for the rights managed data.</span></span> <span data-ttu-id="b21d9-116">Der Wert **false** gibt an, dass Antworten nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b21d9-116">A value of **false** indicates that replies are not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b21d9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b21d9-117">Remarks</span></span>

<span data-ttu-id="b21d9-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b21d9-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b21d9-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b21d9-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b21d9-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b21d9-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b21d9-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b21d9-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b21d9-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b21d9-122">Schema name</span></span>  <br/> |<span data-ttu-id="b21d9-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b21d9-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="b21d9-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b21d9-124">Validation file</span></span>  <br/> |<span data-ttu-id="b21d9-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b21d9-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b21d9-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b21d9-126">Can be empty</span></span>  <br/> ||
   

