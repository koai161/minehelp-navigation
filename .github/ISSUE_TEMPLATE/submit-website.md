name: "提交新网站"
description: "为 MineHelp 导航提交一个新的 Minecraft 相关网站"
title: "[提交网站] 请填写网站名称"
labels: ["website-submission"]
body:
  - type: markdown
    attributes:
      value: |
        ## 欢迎提交新的 Minecraft 相关网站！
        
        请按照以下格式填写信息，确保所有字段都准确无误。
        
        **提交指南：**
        - 网站必须与 Minecraft 服务器相关（插件、教程、工具、资源或社区）
        - 请提供真实有效的网址
        - 图标类型：FA 使用 Font Awesome 图标名称，UP 使用图片 URL
        - 分类必须从预选项中选择
        
        **示例格式：**
        ```
        https://www.example.com
        FA
        fa-cube
        示例网站
        这是一个示例网站描述
        工具
        ```

  - type: input
    id: website-url
    attributes:
      label: "网站 URL"
      description: "请输入完整的网站地址（包含 http:// 或 https://）"
      placeholder: "https://www.example.com"
    validations:
      required: true

  - type: dropdown
    id: icon-type
    attributes:
      label: "图标类型"
      description: "请选择图标类型"
      options:
        - FA (Font Awesome 图标)
        - UP (上传图片 URL)
    validations:
      required: true

  - type: input
    id: icon-value
    attributes:
      label: "图标值"
      description: |
        如果选择 FA，请输入 Font Awesome 图标名称（如：fa-cube）
        如果选择 UP，请输入图片的完整 URL
      placeholder: "fa-cube 或 https://example.com/icon.png"
    validations:
      required: true

  - type: input
    id: website-name
    attributes:
      label: "网站名称"
      description: "请输入网站的名称"
      placeholder: "示例网站"
    validations:
      required: true

  - type: textarea
    id: description
    attributes:
      label: "网站描述"
      description: "请简要描述这个网站的功能和特点"
      placeholder: "这是一个提供Minecraft服务器帮助的示例网站"
    validations:
      required: true

  - type: dropdown
    id: category
    attributes:
      label: "网站分类"
      description: "请选择最适合的分类"
      options:
        - 插件
        - 教程
        - 工具
        - 资源
        - 社区
    validations:
      required: true

  - type: checkboxes
    id: terms
    attributes:
      label: "条款确认"
      description: "请确认您已阅读并同意以下条款"
      options:
        - label: "我确认提交的网站内容与Minecraft服务器相关"
          required: true
        - label: "我确认拥有提交该网站的权利或已获得授权"
          required: true
        - label: "我理解网站提交后需要经过审核才会显示"
          required: true
