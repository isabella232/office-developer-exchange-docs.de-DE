---
title: SetImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c107b8d-714b-4cd5-ad1b-97b7cbcb90d6
description: Das SetImGroup-Element stellt eine Anforderung zum Ändern des Anzeigenamens einer Sofortnachrichten Gruppe dar.
ms.openlocfilehash: 96e93ef595720325448c343c193f25b846ba415e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44438068"
---
# <a name="setimgroup"></a><span data-ttu-id="d1cb9-103">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="d1cb9-103">SetImGroup</span></span>

<span data-ttu-id="d1cb9-104">Das **SetImGroup** -Element stellt eine Anforderung zum Ändern des Anzeigenamens einer Sofortnachrichten Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-104">The **SetImGroup** element represents a request to change the display name of an instant messaging group.</span></span> 
  
```XML
<SetImGroup>
   <GroupId/>
   <NewDisplayName/>
</SetImGroup>
```

 <span data-ttu-id="d1cb9-105">**SetImGroupType**</span><span class="sxs-lookup"><span data-stu-id="d1cb9-105">**SetImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1cb9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d1cb9-106">Attributes and elements</span></span>

<span data-ttu-id="d1cb9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1cb9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1cb9-108">Attributes</span></span>

<span data-ttu-id="d1cb9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1cb9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1cb9-110">Child elements</span></span>

<span data-ttu-id="d1cb9-111">[Gruppen-Nr](groupid.md)  |  [Neuanzeigename](newdisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="d1cb9-111">[GroupId](groupid.md) | [NewDisplayName](newdisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1cb9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1cb9-112">Parent elements</span></span>

<span data-ttu-id="d1cb9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1cb9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1cb9-114">Remarks</span></span>

<span data-ttu-id="d1cb9-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d1cb9-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d1cb9-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1cb9-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d1cb9-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1cb9-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1cb9-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d1cb9-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d1cb9-119">Schema name</span></span>  <br/> |<span data-ttu-id="d1cb9-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d1cb9-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d1cb9-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d1cb9-121">Validation file</span></span>  <br/> |<span data-ttu-id="d1cb9-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d1cb9-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d1cb9-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d1cb9-123">Can be empty</span></span>  <br/> ||
   

