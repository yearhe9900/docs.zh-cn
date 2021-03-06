---
title: 如何：将 ASP.NET 授权管理器角色提供程序与服务一起使用
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f21deb81-91ef-49ef-94d6-494785143271
caps.latest.revision: 6
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 00df44a3f87e5a3fc3374f1429f6b427e0d3d76e
ms.sourcegitcommit: 94d33cadc5ff81d2ac389bf5f26422c227832052
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/30/2018
---
# <a name="how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service"></a>如何：将 ASP.NET 授权管理器角色提供程序与服务一起使用
[!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 承载 Web 服务时，您可以将授权管理器集成到应用程序以向服务提供授权。 授权管理器允许应用程序开发人员定义各个操作，这些操作可组织在一起形成任务。 然后管理员可以授权角色执行特定任务或各个操作。 授权管理器提供管理工具，并将其作为 Microsoft 管理控制台 (MMC) 管理单元来管理角色、任务、操作和用户。 管理员在 XML 文件、Active Directory 或 Active Directory 应用程序模式 (ADAM) 存储区中配置授权管理器策略存储区。  
  
 通过为承载 Web 服务的 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 应用程序配置授权管理器 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 角色提供程序可以将授权管理器集成到该应用程序中。 像其他 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 角色提供程序一样，授权管理器 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 角色提供程序是使用 <`providers`> 元素进行配置的。  
  
 下面的代码示例是 Web 服务配置文件的一部分，该 Web 服务将授权管理器集成到应用程序中。  
  
```xml  
<system.web>  
    <roleManager enabled="true" defaultProvider="AzManRoleProvider">  
      <providers>  
        <add name="AzManRoleProvider"  
             type="System.Web.Security.AuthorizationStoreRoleProvider, System.Web, Version=2.0.0.0, Culture=neutral, publicKeyToken=b03f5f7f11d50a3a"  
             connectionStringName="AzManPolicyStoreConnectionString"   
             applicationName="SecureService"/>  
      </providers>  
    </roleManager>  
</system.web>  
```  
  
 有关将集成的详细信息[!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]具有的角色提供程序[!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]应用程序，请参阅[如何： 使用 ASP.NET 角色提供程序与服务](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)。 有关使用授权管理器使用的详细信息[!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]，请参阅[如何： 使用授权管理器 (AzMan) 与 ASP.NET 2.0](http://go.microsoft.com/fwlink/?LinkId=71303)。  
  
## <a name="see-also"></a>请参阅  
 [如何：将 ASP.NET 角色提供程序与服务一起使用](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)
