---
title: SettingName (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8bcb0411-58b0-4e37-b97e-00c07dcbecb1
description: Das SettingName-Element stellt den Namen einer Einstellung in der Antwort dar.
ms.openlocfilehash: d492b82b7385d6403f15c08356db5d0503792d54
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466724"
---
# <a name="settingname-soap"></a><span data-ttu-id="1de56-103">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1de56-103">SettingName (SOAP)</span></span>

<span data-ttu-id="1de56-104">Das **SettingName** -Element stellt den Namen einer Einstellung in der Antwort dar.</span><span class="sxs-lookup"><span data-stu-id="1de56-104">The **SettingName** element represents the name of a setting in the response.</span></span> 
  
```XML
<SettingName/>
```

 <span data-ttu-id="1de56-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1de56-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1de56-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1de56-106">Attributes and elements</span></span>

<span data-ttu-id="1de56-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1de56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1de56-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1de56-108">Attributes</span></span>

<span data-ttu-id="1de56-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1de56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1de56-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1de56-110">Child elements</span></span>

<span data-ttu-id="1de56-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1de56-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1de56-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1de56-112">Parent elements</span></span>

|<span data-ttu-id="1de56-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1de56-113">**Element**</span></span>|<span data-ttu-id="1de56-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1de56-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1de56-115">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1de56-115">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="1de56-116">Stellt einen Fehler dar, der beim Abrufen einer Benutzereinstellung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1de56-116">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="1de56-117">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1de56-117">DomainSettingError (SOAP)</span></span>](domainsettingerror-soap.md) <br/> |<span data-ttu-id="1de56-118">Stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1de56-118">Represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="1de56-119">Dies stellt einen Fehler aus einer **GetDomainSettings** -Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="1de56-119">This represents an error from a **GetDomainSettings** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1de56-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="1de56-120">Text value</span></span>

<span data-ttu-id="1de56-121">Der Wert des **SettingName** -Elements stellt den Namen einer Einstellung in einer Antwort dar.</span><span class="sxs-lookup"><span data-stu-id="1de56-121">The value of the **SettingName** element represents the name of a setting in a response.</span></span> 
  
<span data-ttu-id="1de56-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1de56-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1de56-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1de56-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1de56-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="1de56-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="1de56-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1de56-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1de56-126">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="1de56-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="1de56-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1de56-127">Validation File</span></span>  <br/> |<span data-ttu-id="1de56-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1de56-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1de56-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1de56-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="1de56-130">True</span><span class="sxs-lookup"><span data-stu-id="1de56-130">True</span></span>  <br/> |
   

