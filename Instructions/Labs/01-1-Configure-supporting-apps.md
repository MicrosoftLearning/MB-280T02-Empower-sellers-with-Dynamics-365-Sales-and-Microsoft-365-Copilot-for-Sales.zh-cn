---
lab:
  title: 实验室 1.1：配置支持应用程序
---

# 模块 1：配置 Dynamics 365 Sales

## 练习实验室 1.1：配置支持应用程序

## 场景

Contoso Coffee 销售人员报告指出，尽管 Dynamics 365 Sales 对提高卖家工作效率非常有用，但该应用程序在提高其日产量方面显得捉襟见肘。 他们对 IT 部门有以下要求：

-   销售人员希望在 CRM 中跟踪和管理与销售相关的电子邮件通信。
-   销售人员希望在 CRM 中存储与销售相关的文档（如产品知识文章、客户研究和市场趋势报告）。 他们希望能够直接从 Sales 应用访问、共享和管理这些文档。
-   销售人员在争取销售商机时希望与其他部门（如库存、订单履行和营销）进行协作。 他们希望这些其他部门能够在 Teams 聊天或频道中协作处理客户记录。
-   销售人员对 Dynamics 365 Sales 中的 Copilot 功能早有所闻，包括记录汇总，补写记录更改，准备会议，和撰写信件。 他们希望确保在其环境中启用 Copilot 功能，以便可以开始在应用中利用 AI 来提高工作效率。

在此实验室中，我们将启用并配置可帮助 CRM 组织满足这些销售人员要求的功能。

## 练习 1：配置电子邮件、SharePoint 和 OneDrive 集成

### 任务 1：配置电子邮件集成

1.  在 Web 浏览器中，导航到 [admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com/)。
2.  在屏幕左侧的站点导航中，选择“环境”****。
3.  选择“Sales 试用版”**** 环境将其打开。
4.  从顶部列出的命令中找到并选择“设置”****。
5.  选择电子邮件标题将其展开，然后选择“邮箱”****。
6.  打开 **MOD 管理员**的邮箱记录。
7.  按如下所示配置 **MOD 管理员邮箱**：
    -   **服务器配置文件**：Microsoft Exchange Online
    -   **传入电子邮件**：服务器端同步或电子邮件路由器
    -   **传出电子邮件**：服务器端同步或电子邮件路由器
    -   **约会、联系人和任务**：服务器端同步
8.  **保存**所做更改。 然后单击“批准电子邮件”****。 （**备注：** 必须先批准邮箱，然后才能发送和接收电子邮件。）
9.  系统会询问是否要批准主电子邮件。 选择“确定”****。
10. 单击“测试和启用邮箱”****。
11. 在“测试并启用”弹出屏幕上，确保如果此邮箱以前配置为与其他组织同步，则选中此选项会将其切换为与此组织同步。
12. 选择“确定”****。

**重要说明：** 测试完成后请勿离开此页面。 如果要在测试完成后处理任务 2，则可以打开新的选项卡或浏览器。

## 任务 2：启用基于服务器的 SharePoint 集成

在此任务中，将为 Dynamics 365 组织启用基于服务器的 SharePoint 集成。

1.  在 Web 浏览器中，导航到 [admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com/)。
2.  在屏幕左侧的站点导航中，选择“环境”****。
3.  打开一直使用的“Sales 试用版”**** 环境以将其打开。
4.  从顶部列出的命令中找到并选择“设置”****。
5.  在“集成”标题下，选择“文档管理设置”****。
6.  此时应看到“启用基于服务器的 SharePoint 集成”**** 选项。 （如果没有此选项，则 SharePoint 集成已启用，此时可以跳到步骤 11。）
    -   如果未配置 SharePoint 集成，请选择“启用基于服务器的 SharePoint 集成”****。
7.  在“启用基于服务器的 SharePoint 集成”屏幕中，单击“下一步”**** 按钮。
8.  为部署类型选择“联机”****，单击“下一步”**** 按钮。
9.  输入要使用的 SharePoint 站点的 URL。 （示例：https://”Orgname”.sharepoint.com），单击“下一步”**** 按钮。

    **备注：***可以通过选择屏幕左上角的“应用检查器图标”来查找 SharePoint URL。（类似于 3 x 3 正方形。）按住 Ctrl 键并选择 SharePoint。*

10. 验证站点后，单击“启用”**** 按钮。
11. 单击“文档管理设置”****。
12. 选择要为其启用文档管理的任何实体，例如潜在客户、客户、商机，然后单击“下一步”****。
    -   **重要说明**：如果计划在 Sales Insights 中配置电子邮件参与度，请选择“电子邮件实体”。
13. 在 SharePoint 站点 URL 字段中，输入在上一个任务中使用的 SharePoint 站点 URL。
14. 单击“下一步”按钮。
15. 单击“完成”**** 按钮即可完成设置。

### 任务 3：设置 OneDrive for Business 集成

在此任务中，将为 Dynamics CRM 组织设置 OneDrie 集成。 （自本课程发布起，Power Platform 管理中心不再提供文档管理设置。 需要从经典 Dynamics 365 设置区域配置 OneDrive for Business 集成。

1.  在 Web 浏览器中，导航到 [admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com/)。
2.  在屏幕左侧的站点导航中，选择“环境”****。
3.  打开一直使用的“Sales 试用版”**** 环境以将其打开。
4.  从顶部列出的命令中找到并选择“设置”****。
5.  在“集成”标题下，选择“文档管理设置”****。
6.  单击“启用 OneDrive for Business”**** 图标。
7.  选择“启用 OneDrive for Business”**** 复选框，然后单击“确定”****。
8.  屏幕刷新后，单击“OneDrive for Business 文件夹设置”****。
9.  接受默认文件夹名称，或输入选择的名称，然后单击“确定”****。

## 练习 2：配置 Teams 和 Copilot

### 任务 1：配置 Teams 集成

1.  如有必要，打开“销售中心”应用。
2.  使用左侧导航选择“销售”**** 区域（左下方）。
3.  从显示的菜单中，选择**应用设置**。
4.  在“常规设置”组下，选择“聊天和协作”****。
5.  将“启用 Dynamics 365 记录与 Microsoft Teams 频道的链接”**** 设置为“是”****。
6.  将“启用增强型 Microsoft Teams 集成”**** 设置为“是”****。 （可能需要选择 MOD 管理员帐户。 如果要求提供权限，请选择“接受”****。）
7.  在“在 Dynamics 365 内开启 Microsoft Teams 聊天”**** 下，选择“为所有 Dynamics 365 应用开启”****。
8.  选择“保存”按钮。  
    **重要说明**：保存更改可能需要几分钟时间。

### 任务 2：配置 Copilot

1.  确保位于“应用设置”**** 区域中。
2.  在“常规设置”组下，选择“Copilot”****。
3.  选中“将我们的最新预览版功能推出给所有人之前，先试用此功能”**** 旁边的复选框，以启用此功能。
4.  在“Copilot 功能”**** 下，更改“所有 Dynamics 365 Sales 应用”****，如下所示：
    -   **聊天**：打开
    -   **电子邮件（预览版）**：打开
5.  选择“保存”按钮。

