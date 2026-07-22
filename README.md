## 中文使用说明

# 批量接口拼接与请求测试工具
# https://sumo166.github.io/Batch-API-Tester-User-Guide/
#使用说明

## 一、工具概述

本工具是一款纯前端轻量级接口批量测试工具，支持批量输入基础域名与接口路径，自动拼接生成完整 URL 并批量发起 GET 请求，以可视化表格展示响应结果，支持数据导出与多语言切换，适用于接口遍历、路径探测、批量可用性检测等场景。

## 二、核心功能

1. **自动 URL 拼接**：自动处理基础域名与接口路径的首尾斜杠，批量生成完整请求地址，避免格式错误
2. **可调并发请求**：支持 1-200 并发数自定义，默认 20 并发，可根据设备性能与网络环境灵活调整
3. **中英文双语切换**：界面全局支持中文 / 英文一键切换，适配不同使用习惯
4. **可排序分页表格**：结果按每页 10 条展示，支持序号、链接、响应长度、标题、内容多维度升序 / 降序排序
5. **结果一键导出**：支持将全部测试结果导出为 CSV 格式文件，兼容 Excel、WPS 等主流表格软件
6. **实时进度展示**：内置进度条与完成统计，实时显示请求进度与成功数量
7. **智能内容提取**：自动识别 HTML 页面标题、JSON 接口响应消息，自动截取响应内容预览

## 三、操作步骤

### 步骤 1：输入基础网址

在左侧「基础网址」输入框中，每行填写一个域名 / 根路径，示例：









```
https://cloud.ifxxy.com/hn
https://live.ifxxy.com/testTRTC/
```

### 步骤 2：输入接口路径

在右侧「接口路径」输入框中，每行填写一个待测试的接口路径，示例：









```
/academyInfo/academyIntroduction
/article/articleContent
/article/getArticleSubjects
```

### 步骤 3：设置并发数

在工具栏「并发数」输入框中填写 1-200 的整数：

- 默认值：20
- 建议值：普通网络环境推荐 10-50；网络条件好可适当调高；出现大量超时时请调低数值

### 步骤 4：开始批量请求

点击「开始批量请求」按钮，工具将自动拼接所有 URL 组合，按设置的并发数批量发起请求，实时展示进度与结果。

### 步骤 5：查看与导出结果

1. 表格浏览：点击表头可对对应列进行升序 / 降序排序；通过底部「上一页 / 下一页」翻页查看，每页固定显示 10 条数据
2. 导出数据：点击「下载表格」按钮，可将全部测试结果导出为 CSV 文件，文件自动按日期命名

### 步骤 6：语言切换

点击页面右上角「中文 / EN」按钮，可一键切换界面显示语言。

## 四、注意事项

1. 跨域限制

   ：受浏览器同源策略（CORS）限制，第三方域名的接口大概率无法直接获取完整响应内容，会显示请求失败。此为浏览器安全机制，非工具问题。

   - 解决方案：将工具部署在同域名服务器下，或使用 Python/Postman 等服务端工具执行批量请求

2. **超时设置**：单条请求默认超时时间为 10 秒，超时自动判定为失败

3. **内容预览**：表格中仅展示响应内容前 300 字符，完整内容需导出 CSV 或访问原链接查看

4. **合规提示**：请仅对自有授权的系统与接口使用本工具，禁止用于未授权的网站探测与攻击行为

------

## English User Guide

# Batch API Tester User Guide

## 1. Overview

This is a lightweight frontend tool for batch API testing. It supports batch input of base domains and API paths, automatically concatenates complete URLs, sends batch GET requests, and displays response results in a visual table. It supports data export and bilingual switching, suitable for API traversal, path detection, and batch availability check scenarios.

## 2. Core Features

1. **Automatic URL Concatenation**: Automatically handles trailing and leading slashes of base URLs and API paths to generate complete request addresses in batches without format errors
2. **Adjustable Concurrency**: Supports custom concurrency from 1 to 200, with a default of 20, adjustable according to device performance and network environment
3. **Bilingual Support**: One-click switch between Chinese and English for the entire interface
4. **Sortable Paginated Table**: Results are displayed 10 items per page, supporting ascending/descending sorting by index, URL, response length, title and content
5. **One-click Export**: Supports exporting all test results as CSV files, compatible with Excel, WPS and other mainstream spreadsheet software
6. **Real-time Progress**: Built-in progress bar and completion statistics to show request progress and success count in real time
7. **Smart Content Extraction**: Automatically identifies HTML page titles and JSON interface response messages, and generates response content previews

## 3. Operation Steps

### Step 1: Enter Base URLs

In the left "Base URLs" input box, enter one domain or root path per line. Example:









```
https://cloud.ifxxy.com/hn
https://live.ifxxy.com/testTRTC/
```

### Step 2: Enter API Paths

In the right "API Paths" input box, enter one API path to be tested per line. Example:









```
/academyInfo/academyIntroduction
/article/articleContent
/article/getArticleSubjects
```

### Step 3: Set Concurrency

Enter an integer between 1 and 200 in the "Concurrency" input box on the toolbar:

- Default value: 20
- Recommended value: 10-50 for normal network environments; increase appropriately for good network conditions; decrease if large numbers of timeouts occur

### Step 4: Start Batch Request

Click the "Start Batch Request" button. The tool will automatically concatenate all URL combinations, send batch requests according to the set concurrency, and display progress and results in real time.

### Step 5: View and Export Results

1. Table browsing: Click table headers to sort the corresponding column in ascending or descending order; use "Previous / Next" at the bottom to flip pages, with 10 items per page
2. Export data: Click the "Export CSV" button to export all test results as a CSV file, automatically named by date

### Step 6: Language Switch

Click the "中文 / EN" button in the upper right corner to switch the interface language with one click.

## 4. Notes

1. CORS Restriction

   : Limited by the browser's same-origin policy (CORS), APIs from third-party domains will mostly fail to return complete response content and show request failures. This is a browser security mechanism, not a tool defect.

   - Solution: Deploy the tool on the same domain server, or use server-side tools such as Python / Postman for batch requests

2. **Timeout Setting**: The default timeout for a single request is 10 seconds; requests will be automatically marked as failed after timeout

3. **Content Preview**: Only the first 300 characters of the response content are displayed in the table. For complete content, please export the CSV file or visit the original link

4. **Compliance Reminder**: Please use this tool only for authorized systems and interfaces. Unauthorized website detection and attack behaviors are prohibited.
