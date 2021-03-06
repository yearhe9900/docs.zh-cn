---
title: "如何：创建绑定控件并设置显示数据的格式"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- data [Windows Forms], formatting
- bound controls [Windows Forms], creating
- bound controls [Windows Forms], formatting data
ms.assetid: d5a56228-899d-41d9-8af8-87b3f4ec2f94
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 6088048ed27b2021e297494275f4e80f7c0cb681
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
# <a name="how-to-create-a-bound-control-and-format-the-displayed-data"></a>如何：创建绑定控件并设置显示数据的格式
使用 Windows 窗体数据绑定，你可以设置使用数据绑定控件中显示的数据格式**格式设置和高级绑定**对话框。  
  
> [!NOTE]
>  显示的对话框和菜单命令可能会与“帮助”中的描述不同，具体取决于你现用的设置或版本。 若要更改设置，请在 **“工具”** 菜单上选择 **“导入和导出设置”** 。 有关详细信息，请参阅[在 Visual Studio 中自定义开发设置](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3)。  
  
### <a name="to-bind-a-control-and-format-the-displayed-data"></a>绑定控件并设置显示的数据的格式  
  
1.  连接到数据源。  
  
     有关详细信息，请参阅[连接到数据源](../../../docs/framework/data/adonet/connecting-to-a-data-source.md)。  
  
2.  在窗体中，选择控件，然后打开“属性”窗口。  
  
3.  展开**(DataBindings)**属性，然后在**（高级）**框中，单击省略号按钮 (![VisualStudioEllipsesButton 屏幕快照](../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) 以显示**格式设置和高级绑定**对话框中，具有该控件的属性的完整列表。  
  
4.  选择你想要将绑定，然后单击的属性**绑定**箭头。  
  
     此时将显示可用数据源的列表。  
  
5.  展开要绑定到的数据源，直到找到所需的单个数据元素。  
  
     例如，如果你正在绑定到数据集表中的列值，请展开该数据集的名称，然后展开表名以显示列名。  
  
6.  单击要绑定到的元素的名称。  
  
7.  在**格式化类型**框中，单击你想要应用于控件中显示的数据的格式。  
  
     在任何情况下，如果数据源包含 <xref:System.DBNull>，都可以指定控件中显示的值。 否则，选项会略有不同，具体取决于你选择的格式类型。 下表显示了格式类型和选项。  
  
    |格式类型|格式选项|  
    |-----------------|-----------------------|  
    |无格式|无选项。|  
    |Numeric|使用指定的小数位数**小数位数**up-down 控件。|  
    |货币|使用指定的小数位数**小数位数**up-down 控件。|  
    |日期时间|选择的日期和时间应显示方式选择其中一个中的项**类型**选择框。|  
    |科学记数法|使用指定的小数位数**小数位数**up-down 控件。|  
    |自定义|指定一个自定义格式字符串用法。<br /><br /> 有关详细信息，请参阅[格式化类型](../../../docs/standard/base-types/formatting-types.md)。 **注意：**自定义格式字符串不能保证可成功往返行程之间的数据源和绑定的控件。 请改为处理该绑定的 <xref:System.Windows.Forms.Binding.Parse> 或 <xref:System.Windows.Forms.Binding.Format> 事件，并在事件处理代码中应用自定义格式设置。|  
  
8.  单击**确定**关闭**格式设置和高级绑定**对话框并返回到属性窗口。  
  
## <a name="see-also"></a>请参阅  
 [如何：在 Windows 窗体上创建简单绑定的控件](../../../docs/framework/winforms/how-to-create-a-simple-bound-control-on-a-windows-form.md)  
 [Windows 窗体中的用户输入验证](../../../docs/framework/winforms/user-input-validation-in-windows-forms.md)  
 [Windows 窗体数据绑定](../../../docs/framework/winforms/windows-forms-data-binding.md)
