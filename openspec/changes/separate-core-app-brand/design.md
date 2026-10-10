---
type: task-plan
project: project-memory
workstream: core-app-brand
status: completed
updated_at: 2026-10-10
---

# Project Memory 分支整理与更名任务计划书

关联工作流：[[project-memory/工作流/分支整理与更名]]。

## 目标与范围

处理误推到 app 的四笔提交，核心与应用各自发布，统一品牌与仓库名称。保留原工作区的未提交功能和历史证据。核心 Skill 的调用标识不是项目名称，继续使用 project-memory-init。

## 方案与职责

main 是核心分发来源，无 desktop 或插件源码；app 以 desktop 为产品入口，根初始化资产仅用于开发/构建时携带的依赖，不在此独立演进核心协议。已有应用构建流程保持不变。将 047f35c、a746599、ba04eae、833b9b7 反序 revert，随后单独发布 app 品牌与分工。

历史工作记录恢复原字节，取消从 app 当前工作流入口导航到核心发布任务；旧记录引用的已回退产物以原提交 Git 树为准，不重新宣称为当前 app 规范。

应用设置名称前保存已有 userData 路径，再恢复该路径，避免品牌变化让项目列表看似丢失。npm 包标识保持 project-content-desktop 以保留已有目录兼容；用户看到的名称均为 Project Memory。

## 执行与验证

见 [tasks.md](tasks.md)，作为唯一执行清单。验证分支树、普通 clone、两条远端 ref、历史文件原字节、用户数据目录和 Electron 实机启动；不据此证明未发布功能或 Obsidian 插件验收。

## 未决项

无。旧 repo 地址可能依赖 GitHub 重定向；当前文档和 Git remote 使用新规范地址。
