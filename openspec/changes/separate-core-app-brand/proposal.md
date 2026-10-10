# Project Memory 核心与应用分支分工

## Why

任务计划书的核心分发提交被误推到应用分支，项目品牌仍混用 Project Memory Init 和项目工作台。用户要求处理误推提交，明确 main 与 project-memory-app 的职责，并统一为 Project Memory。

## What Changes

- 用普通回退提交抵消 app 上四笔错误发布，不重写远端历史；保留工作记录作为历史证据。
- main 维护核心协议、初始化 Skill、模板和分发说明；app 维护 Electron 应用和应用验收，携带的初始化资产是运行依赖而非第二套核心发布。
- GitHub 仓库更名为 project-memory，当前链接与展示品牌同步；初始化动作的 Skill 标识保留兼容。
- 应用标题、侧栏和应用名称显示 Project Memory，保存原用户数据目录。

## Impact

修改当前品牌与导航、应用名称及两分支的发布状态，不发布未提交的行动工作台功能，不升级其他项目代码、不变更权限策略。
